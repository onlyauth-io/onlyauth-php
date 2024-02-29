# OpenAPI\Client\AppsApi

All URIs are relative to https://api.onlyauth.io, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**deleteApp()**](AppsApi.md#deleteApp) | **DELETE** /apps/{app_id} | Delete an app |
| [**getAppById()**](AppsApi.md#getAppById) | **GET** /apps/{app_id} | Get an app by uuid |
| [**getApps()**](AppsApi.md#getApps) | **GET** /apps | Get all apps |
| [**newApp()**](AppsApi.md#newApp) | **POST** /apps | Create a new app |
| [**updateApp()**](AppsApi.md#updateApp) | **POST** /apps/{app_id} | Update an app |


## `deleteApp()`

```php
deleteApp($app_id, $client_id): \OpenAPI\Client\Model\DeleteApp200Response
```

Delete an app

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Secret) authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\AppsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$app_id = 'app_id_example'; // string | Unique identifier of the app to be deleted (APPX-XXX)
$client_id = 'client_id_example'; // string | Client identifier for authentication (CLNT-XXX)

try {
    $result = $apiInstance->deleteApp($app_id, $client_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AppsApi->deleteApp: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **app_id** | **string**| Unique identifier of the app to be deleted (APPX-XXX) | |
| **client_id** | **string**| Client identifier for authentication (CLNT-XXX) | |

### Return type

[**\OpenAPI\Client\Model\DeleteApp200Response**](../Model/DeleteApp200Response.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getAppById()`

```php
getAppById($app_id, $client_id): \OpenAPI\Client\Model\NewApp200Response
```

Get an app by uuid

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Secret) authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\AppsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$app_id = 'app_id_example'; // string | Unique identifier of the app to be fetched (APPX-XXX)
$client_id = 'client_id_example'; // string | Client identifier for authentication (CLNT-XXX)

try {
    $result = $apiInstance->getAppById($app_id, $client_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AppsApi->getAppById: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **app_id** | **string**| Unique identifier of the app to be fetched (APPX-XXX) | |
| **client_id** | **string**| Client identifier for authentication (CLNT-XXX) | |

### Return type

[**\OpenAPI\Client\Model\NewApp200Response**](../Model/NewApp200Response.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getApps()`

```php
getApps($client_id): \OpenAPI\Client\Model\GetApps200Response
```

Get all apps

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Secret) authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\AppsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$client_id = 'client_id_example'; // string | Uuid of you in the OnlyAuth Platform (CLNT-XXX)

try {
    $result = $apiInstance->getApps($client_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AppsApi->getApps: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **client_id** | **string**| Uuid of you in the OnlyAuth Platform (CLNT-XXX) | |

### Return type

[**\OpenAPI\Client\Model\GetApps200Response**](../Model/GetApps200Response.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `newApp()`

```php
newApp($client_id): \OpenAPI\Client\Model\NewApp200Response
```

Create a new app

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Secret) authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\AppsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$client_id = 'client_id_example'; // string | Client identifier

try {
    $result = $apiInstance->newApp($client_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AppsApi->newApp: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **client_id** | **string**| Client identifier | [optional] |

### Return type

[**\OpenAPI\Client\Model\NewApp200Response**](../Model/NewApp200Response.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateApp()`

```php
updateApp($app_id, $client_id, $client_id2): \OpenAPI\Client\Model\NewApp200Response
```

Update an app

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (API Secret) authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\AppsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$app_id = 'app_id_example'; // string | Unique identifier of the app to be updated (APPX-XXX)
$client_id = 'client_id_example'; // string | Client identifier for authentication (CLNT-XXX)
$client_id2 = 'client_id_example'; // string | Client identifier

try {
    $result = $apiInstance->updateApp($app_id, $client_id, $client_id2);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AppsApi->updateApp: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **app_id** | **string**| Unique identifier of the app to be updated (APPX-XXX) | |
| **client_id** | **string**| Client identifier for authentication (CLNT-XXX) | |
| **client_id2** | **string**| Client identifier | [optional] |

### Return type

[**\OpenAPI\Client\Model\NewApp200Response**](../Model/NewApp200Response.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
