# DEPRECATED
Hello everyone, this repo never meant to be maintained and just happened to come to life after a discussion with an user that had the same problem with regenerating urls.
I'm really happy that it have been useful for many of you, but given that I don't use Magento anymore and I don't have time nor will to maintain it, please switch to: https://github.com/peterjaap/magento2-regenurl

By the way, thank you @peterjaap for contributing :)

----

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
