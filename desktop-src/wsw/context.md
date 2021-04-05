---
title: Contexto (serviços Web do Windows)
description: Um contexto é usado em operações de serviço de modelo de serviço e retornos de chamada para passar dados de estado relevantes para a operação de serviço ou retorno de chamada quando ele é invocado.
ms.assetid: 44283854-96df-4e6b-8464-3df685896f07
keywords:
- Contexto de serviços da Web para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f7edd1f8c93bbf4fd4b4d5feea5b2219bc522ea
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/23/2019
ms.locfileid: "103916891"
---
# <a name="context-windows-web-services"></a><span data-ttu-id="09301-106">Contexto (serviços Web do Windows)</span><span class="sxs-lookup"><span data-stu-id="09301-106">Context (Windows Web Services)</span></span>

<span data-ttu-id="09301-107">Um contexto é usado em operações de [serviço](service-operation.md) de modelo de serviço e retornos de chamada para passar dados de estado relevantes para a operação de serviço ou retorno de chamada quando ele é invocado.</span><span class="sxs-lookup"><span data-stu-id="09301-107">A context is used in Service Model [service operations](service-operation.md) and callbacks to pass relevant state data to the service operation or callback when it is invoked.</span></span> <span data-ttu-id="09301-108">Um contexto é referenciado por uma estrutura de [ \_ \_ contexto de operação do WS](ws-operation-context.md) .</span><span class="sxs-lookup"><span data-stu-id="09301-108">A context is referenced by a [WS\_OPERATION\_CONTEXT](ws-operation-context.md) structure.</span></span> <span data-ttu-id="09301-109">As propriedades de um contexto podem ser recuperadas com a função [**WsGetOperationContextProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetoperationcontextproperty) , conforme ilustrado no código a seguir.</span><span class="sxs-lookup"><span data-stu-id="09301-109">The properties of a context can be retrieved with the [**WsGetOperationContextProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetoperationcontextproperty) function, as illustrated in the following code.</span></span>

``` syntax
WS_MESSAGE* requestMessage = NULL;
HRESULT hr = WsGetOperationContextProperty (
                context, 
                WS_OPERATION_CONTEXT_PROPERTY_INPUT_MESSAGE, 
                &requestMessage, 
                sizeof(requestMessage),
                error);
```

<span data-ttu-id="09301-110">Nem todas as propriedades de contexto estão disponíveis em um determinado momento.</span><span class="sxs-lookup"><span data-stu-id="09301-110">Not all the context properties are available at any given time.</span></span> <span data-ttu-id="09301-111">Consulte a documentação da propriedade de contexto sobre a disponibilidade de uma propriedade específica em uma [operação](service-operation.md)de retorno de chamada ou de serviço.</span><span class="sxs-lookup"><span data-stu-id="09301-111">See the context property documentation regarding availability of a specific property in a callback or a [service operation](service-operation.md).</span></span>

<span data-ttu-id="09301-112">Para obter mais informações sobre como manter o tempo de vida e o Threading do contexto de operação, consulte o tópico [tempo de vida do contexto de operação e threading](operation-context-lifetime-and-threading.md) .</span><span class="sxs-lookup"><span data-stu-id="09301-112">For more information on how to maintain operation context lifetime and threading, see the [Operation Context Lifetime and Threading](operation-context-lifetime-and-threading.md) topic.</span></span>

<span data-ttu-id="09301-113">A seguinte Enumeração faz parte do contexto:</span><span class="sxs-lookup"><span data-stu-id="09301-113">The following enumeration is part of the context:</span></span>

-   [<span data-ttu-id="09301-114">**\_ID da \_ propriedade de contexto da operação WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="09301-114">**WS\_OPERATION\_CONTEXT\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_operation_context_property_id)

<span data-ttu-id="09301-115">A função a seguir faz parte do contexto:</span><span class="sxs-lookup"><span data-stu-id="09301-115">The following function is part of the context:</span></span>

-   [<span data-ttu-id="09301-116">**WsGetOperationContextProperty**</span><span class="sxs-lookup"><span data-stu-id="09301-116">**WsGetOperationContextProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetoperationcontextproperty)

<span data-ttu-id="09301-117">O identificador a seguir faz parte do contexto:</span><span class="sxs-lookup"><span data-stu-id="09301-117">The following handle is part of the context:</span></span>

-   [<span data-ttu-id="09301-118">\_contexto de operação WS \_</span><span class="sxs-lookup"><span data-stu-id="09301-118">WS\_OPERATION\_CONTEXT</span></span>](ws-operation-context.md)

 

 




