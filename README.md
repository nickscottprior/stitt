# STITT

STITT is a program for working with interlinear textual data. It provides a structured user interface for inputting and annotating interlinear text. It includes fields for source texts, language correspondences, glosses, translations, and notes.

![Screenshot of STITT](/stitt-screenshot-1.png)

## Benefits

### General benefits

STITT was originally developed for working with Tibetan translations of Sanskrit Buddhist texts. It has several benefits over standard word-processing software, including:

* A simple UI to minimize distractions
* Collapsible sections to show or hide data as needed
* A hierarchical HTML-based data structure to allow for easy data extraction

The hierarchical data structure is a technical point, but it is particularly important. It will ultimately allow STITT to extract interlinear data in a variety of different formats at the click of a button. This has not been implemented yet, but once it has, you will be able to:

1. Extract any of the data fields as interlinear text, continuous text, or chunked text, depending on what you need;
2. Maintain data in only one place (your STITT document) and generate derivative document versions automatically, instead of trying to manually maintain several different versions of the data simultaneously;
3. Input data from your STITT document into digital linguistics tools such as [xigt (eXtensible Interlinear Glossed Text)](https://github.com/xigt/xigt) or the [DLx JavaScript Library](https://github.com/digitallinguistics/javascript).

The flexibility in textual layout will allow you, for example, to write your translation line-by-line in the STITT user interface, and then click a button to collect those lines and convert them into a single continuous text. This is much easier than manually copy-pasting each individual line if you decide you want to change your document layout.

You would also be able to convert the lines into chunked text with a certain amount of lines in a chunk. This would make it easy to create a parallel text with one language on one page and the other language on the opposite page.

You could also combine these different extraction methods to create a continuous or chunked document that supports line-by-line user interaction, such as highlighting a sentence in a source text to see its English translation.

These features are not yet present in STITT, but I hope to add them later, karma permitting.

### Portability and extensibility

STITT is written in three coding languages: HTML, CSS, and JavaScript. These are the three basic languages of the internet, so they are supported by a wide range of different software. This allows STITT to be portable, meaning that you can write data in STITT and then export it easily into office programs, websites, or other kinds of software. It also makes STITT extensible, which means that it can easily accommodate new features thanks to the many resources, libraries, and features that are available for these three languages.

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

You can "save" a STITT document by clicking the "download current page" button at the bottom of the document. This downloads a copy of the current page, with all new user input included. The original document that you opened remains unchanged.

If you're tech-savvy, you could use a private GitHub repo to manage version control on a given document, especially if your document has multiple different contributors.

## Planned features

I eventually plan to add the following features:

* Extracting data fields as an interlinear, chunked, or continuous text;
* Deleting a block;
* Adding a block anywhere in the document;
* Allowing users to customize the components and labels in a block;
* Markdown support to let users format text fields;
* Dark mode;
* Importing related open-source software;
* Implementing version numbers for different versions of STITT;
* Adding support for forward compatibility.

Many of these tasks can already be done by directly editing the code. As a stop-gap measure, I plan to create short guides on how to edit the code to resolve the most important issues. Any such guides will be posted here.
