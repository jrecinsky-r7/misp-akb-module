
#### [MISP JSON Import](https://github.com/MISP/misp-modules/tree/main/misp_modules/modules/import_mod/mispjson.py)

Module to import MISP JSON format for merging MISP events.
[[source code](https://github.com/MISP/misp-modules/tree/main/misp_modules/modules/import_mod/mispjson.py)]

- **features**:
>The module simply imports MISP Attributes from an other MISP Event in order to merge events together. There is thus no special feature to make it work.

- **input**:
>MISP Event

- **output**:
>MISP Event attributes

-----

#### [OCR Import](https://github.com/MISP/misp-modules/tree/main/misp_modules/modules/import_mod/ocr.py)

Optical Character Recognition (OCR) module for MISP.
[[source code](https://github.com/MISP/misp-modules/tree/main/misp_modules/modules/import_mod/ocr.py)]

- **features**:
>The module tries to recognize some text from an image and import the result as a freetext attribute, there is then no special feature asked to users to make it work.

- **input**:
>Image

- **output**:
>freetext MISP attribute

-----

#### [CSV Test Import](https://github.com/MISP/misp-modules/tree/main/misp_modules/modules/import_mod/testimport.py)

Simple CSV import tool with mapable columns
[[source code](https://github.com/MISP/misp-modules/tree/main/misp_modules/modules/import_mod/testimport.py)]

- **features**:
>

-----

#### [ThreadAnalyzer Sandbox Import](https://github.com/MISP/misp-modules/tree/main/misp_modules/modules/import_mod/threatanalyzer_import.py)

Module to import ThreatAnalyzer archive.zip / analysis.json files.
[[source code](https://github.com/MISP/misp-modules/tree/main/misp_modules/modules/import_mod/threatanalyzer_import.py)]

- **features**:
>The module imports MISP Attributes from a ThreatAnalyzer format file. This file can be either ZIP, or JSON format.
>There is by the way no special feature for users to make the module work.

- **input**:
>ThreatAnalyzer format file

- **output**:
>MISP Event attributes

- **references**:
>https://www.threattrack.com/malware-analysis.aspx

-----
