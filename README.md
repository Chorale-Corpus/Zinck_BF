# Zinck_BF


## File formats

Information related to one and the same chorale is represented in multiple variants and formats.
Each comes with its own advantages and disadvantages and users should make informed choices.
Filenames function as IDs in this context in the sense that files representing (information from)
the same chorale share the same filename prefix.

### Authoritative file format: MSCX

At the moment, only one file format in this dataset can be trusted to contain the full amount of 
information to the highest degree of accuracy: the uncompressed MuseScore files ending on 
`.mscx` which can be opened with MuseScore 3 or 4.
To date, we allow modification of these files using 
[MuseScore version 3.6.2](https://github.com/musescore/MuseScore/releases/tag/v3.6.2) exclusively.
However, we use the latest version of MuseScore 4 
(v4.4.4 at the time of writing this in February 2025) to convert these files to MEI and musicXML.
Apart from these format, the information from the MuseScore files is accessible by means of 
tabular files in TSV format, 3 per chorale: `*.notes.tsv`, `*.measures.tsv`, and `*.chords.tsv`
(although the naming of the last is misleading as it contains mainly markup, lyrics, bass figures, etc.).

The latest version of the Python library `ms3` is used to batch convert the MuseScore files
to other formats (`ms3 convert`) and to extract score information to TSV files (`ms3 extract`).

### MEI

To date, MuseScore 4 is able to convert files to MEI Basic 5.0 format. Take these files with a 
grain of salt as we cannot guarantee congruence with the source files.
The quality of these files makes them unsuitable for music research but they may serve as a 
starting point for a well-curated scholarly edition.
In the long run, provided the maturing of the relevant tools, the MEI files should take on 
the role of being the authoritative format.
Until then, they should not be manually modified because they are to be re-generated by conversion
and overwritten once the authoritative MuseScore files are modified.

### musicXML

For convenience and in addition, we offer the chorales in musicXML format. However, experience
shows that musicXML files output by MuseScore come with a number of issues and conversion errors.
These files are unsuited for scholarly work but some users may still appreciate their availability.

### TSV files

Tab-separated files are a dialect of CSV files and can be used the exact same way.
The most convenient way of viewing them is through a spreadsheet program such as LibreOffice Calc
(Excel, Numbers, Sheets, etc.) or a text editor with TSV support/plugin.
Power users may want to load them in their favourite programming language or statistical software.

You can look up what any column means in the documentation of ms3: https://ms3.readthedocs.io/columns

The most important TSV file is called `metadata.tsv`. It contains one row per chorale,
and comes with a number of columns that describe the piece in numerous ways.
A synoptic overview of the most important columns can be found 
[here](https://dcmlab.github.io/mozart_piano_sonatas/#how-to-read-metadata-tsv).


## Overview
|        file_name        |measures|labels|
|-------------------------|-------:|-----:|
|A-MCAU_ZI1785-001_SID039 |      10|     0|
|A-MCAU_ZI1785-002a_SID008|      15|     0|
|A-MCAU_ZI1785-002b       |      14|     0|
|A-MCAU_ZI1785-002c       |      14|     0|
|A-MCAU_ZI1785-003_SID092 |      10|     0|
|A-MCAU_ZI1785-004_SID032 |       9|     0|
|A-MCAU_ZI1785-005_SID006 |      14|     0|
|A-MCAU_ZI1785-006_SID047 |      11|     0|
|A-MCAU_ZI1785-007_SID074 |      12|     0|
|A-MCAU_ZI1785-008        |      13|     0|
|A-MCAU_ZI1785-009_SID036 |      10|     0|
|A-MCAU_ZI1785-010a_SID048|       9|     0|
|A-MCAU_ZI1785-010b       |       9|     0|
|A-MCAU_ZI1785-011a       |      10|     0|
|A-MCAU_ZI1785-011b_SID080|      10|     0|
|A-MCAU_ZI1785-011c       |      11|     0|
|A-MCAU_ZI1785-012_SID086 |      14|     0|
|A-MCAU_ZI1785-013_SID091 |      15|     0|
|A-MCAU_ZI1785-014a       |      13|     0|
|A-MCAU_ZI1785-014b       |      12|     0|
|A-MCAU_ZI1785-015_SID066 |      14|     0|
|A-MCAU_ZI1785-016a_SID053|      13|     0|
|A-MCAU_ZI1785-016b       |      13|     0|
|A-MCAU_ZI1785-017_SID094 |      12|     0|
|A-MCAU_ZI1785-018_SID090 |      12|     0|
|A-MCAU_ZI1785-019_SID058 |      17|     0|
|A-MCAU_ZI1785-020_SID060 |      13|     0|
|A-MCAU_ZI1785-021_SID042 |      13|     0|
|A-MCAU_ZI1785-022        |      17|     0|
|A-MCAU_ZI1785-023_SID029 |      14|     0|
|A-MCAU_ZI1785-024_SID025 |      13|     0|
|A-MCAU_ZI1785-025_SID035 |      10|     0|
|A-MCAU_ZI1785-026_SID065 |      15|     0|
|A-MCAU_ZI1785-027a_SID018|      15|     0|
|A-MCAU_ZI1785-027b       |      11|     0|
|A-MCAU_ZI1785-027c       |      10|     0|
|A-MCAU_ZI1785-028a       |      10|     0|
|A-MCAU_ZI1785-028b_SID071|      10|     0|
|A-MCAU_ZI1785-029_SID072 |      14|     0|
|A-MCAU_ZI1785-030_SID031 |      29|     0|
|A-MCAU_ZI1785-031_SID088 |      10|     0|
|A-MCAU_ZI1785-032        |      11|     0|
|A-MCAU_ZI1785-033_SID012 |      18|     0|
|A-MCAU_ZI1785-034_SID055 |       8|     0|
|A-MCAU_ZI1785-035_SID015 |      15|     0|
|A-MCAU_ZI1785-036_SID026 |      13|     0|
|A-MCAU_ZI1785-037_SID083 |      13|     0|
|A-MCAU_ZI1785-038_SID057 |      23|     0|
|A-MCAU_ZI1785-039_SID054 |      13|     0|
|A-MCAU_ZI1785-040_SID073 |      19|     0|
|A-MCAU_ZI1785-041_SID020 |      20|     0|
|A-MCAU_ZI1785-042_SID093 |      10|     0|
|A-MCAU_ZI1785-043_SID014 |      16|     0|
|A-MCAU_ZI1785-044        |      14|     0|
|A-MCAU_ZI1785-045_SID004 |      13|     0|
|A-MCAU_ZI1785-046_SID084 |      25|     0|
|A-MCAU_ZI1785-047_SID096 |      23|     0|
|A-MCAU_ZI1785-048a       |      19|     0|
|A-MCAU_ZI1785-048b       |      19|     0|
|A-MCAU_ZI1785-049_SID045 |      25|     0|
|A-MCAU_ZI1785-050_SID030 |      11|     0|
|A-MCAU_ZI1785-051        |      17|     0|
|A-MCAU_ZI1785-052        |      20|     0|
|A-MCAU_ZI1785-053_SID034 |     104|     0|
|A-MCAU_ZI1785-054        |      14|     0|
|A-MCAU_ZI1785-055a_SID095|      15|     0|
|A-MCAU_ZI1785-055b       |      12|     0|
|A-MCAU_ZI1785-055c_SID097|      15|     0|
|A-MCAU_ZI1785-056_SID041 |      16|     0|
|A-MCAU_ZI1785-057_SID081 |      16|     0|
|A-MCAU_ZI1785-058        |      16|     0|
|A-MCAU_ZI1785-059a_SID076|       7|     0|
|A-MCAU_ZI1785-059b       |       7|     0|
|A-MCAU_ZI1785-060_SID069 |      15|     0|
|A-MCAU_ZI1785-061        |       9|     0|
|A-MCAU_ZI1785-062        |      12|     0|
|A-MCAU_ZI1785-063        |      17|     0|
|A-MCAU_ZI1785-064        |      12|     0|
|A-MCAU_ZI1785-065a_SID077|      15|     0|
|A-MCAU_ZI1785-065b_SID017|      15|     0|
|A-MCAU_ZI1785-066_SID023 |      15|     0|
|A-MCAU_ZI1785-067a       |      10|     0|
|A-MCAU_ZI1785-067b_SID024|      10|     0|
|A-MCAU_ZI1785-068_SID059 |      13|     0|
|A-MCAU_ZI1785-069_SID007 |      13|     0|
|A-MCAU_ZI1785-070_SID002 |      13|     0|
|A-MCAU_ZI1785-071a_SID050|      13|     0|
|A-MCAU_ZI1785-071b       |      13|     0|
|A-MCAU_ZI1785-072        |      11|     0|
|A-MCAU_ZI1785-073_SID037 |      13|     0|
|A-MCAU_ZI1785-074        |      14|     0|
|A-MCAU_ZI1785-075_SID043 |      13|     0|
|A-MCAU_ZI1785-076a       |       8|     0|
|A-MCAU_ZI1785-076b       |       9|     0|
|A-MCAU_ZI1785-077_SID019 |      19|     0|
|A-MCAU_ZI1785-078a       |      13|     0|
|A-MCAU_ZI1785-078b       |      13|     0|
|A-MCAU_ZI1785-078c       |      13|     0|
|A-MCAU_ZI1785-079a       |      12|     0|
|A-MCAU_ZI1785-079b       |      13|     0|
|A-MCAU_ZI1785-080_SID062 |      10|     0|
|A-MCAU_ZI1785-081_SID078 |      13|     0|
|A-MCAU_ZI1785-082a       |       9|     0|
|A-MCAU_ZI1785-082b_SID089|       9|     0|
|A-MCAU_ZI1785-083_SID038 |      25|     0|
|A-MCAU_ZI1785-084_SID082 |      23|     0|
|A-MCAU_ZI1785-085_SID013 |       9|     0|
|A-MCAU_ZI1785-086_SID061 |      13|     0|
|A-MCAU_ZI1785-087        |       7|     0|
|A-MCAU_ZI1785-088_SID051 |      25|     0|
|A-MCAU_ZI1785-089_SID067 |      17|     0|
|A-MCAU_ZI1785-090_SID010 |      11|     0|
|A-MCAU_ZI1785-091a_SID044|      12|     0|
|A-MCAU_ZI1785-091b       |      11|     0|
|A-MCAU_ZI1785-092_SID011 |      14|     0|
|A-MCAU_ZI1785-093        |      13|     0|
|A-MCAU_ZI1785-094_SID009 |      11|     0|
|A-MCAU_ZI1785-095_SID001 |      11|     0|
|A-MCAU_ZI1785-096_SID052 |      14|     0|
|A-MCAU_ZI1785-097_SID046 |      15|     0|
|A-MCAU_ZI1785-098_SID028 |      18|     0|
|A-MCAU_ZI1785-099_SID016 |      12|     0|
|A-MCAU_ZI1785-100_SID033 |      12|     0|
|A-MCAU_ZI1785-101_SID075 |      13|     0|
|A-MCAU_ZI1785-102        |      11|     0|
|A-MCAU_ZI1785-103        |      10|     0|
|A-MCAU_ZI1785-104        |      14|     0|
|A-MCAU_ZI1785-105_SID085 |      13|     0|
|A-MCAU_ZI1785-106        |      12|     0|
|A-MCAU_ZI1785-107        |      14|     0|
|A-MCAU_ZI1785-108_SID068 |      10|     0|
|A-MCAU_ZI1785-109        |      16|     0|
|A-MCAU_ZI1785-110_SID021 |      15|     0|
|A-MCAU_ZI1785-111_SID064 |      21|     0|
|A-MCAU_ZI1785-112_SID005 |      17|     0|
|A-MCAU_ZI1785-113        |      16|     0|
|A-MCAU_ZI1785-114_SID022 |      10|     0|
|A-MCAU_ZI1785-115_SID027 |      13|     0|
|A-MCAU_ZI1785-116_SID049 |      22|     0|
|A-MCAU_ZI1785-117_SID063 |      11|     0|
|A-MCAU_ZI1785-118        |      12|     0|
|A-MCAU_ZI1785-119a_SID040|      12|     0|
|A-MCAU_ZI1785-119b       |      13|     0|
|A-MCAU_ZI1785-120_SID056 |      10|     0|
|A-MCAU_ZI1785-121        |      11|     0|
|A-MCAU_ZI1785-122        |      17|     0|
|A-MCAU_ZI1785-123        |      48|     0|
|A-MCAU_ZI1785-124        |      14|     0|
|A-MCAU_ZI1785-125        |      17|     0|
|A-MCAU_ZI1785-126        |      12|     0|
|A-MCAU_ZI1785-127_SID003 |      12|     0|
|A-MCAU_ZI1785-128_SID079 |      10|     0|
|A-MCAU_ZI1785-129        |      15|     0|
|A-MCAU_ZI1785-130        |      19|     0|
|A-MCAU_ZI1785-131        |      10|     0|
|A-MCAU_ZI1785-132        |      10|     0|
|A-MCAU_ZI1785-133        |       9|     0|
|A-MCAU_ZI1785-134_SID070 |      13|     0|
|A-MCAU_ZI1785-135        |      21|     0|
|A-MCAU_ZI1785-136_SID087 |      17|     0|
|A-MCAU_ZI1785-137        |     621|     0|
|A-MCAU_ZI1785-138        |     597|     0|


*Overview table automatically updated using [ms3](https://ms3.readthedocs.io/).*
