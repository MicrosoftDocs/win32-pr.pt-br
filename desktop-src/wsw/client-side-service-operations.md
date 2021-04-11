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
ms.openlocfilehash: e4cd00bfbd832db12a722363bf5b1af8f7298345
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170438"
---
# <a name="client-side-service-operations"></a><span data-ttu-id="8da5d-106">Operações de serviço no lado do cliente</span><span class="sxs-lookup"><span data-stu-id="8da5d-106">Client-side Service Operations</span></span>

<span data-ttu-id="8da5d-107">Este é o layout de uma operação de serviço no lado do cliente:</span><span class="sxs-lookup"><span data-stu-id="8da5d-107">The following is the layout of a client-side service operation:</span></span>

-   <span data-ttu-id="8da5d-108">[WS \_ SERVIÇO \_ proxy Service](ws-service-proxy.md) -proxy \* : o [proxy de serviço](service-proxy.md) para a chamada.</span><span class="sxs-lookup"><span data-stu-id="8da5d-108">[WS\_SERVICE\_PROXY](ws-service-proxy.md)\* serviceProxy: The [service proxy](service-proxy.md) for the call.</span></span>
-   <span data-ttu-id="8da5d-109">[WS \_ ](ws-heap.md)Heap \* de heap: um heap necessário usado para serialização de corpo e desserialização da [ \_ mensagem WS](ws-message.md).</span><span class="sxs-lookup"><span data-stu-id="8da5d-109">[WS\_HEAP](ws-heap.md)\* heap: A required heap used for body serialization and deserialization of the [WS\_MESSAGE](ws-message.md).</span></span>
-   <span data-ttu-id="8da5d-110">Parâmetros de operações de serviço: parâmetros que pertencem à operação de serviço.</span><span class="sxs-lookup"><span data-stu-id="8da5d-110">Service Operations Parameters: Parameters pertaining to the service operation.</span></span>
-   <span data-ttu-id="8da5d-111">[**Chame Propriedades e sua contagem**](/windows/desktop/api/WebServices/ns-webservices-ws_call_property): uma matriz de propriedades de chamada.</span><span class="sxs-lookup"><span data-stu-id="8da5d-111">[**Call Properties and their count**](/windows/desktop/api/WebServices/ns-webservices-ws_call_property): An array of call properties.</span></span>
-   <span data-ttu-id="8da5d-112">Contagem de propriedades de [**chamada**](/windows/desktop/api/WebServices/ns-webservices-ws_call_property) : a contagem de propriedades de chamada.</span><span class="sxs-lookup"><span data-stu-id="8da5d-112">[**Call**](/windows/desktop/api/WebServices/ns-webservices-ws_call_property) property count: The count of call properties.</span></span>
-   <span data-ttu-id="8da5d-113">[**WS \_ \_Contexto assíncrono**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) asyncContext: contexto assíncrono para executar a chamada de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="8da5d-113">[**WS\_ASYNC\_CONTEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) asyncContext: Async context for executing the call asynchronously.</span></span>
-   <span data-ttu-id="8da5d-114">[WS \_ Erro de erro:](ws-error.md) objeto de erro avançado.</span><span class="sxs-lookup"><span data-stu-id="8da5d-114">[WS\_ERROR](ws-error.md) error: Rich error object.</span></span>


### <a name="signature-for-client-side-service-operations"></a><span data-ttu-id="8da5d-115">Assinatura para operações de serviço do lado do cliente</span><span class="sxs-lookup"><span data-stu-id="8da5d-115">Signature for Client-side Service Operations</span></span>

``` syntax
typedef HRESULT(CALLBACK *ICalculator_Add)(WS_SERVICE_PROXY* serviceProxy, 
                                           WS_HEAP* heap, 
                                           ULONG a, ULONG b, ULONG* result, 
                                           const WS_CALL_PROPERTY* callProperties, 
                                           const ULONG callPropertyCount, 
                                           const WS_ASYNC_CONTEXT* asyncContext, 
                                           WS_ERROR* error);
```

### <a name="memory-considerations-for-client-side-service-operations"></a><span data-ttu-id="8da5d-116">Considerações sobre memória para operações de serviço no lado do cliente</span><span class="sxs-lookup"><span data-stu-id="8da5d-116">Memory Considerations for Client-side Service Operations</span></span>

