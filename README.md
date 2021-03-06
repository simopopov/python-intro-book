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

## Пакети:
Списък на често използвани пакети, за работа с Python:

### 1. SideBarEnhancements 
Пакета съдържа разширение, с което можем да виждаме файловете и папките в работната директория. Чрез него може да създаваме или изтриване файлове.Струва си да отбележим, че ако използвате опцията изтриване, файла отива във вашео кошче, и ако сте го изтрили по погрешка и не ползвате version control (система за контрол на версиите) може да си го възстановите от там.

### 2. Anaconda 
Това е най-пълния пакет за работа с Python, който съдържа всичко от което се нуждаете, за да работите с Python. С него, ще се чувствате сякаш работите с IDE(integrated software enviroment):

* Autocompletion - автоматичното довършване на код, което работи без проблем след инсталация и позволява да бъде конфицурирано по ваш избор използвайки настройки.

* Code linting - който използва PyLint или PyFlakes с PEP8 (АКо не сте чували какво е PEP8, това е набор от правила приети за конвенция при писането на Python код). АКо все пак искате да сложите собствен пакет, който да ви помогне с налагането на правила на синтаксиса може да изключите тази опция създавайки потребителски настройки за пакета:
Sublime > Preferences > Package Settings > Anaconda > Settings - User: {"anaconda_linting": false}

* Goto Definitions -намира и показва дефинирането на променлива, фукнция или клас в текущия проект.  

* Find Usage - бързо търсене на среащането на променлива, функция или клас, използвани в определен файл. 

* Show Documentation - показвазване на документацията, като извлиза така наречените docstring написани за функция или клас,ако все пак сте си направили труда да напишете такива.


### 3. Djaneiro
Djaneiro е пакет за работа с Django. Това е най-популярния избор на уеб фреймуърк за работа с Python. Пакета поддържа използването на темплейти, използването на кодови фрагменти и отбелязване и разпознаване на ключови думи. Използването на кодови фрагменти спестяват доста време, а за допълнителна бързина при разработката с използването на Django blocks с натискането на няколко клавиша имаме достъп до темплейти, модели, форми и вю-та. 

### 4.requirementstxt
Ако не сте чували какво е requirements.txt това е текстов файл, който се генерира автоматично и ни показва всички включени допълнително библиотеки и тяхната версия, за да можем, да подкараме даден проект. Този пакет ни позвалява да ползваме автоматично довършване и разпознаване на синтаксиса, както и система за контрол на версиите. 

### 5. GitGutter
GitGutter показва малки икони в началото на вски ред, които ни показват дали реда е бил добавен, променен или изтрит спрямо последната качена версия в git. 

## Използването на клавишни комбинации: 

* Ctrl+P - отваряне на файл по име; 
* Ctrl+G - отиване на определен ред във файла
* Ctrl + F - търсене в текущия файл
* Ctrl + Shift+ K - Изтриване на текущия ред
* Ctrl + (ляв бутон намишката) Позволява създаването и използването на много курсори едновременно, чрез които можем да редактираме едновременно на различни места в документа.

### Потребителски настройки: 
Отиваме в Preferences > Settings – User и редактираме файла Preferences.sublime-settings :

