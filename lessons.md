# План занятий


## Занятия 1 – 2
### Лекции
Блок 1
### Семинары
Данный блок читается в отрыве от языка Java как такового. На уроках слушателям объясняются концепции процедурного программирования. Цель – научить мыслить в предметных терминах.


## Занятие 3
### Лекция
Блок 2 (начало)
### Семинар
Разбор задач:
+ Даны два целых числа: `n` и `p` и последовательность из `n` дробных. Вычислить [`Lp`-норму](https://en.wikipedia.org/wiki/Lp_space) вектора. [Пример кода](https://pastebin.com/57CwMcLW).
+ Дано число целое положительное число `n`. Вывести матрицу размера `n` на `n`, заполненную по нижеприведенным формулам. [Пример кода](https://pastebin.com/9JuHmcfJ) (для последнего пункта):
  + `|i - j|`
  + `n - |i-j|`
  + `max(i, j)`
  + `min(i, j)`
  + `k - max(|i - k|, |j - k|)`, где `k = (n - 1) / 2`


## Занятие 4
### Лекция
Блок 2 (продолжение)
### Семинар
+ Демонстрация задачи на сравнение `double`: пересекаются ли две прямые в форме `y = ax + b`.
+ Демонстрация класса `Math` и задачи на него: например, получение длины третьей стороны в треугольнике по теореме косинусов (пример функции `cos`). [Пример кода](https://pastebin.com/VerBRQ74).
+ Немного про геометрию: программа для вычисления скалярного и векторного произведений. [Пример кода](https://pastebin.com/jL1PmXRb).
+ Идея о вычислении площади треугольника (модуль векторного произведение направляющих векторов, разделенный на два). [Пример кода](https://pastebin.com/UCjLXvmV). Использование функции `Math.toRadians()`. Формулировка задачи о нахождении площади выпуклого многоугольника (без решения).
+ Демонстрация битовых операторов:
  + Получение `i`-ого бита числа. [Пример кода](https://pastebin.com/kh4gCyvx).
  + Разница между операторами `>>` и `>>>`.
  + Получение всех битов числа. [Пример кода](https://pastebin.com/Jxbtzs9c). Случай с отрицательными числами.
  + Операторы `~`, `&`, `|` (простые примеры)
  + Два способа нахождения количества единичных битов: циклом и функцией класса `Integer`. [Пример кода](https://pastebin.com/mwEkxMVg).
  + Показать другие полезные методы класса `Integer`: `highestOneBit`, `lowestOneBit`, `numberOfLeadingZeroes`, `numberOfTrailingZeroes`, и другие.


## Занятие 5
### Лекция
Блок 2 (окончание)
### Семинар
+ Демонстрация контеста, механизм отправки решений.
+ Задача: определить, образует ли последовательность точек выпуклый многоугольник, ориентированный кверху (_многоугольник, ориентированный кверху_ есть –_многоугольник, последовательность вершин которого задана в порядке обхода против часовой стрелки_).
  + Написать функции `dotProduct` и `crossProduct`.
  + Проитерироваться по смежным тройкам вершин `p1`, `p2`, `p3`. Построить векторы `v1 = p1 -> p2` и `v2 = p2 -> p3`
  + Рассмотреть полученные векторы, и проверить, образуют ли они левый поворот. Для этого, нужно проверить знак векторного произведения `[v1 x v2]`.
  + [Пример кода](https://pastebin.com/RBm5aBjZ).
+ Задача (сформулировать условие и идею решения, без кода решения): задан выпуклый многоугольник в виде последовательности точек в порядке обхода по или против часовой стрелки, необходимо найти его площадь
  + Находим центр масс всех точек
  + Итерируемся по всем парам смежных точек (всего `n` пар, где `n` – количество точек) и вычисляем площадь треугольника, образованного этой парой точек и центром.
  + Складываем все площади.
  + [Пример кода](https://pastebin.com/u5aqMrmn) (только для преподавателей, в целях ознакомления). Заметьте, код похож на решение прошлой задачи.
+ Задача на `BigDecimal`: извлечение квадратного корня [алгоритмом Герона](https://en.wikipedia.org/wiki/Methods_of_computing_square_roots#Babylonian_method). [Пример кода](https://pastebin.com/j3TZgfGc).
+ Задача на `String` и `StringBuilder`: отфильтровать цифры и латинские буквы. [Пример кода](https://pastebin.com/hx9RMSDC).
+ Задача на рекурсию и `BigInteger`: вычисление факториала. [Пример кода](https://pastebin.com/kkntMazU).


## Занятие 6
### Лекция
Блок 3
### Семинар
+ Процесс отладки в `IntelliJ IDEA`:
  + `Breakpoint`: мотивация, как установить
  + Обзор локальных переменных при активном брейкпоинте
  + Шаги при активном брейкпоинте: `step into`, `step over`, `step out`
  + Вычисление выражения (`evaluate expression`) при активном брейкпоинте
  + `Conditional Breakpoint`: мотивация, как установить
  + Обзор всех breakpoints в проекте (`view all breakpoints`)
  + `Stack trace`: идея, можно показать на какой-нибудь рекурсивной функции
  + Получение `thread dump`
+ Установка [сторонней библиотеки](https://commons.apache.org/) в проект, мотивация существования `jar`-архива. Показать устройство `jar`-файлов.
+ Написание и экспорт `javadocs`
+ Задача на бинпоиск: найти корень уравнения `ln(ln(1/x)) = 0`. [Пример кода](https://pastebin.com/Fp5YWqv7). Другой пример – с функцией `-x^4 + 3`. [Пример кода](https://pastebin.com/WE1VFUrH).


## Занятие 7
### Лекция
Блок 4
### Семинар
+ Класс `Scatter`, реализующий динамический набор взвешенных точек в `2D`-пространстве.
  + Вспомогательный класс `Coordinates`. Концепция иммутабельного класса.
  + Мотивация использования `ArrayList`. Методы `add`, `remove`. Концепция `accessor`’ов: `get` и `set`.
  + Реализация методов `center`, `add`, `remove`, `get`, `set` и `size`.
  + Пример кода: [`Class Scatter`](https://pastebin.com/QSJaPz1g), [`Class Coordinates`](https://pastebin.com/gGd3Jwqn)
+ Класс, реализующий игру крестики-нолики
  + Мотивация использования `Optional`. Треугольные скобки: концепт полиморфизма просто и в двух словах. Методы `isPresent`, `isEmpty`, `get`. Статические фабричные методы `empty` и `of`.
  + Метод `values` у перечисления
  + Пример кода: [`class Main`](https://pastebin.com/CRE6Z63w), [`class TicTacToe`](https://pastebin.com/PXhbx1tS), [`enum Player`](https://pastebin.com/RYb854wH), [`enum Status`](https://pastebin.com/DfMk9vy6)


## Занятие 8
### Лекция
Блок 5
### Семинар
+ Окончание разбора примеров с прошлого семинара (если не успелось на прошлом семинаре)
+ Класс `ArrayList` (если не было рассказано на прошлом семинаре)
  + Классы-обертки примитивных типов: `Integer`, `Long`, `Float`, `Double`, `Boolean`:
  + Мотивация (например, использование вместе с `ArrayList`)
  + Boxing (почему вместо `arr.add(Integer.valueOf(123))` можно написать `arr.add(4)`)
  + Простые примеры использования класса `ArrayList`. Семь основных методов `ArrayList`: `add`, `remove`, `get`, `set`, `size`, `isEmpty`, `clear`
+ Класс `Object`:
  + Методы `toString`, `equals`, `hashCode`. Разбор `equals` и `hashCode` на примере [простой статьи](https://habr.com/ru/post/168195/).
  + Пример переопределения этих методов в классе `ComplexNumber`. [Пример кода](https://pastebin.com/cHa2uudp).


## Занятие 9
### Лекция
Блок 6 (начало)
### Семинар
+ Демонстрация нового блока контеста.
+ Разбор материалов предыдущей лекции: наследование, абстрактные классы и интерфейсы.
+ Еще одна игра: что-нибудь клеточное, наподобие шахмат и шашек. Например, реализация нескольких [`tafl`](https://en.wikipedia.org/wiki/Tafl_games) игр. [Правила игры](http://tafl.cyningstan.com/page/20/a-rule-book-for-hnefatafl). Описание задачи и код проекта можно найти в [репозитории](https://github.com/Costello1329/cell-based-table-games). При разборе кода, акцент делается на:
  + Архитектура решения: диаграмма классов и пояснения почему она должна быть такая.
  + `Record`’ы.
  + Наследования, абстрактность классов: мотивация. Пояснения использования `public` / `protected` / `private` / `abstract`.
  + На этом уроке рассказывается только пакет `core`, остальное будет на следующих уроках, использование исключений, дженериков и коллекций пока что опускается.


## Занятие 10
### Лекция
Блок 6 (окончание), блок 7 (начало)
### Семинар
+ Продолжение написания игровых проектов с предыдущего семинара. Реализация модулей `tafl` и `tictactoe`.
+ Из нового с точки зрения элементов языка:
  + Исключения для валидации `move`’ов.
  + Использование дженерика для параматризации `AbstractField` в `AbstractEngine` и `FieldFactory`. Параметризация `Move` с целью поддержки разных типов игр.
  + Пример: `class TaflEngine extends AbstractEngine<TaflField, TaflMove>`.
+ Попутно поддерживаются крестики-нолики (модуль `tictactoe`). Мотивация параметризации `Move`.
+ Как передавать настройки игр до уровня `FieldFactory` и `Engine` (первое – на примере `TicTacToe`, второе – на примере разных настроек для `Tafl`’а, реализованных в виде рекорда `TaflSettings`).


## Занятие 11
### Лекция
Блок 7 (окончание), блок 8 (начало)
### Семинар
+ Завершение рассказа материала с прошлого семинара. Модуль `talf` получился объемным, поэтому до него не вышло дойти на предыдущей паре.


## Занятие 12
### Лекция
Блок 8 (окончание)
### Семинар
+ Завершение написания проект по `tafl`’ам.
+ Задача на `Map` и `Set`: книга синонимов. [Условие и пример кода](https://pastebin.com/AR3hBYrL).
+ Концепция решения задач контеста `3.2.*` (три задачи на коллекции). Для каждой задачи рассказывается алгоритм решения и рисуются пояснительные картинки. Какие структуры данных (коллекции) необходимо применять в каждой задаче и почему. Методы этих коллекций, необходимые для решения задачи.


## Занятие 13
### Лекция
Блок 9
### Семинар
+ Реализация методов, схожих с `compose`, `andThen`, `identity`. [Пример кода](https://pastebin.com/GGyQaTRh).
+ Имплементация [индикатор-функции из математики](https://ru.wikipedia.org/wiki/%D0%98%D0%BD%D0%B4%D0%B8%D0%BA%D0%B0%D1%82%D0%BE%D1%80_(%D0%BC%D0%B0%D1%82%D0%B5%D0%BC%D0%B0%D1%82%D0%B8%D0%BA%D0%B0)). [Пример кода](https://pastebin.com/2b7C11Ew).
+ Операции над математическими функциями. [Пример кода](https://pastebin.com/VQ9HQeSZ).
+ Численное дифференцирование функций с использованием `DoubleUnaryOperator`. [Пример кода](https://pastebin.com/SEQqPVRi).
+ Способы интегрирования различных функций с использованием `DoubleUnaryOperator`:
  + Метод трапеций. [Пример кода](https://pastebin.com/NNpFixVW).
  + [Рандомизированный способ (он же – геометрический метод Монте Карло)](https://en.wikipedia.org/wiki/Monte_Carlo_method). Демонстрация класса SplittableRandom. [Пример кода](https://pastebin.com/Q949fiwN)


## Занятие 14
### Лекция
Блок 10
### Семинар
+ Класс `Collectors`. Gримеры разных коллекторов:
  + `toList`, `toUnmodifiableList`, `toSet`, `toUnmodifiableSet`, `toCollection`
  + `toMap`, `toUnmodifiableMap`: три варианта.
    + Построение отображения `имя студента <-> возраст студента` с учетом наличия студентов с одинаковым именем: [пример кода](https://pastebin.com/H9LC1Uzd)
  + `joining`
  + `summingInt`, `averagingInt`, `counting`
  + `summarizingInt`.
    + Получение статистики по студентам: [пример кода](https://pastebin.com/ZVTEA39g).
  + `maxBy`, `minBy`
  + `mapping`, `flatMapping`
  + `groupingBy`, `partitioningBy`.
    + Разбиение студентов по группам: [пример кода](https://pastebin.com/ny5nMGXK).
    + Разделение Ивановых и не-Ивановых: [пример кода](https://pastebin.com/zjS6MS14).
  + `reducing`
  + `collectingAndThen`
  + `teeing`.
    + Вычисление средней оценки студентов: [пример кода](https://pastebin.com/Ln6iw8qv).
+ Использование `reduce` для итерирования по смежным парам объектов в стриме. Например, дан стрим точек и нужно вычислить длину пути из них. [Пример кода](https://pastebin.com/TDbsDSs9).
+ Демонстрация всего необходимого для решения задачи `3.4.3` по-отдельности. В том числе и `regex`. [Пример кода](https://pastebin.com/y3GSg8Nj) (только для преподавателей, в целях ознакомления)


## Занятие 15
### Лекция
Блок 11
### Семинар
Использование Reflection API и аннотаций для написания кастомной библиотеки тестирования `java-testlib`, основаной на принципе инстанцирования схожих классов, применении к ним схожих операций и сравнения. Пример кода и описание проекта можно найти в [репозитории](https://github.com/Costello1329/java-testlib).
+ Мотивация проекта, разработка архитектуры проекта.
+ Разбор пакета `core` (пока без `ClassLoader`'ов, так как они требуют класс `Path`, про который рассказывается на следующей лекции).
+ Написание демонстрационного проекта, содержащего тесты к упрощенной версии задачи про геометрию из контеста. Пример кода можно найти в [репозитории](https://github.com/Costello1329/simple-geometry-tests-demo). Написание решений для проверки и тестирования (директории `/reference` и `/solution` в репозитории).

## Занятие 16
### Лекция
Блок 12
### Семинар
+ Разбор пакета `components`.
+ Завершение разбора проекта `java-testlib`. Добавление классов `ClassLoader` и `UrlClassLoader`. Использование последнего для загрузки классов `jar`-архивов с проверяющим и тестируемым решениями. Передача загруженных классов тестеру.
+ Написание упрощенных скриптов сборки `build-testlib.sh` и `make-jars.sh`.
+ Демонстрация работоспособности проекта. Передача тестеру заведомо неверных решений для демонстрации функционала тестера.


## Занятие 17
### Лекция
Блок 13
### Семинар
+ Файловая система в `UNIX`:
  + Типы файлов.
  + Символические ссылки, пример с зацикленностью цепочки символических ссылок.
  + Права доступа к файлам.
  + Пользователи и группы.
  + Информация о файле: размер, дата создания, дата модификации, итд.
+ Разбор утилит `ls` и `tree`, демонстрация основных флагов.
+ Написание утилиты, схожей с командой `tree`. Описание задачи и пример кода можно найти в [репозитории](https://github.com/Costello1329/tree).


## Занятие 18
### Лекция
Блок 14
### Семинар
+ Пакет `com.sun.net.httpserver`.
+ Написание серверного приложения, взаимодействующего с файловой системой. [Пример кода](https://pastebin.com/6MDebSmb).
+ Тестирование написанного приложения как в окне браузера, так и в клиенте **Postman**.

