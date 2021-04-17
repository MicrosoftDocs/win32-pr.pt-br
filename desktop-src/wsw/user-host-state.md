---
title: Estado do usuário do host de serviço
description: O host de serviço permite que um aplicativo associe dados de estado que têm o escopo no nível do host de serviço.
ms.assetid: e18c6c0c-3205-4f88-9a9b-2515a7cfc462
keywords:
- Serviços Web de estado do host do usuário para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56f43942f7743d28534e0286a45203dc01e0e7b6
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "105790593"
---
# <a name="service-host-user-state"></a><span data-ttu-id="f612b-106">Estado do usuário do host de serviço</span><span class="sxs-lookup"><span data-stu-id="f612b-106">Service Host User State</span></span>

<span data-ttu-id="f612b-107">O [host de serviço](service-host.md) permite que um aplicativo associe dados de estado que têm o escopo no nível do host de serviço.</span><span class="sxs-lookup"><span data-stu-id="f612b-107">The [service host](service-host.md) enables an application to associate state data that is scoped at the service-host level.</span></span> <span data-ttu-id="f612b-108">Esse estado é especificado por uma estrutura [**de \_ \_ Propriedade do serviço WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_property) que é passada para a função [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) quando o aplicativo cria um [host de serviço](service-host.md), conforme ilustrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="f612b-108">This state is is specified by a [**WS\_SERVICE\_PROPERTY**](/windows/desktop/api/WebServices/ns-webservices-ws_service_property) structure that is passed to the [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) function when the application creates a [service host](service-host.md), as illustrated in the following example.</span></span>

``` syntax
void* quotePtr = (void*) quotes;
WS_SERVICE_PROPERTY serviceProperties[1] = {0};
serviceProperties[0].id = WS_SERVICE_PROPERTY_HOST_USER_STATE;
serviceProperties[0].value = &quotePtr; // assume this is some state that you want to associate with the service host
serviceProperties[0].valueSize = sizeof(quotePtr);
```


<span data-ttu-id="f612b-109">Os dados de estado estão disponíveis para todos os retornos de chamada do host de serviço e [operações de serviço](service-operation.md).</span><span class="sxs-lookup"><span data-stu-id="f612b-109">The state data is available to all service host callbacks and [service operations](service-operation.md).</span></span> <span data-ttu-id="f612b-110">Os retornos de chamada e as operações de serviço recuperam as informações chamando a função [**WsGetOperationContextProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetoperationcontextproperty) e especificando o contexto, referenciado pela estrutura de [ \_ \_ contexto de operação do WS](ws-operation-context.md) e a propriedade Context, como um dos valores da propriedade de [**\_ contexto WS Operation host eunumeration de \_ \_ \_ \_ \_ estado do usuário**](/windows/desktop/api/WebServices/ne-webservices-ws_operation_context_property_id) , conforme ilustrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="f612b-110">Callbacks and service operations retrieve the information by calling the [**WsGetOperationContextProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetoperationcontextproperty) function and specifying the context, referenced by the [WS\_OPERATION\_CONTEXT](ws-operation-context.md) structure, and the context property, as one of the values of the [**WS\_OPERATION\_CONTEXT\_PROPERTY\_HOST\_USER\_STATE**](/windows/desktop/api/WebServices/ne-webservices-ws_operation_context_property_id) eunumeration, as illustrated in the following example.</span></span>

``` syntax
QuoteTable* table = NULL;
HRESULT hr = NOERROR;
if (FAILED (WsGetOperationContextProperty (context, WS_OPERATION_CONTEXT_PROPERTY_HOST_USER_STATE, &table, sizeof(table), NULL, error)))
    return hr;
```

 

 




