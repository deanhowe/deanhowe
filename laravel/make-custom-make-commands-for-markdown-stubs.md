---
title: 'Make custom make commands for Mardown stubs'
title-url: '/laravel/make-custom-make-commands-for-sites-stubs'
title-class: 'font-semibold text-snow-100 hover:text-snow-500 dark:text-white'
title-style: 'text-shadow: 0px 0px 7px black;'
icon: 'o-rocket-launch'
-icon-class: ''
-link-url: '/laravel/make-custom-make-commands-for-sites-stubs'
-link-title: 'Make custom make commands for Mardown stubs'
-link-icon: 's-arrow-small-right'
description: 'Waste no more time arguing what a good man should be, be one. - Marcus Aurelius'
-content: '/laravel/make-custom-make-commands-for-mardown-stubs.md'
-figure-background: 'images/thumbs/moof-digital.png'
-figure-alt: 'Make custom make commands for Mardown stubs'
-figure-link: '/laravel/make-custom-make-commands-for-mardown-stubs'
article:modified_time: '2019-10-31T15:39:36+00:00'
og:title: 'Make custom make commands for Mardown stubs'
og:image: '/images/moof_logo.jpg'
og:image:width: '1921'
og:image:height: '1920'
og:image:type: 'image/jpeg'
---

# Markdown Stubs[^stubs]

Make custom make commands for Markdown[^Markdown] stubs

I started off with a google search [laravel custom make command stub](https://www.google.com/search?q=laravel+custom+make+command+stub)

1. [Customizing Stubs in Laravel](https://laravel-news.com/customizing-stubs-in-laravel)
   Was about making *custom stubs*, not was i was thinking.
1. [Create make:custom commands in Laravel](https://cosme.dev/post/create-makecustom-commands-in-laravel)
   Was about making *custom Models* - close, and enough to spark a Laravel deep-dive.

The results of the deep-dive - were that the `ViewMakeCommand` - was actually quite close to whatI was after.

The biggest barrier seemed to be that all the other commands are focused on creating `Classes` and worried about `namespacing` - I didn't care about that at all.

```php
namespace Illuminate\Foundation\Console;

#[AsCommand(name: 'make:view')]
class ViewMakeCommand extends GeneratorCommand
{
    use CreatesMatchingTest;

```

I *__changed__* the following methods:

```php
public function handle()

protected function getPath($name): string
protected function getStub(): string
protected function qualifyClass($name)
protected function getNameInput()
protected function getArguments()
protected function getOptions()
```

I __created__ the following methods:

```php
protected function buildBlogPost()
protected function getFileURI(): Stringable
protected function datePositionAndSlashes($format = null): string
protected function getTitleInput()
```

I __still need to look into__ the following `testing` methods:

```php
protected function getTestPath()
protected function handleTestCreation($path): bool
protected function testNamespace()
protected function testClassName()
protected function testClassFullyQualifiedName()
protected function getTestStub()
protected function testViewName()
```

`getArguments()` & `getOptions()` ended up looking like this:

```php
protected function getArguments()
    {
        return [
            ['title', InputArgument::REQUIRED, 'The title of the ' . strtolower($this->type)],
        ];
    }

    /**
     * Get the console command arguments.
     *
     * @return array
     */
    protected function getOptions()
    {
        return [
            ['date', 'd', InputOption::VALUE_NONE, 'Prepend the path with a date to - eg. /2034/april/'],
            ['day', 'j', InputOption::VALUE_NONE, 'Prepend the path with a day in the date to , eg. /2034/april/14/'],
            ['year', 'y', InputOption::VALUE_NONE, 'Prepend the path with a year - eg. /2034/'],
            ['append-date', 'e', InputOption::VALUE_NONE, 'Append the path with the date…'],
            ['force', 'f', InputOption::VALUE_NONE, 'Create the Markdown file even if the file already exists!'],
            ['path', 'p', InputOption::VALUE_OPTIONAL, 'The path of the generated file', '/'],
            ['extension', null, InputOption::VALUE_OPTIONAL, 'The extension of the generated file', 'md'],
            ['date-format', null, InputOption::VALUE_OPTIONAL, 'The date format for the path', '/Y/F/j'],
        ];
    }
```

Example of `artisan` command
```bash  
php artisan make:blog-post "Apple Rant #1337" -dep/vendor/apple
```

Results in a file being created here:

    ./resources/markdown/vendor/apple/2024/april/apple-rant#1337.md

And a URL that looks like this:
    https://deanhowe.co.uk.test/vendor/apple/2024/april/apple-rant#1337


 > Knowing is not enough; we must apply. Being willing is not enough; we must do. - Leonardo da Vinci

[^1]: This text is inside a footnote.
[^stubs]: If you’re reading I commend you :salute:
[^Markdown]: What is [Markdown](/2024/markdown.md).
[^PHP]: Is [PHP](/2024/PHP) dead?.
[^Laravel]: Read my [Laravel 11](/2014/laravel-11.md) review [here](/2014/laravel-11.md).
