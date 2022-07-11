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

Между **концепцией** и набором **терминов** на любых языках существует связь типа "один ко многим", а между **терминами** на различных языках существвует связь типа "многие ко многим". Таким образом модель данных учитывает возможные стуации, когда один **термин** на исходном языке может соответствовать нескольким терминам в языке перевода.

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
- Бизнес-домены, к которым принадлежит термин;
- Типы терминов (концепция, сокращение и т.д.);
- Части речи, исползуемые в качестве терминов;
- Продукты, с которыми связаны термины;
- Модули;
- Наличие или отсутствие статуса "DNT" ("Не переводить");
- Наличие или отсутствие статуса "Одобренный термин";
- Клиент.

The **Apply Filter** button refreshes the **List of Terms** in accordance with the current **Term Filter** settings.

The **Term Filter** also includes the **Export** and **Export TBX** buttons that are used to create and download a XLSX or a TBX file respectively, containing the **Terms** from the filtered **List of Terms**.

The **List of Terms** will show a One-to-Many relationship between the source **Term** and the target **Terms** in multiple languages if the **Term Filter**  is set up for multiple target languages. When you click a source term in the **List of Terms**, the Edit dialog box opens and shows the full multilingual One-to-Many hierarhy - from the **Concept** down to the all its **Terms**, in various languages. You can add new synonym **Terms** in any of the languages already present, or select a new language for adding a **Term**:

![termlode_f3](termlode_f3.png)

The **+ New Term** button at the top right edge of the **Term Filter** calls a dialog window where you can define a new **Concept** and populate it with **Terms**. You are not limited in the number of **Terms** or the languages you can use.

![termlode_add1](termlode_add_7.png)

Selecting any number of **Terms** with the checkboxes on the left side of the **List of Terms** and pressing the **Delete Selected** button will delete them from the **Termbase**.

The drop-down menu over the **Term Filter** is used to switch the top frame between the **Term Filter** and other vital functions:

- The Settings menu, where you can set the name of the **Termbase**, as well as its default source and target languages and its business domain:

![termlode_add1](termlode_add_4.png)

- The Import menu, where you can import **Terms** via XLSX files (example file is provided via download link):

![termlode_add1](termlode_add_5.png)

- The Users menu, where you can see the list of uses that have been invited to this **Termbase** in various roles, as well as invite new users by sending invitation links to their email addresses:

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