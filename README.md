# Dependency management

Manage dependencies with [Composer](http://getcomposer.org/)

# Quoting

* String literals are defined with single quotes (`''`). 
* Double quotes (`""`) are used only for string literals that require variable interpolation:
    ```php
    $name = 'Bob';
    $hi = "Hello $name";
    ```
  This provides a good middle ground between concatenation with `.` and `sprintf()`. 

  Using double quotes with string literals that do not require interpolation: 
  1. Creates minimal but unnecessary overhead. PHP searches for variables in every double-quote enclosed string.
  2. Is, more imporantly, a queue for humans to expect a variable inside the string literal.
