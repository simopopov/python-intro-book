#                                   Настройване на текстов редактор за работа с Python 

## 1.Въведение
Популярен избор за хората, които пишат на Python е текстовия редактор Sublime Text 3 (ST3).  Той не ползва много ресурси, може да се ползва на различни операционни системи и се ползва с репутация на изключително бърз, лесен за ползване, настройване и получава голяма поддръжка сред програмистите. Накратко той е един изключителен редактор, дори след първоначалната си инсталация, но истинската му сила е чрез добавяне на допълнителни функционалности използвайки Package Control (Мениджъра на пакети) и създаването на индивидуални настройки. 

## 2. Функционалности

2.1 Split Layouts (Разделен екран) е функционалност, която ви позволява да гледате едновременно няколко файла и да ги подредите по избран от вас начин. Това е особено полезно когато работите по визуалната част (front end)  и програмната логика (back end) при разработката на уеб продукти или писанаето на тестове за нова функционалност.

2.2 Използване на табове подовно на Chrome за навигация.

2.3 Автоматично зареждане на отворените файлове от сесията, преди да затворите редактора си. 

2.4 Изволзването на Code Snippets повишава цялата продуктивност. Това е възможността, да отделите често използвано парче код като фрагмент, който може да извикате с ключова дума. Има колекция от фрагменти, която може да ползвате по подразбиране. За да ги видите натиснете lorem и после натиснете клавиша Tab.Би трябвало да видите известния параграф, за тестове lorem ipsum.

# Инсталиране на Package Control

