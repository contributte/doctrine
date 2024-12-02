# Contributte Doctrine

All-in-on Doctrine meta package for Nette Framework.

## Content

- [Setup](#setup)
- [Relying](#relying)
- [Configuration](#configuration)
- [Usage](#usage)
  - [Types](#types)
  - [Debug](#debug)
  - [Events](#events)
- [Bridges](#bridges)
    - [PSR3](#PSR-3)
- [Examples](#examples)
- [Other](#other)


## Setup

Install package

```bash
composer require nettrine/nettrine
```

Register extension

```neon
extensions:
  nettrine: Nettrine\Nettrine\DI\NettrineExtension
```


## Relying

This package is composed of these packages:

- [nettrine/dbal](https://github.com/contributte/doctrine-dbal)
- [nettrine/orm](https://github.com/contributte/doctrine-orm)
- [nettrine/migrations](https://github.com/contributte/doctrine-migrations)
- [nettrine/fixtures](https://github.com/contributte/doctrine-fixtures)
- [nettrine/cache](https://github.com/contributte/doctrine-cache)
- [nettrine/annotations](https://github.com/contributte/doctrine-annotations)


## Configuration

**Schema definition**

 ```neon
nettrine:
    debug: <bool>
    preset: <string|class>
```

**Under the hood**

Minimal configuration could look like this:

```neon
nettrine:
    debug: %debugMode%
    preset: default
```

## Examples

### 1. Manual example

```sh
composer require nettrine/migrations
composer require nettrine/fixtures
composer require nettrine/dbal
composer require nettrine/orm
```

```neon
# Extension > Nettrine
# => order is crucial
#
extensions:
  # Common
  nettrine.annotations: Nettrine\Annotations\DI\AnnotationsExtension
  nettrine.cache: Nettrine\Cache\DI\CacheExtension
  nettrine.migrations: Nettrine\Migrations\DI\MigrationsExtension
  nettrine.fixtures: Nettrine\Fixtures\DI\FixturesExtension

  # DBAL
  nettrine.dbal: Nettrine\DBAL\DI\DbalExtension
  nettrine.dbal.console: Nettrine\DBAL\DI\DbalConsoleExtension

  # ORM
  nettrine.orm: Nettrine\ORM\DI\OrmExtension
  nettrine.orm.cache: Nettrine\ORM\DI\OrmCacheExtension
  nettrine.orm.console: Nettrine\ORM\DI\OrmConsoleExtension
  nettrine.orm.annotations: Nettrine\ORM\DI\OrmAnnotationsExtension
```

### 2. Example projects

We've made a few skeletons with preconfigured Nettrine nad Contributte packages.

- https://github.com/contributte/webapp-skeleton
- https://github.com/contributte/apitte-skeleton

### 3. Example playground

- https://github.com/contributte/playground (playground)
- https://contributte.org/examples.html (more examples)

## Other

This repository is inspired by these packages.

- https://github.com/doctrine
- https://gitlab.com/Kdyby/Doctrine
- https://gitlab.com/etten/doctrine
- https://github.com/DTForce/nette-doctrine
- https://github.com/portiny/doctrine

Thank you guys.
