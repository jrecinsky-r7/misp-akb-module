# MISP modules documentation

## Expansion Modules

#### [EQL Query Generator](https://github.com/MISP/misp-modules/tree/main/misp_modules/modules/expansion/eql.py)

<img src=logos/eql.png height=60>

EQL query generation for a MISP attribute.
[[source code](https://github.com/MISP/misp-modules/tree/main/misp_modules/modules/expansion/eql.py)]

- **features**:
>This module adds a new attribute to a MISP event containing an EQL query for a network or file attribute.

- **input**:
>A filename or ip attribute.

- **output**:
>Attribute containing EQL for a network or file attribute.

- **references**:
>https://eql.readthedocs.io/en/latest/

-----

#### [Whois Lookup](https://github.com/MISP/misp-modules/tree/main/misp_modules/modules/expansion/whois.py)

Module to query a local instance of uwhois (https://github.com/rafiot/uwhoisd).
[[source code](https://github.com/MISP/misp-modules/tree/main/misp_modules/modules/expansion/whois.py)]

- **features**:
>This module takes a domain or IP address attribute as input and queries a 'Univseral Whois proxy server' to get the correct details of the Whois query on the input value (check the references for more details about this whois server).

- **config**:
> - server
> - port

- **input**:
>A domain or IP address attribute.

- **output**:
>Text describing the result of a whois request for the input value.

- **references**:
>https://github.com/Lookyloo/uwhoisd

- **requirements**:
>uwhois: A whois python library

-----

## Export Modules

#### [CEF Export](https://github.com/MISP/misp-modules/tree/main/misp_modules/modules/export_mod/cef_export.py)

Module to export a MISP event in CEF format.
[[source code](https://github.com/MISP/misp-modules/tree/main/misp_modules/modules/export_mod/cef_export.py)]

- **features**:
>The module takes a MISP event in input, to look every attribute. Each attribute matching with some predefined types is then exported in Common Event Format.
>Thus, there is no particular feature concerning MISP Events since any event can be exported. However, 4 configuration parameters recognized by CEF format are required and should be provided by users before exporting data: the device vendor, product and version, as well as the default severity of data.

- **config**:
> - Default_Severity
> - Device_Vendor
> - Device_Product
> - Device_Version

- **input**:
>MISP Event attributes

- **output**:
>Common Event Format file

- **references**:
>https://community.softwaregrp.com/t5/ArcSight-Connectors/ArcSight-Common-Event-Format-CEF-Guide/ta-p/1589306?attachment-id=65537

-----

#### [Cisco fireSIGHT blockrule Export](https://github.com/MISP/misp-modules/tree/main/misp_modules/modules/export_mod/cisco_firesight_manager_ACL_rule_export.py)

<img src=logos/cisco.png height=60>

Module to export malicious network activity attributes to Cisco fireSIGHT manager block rules.
[[source code](https://github.com/MISP/misp-modules/tree/main/misp_modules/modules/export_mod/cisco_firesight_manager_ACL_rule_export.py)]

- **features**:
>The module goes through the attributes to find all the network activity ones in order to create block rules for the Cisco fireSIGHT manager.

- **config**:
> - fmc_ip_addr
> - fmc_login
> - fmc_pass
> - domain_id
> - acpolicy_id

- **input**:
>Network activity attributes (IPs, URLs).

- **output**:
>Cisco fireSIGHT manager block rules.

- **requirements**:
>Firesight manager console credentials

-----

#### [Microsoft Defender for Endpoint KQL Export](https://github.com/MISP/misp-modules/tree/main/misp_modules/modules/export_mod/defender_endpoint_export.py)

<img src=logos/defender_endpoint.png height=60>

Defender for Endpoint KQL hunting query export module
[[source code](https://github.com/MISP/misp-modules/tree/main/misp_modules/modules/export_mod/defender_endpoint_export.py)]

- **features**:
>This module export an event as Defender for Endpoint KQL queries that can then be used in your own python3 or Powershell tool. If you are using Microsoft Sentinel, you can directly connect your MISP instance to Sentinel and then create queries using the `ThreatIntelligenceIndicator` table to match events against imported IOC.

- **config**:
>Period

- **input**:
>MISP Event attributes

- **output**:
>Defender for Endpoint KQL queries

- **references**:
>https://docs.microsoft.com/en-us/windows/security/threat-protection/microsoft-defender-atp/advanced-hunting-schema-reference

-----

#### [Lite Export](https://github.com/MISP/misp-modules/tree/main/misp_modules/modules/export_mod/liteexport.py)

Lite export of a MISP event.
[[source code](https://github.com/MISP/misp-modules/tree/main/misp_modules/modules/export_mod/liteexport.py)]

- **features**:
>This module is simply producing a json MISP event format file, but exporting only Attributes from the Event. Thus, MISP Events exported with this module should have attributes that are not internal references, otherwise the resulting event would be empty.

- **config**:
>indent_json_export

- **input**:
>MISP Event attributes

- **output**:
>Lite MISP Event

-----

#### [EQL Query Export](https://github.com/MISP/misp-modules/tree/main/misp_modules/modules/export_mod/mass_eql_export.py)

<img src=logos/eql.png height=60>

Export MISP event in Event Query Language
[[source code](https://github.com/MISP/misp-modules/tree/main/misp_modules/modules/export_mod/mass_eql_export.py)]

- **features**:
>This module produces EQL queries for all relevant attributes in a MISP event.

- **input**:
>MISP Event attributes

- **output**:
>Text file containing one or more EQL queries

- **references**:
>https://eql.readthedocs.io/en/latest/

-----

#### [Nexthink NXQL Export](https://github.com/MISP/misp-modules/tree/main/misp_modules/modules/export_mod/nexthinkexport.py)

<img src=logos/nexthink.svg height=60>

Nexthink NXQL query export module
[[source code](https://github.com/MISP/misp-modules/tree/main/misp_modules/modules/export_mod/nexthinkexport.py)]

- **features**:
>This module export an event as Nexthink NXQL queries that can then be used in your own python3 tool or from wget/powershell

- **config**:
>Period

- **input**:
>MISP Event attributes

- **output**:
>Nexthink NXQL queries

- **references**:
>https://doc.nexthink.com/Documentation/Nexthink/latest/APIAndIntegrations/IntroducingtheWebAPIV2

-----

#### [OSQuery Export](https://github.com/MISP/misp-modules/tree/main/misp_modules/modules/export_mod/osqueryexport.py)

<img src=logos/osquery.png height=60>

OSQuery export of a MISP event.
[[source code](https://github.com/MISP/misp-modules/tree/main/misp_modules/modules/export_mod/osqueryexport.py)]

- **features**:
>This module export an event as osquery queries that can be used in packs or in fleet management solution like Kolide.

- **input**:
>MISP Event attributes

- **output**:
>osquery SQL queries

-----

#### [Test Export](https://github.com/MISP/misp-modules/tree/main/misp_modules/modules/export_mod/testexport.py)

Skeleton export module.
[[source code](https://github.com/MISP/misp-modules/tree/main/misp_modules/modules/export_mod/testexport.py)]

- **features**:
>

-----

#### [ThreatStream Export](https://github.com/MISP/misp-modules/tree/main/misp_modules/modules/export_mod/threatStream_misp_export.py)

<img src=logos/threatstream.png height=60>

Module to export a structured CSV file for uploading to threatStream.
[[source code](https://github.com/MISP/misp-modules/tree/main/misp_modules/modules/export_mod/threatStream_misp_export.py)]

- **features**:
>The module takes a MISP event in input, to look every attribute. Each attribute matching with some predefined types is then exported in a CSV format recognized by ThreatStream.

- **input**:
>MISP Event attributes

- **output**:
>ThreatStream CSV format file

- **references**:
> - https://www.anomali.com/platform/threatstream
> - https://github.com/threatstream

- **requirements**:
>csv

-----

#### [ThreadConnect Export](https://github.com/MISP/misp-modules/tree/main/misp_modules/modules/export_mod/threat_connect_export.py)

<img src=logos/threatconnect.png height=60>

Module to export a structured CSV file for uploading to ThreatConnect.
[[source code](https://github.com/MISP/misp-modules/tree/main/misp_modules/modules/export_mod/threat_connect_export.py)]

- **features**:
>The module takes a MISP event in input, to look every attribute. Each attribute matching with some predefined types is then exported in a CSV format recognized by ThreatConnect.
>Users should then provide, as module configuration, the source of data they export, because it is required by the output format.

- **config**:
>Default_Source

- **input**:
>MISP Event attributes

- **output**:
>ThreatConnect CSV format file

- **references**:
>https://www.threatconnect.com

- **requirements**:
>csv

-----

## Import Modules

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

## Action Modules

#### [Test action](https://github.com/MISP/misp-modules/tree/main/misp_modules/modules/action_mod/testaction.py)

This module is merely a test, always returning true. Triggers on event publishing.
[[source code](https://github.com/MISP/misp-modules/tree/main/misp_modules/modules/action_mod/testaction.py)]

- **features**:
>

- **config**:
>{'params': {'foo': {'type': 'string', 'description': 'blablabla', 'value': 'xyz'}, 'Data extraction path': {'type': 'hash_path', 'description': 'Only post content extracted from this path', 'value': 'Attribute.{n}.AttributeTag.{n}.Tag.name'}}, 'blocking': False, 'support_filters': False, 'expect_misp_core_format': False}

-----
