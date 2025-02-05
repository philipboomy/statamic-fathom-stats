# Statamic Fathom Stats

> Statamic Fathom Stats is a Statamic addon that adds widgets for the dashboard.

![Preview](https://raw.githubusercontent.com/datascaled/statamic-fathom-stats/master/assets/preview.png)

## Features

This addon provides the following widgets:

- Pageviews
- Visitors per device
- Visitors per page
- Average duration on site
- Footer

## There's more 🚀

- Fully translateable
- Each widget is optional
- Each widget allows a custom amount of days

## How to Install

You can search for this addon in the `Tools > Addons` section of the Statamic control panel and click **install**, or run the following command from your project root:

``` bash
composer require datascaled/statamic-fathom-stats
```

``` bash
php artisan vendor:publish --tag="statamic-fathom-stats-config"
```

Add the following values to your env file

``` env
FATHOM_API_TOKEN=
FATHOM_SITE_ID=
```

Add the widgets to config/statamic/cp.php

``` php
[
    'type' => 'general_statistics',
    'days' => 30
    'width' => 100,
],
[
    'type' => 'visitors_per_device',
    'days' => 30
    'width' => 50,
],
[
    'type' => 'visitors_per_page',
    'days' => 30
    'width' => 50,
],
[
    'type' => 'average_duration',
    'days' => 30
    'width' => 100,
],
[
    'type' => 'footer',
    'width' => 100,
],
```

Add the translations to your lang/locale.json if the locale isn't "en"

``` json
    "Visitor": "Besucher",
    "Phone": "Telefon",
    "Desktop": "Desktop",
    "Page views": "Seitenaufrufe",
    "Unique visitors": "Individuelle Besucher",
    "Seconds": "Sekunden"
```


## Important notice

Since the API is early access and Fathom has set a throttling of 10 requests per minute, we have decided not to provide any filters.

Made with ❤️ in Zurich by [Datascale](https://datascale.ch)