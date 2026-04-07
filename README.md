## 1893 Syriac Bible Digitalization Project
- A digital preservation and transcription of the 1893 Syriac (Assyrian) Bible, originally published in Urmia.
- All text is encoded in UTF-8 Unicode to ensure compatibility across all modern operating systems and mobile devices.

### Project Goal
The objective of this repository is to provide a complete, accurate, and searchable Unicode text of the 1893 Syriac Bible. This edition is a landmark of 19th-century Neo-Aramaic literature, and this project serves to ensure its availability for scholars, linguists, and the global Assyrian community in a modern digital format.

### Historical Context
The 1893 Syriac Bible was a monumental publication, often associated with the mission press in Urmia. It represents a specific era of the language and serves as a vital bridge between classical ecclesiastical Syriac and the modern spoken dialects (Sureth) of the time.

### Digitization Status
- Current Phase: Transcription/OCR Verification.
- Source: Scanned images from the Boston Public Library / Archive.org.
  - https://archive.org/details/syriacbible00lond

### Repository Structure
#### Complete books
- books/oldtestament.json
- books/newtestament.json
#### Chapters
- books/ot/old testament books (Books 1-39).
- books/nt/new testament books (Books 1–27).

### Legal & Licensing
- This text was published in 1893 and is in the Public Domain.
- Scripture Text: Unrestricted. No copyright is claimed on the underlying historical text.
- Digital Transcription: This specific digital transcription is provided under the Creative Commons Zero (CC0) license, waiving all rights to the work worldwide under copyright law.

## Get data

### BIBLE INFORMATION
```
https://cdn.jsdelivr.net/gh/Abrei852/assyrian-bible-api/assyrian-bible.json
```

##

### OLD TESTAMENT

```
https://cdn.jsdelivr.net/gh/Abrei852/assyrian-bible-api/books/oldtestament.json
```

##

### NEW TESTAMENT
```
https://cdn.jsdelivr.net/gh/Abrei852/assyrian-bible-api/books/newtestament.json
```

##

### BOOK

- Based on **{bookname}.json**
- To get another book, just change **genesis.json** to the book you want for example **exodus.json**

###

**GENESIS**

```
https://cdn.jsdelivr.net/gh/Abrei852/assyrian-bible-api/books/ot/genesis.json
```
##

### CHAPTER

- Based on **{bookname}** & **{chapternumber.json}**
- To get another chapter just change **1.json** to the chapter number you want for example **2.json**

**GENESIS CHAPTER 1**

```
https://cdn.jsdelivr.net/gh/Abrei852/assyrian-bible-api/books/ot/genesis/1.json
```

##

### API DATA STRUCTURE

- BASE URL: **https://cdn.jsdelivr.net/gh/Abrei852/assyrian-bible-api**

##

(GET) {BASE URL/assyrian-bible.json}
```sh
  {
    id: versionCode,
    code: versionCode,
    version: versionName,
    languageEn: languageNameEn,
    languageAs: languageNameAs,
    description: descriptionText,
    testament: new/old,
  }
```

##

(GET) {BASE URL}/books/{old/new}testament.json}
```sh
  {
    testamentEn: testamentNameEn,
    testamentAs: testamentNameAs,
    books: [
      {
        bookNameEn: genesis,
        bookNameAs: ܣܦܪܐ ܕܒܪܝܬܐ.
      },
      ... All books in order
    ]
  }
```

##

(GET) {BASE URL}/books/{ot/nt}/bookname.json}
```sh
  {
    numberEn: bookNumberEn,
    numberAs: bookNumberAs
    bookNameEn: bookNameEn,
    bookNameAs: bookNameAs,
    chapters: [
      {
        chapterNumberEn: 1,
        chapterNumberAs: ܐ
      },
       ... All chapters in book
    ]
  }
```

##

(GET) {BASE URL}/books/{ot/nt}/books/bookname/chapternumber.json}
```sh
  {
    chapterNumberEn: "Chapter " + chapterNumberEn,
    chapterNumberAs: ChapterNumberAs + " :ܩܦܠܐܘܢ",
    verses: [
      {
        verseNumberEn: verseNumberEn,
        verseNumberAs: verseNumberAs,
        subheadingAs: null,
        verseText: verseText,
        isRedLetter: false,
        verseNote: verseNote,
      },
      ... All verses in chapter
    ]
  }
```

##
