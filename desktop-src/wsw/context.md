---
title: contexto (Windows serviços Web)
description: Um contexto é usado em operações de serviço de modelo de serviço e retornos de chamada para passar dados de estado relevantes para a operação de serviço ou retorno de chamada quando ele é invocado.
ms.assetid: 44283854-96df-4e6b-8464-3df685896f07
keywords:
- Contexto de serviços Web para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd7863f22193dd1496134afff991ff54efbee5026f2a11e52359b2b016c878c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026624"
---
# <a name="context-windows-web-services"></a>contexto (Windows serviços Web)

Um contexto é usado em operações de [serviço](service-operation.md) de modelo de serviço e retornos de chamada para passar dados de estado relevantes para a operação de serviço ou retorno de chamada quando ele é invocado. Um contexto é referenciado por uma estrutura de [ \_ \_ contexto de operação do WS](ws-operation-context.md) . As propriedades de um contexto podem ser recuperadas com a função [**WsGetOperationContextProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetoperationcontextproperty) , conforme ilustrado no código a seguir.

``` syntax
WS_MESSAGE* requestMessage = NULL;
HRESULT hr = WsGetOperationContextProperty (
                context, 
                WS_OPERATION_CONTEXT_PROPERTY_INPUT_MESSAGE, 
                &requestMessage, 
                sizeof(requestMessage),
                error);
```

Nem todas as propriedades de contexto estão disponíveis em um determinado momento. Consulte a documentação da propriedade de contexto sobre a disponibilidade de uma propriedade específica em uma [operação](service-operation.md)de retorno de chamada ou de serviço.

Para obter mais informações sobre como manter o tempo de vida e o Threading do contexto de operação, consulte o tópico [tempo de vida do contexto de operação e threading](operation-context-lifetime-and-threading.md) .

A seguinte Enumeração faz parte do contexto:

-   [**\_ID da \_ propriedade de contexto da operação WS \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_operation_context_property_id)

A função a seguir faz parte do contexto:

-   [**WsGetOperationContextProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetoperationcontextproperty)

O identificador a seguir faz parte do contexto:

-   [\_contexto de operação WS \_](ws-operation-context.md)

 

 




