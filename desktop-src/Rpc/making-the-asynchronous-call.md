---
title: Fazendo a chamada assíncrona
description: Antes de poder fazer uma chamada remota assíncrona, o cliente deve inicializar o identificador assíncrono. Os programas cliente e servidor usam ponteiros para \_ a \_ estrutura de estado assíncrono RPC para identificadores assíncronos.
ms.assetid: b40308ef-88ae-4c80-9118-29c5ffee77ad
keywords:
- Chamada de procedimento remoto RPC, tarefas, fazendo chamadas assíncronas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa06f60b43a7dff3a29223ff1d8e9ad726c0e938
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105778523"
---
# <a name="making-the-asynchronous-call"></a><span data-ttu-id="2bec7-105">Fazendo a chamada assíncrona</span><span class="sxs-lookup"><span data-stu-id="2bec7-105">Making the Asynchronous Call</span></span>

<span data-ttu-id="2bec7-106">Antes de poder fazer uma chamada remota assíncrona, o cliente deve inicializar o identificador assíncrono.</span><span class="sxs-lookup"><span data-stu-id="2bec7-106">Before it can make an asynchronous remote call, the client must initialize the asynchronous handle.</span></span> <span data-ttu-id="2bec7-107">Os programas cliente e servidor usam ponteiros para a estrutura de [**\_ \_ estado assíncrono RPC**](/windows/desktop/api/Rpcasync/ns-rpcasync-rpc_async_state) para identificadores assíncronos.</span><span class="sxs-lookup"><span data-stu-id="2bec7-107">Client and server programs use pointers to the [**RPC\_ASYNC\_STATE**](/windows/desktop/api/Rpcasync/ns-rpcasync-rpc_async_state) structure for asynchronous handles.</span></span>

<span data-ttu-id="2bec7-108">Cada chamada pendente deve ter seu próprio identificador assíncrono exclusivo.</span><span class="sxs-lookup"><span data-stu-id="2bec7-108">Every outstanding call must have its own unique asynchronous handle.</span></span> <span data-ttu-id="2bec7-109">O cliente cria o identificador e o passa para a função [**RpcAsyncInitializeHandle**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncinitializehandle) .</span><span class="sxs-lookup"><span data-stu-id="2bec7-109">The client creates the handle and passes it to the [**RpcAsyncInitializeHandle**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncinitializehandle) function.</span></span> <span data-ttu-id="2bec7-110">Para que a chamada seja concluída corretamente, o cliente deve garantir que a memória do identificador não seja liberada até receber a resposta assíncrona do servidor.</span><span class="sxs-lookup"><span data-stu-id="2bec7-110">For the call to complete correctly, the client must ensure that the memory for the handle is not released until it receives the server's asynchronous reply.</span></span> <span data-ttu-id="2bec7-111">Além disso, antes de fazer outra chamada em um identificador assíncrono existente, o cliente deve reinicializar o identificador.</span><span class="sxs-lookup"><span data-stu-id="2bec7-111">Also, before making another call on an existing asynchronous handle, the client must reinitialize the handle.</span></span> <span data-ttu-id="2bec7-112">A falha em fazer isso pode fazer com que o stub do cliente gere uma exceção durante a chamada.</span><span class="sxs-lookup"><span data-stu-id="2bec7-112">Failure to do this can cause the client stub to raise an exception during the call.</span></span> <span data-ttu-id="2bec7-113">O cliente também deve garantir que os buffers que ele fornece para parâmetros de \[ [**saída**](/windows/desktop/Midl/out-idl) \] e os \[ parâmetros [**de**](/windows/desktop/Midl/in) **saída** \] para um procedimento remoto assíncrono permaneçam alocados até que ele tenha recebido a resposta do servidor.</span><span class="sxs-lookup"><span data-stu-id="2bec7-113">The client must also ensure that the buffers it supplies for \[[**out**](/windows/desktop/Midl/out-idl)\] parameters and \[[**in**](/windows/desktop/Midl/in), **out**\] parameters to an asynchronous remote procedure remain allocated until it has received the reply from the server.</span></span>

<span data-ttu-id="2bec7-114">Quando ele invoca um procedimento remoto assíncrono, o cliente deve selecionar o método que a biblioteca de tempo de execução RPC usará para notificá-lo da conclusão da chamada.</span><span class="sxs-lookup"><span data-stu-id="2bec7-114">When it invokes an asynchronous remote procedure, the client must select the method that the RPC run-time library will use to notify it of the call's completion.</span></span> <span data-ttu-id="2bec7-115">O cliente pode receber essa notificação em qualquer uma das seguintes maneiras:</span><span class="sxs-lookup"><span data-stu-id="2bec7-115">The client can receive this notification in any one of the following ways:</span></span>

