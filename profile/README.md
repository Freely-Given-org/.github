# Freely-Given.org

Freely-Given.org is dedicated to creating, curating, converting, and serving **open-licensed
Biblical resources and software** that can be freely used by anyone in the world
wanting to investigate the Bible for themselves
and/or provide such services to others.

Our website is https://Freely-Given.org, established in late 2019.

## Contributing

We welcome several kinds of help:

- Assistance in compiling datasets
- Using and checking datasets, and reporting errors that need fixing, or improvements that can be added
- Software developers to improve our proof-of-concept apps and APIs

## Foundational projects

These are reference projects where we needed a "standard" dataset for interactions between multi-cultural Bible software components,
and tried to generalise and document our own needs,
so that they also might be available for others to consider using.

- [USFMMarkers](https://github.com/Freely-Given-org/USFMMarkers): A list of USFM3 markers and some related information extracted from the [USFM documents](https://ubsicap.github.io/usfm/) and put into a form that can easily be loaded by software. Used by BibleOrgSys below.
- [ESFM](https://github.com/Freely-Given-org/ESFM): Enhanced Standard Format Markers -- an attempt to enhance USFM3 to handle encoding of information beyond just Strongs numbers, as well as alternative text, i.e., to have one ESFM file capable of producing multiple USFM files, such as one dataset being able to produce both US spelling and UK spelling versions, or replacing *Jahweh* with *the Lord* (which sometimes requires reordering of the phrase).
- [BibleBooksCodes](https://github.com/Freely-Given-org/BibleBooksCodes): An extensive set of three-character consistently-defined codes (like *GEN* and *TH2*) that can be used by computer software to label particular Bible "books" and letters. They're also referenced against the commonly used (but less consistent and less general) **OSIS** and **USFM** Bible book codes, among others. (Note that our codes all start with an UPPERCASE letter, so unlike most other systems, they can also be used as variable names in most computer languages.) The dataset also includes sample implementations in some common computer languages. Used by BibleOrgSys below.
- [BibleBooksNames](https://github.com/Freely-Given-org/BibleBooksNames): This contains default and alternative book names for different language and Bible cultures. For example, *Genesis* vs *The First Book of Moses*. Also, some Bibles will use Roman numerals for books like *1 John* and *2 John*, so *I John* and *II John*. But we usually want searches to find either.
- [BibleBooksOrders](https://github.com/Freely-Given-org/BibleBooksOrders): A small language-independent dataset that provides a way to tell Bible software what order books should be displayed to the users, e.g., most New Testaments start with MAT, MRK, LUK, etc., but some [OET](https://OpenEnglishTranslation.Bible) editions use JHN, MAT, MAR, LUK, etc.
- [BiblePunctuationSystems](https://github.com/Freely-Given-org/BiblePunctuationSystems): Punctuation systems for Bibles of various languages and cultures. For example, some languages use a period as a decimal point and commas for marking off thousands, but other languages and cultures do it differently. This repo als
- [BibleVersificationSystems](https://github.com/Freely-Given-org/BibleVersificationSystems): Reference versification systems for Hebrew and Greek original texts, along with maps to and from alternative Bible versification schemes. This mapping is required because of mismatches between publications, e.g., some publications list subheaders like "*A psalm of David*" as headers and others list that text as verse 1, so Psalms in some publications appear to have one less or more verse than others.
- [BibleVersionCodes](https://github.com/Freely-Given-org/BibleVersionCodes): A list of short Bible abbreviations (like *ASV* and *NIV* and sometimes including extended versions like *NIV-1984*). This repository is intended to be a registry that any Bible publisher can request additions to. Each entry contains minimal information -- the main fields for each abbreviation are just the version name and language. (A separate dataset will contain fuller entries -- this lightweight dataset is mostly to connect the version abbreviation to the name.) The dataset will also include sample implementations in some common computer languages. Will be used by BibleOrgSys below.
- [BiblePublicationDetails](https://github.com/Freely-Given-org/BiblePublicationDetails): A list of details for the above Bible version codes, including information on specific editions, e.g., "Women's Study Bible". These include technical details like character set and punctuation standards, "books" included and book order, and versification system used, as well as supplementary details like contributors, editors, etc.
- [BibleJSON](https://github.com/Freely-Given-org/BibleJSON): A well thought-out set of JSON formats that Bible files (like ESFM, USX, OSIS, etc.) can be "compiled" to for data interchange and online services and for internal program use. As well as the basic "contents" of a Bible, B/C/V and B/S/P indexes and possibly word indexes will also be defined. A Rust "compiler" will also be supplied.

## User projects

- [BibleOrgSys](https://github.com/Freely-Given-org/BibleOrgSys): The *Bible Organisational System* (or *BOS*) is a Python library that reads, processes, and writes many kinds of B/C/V materials, especially including Bibles and Bible notes and commentaries. It can be used to quickly create a Python script to step through and process Bible "books", chapters, verses, etc.
- [Biblelator](https://github.com/Freely-Given-org/Biblelator): A Python and TKinter Bible-translation editor based on the BibleOrgSys. Biblelator can read and write Bible "book" files in MyParatextProjects as well as in its native project folders.

## Forthcoming projects

- [Biblelastic](https://github.com/Freely-Given-org/Biblelastic): A planned "fantastic" Bible study app. Designers and coders wanted.
- OET Bible app: The [Open English Translation](https://OpenEnglishTranslation.Bible) is designed to have the Literal Version* and the *Readers' Version* used side-by-side to complement each other. This will require a custom app to handle this and other special features.

## Glossary

- **B/C/V**: Bible **"book" / chapter / verse** -- a common method of referencing Bible text as well as related resources such as Bible commentaries. Freely-Given.org discourages the over-use of the historically popular chapter-based and verse-based ways of thinking as they are "non-logical" and sometimes "non-sensible" historic units (now often quoted out-of-context).
- **B/S/P**: Bible **"book" / section / paragraph** -- an alternative method of referencing Bible text, where logical sections are segments separated by section headings and contain discourse units like paragraphs.
- **BOS**: **Bible Organisational System** (**BibleOrgSys**) -- a Python library for processing B/C/V materials such as Bibles and commentaries (and also provides B/S/P referencing).
