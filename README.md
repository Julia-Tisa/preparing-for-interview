# Вопросы для подготовки к собеседованию (frontend developer)

### Описание
Этот файл будет дорабатываться. На каждый вопрос есть краткий ответ для собеседования и (оционально) более полный для понимания сути вопроса.

## Блок вопросов по HTML.

#### Что такое doctype? И для чего он используется?

**Кратко:** doctype используется для указания типа документа, чтобы браузер понял, в соответствии с каким стандартом ему парсить файл.

**Развернуто:** Можно добавить, что doctype идет первой строкой html/xml документа. В соответсвии с doctype браузер при парсинге будет определять, какие теги считаются валидными, а какие устаревшими.

#### Опишите базовую структуру HTML-страницы?

**Кратко:** В базовую структуру входит doctype, тег html, тег head, содержащий в себе мета-теги, и тег body, в котором располагается основной контент.

**Развернуто:** Можно добавить, что doctype идет первой строкой html/xml документа. Тег html является базовой оберткой страницы и содержит внутри себя теги head и body. Тег head является вспомогательным тегом, который содержит все необходимые данные о html/xml документе: заголвок, описание, сео-информация, подключение стилей, шрифтов и скриптов. Данные, содержащиеся в этом теге не отображаются на странице. Тег body же как раз содержит в себе разметку, которая будет отображена в браузере.

#### Что такое семантика? Какие семантичные тэги вы знаете?

**Кратко:** Семантика в контексте html - это использование правильных тегов, описывающих содержимое внутри себя. По семантичному тегу понятно, что за контент в нем содержится. Семантичных тегов достаточно много, например, к таковым относятся header (шапка сайта),  footer (подвал сайта), nav (навигационное меню), main (основной контент), h1-5 (заголовки), ul (списки) и другие.

**Развернуто:** Можно добавить, что семантичный тег - это тег, который носит смысловое объяснение, то есть обладает каким-то пояснением для своего предназначения.

#### Какая разница между тегами strong/em и b/i?

**Кратко:** Теги b/i просто меняют внешний вид элемента. strong/em тоже меняют внешний вид элемента, но также являются семантическими и используются для добавления *логического* выделения. При чтении страницы поисковыми роботами/скринридерами на выделенных словах будет сделан акцент.

#### Что такое валидация? И какие типы проверок HTML документа вы знаете?

**Кратко:** Валидация - это проверка документа на соответсвие установленным веб-стандратам и обнаружение ошибок. Эти стандарты называются спецификациями. Основные четыре типа проверок: проверка синтаксиса, проверка вложенности тегов, проверка DTD, проверка на наличие постонних тегов.

**Развернуто:** Можно добавить, что спецификации устанавливаются W3C и что работа валидатора заключается в следующем: определяется тип документа (который указывается с помощью doctype), затем проверяется html код на правильность и отсутсвие ошибок, а также проверяется правильность использования имен тегов и их вложенности.

#### Какой тэг использовать для того, что бы сверстать кнопку?

**Кратко:** В зависимости от того, какую кнопку мы хотим сделать. Простая кнопка: тег button. Кнопка отправки формы: тег input или button с типом сабмит. Кнопка - ссылка: тег a. И кнопка input с типом button (устаревший метод).

#### Что такое инлайновый стиль? Можно ли его переопределить?

**Кратко:** Инлайновый стиль - тот, который пишется в самом документе, в самом теге c помощью атрибута style. Переопределить можно, использовав дериктиву important у css-свойства.

#### Есть ли у HTML элементов свои дефолтные специфичные стили?

**Кратко:** Да, почти у всех, например, теги h будут разными по размеру, тег p обладает дефолтными margin, теги i и b добавят тексту свои специфичные стили. И они отличаются у разных браузеров.

#### Для какого тэга используется атрибут alt и зачем он нужен?

**Кратко:** Для тега img, нужен для того, чтобы, если картинка не отображается, вместо нее отображался текст. Атрибут является обязательным и улучшает доступность страницы.

#### Типы списков в HTML?

**Кратко:** ul-li: маркированный, ol-li: нумерованный, dl-dt-dd: список определений, списки можно вкладывать друг в друга.