-   <span data-ttu-id="2bec7-116">Circunstância.</span><span class="sxs-lookup"><span data-stu-id="2bec7-116">Event.</span></span> <span data-ttu-id="2bec7-117">O cliente pode especificar um evento a ser acionado quando a chamada for concluída.</span><span class="sxs-lookup"><span data-stu-id="2bec7-117">The client can specify an event to be fired when the call has completed.</span></span> <span data-ttu-id="2bec7-118">Para obter detalhes, consulte [objetos de evento](/windows/desktop/Sync/event-objects).</span><span class="sxs-lookup"><span data-stu-id="2bec7-118">For details, see [Event Objects](/windows/desktop/Sync/event-objects).</span></span>
-   <span data-ttu-id="2bec7-119">Executar a sondagem.</span><span class="sxs-lookup"><span data-stu-id="2bec7-119">Polling.</span></span> <span data-ttu-id="2bec7-120">O cliente pode chamar repetidamente [**RpcAsyncGetCallStatus**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncgetcallstatus).</span><span class="sxs-lookup"><span data-stu-id="2bec7-120">The client can repeatedly call [**RpcAsyncGetCallStatus**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncgetcallstatus).</span></span> <span data-ttu-id="2bec7-121">Se o valor de retorno for algo diferente da \_ \_ chamada assíncrona de RPC S \_ \_ pendente, a chamada será concluída.</span><span class="sxs-lookup"><span data-stu-id="2bec7-121">If the return value is anything other than RPC\_S\_ASYNC\_CALL\_PENDING, the call is complete.</span></span> <span data-ttu-id="2bec7-122">Esse método usa mais tempo de CPU do que os outros métodos descritos aqui.</span><span class="sxs-lookup"><span data-stu-id="2bec7-122">This method uses more CPU time than the other methods described here.</span></span>
-   <span data-ttu-id="2bec7-123">APC.</span><span class="sxs-lookup"><span data-stu-id="2bec7-123">APC.</span></span> <span data-ttu-id="2bec7-124">O cliente pode especificar uma [APC (chamada de procedimento assíncrono)](/windows/desktop/Sync/asynchronous-procedure-calls) que é chamada quando a chamada é concluída.</span><span class="sxs-lookup"><span data-stu-id="2bec7-124">The client can specify an [asynchronous procedure call (APC)](/windows/desktop/Sync/asynchronous-procedure-calls) that gets called when the call completes.</span></span> <span data-ttu-id="2bec7-125">Para o protótipo da função APC, consulte [**\_ rotina RPCNOTIFICATION**](/previous-versions/aa375808(v=vs.80)).</span><span class="sxs-lookup"><span data-stu-id="2bec7-125">For the prototype of the APC function, see [**RPCNOTIFICATION\_ROUTINE**](/previous-versions/aa375808(v=vs.80)).</span></span> <span data-ttu-id="2bec7-126">A APC é chamada com seu parâmetro de evento definido como RpcCallComplete.</span><span class="sxs-lookup"><span data-stu-id="2bec7-126">The APC is called with its Event parameter set to RpcCallComplete.</span></span> <span data-ttu-id="2bec7-127">Para que o APCs seja expedido, o thread do cliente deve estar em um estado de espera alertável.</span><span class="sxs-lookup"><span data-stu-id="2bec7-127">For APCs to get dispatched, the client thread must be in an alertable wait state.</span></span>

    <span data-ttu-id="2bec7-128">Se o campo **hThread** no identificador assíncrono for definido como 0, os APCs serão enfileirados no thread que fez a chamada assíncrona.</span><span class="sxs-lookup"><span data-stu-id="2bec7-128">If the **hThread** field in the asynchronous handle is set to 0, the APCs are queued on the thread that made the asynchronous call.</span></span> <span data-ttu-id="2bec7-129">Se ele for diferente de zero, os APCs serão enfileirados no thread especificado por m.</span><span class="sxs-lookup"><span data-stu-id="2bec7-129">If it is nonzero, the APCs are queued on the thread specified by m.</span></span>

