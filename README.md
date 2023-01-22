# Squeeze plugin for Craft CMS 4.x

Zip one or multiple craft assets on the fly for frontend user to download.

## Requirements

This plugin requires Craft CMS 4.x.

## Installation
Add these lines to your composer.json file:
```
"repositories": [
        {"type": "composer", "url": "https://repo.repman.io"},
        {"packagist": false}
    ]
```
Then:
```
composer require scandella/craft-squeeze
```

## Usage

```html
<form method="post" target="_blank">
    {{ csrfInput() }}
    {{ actionInput('squeeze/download') }}
    <input type="hidden" name="archivename" value="archive">
    <input type="checkbox" name="files[]" value="10"><!-- asset id -->
    <input type="checkbox" name="files[]" value="20"><!-- asset id -->
    <input type="submit" value="Download!">
</form>
```
To trigger download via url you can use:
```
/actions/squeeze/download?archivename=archive&files[]=10&files[]=20
```
## Credits

This plugin is a clone of [Olivier Bon's plugin](https://github.com/olivierbon/craft-squeeze) just modified to work in Craft 4.

Icon by Yazmin Alanis from the Noun Project

This plugin is mostly a port of [Bob's](https://github.com/boboldehampsink/zipassets)