<span data-ttu-id="8da5d-117">A chamada para a operação de serviço usa um [WS \_ heap](ws-heap.md) \* como parâmetro.</span><span class="sxs-lookup"><span data-stu-id="8da5d-117">The call to the service operation takes a [WS\_HEAP](ws-heap.md)\* as parameter.</span></span> <span data-ttu-id="8da5d-118">Esse é um parâmetro necessário usado para serialização/desserialização de corpos de mensagem para parâmetros.</span><span class="sxs-lookup"><span data-stu-id="8da5d-118">This is a required parameter used for serialization/deserialization of message bodies to parameters.</span></span>

<span data-ttu-id="8da5d-119">O aplicativo deve chamar [**WsResetHeap**](/windows/desktop/api/WebServices/nf-webservices-wsresetheap) se a chamada foi bem-sucedida ou não.</span><span class="sxs-lookup"><span data-stu-id="8da5d-119">The application must call [**WsResetHeap**](/windows/desktop/api/WebServices/nf-webservices-wsresetheap) whether the call succeeded or not.</span></span> <span data-ttu-id="8da5d-120">Se a chamada for bem-sucedida e tiver parâmetros de saída, o aplicativo deverá chamar **WsResetHeap** imediatamente depois que for concluído com os parâmetros de saída.</span><span class="sxs-lookup"><span data-stu-id="8da5d-120">If the call succeeded and it has outgoing parameters, the application should call **WsResetHeap** immediately after it is finished with the outgoing parameters.</span></span>

<span data-ttu-id="8da5d-121">O aplicativo deve alocar memória para parâmetros de entrada e saída com [**WsAlloc**](/windows/desktop/api/WebServices/nf-webservices-wsalloc).</span><span class="sxs-lookup"><span data-stu-id="8da5d-121">The application should allocate memory for in and out parameters with [**WsAlloc**](/windows/desktop/api/WebServices/nf-webservices-wsalloc).</span></span> <span data-ttu-id="8da5d-122">O proxy de serviço pode precisar realocá-los, de forma que os ponteiros fornecidos serão substituídos.</span><span class="sxs-lookup"><span data-stu-id="8da5d-122">The service proxy may need to reallocate them so provided pointers will be overwritten.</span></span> <span data-ttu-id="8da5d-123">Uma tentativa de liberar essa memória fará com que o aplicativo falhe.</span><span class="sxs-lookup"><span data-stu-id="8da5d-123">An attempt to free such memory will cause the application to crash.</span></span>

### <a name="client-side-service-operation-and-ws_heap"></a><span data-ttu-id="8da5d-124">Operação de serviço do lado do cliente e WS \_ heap</span><span class="sxs-lookup"><span data-stu-id="8da5d-124">Client-side Service Operation and WS\_HEAP</span></span>

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

### <a name="error-parameter"></a><span data-ttu-id="8da5d-125">Parâmetro de erro</span><span class="sxs-lookup"><span data-stu-id="8da5d-125">Error parameter</span></span>

<span data-ttu-id="8da5d-126">O aplicativo sempre deve passar o parâmetro de erro para:</span><span class="sxs-lookup"><span data-stu-id="8da5d-126">The application should always pass in the error parameter to:</span></span>

-   <span data-ttu-id="8da5d-127">Obtenha informações de erro avançadas se ocorrer uma falha durante a chamada de operação de serviço.</span><span class="sxs-lookup"><span data-stu-id="8da5d-127">Get rich error information if a failure occurs during the service operation call.</span></span>
-   <span data-ttu-id="8da5d-128">Obtenha o objeto de falha se o serviço retornar uma falha.</span><span class="sxs-lookup"><span data-stu-id="8da5d-128">Get the fault object if the service returned back a fault.</span></span> <span data-ttu-id="8da5d-129">A falha está contida no objeto de erro.</span><span class="sxs-lookup"><span data-stu-id="8da5d-129">The fault is contained in the error object.</span></span> <span data-ttu-id="8da5d-130">Nesse caso, o valor **HRESULT** retornado da operação de serviço é de **\_ falha de \_ ponto de extremidade WS E \_ \_ recebido** (consulte [valores de retorno dos serviços Web do Windows](windows-web-services-return-values.md)).</span><span class="sxs-lookup"><span data-stu-id="8da5d-130">In this case, the **HRESULT** value returned from the service operation is **WS\_E\_ENDPOINT\_FAULT\_RECEIVED** (see [Windows Web Services Return Values](windows-web-services-return-values.md)).</span></span>

