---
title: Criando um cliente
description: A criação de um cliente para serviços Web é bastante simplificada no WWSAPI pela API do modelo de serviço e pela ferramenta de WsUtil.exe.
ms.assetid: 09f489e8-958d-4bc5-a232-aa59bd75333a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 606a68f574a9ad79d15f3ddd48247f93a5414250
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364434"
---
# <a name="creating-a-client"></a>Criando um cliente

A criação de um cliente para serviços Web é bastante simplificada no WWSAPI pela API do [modelo de serviço](service-model-layer-overview.md) e pela ferramenta de [WsUtil.exe](wsutil-compiler-tool.md) . O modelo de serviço fornece uma API que permite que o cliente envie e receba [mensagens](message.md) em um [canal](channel.md) como chamadas de método C. A ferramenta WsUtil gera cabeçalhos e auxiliares para implementar o cliente. Esses cabeçalhos incluem os tipos e os protótipos de função para funções C que representam os serviços oferecidos pelo serviço Web de destino. Os auxiliares são usados para criar o proxy de serviço, que contém as informações de associação e o [endereço do ponto de extremidade](endpoint-address.md) para o serviço.

## <a name="using-wsutil-to-generate-headers-and-helpers"></a>Usando WsUtil para gerar cabeçalhos e auxiliares

Para gerar os cabeçalhos e auxiliares, o WsUtil é aberto e lê os arquivos de metadados para o serviço de destino – arquivos WSDL e XSD — e os converte em cabeçalhos; Portanto, é necessário recuperar os arquivos de metadados para o serviço de destino com antecedência, por exemplo, usando SvcUtil, uma parte do Windows Communication Foundation. Por motivos de segurança, é imperativo que suas cópias desses arquivos sejam confiáveis. (Para obter mais informações, consulte a seção "segurança" do tópico da [ferramenta do compilador WsUtil](wsutil-compiler-tool.md) .)

Para executar o WsUtil, use a seguinte sintaxe de linha de comando se os arquivos WSDL e XSD do serviço estiverem em seu próprio diretório: `WsUtil.exe *.wsdl *.xsd` . Como alternativa, você pode especificar os arquivos por nome completo.

O WsUtil geralmente gera dois arquivos para cada arquivo de metadados: um cabeçalho e um arquivo C. Adicione esses arquivos ao seu projeto de codificação e use \# instruções include para incluí-los no código do seu cliente. (Os arquivos XSD representam tipos e os arquivos WSDL representam operações.)

## <a name="creating-the-service-proxy"></a>Criando o proxy de serviço

O cabeçalho gerado por WsUtil contém uma rotina auxiliar para criar o proxy de serviço com a associação necessária. Essa rotina está incluída na seção "rotinas auxiliares de política" do arquivo de cabeçalho gerado. Por exemplo, o cabeçalho gerado para o serviço de calculadora ilustrado no exemplo [httpcalculatorclientexample](httpcalculatorclientexample.md) conterá o protótipo de função a seguir.


```
HRESULT BasicHttpBinding_ICalculator_CreateServiceProxy(
    __in_opt WS_HTTP_BINDING_TEMPLATE* templateValue,
    __in_ecount_opt(proxyPropertyCount) const WS_PROXY_PROPERTY* proxyProperties,
    __in const ULONG proxyPropertyCount,
    __deref_out_opt WS_SERVICE_PROXY** _serviceProxy,
    __in_opt WS_ERROR* error);
```



Incorpore esse auxiliar em seu código e passe um identificador de [ \_ \_ proxy de serviço WS](ws-service-proxy.md) para receber o identificador para o proxy de serviço criado. No cenário mais simples, no qual apenas um identificador de proxy de serviço e um objeto de erro são passados para a função, a chamada é semelhante ao seguinte.


```C++
hr = BasicHttpBinding_ICalculator_CreateServiceProxy(
            NULL,
            NULL,
            0,
            &serviceProxy,
            error);
```



Para criar a parte de endereço do proxy de serviço, chame [**WsOpenServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy) com um identificador para o proxy de serviço e um ponteiro para um [**\_ \_ endereço de ponto de extremidade WS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) contendo o endereço do ponto de extremidade de serviço ao qual você deseja se conectar.

## <a name="implementing-the-client-with-function-prototypes"></a>Implementando o cliente com protótipos de função

Os cabeçalhos gerados nos arquivos WSDL de serviço também contêm protótipos de função C que representam os serviços disponíveis do serviço Web e específicos para a associação necessária. Por exemplo, um cabeçalho gerado para o serviço de calculadora ilustrado em HttpCalculatorServiceExample conterá o protótipo a seguir para a operação de multiplicação desse serviço.

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

Você pode copiar os protótipos e usá-los como modelos para codificar as chamadas de função em seu cliente, em cada caso passando o identificador para o proxy de serviço. Quando terminar com o proxy de serviço, chame [**WsCloseServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy).

 

 




