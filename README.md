# Install
Download and copy the `Iazel` directory into `app/code/` or install using composer

```sh
composer require iazel/module-regen-product-url 
```

Then call:
```sh
php bin/magento setup:upgrade
```

# How to use
```
Usage:
 iazel:regenurl [-s|--store="..."] [pids1] ... [pidsN]

Arguments:
 pids                  Products to regenerate

Options:
 --store (-s)          Use the specific Store View (default: 0)
 --help (-h)           Display this help message
```

Eg:
```sh
# Regenerate url for all products and the global store
php bin/magento iazel:regenurl

# Regenerate url for products with id (1, 2, 3, 4) for store 1
php bin/magento iazel:regenurl -s1 1 2 3 4
```

Limitations of  URL Generation Module:
``` 
Generate only product urls, but not static pages, catalog urls
Clear url_rewrite table and regenerate product urls, but not static pages and catalog urls 
Generate urls without clearing url_rewrite table, working fine
Generate all stores urls, if not specific store id
Generate specific store urls by mentioned -s<store_id> as paramater
```