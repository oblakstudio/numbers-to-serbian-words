# oblak/number-serbianisation [![Readme EN](https://img.shields.io/badge/Readme-English-red)](https://github.com/oblakstudio/number-serbianisation/blob/master/README.md) [![Readme SR](https://img.shields.io/badge/Readme-Serbian-blue)](https://github.com/oblakstudio/number-serbianisation/blob/master/README.sr.md)

[![Packagist Version](https://img.shields.io/packagist/v/oblak/number-serbianisation)](https://packagist.org/packages/oblak/number-serbianisation)
![Packagist Dependency Version](https://img.shields.io/packagist/dependency-v/oblak/number-serbianisation/php)
[![codecov](https://codecov.io/gh/oblakstudio/number-serbianisation/graph/badge.svg?token=RoeLb6hV76)](https://codecov.io/gh/oblakstudio/number-serbianisation)
[![semantic-release: angular](https://img.shields.io/badge/semantic--release-angular-e10079?logo=semantic-release)](https://github.com/semantic-release/semantic-release)




## Installation

You can install the package via composer:

```bash
composer require oblak/number-serbianisation
```

## Usage

```php
<?php

use Oblak\Intl\NumberSerbianizer;
use Oblak\Intl\NumberScale;

require 'vendor/autoload.php';

$srn = new NumberSerbianizer();

echo $srn->toWordString(1000); // jedna hiljada
echo $srn->useAccusative()->toWordString(1000); // hiljadu

echo $srn->useScale(NumberScale::Short)->toWordString(1000000000); // jedan bilion
echo $srn->useScale(NumberScale::Long)->toWordString(1000000000); // jedna milijarda
echo $srn->useAccusative()->toWordString(1000000000); // milijardu
```
