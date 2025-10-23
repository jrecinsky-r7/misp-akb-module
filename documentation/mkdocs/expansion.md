
#### [EQL Query Generator](https://github.com/MISP/misp-modules/tree/main/misp_modules/modules/expansion/eql.py)

<img src=../logos/eql.png height=60>

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
