# For fun and profit:

PHP can be great! To achieve greatness, let's set some conventions.

## Dependencies

Manage dependencies with [Composer](http://getcomposer.org/).

## Libraries for common tasks

* HTTP requests: [Guzzle](http://guzzlephp.org/)
* Testing: PHPUnit

## Code Style

### Quoting

* String literals are defined with single quotes (`''`). 
* Double quotes (`""`) are used only for string literals that require variable and escape sequence interpolation:
    ```php
    $name = 'Bob';
    $hi = "Hello $name.";  // `$hi` is 'Hello Bob.' 
    ```
  Such use of double quotes provides a good middle ground between concatenation with `.` and `sprintf()`. 

  Using double quotes with string literals that do not require variable or escape sequence interpolation: 
  1. Causes confusion for the human reader when no variables or escape sequences are present in the string: double quotes are a queue for humans to expect a interpolation in a string literal.
  2. Creates minimal but unnecessary overhead. PHP searches for variables in every double-quote enclosed string.
  3. May lead to unintended effects. In addition to variables, PHP looks and renders for backslash escape sequences in double-quoted strings.
 
## Testing

> Whenever you are tempted to type something into a print statement or a debugger expression, write it as a test instead.
> --Martin Fowler
