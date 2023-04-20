# Freely-Given.org

Freely-Given.org is dedicated to creating, curating, converting, and serving **open-licensed
Biblical resources and software** that can be freely used by anyone in the world
wanting to investigate the Bible for themselves
and/or provide such services to others.

Also the home of the new, exciting **[Open English Translation](https://github.com/Freely-Given-org/OpenEnglishTranslation--OET)** of the Bible.

Our websites are [Freely-Given.org](https://Freely-Given.org) (established in late 2019) and [OpenEnglishTranslation.Bible](https://OpenEnglishTranslation.Bible) (established in 2023).

## Contributing

We welcome several kinds of help.

For our software:

- Assistance in compiling datasets
- Using and checking datasets, and reporting errors that need fixing, or improvements that can be added
- Software developers to improve our library APIs and proof-of-concept desktop and mobile apps
- Software developers to improve our automatic conversion flows (using GitHub actions) and unit tests

For the **Open English Translation**:

- Bible translators, translation consultants, checkers, notes writers, article writers
- Artists and stylists
- More on [the website](https://OpenEnglishTranslation.Bible/About/Partners)

## Foundational reference and software projects (library)

These are reference projects where we needed a "standard" dataset for interactions between multi-cultural Bible software components.
We have attempted to generalise and document our own needs,
so that they also might be available for others to consider using.

- [USFMMarkers](https://github.com/Freely-Given-org/USFMMarkers): A list of USFM3 markers and some related information extracted from the [USFM documents](https://ubsicap.github.io/usfm/) and put into a form that can easily be loaded by software. Used by BibleOrgSys below.
- [ESFM](https://github.com/Freely-Given-org/ESFM): Enhanced Standard Format Markers -- an attempt to enhance USFM3 to handle encoding of information beyond just Strongs numbers, as well as alternative text, i.e., to have one ESFM file capable of producing multiple USFM files, such as one dataset being able to produce both US spelling and UK spelling versions, or replacing *Jahweh* with *the Lord* (which sometimes requires reordering of the phrase).
- [BibleBooksCodes](https://github.com/Freely-Given-org/BibleBooksCodes): An extensive set of three-character consistently-defined codes (like *GEN* and *TH2*) that can be used internally by computer software to label particular Bible "books" and letters. They're also referenced against the commonly used (but less consistent and less general) **OSIS** and **USFM** Bible book codes, among others. (Note that our codes all start with an UPPERCASE letter, so unlike most other systems, they can also be used as variable names in most computer languages.) The reference XML dataset also includes sample implementations in some common computer languages. Used by BibleOrgSys below.
- [BibleBooksNames](https://github.com/Freely-Given-org/BibleBooksNames): This contains default and alternative book names for different languages and Bible cultures. For example, *Genesis* vs *The First Book of Moses*. Also, some Bibles will use Roman numerals for books like *1 John* and *2 John*, so *I John* and *II John*. But we usually want searches to find either.
- [BibleBooksOrders](https://github.com/Freely-Given-org/BibleBooksOrders): A small language-independent dataset that provides a way to tell Bible software what order books should be displayed to the users, e.g., most New Testaments start with MAT, MRK, LUK, etc., but some [OET](https://OpenEnglishTranslation.Bible) editions use JHN, MAT, MAR, LUK, etc.
- [BiblePunctuationSystems](https://github.com/Freely-Given-org/BiblePunctuationSystems): Punctuation systems for Bibles of various languages and cultures. For example, some languages use a period as a decimal point and commas for marking off thousands, but other languages and cultures do it differently. This repo also defines how chapter:verse references are formatted, including verse lists and ranges.
- [BibleVersificationSystems](https://github.com/Freely-Given-org/BibleVersificationSystems): Reference versification systems for reconstructed Hebrew and Greek "original" texts, along with maps to and from alternative Bible versification schemes. This mapping is required because of mismatches between publications, e.g., some publications list subheaders like "*A psalm of David*" as headers and others list that text as verse 1, so Psalms in some publications appear to have one less or more verse than others.
- [BibleReferences](https://github.com/Freely-Given-org/BibleReferences): A standardised way to refer to a verse or a snippet from a verse in a range of works, e.g., to specify "Open English Translation, Literal Version, Matthew 7:1, words 3-5". Then we also need a way to communicate these standardised references to different user windows, browser tabs, servers, devices, e.g., to translate in one app and view resources in another and have them scroll together, or to use a tablet alongside a laptop to be able to see more translation resources at once.
- ARCHIVED [BibleVersionCodes](https://github.com/Freely-Given-org/BibleVersionCodes): A list of short Bible abbreviations (like *ASV* and *NIV* and sometimes including extended versions like *NIV-1984*). This minimal repository is intended to be a registry that any Bible publisher can request additions to. Each entry contains only basic identifying information -- the main fields for each abbreviation are just the version name and language. (The *Bible Publication Details* dataset below contains fuller entries -- this lightweight dataset here is mostly to connect the version abbreviation to the name where fuller details are not required.) The dataset will also include sample API implementations in some common computer languages. Will be used by BibleOrgSys below. **ARCHIVED because too much overlap with BiblePublicationDetails below -- see [there](https://github.com/Freely-Given-org/BiblePublicationDetails) instead**
- [BiblePublicationDetails](https://github.com/Freely-Given-org/BiblePublicationDetails): A much fuller list of details for the above *Bible Version Codes*, including information on specific editions, e.g., "Women's Study Bible". These details include technical information like character set and punctuation standards, "books" included and their order, and versification system used, as well as supplementary details like contributors, editors, revision history, etc.
- [BibleJSON](https://github.com/Freely-Given-org/BibleJSON): A well thought-out set of JSON formats that Bible files (like ESFM, USX, OSIS, etc.) can be "compiled" to for data interchange and online services and for internal program use. As well as the basic "contents" of a Bible, B/C/V and B/S/P indexes and possibly word indexes will also be defined. A Rust "compiler" will also be supplied.

## Software Applications

- [BibleOrgSys](https://github.com/Freely-Given-org/BibleOrgSys): The *Bible Organisational System* (or *BOS*) is a Python library that reads, processes, and writes many kinds of B/C/V materials, especially including Bibles and Bible notes and commentaries. It can be used to quickly create a Python script to step through and process Bible "books", chapters, verses, etc.
- [Biblelator](https://github.com/Freely-Given-org/Biblelator): A Python and TKinter Bible-translation editor based on the BibleOrgSys. Biblelator can read and write Bible "book" files in MyParatextProjects as well as in its native project folders.
- [Scripted Bible Editor](https://github.com/Freely-Given-org/ScriptedBibleEditor): A Python ESFM/USFM batch editor that applies TSV edit tables to various books or verses as required. (This is used inside a makefile to create the OET Literal Version.)

## Forthcoming projects

- OET Bible app: The [Open English Translation](https://OpenEnglishTranslation.Bible) is designed to have the *Readers' Version* and the *Literal Version* used side-by-side to complement each other. This will require a custom app to handle this and other special features including the many linked datasets.
- [Biblelastic](https://github.com/Freely-Given-org/Biblelastic): A planned "fantastic" Bible-study app. Designers and coders wanted. This endeavour needs to begin with defining linked data sets so that non-B/C/V reference books and courses can also be integrated. (Think "free and open version of your current expensive Bible-study app".)
- [BibleCompiler](https://github.com/Freely-Given-org/BibleCompiler): A set of scripts (including Python and Rust) to compile an ESFM Bible into a pre-parsed, indexed, efficient format suitable for distribution of open-licensed works and also usable for serving them. SQLite3 will be the first target output.
- [BibleTypesetter](https://github.com/Freely-Given-org/BibleTypesetter): A system to typeset a Bible (i.e., produce a beautiful PDF amongst other things) using [SILE](https://sile-typesetter.org/) supplemented by Lua scripts/classes as necessary with minimal user input, i.e., without requiring a full-time typesetter to manually layout every page.

## Glossary

- **B/C/V**: Bible **"book" / chapter / verse** -- a common method of referencing Bible text as well as related resources such as Bible commentaries. However, for user-facing display of Biblical narrative, Freely-Given.org discourages the over-use of the historically popular chapter-based and verse-based ways of thinking as they are "non-logical" and sometimes "non-sensible" historic units (frequently quoted out-of-context).
- **W/B/C/V**: Bible **work / "book" / chapter / verse** -- to meet the need to refer to a text in a specific Bible version
- **B/S/P**: Bible **"book" / section / paragraph** -- an alternative method of referencing Bible text, where logical sections are segments separated by section headings and contain discourse units like paragraphs.
- **BOS**: **Bible Organisational System** (**BibleOrgSys**) -- a Python library for processing B/C/V materials such as Bibles and commentaries (and also provides B/S/P referencing). It can be used to quickly create a Python script to step through and process Bible "books", chapters, verses, etc.

Note: For usable linking between Bible resources, we need to extend B/C/V (and B/S/P) to W/B/C/V (and W/B/S/P), i.e., to have a standard way to link to (and within) other works.