```js
{
    // Colors
    "color_scheme": "Packages/Tomorrow Color Schemes/Tomorrow-Night.tmTheme",
    "theme": "Soda Dark.sublime-theme",

    // Font
    "font_face": "Ubuntu Mono",
    "font_size": 16.0,
    "font_options": ["subpixel_antialias", "no_bold"],
    "line_padding_bottom": 0,
    "line_padding_top": 0,

    // Cursor style - no blinking and slightly wider than default
    "caret_style": "solid",
    "wide_caret": true,

    // Editor view look-and-feel
    "draw_white_space": "all",
    "fold_buttons": false,
    "highlight_line": true,
    "auto_complete": false,
    "show_minimap": false,
    "show_full_path": true,

    // Editor behavior
    "scroll_past_end": false,
    "highlight_modified_tabs": true,
    "find_selected_text": true,

    // Word wrapping - follow PEP 8 recommendations
    "rulers": [ 72, 79 ],
    "word_wrap": true,
    "wrap_width": 80,

    // Whitespace - no tabs, trimming, end files with \n
    "tab_size": 4,
    "translate_tabs_to_spaces": true,
    "trim_trailing_white_space_on_save": true,
    "ensure_newline_at_eof_on_save": true,

    // Sidebar - exclude distracting files and folders
    "file_exclude_patterns":
    [
        "*.pid",
        "*.pyc"
    ],
    "folder_exclude_patterns":
    [
        ".git",
        "__pycache__",
        "env",
        "env3"
    ]
}
``` 
Можем да настроим и pylinter според нашите изисквания редактирайки файла Pylinter.sublime-settings: 
```js
{
    // Configure pylint's behavior
    "pylint_rc": "/Users/daniel/dev/pylintrc",

    // Show different icons for errors, warnings, etc.
    "use_icons": true,

    // Automatically run Pylinter when saving a Python document
    "run_on_save": true,

    // Don't hide pylint messages when moving the cursor
    "message_stay": true
}
```

#                                 Какво е Virtualenv и защо трябва да знаем какво е 

Виртуалната среда или virtualenv ни позволяваше да ползваме изолирани контейнери много преди наличието на Docker. Простичко казано технологията ни позволява да ползваме изолирани среди да всеки проект, където може да инсталираме различни версии на модулите (библиотеките) без да влияем на централната инсталация.  Тук не става въпрос за подръжка на отделни копия на Python, а по-скоро ползването на изолирана среда за всеки отделен проект. 

## 1. Как да проверим, че имаме инсталиран virtualenv 
 Отиваме в терминала и пишем :
 ```sh  
 virtualenv --version
```
## 2. Как да инсталираме virtualenv 
 Отиваме в терминала и пишем една от следните команди:
```sh  
 sudo apt-get install python-virtualenv
 sudo easy_install virtualenv
 sudo pip install virtualenv
```
## 3. Как да използваме virtualenv 
Отиваме в терминала и пишем :
```sh  
  mkdir ~/env  # Създай папка с име env
  virtualenv ~/env/new_app # Създай проект с име new_app в папка env
  cd ~/env/new_app/bin # Влез в папката с помощни скриптове
  source activate # Използвай скрипта за стартиране на контейнер 
```
Последните две команди може да ги слеем:
```sh  
  source new_app/bin/activate
```
## 4. Инсталиране на пакети в virtualenv 
Отиваме в терминала и пишем :
```sh  
  pip install flask # инсталирай модула flask в контейнера, в ляво трябва да показва в терминала, че сме в контейнер
```
## 5. Излизане от средата на контейнера: 
```sh  
 source new_app/bin/deactivate
```

#                     Какво е PEP8 - това е конвенцията за писане на код в Python:

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
#                                                Изключения

Изключения ще наричаме някоя извънредна ситуация, която е възниквала при изпълнение на вашата програма. Например опитвате се да четете файл и откривате, че той не съществува. Или без да искате изтривате файла докато програмта ви все още го чете. Такива ситуации се наричат изключения. 

Забележете, че изключението е съвсем различно от грешката. Например, ако вместо print сте написали грешно Print, това е грешка.

Обработване на изключения

Нека гледаме на на изключенията като на горещ картоф, някой трябва да го хване и да го обработи. Това се прави с конструкцията try..except, която можем да разгледаме в примера по-долу: 


```python
# import module sys to get the type of exception
import sys

randomList = ['a', 0, 2]

for entry in randomList:
    try:
        print("The entry is", entry)
        r = 1/int(entry)
        break
    except:
        print("Oops!",sys.exc_info()[0],"occured.")
        print("Next entry.")
        print()
print("The reciprocal of",entry,"is",r)
```
Изход:

