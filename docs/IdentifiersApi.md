# ApiIdaasSdkJavascript.IdentifiersApi

All URIs are relative to *https://idp.mydexid.org*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getIdentifierInvite**](IdentifiersApi.md#getIdentifierInvite) | **GET** /members/invite/{invite} | Fetch an invitation code and identifier auth data.
[**patchNotifyStatus**](IdentifiersApi.md#patchNotifyStatus) | **PATCH** /members/notify/status | Update the status of a notification.
[**postInviteStatus**](IdentifiersApi.md#postInviteStatus) | **POST** /members/invite/status | Check the status of an invite.
[**postNotifyMemberViaIdentifier**](IdentifiersApi.md#postNotifyMemberViaIdentifier) | **POST** /members/notify | Send a notification to a member via its identifier.
[**postStoreAndSendIdentifierInvite**](IdentifiersApi.md#postStoreAndSendIdentifierInvite) | **POST** /members/invite | Store an invitation code and send notification.



## getIdentifierInvite

> GetInviteResponse getIdentifierInvite(invite)

Fetch an invitation code and identifier auth data.

Retrieves the invitation data for a given invite code.

### Example

```javascript
import ApiIdaasSdkJavascript from 'api-idaas-sdk-javascript';
let defaultClient = ApiIdaasSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiIdaasSdkJavascript.IdentifiersApi();
let invite = "a1b2c3d4e5f6"; // String | The invitation code
apiInstance.getIdentifierInvite(invite, (error, data, response) => {
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
 **invite** | **String**| The invitation code | 

### Return type

[**GetInviteResponse**](GetInviteResponse.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## patchNotifyStatus

> CreateIdentifierResponse patchNotifyStatus(opts)

Update the status of a notification.

Updates the status of a notification identifier.

### Example

```javascript
import ApiIdaasSdkJavascript from 'api-idaas-sdk-javascript';
let defaultClient = ApiIdaasSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiIdaasSdkJavascript.IdentifiersApi();
let opts = {
  'updateNotificationStatusRequestBody': new ApiIdaasSdkJavascript.UpdateNotificationStatusRequestBody() // UpdateNotificationStatusRequestBody | 
};
apiInstance.patchNotifyStatus(opts, (error, data, response) => {
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
 **updateNotificationStatusRequestBody** | [**UpdateNotificationStatusRequestBody**](UpdateNotificationStatusRequestBody.md)|  | [optional] 

### Return type

[**CreateIdentifierResponse**](CreateIdentifierResponse.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## postInviteStatus

> InviteStatusResponse postInviteStatus(opts)

Check the status of an invite.

Checks the status of an invitation without modifying it.

### Example

```javascript
import ApiIdaasSdkJavascript from 'api-idaas-sdk-javascript';
let defaultClient = ApiIdaasSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiIdaasSdkJavascript.IdentifiersApi();
let opts = {
  'inviteStatusRequestBody': new ApiIdaasSdkJavascript.InviteStatusRequestBody() // InviteStatusRequestBody | 
};
apiInstance.postInviteStatus(opts, (error, data, response) => {
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
 **inviteStatusRequestBody** | [**InviteStatusRequestBody**](InviteStatusRequestBody.md)|  | [optional] 

### Return type

[**InviteStatusResponse**](InviteStatusResponse.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## postNotifyMemberViaIdentifier

> CreateIdentifierResponse postNotifyMemberViaIdentifier(opts)

Send a notification to a member via its identifier.

Sends a notification (email or SMS) to a member using their identifier for authentication.

### Example

```javascript
import ApiIdaasSdkJavascript from 'api-idaas-sdk-javascript';
let defaultClient = ApiIdaasSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiIdaasSdkJavascript.IdentifiersApi();
let opts = {
  'notifyMemberRequestBody': new ApiIdaasSdkJavascript.NotifyMemberRequestBody() // NotifyMemberRequestBody | 
};
apiInstance.postNotifyMemberViaIdentifier(opts, (error, data, response) => {
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
 **notifyMemberRequestBody** | [**NotifyMemberRequestBody**](NotifyMemberRequestBody.md)|  | [optional] 

### Return type

[**CreateIdentifierResponse**](CreateIdentifierResponse.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## postStoreAndSendIdentifierInvite

> GetInviteResponse postStoreAndSendIdentifierInvite(opts)

Store an invitation code and send notification.

Stores an invitation code and sends an invitation to the member via their identifier.

### Example

```javascript
import ApiIdaasSdkJavascript from 'api-idaas-sdk-javascript';
let defaultClient = ApiIdaasSdkJavascript.ApiClient.instance;
// Configure OAuth2 access token for authorization: oauth2
let oauth2 = defaultClient.authentications['oauth2'];
oauth2.accessToken = 'YOUR ACCESS TOKEN';

let apiInstance = new ApiIdaasSdkJavascript.IdentifiersApi();
let opts = {
  'inviteRequestBody': new ApiIdaasSdkJavascript.InviteRequestBody() // InviteRequestBody | 
};
apiInstance.postStoreAndSendIdentifierInvite(opts, (error, data, response) => {
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
 **inviteRequestBody** | [**InviteRequestBody**](InviteRequestBody.md)|  | [optional] 

### Return type

[**GetInviteResponse**](GetInviteResponse.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

