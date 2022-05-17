# Freely-Given.org

Freely-Given.org is dedicated to creating, curating, converting, and serving **open-licensed
Biblical resources and software** that can be freely used by anyone in the world
wanting to investigate the Bible for themselves
and/or provide such services to others.

Our website is https://Freely-Given.org, established in 2010.

## Contributing

We welcome several kinds of help:

- Assistance in compiling datasets
- Using and checking datasets, and reporting errors that need fixing, or improvements that can be added
- Software developers to improve our proof-of-concept apps and APIs

## "Standards" projects

These are projects where we needed a "standard" dataset for interactions between software components,
and tried to generalise and document our own needs, so that they also might be available for others to consider using.

- [BibleBooksCodes](https://github.com/Freely-Given-org/BibleBooksCodes): An extensive set of three-character consistently-defined codes (like *GEN* and *TH2*) that can be used by computer software to label particular Bible "books" and letters. They're also referenced against the OSIS and USFM Bible book codes, among others. (Note that the codes all start with an UPPERCASE letter, so unlike most other systems, they can also be used as variable names in most computer languages.) The dataset also includes sample implementations in some common computer languages. Used by BibleOrgSys below.
- [BibleVersionCodes](https://github.com/Freely-Given-org/BibleVersionCodes): A list of short Bible abbreviations (like *ASV* and *NIV* and sometimes including extended versions like *NIV-1984*). This repository is intended to be a registry that any Bible publisher can request additions to. Each entry contains minimal information -- the main fields for each abbreviation are just the version name and language. (A separate dataset will contain fuller entries -- this lightweight dataset is mostly to connect the version abbreviation to the name.) The dataset will also include sample implementations in some common computer languages. Will be used by BibleOrgSys below.
- [USFMMarkers](https://github.com/Freely-Given-org/USFMMarkers): A list of USFM3 markers and some related information extracted from the [USFM documents](https://ubsicap.github.io/usfm/) and put into a form that can easily be loaded by software. Used by BibleOrgSys below.

## Specific projects

- [BibleOrgSys](https://github.com/Freely-Given-org/BibleOrgSys): The Bible Organisational System is a Python library that reads, processes, and writes many kinds of B/C/V materials, especially including Bibles and Bible notes and commentaries.
- [Biblelator](https://github.com/Freely-Given-org/Biblelator): A Python and TKinter Bible-translation editor based on the BibleOrgSys. Biblelator can read and write Bible "book" files in MyParatextProjects as well as in its native project folders.

## Forthcoming projects

- [ESFM](https://github.com/Freely-Given-org/ESFM): Enhanced Standard Format Markers -- an attempt to enhance USFM3 to handle encoding of information beyond just Strongs numbers, as well as alternative text, i.e., to have one ESFM file capable of producing multiple USFM files, such as one dataset being able to produce both US spelling and UK spelling versions.
- [Biblelastic](https://github.com/Freely-Given-org/Biblelastic): A planned "fantastic" Bible study app. Designers and coders wanted.

## Glossary

- **B/C/V**: Bible "book" / chapter / verse -- a common method of referencing Bible text as well as related resources such as Bible commentaries
- **BOS**: Bible Organisational System (BibleOrgSys) -- a Python library for processing B/C/V materials such as Bibles and commentaries