The entry is a
Oops! <class 'ValueError'> occured.
Next entry.

The entry is 0
Oops! <class 'ZeroDivisionError'> occured.
Next entry.

The entry is 2
The reciprocal of 2 is 0.5

## Как работи тази конструкция 

Когато знаем, че при дадена операция, например четенето на файл може да възникне извънредна ситуация трябва да сложим кода си в try блок и и след това да обратим възможните изключения, да хванем горещите картофи, в except блок. Except клаузата може да обработи само едно точно определено изключение/ извънреден случай. Забележете, че винаги трябва да използваме поне една except клауза след всеки try блок. Иначе би било безсмиселно да използваме try блок-а. 
```python
def linux_interaction():
    assert ('linux' in sys.platform), "Function can only run on Linux systems."
    print('Doing something.')

try:
    linux_interaction()
except:
    print('Linux function was not executed')
```
#### Понякога искаме да хванем точно определено изключение:
```python
try:
    linux_interaction()
except AssertionError as error:
    print(error)
    print('The linux_interaction() function was not executed')
```
#### Понякога може да искаме да иползваме и else клауза веднага след try...except блок-а.
```python
try:
    linux_interaction()
except AssertionError as error:
    print(error)
else:
    print('Executing the else clause.')
```
#### А понякога може да искаме да не обработваме изключението:
```python
try:
    linux_interaction()
except:
    pass
```
## Try ... Finally 

Finally клаузата винаги се изпълнява независимо дали има възникване на изключение или не. Тя често се използва, за да се освободят използваните ресурси. 
```python
try:
   f = open("test.txt",encoding = 'utf-8')
   for line in f:
        # perform file operations
finally:
   f.close()
```
## With ...

Използването на ресурси в try клауза и освобождаването им във finally клауза се среща доста често затова има и по-кратка версия да се напише горното:
```python
with open("test.txt",encoding = 'utf-8') as f:
    for line in f:
        # perform file operations
```

#                                                       Вход и изход с конзолата

Понякога когато пишем програмира ни се налага да общуваме с потребителя. Например той да въведе някакви данни и ние да му върнем резултата от операцията над теззи данни. За изход в конзолата можем да ползваме различни методи на str (string) класа. Ако искаме да разгледаме методите на този клас можем просто да изпълним: 
```python
>>>help(str)
```
```python
#Четене от конзолата:
>>>s=input()
#I am learning at Python

# Писане в конзолата:
>>>print(c)
'I am learning at hackerearth.'

#Казваме на потребителя какви данни искаме да ни подаде: 
>>> number = input("Tell us a number")
Tell us a number 6
>>> print(number)
'6'

#Искаме да отпечатаме произволен брой елементи, използвайки разделител(sep) ',' и отпечатвайки накрая '!!\n' : 
>>>print('LOVE', 30, 82.2, sep=',', end='!!\n')
'LOVE', 30, 82.2!!
```

#### Четене на числа
Нека съберем две числа и отпечатаме сумата им.
```python
xString = input("Enter a number: ")
x = int(xString)
yString = input("Enter a second number: ")
y = int(yString)
print('The sum of ', x, ' and ', y, ' is ', x+y, '.', sep='')
```
#### Използвайки композиране (влагане на функции) може първите четири реда да пренапишем като:
```python
x = int(input("Enter a number: "))
y = int(input("Enter a second number: "))
```
По същия начин можем да използваме маркери, които да ни пазят местата за променливите, и да пренапишем изхода:
```python
print('The sum of {} and {} is {}.'.format(x, y, x+y))
```
## Как да чета ефективно код от конзолата

Нека си представим, че искаме да прочетем стойностите на четири числа от конзолата a, b, c и d. После искаме да намерим тяхното произведение. 

Вариант 1А (чрез композиране на списък):
```python
a, b, c, d = [int(x) for x in input().split()]
print(a*b*c*d)
```
Вариант 1Б, използвайки функцията map:
```python
a, b, c, d = map(int, input().split())
print(a*b*c*d)
```
Как да чета код бързо от конзолата

