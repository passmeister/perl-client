# WWW::SwaggerClient::PassApi

## Load the API package
```perl
use WWW::SwaggerClient::Object::PassApi;
```

All URIs are relative to *https://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_or_update_pass**](PassApi.md#create_or_update_pass) | **POST** /pass | This method creates or (if the pass id already exists) updates a pass, so you don&#39;t have to track ids and creation status of your passes.
[**delete_pass**](PassApi.md#delete_pass) | **DELETE** /pass | Delete pass by pass id.
[**get_pass**](PassApi.md#get_pass) | **GET** /pass | Get pass information by pass id.
[**pass_list**](PassApi.md#pass_list) | **GET** /pass/list | Retrieve the list of active pass ids for a given pass type.
[**pass_sync**](PassApi.md#pass_sync) | **POST** /pass/sync | Send updates to all active passes for a given pass type.


# **create_or_update_pass**
> create_or_update_pass(pass_type_id => $pass_type_id, pass_id => $pass_id)

This method creates or (if the pass id already exists) updates a pass, so you don't have to track ids and creation status of your passes.

This method creates or (if the pass id already exists) updates a pass, so you don't have to track ids and creation status of your passes.

### Example 
```perl
use Data::Dumper;
use WWW::SwaggerClient::PassApi;
my $api_instance = WWW::SwaggerClient::PassApi->new(
);

my $pass_type_id = ; # object | your pass type id, for example P963493 (Urban Fitness)
my $pass_id = ; # object | id of the pass (provided by you when creating the pass or automatically set by passmeister)

eval { 
    $api_instance->create_or_update_pass(pass_type_id => $pass_type_id, pass_id => $pass_id);
};
if ($@) {
    warn "Exception when calling PassApi->create_or_update_pass: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **pass_type_id** | [**object**](.md)| your pass type id, for example P963493 (Urban Fitness) | 
 **pass_id** | [**object**](.md)| id of the pass (provided by you when creating the pass or automatically set by passmeister) | [optional] 

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_pass**
> delete_pass(pass_type_id => $pass_type_id, pass_id => $pass_id)

Delete pass by pass id.

Delete pass by pass id.

### Example 
```perl
use Data::Dumper;
use WWW::SwaggerClient::PassApi;
my $api_instance = WWW::SwaggerClient::PassApi->new(
);

my $pass_type_id = ; # object | your pass type id, for example P963493 (Urban Fitness)
my $pass_id = ; # object | id of the pass

eval { 
    $api_instance->delete_pass(pass_type_id => $pass_type_id, pass_id => $pass_id);
};
if ($@) {
    warn "Exception when calling PassApi->delete_pass: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **pass_type_id** | [**object**](.md)| your pass type id, for example P963493 (Urban Fitness) | 
 **pass_id** | [**object**](.md)| id of the pass | 

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_pass**
> get_pass(pass_type_id => $pass_type_id, pass_id => $pass_id)

Get pass information by pass id.

Get pass information by pass id.

### Example 
```perl
use Data::Dumper;
use WWW::SwaggerClient::PassApi;
my $api_instance = WWW::SwaggerClient::PassApi->new(
);

my $pass_type_id = ; # object | your pass type id, for example P963493 (Urban Fitness)
my $pass_id = ; # object | id of the pass

eval { 
    $api_instance->get_pass(pass_type_id => $pass_type_id, pass_id => $pass_id);
};
if ($@) {
    warn "Exception when calling PassApi->get_pass: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **pass_type_id** | [**object**](.md)| your pass type id, for example P963493 (Urban Fitness) | 
 **pass_id** | [**object**](.md)| id of the pass | 

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **pass_list**
> pass_list(pass_type_id => $pass_type_id, page => $page, limit => $limit)

Retrieve the list of active pass ids for a given pass type.

Retrieve the list of active pass ids for a given pass type.

### Example 
```perl
use Data::Dumper;
use WWW::SwaggerClient::PassApi;
my $api_instance = WWW::SwaggerClient::PassApi->new(
);

my $pass_type_id = ; # object | your pass type id, for example P963493 (Urban Fitness)
my $page = ; # object | 
my $limit = ; # object | 

eval { 
    $api_instance->pass_list(pass_type_id => $pass_type_id, page => $page, limit => $limit);
};
if ($@) {
    warn "Exception when calling PassApi->pass_list: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **pass_type_id** | [**object**](.md)| your pass type id, for example P963493 (Urban Fitness) | 
 **page** | [**object**](.md)|  | [optional] 
 **limit** | [**object**](.md)|  | [optional] 

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **pass_sync**
> pass_sync(pass_type_id => $pass_type_id)

Send updates to all active passes for a given pass type.

For example: you changed the pass type layout and now you want to update all installed passes. (The API call only confirms the scheduling of the updates, actual updating of passes on your customers devices can take a while.)

### Example 
```perl
use Data::Dumper;
use WWW::SwaggerClient::PassApi;
my $api_instance = WWW::SwaggerClient::PassApi->new(
);

my $pass_type_id = ; # object | your pass type id, for example P963493 (Urban Fitness)

eval { 
    $api_instance->pass_sync(pass_type_id => $pass_type_id);
};
if ($@) {
    warn "Exception when calling PassApi->pass_sync: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **pass_type_id** | [**object**](.md)| your pass type id, for example P963493 (Urban Fitness) | 

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

