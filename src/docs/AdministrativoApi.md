# Org.OpenAPITools.Api.AdministrativoApi

All URIs are relative to *http://localhost:8080*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CadastrarCesta**](AdministrativoApi.md#cadastrarcesta) | **POST** /api/admin/cesta | Cadastrar/Alterar cesta Top Five |
| [**ConsultarCestaAtual**](AdministrativoApi.md#consultarcestaatual) | **GET** /api/admin/cesta/atual | Consultar cesta atual |
| [**ConsultarHistoricoCestas**](AdministrativoApi.md#consultarhistoricocestas) | **GET** /api/admin/cesta/historico | Histórico de cestas |

<a id="cadastrarcesta"></a>
# **CadastrarCesta**
> CadastrarCesta201Response CadastrarCesta (CestaRequest cestaRequest)

Cadastrar/Alterar cesta Top Five

Cadastra uma nova cesta ou altera a cesta ativa

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Org.OpenAPITools.Api;
using Org.OpenAPITools.Client;
using Org.OpenAPITools.Model;

namespace Example
{
    public class CadastrarCestaExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8080";
            var apiInstance = new AdministrativoApi(config);
            var cestaRequest = new CestaRequest(); // CestaRequest | 

            try
            {
                // Cadastrar/Alterar cesta Top Five
                CadastrarCesta201Response result = apiInstance.CadastrarCesta(cestaRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdministrativoApi.CadastrarCesta: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CadastrarCestaWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Cadastrar/Alterar cesta Top Five
    ApiResponse<CadastrarCesta201Response> response = apiInstance.CadastrarCestaWithHttpInfo(cestaRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdministrativoApi.CadastrarCestaWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **cestaRequest** | [**CestaRequest**](CestaRequest.md) |  |  |

### Return type

[**CadastrarCesta201Response**](CadastrarCesta201Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Cesta cadastrada com sucesso |  * X-Request-Id -  <br>  |
| **400** | Requisição inválida |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="consultarcestaatual"></a>
# **ConsultarCestaAtual**
> CestaAtualResponse ConsultarCestaAtual ()

Consultar cesta atual

Retorna a cesta ativa no momento

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Org.OpenAPITools.Api;
using Org.OpenAPITools.Client;
using Org.OpenAPITools.Model;

namespace Example
{
    public class ConsultarCestaAtualExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8080";
            var apiInstance = new AdministrativoApi(config);

            try
            {
                // Consultar cesta atual
                CestaAtualResponse result = apiInstance.ConsultarCestaAtual();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdministrativoApi.ConsultarCestaAtual: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ConsultarCestaAtualWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Consultar cesta atual
    ApiResponse<CestaAtualResponse> response = apiInstance.ConsultarCestaAtualWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdministrativoApi.ConsultarCestaAtualWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**CestaAtualResponse**](CestaAtualResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Cesta atual consultada com sucesso |  * X-Request-Id -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="consultarhistoricocestas"></a>
# **ConsultarHistoricoCestas**
> HistoricoCestasResponse ConsultarHistoricoCestas ()

Histórico de cestas

Retorna o histórico de todas as cestas cadastradas

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Org.OpenAPITools.Api;
using Org.OpenAPITools.Client;
using Org.OpenAPITools.Model;

namespace Example
{
    public class ConsultarHistoricoCestasExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8080";
            var apiInstance = new AdministrativoApi(config);

            try
            {
                // Histórico de cestas
                HistoricoCestasResponse result = apiInstance.ConsultarHistoricoCestas();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AdministrativoApi.ConsultarHistoricoCestas: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ConsultarHistoricoCestasWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Histórico de cestas
    ApiResponse<HistoricoCestasResponse> response = apiInstance.ConsultarHistoricoCestasWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AdministrativoApi.ConsultarHistoricoCestasWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**HistoricoCestasResponse**](HistoricoCestasResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Histórico de cestas consultado com sucesso |  * X-Request-Id -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

