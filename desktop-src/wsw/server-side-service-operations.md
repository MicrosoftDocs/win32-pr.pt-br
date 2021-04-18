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
# <a name="server-side-service-operations"></a><span data-ttu-id="c99fe-106">Operações de serviço no servidor</span><span class="sxs-lookup"><span data-stu-id="c99fe-106">Server Side Service Operations</span></span>

<span data-ttu-id="c99fe-107">Esta seção descreve as operações de serviço do lado do serviço.</span><span class="sxs-lookup"><span data-stu-id="c99fe-107">This section describes service side service operations.</span></span>


<span data-ttu-id="c99fe-108">Este é o layout de uma operação de serviço no servidor</span><span class="sxs-lookup"><span data-stu-id="c99fe-108">The following is the layout of a server side service operation</span></span>

-   <span data-ttu-id="c99fe-109">contexto [de \_ \_ contexto de operação const WS](ws-operation-context.md) \* : [o contexto](context.md)de operação.</span><span class="sxs-lookup"><span data-stu-id="c99fe-109">const [WS\_OPERATION\_CONTEXT](ws-operation-context.md)\* context: The operation [context](context.md).</span></span>
-   <span data-ttu-id="c99fe-110">Parâmetros de operações de serviço: parâmetros que pertencem à operação de serviço.</span><span class="sxs-lookup"><span data-stu-id="c99fe-110">Service Operations Parameters: Parameters pertaining to the service operation.</span></span>
-   <span data-ttu-id="c99fe-111">const [**WS \_ Async \_ Context**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) \* asyncContext: contexto assíncrono para executar as operações de serviço de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="c99fe-111">const [**WS\_ASYNC\_CONTEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context)\* asyncContext: Async context for executing the service operations asynchronously.</span></span>
-   <span data-ttu-id="c99fe-112">[WS \_ Erro de erro](ws-error.md) \* : objeto de erro avançado.</span><span class="sxs-lookup"><span data-stu-id="c99fe-112">[WS\_ERROR](ws-error.md)\* error: Rich error object.</span></span>

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

## <a name="fault-and-error-handling"></a><span data-ttu-id="c99fe-113">Tratamento de falhas e erros</span><span class="sxs-lookup"><span data-stu-id="c99fe-113">Fault And Error Handling</span></span>

<span data-ttu-id="c99fe-114">O lado do servidor deve usar falhas para fornecer condições de erro ao cliente.</span><span class="sxs-lookup"><span data-stu-id="c99fe-114">The server side should use faults to deliver error conditions to the client.</span></span> <span data-ttu-id="c99fe-115">Isso pode fazer isso retornando um HRESULT com falha e inserindo a falha no objeto de erro.</span><span class="sxs-lookup"><span data-stu-id="c99fe-115">It can do so by returning a failing HRESULT and embedding the fault in the error object.</span></span>

<span data-ttu-id="c99fe-116">Se a falha não estiver definida no objeto de erro e um HRESULT de falha for retornado, a infraestrutura tentará fornecer uma falha de volta ao cliente.</span><span class="sxs-lookup"><span data-stu-id="c99fe-116">If the fault is not set on the error object and a failure HRESULT is returned, the infrastructure will attempt deliver a fault back to client.</span></span> <span data-ttu-id="c99fe-117">O nível de detalhes divulgado ao cliente nesse caso é controlado pela propriedade serviço de [**divulgação de \_ \_ falha de \_ propriedade \_ de serviço WS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) no [host de serviço](service-host.md).</span><span class="sxs-lookup"><span data-stu-id="c99fe-117">The level of details disclosed to the client in such a case is controlled by [**WS\_SERVICE\_PROPERTY\_FAULT\_DISCLOSURE**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) service property on the [Service Host](service-host.md).</span></span>

## <a name="call-completion"></a><span data-ttu-id="c99fe-118">Conclusão da chamada</span><span class="sxs-lookup"><span data-stu-id="c99fe-118">Call Completion</span></span>

<span data-ttu-id="c99fe-119">Uma chamada em uma operação de serviço do servidor síncrono deve ser concluída quando ela retornar o controle de volta ao host de serviço.</span><span class="sxs-lookup"><span data-stu-id="c99fe-119">A call on a synchronous server side service operation is said to be complete when either it has returned control back to the service host.</span></span> <span data-ttu-id="c99fe-120">Para uma operação de serviço assíncrona, uma chamada é considerada completa quando a notificação de retorno de chamada é emitida pela implementação da operação de serviço.</span><span class="sxs-lookup"><span data-stu-id="c99fe-120">For an asynchronous service operation a call is considered complete once the callback notification is issued by the service operation implementation.</span></span>

## <a name="call-lifetime"></a><span data-ttu-id="c99fe-121">Tempo de vida da chamada</span><span class="sxs-lookup"><span data-stu-id="c99fe-121">Call Lifetime</span></span>

