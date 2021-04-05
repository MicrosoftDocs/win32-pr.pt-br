---
description: A WCT (Wait Chain Traversal) permite que os depuradores diagnostiquem travamentos e bloqueios do aplicativo.
ms.assetid: d266a663-b101-4936-9574-f6ce223419ae
title: Passagem de cadeia de espera
ms.topic: article
ms.date: 08/10/2020
ms.custom: contperf-fy21q1
ms.openlocfilehash: 842beb7d5470bc2b3e6e9c7c1150ff2aa1a4cf76
ms.sourcegitcommit: f374b50b37160b683da16b59ac9340282a8f50a5
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/04/2021
ms.locfileid: "103825453"
---
# <a name="wait-chain-traversal"></a><span data-ttu-id="4d398-103">Passagem de cadeia de espera</span><span class="sxs-lookup"><span data-stu-id="4d398-103">Wait Chain Traversal</span></span>

<span data-ttu-id="4d398-104">A WCT (Wait Chain Traversal) permite que os depuradores diagnostiquem travamentos e bloqueios do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4d398-104">Wait Chain Traversal (WCT) enables debuggers to diagnose application hangs and deadlocks.</span></span>

<span data-ttu-id="4d398-105">Uma *cadeia de espera* é uma sequência alternada de threads e objetos de sincronização em que cada thread aguarda o objeto a seguir.</span><span class="sxs-lookup"><span data-stu-id="4d398-105">A *wait chain* is an alternating sequence of threads and synchronization objects where each thread waits for the object that follows.</span></span> <span data-ttu-id="4d398-106">Cada objeto a seguir é, por sua vez, de Propriedade do thread subsequente na cadeia.</span><span class="sxs-lookup"><span data-stu-id="4d398-106">Each object that follows is, in turn, owned by the subsequent thread in the chain.</span></span>

<span data-ttu-id="4d398-107">Um thread aguarda um objeto de sincronização do momento em que o thread solicita o objeto até que o thread o tenha adquirido.</span><span class="sxs-lookup"><span data-stu-id="4d398-107">A thread waits for a synchronization object from the time the thread requests the object until the thread has acquired it.</span></span> <span data-ttu-id="4d398-108">Esse "bloqueio" pertence a um thread a partir do momento em que o thread o adquire, até que o thread o libere.</span><span class="sxs-lookup"><span data-stu-id="4d398-108">This "lock" is owned by a thread from the time the thread acquires it, until the thread releases it.</span></span> <span data-ttu-id="4d398-109">Em outras palavras, quando o thread 1 está aguardando um bloqueio pertencente ao thread 2, o thread 1 é "aguardando" para o thread 2.</span><span class="sxs-lookup"><span data-stu-id="4d398-109">In other words, when thread 1 is waiting for a lock that is owned by thread 2, thread 1 is "waiting" for thread 2.</span></span>

<span data-ttu-id="4d398-110">A WCT dá suporte aos seguintes primitivos de sincronização:</span><span class="sxs-lookup"><span data-stu-id="4d398-110">WCT supports the following synchronization primitives:</span></span>

- [<span data-ttu-id="4d398-111">Chamada de procedimento local avançada (ALPC)</span><span class="sxs-lookup"><span data-stu-id="4d398-111">Advanced Local Procedure Call (ALPC)</span></span>](../etw/alpc.md)
- [<span data-ttu-id="4d398-112">COM (Component Object Model)</span><span class="sxs-lookup"><span data-stu-id="4d398-112">Component Object Model (COM)</span></span>](../com/the-component-object-model.md)
- [<span data-ttu-id="4d398-113">Seções críticas</span><span class="sxs-lookup"><span data-stu-id="4d398-113">Critical sections</span></span>](../sync/critical-section-objects.md)
- [<span data-ttu-id="4d398-114">Mutexes</span><span class="sxs-lookup"><span data-stu-id="4d398-114">Mutexes</span></span>](../sync/mutex-objects.md)
- [<span data-ttu-id="4d398-115">SendMessage</span><span class="sxs-lookup"><span data-stu-id="4d398-115">SendMessage</span></span>](/windows/win32/api/winuser/nf-winuser-sendmessage)
- <span data-ttu-id="4d398-116">Operações de [espera](../sync/wait-functions.md) em [processos e threads](../procthread/processes-and-threads.md)</span><span class="sxs-lookup"><span data-stu-id="4d398-116">[Wait](../sync/wait-functions.md) operations on [processes and threads](../procthread/processes-and-threads.md)</span></span>

