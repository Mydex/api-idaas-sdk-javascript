# ApiIdaasSdkJavascript.ScotAccountApi

All URIs are relative to *https://idp.mydexid.org*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getMydexIdFromScotAccountSub**](ScotAccountApi.md#getMydexIdFromScotAccountSub) | **GET** /members/scotaccount/{sub} | Check if a ScotAccount sub GUID has an associated MydexID.



## getMydexIdFromScotAccountSub

> String getMydexIdFromScotAccountSub(sub)

Check if a ScotAccount sub GUID has an associated MydexID.

Retrieves the MydexID associated with a ScotAccount GUID.

### Example

```javascript
import ApiIdaasSdkJavascript from 'api-idaas-sdk-javascript';
let defaultClient = ApiIdaasSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiIdaasSdkJavascript.ScotAccountApi();
let sub = "123e4567-e89b-12d3-a456-426614174000"; // String | The ScotAccount GUID
apiInstance.getMydexIdFromScotAccountSub(sub, (error, data, response) => {
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
 **sub** | **String**| The ScotAccount GUID | 

### Return type

**String**

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

