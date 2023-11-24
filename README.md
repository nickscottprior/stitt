# STITT

STITT is a program for working with interlinear textual data. It provides a structured user interface for inputting, annotating, and processing interlinear text. It includes fields for source texts, language correspondences, glosses, translations, and notes.

Screenshot of STITT version 1.2:

![Screenshot of STITT](/stitt-screenshot-1.png)

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

## How to use STITT

You don't need to know coding to use STITT. It opens in your web browser and has an interactive user interface.

To use STITT, click on [stitt.html](/stitt.html) and then click on the download icon in the top right to download the raw file:

![Screenshot of the download button](/download-raw-file.png)

You can then double-click the downloaded file to open the program in a web browser.

STITT is a local file, not a website. It is stored on your computer but opened in a web browser. As a result, it functions even if you have no internet connection.

Because STITT is a local HTML file, it will not update automatically and you may end up using an out-of-date version. This shouldn't cause any issues, but you wouldn't want to miss out on new features :) I recommend checking this page periodically to see if there have been any new updates since you last downloaded STITT.

You can "save" a STITT document by typing ctrl+s or clicking the "download current page" button at the bottom of the document. This downloads a copy of the current page, with all new user input included. The original document that you opened remains unchanged. I recommend clicking on "show all fields" and "close all fields" before saving.

If you're tech-savvy, you could use a private GitHub repo to manage version control on a given document, especially if your document has multiple different contributors.

## Planned features

I would eventually like to add the following features:

* Extracting data fields as chunked text;
* Customizing the fields in a block;
* Dark mode;
* Importing related open-source software;
* Adding support for forward compatibility;
* Incorporating open-source linguistics software.
