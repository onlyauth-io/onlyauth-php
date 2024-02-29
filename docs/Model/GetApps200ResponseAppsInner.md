# # GetApps200ResponseAppsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**sandbox_mode** | **bool** | Indicates if the app is in sandbox mode |
**allow_sms_channel** | **bool** | Indicates if SMS channel is allowed for guests |
**client_id** | **string** | Client identifier (CLNT-XXX) | [optional]
**friendly_name** | **string** | Friendly name of the app | [optional]
**icon** | **string** | URL to the app&#39;s icon |
**allow_totp_channel** | **bool** | Indicates if TOTP channel is allowed for guests |
**enabled** | **int** | Indicates if the app is enabled |
**webauthn_redirect_allowed** | **bool** | Indicates if WebAuthn redirect is allowed when webauthn_enabled is set to true | [optional]
**app_domain** | **string** | Domain of the app |
**webauthn_enabled** | **bool** | Indicates if WebAuthn is enabled |
**id** | **string** | Uuid of the app (APPX-XXX) |
**supported_factors** | **string** | Supported factors for the app | [optional]
**webauth_enabled** | **bool** | Indicates if WebAuth is enabled | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