#### Как семантически правильно сверстать картинку с подписью?

**Кратко:** Использовать два тега, figure, в который вкладывается картинка и тег figcaptuon для текста.

## Блок вопросов по CSS.

#### Что такое CSS? И для чего он используется?

**Кратко:** CSS - каскадные таблицы стилей. Используются для добавления стилей на страницу.

**Развернуто:** Можно добавить, что чистый html представляет из себя каркас страницы, в то время как css добавляет странице различные визуальные эффекты.

#### Варианты добавление CSS стилей на страницу?

**Кратко:** Всего их четыре: 
- В теге <head> через тег <link> и ссылку на документ.
- В теге <head> через тег <style> и описание стилей.
- Инлайново, в каждом теге, к которому относятся стили.
- Импорты непосредственно в файлах стилей.

#### Типы позиционирования в CSS?

**Кратко:** Всего 5 основных видов:
- Static - по дефолту, в основном потоке.
- Relative - относительно своего текущего положения, в основном потоке
- Absolute - относительно другого элемента, который не static или относительно окна браузера, формирует новый поток
- Fixed - относительно окна браузера, формирует новый поток
- Sticky - относительно своего родителя, в видимой области ведет себя как fixed, но при скролле уезжает вместе с родителем

#### Блочная модель CSS?

**Кратко:** Блочная модель помогает рассчитать, какое итоговое простраснство займет элемент на странице. Включает в себя сам элемент, внутренние и внешние отступы и границу элемента.

**Развернуто:** Итоговый размер считается так: ширина элемента + 2 * внешний отступ + 2 * внунтренний отступ + 2 * граница элемента. Если мы хотим, чтоб элемент занимал только ту ширину, которую мы ему задали, то необходимо установить box-sizing: border-box.

#### Что такое селектор? И какие селекторы существуют?

**Кратко:** Селектор - это часть css-правила, которая сообщает браузеру к какому элементу/ам будет применен стиль. Есть простые и составные селекторы. Простые, то есть один вариант селектора: по тегу, по классу, по id и тд. Составные, то есть несколько вариантов, объедененные пробелом или комбинатором: несколько тегов/классов, вложенный тег/класс, дочерний элемент, псевдоклассы и псевдоэлементы.

#### Что такое специфичность селектора? Как считать вес селектора?

**Кратко:** Специфичность - это то, благодаря чему браузер определяет, какие из css-свойств будут применены к элементу, потому что на одном элементе могут быть сразу несколько стилей. Четыре основных вида: инлайновый - 1000, id - 100, класс/аттрибут/псевдокласс - 10, элемент/псевдоэлемент - 1. Чтобы посчитать вес, надо сложить все селекторы, один тег - 1, два тега - 2, id и класс - 110 и тд.

#### Разница между Reset.css и Normalize.css?

**Кратко:** Reset.css - сбрасывает дефолтные стили элементов, Normalize.css - одинаково отображает их во всех браузерах.

#### Разница между margin и padding?

**Кратко:** margin - внешний отступ, пространство от границы блока до другого элеметна, padding - внутренний, пространство от границы блока до контента внутри него.

#### Разница между display: none и visibility: hidden?

**Кратко:** Оба используются для сокрытия элемента, но display: none полностью удаляет элемент со страницы и из основного потока, контент внутри него не доступен для поисковых роботов, получить доступ можно только через DOM-дерево, а visibility: hidden не вырывает элемент из основного потока, контент остается доступен для поисковых роботов.

#### Разница между блочным и строчным (инлайновым) элементами?

**Кратко:** Блочный элемент по умолчанию занимает всю доступную ширину экрана, а строчный родстраивается под контент.

**Развернуто:** Блочным элементам можно устанавливать размеры, а строчным нет, у блочных есть свойство margin и padding, а строчным margin сверху и снизу недоступен.

#### Разница между адаптивным (adaptive) и отзывчивым (responsive) дизайнами?

**Кратко:** Адаптивный дизайн - это несколько версий одного и того же сайта, которые загружаются пользователю, в зависимости от того, какое устройство он использует. Отзывчивый дизайн предполагает перестройку одного и того же макета в зависимости от ширины экрана.

## Блок вопросов по JavaScript.

