# PHP Runtime Settings

The PHP runtime is configured by a file called `php.ini`. 

The default path to `php.ini` is configured and built into the `php` binary. You can see information about these paths with `php --ini`:

```
$ php --ini
Configuration File (php.ini) Path: /etc
Loaded Configuration File:         /private/etc/php.ini
Scan for additional .ini files in: (none)
Additional .ini files parsed:      (none)
```

You can instruct `php` to look for `php.ini` at a non-default path using the `-c` switch. Or you can use `-n` to run entirely with compiled-in settings:

```
$ php --help | grep php\.ini
  -c <path>|<file> Look for php.ini file in this directory
  -n               No php.ini file will be used
```


## First: Settings-related Functions

There are a few notable settings-related functions every PHP developer should know about. You can use these functions to inspect or manipulate runtime settings.

* `get_cfg_var()`: Returns the value of a setting as specified in the current `php.ini`. This may not be the current value in the runtime.
* `ini_set()`: Sets the value of a setting in the runtime. Allows you to override settings as specified in `php.ini`.
* `ini_get()`: Get the value of a setting from the current runtime. 


## Notable Settings

See [all settings](http://php.net/manual/en/errorfunc.configuration.php)



