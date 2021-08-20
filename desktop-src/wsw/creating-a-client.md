---
title: Criando um cliente
description: A criação de um cliente para serviços Web é bastante simplificada no WWSAPI pela API do Modelo de Serviço e pela WsUtil.exe web.
ms.assetid: 09f489e8-958d-4bc5-a232-aa59bd75333a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50ca04ef5fbbeef76cd32a0b6523391deb19957479cd5f332715972f3b5bfbc8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026554"
---
# <a name="creating-a-client"></a>Criando um cliente

A criação de um cliente para serviços Web é bastante simplificada no WWSAPI pela [API](service-model-layer-overview.md) do Modelo de Serviço e pela [WsUtil.exe](wsutil-compiler-tool.md) de serviço. O Modelo de Serviço fornece uma API que permite que o cliente envie e receba [mensagens](message.md) por um [canal como](channel.md) chamadas de método C. A ferramenta WsUtil gera headers e auxiliares para implementar o cliente. Esses headers incluem os tipos e protótipos de função para funções C que representam os serviços oferecidos pelo serviço Web de destino. Os auxiliares são usados para criar o proxy de serviço, que contém as informações de associação e o endereço [do](endpoint-address.md) ponto de extremidade para o serviço.

## <a name="using-wsutil-to-generate-headers-and-helpers"></a>Usando o WsUtil para gerar títulos e auxiliares

Para gerar os títulos e auxiliares, o WsUtil abre e lê os arquivos de metadados para o serviço de destino – arquivos wsdl e xsd – e os converte em títulos; portanto, é necessário recuperar os arquivos de metadados para o serviço de destino com antecedência, por exemplo, usando SvcUtil, uma parte do Windows Communication Foundation. Por motivos de segurança, é imperativo que suas cópias desses arquivos sejam confiáveis. (Para obter mais informações, consulte a seção "Segurança" do [tópico Ferramenta do Compilador WsUtil.)](wsutil-compiler-tool.md)

Para executar o WsUtil, use a seguinte sintaxe de linha de comando se os arquivos WSDL e XSD para o serviço estão em seu próprio diretório: `WsUtil.exe *.wsdl *.xsd` . Como alternativa, você pode especificar os arquivos por nome completo.

O WsUtil geralmente gera dois arquivos para cada arquivo de metadados: um header e um arquivo C. Adicione esses arquivos ao seu projeto de codificação e use instruções include para \# incluí-los no código do cliente. (Os arquivos XSD representam tipos e os arquivos WSDL representam operações.)

## <a name="creating-the-service-proxy"></a>Criando o proxy de serviço

O título gerado pelo WsUtil contém uma rotina auxiliar para criar o proxy de serviço com a associação necessária. Essa rotina está incluída na seção "Rotinas auxiliares de política" do arquivo de header gerado. Por exemplo, o cabeçalho gerado para o serviço de calculadora ilustrado no [exemplo httpcalculatorcltexample](httpcalculatorclientexample.md) conterá o protótipo de função a seguir.


```
HRESULT BasicHttpBinding_ICalculator_CreateServiceProxy(
    __in_opt WS_HTTP_BINDING_TEMPLATE* templateValue,
    __in_ecount_opt(proxyPropertyCount) const WS_PROXY_PROPERTY* proxyProperties,
    __in const ULONG proxyPropertyCount,
    __deref_out_opt WS_SERVICE_PROXY** _serviceProxy,
    __in_opt WS_ERROR* error);
```



Incorpore esse auxiliar em seu código e passe um guidão [ \_ \_ proxy de](ws-service-proxy.md) SERVIÇO do WS para receber o handle para o proxy de serviço criado. No cenário mais simples, no qual apenas um identificador de proxy de serviço e um objeto de erro são passados para a função, a chamada se parece com a seguinte.


```C++
hr = BasicHttpBinding_ICalculator_CreateServiceProxy(
            NULL,
            NULL,
            0,
            &serviceProxy,
            error);
```



Para criar a parte de endereço do proxy de serviço, chame [**WsOpenServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy) com um handle para o proxy de serviço e um ponteiro para um ENDEREÇO DE PONTO DE EXTREMIDADE do [**WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) que contém o endereço do ponto de extremidade de serviço ao qual você deseja se conectar.

## <a name="implementing-the-client-with-function-prototypes"></a>Implementando o cliente com protótipos de função

Os títulos gerados a partir dos arquivos WSDL de serviço também contêm protótipos de função C que representam os serviços disponíveis no serviço Web e específicos para a associação necessária. Por exemplo, um cabeçalho gerado para o serviço de calculadora ilustrado em HttpCalculatorServiceExample conterá o protótipo a seguir para a operação de multiplicação desse serviço.

``` syntax
HRESULT BasicHttpBinding_ICalculator_Multiply(
    __in WS_SERVICE_PROXY* _serviceProxy,
    __in double n1,
    __in double n2,
    __out double* MultiplyResult,
    __in WS_HEAP* _heap,
    __in_ecount_opt(_callPropertyCount) const WS_CALL_PROPERTY* _callProperties,
    __in const ULONG _callPropertyCount,
    __in_opt const WS_ASYNC_CONTEXT* _asyncContext,
    __in_opt WS_ERROR* _error);
```

Você pode copiar os protótipos e usá-los como modelos para codificar as chamadas de função em seu cliente, em cada caso, passando o handle para o proxy de serviço. Quando terminar o proxy de serviço, chame [**WsCloseServiceProxy.**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy)

 

 




