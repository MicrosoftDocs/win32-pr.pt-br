---
description: Especifica um descritor de fila de conclusão usado para notificação de conclusão de e/s por envio e recebimento de solicitações com as extensões de e/s registradas do Winsock.
ms.assetid: 9196F8AF-3C48-445D-B2D5-E22A99759D92
title: RIO_CQ (Mswsockdef.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69ca4376c5b130cccaefd7170f62878f31fd1457
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105763339"
---
# <a name="rio_cq"></a><span data-ttu-id="47e06-103">RIO de \_ CQ</span><span class="sxs-lookup"><span data-stu-id="47e06-103">RIO\_CQ</span></span>

<span data-ttu-id="47e06-104">O **typedef \_ CQ do Rio** especifica um descritor de fila de conclusão usado para notificação de conclusão de e/s por envio e recebimento de solicitações com as extensões de e/s registradas do Winsock.</span><span class="sxs-lookup"><span data-stu-id="47e06-104">The **RIO\_CQ** typedef specifies a completion queue descriptor used for I/O completion notification by send and receive requests with the Winsock registered I/O extensions.</span></span>


```C++
typedef struct RIO_CQ_t* RIO_CQ, **PRIO_CQ;
```



<dl> <dt>

<span data-ttu-id="47e06-105">**RIO de \_ CQ**</span><span class="sxs-lookup"><span data-stu-id="47e06-105">**RIO\_CQ**</span></span>
</dt> <dd>

<span data-ttu-id="47e06-106">Um tipo de dados que especifica um descritor de fila de conclusão usado para notificação de conclusão de e/s por solicitações de envio e recebimento.</span><span class="sxs-lookup"><span data-stu-id="47e06-106">A data type that specifies a completion queue descriptor used for I/O completion notification by send and receive requests.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="47e06-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="47e06-107">Remarks</span></span>

<span data-ttu-id="47e06-108">O objeto **rio \_ CQ** é usado para a notificação de conclusão de e/s de envio e recebimento de solicitações de rede pelas extensões de e/s registradas pelo Winsock.</span><span class="sxs-lookup"><span data-stu-id="47e06-108">The **RIO\_CQ** object is used for I/O completion notification of send and receive networking requests by the Winsock registered I/O extensions.</span></span>

<span data-ttu-id="47e06-109">Um aplicativo pode usar a função [**RIONotify**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify) para solicitar notificação quando uma fila de preenchimento do **rio \_ CQ** não está vazia.</span><span class="sxs-lookup"><span data-stu-id="47e06-109">An application can use the [**RIONotify**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify) function to request notification when a **RIO\_CQ** completion queue is not empty.</span></span> <span data-ttu-id="47e06-110">Um aplicativo também pode sondar o status a qualquer momento de uma fila de conclusão **rio \_ CQ** em uma forma sem bloqueio usando a função [**RIODequeueCompletion**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion) .</span><span class="sxs-lookup"><span data-stu-id="47e06-110">An application can also poll the status at any time of a **RIO\_CQ** completion queue in a non-blocking way using the [**RIODequeueCompletion**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion) function.</span></span>

<span data-ttu-id="47e06-111">O objeto **Rio de \_ CQ** é criado usando a função [**RIOCreateCompletionQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion) .</span><span class="sxs-lookup"><span data-stu-id="47e06-111">The **RIO\_CQ** object is created using the [**RIOCreateCompletionQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion) function.</span></span> <span data-ttu-id="47e06-112">No momento da criação, o aplicativo deve especificar o tamanho da fila, o que determina quantas entradas de conclusão ela pode conter.</span><span class="sxs-lookup"><span data-stu-id="47e06-112">At creation time, the application must specify the size of the queue, which determines how many completion entries it can hold.</span></span> <span data-ttu-id="47e06-113">Quando um aplicativo chama a função [**RIOCreateRequestQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreaterequestqueue) para obter um identificador [**rio \_ RQ**](riorqueue.md) , o aplicativo deve especificar um identificador **Rio de \_ CQ** para as conclusões de envio e um identificador **rio \_ CQ** para as conclusões de recebimento.</span><span class="sxs-lookup"><span data-stu-id="47e06-113">When an application calls the [**RIOCreateRequestQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreaterequestqueue) function to obtain a [**RIO\_RQ**](riorqueue.md) handle, the application must specify a **RIO\_CQ** handle for send completions and a **RIO\_CQ** handle for receive completions.</span></span> <span data-ttu-id="47e06-114">Esses identificadores podem ser idênticos quando a mesma fila deve ser usada para a conclusão de envio e recebimento.</span><span class="sxs-lookup"><span data-stu-id="47e06-114">These handles may be identical when the same queue should be used for send and receive completion.</span></span> <span data-ttu-id="47e06-115">A função **RIOCreateRequestQueue** também requer um número máximo de operações pendentes de envio e recebimento, que são cobradas em relação à capacidade da fila ou filas de conclusão associadas.</span><span class="sxs-lookup"><span data-stu-id="47e06-115">The **RIOCreateRequestQueue** function also requires a maximum number of outstanding send and receive operations, which are charged against the capacity of the associated completion queue or queues.</span></span> <span data-ttu-id="47e06-116">Se as filas não tiverem capacidade suficiente restante, a chamada **RIOCreateRequestQueue** falhará com [WSAENOBUFS](windows-sockets-error-codes-2.md).</span><span class="sxs-lookup"><span data-stu-id="47e06-116">If the queues do not have sufficient capacity remaining, the **RIOCreateRequestQueue** call will fail with [WSAENOBUFS](windows-sockets-error-codes-2.md).</span></span>

<span data-ttu-id="47e06-117">O comportamento de notificação para uma fila de conclusão é definido quando o **Rio de \_ CQ** é criado.</span><span class="sxs-lookup"><span data-stu-id="47e06-117">The notification behavior for a completion queue is set when the **RIO\_CQ** is created.</span></span>

<span data-ttu-id="47e06-118">Para uma fila de conclusão que usa um evento, o **tipo** membro da estrutura de [**\_ \_ conclusão de notificação do Rio**](/windows/desktop/api/Mswsock/ns-mswsock-rio_notification_completion) é definido como **\_ \_ conclusão do evento Rio**.</span><span class="sxs-lookup"><span data-stu-id="47e06-118">For a completion queue that uses an event, the **Type** member of the [**RIO\_NOTIFICATION\_COMPLETION**](/windows/desktop/api/Mswsock/ns-mswsock-rio_notification_completion) structure is set to **RIO\_EVENT\_COMPLETION**.</span></span> <span data-ttu-id="47e06-119">O membro **Event. EventHandle** deve conter o identificador de um evento criado pela função [**WSACreateEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacreateevent) ou [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) .</span><span class="sxs-lookup"><span data-stu-id="47e06-119">The **Event.EventHandle** member should contain the handle for an event created by the [**WSACreateEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacreateevent) or [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) function.</span></span> <span data-ttu-id="47e06-120">Para receber a conclusão de [**RIONotify**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify) , o aplicativo deve aguardar o identificador de evento especificado usando [**WSAWaitForMultipleEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) ou uma rotina de espera semelhante.</span><span class="sxs-lookup"><span data-stu-id="47e06-120">To receive the [**RIONotify**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify) completion, the application should wait on the specified event handle using [**WSAWaitForMultipleEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) or a similar wait routine.</span></span> <span data-ttu-id="47e06-121">Se o aplicativo planeja redefinir e reutilizar o evento, o aplicativo pode reduzir a sobrecarga definindo o membro **Event. NotifyReset** com um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="47e06-121">If the application plans to reset and reuse the event, the application can reduce overhead by setting the **Event.NotifyReset** member to a non-zero value.</span></span> <span data-ttu-id="47e06-122">Isso faz com que o evento seja redefinido automaticamente pela função **RIONotify** quando a notificação ocorre.</span><span class="sxs-lookup"><span data-stu-id="47e06-122">This causes the event to be automatically reset by the **RIONotify** function when the notification occurs.</span></span> <span data-ttu-id="47e06-123">Isso reduz a necessidade de chamar a função [**WSAResetEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsaresetevent) para redefinir o evento entre chamadas para a função **RIONotify** .</span><span class="sxs-lookup"><span data-stu-id="47e06-123">This mitigates the need to call the [**WSAResetEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsaresetevent) function to reset the event between calls to the **RIONotify** function.</span></span>

<span data-ttu-id="47e06-124">Para uma fila de conclusão que usa uma porta de conclusão de e/s, o membro de **tipo** da estrutura de [**\_ \_ conclusão de notificação Rio**](/windows/desktop/api/Mswsock/ns-mswsock-rio_notification_completion) é definido como a **\_ \_ conclusão Rio IOCP**.</span><span class="sxs-lookup"><span data-stu-id="47e06-124">For a completion queue that uses an I/O completion port, the **Type** member of the [**RIO\_NOTIFICATION\_COMPLETION**](/windows/desktop/api/Mswsock/ns-mswsock-rio_notification_completion) structure is set to **RIO\_IOCP\_COMPLETION**.</span></span> <span data-ttu-id="47e06-125">O membro **IOCP. IocpHandle** deve conter o identificador para uma porta de conclusão de e/s criada pela função [**CreateIoCompletionPort**](/windows/win32/api/ioapiset/nf-ioapiset-createiocompletionport) .</span><span class="sxs-lookup"><span data-stu-id="47e06-125">The **Iocp.IocpHandle** member should contain the handle for an I/O completion port created by the [**CreateIoCompletionPort**](/windows/win32/api/ioapiset/nf-ioapiset-createiocompletionport) function.</span></span> <span data-ttu-id="47e06-126">Para receber a conclusão de [**RIONotify**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify) , o aplicativo deve chamar a função [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) ou [**GetQueuedCompletionStatusEx**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatusex) .</span><span class="sxs-lookup"><span data-stu-id="47e06-126">To receive the [**RIONotify**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify) completion, the application should call the [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) or [**GetQueuedCompletionStatusEx**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatusex) function.</span></span> <span data-ttu-id="47e06-127">O aplicativo deve fornecer um objeto [**sobreposto**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) dedicado para a fila de conclusão e também pode usar o membro **IOCP. CompletionKey** para distinguir solicitações **RIONotify** na fila de conclusão de outras conclusões de e/s, incluindo preenchimentos **RIONotify** para outras filas de conclusão.</span><span class="sxs-lookup"><span data-stu-id="47e06-127">The application should provide a dedicated [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) object for the completion queue, and it may also use the **Iocp.CompletionKey** member to distinguish **RIONotify** requests on the completion queue from other I/O completions including **RIONotify** completions for other completion queues.</span></span>

> [!Note]  
> <span data-ttu-id="47e06-128">Para fins de eficiência, o acesso às filas de conclusão (as estruturas do **rio \_ CQ** ) e as filas de solicitação (do [**rio \_ RQ**](riorqueue.md) ) não são protegidos por primitivos de sincronização.</span><span class="sxs-lookup"><span data-stu-id="47e06-128">For purposes of efficiency, access to the completion queues (**RIO\_CQ** structs) and request queues ([**RIO\_RQ**](riorqueue.md) structs) are not protected by synchronization primitives.</span></span> <span data-ttu-id="47e06-129">Se você precisar acessar uma fila de conclusão ou de solicitação de vários threads, o acesso deve ser coordenado por uma seção crítica, bloqueio de gravação de leitor fino ou mecanismo semelhante.</span><span class="sxs-lookup"><span data-stu-id="47e06-129">If you need to access a completion or request queue from multiple threads, access should be coordinated by a critical section, slim reader write lock or similar mechanism.</span></span> <span data-ttu-id="47e06-130">Esse bloqueio não é necessário para o acesso por um único thread.</span><span class="sxs-lookup"><span data-stu-id="47e06-130">This locking is not needed for access by a single thread.</span></span> <span data-ttu-id="47e06-131">Threads diferentes podem acessar filas de solicitações/conclusão separadas sem bloqueios.</span><span class="sxs-lookup"><span data-stu-id="47e06-131">Different threads can access separate requests/completion queues without locks.</span></span> <span data-ttu-id="47e06-132">A necessidade de sincronização ocorre somente quando vários threads tentam acessar a mesma fila.</span><span class="sxs-lookup"><span data-stu-id="47e06-132">The need for synchronization occurs only when multiple threads try to access the same queue.</span></span> <span data-ttu-id="47e06-133">A sincronização também será necessária se vários threads emitirem o envio e receberem no mesmo soquete, pois as operações de envio e recebimento usam a fila de solicitações do soquete.</span><span class="sxs-lookup"><span data-stu-id="47e06-133">Synchronization is also required if multiple threads issue sends and receives on the same socket because the send and receive operations use the socket’s request queue.</span></span>

 

<span data-ttu-id="47e06-134">Se vários threads tentarem acessar o mesmo **Rio de \_ CQ** usando [**RIODequeueCompletion**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion), o acesso deverá ser coordenado por uma seção crítica, bloqueio de gravador de leitor fino ou mecanismo de exclusão mútua semelhante.</span><span class="sxs-lookup"><span data-stu-id="47e06-134">If multiple threads attempt to access the same **RIO\_CQ** using [**RIODequeueCompletion**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion), access must be coordinated by a critical section, slim reader writer lock , or similar mutual exclusion mechanism.</span></span> <span data-ttu-id="47e06-135">Se as filas de conclusão não forem compartilhadas, a exclusão mútua não será necessária.</span><span class="sxs-lookup"><span data-stu-id="47e06-135">If the completion queues are not shared, mutual exclusion is not required.</span></span>

<span data-ttu-id="47e06-136">Quando uma fila de conclusão não for mais necessária, um aplicativo poderá fechá-la usando a função [**RIOCloseCompletionQueue**](/previous-versions/windows/desktop/legacy/hh448837(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="47e06-136">When a completion queue is no longer needed, an application can close it using the [**RIOCloseCompletionQueue**](/previous-versions/windows/desktop/legacy/hh448837(v=vs.85)) function.</span></span>

<span data-ttu-id="47e06-137">O **typedef \_ CQ do Rio** é definido no arquivo de cabeçalho *Mswsockdef. h* que é incluído automaticamente no arquivo de cabeçalho *mswsock. h* .</span><span class="sxs-lookup"><span data-stu-id="47e06-137">The **RIO\_CQ** typedef is defined in the *Mswsockdef.h* header file which is automatically included in the *Mswsock.h* header file.</span></span> <span data-ttu-id="47e06-138">O arquivo de cabeçalho *Mswsockdef. h* nunca deve ser usado diretamente.</span><span class="sxs-lookup"><span data-stu-id="47e06-138">The *Mswsockdef.h* header file should never be used directly.</span></span>

## <a name="thread-safety"></a><span data-ttu-id="47e06-139">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="47e06-139">Thread Safety</span></span>

<span data-ttu-id="47e06-140">Se vários threads tentarem acessar o mesmo **Rio de \_ CQ** usando [**RIODequeueCompletion**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion), o acesso deverá ser coordenado por uma seção crítica, bloqueio de gravador de leitor fino ou mecanismo de exclusão mútua semelhante.</span><span class="sxs-lookup"><span data-stu-id="47e06-140">If multiple threads attempt to access the same **RIO\_CQ** using [**RIODequeueCompletion**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion), access must be coordinated by a critical section, slim reader writer lock , or similar mutual exclusion mechanism.</span></span> <span data-ttu-id="47e06-141">Se as filas de conclusão não forem compartilhadas, a exclusão mútua não será necessária.</span><span class="sxs-lookup"><span data-stu-id="47e06-141">If the completion queues are not shared, mutual exclusion is not required.</span></span>

## <a name="requirements"></a><span data-ttu-id="47e06-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="47e06-142">Requirements</span></span>



| <span data-ttu-id="47e06-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="47e06-143">Requirement</span></span> | <span data-ttu-id="47e06-144">Valor</span><span class="sxs-lookup"><span data-stu-id="47e06-144">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47e06-145">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="47e06-145">Minimum supported client</span></span><br/> | <span data-ttu-id="47e06-146">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="47e06-146">Windows 8 \[desktop apps only\]</span></span><br/>                                                                  |
| <span data-ttu-id="47e06-147">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="47e06-147">Minimum supported server</span></span><br/> | <span data-ttu-id="47e06-148">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="47e06-148">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="47e06-149">parâmetro</span><span class="sxs-lookup"><span data-stu-id="47e06-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="47e06-150"><dt>Mswsockdef. h (incluir mswsock. h)</dt></span><span class="sxs-lookup"><span data-stu-id="47e06-150"><dt>Mswsockdef.h (include Mswsock.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47e06-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="47e06-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47e06-152">**CreateIoCompletionPort**</span><span class="sxs-lookup"><span data-stu-id="47e06-152">**CreateIoCompletionPort**</span></span>](/windows/win32/api/ioapiset/nf-ioapiset-createiocompletionport)
</dt> <dt>

[<span data-ttu-id="47e06-153">**CreateEvent**</span><span class="sxs-lookup"><span data-stu-id="47e06-153">**CreateEvent**</span></span>](/windows/win32/api/synchapi/nf-synchapi-createeventa)
</dt> <dt>

[<span data-ttu-id="47e06-154">**GetQueuedCompletionStatus**</span><span class="sxs-lookup"><span data-stu-id="47e06-154">**GetQueuedCompletionStatus**</span></span>](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)
</dt> <dt>

[<span data-ttu-id="47e06-155">**GetQueuedCompletionStatusEx**</span><span class="sxs-lookup"><span data-stu-id="47e06-155">**GetQueuedCompletionStatusEx**</span></span>](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatusex)
</dt> <dt>

[<span data-ttu-id="47e06-156">**SOBREPÕE**</span><span class="sxs-lookup"><span data-stu-id="47e06-156">**OVERLAPPED**</span></span>](/windows/win32/api/minwinbase/ns-minwinbase-overlapped)
</dt> <dt>

[<span data-ttu-id="47e06-157">**\_conclusão da notificação do Rio \_**</span><span class="sxs-lookup"><span data-stu-id="47e06-157">**RIO\_NOTIFICATION\_COMPLETION**</span></span>](/windows/desktop/api/Mswsock/ns-mswsock-rio_notification_completion)
</dt> <dt>

[<span data-ttu-id="47e06-158">**\_tipo de \_ conclusão de notificação rio \_**</span><span class="sxs-lookup"><span data-stu-id="47e06-158">**RIO\_NOTIFICATION\_COMPLETION\_TYPE**</span></span>](/windows/desktop/api/Mswsock/ne-mswsock-rio_notification_completion_type)
</dt> <dt>

[<span data-ttu-id="47e06-159">**RIO de \_ RQ**</span><span class="sxs-lookup"><span data-stu-id="47e06-159">**RIO\_RQ**</span></span>](riorqueue.md)
</dt> <dt>

<span data-ttu-id="47e06-160">[**RIOCloseCompletionQueue**](/previous-versions/windows/desktop/legacy/hh448837(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="47e06-160">[**RIOCloseCompletionQueue**](/previous-versions/windows/desktop/legacy/hh448837(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="47e06-161">**RIOCreateCompletionQueue**</span><span class="sxs-lookup"><span data-stu-id="47e06-161">**RIOCreateCompletionQueue**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion)
</dt> <dt>

[<span data-ttu-id="47e06-162">**RIOCreateRequestQueue**</span><span class="sxs-lookup"><span data-stu-id="47e06-162">**RIOCreateRequestQueue**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreaterequestqueue)
</dt> <dt>

[<span data-ttu-id="47e06-163">**RIODequeueCompletion**</span><span class="sxs-lookup"><span data-stu-id="47e06-163">**RIODequeueCompletion**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion)
</dt> <dt>

[<span data-ttu-id="47e06-164">**RIONotify**</span><span class="sxs-lookup"><span data-stu-id="47e06-164">**RIONotify**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify)
</dt> <dt>

[<span data-ttu-id="47e06-165">**WSACreateEvent**</span><span class="sxs-lookup"><span data-stu-id="47e06-165">**WSACreateEvent**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsacreateevent)
</dt> <dt>

[<span data-ttu-id="47e06-166">**WSAResetEvent**</span><span class="sxs-lookup"><span data-stu-id="47e06-166">**WSAResetEvent**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsaresetevent)
</dt> <dt>

[<span data-ttu-id="47e06-167">**WSAWaitForMultipleEvents**</span><span class="sxs-lookup"><span data-stu-id="47e06-167">**WSAWaitForMultipleEvents**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents)
</dt> </dl>

 

 