Тайната е да използваме  stdin и stdout. Тогава решението на горната задача можем да направим по следния начин:

Вариант 2А (чрез композиране на списък):
```python
from sys import stdin, stdout
a, b, c, d = [int(x) for x in stdin.readline().rstrip().split()]
stdout.write( str(a*b*c*d) + "\n" )
```
Вариант 2Б, използвайки функцията map:
```python
from sys import stdin, stdout
a, b, c, d = map( int, stdin.readline().rstrip().split() )
stdout.write( str(a*b*c*d) + "\n" )
```
Задача: Столичната улица "Граф Игнатиев" се нуждае от ремонт на ремонта и затова трябва набързо да изчислим оптималния брой на нужните павета, за да я павираме като хората. Улицата има формата на правоъгълник (n×m) и паветата се слагат успоредно на страните му.Размера на всяко паве е a×a.

Позволява се да се покрие по-голяма площ отколкото улицата, но е задължително площта на цялата улица да бъде павирана. 

Вход: n,  m и a (1 ≤  n, m, a ≤ 10**9).
Изход: нужния брой павета. 
Пример:
Вход: 6 6 4
Изход: 4

Решение използвайки стандартния вход/изход:
```python
n, m, a = map(int, input().split())
 
h = n//a
if n%a != 0: h+=1
 
w = m//a
if m%a != 0: w+=1
 
print(h*w)
```

Решение използвайки бързия вход/изход:
```python
from sys import stdin, stdout
n, m, a = map(int, stdin.readline().rstrip().split())
 
h = n//a
if n%a != 0: h+=1
 
w = m//a
if m%a != 0: w+=1
 
stdout.write( str(h*w) + "\n" )
```
Оптимизирано четене на големи входни данни:

Задача. 
От конзолата ще прочетем две числа n и k. за следващите n реда ще прочетем по едно число не по-голямо от 10**9(10^9). Трябва да върнем колко от прочетените числа се делят на k. 

Пример :
Вход:
7 3
1
51
966369
7
9
999996
11

Изход:
4

1. Стандартно решение: 
```python
def main():
    n, k = [int(c) for c in input().split()]
    cnt = 0
    for _ in range(n):
        t = int(input())
        if t % k == 0:
            cnt += 1
    print(cnt)
 
if __name__ == "__main__":
    main()    
```
2. Решение използващо по-бързото четене и писане от конзолата:
```python
from sys import stdin, stdout 
 
def main():
    n, k = [int(c) for c in input().split()]
    cnt = 0
    for _ in range(n):
        t = int(stdin.readline())
        if t % k == 0:
            cnt += 1
    stdout.write(str(cnt))
 
 
if __name__ == "__main__":
    main()  
```
3. Оптималното решение:
```python
def main():
    from sys import stdin, stdout
    n, k = stdin.readline().split()
    n = int(n)
    k = int(k)
     
    cnt = 0
    lines = stdin.readlines()
    for line in lines:
        if int(line) % k == 0:
            cnt += 1
 
    stdout.write(str(cnt))
 
if __name__ == "__main__":
    main()
```
Забежете, че тука четем списъка от данни наведнъж, а не елемент по елемент. В това се крие тайната за по-бързото решение. Забележете също, че никъде не ни потрябва колко е стойността на n. Тоест ако трябва да прочетем вход, чиято дължина не знаем, можем просто да направим: 
```python
#четем входните данни, чиято дължина не знаем
lines = stdin.read().splitlines()

#можем вече да определим колко е дължината на прочетените данни:
n = len(lines)
```
#                                                Python magic или Питонска магия

itertools е питонски модул, който може да ни накара да повярваме, че магията съществува или иначе казано чрез него имаме достатъп до доста благинки, които са написани като бързи и ефикасни спрямо паметта методи. Обикновено функциите от този модул връщат итеруеми множества. 

