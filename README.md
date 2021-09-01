# Bagisto Razorpay Payment Gateway
Razorpay is a popular payment gateway in india. This package provides a additional strong help for the user to use the Razorpay payment gateway in their Bagisto laravel ecommerce application.

## Automatic Installation
1. Use command prompt to run this package `composer require wontonee/razorpay`
2. Now open `config/app.php` and register razorpay provider.
```sh
'providers' => [
        // Razorpay provider
        Wontonee\Razorpay\Providers\RazorpayServiceProvider::class,
]
```
3. Now open composer.json and go to `autoload psr-4`.
```sh
"autoload": {
        "psr-4": {
        "Wontonee\\Razorpay\\": "Wontonee/Razorpay/src"
        }
    }
```
4. Now go to `package/Webkul/Admin/src/Resources/lang/en` copy these line at the bottom end of code.
```sh
 'key-id'                      => 'Key Id',
 'key-secret'                      => 'Key Secret',
```
5. Now open the command prompt and run `composer dump-autoload`.
6. Now run `php artisan config:cache`
7. Now go to your bagisto admin section `admin/configuration/sales/paymentmethods` you will see the new payment gateway razorpay. 
8. Now open `app\Http\Middleware\VerifyCsrfToken.php` and add this route to the exception list.
```sh
protected $except = [
                  '/razorpaycheck',
           ];

```

## Manual Installation
1. Download the zip folder from the github repository.
2. Unzip the folder and go to your bagisto application path `package` and create a folder name `Wontonee/Razorpay/` upload `src` folder inside this path.
3. Now open `config/app.php` and register razorpay provider.
```sh
'providers' => [
        // Razorpay provider
        Wontonee\Razorpay\Providers\RazorpayServiceProvider::class,
]
```
4. Now open composer.json and go to `autoload psr-4`.
```sh
"autoload": {
        "psr-4": {
        "Wontonee\\Razorpay\\": "packages/Wontonee/Razorpay/src"
        }
    }
```
5. Now go to `package/Webkul/Admin/src/Resources/lang/en` copy these line at the bottom end of code.
```sh
 'key-id'                      => 'Key Id',
 'key-secret'                      => 'Key Secret',
```
6. Now open the command prompt and run `composer dump-autoload`.
7. Now run `php artisan config:cache`
9. Now go to your bagisto admin section `admin/configuration/sales/paymentmethods` you will see the new payment gateway razorpay. 
9. Now open `app\Http\Middleware\VerifyCsrfToken.php` and add this route to the exception list.
```sh
protected $except = [
                  '/razorpaycheck',
           ];

```

For any help or customisation  <https://www.wontonee.com> or email us <hello@wontonee.com>
