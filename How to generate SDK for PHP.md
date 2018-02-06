PHP
--------
To install (download and unpack zip) with PHP from [http://windows.php.net/download#php-7.2](http://windows.php.net/download#php-7.2) e.g. `VC15 x64 Non Thread Safe (2018-Jan-31 23:18:33)`
 - Unpack zip to `c:\php\`
 - Rename `c:\php\php.ini-development` to `c:\php\php.ini`
 - Open `c:\php\php.ini` and enable next extensions (remove `;` before each line)
    - `extension=curl`
    - `extension=mbstring`
    - `extension=openssl`
 - Add `c:\php\` to your path

Debugging
--------

I prefer [Visual Studio Code](https://code.visualstudio.com/) with `PHP Debug` extension but you can use any editor or IDE which supports PHP.

Extensions:
 - [PHP Debug](https://marketplace.visualstudio.com/items?itemName=felixfbecker.php-debug) - follow the instructions at the extension page to setup debugging

Templates
--------

Codegen tool can be downloaded here: https://drive.google.com/open?id=1Lnys_JfdCQ7ih4gECQx6anU7yI1JsDS6

 - Open `\SDKs\codegen\Templates\php\` and replace `Viewer` with your product name
 - Open `\SDKs\codegen\generate-php-sdk.bat` and replace `Viewer` with your product name
 - Open `\SDKs\codegen\config-php.json` and replace `Viewer` with your product name

Spec file
--------

Replace spec file in `SDKs\spec\` with your.

Make sure you have similar data in your spe file
```json
"info": {
    "title": "GroupDocs.Viewer for Cloud API",
    "version": "18.2"
  },
  "host": "api.groupdocs.cloud",
  "basePath": "/v1",
  "schemes": [
    "https"
  ],
```

Running codegen
--------

Execute `SDKs\codegen\generate-php-sdk.bat` from the root directory and check results in the `SDKs\PHP` directory.

Tests
--------

Navigate into `SDKs\PHP` directory and execute folliwing commands:
  - `php composer.phar install` to install dependencies
  - `vendor\bin\phpunit` to run unit tests


Example
--------
  - https://github.com/groupdocs-viewer-cloud/groupdocs-viewer-cloud-php


