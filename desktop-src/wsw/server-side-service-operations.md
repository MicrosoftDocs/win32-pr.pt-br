---
title: Operações de serviço do lado do servidor
description: Esta seção descreve as operações de serviço do lado do serviço.
ms.assetid: d209cf2f-47f5-4025-8af4-1626c867a66a
keywords:
- Serviços Web de Operações do Lado do Servidor para Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f1656e56df08d00a0551946c4e52898beccd4d1a37a5bd96c63eb2066928fe1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119344626"
---
# <a name="server-side-service-operations"></a>Operações de serviço do lado do servidor

Esta seção descreve as operações de serviço do lado do serviço.


A seguir está o layout de uma operação de serviço do lado do servidor

-   const [WS \_ OPERATION \_ CONTEXT](ws-operation-context.md) \* context: o contexto de [operação](context.md).
-   Parâmetros de operações de serviço: parâmetros pertencentes à operação de serviço.
-   const [**WS \_ ASYNC \_ CONTEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) \* asyncContext: contexto assíncrono para executar as operações de serviço de forma assíncrona.
-   [WS \_ Erro DE](ws-error.md) \* ERRO: objeto de erro rich.

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

O lado do servidor deve usar falhas para fornecer condições de erro ao cliente. Ele pode fazer isso retornando um HRESULT com falha e incorporação da falha no objeto de erro.

Se a falha não estiver definida no objeto de erro e um HRESULT de falha for retornado, a infraestrutura tentará entregar uma falha de volta ao cliente. O nível de detalhes divulgados para o cliente nesse caso é controlado pela [](service-host.md)propriedade do serviço DIVULGAÇÃO DE FALHA DA PROPRIEDADE DO SERVIÇO [**WS \_ \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) no Host de Serviço .

## <a name="call-completion"></a>Conclusão da chamada

Uma chamada em uma operação de serviço do lado do servidor síncrona é contada como concluída quando ele retorna o controle de volta para o host de serviço. Para uma operação de serviço assíncrona, uma chamada é considerada concluída depois que a notificação de retorno de chamada é emitida pela implementação da operação de serviço.

## <a name="call-lifetime"></a>Tempo de vida da chamada

É preciso ter cuidado especial ao implementar uma operação de serviço do lado do servidor sobre seu tempo de vida. O tempo de vida de uma chamada pode afetar muito quanto tempo o host de serviço leva para ser desligado.

Se espera-se que uma operação de serviço do lado do servidor bloqueie devido a alguma operação de limite de E/S, é recomendável registrar um retorno de chamada de cancelamento de forma que seja notificado se quando o host de serviço estiver sendo anulado ou quando a conexão subjacente for fechada pelo cliente.

## <a name="server-side-service-operations-and-memory-consideration"></a>Considerações sobre memória e operações de serviço do lado do servidor

Se uma operação de serviço precisar alocar memória para seus parâmetros de saída, ela deverá usar o objeto HEAP do [WS \_ ](ws-heap.md) disponível para ele por meio do [CONTEXTO DE OPERAÇÃO \_ \_ do WS.](ws-operation-context.md)

Exemplo: Operação de Serviço e HEAP do WS \_

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

-   WS \_ S \_ ASYNC: a chamada será concluída assíncrona.
-   WS S END: chamada concluída com êxito, o servidor não está esperando \_ \_ nenhuma MENSAGEM [WS \_ ](ws-message.md) do cliente além dessa chamada. Se outra MENSAGEM WS \_ entrar, o servidor deverá anular o canal.
-   NOERROR/Todos os outros HRESULTS de sucesso: chamada concluída com êxito. Observe que é recomendável que o aplicativo não retorne HRESULT, em seguida, NOERROR para a conclusão bem-sucedida da operação de serviço.
-   Tudo com uma falha HRESULT: uma falha será enviado de volta para o cliente se uma estiver disponível em WS \_ ERROR. Caso contrário, uma falha genérica será enviado de volta para o cliente. Consulte a discussão sobre falhas acima.

Consulte, [Cancelamento de chamada.](call-cancellation.md)

 

 