## count(start=0, step=1)
count е функция итератор, която ще ни връща безкрайно итеруемо множество започващо от start, със стъпка step. Ако не са зададени стойности на параметрите се взимат показаните по-горе по подразбиране. Обикновено използваме count във for цикъл с терминиращо условие: 
```python
from itertools import count
 for i in count(10):
     if i > 20: 
        break
     else:
         print(i)
#Връща числата 10-20
```

или използвайки islice(функция, показва колко пъти да викаме итеруемото множество) :
```python
from itertools import islice
for i in islice(count(10), 5):
    print(i)
#Връща числата 10-14
```

## cycle(iterable)
cycle е функция итератор, която ще ни връща безкрайно итеруемо множество повтаряйки безкрайно стойностите от iterable параметъра си: 
```python
from itertools import cycle
count = 0
for item in cycle('XYZ'):
     if count > 7:
         break
     print(item)
     count += 1
 ```
Друг начин за използване е следния пример: 
```python
polys = ['triangle', 'square', 'pentagon', 'rectangle']
iterator = cycle(polys)
next(iterator)
# Ще върне 'triangle'
next(iterator)
# Ще върне 'square'
```

Тука използваме оператора next, за да върнем следващия елемент от итеруемото множество. 

##  repeat(object[, times])
repeat е функция итератор, която ще ни връща object безкраен брой , пъти освен ако няма заден параметър times.
```python
from itertools import repeat
iterator = repeat(5, 5)
next(iterator)
```

##  accumulate(iterable[, func])
accumulate - функция, която акумулира сумата на предходните елементи и следващия от итеруемо множество
```python
from itertools import accumulate
list(accumulate(range(10)))
[0, 1, 3, 6, 10, 15, 21, 28, 36, 45]
```

## chain(*iterables)
chain  итератор, който взима поредица от итеруеми и ги преобразува в едно голямо итеруемо множество.
```python
from itertools import chain
my_list = ['foo', 'bar']
numbers = list(range(5))
cmd = ['ls', '/some/dir']
my_list = list(chain(['foo', 'bar'], cmd, numbers))
#['foo', 'bar', 'ls', '/some/dir', 0, 1, 2, 3, 4]
```

## compress(data, selectors)
compress е много полезна функция, която компресира едно итеруемо множество използвайки за филтър второ итеруемо множество:
```python
from itertools import compress
letters = 'ABCDEFG'
bools = [True, False, True, True, False]
list(compress(letters, bools))
['A', 'C', 'D']
```

## dropwhile(predicate, iterable)
dropwhile е оператор, който ще маха елементи от итеруемото множество докато функцията предикат не върне истина (True).Зaради това върнатите елементи, започват веднага след първото връщане на неистина (False) от предикатната функция. 
```python
from itertools import dropwhile
list(dropwhile(lambda x: x<5, [1,4,6,4,1]))
[6, 4, 1] # Първото връщане на неистина е при 6

from itertools import dropwhile
def greater_than_five(x):
     return x > 5 
 
list(dropwhile(greater_than_five, [6, 7, 8, 9, 1, 2, 3, 10]))
[1, 2, 3, 10] # Първото връщане на неистина е при 1
```

##  filterfalse(predicate, iterable)
filterfalse  функция, която ще върне от итеруемото множество, само тези елементи, за които предикатната функция ще върне неистина (False).
```python
from itertools import filterfalse
def greater_than_five(x):
     return x > 5 
 
list(filterfalse(greater_than_five, [6, 7, 8, 9, 1, 2, 3, 10]))
[1, 2, 3]
```

