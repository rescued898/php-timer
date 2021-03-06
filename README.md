# phpunit/php-timer

[![CI Status](https://github.com/sebastianbergmann/php-timer/workflows/CI/badge.svg)](https://github.com/sebastianbergmann/php-timer/actions)
[![Type Coverage](https://shepherd.dev/github/sebastianbergmann/php-timer/coverage.svg)](https://shepherd.dev/github/sebastianbergmann/php-timer)

Utility class for timing things, factored out of PHPUnit into a stand-alone component.

## Installation

You can add this library as a local, per-project dependency to your project using [Composer](https://getcomposer.org/):

```
composer require phpunit/php-timer
```

If you only need this library during development, for instance to run your project's test suite, then you should add it as a development-time dependency:

```
composer require --dev phpunit/php-timer
```

## Usage

### Basic Timing

```php
use SebastianBergmann\Timer\Timer;

Timer::start();

// ...

$time = Timer::stop();
var_dump($time);

print Timer::secondsToTimeString($time);
```

The code above yields the output below:

```
double(1.0967254638672E-5)
0 ms
```

### Resource Consumption Since PHP Startup

```php
use SebastianBergmann\Timer\Timer;

print Timer::resourceUsage();
```

The code above yields the output below:

```
Time: 0 ms, Memory: 0.50MB
```
