# Org.OpenAPITools.Api.MotorDeCompraApi

All URIs are relative to *http://localhost:8080*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**ExecutarCompra**](MotorDeCompraApi.md#executarcompra) | **POST** /api/motor/executar-compra | Executar compra manualmente |

<a id="executarcompra"></a>
# **ExecutarCompra**
> ExecutarCompraResponse ExecutarCompra (ExecutarCompraRequest executarCompraRequest)

Executar compra manualmente

Executa o motor de compra manualmente para uma data específica (para testes)

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Org.OpenAPITools.Api;
using Org.OpenAPITools.Client;
using Org.OpenAPITools.Model;

namespace Example
{
    public class ExecutarCompraExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8080";
            var apiInstance = new MotorDeCompraApi(config);
            var executarCompraRequest = new ExecutarCompraRequest(); // ExecutarCompraRequest | 

            try
            {
                // Executar compra manualmente
                ExecutarCompraResponse result = apiInstance.ExecutarCompra(executarCompraRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MotorDeCompraApi.ExecutarCompra: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ExecutarCompraWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Executar compra manualmente
    ApiResponse<ExecutarCompraResponse> response = apiInstance.ExecutarCompraWithHttpInfo(executarCompraRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MotorDeCompraApi.ExecutarCompraWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **executarCompraRequest** | [**ExecutarCompraRequest**](ExecutarCompraRequest.md) |  |  |

### Return type

[**ExecutarCompraResponse**](ExecutarCompraResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Compra executada com sucesso |  * X-Request-Id -  <br>  |
| **404** | Cotação não encontrada |  -  |
| **409** | Compra já executada |  -  |
| **500** | Erro interno do servidor |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