## groupby(iterable, key=None)
groupby връща последователни ключове и групи от итеруемо множество. 
```python
from itertools import groupby
 
vehicles = [('Ford', 'Taurus'), ('Dodge', 'Durango'),
            ('Chevrolet', 'Cobalt'), ('Ford', 'F150'),
            ('Dodge', 'Charger'), ('Ford', 'GT')]
 
sorted_vehicles = sorted(vehicles)
 
for key, group in groupby(sorted_vehicles, lambda make: make[0]):
    for make, model in group:
        print('{model} is made by {make}'.format(model=model,make=make))

#Cobalt is made by Chevrolet
# 
#Charger is made by Dodge
#Durango is made by Dodge
# 
#F150 is made by Ford
#GT is made by Ford
#Taurus is made by Ford
```
##  starmap(function, iterable)
starmap е функция, която ни позволява да прилагаме функция върху списък с аргументи например, което я превръща в прекрасен инструмент за изчисления. 
```python
from itertools import starmap
def add(a, b):
    return a+b
 
for item in starmap(add, [(2,3), (4,5)]):
     print(item) 
#5=2+3
#9=4+5

##  takewhile(predicate, iterable)
takewhile ще върне итеруемо множесто от елементи от друго итеруемо множесто докато предикатната функция за елементите връща истина (True)

from itertools import takewhile
list(takewhile(lambda x: x<5, [1,4,6,4,1]))
[1, 4]
```
## tee(iterable, n=2)
tee е функция, която ни позволява да имаме много независими един от друг итератори върху едно и също итеруемо множество.
```python
from itertools import tee
data = 'ABCDE'
iter1, iter2 = tee(data)
for item in iter1:
     print(item)
```
##  zip_longest(*iterables, fillvalue=None)
zip_longest е функция, която опакова две итеруеми спрямо дължината на по-дългото. 
```python
from itertools import zip_longest
for item in zip_longest('ABCD','xy',fillvalue='BLANK'):
     print (item)

#('A', 'x')
#('B', 'y')
#('C', 'BLANK')
#('D', 'BLANK')
```
##  combinations(iterable, r)
combinations ни връща кобинациите с дължина r от различните елементи на итеруемо множество: 
```python
from itertools import combinations
list(combinations('WXYZ', 2))
#[('W', 'X'), ('W', 'Y'), ('W', 'Z'), ('X', 'Y'), ('X', 'Z'), ('Y', 'Z')]
```
##  combinations_with_replacement(iterable, r)
combinations_with_replacement ни връща кобинациите с повторение с дължина r от различните елементи на итеруемо множество: 
```python
from itertools import combinations_with_replacement
list=[]
for item in combinations_with_replacement('WXYZ', 2):
     list.add(''.join(item))
#[WW,WX,WY,WZ,XX,XY,XZ,YY,YZ,ZZ]
```

##  product(*iterables, repeat=1)
product е готина функция, която ни позволява да правим Декартово произведение от множества от входни итеруеми:
```python
from itertools import product
arrays = [(-1,1), (-3,3), (-5,5)]
cp = list(product(*arrays))

#[(-1, -3, -5),(-1, -3, 5), (-1, 3, -5),
# (-1, 3, 5), (1, -3, -5),(1, -3, 5),
# (1, 3, -5), (1, 3, 5)]
```
##  permutations(iterable, r)
permutations е функция, която ще ни върне пермутации с дължина r от елементи от итеруемо множество:
```python
from itertools import permutations
list=[]
for item in permutations('WXYZ', 2):
     list.add(''.join(item))
#[WX,WY,WZ,XW,XY,XZ,YW,YX,YZ,ZW,ZX,ZY]
```
## Примери :
### 1. Комбиниране на елементи: 

```python
list(zip([1, 2, 3], ['a', 'b', 'c']))
[(1, 'a'), (2, 'b'), (3, 'c')]
```
### 2. Връщане на дължината на низове

```python
list(map(len, ['abc', 'de', 'fghi']))
[3, 2, 4]
```
### 3. Сумиране на интеруеми:

```python
list(map(sum, zip([1, 2, 3], [4, 5, 6])))
[5, 7, 9] # 5=1+4, 7=2+5, 9=3+6
```
### 4. Групиране на елементи:

