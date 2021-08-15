---
title: Estado do Usuário do Host do Serviço
description: O host de serviço permite que um aplicativo associe dados de estado com escopo no nível do host de serviço.
ms.assetid: e18c6c0c-3205-4f88-9a9b-2515a7cfc462
keywords:
- Serviços Web de Estado do Host do Usuário para Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04530b74ef1ab0125b31e56751cdd6cec8109711f603c909f3afeb66970f081a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118192426"
---
# <a name="service-host-user-state"></a>Estado do Usuário do Host do Serviço

O [host de](service-host.md) serviço permite que um aplicativo associe dados de estado com escopo no nível do host de serviço. Esse estado é especificado por uma estrutura [**WS \_ SERVICE \_ PROPERTY**](/windows/desktop/api/WebServices/ns-webservices-ws_service_property) que é passada para a [**função WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) quando o aplicativo cria um host de [serviço](service-host.md), conforme ilustrado no exemplo a seguir.

``` syntax
void* quotePtr = (void*) quotes;
WS_SERVICE_PROPERTY serviceProperties[1] = {0};
serviceProperties[0].id = WS_SERVICE_PROPERTY_HOST_USER_STATE;
serviceProperties[0].value = &quotePtr; // assume this is some state that you want to associate with the service host
serviceProperties[0].valueSize = sizeof(quotePtr);
```


Os dados de estado estão disponíveis para todos os retornos de chamada do host de serviço e operações [de serviço](service-operation.md). Os retornos de chamada e as operações de serviço recuperam as informações chamando a função [**WsGetOperationContextProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetoperationcontextproperty) e especificando o contexto, referenciado pela estrutura [OPERATION \_ \_ CONTEXT](ws-operation-context.md) do WS e a propriedade de contexto, como um dos valores da eunumeração ESTADO DO USUÁRIO DO HOST DA PROPRIEDADE DO CONTEXTO DE OPERAÇÃO do [**WS, conforme ilustrado no exemplo \_ \_ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_operation_context_property_id) a seguir.

``` syntax
QuoteTable* table = NULL;
HRESULT hr = NOERROR;
if (FAILED (WsGetOperationContextProperty (context, WS_OPERATION_CONTEXT_PROPERTY_HOST_USER_STATE, &table, sizeof(table), NULL, error)))
    return hr;
```

 

 




