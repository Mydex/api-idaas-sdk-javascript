# ApiIdaasSdkJavascript.MyAccountApi

All URIs are relative to *https://idp.mydexid.org*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getMydexIdFromMyAccountSvt**](MyAccountApi.md#getMydexIdFromMyAccountSvt) | **GET** /members/myaccount/{svt} | Check if a MyAccount SVT has an associated MydexID.



## getMydexIdFromMyAccountSvt

> String getMydexIdFromMyAccountSvt(svt)

Check if a MyAccount SVT has an associated MydexID.

Retrieves the MydexID associated with a MyAccount SVT.

### Example

```javascript
import ApiIdaasSdkJavascript from 'api-idaas-sdk-javascript';
let defaultClient = ApiIdaasSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiIdaasSdkJavascript.MyAccountApi();
let svt = "abc123xyz456"; // String | The MyAccount security verification token
apiInstance.getMydexIdFromMyAccountSvt(svt, (error, data, response) => {
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
 **svt** | **String**| The MyAccount security verification token | 

### Return type

**String**

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

