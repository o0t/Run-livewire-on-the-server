# Run-livewire-on-the-server
Explanation of running livewire on the server

[livewire website](https://laravel-livewire.com/)

-----------


## Installation

First you need to download livewire into the project

 - https://laravel-livewire.com/docs/2.x/quickstart#install-livewire
    
### After following the steps this error appears

![error](https://github.com/o0t/Run-livewire-on-the-server/assets/94997828/8d4a7d36-4756-4b2b-92d9-d495604343b3)


To resolve the error, follow these steps :

## Publishing Livewire Assets

One of the most direct methods to resolve this issue is to publish the Livewire assets using the following command:

```bash
   php artisan vendor:publish --force --tag=livewire:assets
```

## Modifying the asset_url in Livewire’s Configuration

```bash
   php artisan vendor:publish --tag=livewire:config
```

After publishing the config file, locate the `asset_url` setting in the `config/livewire.php` file and change it to match your local or production domain, like so:

```bash
   'asset_url' => "http://localhost/my_project/public",
```

But I prefer to use the `APP_URL` configuration of the application to set the `asset_url` Livewire variable:


```bash
   'asset_url' => env('APP_URL'),
```

Apply your URL in  `.env`

![9](https://github.com/o0t/Run-livewire-on-the-server/assets/94997828/710253f1-20bd-4321-b717-e4775ea5dd52)


```bash
   php artisan config:cache
```




