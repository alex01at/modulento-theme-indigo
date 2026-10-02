# Indigo

A site theme for [Modulento](https://github.com/alex01at/modulento): a light,
roomy marketplace look with white cards on a pale ground, indigo as the one
accent and large rounded shapes.

It brings a layout, a home page (search box, category tiles, the newest
offers, a provider showcase, three steps and a closing call to action), card
partials for offers and providers, a stylesheet and its font. Every other
page comes from Modulento's `default` theme and only looks different.

The theme has a dark scheme. It follows the device, unless an account has
chosen "light" or "dark" in its settings. Every colour in `assets/theme.css`
is a variable; the dark values are in the two blocks below `:root`.

## Installing

In Modulento, open **Administration → Packages**, enter
`alex01at/modulento-theme-indigo` and install. Then choose "Indigo" under
**Administration → Themes**. New versions appear on the Packages page.

By hand: unpack a release into `themes/indigo/` of the installation.

## Changing the wording

The texts of the home page are in `lang/de.php` and `lang/en.php`, with keys
starting `theme.`. Do not edit them here - an update would replace the
file. Put your own wording into `lang/<language>.php` of the installation:

```php
<?php

return [
    'theme.hero.title' => 'Finde Hilfe für dein',
    'theme.hero.title_accent' => 'nächstes Vorhaben.',
];
```

## Releasing

Set `version` in `theme.json`, commit, then tag and push:

```
git tag v0.1.1 && git push origin main v0.1.1
```

The workflow checks that tag and `theme.json` agree, builds
`modulento-theme-indigo-<version>.zip` with its SHA-256 and publishes both as
a GitHub Release.

## Licence

The theme is licensed under GPL-3.0-or-later, see `LICENSE`. The font Plus
Jakarta Sans in `assets/fonts/` is licensed under the SIL Open Font License,
see `assets/fonts/OFL.txt`.
