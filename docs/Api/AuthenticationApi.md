# OpenAPI\Client\AuthenticationApi

All URIs are relative to https://api.onlyauth.io, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createAccessToken()**](AuthenticationApi.md#createAccessToken) | **POST** /server/access-tokens/new | Creates a short-lived JWT token to integrate the widget |
| [**validateSuccessToken()**](AuthenticationApi.md#validateSuccessToken) | **GET** /server/success-tokens | Validates a success token after user completes authentication |


## `createAccessToken()`

```php
createAccessToken($app_id, $client_id, $end_user_phone_number, $end_user_uuid, $redirect_uri, $language, $region): \OpenAPI\Client\Model\CreateAccessToken200Response
```

Creates a short-lived JWT token to integrate the widget

### Example

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

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **app_id** | **string**| Uuid of the OnlyAuth App (APPX-XXX) | |
| **client_id** | **string**| Uuid of you in the OnlyAuth Platform (CLNT-XXX) | |
| **end_user_phone_number** | **string**| Phone number of the end user (E164 format) | |
| **end_user_uuid** | **string**| Uuid of the end user (any type) | |
| **redirect_uri** | **string**| URL to redirect to after authentication | |
| **language** | **string**| Language code (e.g., en-US) | |
| **region** | **string**| Region code (us-1) | |

### Return type

[**\OpenAPI\Client\Model\CreateAccessToken200Response**](../Model/CreateAccessToken200Response.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `validateSuccessToken()`

```php
validateSuccessToken($authorization, $app_id, $client_id, $token): \OpenAPI\Client\Model\ValidateSuccessToken200Response
```

Validates a success token after user completes authentication

### Example

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
$authorization = 'authorization_example'; // string | Bearer token for authentication (your API Secret)
$app_id = 'app_id_example'; // string | Uuid of the OnlyAuth App (APPX-XXX)
$client_id = 'client_id_example'; // string | Uuid of you in the OnlyAuth Platform  (CLNT-XXX)
$token = 'token_example'; // string | The success token to be validated (TOKN-XXX)

try {
    $result = $apiInstance->validateSuccessToken($authorization, $app_id, $client_id, $token);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AuthenticationApi->validateSuccessToken: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **authorization** | **string**| Bearer token for authentication (your API Secret) | |
| **app_id** | **string**| Uuid of the OnlyAuth App (APPX-XXX) | |
| **client_id** | **string**| Uuid of you in the OnlyAuth Platform  (CLNT-XXX) | |
| **token** | **string**| The success token to be validated (TOKN-XXX) | |

### Return type

[**\OpenAPI\Client\Model\ValidateSuccessToken200Response**](../Model/ValidateSuccessToken200Response.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
