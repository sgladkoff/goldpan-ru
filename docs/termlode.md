# Семейство приложений TermLode

Семейство приложений **TermLode** - это облачное решение, включающее в себя серверные и клиентские приложения для корпоративного использования. Оно позволяет создавать терминологические базы данных и управлять ими.

В семейство входят следующие приложения:

- Терминологическая БД **TermLode**;
- Поисковое приложение **Omnitran**;
- Экстрактор терминологии **Prospector**;
- Коннектор для **TermLode** и Trados.

Архитектура **TermLode** включает следующие основные элементы:

- Термбанк **TermLode**;
- Облачный frontend **TermLode**;
- Облачный frontend **Omnitran**;
- Облачный frontend **Prospector**;
- DLL-библиотека коннектора **TermLode**-**Trados**.

## Модель данных

Модель данных **TermLode** соответствует стандарту TBX standard (ISO 30042). Корнем иерархии является **концепция**, и **термины** на различных языках происходят из неё, как показано на схеме:

![termlode_f1](termlode_f1.png)

Между **концепцией** и набором **терминов** на любых языках существует связь типа "один ко многим", а между **терминами** на различных языках существвует связь типа "многие ко многим". Таким образом модель данных учитывает возможные стуации, когда один **термин** на исходном языке может соответствовать нескольким **терминам** в языке перевода.

## Применение

### TermLode

После входа на страницу **TermLode** пользователь попадает на экран **Управления терминологическими базами данных**.

![termlode_add1](termlode_add_1.png)

Здесь отображается список доступных пользователю **термбаз** (**терминологических баз данных**), сгруппированный по названиям компаний. Этот список можно фильтровать по названиям компаний или самих **термбаз**. Используя выпадающее меню наверху экрана, можно переключаться между этим списком и экраном создания новых **термбаз**: 

![termlode_add1](termlode_add_2.png)

Для создания новой **термбазы** нужно ввести название, выбрать исходный язык и язык перевода по умолчанию, а затем нажать кнопку **Создать новую термбазу**. **TermLode** создаст новую **термбазу** без содержимого.

Нажатие на одно из названий **термбаз** ведет на экран **Терминологическая база данных**:

![termlode_add1](termlode_add_3.png)

Верхнюю часть этого экрана занмиает **фильтр терминов**. С его помощью можно заполнять **список терминов** под ним, отбирая **термины** из **термбазы** по выбранным значениям переменных:

- Исходный язык и текст;
- Язык и текст перевода;
- Бизнес-домены, к которым принадлежит **термин**;
- Типы **терминов** (концепция, сокращение и т.д.);
- Части речи, исползуемые в качестве **терминов**;
- Продукты, с которыми связаны **термины**;
- Модули;
- Наличие или отсутствие статуса "DNT" ("Не переводить");
- Наличие или отсутствие статуса "Одобренный **термин**";
- Клиент.

Кнопка **Применить фильтр** обновляет **список терминов** в соответствии с настройками **фильтра терминов**.

Кроме того, с помощью кнопок **Экспорт** и **Экспорт TBX** можно загрузить **термины** из отфильтрованного **списка терминов** в виде файла XLSX или TBX соответственно.

Если в **фильтре терминов** установлено несколько языков перевода, **список терминов** будет отображать связь типа "один ко многим" между исходным **термином** и его переводами на соответствующие языки. При нажатии на исходный **термин** в **списке** открывается диалоговое окно редактирования, в котором отображается полная иерархия "один ко многим" - от **концепции** до каждого внесенного в базу **термина** на всех языках. В этом окне можно добавить новые **термины**-синонимы на присутствующих языках, либо выбрать новый язык для добавления **терминов**.

![termlode_f3](termlode_f3.png)

Кнопка **+ Новый термин** в правом верхнем углу **фильтра терминов** вызывает диалоговое окно, в котором можно обозначить новую **концепцию** и добавить соответствующие ей **термины**. Количество используемых языков и **терминов** ничем не ограничивается.

![termlode_add1](termlode_add_7.png)

Можно удалить из базы несколько **терминов** одновременно, расставив галочки с левой стороны **списка терминов** и нажав кнопку **Удалить выделенные**.

Выпадающее меню над **фильтром терминов** служит для переключения верхней области между **фильтром терминов** и другими важными функциями:

- Меню настроек, в котором можно задать название **термбазы** и её настройки по умолчанию: исходный язык, язык перевода, бизнес-домен:

![termlode_add1](termlode_add_4.png)

- Меню импорта, в котором можно импортировать **термины** из файлов XLSX (файл-пример предоставляется по ссылке):

![termlode_add1](termlode_add_5.png)

- Меню пользователей, в котором находится список пользователей, приглашенных в данную **термбазу** на различные роли. Здесь же можно приглашать новых пользователей, отправля им ссылки на электронную почту:

![termlode_add1](termlode_add_6.png)

### OmniTran

The **TermLode** data model organizes collections of **Terms** into **Glossaries** by client, as well as by topic. **OmniTran**, a global search front end web interface, enables you to carry out searches for a **Term** across multiple **Glossaries** at once.

![termlode_add1](termlode_add_8.png)

You can select just a single **Glossary** or source/target language, or any number of them at once. You can also view selected **Glossaries**, one at a time, as collections of alphabetical sections, by pressing the **A-Z** button:

![termlode_f7](termlode_f7.png)

### Prospector

**Prospector** is an automatic English terminology extraction tool with possibility to review and manually filter terminology candidates.

![termlode_add1](termlode_add_9.png)

You can use **Prospector** to extract **Terms** from a file (the TXT, HTM/HTML, DOC/DOCX XLF/XLIFF/SDXLIFF formats are supported) or from a webpage URL. Choose either option with the File/URL switch and then either copy and paste the web page address into the text box, or click on it to call the file selection dialog. Then, select any pre-existing **Glossaries** as well as processing options that you'd like to use, and press the **Extract Terminology** button.

You will see the **Terminology Candidates** window, with all the extracted **Terms** arranged in a list. The list has an option to search for **Terms**, as well as one to save any checked **Terms** in an XLS file. All the terms that appeared more than once will be, by default, checked for saving.

![termlode_add1](termlode_add_10.png)

## Architecture

**TermLode** has an SQL-based backen and a .NET-based frontend, which is an ideal architecture for cloud deployment:

![termlode_f8](termlode_f8.png)

**TermLode** can only be accessed by users via browser, as it is a completely web-based, cloud-ready application.

**TermLode** is built as a corporate application, implementing an ID service and roles to control access for various groups of users with different rights. 

The current roles are:

- Global Administrator
- Corporate Administrator
- Corporate User/Editor
- Terminologist
- Super Editor
- Super Terminologist
- Super Reviewer
- Viewer/Reviewer

![termlode_add1](termlode_add_11.png)