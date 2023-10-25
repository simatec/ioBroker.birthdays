![Logo](admin/birthdays.png)

# ioBroker.birthdays

[![NPM version](https://img.shields.io/npm/v/iobroker.birthdays?style=flat-square)](https://www.npmjs.com/package/iobroker.birthdays)
[![Downloads](https://img.shields.io/npm/dm/iobroker.birthdays?label=npm%20downloads&style=flat-square)](https://www.npmjs.com/package/iobroker.birthdays)
![node-lts](https://img.shields.io/node/v-lts/iobroker.birthdays?style=flat-square)
![Libraries.io dependency status for latest release](https://img.shields.io/librariesio/release/npm/iobroker.birthdays?label=npm%20dependencies&style=flat-square)

![GitHub](https://img.shields.io/github/license/klein0r/iobroker.birthdays?style=flat-square)
![GitHub repo size](https://img.shields.io/github/repo-size/klein0r/iobroker.birthdays?logo=github&style=flat-square)
![GitHub commit activity](https://img.shields.io/github/commit-activity/m/klein0r/iobroker.birthdays?logo=github&style=flat-square)
![GitHub last commit](https://img.shields.io/github/last-commit/klein0r/iobroker.birthdays?logo=github&style=flat-square)
![GitHub issues](https://img.shields.io/github/issues/klein0r/iobroker.birthdays?logo=github&style=flat-square)
![GitHub Workflow Status](https://img.shields.io/github/actions/workflow/status/klein0r/iobroker.birthdays/test-and-release.yml?branch=master&logo=github&style=flat-square)

## Versions

![Beta](https://img.shields.io/npm/v/iobroker.birthdays.svg?color=red&label=beta)
![Stable](http://iobroker.live/badges/birthdays-stable.svg)
![Installed](http://iobroker.live/badges/birthdays-installed.svg)

Use an ical file to import your contacts birthdays or define the birthday dates directly in the adapter settings

## Sponsored by

[![ioBroker Master Kurs](https://haus-automatisierung.com/images/ads/ioBroker-Kurs.png)](https://haus-automatisierung.com/iobroker-kurs/?refid=iobroker-birthdays)

## Installation

Please use the "adapter list" in ioBroker to install a stable version of this adapter. You can also use the CLI to install this adapter:

```
iobroker add birthdays
```

## Documentation

[🇺🇸 Documentation](./docs/en/README.md)

[🇩🇪 Dokumentation](./docs/de/README.md)

## Changelog

<!--
  Placeholder for the next version (at the beginning of the line):
  ### **WORK IN PROGRESS**
-->
### **WORK IN PROGRESS**

NodeJS 16.x is required

* (klein0r) Added icons in admin tabs

### 2.3.1 (2023-06-16)

* (klein0r) Added current age text to JSON

### 2.3.0 (2023-06-16)

* (klein0r) Added JSON and count for each month
* (klein0r) Added current age as text

### 2.2.2 (2023-05-01)

* (klein0r) Warn if a birthday with the same name has already been added
* (klein0r) Code optimization

### 2.2.1 (2023-02-13)

NodeJS 14.5 is required

* (klein0r) Allow spaces in text separator
* (klein0r) Added Ukrainian language

### 2.2.0 (2022-12-12)

* (klein0r) Dropped Admin 5 support
* (klein0r) Added Ukrainian language

## Credits

[Logo by herbanu](https://pixabay.com/de/vectors/geburtstag-karte-cele-feier-design-3148707/)

## License

The MIT License (MIT)

Copyright (c) 2023 Matthias Kleine <info@haus-automatisierung.com>

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
