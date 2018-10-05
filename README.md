# textpattern/composer-lock

[Composer](https://getcomposer.org/) meta package for [Textpattern CMS](https://textpattern.com/). This package can be used to lock the installed Textpattern version and handle Textpattern version dependencies in packages. This package makes sure your Textpattern installation and packages are compatible and can work together, making painless dependency management a reality.

## Locking your Textpattern installation version

When you start using Composer to manage Textpattern packages, plugins and themes, you should lock in your Textpattern version. This makes sure the packages you install are compatible with the Textpattern version you have. You can lock in your Textpattern version using Composer's require command.

```ShellSession
$ composer require textpattern/lock:4.7.1
```

Where the `4.7.1` is the Textpattern version you have.

## Defining required Textpattern version as a dependency in your packages

Textpattern plugin and theme developers can define the compatible and required Textpattern versions using the `textpattern/lock` package. You can set requirements using the [require](https://getcomposer.org/doc/04-schema.md#require) property, or exclude versions using the [conflict](https://getcomposer.org/doc/04-schema.md#conflict).

```json
{
  "require": {
    "textpattern/lock": ">=4.7.0"
  }
}
```

The above, for example, would set require Textpattern version 4.7.0 or newer. The plugin or theme will not be installed if the user's Textpattern version doesn't meet the requirements. See Composer [schema](https://getcomposer.org/doc/04-schema.md) and [basic usage](https://getcomposer.org/doc/01-basic-usage.md) for more information about defining requirements.
