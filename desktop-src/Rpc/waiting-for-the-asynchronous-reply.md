---
title: Aguardando a resposta assíncrona
description: O que o cliente faz enquanto aguarda ser notificado de uma resposta do servidor depende do mecanismo de notificação que ele seleciona.
ms.assetid: b1d4ea54-26bc-49f9-8cc1-a74fd4ffced3
keywords:
- Chamada de procedimento remoto RPC, tarefas, aguardando respostas assíncronas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0890b3024a05bb704f7b5a803c4b1e517c65ee21
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294310"
---
# <a name="waiting-for-the-asynchronous-reply"></a><span data-ttu-id="07812-104">Aguardando a resposta assíncrona</span><span class="sxs-lookup"><span data-stu-id="07812-104">Waiting for the Asynchronous Reply</span></span>

<span data-ttu-id="07812-105">O que o cliente faz enquanto aguarda ser notificado de uma resposta do servidor depende do mecanismo de notificação que ele seleciona.</span><span class="sxs-lookup"><span data-stu-id="07812-105">What the client does while it waits to be notified of a reply from the server depends on the notification mechanism it selects.</span></span>

<span data-ttu-id="07812-106">Se o cliente usar um evento para notificação, ele normalmente chamará a função [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) ou a função [**WaitForSingleObjectEx**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex) .</span><span class="sxs-lookup"><span data-stu-id="07812-106">If the client uses an event for notification, it will typically call the [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) function or the [**WaitForSingleObjectEx**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex) function.</span></span> <span data-ttu-id="07812-107">O cliente entra em um estado bloqueado quando chama uma dessas funções.</span><span class="sxs-lookup"><span data-stu-id="07812-107">The client enters a blocked state when it calls either of these functions.</span></span> <span data-ttu-id="07812-108">Isso é eficiente porque o cliente não consome ciclos de execução de CPU enquanto está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="07812-108">This is efficient because the client does not consume CPU run cycles while it is blocked.</span></span>

<span data-ttu-id="07812-109">Quando ele usa a sondagem para aguardar seus resultados, o programa cliente entra em um loop que chama repetidamente a função [**RpcAsyncGetCallStatus**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncgetcallstatus).</span><span class="sxs-lookup"><span data-stu-id="07812-109">When it uses polling to wait for its results, the client program enters a loop that repeatedly calls the function [**RpcAsyncGetCallStatus**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncgetcallstatus).</span></span> <span data-ttu-id="07812-110">Esse é um método eficiente de espera se o seu programa cliente faz outro processamento no loop de sondagem.</span><span class="sxs-lookup"><span data-stu-id="07812-110">This is an efficient method of waiting if your client program does other processing in the polling loop.</span></span> <span data-ttu-id="07812-111">Por exemplo, ele pode preparar dados em pequenas partes para uma chamada de procedimento remoto assíncrona subsequente.</span><span class="sxs-lookup"><span data-stu-id="07812-111">For instance, it can prepare data in small chunks for a subsequent asynchronous remote procedure call.</span></span> <span data-ttu-id="07812-112">Depois que cada parte for concluída, o cliente poderá sondar a chamada de procedimento remoto assíncrona pendente para ver se ela está concluída.</span><span class="sxs-lookup"><span data-stu-id="07812-112">After each chunk is finished, your client can poll the outstanding asynchronous remote procedure call to see if it is complete.</span></span>

<span data-ttu-id="07812-113">O programa cliente pode fornecer uma APC (chamada de procedimento assíncrono), que é um tipo de função de chamada de retorno que a biblioteca de tempo de execução RPC invocará quando a chamada de procedimento remoto assíncrona for concluída.</span><span class="sxs-lookup"><span data-stu-id="07812-113">Your client program can provide an asynchronous procedure call (APC), which is a type of callback function that the RPC run-time library will invoke when the asynchronous remote procedure call completes.</span></span> <span data-ttu-id="07812-114">O programa cliente deve estar em um estado de espera alertável.</span><span class="sxs-lookup"><span data-stu-id="07812-114">Your client program must be in an alertable wait state.</span></span> <span data-ttu-id="07812-115">Isso normalmente significa que o cliente chama uma função da API do Windows para se colocar em um estado bloqueado.</span><span class="sxs-lookup"><span data-stu-id="07812-115">This typically means that the client calls a Windows API function to put itself in a blocked state.</span></span> <span data-ttu-id="07812-116">Para obter mais informações, consulte [chamadas de procedimento assíncrono](/windows/desktop/Sync/asynchronous-procedure-calls).</span><span class="sxs-lookup"><span data-stu-id="07812-116">For more information, see [Asynchronous Procedure Calls](/windows/desktop/Sync/asynchronous-procedure-calls).</span></span>

