# Home

[![Build status](https://github.com/MISP/misp-modules/actions/workflows/test-package.yml/badge.svg)](https://github.com/MISP/misp-modules/actions/workflows/test-package.yml)[![Coverage Status](https://coveralls.io/repos/github/MISP/misp-modules/badge.svg?branch=main)](https://coveralls.io/github/MISP/misp-modules?branch=main)
[![codecov](https://codecov.io/gh/MISP/misp-modules/branch/main/graph/badge.svg)](https://codecov.io/gh/MISP/misp-modules)

MISP modules are autonomous modules that can be used to extend [MISP](https://github.com/MISP/MISP) for new services such as expansion, import, export and workflow action.

MISP modules can be also installed and used without MISP as a [standalone tool accessible via a convenient web interface](./website).

The modules are written in Python 3 following a simple API interface. The objective is to ease the extensions of MISP functionalities
without modifying core components. The API is available via a simple REST API which is independent from MISP installation or configuration and can be used with other tools.

For more information: [Extending MISP with Python modules](https://www.misp-project.org/misp-training/3.1-misp-modules.pdf) slides from [MISP training](https://github.com/MISP/misp-training).

## Existing MISP modules

### Expansion Modules
* [EQL Query Generator](https://misp.github.io/misp-modules/expansion/#eql-query-generator) - EQL query generation for a MISP attribute.
* [Whois Lookup](https://misp.github.io/misp-modules/expansion/#whois-lookup) - Module to query a local instance of uwhois (https://github.com/rafiot/uwhoisd).

### Export Modules
* [CEF Export](https://misp.github.io/misp-modules/export_mod/#cef-export) - Module to export a MISP event in CEF format.
* [Cisco fireSIGHT blockrule Export](https://misp.github.io/misp-modules/export_mod/#cisco-firesight-blockrule-export) - Module to export malicious network activity attributes to Cisco fireSIGHT manager block rules.
* [Microsoft Defender for Endpoint KQL Export](https://misp.github.io/misp-modules/export_mod/#microsoft-defender-for-endpoint-kql-export) - Defender for Endpoint KQL hunting query export module
* [Lite Export](https://misp.github.io/misp-modules/export_mod/#lite-export) - Lite export of a MISP event.
* [EQL Query Export](https://misp.github.io/misp-modules/export_mod/#eql-query-export) - Export MISP event in Event Query Language
* [Nexthink NXQL Export](https://misp.github.io/misp-modules/export_mod/#nexthink-nxql-export) - Nexthink NXQL query export module
* [OSQuery Export](https://misp.github.io/misp-modules/export_mod/#osquery-export) - OSQuery export of a MISP event.
* [Test Export](https://misp.github.io/misp-modules/export_mod/#test-export) - Skeleton export module.
* [ThreatStream Export](https://misp.github.io/misp-modules/export_mod/#threatstream-export) - Module to export a structured CSV file for uploading to threatStream.
* [ThreadConnect Export](https://misp.github.io/misp-modules/export_mod/#threadconnect-export) - Module to export a structured CSV file for uploading to ThreatConnect.

### Import Modules
* [MISP JSON Import](https://misp.github.io/misp-modules/import_mod/#misp-json-import) - Module to import MISP JSON format for merging MISP events.
* [OCR Import](https://misp.github.io/misp-modules/import_mod/#ocr-import) - Optical Character Recognition (OCR) module for MISP.
* [CSV Test Import](https://misp.github.io/misp-modules/import_mod/#csv-test-import) - Simple CSV import tool with mapable columns
* [ThreadAnalyzer Sandbox Import](https://misp.github.io/misp-modules/import_mod/#threadanalyzer-sandbox-import) - Module to import ThreatAnalyzer archive.zip / analysis.json files.

### Action Modules
* [Test action](https://misp.github.io/misp-modules/action_mod/#test-action) - This module is merely a test, always returning true. Triggers on event publishing.


## How to contribute your own module?

Fork the project, add your module, test it and make a pull-request. Modules can be also private as you can add a module in your own MISP installation.
For further information please see [Contribute](contribute/).


## Licenses
For further Information see also the [license file](license/).
