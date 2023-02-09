# Manually Uninstalling PHP Required Parameter OpenCart Error

If you are running **PHP8.0** (and can't go back to PHP7.x) and you get errors related to `google shopping` you may not be able to uninstall the extension via the button on the Extensions form under Advertising.

I got the "error undefined" alert popup error when I was trying to add a basic product...

```
2023-12-27 14:50:04 - PHP Unknown:  Required parameter $store_id follows optional parameter $product_ids in /usr/www/users/username/myshop.com/admin/model/extension/advertise/google.php on line 341
2023-12-27 14:50:04 - PHP Unknown:  Required parameter $store_id follows optional parameter $data in /usr/www/users/username/myshop.com/admin/model/extension/advertise/google.php on line 413
2023-12-27 14:50:04 - PHP Warning:  Cannot modify header information - headers already sent by (output started at /usr/www/users/username/myshop.com/admin/controller/startup/error.php:34) in /usr/www/users/username/myshop.com/system/library/response.php on line 36
```

So you will have to painstakingly rename or delete all the files I have made reference to below...

Login to your favorite FTP client and get busy.

- Rename all google related files in the folders below:
  - admin/controller/advertise/xxx.php
  - admin/language/english/advertise/xxx.php
  - admin/view/template/advertise/xxx.tpl
  - catalog/controller/advertise/xxx.php
  - catalog/language/english/advertise/xxx.php
  - catalog/view/template/advertise/xxx.tpl

- ref
  - https://forum.opencart.com/viewtopic.php?f=202&t=229401
  - https://forum.opencart.com/viewtopic.php?f=167&t=226968
  - https://forum.opencart.com/viewtopic.php?t=157668
