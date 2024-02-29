# OnlyAuth PHP Library

<div align="left">
    <a href="https://opensource.org/licenses/MIT">
        <img src="https://img.shields.io/badge/License-MIT-blue.svg" style="width: 100px; height: 28px;" />
    </a>
</div>

## Sign up for OnlyAuth 2FA API

Sign up for the [OnlyAuth 2FA API](https://app.onlyauth.io) to get your API credentials.

## Installation Guide
Check out the [OnlyAuth 2FA API Implementation guide](https://www.onlyauth.io/docs) for full details.


## SDK Installation

### Requirements

PHP 7.4 and later.

### Composer

OnlyAuth SDK is available via Packagist, onlyauth/sdk. Install it via composter:

```bash
composer require onlyauth/sdk

```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
<?php
require_once('/path/to/OpenAPIClient-php/vendor/autoload.php');
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Secret) authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\AuthenticationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$app_id = 'app_id_example'; // string | Uuid of the OnlyAuth App (APPX-XXX)
$client_id = 'client_id_example'; // string | Uuid of you in the OnlyAuth Platform (CLNT-XXX)
$end_user_phone_number = 'end_user_phone_number_example'; // string | Phone number of the end user (E164 format)
$end_user_uuid = 'end_user_uuid_example'; // string | Uuid of the end user (any type)
$redirect_uri = 'redirect_uri_example'; // string | URL to redirect to after authentication
$language = 'language_example'; // string | Language code (e.g., en-US)
$region = 'region_example'; // string | Region code (us-1)

try {
    $result = $apiInstance->createAccessToken($app_id, $client_id, $end_user_phone_number, $end_user_uuid, $redirect_uri, $language, $region);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AuthenticationApi->createAccessToken: ', $e->getMessage(), PHP_EOL;
}

```

## API Endpoints

All URIs are relative to *https://api.onlyauth.io*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*AppsApi* | [**deleteApp**](docs/Api/AppsApi.md#deleteapp) | **DELETE** /apps/{app_id} | Delete an app
*AppsApi* | [**getAppById**](docs/Api/AppsApi.md#getappbyid) | **GET** /apps/{app_id} | Get an app by uuid
*AppsApi* | [**getApps**](docs/Api/AppsApi.md#getapps) | **GET** /apps | Get all apps
*AppsApi* | [**newApp**](docs/Api/AppsApi.md#newapp) | **POST** /apps | Create a new app
*AppsApi* | [**updateApp**](docs/Api/AppsApi.md#updateapp) | **POST** /apps/{app_id} | Update an app
*AuthenticationApi* | [**createAccessToken**](docs/Api/AuthenticationApi.md#createaccesstoken) | **POST** /server/access-tokens/new | Creates a short-lived JWT token to integrate the widget
*AuthenticationApi* | [**validateSuccessToken**](docs/Api/AuthenticationApi.md#validatesuccesstoken) | **GET** /server/success-tokens | Validates a success token after user completes authentication

## Models

- [CreateAccessToken200Response](docs/Model/CreateAccessToken200Response.md)
- [DeleteApp200Response](docs/Model/DeleteApp200Response.md)
- [ErrorResponse](docs/Model/ErrorResponse.md)
- [GetApps200Response](docs/Model/GetApps200Response.md)
- [GetApps200ResponseAppsInner](docs/Model/GetApps200ResponseAppsInner.md)
- [NewApp200Response](docs/Model/NewApp200Response.md)
- [ValidateSuccessToken200Response](docs/Model/ValidateSuccessToken200Response.md)

## Authorization

Authentication schemes defined for the API:
### BearerAuth

- **Type**: Bearer authentication (API Secret)

## Tests

To run the tests, use:

```bash
composer install
vendor/bin/phpunit
```

