ColorTime
=========

[![Build Status](https://travis-ci.org/dwightwatson/colortime.svg?branch=master)](https://travis-ci.org/dwightwatson/colortime)
[![Dependency Status](https://www.versioneye.com/php/watson:colortime/1.0.0/badge.svg)](https://www.versioneye.com/php/watson:colortime/1.0.0)
[![Total Downloads](https://poser.pugx.org/watson/colortime/downloads.svg)](https://packagist.org/packages/watson/colortime)
[![Latest Stable Version](https://poser.pugx.org/watson/colortime/v/stable.svg)](https://packagist.org/packages/watson/colortime)
[![Latest Unstable Version](https://poser.pugx.org/watson/colortime/v/unstable.svg)](https://packagist.org/packages/watson/colortime)
[![License](https://poser.pugx.org/watson/colortime/license.svg)](https://packagist.org/packages/watson/colortime)

Get time as a hexadecimal color, like [the color clock](http://www.jacopocolo.com/hexclock/).

For example, 10:10:10 AM will have a hex value of #101010.

## Installation

Easy, use Composer! If you're yet to be enlightened by dependency management or like a challenge, copy the code in manually.

```sh
composer require "watson/colortime"
```

## Usage

Create a new instance and pass in the `DateTime` instance you want to use, or use the factory to get an instance for right now.

```php
// Using a specific time.
$datTime = DateTime::createFromFormat('H:i:s', '10:10:10');

$colorTime = new \Watson\ColorTime\ColorTime($dateTime);

// Using the current time (you could also pass a DateTime instance to the factory if you so desired).
$colorTime = \Watson\ColorTime\ColorTime::make();
```

To get the time as a hex value, simply call the `hex()` method.

```php
$hex = $colorTime->hex(); // '#101010'
```

## Spellcheck

If you'd rather spell colour correctly, simply subclass the `ColorTime` instance into your own application and use that instead.

This is just a joke, don't do this. Unless you want to, in which case feel free.

```php
class ColourTime extends \Watson\ColorTime\ColorTime {}
```