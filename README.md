# ASSYRIAN BIBLE API

**WORK IN PROGRESS!**

- **SOME LINKS MAY NOT WORK** 

- **FILE AND FOLDER STRUCTURE MAY CHANGE**

##

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

- Based on **{bookname}.json** & **{chapternumber.json}**
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

(GET) {BASE URL/assyrian-bible.json/books/{old/new}testament.json}
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

(GET) {BASE URL/assyrian-bible.json/books/{ot/nt}/bookname.json}
```sh
  {
    numberEn: bookNumberEn,
    numberAS: bookNumberAS
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

(GET) {BASE URL/assyrian-bible.json/books/{ot/nt}/books/bookname/chapternumber.json}
```sh
  {
    chapterNumberEn: "Chapter " + chapterNumberEn,
    chapternumberAs: ChapterNumberAs + " :ܩܦܠܐܘܢ",
    verses: [
      {
        verseNumberEn: verseNumberEn,
        verseNumberAs: verseNumberAs,
        verseText: versetext,
        verseNote: verseNote,
      },
      ... All verses in chapter
    ]
  }
```

##
