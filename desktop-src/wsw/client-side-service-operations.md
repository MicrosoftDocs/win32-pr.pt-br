---
title: Operações de serviço no lado do cliente
ms.assetid: 9d6e2441-91de-4108-b1c4-282fbca5fe7c
description: 'Saiba mais sobre: operações de serviço do lado do cliente'
keywords:
- Serviços Web de operações de serviço do cliente para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e73ccbb0c742d0be09570b0959c9c1a663d7f4d0f054cc88070d842ac6d954ff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119657296"
---
# <a name="client-side-service-operations"></a>Operações de serviço no lado do cliente

Este é o layout de uma operação de serviço no lado do cliente:

-   [WS \_ SERVIÇO \_ proxy Service](ws-service-proxy.md) -proxy \* : o [proxy de serviço](service-proxy.md) para a chamada.
-   [WS \_ ](ws-heap.md)Heap \* de heap: um heap necessário usado para serialização de corpo e desserialização da [ \_ mensagem WS](ws-message.md).
-   Parâmetros de operações de serviço: parâmetros que pertencem à operação de serviço.
-   [**Chame Propriedades e sua contagem**](/windows/desktop/api/WebServices/ns-webservices-ws_call_property): uma matriz de propriedades de chamada.
-   Contagem de propriedades de [**chamada**](/windows/desktop/api/WebServices/ns-webservices-ws_call_property) : a contagem de propriedades de chamada.
-   [**WS \_ \_Contexto assíncrono**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) asyncContext: contexto assíncrono para executar a chamada de forma assíncrona.
-   [WS \_ Erro de erro:](ws-error.md) objeto de erro avançado.


### <a name="signature-for-client-side-service-operations"></a>Assinatura para operações de serviço do lado do cliente

``` syntax
typedef HRESULT(CALLBACK *ICalculator_Add)(WS_SERVICE_PROXY* serviceProxy, 
                                           WS_HEAP* heap, 
                                           ULONG a, ULONG b, ULONG* result, 
                                           const WS_CALL_PROPERTY* callProperties, 
                                           const ULONG callPropertyCount, 
                                           const WS_ASYNC_CONTEXT* asyncContext, 
                                           WS_ERROR* error);
```

### <a name="memory-considerations-for-client-side-service-operations"></a>Considerações sobre memória para operações de serviço no lado do cliente

A chamada para a operação de serviço usa um [WS \_ heap](ws-heap.md) \* como parâmetro. Esse é um parâmetro necessário usado para serialização/desserialização de corpos de mensagem para parâmetros.

O aplicativo deve chamar [**WsResetHeap**](/windows/desktop/api/WebServices/nf-webservices-wsresetheap) se a chamada foi bem-sucedida ou não. Se a chamada for bem-sucedida e tiver parâmetros de saída, o aplicativo deverá chamar **WsResetHeap** imediatamente depois que for concluído com os parâmetros de saída.

O aplicativo deve alocar memória para parâmetros de entrada e saída com [**WsAlloc**](/windows/desktop/api/WebServices/nf-webservices-wsalloc). O proxy de serviço pode precisar realocá-los, de forma que os ponteiros fornecidos serão substituídos. Uma tentativa de liberar essa memória fará com que o aplicativo falhe.

### <a name="client-side-service-operation-and-ws_heap"></a>Operação de serviço do lado do cliente e WS \_ heap

``` syntax
HRESULT hr = IProcessOrder_ProcessOrder(serviceProxy, heap, orderNumber, &orderReceipt, NULL, 0, NULL, error);
if(FAILED(hr))
    goto error;
hr = ProcessReceipt(orderReceipt);
WsResetHeap(heap);
if(FAILED(hr))
    goto error;
hr = IProcessOrder_CompleteOrder(serviceProxy, heap, orderNumber, &orderMemo, NULL, 0, NULL, error);
if(FAILED(hr))
    goto error;
hr = ProcessMemo(orderMemo);
WsResetHeap(heap);
if(FAILED(hr))
    goto error;
```

### <a name="error-parameter"></a>Parâmetro de erro

O aplicativo sempre deve passar o parâmetro de erro para:

