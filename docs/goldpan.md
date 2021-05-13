# Goldpan — бесплатный редактор и конвертер файлов TMX и TBX

С большим удовольствием мы предоставляем этот полезный инструмент всем переводчикам бесплатно.
Профессиональная версия программы отличается тем, что ряд ключевых функций, доступных в бесплатной версии, оптимизированы для нужд крупных компаний и пакетной обработки данных. Этот пакет распространяется по платной подписке. Однако все основные функции Goldpan совершенно бесплатны и таковыми останутся.

Текущая версия Goldpan: 3.6.1.

## Для чего нужна программа Goldpan?

Программа Goldpan была создана для обработки двуязычных файлов, используемых в процессе перевода любого контента в CAT-системах. Целью этой обработки является сохранение и повторное использование лингвистической информации, которая накапливается у переводчиков по мере их работы. Программа Goldpan позволяет:

- преобразовывать различные двуязычные файлы в универсальный формат TMX для сохранения в виде памяти переводов;

- обрабатывать имеющиеся файлы памяти переводов (ТМ), редактировать их, извлекать терминологию;

- удалять ненужную служебную разметку (внутренние теги) из файлов перед их загрузкой в CAT-систему или на сервер памяти переводов;

- готовить массивы памяти переводов для обучения систем машинного перевода.

## Что можно делать с накопленной библиотекой памяти переводов?

Файлы памяти переводов можно просто подготовить и очистить для дальнейшего хранения на локальном компьютере или на файловом сервере организации. Но такой способ организации лингвистических активов давно устарел — он не позволяет эффективно повторно использовать накопленные переводы.

Лучше всего хранить очищенные массивы памяти переводов на облачном сервере, где эти разрозненные файлы превращаются в единый источник переводов для отдельного пользователя или для целой организации.

Компания Logrus Global предлагает соответствующее решение: **Memose**. Облачная платформа **Memose** позволяет:

- упорядочить и централизовать хранение массивов памяти переводов и управление ими;

- выполнять поиск фразх и предложений (поиск по конкордансу) сразу по всем имеющимся массивам памяти переводов;

- собирать проектные памяти переводов для подключения к любым CAT-системам;

- и даже переводить и редактировать непосредственно файлы формата XLIFF! 

Чтобы больше узнать о платформе Memose, напишите нам по адресу: marcom @ logrusglobal.com.

## Поддерживаемые операционные системы

Поддерживаетя только Windows x64. Не поддерживаются: Windows x32, OS X, Linux.

Для организаций по запросу возможна доработка имеющихся функций пролграммы и разработка новых за соответствующую плату. Запросы частных лиц принимаются в разработку по нашему усмотрению и за наш счет. Пожертвования на улучшение программы всегда приветствуются.

## Установка программы Goldpan

