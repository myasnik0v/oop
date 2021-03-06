## Виды критериев ОО-системы:
- **Метод и язык  (Method and Language)** - нотации, использующиеся для анализа, проектирования и программирования ПО.
- **Реализация (Implementation) и Среда (Environment)** - основные свойства инструментария
- **Библиотеки (Libraries)** - базовые библиотеки + механизмы создания новых

## Набор критериев для метода и языка
**Бесшовность (seamlessness)** - согласованность нотаций на этапе анализа, проектирования и программирования.

**Классы** - понятие класса должно быть центральной концепцией метода и языка.
Класс - элемент ПО, описывающий абстрактный тип данных и его реализацию.
Абстрактный тип данных - множество объектов, определяемое операциями, применимыми к этим объектам и их свойствам.

**Утверждения (Assertions)** - возможность поставлять класс и его компоненты вместе с утверждениями (предусловиями, постусловиями и инвариантами); включать инструментарий для получения документации из этих утверждения; осуществлять мониторинг во время выполнения программы.

**Классы как модули** - классы должны быть единственным видом модулей.

**Классы как типы** - понятие класса достаточно мощное, чтобы избежать любого другого механизма типизации.

**Вычисления, основанные на компонентах** - передача сообщения (вызов компонента) должна быть основным механизмом вычисления.

Пример: 
Повысить зарплату Васе на 10 рублей - vasya.raise(10);

**Сокрытие информации** - автор класса должен иметь возможность указать, что компонент доступен: всем, никому, избранным. 
Никаких глобальных переменных, классы обмениваются информацией исключительно через передачу сообщений и наследование.

**Обработка исключений (Exception handling)** - язык должен обеспечивать механизм восстановления в аварийных ситуациях.

**Статическая типизация** - гарантирует безопасность работы с объектами
- каждая сущность (entity) объявляется явным образом с указанием конкретного типа.
- каждый вызов компонента - вызов **доступного** компонента класса.
- присваивание и передача аргументов подчиняются правилам согласования, требующим совместимости исходного типа и целевого типа.

**Универсальность  (genericity)** 
Пример: List<int>, List<CustomClass>

**Ограниченная универсальность (Constrained genericity)** - Механизм универсальности должен поддерживать форму ограниченной универсальности.
Пример: List<ParentClass> => List<DerivedClass> && !List<int>

**Единичное наследование (single inheritance)**

**Множественное наследование (Multiple inheritance)**

**Переопределение (redefinition)** - должно быть возможным переопределить спецификацию, сигнатуру и реализацию наследованного компонента.

**Полиморфизм** - должна иметься возможность в период выполнения присоединять к сущности (переменной) объекты различных возможных типов под управлением наследования.

**Динамическое связывание** - вызов сущностью компонента всегда должен запускать тот компонент, который соответствует типу присоединенного объекта, а не типу сущности.

**Выяснение типа объекта в период выполнения** - возможность определять соответствует ли тип объекта статически заданному типу во время выполнения программы.

**Отложенные (deferred) свойства и классы** - возможность написания не полностью реализованного класса.
Пример: абстрактные методы и интерфейсыв C#

**Управление памятью (memory management) и сборка мусора (garbage collection)** - возможность надежного автоматического управления памятью и сборки мусора.


## Реализация и среда
**Автоматическое обновление (automatic update)** - при изменении метода f класса C мы должны быть уверены, что все потомки С, которые не переопределяли f, получат его новую версию.

**Быстрое обновление (fast update)** - время обновления должно определяться размером измененных компонентов, а не зависить от системы в целом.

**Живучесть (persistence)** - должен существовать механизм хранения и восстановления объекта вместе со всеми зависимыми объектами.

**Документация** - возможность автоматического получения документации о классах и системах.

**Быстрый просмотр (browsing)** - средства интерактивного просмотра должны давать возможность быстро и удобно прослеживать зависимости между классами и компонентами.



