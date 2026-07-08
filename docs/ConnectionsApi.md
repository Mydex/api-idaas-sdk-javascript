# ApiIdaasSdkJavascript.ConnectionsApi

All URIs are relative to *https://idp.mydexid.org*

Method | HTTP request | Description
------------- | ------------- | -------------
[**postFtcSetup**](ConnectionsApi.md#postFtcSetup) | **POST** /ftc/setup | Set up a First Time Connection URL.
[**postIdentify**](ConnectionsApi.md#postIdentify) | **POST** /identify | Set up an identification URL.



## postFtcSetup

> FtcUrlResponse postFtcSetup(opts)

Set up a First Time Connection URL.

Generates a one-time URL for a member to complete First Time Connection. Requires OAuth2.0 authentication.

### Example

```javascript
import ApiIdaasSdkJavascript from 'api-idaas-sdk-javascript';
let defaultClient = ApiIdaasSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiIdaasSdkJavascript.ConnectionsApi();
let opts = {
  'ftcSetupRequestBody': new ApiIdaasSdkJavascript.FtcSetupRequestBody() // FtcSetupRequestBody | 
};
apiInstance.postFtcSetup(opts, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ftcSetupRequestBody** | [**FtcSetupRequestBody**](FtcSetupRequestBody.md)|  | [optional] 

### Return type

[**FtcUrlResponse**](FtcUrlResponse.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## postIdentify

> IdentifyUrlResponse postIdentify(opts)

Set up an identification URL.

Generates a one-time URL for identifying a member without requiring them to know their MydexID. Requires OAuth2.0 authentication.

### Example

```javascript
import ApiIdaasSdkJavascript from 'api-idaas-sdk-javascript';
let defaultClient = ApiIdaasSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiIdaasSdkJavascript.ConnectionsApi();
let opts = {
  'identifyRequestBody': new ApiIdaasSdkJavascript.IdentifyRequestBody() // IdentifyRequestBody | 
};
apiInstance.postIdentify(opts, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **identifyRequestBody** | [**IdentifyRequestBody**](IdentifyRequestBody.md)|  | [optional] 

### Return type

[**IdentifyUrlResponse**](IdentifyUrlResponse.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

