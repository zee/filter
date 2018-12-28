# Filter Interface

[![Software License][ico-license]][link-license]
[![Latest Version on Packagist][ico-version]][link-packagist]
[![PHP Version][ico-php-version]][link-github]

The common interface for filters.

## Installation

~~~bash
composer require zeeproject/filter
~~~

## Usage

If you need a filter, you can use the interface like this:

~~~php
<?php

use Zee\Filter\Filter;

class Foo
{
    private $filter;

    public function __construct(Filter $filter)
    {
        $this->filter = $filter;
    }

    public function doSomething($rawValue)
    {
        $filteredValue = $this->filter->process($rawValue);
        
        // do something with filtered value
        
        return $filteredValue;
    }
}
~~~

You can then pick [one of the implementation](https://packagist.org/providers/zeeproject/filter-implementation)
of the interface and inject into your object.

If you want to implement the interface, you can require this package and implement `Zee\Filter\Filter` in your code.

[ico-license]: https://img.shields.io/badge/License-BSD%202--Clause-blue.svg?style=for-the-badge
[ico-version]: https://img.shields.io/packagist/v/zeeproject/filter.svg?style=for-the-badge&label=Latest
[ico-php-version]: https://img.shields.io/packagist/php-v/zeeproject/exceptions.svg?style=for-the-badge

[link-license]: LICENSE
[link-packagist]: https://packagist.org/packages/zeeproject/filter
[link-github]: https://github.com/zee/filter
