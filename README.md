# RecapController

# Installation

dans votre projet, à la racine, executez ces commandes :

## Installation Composer

```
php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
php -r "if (hash_file('sha384', 'composer-setup.php') === 'a5c698ffe4b8e849a443b120cd5ba38043260d5c4023dbf93e1558871f1f07f58274fc6f4c93bcfd858c6bd0775cd8d1') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"
php composer-setup.php
php -r "unlink('composer-setup.php');"
```

## Mettre composer dans le path pour le rendre accessible partout

```
sudo mv composer.phar /usr/local/bin/composer
```

## Installer des dépendances

utilisez le site https://packagist.org

composer require nomdemadependence

## Installer var-Dumper

```
composer require symfony/var-dumpevar
```

Il peut y avoir un problème de cache, pour le régler, tapez :

```
sudo chown -R mint /home/mint/.cache
```

## Installer AltoRouter

```
composer require altorouter/altorouter
```

## Installer BenRouter ( AltoDispatcher )

```
composer require benoclock/alto-dispatcher
```

si un problème de version se produit, modifiez votre fichier composer.json et mettez :

```
{
    "require": {
        "symfony/var-dumper": "^5.0",
        "altorouter/altorouter": "^1.2",
        "benoclock/alto-dispatcher": "dev-master"
    }
}
```

une fois ces modifications apportés, tapez :

```
composer update
```