<span data-ttu-id="c99fe-122">Deve-se tomar cuidado especial ao implementar uma operação de serviço no servidor sobre seu tempo de vida.</span><span class="sxs-lookup"><span data-stu-id="c99fe-122">Special care should be taken when implementing a server side service operation about its lifetime.</span></span> <span data-ttu-id="c99fe-123">O tempo de vida de uma chamada pode afetar muito quanto tempo o host de serviço leva para ser desligado.</span><span class="sxs-lookup"><span data-stu-id="c99fe-123">The lifetime of a call can greatly affect how long the service host takes to shutdown.</span></span>

<span data-ttu-id="c99fe-124">Se espera-se que uma operação de serviço do servidor seja bloqueada devido a alguma operação associada de e/s, é recomendável que ele registre um retorno de chamada de cancelamento, de modo que seja notificado se quando o host de serviço estiver sendo anulado ou quando a conexão subjacente for fechada pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="c99fe-124">If a server side service operation is expected to block because of some IO bound operation, it is recommended that it registers a cancellation callback such that it is notified if when service host is being aborted, or when the underlying connection is closed by the client.</span></span>

## <a name="server-side-service-operations-and-memory-consideration"></a><span data-ttu-id="c99fe-125">Considerações de memória e operações de serviço no servidor</span><span class="sxs-lookup"><span data-stu-id="c99fe-125">Server side service operations and memory consideration</span></span>

<span data-ttu-id="c99fe-126">Se uma operação de serviço precisar alocar memória para seus parâmetros de saída, ela deverá usar o objeto de [ \_ heap do WS](ws-heap.md) disponível por meio do [contexto de \_ operação \_ do WS](ws-operation-context.md).</span><span class="sxs-lookup"><span data-stu-id="c99fe-126">If a service operation needs to allocate memory for its outgoing parameters, it should use [WS\_HEAP](ws-heap.md) object available to it through the [WS\_OPERATION\_CONTEXT](ws-operation-context.md).</span></span>

<span data-ttu-id="c99fe-127">Exemplo: operação de serviço e WS \_ heap</span><span class="sxs-lookup"><span data-stu-id="c99fe-127">Example: Service Operation and WS\_HEAP</span></span>

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

## <a name="return-values"></a><span data-ttu-id="c99fe-128">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="c99fe-128">Return Values</span></span>

-   <span data-ttu-id="c99fe-129">WS \_ S \_ Async: a chamada será concluída assíncrona.</span><span class="sxs-lookup"><span data-stu-id="c99fe-129">WS\_S\_ASYNC: Call will be completed async.</span></span>
-   <span data-ttu-id="c99fe-130">WS \_ - \_ end: chamada concluída com êxito, o servidor não está esperando nenhuma [ \_ mensagem WS](ws-message.md) do cliente além dessa chamada.</span><span class="sxs-lookup"><span data-stu-id="c99fe-130">WS\_S\_END: Call completed successfully, the server is not expecting any [WS\_MESSAGE](ws-message.md) from the client beyond this call.</span></span> <span data-ttu-id="c99fe-131">Se outra mensagem WS for \_ recebida, o servidor deverá abortar o canal.</span><span class="sxs-lookup"><span data-stu-id="c99fe-131">If another WS\_MESSAGE comes in then the server should abort the channel.</span></span>
-   <span data-ttu-id="c99fe-132">NOERROR/todos os outros HRESULTs de êxito: chamada concluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="c99fe-132">NOERROR/All other success HRESULTS: Call completed successfully.</span></span> <span data-ttu-id="c99fe-133">Observe que é recomendável que o aplicativo não retorne HRESULT outro, então NOERROR para a conclusão bem-sucedida da operação de serviço.</span><span class="sxs-lookup"><span data-stu-id="c99fe-133">Note that it is recommended that the application should not return HRESULT other then NOERROR for successful completion of service operation.</span></span>
-   <span data-ttu-id="c99fe-134">Tudo com falha HRESULT: uma falha é enviada de volta para o cliente se uma estiver disponível em \_ erro WS.</span><span class="sxs-lookup"><span data-stu-id="c99fe-134">Everything with a failure HRESULT: A fault is send back to the client if one is available in WS\_ERROR.</span></span> <span data-ttu-id="c99fe-135">Caso contrário, uma falha genérica será enviada de volta ao cliente.</span><span class="sxs-lookup"><span data-stu-id="c99fe-135">Otherwise a generic fault is send back to the client.</span></span> <span data-ttu-id="c99fe-136">Consulte a discussão sobre falhas acima.</span><span class="sxs-lookup"><span data-stu-id="c99fe-136">See fault discussion above.</span></span>

<span data-ttu-id="c99fe-137">Consulte o [cancelamento da chamada](call-cancellation.md).</span><span class="sxs-lookup"><span data-stu-id="c99fe-137">See, [Call cancellation](call-cancellation.md).</span></span>

 

 




