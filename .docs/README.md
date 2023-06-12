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
composer require nettrine/nettrine
```

```neon
extensions:
  nettrine: Nettrine\Nettrine\DI\NettrineExtension
```

### 2. Example projects

We've made a few skeletons with preconfigured Nettrine nad Contributte packages.

- https://github.com/contributte/doctrine-skeleton
- https://github.com/contributte/webapp-skeleton
- https://github.com/contributte/apitte-skeleton