Для установки программы Goldpan зайдите на сайт Logrus Global Localization Cloud (https://cloud.logrusglobal.com/) и выберите раздел Goldpan. Наждмите кнопку **Try it**. Вы будете перенаправлены в личный кабинет пользователя Logrus Global Localization Cloud, где можно скачать текущую версию программы.

Нажмите ссылку **Free Download** на карточке программы Goldpan.

Будет запущена загрузка текущего дистрибутива в виде файла формата MSI. По завершении загрузки запустите этот файл и завершите установку.

## Версия PRO

Если ваша учетная запись на платформе Logrus Global Localization Cloud авторизована для использования версии Goldpan **PRO**, нажмите кнопку **PRO Version** на вкладке Home или на вкладке Help меню программы и введите имя и пароль вашей учетной записи. После этого будут активированы функции **PRO Version**.

В настоящее время следующие функции доступны только в версии **PRO**:

- пакетная очитстка тегов в файлах (кнопка **Clean tags in files** на вкладке Batch Tools — см. ниже раздел **Очистка тегов**).

## Создание, открытие, редактирование файлов TMX и TBX

Программа Goldpan является простым, но мощным инструментом для создания и редактирования файлов многоязычной памяти переводов (TMX) и файлов глоссариев (TBX) с не более чем девятью языками одновременно.

В простом интерфейсе пользователя реализовано множество функций. Не все из них очевидны — такие функции описаны в этой справке.

### Поддерживаемые форматы файлов

Программа Goldpan поддерживает разные форматы файлов для импорта данных в программу и для экспорта данных из нее. Некоторые из этих форматов файлов только читаются (импортируются), но не экспортируются.

### Импорт

В программу Goldpan можно импортировать файлы переводческих ресурсов следующих форматов: **SDLTM**, **SDLXLIFF**, **XLIFF**, **TMX**, **TBX**.

Чтобы импортировать в программу переводческие ресурсы из какого-нибудь файла, на вкладке Import/Export нажмите кнопку Import File. В диалоговом окне импорта выберите нужный формат в раскрывающемся списке, затем найдите и выделите требуемый файл. Импорт возможен только из одного файла за раз. Для импорта нескольких файлов повторите процедуру для каждого файла отдельно.

### Экспорт

Чтобы экспортировать данные из программы, нужно выбрать соответствующие строки, а затем экспортировать их в виде файла формата **TMX**, **XLIFF**, **TBX** или **XLSX**.

Экспорт из программы Goldpan выполняется только из специального буфера обмена. Для переноса данных в этот буфер служат кнопки **Move to Memory** (перемещение) и **Copy to Memory** (копирование) на вкладке **Import/Export**. Операция **Move to Memory** удаляет выделенные сегменты из окна редактирования при их переносе в буфер. Команда **Copy to Memory** сохраняет исходные сегменты на их месте. Выделить нужные сегменты можно стандартным образом —  щелчком при нажатой клавише SHIFT или CTRL, либо путем перетаскивания. Сегменты перемещаются или копируются только целиком. Если сегмент выделен частично, он все равно будет перемещен или скопирован целиком. Для запуска процесса экспорта служит кнопка Export, расположенная на границе между панелью редактора и панелью буфера обмена. Либо можно воспользоваться кнопками в группе Export на вкладке Import/Export. (Соответствующий формат файла будет выбран по умполчанию.)

### Выделение цветом и фильтрация

Строки переводческих ресурсов можно пометить цветом или применить к ним фильтры. Для этого служит выделение цветом.

Выделение цветом выполняется с помощью раскрывающегося списка **Color** в группе **Markup** на вкладке **Home**. Если в этом списке выбран какой-нибудь цвет, все выбранные сегменты будут подсвечены этим цветом. Допускается выделение сегмента только одним цветом одновременно, и только сегмента целиком. (Для удобства поле TU# не выделяется.) Для отмены выделения сегментов цветом в списке имеется опция **Clear Markup**.

Фильтрация на базе выделения цветом выполнятся с помощью раскрывающегося списка **Color** в группе **Marked Up** на вкладке **Filters and Checks**. Если какие-либо цвета выбраны в этом списке (допускается множественный выбор), в окне редактора не будут отображаться сегменты, которые не помечены одним из этих цветов.

### Фильтрация

You can filter your translation resources by various criteria, such as segment status and presence of particular text fragments within cells.

The **Filters and Checks** tab elements are used for this purpose:

- The **Clear** button resets the list of filtering criteria.

- The **Status** button group is used for displaying only the new, modified or locked segments in the editor. Segments are locked or unlocked using the Protection button group in the Home tab.

- The **Marked Up** element group (see above).

- The **Search** element group is used to filter away any segments that don't contain the specified text fragment. A specific segment field, selected by means of the Field drop-down list, will be searched for the fragment entered in the Text box. If the Contains button is used to start the filtering process, the editor will display every segment that contains the text within the appropriate field. If the Equals button is used, only the segment in which the field’s content is a complete match to the text will be shown.

- The **Advanced** element group (see below).

### Find and Replace

You can use standard find-and-replace functions in the editor.

You can activate the **Search and Replace** window by pressing either `CTRL+F` or the **Search** button in the **Text Search** group of the **Home** tab.

Goldpan enables the use of regular expressions with these functions, which can be quite useful. For example, you may need to edit or remove the time codes that are present in your TM data. In that case, you'd simply run a search or replace query with the "\d\d:\d\d:\d\d\s" regular expression (for a "11:22:33" format of time codes) in the "Find what" field. The use of regular expressions is toggled via the **Use Regular expression** checkbox.

### Clearing tags

You can clean up your translation resources by removing unwanted tags of various types (including the `XML` and `RTF` tags) as well as any superfluous spaces at the start and at the end of a given text.

The **Clean** drop-down list in the **Text Cleaning** group of the Home tab is used for this purpose. Selecting any of the items on the list executes the corresponding operation for all highlighted cells:

- **Tags only** removes any angle bracket (< >) tags.

- **Tags such as { }** remove any curly bracket or other corresponding tags.

- **Trim first and last spaces** removes any unneeded spaces.

- **Clear cells** clears the cells.

If you are operating a **PRO Version** of Goldpan, there is now - as of Version 3.6 - another option ready for you: the **Clean tags in files** button in the Batch Tools tab. With it, you can clean up entire batches of files in a few clicks. Pressing this button calls a dialog window. There, you can set up a list of files to be cleared of tags using the **Add File** (which calls an additional dialog window for selecting one or more TMX/TBX files) and **Add TMX Dir** (which calls another window for designating entire folders) buttons. The **Clean tags**, **Clean tags like { }** and **Trim first and last spaces** checkboxes determine the method of tag-clearing to be employed, similiar to the buttons described above. After you've listed all the files and chosen the clearing method, press the CLEAN button to execute!

![The dialog window](clean.png)

### QA Filtering options

You can perform basic QA checking on your translation resources, as Goldpan provides various methods of segment filtering based on source-target comparison.

The **Filter Checks** drop-down list from the Advanced group of the Filters and Checks tab is used for this purpose. It contains the following elements:

- **Source = Target** displays only the segments in which the contents of the source and target fields match.

- **Capitalization** displays only the segments in which the text in the source and target fields begins with different capitalization.

- **Leading and trailing spaces** displays only the segments with different leading and trailing spaces in their source and target fields.

- **Double spaces** displays only the segments in which the source and target fields contain different sets of double spaces.

- **Digits and numbers** displays only the segments in which the source and target fields contain different sets of digits and numbers.

- **Placeholders** displays only the segments in which the source and target fields contain different sets of placeholders (i.e., formatted printing sequences: %s, %d, %1, etc.)

- **Punctuation** displays only the segments in which the source and target fields differ in leading and trailing punctuation.

- **Relative size** displays only the segments in which the source and target fields vary greatly in the volume of text they contain.

- **Empty segments** displays only the segments in which either the source or the target field is empty.

- **Partially translated** displays only the segments in which the target field partially matches the content of the source field, pointing to partial translation.

- **Find duplicates** displays duplicate segments.

The check is performed for a single language pair, i.e. the source language and a particular target language selected from the **Ref.Pair** drop-down list.

A new element, **Text and RegExp Filter**, has been added in Version 3.5.3. It deserves a chapter of its own.

### Text and Regular Expression Filtering

The **Text and RegExp Filter** function is different from the other ones that are accessed through the **Filter Checks** drop-down list.

It displays a dialog window resembling the standard Find & Replace window. However, instead of finding or replacing individual records, this one filters out a list of all the records containing a specific string, or matching a regular expression.

We've created this function with the task of 'cleaning up TM corpi' in mind. For example, if you need to send a corpus (or a fragment of it) somewhere, for training or testing a machine translation engine, you may want to filter out all the records containing the name of your company, in order to then remove them (or to edit them, perhaps using regular expressions). In the past, it has been noted that Goldpan did not offer this capability - but it does, now!

By default, the filtering is performed through the target cell contents. The **Search in source** option enables filtering via the source cell contents. There is a **Match case** option, as well.

![Let's filter out all the records that have the word 'Accounting' in the source](accounting1.png)
*Let's filter out all the records that have the word 'Accounting' in the source*

The **Use RegExp** option enables you to use regular expressions for filtering. A link to the regular expression specification at microsoft.com is provided for quick reference.

![Now let's filter out those that specifically start with this word, instead of just having it anywhere](regexp1.png)
*Now let's filter out those that specifically start with this word, instead of just having it anywhere*

### Split & Merge

You can split and merge translation memory files using several criteria, in batch mode.

The **Split & Merge** group of the Batch Tools tab is used:

- The **Split** button opens a dialog window that is used to split TBX/TMX files, and the source file is selected by means of the Browse button. The size of the resulting files is determined by segment count or by file size, depending on the user's requirement. The OK button is activated when the source file and splitting method are selected.

- The **Merge** button opens a dialog window used for merging a batch of TBX/TMX files. The source language of the resulting file is selected from the Source/Admin language drop-down list or set by entering a language code. The File List element group facilitates the addition of all TMX/TBX files in a particular folder to the list (Add TMX Dir, Add TBX Dir), the addition of arbitrary files or groups of files (Add File), the removal of files from the list one by one (Delete) or the clearing of the list (Clear). The OK button becomes active when a source language is set and at least one or more files are added to the list.

### Format conversions

You can convert `XLSX` files into the `TMX`, `TBX` or `XLF` format, in batch mode.

The **Converters** group of the Batch Tools tab is used. Each of the buttons (Convert to TMX, Convert to TBX, Convert to XLF) calls a dialog window in which the user will:

- select a single XLSX file for conversion using the Browse button

- set the languages for the resulting multilingual file. Each language has to be selected from the Language drop-down list (or entered as a language code) and added to the list by means of the Add button

- set the source language by selecting it from the Primary language drop-down list or entering a language code

The OK button becomes active when a XLSX file is selected and at least two languages are added to the list.

Goldpan lets the user choose each of the resources required from various sources and then merge them into new translation-memory resource files as needed.
