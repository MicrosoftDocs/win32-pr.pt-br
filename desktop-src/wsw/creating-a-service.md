---
title: Criando um serviço
description: A criação de um serviço Web é bastante simplificada no WWSAPI pela API do modelo de serviço e pela ferramenta de WsUtil.exe.
ms.assetid: 3536d1c6-6179-4f69-9cc8-27fe6ae30826
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4700324a84962047f403ca7ad090adc3e9f4e99
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103823008"
---
# <a name="creating-a-service"></a>Criando um serviço

A criação de um serviço Web é bastante simplificada no WWSAPI pela API do [modelo de serviço](service-model-layer-overview.md) e pela ferramenta de [WsUtil.exe](wsutil-compiler-tool.md) . O modelo de serviço fornece uma API que permite que o serviço e o cliente enviem e recebam [mensagens](message.md) em um [canal](channel.md) como chamadas de método C. A ferramenta WsUtil gera stubs e cabeçalhos para implementar o serviço.

## <a name="implementing-a-calculator-service-using-wwsapi"></a>Implementando um serviço de calculadora usando o WWSAPI

Usando as fontes geradas da ferramenta [Wsutil.exe](wsutil-compiler-tool.md) , implemente o serviço das etapas a seguir.

Inclua os cabeçalhos na origem do aplicativo.

``` syntax
#include "CalculatorProxyStub.h"
```

Implemente as operações de serviço. Neste exemplo, as operações de serviço são as funções adicionar e subtrair do serviço de calculadora.

``` syntax
HRESULT CALLBACK Add (const WS_OPERATION_CONTEXT* context, 
                  int a, int b, int* result, 
                  const WS_ASYNC_CONTEXT* asyncContext, 
                  WS_ERROR* error)
{
    *result = a + b;
    printf ("%d + %d = %d\n", a, b, *result);
    return NOERROR;
}

HRESULT CALLBACK Subtract (const WS_OPERATION_CONTEXT* context, 
                  int a, int b, int* result, 
                  const WS_ASYNC_CONTEXT* asyncContext, 
                  WS_ERROR* error)
{
    *result = a - b;
    printf ("%d - %d = %d\n", a, b, *result);
    return NOERROR;
}
```

Defina o contrato de serviço definindo os campos de uma estrutura de [**\_ \_ contrato de serviço WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_contract) .

``` syntax
static const DefaultBinding_ICalculatorFunctionTable calculatorFunctions = {Add, Subtract};
static const WS_SERVICE_CONTRACT calculatorContract = 
{
    &DefaultBinding_ICalculatorContractDesc, // comes from the generated header.
    NULL, // for not specifying the default contract
    &calculatorFunctions // specified by the user
};
```

Agora, crie um host de serviço e abra-o para comunicação.

``` syntax
WS_SERVICE_ENDPOINT serviceEndpoint = {0};
serviceEndpoint.uri.chars = L"https://+:80/example"; // address given as uri
serviceEndpoint.binding.channelBinding =  WS_HTTP_CHANNEL_BINDING; // channel binding for the endpoint
serviceEndpoint.channelType = WS_CHANNEL_TYPE_REPLY; // the channel type
serviceEndpoint.uri.length = (ULONG)wcslen(serviceEndpoint.uri.chars);
serviceEndpoint.contract = (WS_SERVICE_CONTRACT*)&calculatorContract;  // the contract
serviceEndpoint.properties = serviceProperties;
serviceEndpoint.propertyCount = WsCountOf(serviceProperties);

if (FAILED (hr = WsCreateServiceHost (&serviceEndpoint, 1, NULL, 0, &host, error)))
    goto Error;

// WsOpenServiceHost  to start the listeners in the service host 
if (FAILED (hr = WsOpenServiceHost (host, NULL, error)))
    goto Error;
```

Consulte o exemplo de código em [HttpCalculatorServiceExample](httpcalculatorserviceexample.md) para obter uma implementação completa do serviço de calculadora.

 

 