```python
nums = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
def naive_grouper(inputs, n):
    num_groups = len(inputs) // n
    return [tuple(inputs[i*n:(i+1)*n]) for i in range(num_groups)]
naive_grouper(nums, 2)
[(1, 2), (3, 4), (5, 6), (7, 8), (9, 10)]
```

### 5. Опаковане:
```python
import itertools as it
x = [1, 2, 3, 4, 5]
y = ['a', 'b', 'c']
list(zip(x, y))
[(1, 'a'), (2, 'b'), (3, 'c')]
list(it.zip_longest(x, y))
[(1, 'a'), (2, 'b'), (3, 'c'), (4, None), (5, None)]
```

### 6. Brute Force или грубата сила:

Имаме 3 банкноти по $20 долара, 5 по $10 долара, 2 по $5 долара, 5 по $1 долар. По колко начина можем да развалим(разбием на дребни банкноти) банкнота от $100 долара. 

```python
bills = [20, 20, 20, 10, 10, 10, 10, 10, 5, 5, 1, 1, 1, 1, 1]
makes_100 = []
for n in range(1, len(bills) + 1):
     for combination in it.combinations(bills, n):
         if sum(combination) == 100:
            makes_100.append(combination)
set(makes_100)

{(20, 20, 10, 10, 10, 10, 10, 5, 1, 1, 1, 1, 1),
 (20, 20, 10, 10, 10, 10, 10, 5, 5),
 (20, 20, 20, 10, 10, 10, 5, 1, 1, 1, 1, 1),
 (20, 20, 20, 10, 10, 10, 5, 5),
 (20, 20, 20, 10, 10, 10, 10)}
```

7. Използване на рекурентна връзка
Нека имплементираме итеруема функция за Фибуначи.
```python
def fibs():
    a, b = 0, 1
    while True:
        yield a
        a, b = b, a + b
```
Която може да използваме по следния начин:
```python
list(next(fibs) for _ in range(8))
[0, 1, 1, 2, 3, 5, 8, 13]
```

#                                                      Регулярни изрази и Python 

## 1. Въведение в регулярните изрази 

Регулярните изрази, наричани още regex може да открием в почти всички езици за програмиране. В Python те са имплементирани в стандартния модул re.

Регулярните изрази са по-скоро средство да търсим, извличаме и манипуливаме специфични низови шаблони от големи обеми текст. Те се използват предимно  проекти, които изискват валидиране на текста при вход (уеб проекти) или обработка на големи обеми обеми от текст, с цял извлизане на определена информация. 

## 2. Пищов на регулярните изрази: 

#### Основен синтаксис:
| Израз     | Значение          |
| :-------------: |:-------------:|
| .             |Един знак независимо какъв с изключение на нов ред|
| \.            |Период. \ се използва за избягване на специални символи|
| \d            |Една цифра|
| \D            |Един знак не цифра|
| \w            |Един знак за буква вклучително цифри|
| \W            |Един знак не буква|
| \s            |Интервал|
| \S            |Символ, различен от интервал|
| \b            |Гранична дума|
| \n            |Нов ред|
| \t            |Табулация|

#### Модификатори
| Израз     | Значение          |
| :-------------: |:-------------:|
| $             |Край на низа(терминиращ оператор)|
| ^             |Начало на стринга|
| ab|cd         |Съвпадение на ab или de|
| [ab-d]	      |One character of: a, b, c, d|
| [^ab-d]	      |One character except: a, b, c, d|
| ()            |Items within parenthesis are retrieved|
| (a(bc))       |Items within the sub-parenthesis are retrieved|

#### Повторения
| Израз     | Значение          |
| :-------------: |:-------------:|
| [ab]{2}       |Точно 2 непрекъснати повторения на a или b|
| [ab]{2,5}     |2 до 5 непрекъснати повторения на a или b|
| [ab]{2,}      |2 до повече непрекъснати повторения на a или b|
|   +           |Едно или повече|
|   *           |Нула или повече|
|   ?           |0 или 1|


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


