# PHPMailer – Upgrade Guide

## 1. Overview

mPDF is used to export HTML to PDF.

## 2. Progress

- Current versions: 6.0 and 7.1
- New version: 8.3.1

Version 8.3.1 is compatible with PHP 8.3 and has additional functionality and security fixes.

You can find a full list of releases at... [https://github.com/phpmailer/phpmailer/releases](https://github.com/mpdf/mpdf/blob/development/CHANGELOG.md)

## 3. New Locaton

The new location is /var/www/html/libraries_php/mpdf831

This is available on the following servers (before migration)...

| Current Server | Available? |
|------|---------|
| alpha | no (older versions not on there) |
| bravo | yes |
| echo | yes |
| nightingale | yes |

## 4. Code Changes Required in Apps

Code will need to updated to point to the new files. For example,...

```
require_once "../../libraries_php/mpdf71/vendor/autoload.php";
```

...will become...

```
require_once "../../libraries_php/mpdf831/vendor/autoload.php";
```

Also, if moving from version 6.0, the way mPDF is initiated has changed, meaning code such as...

```
$mpdf = new mPDF();
```

...will become...

```
$mpdf = new \Mpdf\Mpdf();
```

Other changes may be required. If you come across any, please let me know, and I will add them here. 

## 5. Change History

| Date | Changes |
|------|---------|
| 24/11/2026 | Initial documentation |
