#                                   Избиране на текстов редактор за работа с Python 

## 1.Въведение
Популярен избор за хората, които пишат на Python е текстовия редактор Sublime Text 3 (ST3).  Той не ползва много ресурси, може да се ползва на различни операционни системи и се ползва с репутация на изключително бърз, лесен за ползване, настройване и получава голяма поддръжка сред програмистите. Накратко той е един изключителен редактор, дори след първоначалната си инсталация, но истинската му сила е чрез добавяне на допълнителни функционалности използвайки Package Control (Мениджъра на пакети) и създаването на индивидуални настройки. 

## 2. Функционалности

2.1 Split Layouts (Разделен екран) е функционалност, която ви позволява да гледате едновременно няколко файла и да ги подредите по избран от вас начин. Това е особено полезно когато работите по визуалната част (front end)  и програмната логика (back end) при разработката на уеб продукти или писанаето на тестове за нова функционалност.

2.2 Използване на табове подовно на Chrome за навигация.

2.3 Автоматично зареждане на отворените файлове от сесията, преди да затворите редактора си. 

2.4 Изволзването на Code Snippets повишава цялата продуктивност. Това е възможността, да отделите често използвано парче код като фрагмент, който може да извикате с ключова дума. Има колекция от фрагменти, която може да ползвате по подразбиране. За да ги видите натиснете lorem и после натиснете клавиша Tab.Би трябвало да видите известния параграф, за тестове lorem ipsum.

# Инсталиране на Package Control

За да се възползваме напълно от всички възможности и да можем да разширим нашия текстов редактор Sublime трябва да инсталираме Мениджъра на пакети (Package Control). След като го инсталираме ще можем да имаме достъп до различни пакети, които от своя страна можем да инсталираме, премахваме или обновяваме. Можете да разгледате различните пакети и какво включва всеки от тях на този [сайт](https://packagecontrol.io/).

## 1. За да инсталираме Мениджъра на пакети, трябва да влезем в конзолата на Sublime, а това става като изберем View > Show Console ,за да я отворим. Отиваме на [адреса](https://packagecontrol.io/installation#st3) и копираме кода, който е показан там :
```python
import urllib.request,os,hashlib; h = '6f4c264a24d933ce70df5dedcf1dcaee' + 'ebe013ee18cced0ef93d5f746d80ef60'; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); urllib.request.install_opener( urllib.request.build_opener( urllib.request.ProxyHandler()) ); by = urllib.request.urlopen( 'http://packagecontrol.io/' + pf.replace(' ', '%20')).read(); dh = hashlib.sha256(by).hexdigest(); print('Error validating download (got %s instead of %s), please try manual install' % (dh, h)) if dh != h else open(os.path.join( ipp, pf), 'wb' ).write(by) 
```

Пействаме го в конзолата, натискаме клавиша Enter и чакаме инсталацията да завърши след което рестартираме нашия текстов редактор. 

## 2. Вече можете инсталирате всеки от пакетите, които видяхте по-рано. За да го направите използвайте клавишната комбинация Ctrl+Shift+P. След това напишете install докато се появи Package Control: Install Package. Натиснете клавиша Enter и може да изберете любимите си пакети, за да бъдат инсталирани. 

Списък на някои команди:
  
* List Packages -показва списък на инсталираните пакети.
  
* Remove Package <име_пакет> премахва пакета от редактора.
  
* Upgrade Package <име_пакет> обновява пакет за редактора.

# Пакети:
Списък на често използвани пакети, за работа с Python:

##1. SideBarEnhancements 
Пакета съдържа разширение, с което можем да виждаме файловете и папките в работната директория. Чрез него може да създаваме или изтриване файлове.Струва си да отбележим, че ако използвате опцията изтриване, файла отива във вашео кошче, и ако сте го изтрили по погрешка и не ползвате version control (система за контрол на версиите) може да си го възстановите от там.

##2. Anaconda 
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
