# Org.OpenAPITools.Api.ContaMasterApi

All URIs are relative to *http://localhost:8080*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**ConsultarCustodiaMaster**](ContaMasterApi.md#consultarcustodiamaster) | **GET** /api/admin/conta-master/custodia | Consultar custódia master |

<a id="consultarcustodiamaster"></a>
# **ConsultarCustodiaMaster**
> CustodiaMasterResponse ConsultarCustodiaMaster ()

Consultar custódia master

Retorna a custódia da conta master

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Org.OpenAPITools.Api;
using Org.OpenAPITools.Client;
using Org.OpenAPITools.Model;

namespace Example
{
    public class ConsultarCustodiaMasterExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8080";
            var apiInstance = new ContaMasterApi(config);

            try
            {
                // Consultar custódia master
                CustodiaMasterResponse result = apiInstance.ConsultarCustodiaMaster();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ContaMasterApi.ConsultarCustodiaMaster: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ConsultarCustodiaMasterWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Consultar custódia master
    ApiResponse<CustodiaMasterResponse> response = apiInstance.ConsultarCustodiaMasterWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ContaMasterApi.ConsultarCustodiaMasterWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**CustodiaMasterResponse**](CustodiaMasterResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Custódia master consultada com sucesso |  * X-Request-Id -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

