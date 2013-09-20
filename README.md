# For fun and profit:

PHP can be great! To achieve greatness, let's set some conventions.

## Dependencies

Manage dependencies with [Composer](http://getcomposer.org/).

## Libraries for common tasks

* HTTP requests: [Guzzle](http://guzzlephp.org/)

## Code Style

### Quoting

* String literals are defined with single quotes (`''`). 
* Double quotes (`""`) are used only for string literals that require variable interpolation:
    ```php
    $name = 'Bob';
    $hi = "Hello $name.";  // `$hi` is 'Hello Bob.' 
    ```
  This provides a good middle ground between concatenation with `.` and `sprintf()`. 

  Using double quotes with string literals that do not require interpolation: 
  1. Causes confusion for the human reader when no variables are present within the string: double quotes are a queue for humans to expect a variable inside the string literal. 
  2. Creates minimal but unnecessary overhead. PHP searches for variables in every double-quote enclosed string.
