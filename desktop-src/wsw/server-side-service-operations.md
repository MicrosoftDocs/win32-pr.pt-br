---
title: Operações de serviço no servidor
description: Esta seção descreve as operações de serviço do lado do serviço.
ms.assetid: d209cf2f-47f5-4025-8af4-1626c867a66a
keywords:
- Serviços Web de operações de serviço do servidor para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c7ad5a327c1cb79278aa562bfaa1753f008a542
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104366931"
---
# <a name="server-side-service-operations"></a>Operações de serviço no servidor

Esta seção descreve as operações de serviço do lado do serviço.


Este é o layout de uma operação de serviço no servidor

-   contexto [de \_ \_ contexto de operação const WS](ws-operation-context.md) \* : [o contexto](context.md)de operação.
-   Parâmetros de operações de serviço: parâmetros que pertencem à operação de serviço.
-   const [**WS \_ Async \_ Context**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) \* asyncContext: contexto assíncrono para executar as operações de serviço de forma assíncrona.
-   [WS \_ Erro de erro](ws-error.md) \* : objeto de erro avançado.

``` syntax
HRESULT CALLBACK Add(const WS_OPERATION_CONTEXT* context, 
                     ULONG a, ULONG b, ULONG* result, 
                     const WS_ASYNC_CONTEXT* asyncContext, 
                     WS_ERROR* error)
{
    *result = a +b;
    return NOERROR;
}
```

## <a name="fault-and-error-handling"></a>Tratamento de falhas e erros

O lado do servidor deve usar falhas para fornecer condições de erro ao cliente. Isso pode fazer isso retornando um HRESULT com falha e inserindo a falha no objeto de erro.

Se a falha não estiver definida no objeto de erro e um HRESULT de falha for retornado, a infraestrutura tentará fornecer uma falha de volta ao cliente. O nível de detalhes divulgado ao cliente nesse caso é controlado pela propriedade serviço de [**divulgação de \_ \_ falha de \_ propriedade \_ de serviço WS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) no [host de serviço](service-host.md).

## <a name="call-completion"></a>Conclusão da chamada

Uma chamada em uma operação de serviço do servidor síncrono deve ser concluída quando ela retornar o controle de volta ao host de serviço. Para uma operação de serviço assíncrona, uma chamada é considerada completa quando a notificação de retorno de chamada é emitida pela implementação da operação de serviço.

## <a name="call-lifetime"></a>Tempo de vida da chamada

Deve-se tomar cuidado especial ao implementar uma operação de serviço no servidor sobre seu tempo de vida. O tempo de vida de uma chamada pode afetar muito quanto tempo o host de serviço leva para ser desligado.

Se espera-se que uma operação de serviço do servidor seja bloqueada devido a alguma operação associada de e/s, é recomendável que ele registre um retorno de chamada de cancelamento, de modo que seja notificado se quando o host de serviço estiver sendo anulado ou quando a conexão subjacente for fechada pelo cliente.

## <a name="server-side-service-operations-and-memory-consideration"></a>Considerações de memória e operações de serviço no servidor

Se uma operação de serviço precisar alocar memória para seus parâmetros de saída, ela deverá usar o objeto de [ \_ heap do WS](ws-heap.md) disponível por meio do [contexto de \_ operação \_ do WS](ws-operation-context.md).

Exemplo: operação de serviço e WS \_ heap

``` syntax
HRESULT CALLBACK ProcessOrder (const WS_OPERATION_CONTEXT* context, const ULONG orderNumber, OrderReceipt** orderReceipt, const WS_ASYNC_CONTEXT* asyncContext, WS_ERROR* error)
{
    WS_HEAP* heap;
    HRESULT hr = WsGetOperationContextProperty (context, WS_OPERATION_CONTEXT_PROPERTY_HEAP, &heap, sizeof(heap), NULL, error);
    if (FAILED(hr))
        return hr;
    hr = WsAlloc(heap, sizeof (OrderReceipt), orderReceipt, error);
    if (FAILED(hr))
        return hr;
    hr = FillInReceipt(*orderReceipt);
    if (FAILED(hr))
        return hr;
    return NOERROR;
} 
```

## <a name="return-values"></a>Valores de retorno

-   WS \_ S \_ Async: a chamada será concluída assíncrona.
-   WS \_ - \_ end: chamada concluída com êxito, o servidor não está esperando nenhuma [ \_ mensagem WS](ws-message.md) do cliente além dessa chamada. Se outra mensagem WS for \_ recebida, o servidor deverá abortar o canal.
-   NOERROR/todos os outros HRESULTs de êxito: chamada concluída com êxito. Observe que é recomendável que o aplicativo não retorne HRESULT outro, então NOERROR para a conclusão bem-sucedida da operação de serviço.
-   Tudo com falha HRESULT: uma falha é enviada de volta para o cliente se uma estiver disponível em \_ erro WS. Caso contrário, uma falha genérica será enviada de volta ao cliente. Consulte a discussão sobre falhas acima.

Consulte o [cancelamento da chamada](call-cancellation.md).

 

 




