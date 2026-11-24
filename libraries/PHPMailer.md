# PHPMailer – Upgrade Guide

## 1. Overview

PHPMailer is used to send emails.

## 2. Progress

- Current version: 6.0.3
- New version: 6.12.0

Version 6.12.0 appears to be a stable release that is compatible with PHP 8.3 and has several security fixes and new features, while avoiding the extra work/risks of moving to a newer version.

You can find a full list of releases at... https://github.com/phpmailer/phpmailer/releases

## 3. New Locaton

The new location is /var/www/html/libraries_php/PHPMailer-6.12.0

This is available on the following servers (before migration)...

| Current Server | Available? |
|------|---------|
| alpha | yes |
| bravo | yes |
| echo | yes |
| test | yes |
| nightingale | yes |

## 4. Code Changes Required in Apps

Code will need to updated to point to the new library files. For example,...

```
require_once ("../../libraries_php/PHPMailer-6.0.3/src/PHPMailer.php");
require_once ("../../libraries_php/PHPMailer-6.0.3/src/SMTP.php");
require_once ("../../libraries_php/PHPMailer-6.0.3/src/Exception.php");
```

...will become...

```
require_once ("../../libraries_php/PHPMailer-6.12.0/src/PHPMailer.php");
require_once ("../../libraries_php/PHPMailer-6.12.0/src/SMTP.php");
require_once ("../../libraries_php/PHPMailer-6.12.0/src/Exception.php");
```

Otherwise, this library appears to be backwards compatible, and there are no other changes required that we currently know of. If you come across any, please let me know, and I will add them here.

## 5. Change History

| Date | Changes |
|------|---------|
| 20/11/2026 | Initial documentation |
