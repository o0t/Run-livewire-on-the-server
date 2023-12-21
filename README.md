# Run-livewire-on-the-server
Explanation of running livewire on the server

[livewire website](https://laravel-livewire.com/)

-----------


## Installation

First you need to download livewire into the project

 - [https://laravel-livewire.com/docs/2.x/installation#publishing-config](https://laravel-livewire.com/docs/2.x/installation)https://laravel-livewire.com/docs/2.x/installation
    
### After following the steps this error appears

![error](https://github.com/o0t/Run-livewire-on-the-server/assets/94997828/8d4a7d36-4756-4b2b-92d9-d495604343b3)


To resolve the error, follow these steps

After publishing the config file, locate the `asset_url` setting in the `config/livewire.php` file and change it to match your local or production domain, like so:

```bash
   'asset_url' => "http://localhost/my_project/public",
```

But I prefer to use the `APP_URL` configuration of the application to set the `asset_url` Livewire variable:


```bash
   'asset_url' => env(APP_URL),
```
