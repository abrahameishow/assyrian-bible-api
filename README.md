## 1893 Syriac Bible Digitalization Project
- A digital preservation and transcription of the 1893 Syriac (Assyrian) Bible, originally published in Urmia.
- All text is encoded in UTF-8 Unicode to ensure compatibility across all modern operating systems and mobile devices.

### Project Goal
The objective of this repository is to provide a complete, accurate, and searchable Unicode text of the 1893 Syriac Bible. This edition is a landmark of 19th-century Neo-Aramaic literature, and this project serves to ensure its availability for scholars, linguists, and the global Assyrian community in a modern digital format.

### Historical Context
The 1893 Syriac Bible was a monumental publication, often associated with the mission press in Urmia. It represents a specific era of the language and serves as a vital bridge between classical ecclesiastical Syriac and the modern spoken dialects (Sureth) of the time.

### Digitization Status
- **Current Phase:** Transcription/OCR Verification.
- **Source:** Scanned images from the [Boston Public Library / Archive.org](https://archive.org/details/syriacbible00lond).
- **Book-by-Book Status:**
  
  - **Old Testament**
    - 🟢 Genesis
    - 🟢 Malachi
    - 🟡 Exodus (In Progress...)
    - 🟡 Psalms (In Progress...)
      
  - **New Testament**
    - 🟢 Philemon
    - 🟢 Jude

### Repository Structure
- **books/oldtestament.json:** Metadata for the Old Testament.
- **books/newtestament.json:** Metadata for the New Testament.
- **books/ot/:** Individual JSON files for Old Testament books (1–39).
- **books/nt/:** Individual JSON files for New Testament books (1–27).

### Legal & Licensing
This text was published in 1893 and is in the Public Domain.
- **Scripture Text:** This text was originally published in 1893 and is in the Public Domain. Use of the underlying historical text is unrestricted.
- **​Digital Edition & API:** The digital transcription, JSON data structures, and organizational code in this repository are licensed under the MIT License.

## Get data (API Access)
**Base URL:** https://cdn.jsdelivr.net/gh/Abrei852/assyrian-bible-api

#### 1. Bible information
`GET {BASE URL}/assyrian-bible.json`
```sh
{
  "id": "aii",
  "code": "aii",
  "version": "Assyrian/Syriac",
  "languageEn": "Suret",
  "languageAs": "ܣܘܪܝܬ",
  "description": "This is the Assyrian version of the bible",
  "testament": "Old Testament & New Testament"
}
```

#### 2. Testament metadata
`GET {BASE URL}/books/oldtestament.json`
```sh
{
  "testamentEn": "Old testament",
  "testamentAs": "ܟܬܒ̣̈ܐ ܕܕܝܬܩܐ ܥܬܝܩܬܐ",
  "books": [
    {
      "bookNameEn": "genesis",
      "bookNameAs": "ܣܦܪܐ ܕܒܪܝܬܐ."
    },
    ... All books in order
  ]
}
```

#### 3. Individual Book Data
`GET {BASE URL}/books/ot/genesis.json`
```sh
{
  "numberEn": "1",
  "numberAs": "ܐ",
  "bookNameEn": "genesis",
  "bookNameAs": "ܣܦܪܐ ܕܒܪܝܬܐ.",
  "chapters": [
    {
      "en": "1",
      "as": "ܐ"
    },
     ... All chapters in book
  ]
}
```
#### 4. Chapter content
`GET {BASE URL}/books/ot/genesis/1.json`
```sh
{
  "chapterEn": "Chapter 1",
  "chapterAs": "ܩܦܠܐܘܢ؛ ܐ",
  "verses": [
    {
      "verseNumberEn": "1",
      "verseNumberAs": "ܐ",
      "subheadingAs": "",
      "verseText": "ܒܪܵܫܝܼܬ ܒܪܹܠܹܐ ܐܲܠܵܗܵܐ ܠܫܡܲܝܵܐ ܘܠܲܐܪܥܵܐ",
      "isRedLetter": false,
      "verseNote": "",
    },
    ... All verses in chapter
  ]
}
```