> [!Note]  
> <span data-ttu-id="07812-117">A notificação de conclusão não será retornada de uma rotina RPC assíncrona se uma exceção RPC for gerada durante uma chamada assíncrona.</span><span class="sxs-lookup"><span data-stu-id="07812-117">Notification of completion will not be returned from an asynchronous RPC routine if an RPC exception is raised during a asynchronous call.</span></span>

 

<span data-ttu-id="07812-118">Se o programa cliente usar uma porta de conclusão de e/s para receber a notificação de conclusão, ele deverá chamar a função [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .</span><span class="sxs-lookup"><span data-stu-id="07812-118">If your client program uses an I/O completion port to receive completion notification, it must call the [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span> <span data-ttu-id="07812-119">Quando isso é feito, ele pode aguardar indefinidamente uma resposta ou continuar a fazer outro processamento.</span><span class="sxs-lookup"><span data-stu-id="07812-119">When it does, it can either wait indefinitely for a response or continue to do other processing.</span></span> <span data-ttu-id="07812-120">Se ele faz outro processamento enquanto aguarda uma resposta, ele deve sondar a porta de conclusão com a função **GetQueuedCompletionStatus** .</span><span class="sxs-lookup"><span data-stu-id="07812-120">If it does other processing while it waits for a reply, it must poll the completion port with the **GetQueuedCompletionStatus** function.</span></span> <span data-ttu-id="07812-121">Nesse caso, normalmente, ele precisa definir *dwMilliseconds* como zero.</span><span class="sxs-lookup"><span data-stu-id="07812-121">In this case, it typically needs to set the *dwMilliseconds* to zero.</span></span> <span data-ttu-id="07812-122">Isso faz com que o **GetQueuedCompletionStatus** retorne imediatamente, mesmo que a chamada assíncrona não tenha sido concluída.</span><span class="sxs-lookup"><span data-stu-id="07812-122">This causes **GetQueuedCompletionStatus** to return immediately, even if the asynchronous call has not completed.</span></span>

<span data-ttu-id="07812-123">Os programas cliente também podem receber a notificação de conclusão por meio de suas filas de mensagens do Windows.</span><span class="sxs-lookup"><span data-stu-id="07812-123">Client programs can also receive completion notification through their window message queues.</span></span> <span data-ttu-id="07812-124">Nessa situação, eles simplesmente processam a mensagem de conclusão como fariam com qualquer mensagem do Windows.</span><span class="sxs-lookup"><span data-stu-id="07812-124">In this situation, they simply process the completion message as they would any Windows message.</span></span>

<span data-ttu-id="07812-125">Em um aplicativo multithread, uma chamada assíncrona pode ser cancelada pelo cliente somente depois que o thread que originou a chamada foi retornado com êxito da chamada.</span><span class="sxs-lookup"><span data-stu-id="07812-125">In a multithreaded application, an asynchronous call can be canceled by the client only after the thread that originated the call has returned successfully from the call.</span></span> <span data-ttu-id="07812-126">Isso garante que a chamada não seja cancelada de forma assíncrona por outro thread após a falha de uma chamada síncrona.</span><span class="sxs-lookup"><span data-stu-id="07812-126">This ensures that the call is not canceled asynchronously by another thread after it failed a synchronous call.</span></span> <span data-ttu-id="07812-127">Como prática padrão, uma chamada assíncrona que falha de forma síncrona não deve ser cancelada de modo assíncrono.</span><span class="sxs-lookup"><span data-stu-id="07812-127">As standard practice, an asynchronous call that fails synchronously should not be canceled asynchronously.</span></span> <span data-ttu-id="07812-128">O aplicativo cliente deve observar esse comportamento se as chamadas podem ser emitidas e canceladas em threads diferentes.</span><span class="sxs-lookup"><span data-stu-id="07812-128">The client application must observe this behavior if calls may be issued and canceled on different threads.</span></span> <span data-ttu-id="07812-129">Além disso, após a chamada ser cancelada, o código do cliente deve aguardar a notificação de conclusão e concluir a chamada.</span><span class="sxs-lookup"><span data-stu-id="07812-129">Also, after the call is canceled, the client code must wait for the completion notification and complete the call.</span></span> <span data-ttu-id="07812-130">A função [**RpcAsyncCancelCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall) simplesmente recorrendo a notificação de conclusão; Não é um substituto da conclusão da chamada.</span><span class="sxs-lookup"><span data-stu-id="07812-130">The [**RpcAsyncCancelCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall) function simply rushes the completion notification; it is not a substitute for completing the call.</span></span>

<span data-ttu-id="07812-131">O fragmento de código a seguir ilustra como um programa cliente pode usar um evento para aguardar uma resposta assíncrona.</span><span class="sxs-lookup"><span data-stu-id="07812-131">The following code fragment illustrates how a client program can use an event to wait for an asynchronous reply.</span></span>


```C++
// This code fragment assumes that Async is a valid asynchronous
// RPC handle.
if (WaitForSingleObject(Async.u.hEvent, INFINITE) == WAIT_FAILED)
{
    RpcRaiseException(APP_ERROR);
}
```



<span data-ttu-id="07812-132">Os programas cliente que usam uma APC para receber notificação de uma resposta assíncrona normalmente se colocam em um estado bloqueado.</span><span class="sxs-lookup"><span data-stu-id="07812-132">Client programs that use an APC to receive notification of an asynchronous reply typically put themselves into a blocked state.</span></span> <span data-ttu-id="07812-133">O fragmento de código a seguir mostra isso.</span><span class="sxs-lookup"><span data-stu-id="07812-133">The following code fragment shows this.</span></span>


```C++
if (SleepEx(INFINITE, TRUE) != WAIT_IO_COMPLETION)
{
    RpcRaiseException(APP_ERROR);
}
```



<span data-ttu-id="07812-134">Nesse caso, o programa cliente entra em suspensão, não consumindo ciclos de CPU, até que a biblioteca de tempo de execução RPC chame a APC (não mostrada).</span><span class="sxs-lookup"><span data-stu-id="07812-134">In this case, the client program goes to sleep, consuming no CPU cycles, until the RPC run-time library calls the APC (not shown).</span></span>

<span data-ttu-id="07812-135">O exemplo a seguir demonstra um cliente que usa uma porta de conclusão de e/s para aguardar uma resposta assíncrona.</span><span class="sxs-lookup"><span data-stu-id="07812-135">The next example demonstrates a client that uses an I/O completion port to wait for an asynchronous reply.</span></span>


```C++
// This code fragment assumes that Async is a valid asynchronous
// RPC handle.
if (!GetQueuedCompletionStatus(
         Async.u.IOC.hIOPort,
         &Async.u.IOC.dwNumberOfBytesTransferred,
         &Async.u.IOC.dwCompletionKey,
         &Async.u.IOC.lpOverlapped,
         INFINITE))
{
    RpcRaiseException(APP_ERROR);
}
```



<span data-ttu-id="07812-136">No exemplo anterior, a chamada para [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) aguarda indefinidamente até que a chamada de procedimento remoto assíncrona seja concluída.</span><span class="sxs-lookup"><span data-stu-id="07812-136">In the preceding example, the call to [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) waits indefinitely until the asynchronous remote procedure call completes.</span></span>

<span data-ttu-id="07812-137">Uma possível armadilha ocorre durante a gravação de aplicativos multithread.</span><span class="sxs-lookup"><span data-stu-id="07812-137">One potential pitfall occurs when writing multithreaded applications.</span></span> <span data-ttu-id="07812-138">Se um thread invocar uma chamada de procedimento remoto e terminar antes de receber a notificação de que o envio foi concluído, a chamada de procedimento remoto poderá falhar e o stub do cliente poderá fechar a conexão com o servidor.</span><span class="sxs-lookup"><span data-stu-id="07812-138">If a thread invokes a remote procedure call and then terminates before it receives notification that the send completed, the remote procedure call may fail and the client stub may close the connection to the server.</span></span> <span data-ttu-id="07812-139">Portanto, os threads que chamam um procedimento remoto não devem terminar antes que a chamada seja concluída ou cancelada quando o comportamento for indesejável.</span><span class="sxs-lookup"><span data-stu-id="07812-139">Therefore, threads that call a remote procedure should not terminate before the call is completed or canceled when behavior is undesirable.</span></span>

 

 