### <a name="call-properties-for-client-side-service-operations"></a><span data-ttu-id="8da5d-131">Chamar Propriedades para operações de serviço no lado do cliente</span><span class="sxs-lookup"><span data-stu-id="8da5d-131">Call Properties for Client-side Service Operations</span></span>

<span data-ttu-id="8da5d-132">As propriedades da chamada permitem que um aplicativo especifique configurações personalizadas para uma determinada chamada.</span><span class="sxs-lookup"><span data-stu-id="8da5d-132">Call properties allow an application to specify custom settings for a given call.</span></span> <span data-ttu-id="8da5d-133">Atualmente, apenas uma propriedade de chamada está disponível com o modelo de serviço, [**ID de chamada de \_ propriedade de chamada \_ \_ \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_call_property_id).</span><span class="sxs-lookup"><span data-stu-id="8da5d-133">Currently, only one call property is available with the service model, [**WS\_CALL\_PROPERTY\_CALL\_ID**](/windows/desktop/api/WebServices/ne-webservices-ws_call_property_id).</span></span>

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

### <a name="abandoning-a-call"></a><span data-ttu-id="8da5d-134">Abandonando uma chamada</span><span class="sxs-lookup"><span data-stu-id="8da5d-134">Abandoning a Call</span></span>

<span data-ttu-id="8da5d-135">Geralmente, é desejável abandonar os resultados de uma chamada para abandonar o controle de volta ao aplicativo, de modo que a conclusão da chamada real seja tratada pela infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="8da5d-135">It is often desirable to abandon the results of a call in order to relinquish the control back to the application, such that the actual call completion is handled by the infrastructure.</span></span> <span data-ttu-id="8da5d-136">O proxy de serviço fornece esse recurso por meio do [**WsAbandonCall**](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall).</span><span class="sxs-lookup"><span data-stu-id="8da5d-136">Service proxy provides this facility through [**WsAbandonCall**](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall).</span></span>

<span data-ttu-id="8da5d-137">Observe que o controle para o chamador pode não ser retornado imediatamente, a única garantia de que o tempo de execução do proxy de serviço dá é que ele não esperaria que nenhuma operação associada de e/s seja concluída antes de conceder o controle de volta ao chamador.</span><span class="sxs-lookup"><span data-stu-id="8da5d-137">Note that the control to the caller may not be given back immediately, the only guarantee that the service proxy runtime gives is that it would not wait for any I/O bound operation to complete before it gives control back to the caller.</span></span>

<span data-ttu-id="8da5d-138">Chamadas em uma operação de serviço no lado do cliente podem ser abandonadas por meio de uma chamada para [**WsAbandonCall**](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall).</span><span class="sxs-lookup"><span data-stu-id="8da5d-138">Calls on a client side service operation can be abandoned by means of a call to [**WsAbandonCall**](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall).</span></span> <span data-ttu-id="8da5d-139">Ele usa um proxy de serviço e uma ID de chamada. Uma ID de chamada é fornecida como parte de uma chamada de propriedades em uma operação de serviço.</span><span class="sxs-lookup"><span data-stu-id="8da5d-139">It takes a service proxy and a call id. A call Id is given as part of a call properties on a service operation.</span></span>

<span data-ttu-id="8da5d-140">Se a ID de chamada for 0, o proxy de serviço abandonará todas as chamadas pendentes nessa instância.</span><span class="sxs-lookup"><span data-stu-id="8da5d-140">If the call Id is 0, then the service proxy will abandon all pending calls at that instance.</span></span>

### <a name="call-timeouts"></a><span data-ttu-id="8da5d-141">Tempos limite de chamada</span><span class="sxs-lookup"><span data-stu-id="8da5d-141">Call Timeouts</span></span>