-   <span data-ttu-id="2bec7-130">IOC.</span><span class="sxs-lookup"><span data-stu-id="2bec7-130">IOC.</span></span> <span data-ttu-id="2bec7-131">A porta de conclusão de e/s é notificada com os parâmetros especificados no identificador assíncrono.</span><span class="sxs-lookup"><span data-stu-id="2bec7-131">The I/O completion port is notified with the parameters specified in the asynchronous handle.</span></span> <span data-ttu-id="2bec7-132">Para obter mais informações, consulte [**CreateIoCompletionPort**](/windows/desktop/FileIO/createiocompletionport).</span><span class="sxs-lookup"><span data-stu-id="2bec7-132">For more information, see [**CreateIoCompletionPort**](/windows/desktop/FileIO/createiocompletionport).</span></span>
-   <span data-ttu-id="2bec7-133">Identificador do Windows.</span><span class="sxs-lookup"><span data-stu-id="2bec7-133">Windows handle.</span></span> <span data-ttu-id="2bec7-134">Uma mensagem é postada para o identificador de janela especificado (HWND).</span><span class="sxs-lookup"><span data-stu-id="2bec7-134">A message is posted to the specified window handle (HWND).</span></span>

<span data-ttu-id="2bec7-135">O fragmento de código a seguir mostra as etapas essenciais necessárias para inicializar um identificador assíncrono e usá-lo para fazer uma chamada de procedimento remoto assíncrona.</span><span class="sxs-lookup"><span data-stu-id="2bec7-135">The following code fragment shows the essential steps required for initializing an asynchronous handle and using it to make an asynchronous remote procedure call.</span></span>


```C++
RPC_ASYNC_STATE Async;
RPC_STATUS status;
 
// Initialize the handle.
status = RpcAsyncInitializeHandle(&Async, sizeof(RPC_ASYNC_STATE));
if (status)
{
    // Code to handle the error goes here.
}
 
Async.UserInfo = NULL;
Async.NotificationType = RpcNotificationTypeEvent;
 
Async.u.hEvent = CreateEvent(NULL, FALSE, FALSE, NULL);
if (Async.u.hEvent == 0)
{
    // Code to handle the error goes here.
}
// Call an asynchronous RPC routine here
RpcTryExcept
{
    printf("\nCalling the remote procedure 'AsyncFunc'\n");
    AsyncFunc(&Async, AsyncRPC_ClientIfHandle, nAsychDelay);
}
RpcExcept(1)
{
    ulCode = RpcExceptionCode();
    printf("AsyncFunc: Run time reported exception 0x%lx = %ld\n", 
            ulCode, ulCode);
}
RpcEndExcept
 
// Call a synchronous routine while
// the asynchronous procedure is still running
RpcTryExcept
{
    printf("\nCalling the remote procedure 'NonAsyncFunc'\n");
    NonAsyncFunc(AsyncRPC_ClientIfHandle, pszMessage);
    fprintf(stderr, 
            "While 'AsyncFunc' is running asynchronously,\n"
            "we still can send message to the server in the mean "
            "time.\n\n");
}
RpcExcept(1)
{
    ulCode = RpcExceptionCode();
    printf("NonAsyncFunc: Run time reported exception 0x%lx = %ld\n", 
            ulCode, ulCode);
}
RpcEndExcept
```



<span data-ttu-id="2bec7-136">Como demonstra este exemplo, o programa cliente pode executar chamadas síncronas de procedimento remoto enquanto uma chamada de procedimento assíncrono ainda está pendente.</span><span class="sxs-lookup"><span data-stu-id="2bec7-136">As this example demonstrates, your client program can execute synchronous remote procedure calls while an asynchronous procedure call is still pending.</span></span> <span data-ttu-id="2bec7-137">Esse cliente cria um objeto de evento para a biblioteca de tempo de execução RPC a ser usada para notificá-lo quando a chamada assíncrona for concluída.</span><span class="sxs-lookup"><span data-stu-id="2bec7-137">This client creates an event object for the RPC run-time library to use to notify it when the asynchronous call completes.</span></span>

> [!Note]  
> <span data-ttu-id="2bec7-138">A notificação de conclusão não será retornada de uma rotina RPC assíncrona se uma exceção RPC for gerada durante uma chamada assíncrona.</span><span class="sxs-lookup"><span data-stu-id="2bec7-138">Notification of completion will not be returned from an asynchronous RPC routine if an RPC exception is raised during an asynchronous call.</span></span>

 

 

 