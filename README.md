# STITT

STITT is a program for working with trilingual textual data. It's designed to support translators who are working on texts that are extant in both Sanskrit and Tibetan. STITT provides a structured user interface for inputting, annotating, and processing text in Sanskrit, Tibetan, and English. It includes fields for source texts, language correspondences, glosses, a translation, and notes. The current version of STITT is 1.4c.

Screenshot of STITT version 1.4c:

![stitt-1-4b-screenshot](https://github.com/nickscottprior/stitt/assets/140344267/38b448c7-7c23-453a-b889-3b8ad4c4ee12)


## How to use STITT

You don't need to know coding to use STITT. It opens in your web browser and has an interactive user interface.

To use STITT, click on [stitt.html](/stitt.html) and then click on the download icon in the top right to download the raw file:

![Screenshot of the download button](/download-raw-file.png)

You can then double-click the downloaded file to open the program in a web browser. If double-clicking doesn't work, then you can right-click the file and select the option to open it with a web browser. STITT works best in Firefox; its content may not be editable in other browsers. 

STITT is a file, not a website. It is stored locally on your computer but opened in a web browser, just like you might open .doc files in Microsoft Word or .pdf files in Adobe Acrobat Reader. As a result, it functions even if you have no internet connection.

Because STITT is a local file, it will not update automatically and you may end up using an out-of-date version. This shouldn't cause any issues, but you wouldn't want to miss out on new features! I recommend checking this page periodically to see if there have been any new updates since you last downloaded STITT.

You can "save" a STITT document by typing Ctrl+S or by clicking the "download current page" button at the bottom of the document. I recommend using the SHOC menu to show all fields and close all fields before saving.

**For a detailed guide to using STITT, see the [Documentation](#documentation) section further below.**

## New in version 1.4c

* bug fix for adding new lines to a paragraph in Chrome
* bug fix for "delete blocks in range" button
* added link to a Wylie converter

## New in version 1.4b

* added support for Wylie throughout the program
* renamed the automatic text processor + inputter to "automatic text importer"
* renamed the GRETIL preprocessor to "IAST preprocessor"
* added common diacritics to the default project notes
* added outline to the correspondences table
* correspondences are now excluded from HTML parse + purge buttons to avoid causing issues with data extraction
* added buttons for combined interlinear text output (Sanskrit + translation, Tibetan + translation, Sanskrit + Tibetan + translation)
* added a button to remove extra line breaks + spaces from a text, to help support a wider range of texts

## New in version 1.4

* An automatic text processor + inputter for GRETIL and ACIP e-texts
* SHOC buttons to Show, Hide, Open, or Close any fields of your choice
* A text box to store project notes
* Move blocks, delete blocks, and insert blocks anywhere in the work area
* Delete a range of blocks from the work area all at once
* Parse or purge user-created HTML content (for advanced users)
* Extract and display the field of your choice in either block-by-block or continuous format at the bottom of the document
* Export language correspondences as a table that you can copy-paste into Word, Excel, Anki, or other software
* Convert GRETIL or ACIP texts into the format of your choice, and display the output at the bottom of the document
* Hover your mouse over a menu for an explanation of its function

## Benefits

### General benefits

STITT was originally developed for working with Tibetan translations of Sanskrit Buddhist texts. It has several benefits over standard word-processing software, including:

* A simple and customizable UI to minimize distractions
* Collapsible sections to show or hide data as needed
* A hierarchical HTML-based data structure to allow for easy data extraction

The hierarchical data structure is particularly important. It allows STITT to import and export textual data in a variety of different formats at the click of a button. As of STITT version 1.4, you can automatically import GRETIL and ACIP e-texts into the work area at the click of a button, and can export your translation from the work area in either block-by-block format or as a continuous text. You can also export your notes on language correspondences as a table that you can easily copy-paste into other programs.

Once this feature has been fully implemented, you will be able to:

1. Extract any of the data fields as interlinear text, continuous text, or chunked text, depending on what you need;
2. Maintain data in only one place (your STITT document) and generate derivative data automatically, instead of trying to manually convert data from one format to another;
3. Input data from your STITT document into digital linguistics tools such as [xigt (eXtensible Interlinear Glossed Text)](https://github.com/xigt/xigt) or the [DLx JavaScript Library](https://github.com/digitallinguistics/javascript).

Chunked text has not yet been implemented. This would include a certain amount of lines in a chunk, which would make it easy to create a parallel text with one language on one page and the other language on the opposite page. You could also combine these different extraction methods to create a continuous or chunked document that supports line-by-line user interaction, such as highlighting a sentence in a source text to see its English translation.

### Portability and extensibility

STITT is written in three coding languages: HTML, CSS, and JavaScript. These are the three basic languages of the internet, so they are supported by a wide range of different software. This allows data in STITT to be portable, meaning that you can write content in STITT and then export it easily into office programs, websites, or other kinds of software. It also makes STITT extensible, which means that it can easily accommodate new features thanks to the many resources, libraries, and features that are available for these three languages.

## Target audience

STITT ultimately aims to support five main types of users:

* translators
* language learners
* linguists
* linguistic software developers
* editors of translated texts

## Planned features

I would eventually like to add the following features:

* Extracting data fields as chunked text;
* Customizing the fields in a block;
* Dark mode;
* Importing related open-source software;
* Adding support for forward compatibility;
* Incorporating open-source linguistics software.

## Documentation

STITT is composed of four main sections:
1. the header;
2. the input menu;
3. the work area;
4. the output menu.

### The header and input menu

The header and input menu in version 1.4c:

![stitt-1-4b-header-and-input-menu](https://github.com/nickscottprior/stitt/assets/140344267/31280999-ce09-403a-a9a3-584abb22e649)

The header contains general information about STITT. The "technical details" line is the first dropdown menu you will encounter; click on it to open it up. It contains technical information about STITT and lists the version that you are using. The latest version is 1.4c.

The input menu contains 3 sections:
1. The automatic text importer
2. The SHOC buttons
3. Project notes

**The automatic text importer**

The automatic text importer is exactly what it sounds like. If you copy-paste (ctrl+c and ctrl+v) a GRETIL or ACIP e-text into the importer box and click the corresponding import button, it will automatically split the text into individual lines and add them to the bottom of the work area. For Sanskrit texts it will preserve the line breaking of the original, and for Tibetan texts it will break lines after every double shad (༎). You can either import a text all at once, or in chunks as needed. Using ctrl+shift+v to paste unformatted text may cause issues with the importer, because it relies partially on the formatting to help it break texts into individual lines.

The "Import Sanskrit text" button is designed for GRETIL e-texts, but it can often support other types of Sanskrit e-text too. The most common issue with importing other types of e-text (e.g. from sanskritdocuments.org or www.dsbcproject.org) is that they have too many spaces and line breaks. If you encounter this issue, you can first copy-paste the text into the output menu, click on "Remove extra lines and spaces", and then copy-paste the output into the automatic text importer. That should allow you to import the text without including extra spaces and line breaks.

The importer works with Devanagari, IAST romanization, Uchen, and Wylie romanization. If you decide that you want to transliterate a GRETIL or ACIP e-text before importing it, the "automatic text importer instructions" dropdown has further instructions. Otherwise, you should be able to just copy-paste the text.

**The SHOC buttons**

SHOC stands for "Show, Hide, Open, Close". The SHOC buttons let you show, hide, open, or close different dropdown fields in the work area. They can also be used to show or hide the sidebar buttons beside each block in the work area. The SHOC buttons make it easy to close or hide any content that you don't want filling up space on your screen.

**Project notes**

The project notes is an editable field, like most of the fields you will encounter. You can use it however you like, but the intended purpose is to store any links, notes, to-do items, or other information that is relevant to the project you're working on in that STITT document.

### The work area

The work area in version 1.4c:

![stitt-1-4b-work-area](https://github.com/nickscottprior/stitt/assets/140344267/6289ae9c-7832-48e4-8623-89b815851ef2)

The work area contains a series of automatically numbered blocks. Each block contains a sentence or paragraph of text from the Sanskrit and Tibetan source texts. The dropdown fields in each block are spaces where the translators can insert language correspondences, glosses, a translation of that passage, and any relevant notes. Click on a dropdown field to open it up, and then click on its content to edit it. These dropdown fields can be collectively shown, hidden, opened, or closed using the SHOC buttons in the input menu. The correspondences fields should follow a specific format, which will be discussed in the "correspondence chart buttons" section below. Beside each block is a sidebar menu with four buttons to let you move a given block up or down, delete it, or insert a block immediately below it.

STITT 1.4c comes with three sample blocks already filled in; namely, the first three sentences of Vasubandhu's Pañcaskandhaka. You can delete these blocks before starting your own project. 

At the bottom of the work area is a series of buttons:

* The "**New block**" button adds a new block to the bottom of a document.
* The "**Save current page**" button downloads a version of the current page, but you could also just do Ctrl+S to choose the file's name and location before downloading it.
* The "**Delete blocks in range**" button lets you delete a range of blocks all at once. In the adjacent two boxes, you must first type in the number of the first and last block that you want to delete in order to specify the range. Note that it is not possible to undo deleting a block, so you may want to save a copy of your work before making any big changes.
* The "**Parse HTML**" and "**Purge HTML**" boxes are for advanced users. They let you add and remove custom styling in the dropdown fields using HTML and CSS. This would let you use bolding, italics, underlines, lists, and other kinds of markup.

### The output menu

The output menu in 1.4c:

![stitt-1-4b-output-menu](https://github.com/nickscottprior/stitt/assets/140344267/6ba13e6c-da88-4cae-b359-aacd27bc778c)

The output menu has two sections: the output controls, and the output content. When you click a button in the output controls, the result will display as the output content below.

The output controls have two sections: outputting text from the work area, and outputting text from an input box.

Outputting text from the work area has three sections:
1. Block-by-block buttons;
2. Continuous buttons;
3. Correspondence chart buttons.

The **block-by-block** buttons give you a variety of options for displaying content from the work area in a block-by-block format. For example, you can display your translation, or the Sanskrit text + your translation, or the Tibetan text + your translation, or all three fields at once. This section also lets you display correspondences block-by-block, but it's usually better to use the correspondence chart buttons.

The **continuous** buttons convert the work area content into a continuous text. This is most useful for displaying your translation in a continuous format.

The **correspondence chart** buttons allow you to display the content of the "correspondences" fields as a table that you can copy-paste into other programs. This lets you easily import the correspondences into word-processing software like Microsoft Word, or into a flashcard program like Anki. It is important to note that you must format the correspondence fields in a particular way for these buttons to work. Line breaks are used to mark new rows in the correspondence chart, so each term should be on a different line. You can press "enter" or "return" on your keyboard at the end of a line to insert a line break. Within any individual line, some kind of separator should be used between the different languages. This is because the separator you choose is used to mark new columns in the correspondence chart. STITT currently supports five different separators, so it's best to just pick one and use it consistently throughout all the correspondence fields in the document.

Outputting text from an input menu has three sections:
1. Line-by-line buttons;
2. Continuous buttons,
3. Other buttons

The **line-by-line** buttons allow you to break up a text in the input box into different lines, and display the result below. These buttons preserve any pre-formatted line breaks in the Sanskrit, and insert line breaks after double shads (༎) in the Tibetan. They work much the same as the automatic text importer, but they let you see and control the output without actually inputting it into the work area. This can be useful for text formatting.

The **continuous buttons** allow you to display the content of the input box as a continuous text. This can be useful for text formatting.

There are three other buttons in this section:

* The "**IAST preprocessor**" is only used when you specifically want to convert a GRETIL e-text from IAST to Devanagari before importing it into STITT. It converts text to lower-case and converts slash (/) dandas into vertical bar (|) dandas, which allow the IAST text to be properly picked up and converted using online transliteration converters. This is only necessary for IAST texts in GRETIL format because GRETIL uses capital letters and slash dandas, which deviate from proper IAST conventions.
* The "**Remove extra space & line breaks**" button removes extra spaces and line breaks from a text. This can be used as a pre-processor before importing a non-GRETIL Sanskrit text into STITT, because many non-GRETIL Sanskrit e-texts have lots of extra spaces and line breaks. You could also use this button to remove extra spaces and line breaks from any kind of text, even for things unrelated to STITT or translation.
* The "**Clear output**" button just clears the output content.

### Other notes

If you encounter a technical issue, you can either [email me about it](https://tibetanlanguage.school/) or [post the issue on GitHub](https://github.com/nickscottprior/stitt/issues). I'm always open to any ideas for new features, too.

STITT is **not** a collaborative real-time editor like Google Docs, so it is not possible for multiple people to simultaneously edit a STITT document out-of-the-box.

If multiple people want to collaborate on a STITT document, there are two easy options:

* you could edit the document in turns, and send it to the other person once you're done;
* one person could screenshare their STITT document using a video call program like Zoom or Jitsi, and then type in any input from the other person on the fly.

If you're somewhat tech-savvy, you could use a private GitHub repo to manage version control on a given document, especially if your document has multiple different contributors.

If you're very tech-savvy, you might be able to import a STITT document onto a website and then add collaborative editing support using a program like [TogetherJS](https://togetherjs.com/). You would have to manage access permissions yourself.

(end of notes)








