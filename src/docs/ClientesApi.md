# Org.OpenAPITools.Api.ClientesApi

All URIs are relative to *http://localhost:8080*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**AderirProduto**](ClientesApi.md#aderirproduto) | **POST** /api/clientes/adesao | Aderir ao produto |
| [**AlterarValorMensal**](ClientesApi.md#alterarvalormensal) | **PUT** /api/clientes/{clienteId}/valor-mensal | Alterar valor mensal |
| [**ConsultarCarteira**](ClientesApi.md#consultarcarteira) | **GET** /api/clientes/{clienteId}/carteira | Consultar carteira (custódia) |
| [**ConsultarRentabilidade**](ClientesApi.md#consultarrentabilidade) | **GET** /api/clientes/{clienteId}/rentabilidade | Consultar rentabilidade detalhada |
| [**SairProduto**](ClientesApi.md#sairproduto) | **POST** /api/clientes/{clienteId}/saida | Sair do produto |

<a id="aderirproduto"></a>
# **AderirProduto**
> AdesaoResponse AderirProduto (AdesaoRequest adesaoRequest)

Aderir ao produto

Permite que um cliente faça adesão ao produto de compra programada

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Org.OpenAPITools.Api;
using Org.OpenAPITools.Client;
using Org.OpenAPITools.Model;

namespace Example
{
    public class AderirProdutoExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8080";
            var apiInstance = new ClientesApi(config);
            var adesaoRequest = new AdesaoRequest(); // AdesaoRequest | 

            try
            {
                // Aderir ao produto
                AdesaoResponse result = apiInstance.AderirProduto(adesaoRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ClientesApi.AderirProduto: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AderirProdutoWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Aderir ao produto
    ApiResponse<AdesaoResponse> response = apiInstance.AderirProdutoWithHttpInfo(adesaoRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ClientesApi.AderirProdutoWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **adesaoRequest** | [**AdesaoRequest**](AdesaoRequest.md) |  |  |

### Return type

[**AdesaoResponse**](AdesaoResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Adesão realizada com sucesso |  * X-Request-Id -  <br>  |
| **400** | Requisição inválida |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="alterarvalormensal"></a>
# **AlterarValorMensal**
> AlterarValorMensalResponse AlterarValorMensal (long clienteId, AlterarValorMensalRequest alterarValorMensalRequest)

Alterar valor mensal

Altera o valor mensal de aporte do cliente

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Org.OpenAPITools.Api;
using Org.OpenAPITools.Client;
using Org.OpenAPITools.Model;

namespace Example
{
    public class AlterarValorMensalExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8080";
            var apiInstance = new ClientesApi(config);
            var clienteId = 789L;  // long | 
            var alterarValorMensalRequest = new AlterarValorMensalRequest(); // AlterarValorMensalRequest | 

            try
            {
                // Alterar valor mensal
                AlterarValorMensalResponse result = apiInstance.AlterarValorMensal(clienteId, alterarValorMensalRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ClientesApi.AlterarValorMensal: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AlterarValorMensalWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Alterar valor mensal
    ApiResponse<AlterarValorMensalResponse> response = apiInstance.AlterarValorMensalWithHttpInfo(clienteId, alterarValorMensalRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ClientesApi.AlterarValorMensalWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **clienteId** | **long** |  |  |
| **alterarValorMensalRequest** | [**AlterarValorMensalRequest**](AlterarValorMensalRequest.md) |  |  |

### Return type

[**AlterarValorMensalResponse**](AlterarValorMensalResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Valor mensal alterado com sucesso |  * X-Request-Id -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="consultarcarteira"></a>
# **ConsultarCarteira**
> CarteiraResponse ConsultarCarteira (long clienteId)

Consultar carteira (custódia)

Retorna a carteira de ativos do cliente em custódia

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Org.OpenAPITools.Api;
using Org.OpenAPITools.Client;
using Org.OpenAPITools.Model;

namespace Example
{
    public class ConsultarCarteiraExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8080";
            var apiInstance = new ClientesApi(config);
            var clienteId = 789L;  // long | 

            try
            {
                // Consultar carteira (custódia)
                CarteiraResponse result = apiInstance.ConsultarCarteira(clienteId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ClientesApi.ConsultarCarteira: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ConsultarCarteiraWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Consultar carteira (custódia)
    ApiResponse<CarteiraResponse> response = apiInstance.ConsultarCarteiraWithHttpInfo(clienteId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ClientesApi.ConsultarCarteiraWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **clienteId** | **long** |  |  |

### Return type

[**CarteiraResponse**](CarteiraResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Carteira consultada com sucesso |  * X-Request-Id -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="consultarrentabilidade"></a>
# **ConsultarRentabilidade**
> RentabilidadeResponse ConsultarRentabilidade (long clienteId)

Consultar rentabilidade detalhada

Retorna a rentabilidade detalhada do cliente

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Org.OpenAPITools.Api;
using Org.OpenAPITools.Client;
using Org.OpenAPITools.Model;

namespace Example
{
    public class ConsultarRentabilidadeExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8080";
            var apiInstance = new ClientesApi(config);
            var clienteId = 789L;  // long | 

            try
            {
                // Consultar rentabilidade detalhada
                RentabilidadeResponse result = apiInstance.ConsultarRentabilidade(clienteId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ClientesApi.ConsultarRentabilidade: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ConsultarRentabilidadeWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Consultar rentabilidade detalhada
    ApiResponse<RentabilidadeResponse> response = apiInstance.ConsultarRentabilidadeWithHttpInfo(clienteId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ClientesApi.ConsultarRentabilidadeWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **clienteId** | **long** |  |  |

### Return type

[**RentabilidadeResponse**](RentabilidadeResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Rentabilidade consultada com sucesso |  * X-Request-Id -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="sairproduto"></a>
# **SairProduto**
> SaidaResponse SairProduto (long clienteId)

Sair do produto

Permite que um cliente saia do produto de compra programada

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Org.OpenAPITools.Api;
using Org.OpenAPITools.Client;
using Org.OpenAPITools.Model;

namespace Example
{
    public class SairProdutoExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost:8080";
            var apiInstance = new ClientesApi(config);
            var clienteId = 789L;  // long | 

            try
            {
                // Sair do produto
                SaidaResponse result = apiInstance.SairProduto(clienteId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ClientesApi.SairProduto: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SairProdutoWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Sair do produto
    ApiResponse<SaidaResponse> response = apiInstance.SairProdutoWithHttpInfo(clienteId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ClientesApi.SairProdutoWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **clienteId** | **long** |  |  |

### Return type

[**SaidaResponse**](SaidaResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Saída realizada com sucesso |  * X-Request-Id -  <br>  |
| **404** | Cliente não encontrado |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