<span data-ttu-id="8da5d-142">Por padrão, um proxy de serviço tem um tempo limite de 30 segundos para cada chamada.</span><span class="sxs-lookup"><span data-stu-id="8da5d-142">By default a service proxy has a 30 second timeout for every call.</span></span> <span data-ttu-id="8da5d-143">O tempo limite em uma chamada pode ser alterado pela propriedade de proxy de serviço de [**\_ \_ \_ \_ tempo limite de chamada de propriedade de proxy WS**](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id) ao criar um proxy de serviço por meio de [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy).</span><span class="sxs-lookup"><span data-stu-id="8da5d-143">The timeout on a call can be changed by [**WS\_PROXY\_PROPERTY\_CALL\_TIMEOUT**](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id) service proxy property when creating a service proxy through [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy).</span></span>

<span data-ttu-id="8da5d-144">Depois que um tempo limite é atingido, a chamada é abandonada.</span><span class="sxs-lookup"><span data-stu-id="8da5d-144">After a timeout is reached, the call is abandoned.</span></span>

### <a name="return-values"></a><span data-ttu-id="8da5d-145">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="8da5d-145">Return Values</span></span>

<span data-ttu-id="8da5d-146">Todos os valores **HRESULT** de êxito devem ser tratados como êxito e todos os valores de falha devem ser tratados como falhas.</span><span class="sxs-lookup"><span data-stu-id="8da5d-146">All success **HRESULT** values must be treated as success, and all failure values must be treated as failures.</span></span> <span data-ttu-id="8da5d-147">A seguir estão alguns dos valores **HRESULT** que um aplicativo pode esperar:</span><span class="sxs-lookup"><span data-stu-id="8da5d-147">The following are some of the **HRESULT** values that an application can expect:</span></span>

-   <span data-ttu-id="8da5d-148">**WS \_ S \_ Async**: a chamada será concluída de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="8da5d-148">**WS\_S\_ASYNC**: Call will be completed asynchronously.</span></span>
-   <span data-ttu-id="8da5d-149">NOERROR: chamada concluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="8da5d-149">NOERROR: Call completed successfully.</span></span>
-   <span data-ttu-id="8da5d-150">**WS \_ \_Operação E \_ abandonada**: a chamada foi abandonada.</span><span class="sxs-lookup"><span data-stu-id="8da5d-150">**WS\_E\_OPERATION\_ABANDONED**: The call has been abandoned.</span></span> <span data-ttu-id="8da5d-151">O objeto de erro contém o motivo para abandono.</span><span class="sxs-lookup"><span data-stu-id="8da5d-151">The error object contains the reason for abandon.</span></span>
-   <span data-ttu-id="8da5d-152">**WS \_ E \_ \_ operação inválida**: o proxy de serviço não está em um estado apropriado para fazer uma chamada, verifique o estado do proxy de serviço para descobrir o estado do proxy de serviço.</span><span class="sxs-lookup"><span data-stu-id="8da5d-152">**WS\_E\_INVALID\_OPERATION**: The service proxy is not in an appropriate state to make a call, check the service proxy state to figure out the state of the service proxy.</span></span>

<span data-ttu-id="8da5d-153">Para obter uma lista completa de valores de retorno, consulte [valores de retorno dos serviços Web do Windows](windows-web-services-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="8da5d-153">For a complete list of return values, see [Windows Web Services Return Values](windows-web-services-return-values.md).</span></span>

### <a name="code-examples"></a><span data-ttu-id="8da5d-154">Exemplos de código</span><span class="sxs-lookup"><span data-stu-id="8da5d-154">Code Examples</span></span>

<span data-ttu-id="8da5d-155">Para obter exemplos de código, consulte o seguinte:</span><span class="sxs-lookup"><span data-stu-id="8da5d-155">For code examples, see the following:</span></span>

-   [<span data-ttu-id="8da5d-156">CallAbandonExample</span><span class="sxs-lookup"><span data-stu-id="8da5d-156">CallAbandonExample</span></span>](callabandonexample.md)
-   [<span data-ttu-id="8da5d-157">**WsAbandonCall**</span><span class="sxs-lookup"><span data-stu-id="8da5d-157">**WsAbandonCall**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall)

 

 




