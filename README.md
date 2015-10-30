# WP-CoreTestLib

This library allows for easy testing of WordPress plugins, themes
widgets, libraries. You name it.

# Setup
You need to have access to a database server to make use of this library.

1.
Clone this repo into your `tests` directory

```bash
$ cd my-project/
$ cd tests/
$ git clone https://github.com/mekom/WP-CoreTestLib
``` 

2.
Copy the config sample into the root of your `tests` directory.

*note: Your config file should be besides the WP-CoreTestLib directory, and not inside it.*

<pre>
my-project/
    tests/
        WP-CoreTestLib/
            wp-test-config-sample.php
        wp-test-config.php
</pre>

```bash
$ cd my-project/tests/
$ cp WP-CoreTestLib/wp-test-config-sample.php wp-test-config.php
```

3.
Supply the correct settings for database access to the my-project/tests/wp-test-config.php file. (Remember: Using 127.0.0.1 instead of localhost might be preferable)

4.
Include the WP-CoreTestLib/bootstrap.php file from your PHPUnit bootstrap file.

my-project/tests/bootstrap.php

```php
require __DIR__ . "/WP-CoreTestLib/bootstrap.php";
```


Great! That should be it. You now be able to test WordPress things, and have access to some special wordpress testing functions. You can google the "wordpress testing library" to find out which these are.

But I'll list some of them for you

# The Api

###WP_UnitTestCase
This is the class you should extend instead of `PHPUnitTestCase