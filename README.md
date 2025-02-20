
# Filament Image Manager

A simple yet powerful image manager for Laravel Filament

## Features

- Field for Filament to select or upload an image
- Working with different disks/directories
- Filament Resource for overview of all images
- Performing conversions with ```Spatie/Image```
- Soft Deletes of Images, cleaning up the database record and belonging files after a set amount of days.

## Installation

You can install this package using Composer. Ensure that Laravel and Filament are already set up in your main project before proceeding. This package will also install the [Spatie/Image](https://github.com/spatie/image)-package.

```bash
  composer require n-schouten/filament-image-manager
```

After installing, you need to publish the migrations and migrate by running the following commands:

```bash
  php artisan vendor:publish --tag=image-manager-migrations

  php artisan migrate
```

You can publish the configuration file, although it is not required. To do so, run the following command: ```php artisan vendor:publish --image-manager-config```

## Installation as Filament Plugin

After this, install the package as a plugin in your Filament Panel Service Provider ```panel()``` function
```bash
  use NSchouten\FilamentImageManager\ImageManagerPlugin;

  $panel->plugin(new ImageManagerPlugin())
```