<span data-ttu-id="4d398-117">Para recuperar a cadeia de espera para um ou mais threads, crie uma sessão WCT usando as funções [OpenThreadWaitChainSession](/windows/desktop/api/Wct/nf-wct-openthreadwaitchainsession) e [GetThreadWaitChain](/windows/desktop/api/Wct/nf-wct-getthreadwaitchain) .</span><span class="sxs-lookup"><span data-stu-id="4d398-117">To retrieve the wait chain for one or more threads, create a WCT session using the [OpenThreadWaitChainSession](/windows/desktop/api/Wct/nf-wct-openthreadwaitchainsession) and [GetThreadWaitChain](/windows/desktop/api/Wct/nf-wct-getthreadwaitchain) functions.</span></span> <span data-ttu-id="4d398-118">As sessões WCT são representadas por um identificador do tipo **HWCT**.</span><span class="sxs-lookup"><span data-stu-id="4d398-118">WCT sessions are represented by a handle of type **HWCT**.</span></span>

## <a name="sessions-can-be-synchronous-or-asynchronous"></a><span data-ttu-id="4d398-119">As sessões podem ser síncronas ou assíncronas</span><span class="sxs-lookup"><span data-stu-id="4d398-119">Sessions can be synchronous or asynchronous</span></span>

<span data-ttu-id="4d398-120">As sessões síncronas não podem ser canceladas e bloqueiam o thread de chamada até que uma cadeia de espera tenha sido recuperada.</span><span class="sxs-lookup"><span data-stu-id="4d398-120">Synchronous sessions cannot be canceled, and block the calling thread, until a wait chain has been retrieved.</span></span>

<span data-ttu-id="4d398-121">As sessões assíncronas não bloqueiam o thread de chamada e podem ser canceladas pelo aplicativo usando a função [CloseThreadWaitChainSession](/windows/desktop/api/Wct/nf-wct-closethreadwaitchainsession) .</span><span class="sxs-lookup"><span data-stu-id="4d398-121">Asynchronous sessions do not block the calling thread, and can be canceled by the application using the [CloseThreadWaitChainSession](/windows/desktop/api/Wct/nf-wct-closethreadwaitchainsession) function.</span></span> <span data-ttu-id="4d398-122">Os resultados de operações assíncronas são disponibilizados por meio de uma função de retorno de chamada [WaitChainCallback](/windows/win32/api/wct/nc-wct-pwaitchaincallback) fornecida pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4d398-122">Results from asynchronous operations are made available through a [WaitChainCallback](/windows/win32/api/wct/nc-wct-pwaitchaincallback) callback function provided by the application.</span></span>

<span data-ttu-id="4d398-123">Para sessões assíncronas, o chamador pode especificar um ponteiro para uma estrutura de dados de contexto por meio de [GetThreadWaitChain](/windows/desktop/api/Wct/nf-wct-getthreadwaitchain) (esse mesmo ponteiro é passado para a função de retorno de chamada [WaitChainCallback](/windows/win32/api/wct/nc-wct-pwaitchaincallback) ).</span><span class="sxs-lookup"><span data-stu-id="4d398-123">For asynchronous sessions, the caller can specify a pointer to a context data structure through [GetThreadWaitChain](/windows/desktop/api/Wct/nf-wct-getthreadwaitchain) (this same pointer is passed to the [WaitChainCallback](/windows/win32/api/wct/nc-wct-pwaitchaincallback) callback function).</span></span>

<span data-ttu-id="4d398-124">A estrutura de dados de contexto é definida pelo usuário e opaca para a WCT.</span><span class="sxs-lookup"><span data-stu-id="4d398-124">The context data structure is user-defined and opaque to WCT.</span></span> <span data-ttu-id="4d398-125">Ele pode ser usado pelo aplicativo para comunicar o contexto entre uma consulta WCT e uma função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="4d398-125">It can be used by the application to communicate context between a WCT query and a callback function.</span></span> <span data-ttu-id="4d398-126">Normalmente, você passa um identificador de evento por essa estrutura e, quando o retorno de chamada é executado, esse evento é sinalizado e um thread de monitoramento é informado de que a consulta foi concluída.</span><span class="sxs-lookup"><span data-stu-id="4d398-126">Typically, you pass an event handle through this structure and, when the callback is executed, this event is signalled and a monitoring thread is informed that the query has been completed.</span></span>

<span data-ttu-id="4d398-127">Consulte [usando a WCT](using-wct.md) para obter um exemplo de percurso de cadeia de espera.</span><span class="sxs-lookup"><span data-stu-id="4d398-127">See [Using WCT](using-wct.md) for an example of wait chain traversal.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4d398-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4d398-128">Related topics</span></span>

<span data-ttu-id="4d398-129">[Usando WCT](using-wct.md), [referência WCT](wct-reference.md), [msdn Magazine 2007 julho-Bugslayer: espera de passagem de cadeia](/archive/msdn-magazine/2007/july/bugslayer-wait-chain-traversal)</span><span class="sxs-lookup"><span data-stu-id="4d398-129">[Using WCT](using-wct.md), [WCT Reference](wct-reference.md), [MSDN Magazine 2007 July - Bugslayer: Wait Chain Traversal](/archive/msdn-magazine/2007/july/bugslayer-wait-chain-traversal)</span></span>