#### Типы данных в JavaScript?

**Кратко:** Примитивные и ссылочные.

**Развернуто:** К примитивным относятся: строка, число, булевые значения, bigInt, Symbol, null, undefined. К ссылочным: объекты и массивы. Проверить тип можно оператором typeof, однако нужно учесть, что typeof null выдаст object. Такая ошибка сложилась исторически.

#### Разница между «==» и «===»?

**Кратко:** Двойное равно использует приведение типов, а тройное нет.

**Развернуто:** Двойное или нестрогое сравнение сравнивает только значение, а тройное или строгое - значения и типы:
1 == '1' // true
1 === '1' // false

#### Строгий режим (strict mode) в JavaScript?

**Кратко:** Синтаксис ES5, в ES6 стоит по умолчанию, то есть при транспайлинге файла скриптов добавляется с помощью бабеля автоматически. Превращает все предупреждения в ошибки, чтобы в проде код был более чистым.

**Развернуто:** Примеры ограничений, которые вводятся: нельзя удалить несуществующее свойство объекта, this равен undefined, запрещено дублирование параметров и другие.

#### Разница между function declaration и function expression?

**Кратко:** function declaration обявляется в общем потоке документа и ее можно использовать до объявления, а function expression присваивается переменной и ее нельзя использовать до объявляния. Происходит это потому, что при hoisting поднимаются объявления переменных и функций, но не присваивания.

#### Разница между null и undefined?

**Кратко:** null - можно и нужно присваивать явно, undefined - значение по умолчанию для непроинцилизированной переменной, функции, которая ничего не возвращает и несуществующего значения в объекте. Оба означают отсутствие значения.

#### Что такое Hoisting (поднятие)?

**Кратко:** Это поведение компилятора в JS. Поднимает функции, определенные с помощью function declaration и переменные, определенные с помощью var в глобальную область видимости. А let и const не всплывают.

**Развернуто:** Примеры ограничений, которые вводятся: нельзя удалить несуществующее свойство объекта, this равен undefined, запрещено дублирование параметров и другие.

#### Операторы «И» и «ИЛИ» (&& и ||)?

**Кратко:** «И» - находит первое ложное значение и выбрасывает его, либо, если такового нет, выбрасывает последнее истинное. «ИЛИ» - находит первое истинное и выбрасывает его. В es5 использовался для указания значения по умолчанию.

#### Типы таймеров в JavaScript?

**Кратко:** Их два: setTimeout - устанавливает через сколько должен сработать код, setInterval - устанавливает интервал, код будет срабатывать снова и снова.

**Развернуто:** Можно добавить, что оба таймера возвращают уникальный идентификатор, который можно присвоить в переменную, а в дальнейшем благодаря этому идентификатору, например, остановить выполнение через clear.

#### Что такое область видимости (Scope)?

**Кратко:** Это место из которого мы имеем доступ к функциям и переменным. В JS есть три области видимости: глобальная, функциональная и блочная.

#### Разница между «let», «const» и «var»?

**Кратко:** «var» - можно переопределять и переприсваивать значение, поднимается в функциональной области видимости, «let» - нельзя переопределить, но значение можно изменять, поднимается в блочной области видимости, «const» - нельзя переопределить и изменить значение, поднимается в блочной области видимости.

#### Что такое функции высшего порядка (Higher Order Functions)?

**Кратко:** Функции, которые принимают в качестве аргумента функцию или возвращают из себя функцию.

## Блок вопросов по JavaScript DOM.

#### Что такое DOM?

**Кратко:** Объектная модель документа - дерево из всех узлов html, который распарсил браузер. Благодаря DOM мы можем взаимодействовать с элементами с помощью JavaScript.

#### Что такое распространение события (Event Propagation)?

**Кратко:** Событие происходит не только на том элементе, на который повешен обработчик, оно распространяется по дереву вниз от глобального объекта window до целевого элемента, а потом всплывает опять по дереву ввуерх до глобального объекта.

#### Что такое делегирование событий (Event Delegation)?

**Кратко:** Делегирование - это прием, при котором вместо того, чтобы вешать много одинаковых обработчиков на все элементы, мы вешаем одно на общего предка.