-   Obtenha informações de erro avançadas se ocorrer uma falha durante a chamada de operação de serviço.
-   Obtenha o objeto de falha se o serviço retornar uma falha. A falha está contida no objeto de erro. nesse caso, o valor **HRESULT** retornado da operação de serviço é de **\_ falha de \_ ponto de extremidade WS E \_ \_ recebido** (consulte [Windows valores de retorno de serviços Web](windows-web-services-return-values.md)).

### <a name="call-properties-for-client-side-service-operations"></a>Chamar Propriedades para operações de serviço no lado do cliente

As propriedades da chamada permitem que um aplicativo especifique configurações personalizadas para uma determinada chamada. Atualmente, apenas uma propriedade de chamada está disponível com o modelo de serviço, [**ID de chamada de \_ propriedade de chamada \_ \_ \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_call_property_id).

``` syntax
WS_CALL_PROPERTY callProperties[1] = {0};
callProperties[0].id = WS_CALL_PROPERTY_CALL_ID;
callProperties[0].value = 5;

HRESULT hr = IProcessOrder_ProcessOrder(serviceProxy, heap, orderNumber, &orderReceipt,  callProperties, WsCountOf(callProperties), NULL, error);
if(FAILED(hr))
    goto error;
//:
//:
hr = IProcessOrder_CompleteOrder(serviceProxy, heap, orderNumber, &orderReceipt, callProperties, WsCountOf(callProperties), NULL, error);
if(FAILED(hr))
    goto error;

//:
//:
//:
// On a separate thread 
// In this case both the calls belong to call group 5, and will abandon as a result of the call to WsAbandonCall. 
hr = WsAbandonCall(serviceProxy, 5, error);
```

### <a name="abandoning-a-call"></a>Abandonando uma chamada

Geralmente, é desejável abandonar os resultados de uma chamada para abandonar o controle de volta ao aplicativo, de modo que a conclusão da chamada real seja tratada pela infraestrutura. O proxy de serviço fornece esse recurso por meio do [**WsAbandonCall**](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall).

Observe que o controle para o chamador pode não ser retornado imediatamente, a única garantia de que o tempo de execução do proxy de serviço dá é que ele não esperaria que nenhuma operação associada de e/s seja concluída antes de conceder o controle de volta ao chamador.

Chamadas em uma operação de serviço no lado do cliente podem ser abandonadas por meio de uma chamada para [**WsAbandonCall**](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall). Ele usa um proxy de serviço e uma ID de chamada. Uma ID de chamada é fornecida como parte de uma chamada de propriedades em uma operação de serviço.

Se a ID de chamada for 0, o proxy de serviço abandonará todas as chamadas pendentes nessa instância.

### <a name="call-timeouts"></a>Tempos limite de chamada

Por padrão, um proxy de serviço tem um tempo limite de 30 segundos para cada chamada. O tempo limite em uma chamada pode ser alterado pela propriedade de proxy de serviço de [**\_ \_ \_ \_ tempo limite de chamada de propriedade de proxy WS**](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id) ao criar um proxy de serviço por meio de [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy).

Depois que um tempo limite é atingido, a chamada é abandonada.

### <a name="return-values"></a>Valores de retorno

Todos os valores **HRESULT** de êxito devem ser tratados como êxito e todos os valores de falha devem ser tratados como falhas. A seguir estão alguns dos valores **HRESULT** que um aplicativo pode esperar:

-   **WS \_ S \_ Async**: a chamada será concluída de forma assíncrona.
-   NOERROR: chamada concluída com êxito.
-   **WS \_ \_Operação E \_ abandonada**: a chamada foi abandonada. O objeto de erro contém o motivo para abandono.
-   **WS \_ E \_ \_ operação inválida**: o proxy de serviço não está em um estado apropriado para fazer uma chamada, verifique o estado do proxy de serviço para descobrir o estado do proxy de serviço.

para obter uma lista completa de valores de retorno, consulte [Windows valores de retorno de serviços Web](windows-web-services-return-values.md).

### <a name="code-examples"></a>Exemplos de código

Para obter exemplos de código, consulte o seguinte:

-   [CallAbandonExample](callabandonexample.md)
-   [**WsAbandonCall**](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall)

 

 