За да се възползваме напълно от всички възможности и да можем да разширим нашия текстов редактор Sublime трябва да инсталираме Мениджъра на пакети (Package Control). След като го инсталираме ще можем да имаме достъп до различни пакети, които от своя страна можем да инсталираме, премахваме или обновяваме. Можете да разгледате различните пакети и какво включва всеки от тях на този [сайт](https://packagecontrol.io/).

## 1.Инсталиране на Мениджъра на пакети (Package Control)
За да инсталираме Мениджъра на пакети, трябва да влезем в конзолата на Sublime, а това става като изберем View > Show Console ,за да я отворим. Отиваме на [адреса](https://packagecontrol.io/installation#st3) и копираме кода, който е показан там :
```python
import urllib.request,os,hashlib; h = '6f4c264a24d933ce70df5dedcf1dcaee' + 'ebe013ee18cced0ef93d5f746d80ef60'; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); urllib.request.install_opener( urllib.request.build_opener( urllib.request.ProxyHandler()) ); by = urllib.request.urlopen( 'http://packagecontrol.io/' + pf.replace(' ', '%20')).read(); dh = hashlib.sha256(by).hexdigest(); print('Error validating download (got %s instead of %s), please try manual install' % (dh, h)) if dh != h else open(os.path.join( ipp, pf), 'wb' ).write(by) 
```

Пействаме го в конзолата, натискаме клавиша Enter и чакаме инсталацията да завърши след което рестартираме нашия текстов редактор. 

## 2. Инсталиране на пакети чрез Мениджъра на пакети (Package Control)
Вече можете инсталирате всеки от пакетите, които видяхте по-рано. За да го направите използвайте клавишната комбинация Ctrl+Shift+P. След това напишете install докато се появи Package Control: Install Package. Натиснете клавиша Enter и може да изберете любимите си пакети, за да бъдат инсталирани. 

Списък на някои команди:
  
* List Packages -показва списък на инсталираните пакети.
  
* Remove Package <име_пакет> премахва пакета от редактора.
  
* Upgrade Package <име_пакет> обновява пакет за редактора.

# Пакети:
Списък на често използвани пакети, за работа с Python:

## 1. SideBarEnhancements 
Пакета съдържа разширение, с което можем да виждаме файловете и папките в работната директория. Чрез него може да създаваме или изтриване файлове.Струва си да отбележим, че ако използвате опцията изтриване, файла отива във вашео кошче, и ако сте го изтрили по погрешка и не ползвате version control (система за контрол на версиите) може да си го възстановите от там.

## 2. Anaconda 
Това е най-пълния пакет за работа с Python, който съдържа всичко от което се нуждаете, за да работите с Python. С него, ще се чувствате сякаш работите с IDE(integrated software enviroment):

* Autocompletion - автоматичното довършване на код, което работи без проблем след инсталация и позволява да бъде конфицурирано по ваш избор използвайки настройки.

* Code linting - който използва PyLint или PyFlakes с PEP8 (АКо не сте чували какво е PEP8, това е набор от правила приети за конвенция при писането на Python код). АКо все пак искате да сложите собствен пакет, който да ви помогне с налагането на правила на синтаксиса може да изключите тази опция създавайки потребителски настройки за пакета:
Sublime > Preferences > Package Settings > Anaconda > Settings - User: {"anaconda_linting": false}

* Goto Definitions -намира и показва дефинирането на променлива, фукнция или клас в текущия проект.  

* Find Usage - бързо търсене на среащането на променлива, функция или клас, използвани в определен файл. 

* Show Documentation - показвазване на документацията, като извлиза така наречените docstring написани за функция или клас,ако все пак сте си направили труда да напишете такива.


## 3. Djaneiro
Djaneiro е пакет за работа с Django. Това е най-популярния избор на уеб фреймуърк за работа с Python. Пакета поддържа използването на темплейти, използването на кодови фрагменти и отбелязване и разпознаване на ключови думи. Използването на кодови фрагменти спестяват доста време, а за допълнителна бързина при разработката с използването на Django blocks с натискането на няколко клавиша имаме достъп до темплейти, модели, форми и вю-та. 

## 4.requirementstxt
Ако не сте чували какво е requirements.txt това е текстов файл, който се генерира автоматично и ни показва всички включени допълнително библиотеки и тяхната версия, за да можем, да подкараме даден проект. Този пакет ни позвалява да ползваме автоматично довършване и разпознаване на синтаксиса, както и система за контрол на версиите. 

## 5. GitGutter
GitGutter показва малки икони в началото на вски ред, които ни показват дали реда е бил добавен, променен или изтрит спрямо последната качена версия в git. 

# Използването на клавишни комбинации: 

* Ctrl+P - отваряне на файл по име; 
* Ctrl+G - отиване на определен ред във файла
* Ctrl + F - търсене в текущия файл
* Ctrl + Shift+ K - Изтриване на текущия ред
* Ctrl + (ляв бутон намишката) Позволява създаването и използването на много курсори едновременно, чрез които можем да редактираме едновременно на различни места в документа.

# Какво е PEP8 - това е конвенцията за писане на код в Python:

* Индентация с 4 интервала за всяко ниво на влагане
* Максимално 79 символа на ред!
* Всеки блок код (тяло на if, тяло на функция, и т.н.) се определя с индентацията му спрямо обгръщащия го блок.
* Всеки блок код започва само след двуеточие в края на предишния ред.
* Блокът свършва, когато се върнете към предишната индентация.
* 4 празни места = нов блок. 
* snake_case за имена на функции, методи, променливи, параметри
* имена на "константи" в SCREAMING_SNAKE_CASE
* _turn_around, __seriously_turn_around за "частни"("private")
* използване на запазени думи? 1 подчертавка след името: range_, но..по-добре използвайте друго име
* интервал след "," при изброяване и ":" при конструиране на dict: [1, 2, 3] {1: 2, 2: 4, 13: 26}
* без интервали след (, [, { и след ), ], }: func(1, 2, 3), [5, 6, 7, 8]
* по един интервал около оператори: a == b; 3 > 4; "abra" + "-" + "kadabra"
* изключение: може да липсват около оператори с по-висок приоритет в подходящ конеткст: 42 - 6*9
* без интервали, когато задаваме стойност по подразбиране: def my_func(a, b, option=True): ..
* и при подаване на именовани параметри при извикване my_func(option=False, b=13, a=666)
* без скоби около условията на while/for/if/elif/return: while True: ...

# Типове от данни в Python:

* Всяка стойност е обект и има клас, включително функциите
* Всичко в python е обект, включително функциите и типовете!
* Можем да проверим типа на един обект с функцията type()

## 1. int

* Цели числа, положителни и отрицателни
* Стандартни операции: +, -, *, /, %, ** (степенуване)
* Без максимален размер
* Може да пробваме 2 ** 4 ** 8

## 2. float

* Числа с плаваща запетая(точка?) 3.1452
* По всичко друго приличат на целите числа

## 3. complex

* Още един вид число - комплексно
* Пишат се така: (2+3j)
* Да, j, а не i

## 4. str

* Текстови низове с произволна дължина
* Единични или двойни кавички
* Unicode навсякъде!!!!
* Поддържат \n, \t и пр.

## 5. bool

* * True и False
* NB! главните букви

## 6. None

* Като null в другите езици.
* Когато една функция не върне нищо, тя връща None. 


# Контролни структури в Python

## 1. if .. elif .. else
```python
if a == 5:
    print("a is five")
elif a == 3 and not b == 2:
    print("a is three, but b is not two")
else:
    print("a is something else or b is two")
 ```

Точно каквото очаквахте.
Не слагайте скоби около условията.
and, or и not
НЕ &&, ||, !

## 2. while
```python
while a > 5:
    a -= 1
    print("a is {}".format(a))
```

## 3.for
```python
primes = [3, 5, 7, 11]
for e in primes:
    print(e ** 2) # 9 25 49 121

people = {'bob': 25, 'john': 22, 'mitt': 56}
for name, age in people.items():
    print("{} is {} years old".format(name, age))
    # bob is 25 years old
    # john is 22 years old
    # ...
```
* for е като foreach в другите езици 


## 4.break и continue

* Работят както очаквате въвfor и while.
* Афектират само най-вътрешния цикъл.


## Функции
```python
def say_hello(name, from):
    return "Hello… It's me…"
```

* Функцията приема аргументи
* Функцията може да върне нещо с return, а ако няма return връща None
* Не се описват типовете на аргументите, нито типа на резултата

* Променлив брой аргументи
```python
def varfunc(some_arg, *args, **kwargs):
    #...

varfunc('hello', 1, 2, 3, name='Bob', age=12)
    # some_arg == 'hello'
    # args = (1, 2, 3)
    # kwargs = {'name': 'Bob', 'age': 12}
```
* Функциите могат да приемат произволен брой аргументи
* Позиционните аргументи (тези без име) отиват в args, което е tuple от агументи
*  Именуваните аргументи отиват в kwargs, което е dict от имена на аргументи и съответните им стойности 


# Структури от данни/ Видове колекции в Python

* В Python всички колекции са итерируеми (iterable)
* Един итерируем обект може да бъде обхождан последователно (поне веднъж)
* Някои могат да бъдат обхождани многократно или непоследователно

## 1. Списък - list (list (a.k.a. array, масив) = подредена последователност от стойности)

* Характеристика на списъците:
* Списък = list = масив = array
* Mutable и без фиксирана дължина
* Бързи за търсене по индекс, бавни за търсене по стойност
* Гарантиран ред 
* Не е нужно елементите да са от еднакъв тип (т.е. списъците са хетерогенни)


### методи на списъци

* .index(element) - Индекса на първото срещане на element в списъка или гърми с ValueError
* .count(element) - Броят срещания на element в списъка
* .append(element) - Добавя element в края на списъка
* .extend(elements) - Добавя елементите на elements в списъка (като + ама по-бързо)
* .sort() - Сортиране на списъка


## 2. Речник - dict (dict = ключове/имена, зад които стоят стойности (без подредба))

* Речник = dict = hashtable = associative array
* Реда не е гарантиран
* Асоциира ключ със стойност

* Чрез наименовани параметри към конструктора (не питайте):
```python
>>> dict(france="Paris", italy="Rome")
{'italy': 'Rome', 'france': 'Paris'}
```
* Чрез списък от двойки
```python
>>> dict([('One', 'I'), ('Two', 'II')])
{'Two': 'II', 'One': 'I'}
```
* Чрез списък от ключове и стойност по подразбиране
```python
>>> dict.fromkeys([1, 2, 3], 'Unknown')
{1: 'Unknown', 2: 'Unknown', 3: 'Unknown'}
```

## 3. Tuple - tuple a.k.a кортеж (tuple = непроменяема по състав подредена последователност от обекти (~списък, но не съвсем))

* tuple = кортеж = n-торка
* Immutable
* Гарантиран ред
* Ползват за да подадете или върнете няколко стойности от функция, когато специален клас би бил твърде много
* Tuple от един елемент - със запетайка на края: ('Your friends will never love you.',)
* Може и без скобите

* последователността от елементи в кортежа не може да се променя, самите елементи може да изменят вътрешната си структура

## 4. Множество - set (set = стойности без повтаряне и без подредба (множество в математическия смисъл))
* set = множество = списък без повтарящи се елементи
* Редът не е гарантиран
* Нямаме пряк достъп до конкретен елемент
* Можем да проверяваме за принадлежност
* Можем да обхождаме всичките(след малко ще видим как)

* !!! ВАЖНО {} не е празния set! {} е празен речник, по простата причина, речниците са доста по-често използвана структура от множестватаю

## 5. Comprehensions
* Изрази, които генерират колекции
* Елегантен заместител на map и/или filter
* Колекциите могат да са динамични

* [израз for променлива in поредица if условие]
* Примери:
```python
>>> [x * x for x in range(0, 10)]
[0, 1, 4, 9, 16, 25, 36, 49, 64, 81]

>>> [(x, y) for x in [1,2,3] for y in [3,1,4] if x != y]
[(1, 3), (1, 4), (2, 3), (2, 1), (2, 4), (3, 1), (3, 4)]
```
## 6. Разрязване на списъци/ кортежи
```python
a[start:end] # всички елементи на списъка стартирайки от start до  end-1
a[start:]    # Всички елементи на списъка след start 
a[:end]      # всички елементи на списъка от началото до end-1
a[:]         # Копие на целия списък
```
При разрязване на списъци можем да ползваме и стъпки:
```python
a[start:end:step] # всички елементи на списъка стартирайки от start до  end-1 през step
```
ВАЖНО !!! Ключово е да запомним, че :end е първият индекс, който не се вклява в отрязъка. Така, че разликата end -start е броя на върнатите елементи.(по поразбиране стъпката е 1)

Друга особеност е, че start или end могат да бъдат отрицателни числа, което означава че броенето започва от края на списъка вместо от началото, така, че: 
```python
a[-1]    # връща последния елемент в списъка
a[-2:]   # връща последните 2 елемента от списъка
a[:-2]   # връща всички елементи от списъка, без позледните два
```
Подобно, стъпката пак може да бъде отрицателно число:
```python
a[::-1]    # всички елементи от списъка от края до началото, списъка в обратен ред
a[1::-1]   # първите два елелемнта в обратен ред
a[:-3:-1]  # последните два елемента в обратен ред
a[-3::-1]  # всичко, без последните два елелемента, в обратен ред
```
## 7. Функции от по-висок ред: 
* map(function, iterable) създава колекция от резултатите от прилагането на function върху всеки елемент от iterable
* filter(function, iterable) създава колекция само с елементите, за които function върне True
* reduce(function, iterable) вика function с елементите на колекцията, докато сведе всичко до една стойност (във functools вж.тук)
* all(iterable) всички елементи се оценяват на истина
* any(iterable) поне един от елементите се оценява на истина

## 8. Допълнителни структури от данни в collections:

* deque - двупосочни опашки
* OrderedDict - речник, който помни реда
* defaultdict - речник със стойност по подразбиране
* Counter - речник, който брои повтарящи се стойности
* namedtuple - кортеж с именовани полета

Използване: 
```python
from collections import deque
```

#                                                      Регулярни изрази и Python 

## 1. Въведение в регулярните изрази 

Регулярните изрази, наричани още regex може да открием в почти всички езици за програмиране. В Python те са имплементирани в стандартния модул re.

Регулярните изрази са по-скоро средство да търсим, извличаме и манипуливаме специфични низови шаблони от големи обеми текст. Те се използват предимно  проекти, които изискват валидиране на текста при вход (уеб проекти) или обработка на големи обеми обеми от текст, с цял извлизане на определена информация. 

## 2. Пищов на регулярните изрази: 

#### Основен синтаксис:

* .             Един знак независимо какъв с изключение на нов ред
* \.            Период. \ се използва за избягване на специални символи
* \d            Една цифра
* \D            Един знак не цифра
* \w            Един знак за буква вклучително цифри
* \W            Един знак не буква
* \s            Интервал
* \S            Символ, различен от интервал
* \b            Гранична дума
* \n            Нов ред
* \t            Табулация

#### Модификатори

* $             Край на низа(терминиращ оператор)
* ^             Начало на стринга
* ab|cd         Съвпадение на ab или de
* [ab-d]	      One character of: a, b, c, d
* [^ab-d]	      One character except: a, b, c, d
* ()            Items within parenthesis are retrieved
* (a(bc))       Items within the sub-parenthesis are retrieved

#### Повторения

* [ab]{2}       Точно 2 непрекъснати повторения на a или b
* [ab]{2,5}     2 до 5 непрекъснати повторения на a или b
* [ab]{2,}      2 до повече непрекъснати повторения на a или b
* +             Едно или повече
* *             Нула или повече
* ?             0 или 1

## 3. Какво е шаблон на регулярен израз и как да компилираме един 

Шаблоните на регулярен израз се градят със специален език, където използвайки букви, цифри и специални символи може да извлизаме съвпадения на шаблона в големи обеми текст. 
```python
 import re   
 regex = re.compile('\s+')
 ```

Например горния шаблон открива един или повече интервала в тескта.

## 4. Как да разделим низ използвайки regex

Нека погледнем следния текст: 
```python
text = """101 COM    Computers
205 MAT   Mathematics
189 ENG   English""" 
```

Всеки ред от низа представлява наредена тройка [номер на курс] [Код на курса] [Име на курса]. Както се вижда може да имаме повече от един интервал между думите. Това което искаме е да отделим думите, спрямо интервалите в низа.

Начин 1:
```python
# Разделяме текста спрямо това дали има един или повече интервала (шаблон)
re.split('\s+', text)
```
Начин 2: 
```python
# Разделяме текста спрямо наличието на интервал
regex.split(text)
#> ['101', 'COM', 'Computers', '205', 'MAT', 'Mathematics', '189', 'ENG', 'English']
```

Решихме поставения проблем, но кой начин е препоръчително да ползваме в практиката. Ако ни се налага да решаваме проблема много пъти добрата практика налага да използваме първият начин. 


## 5. Какво са findall, search и match 


