---
description: E/s de alerta é o método pelo qual os threads de aplicativo processam solicitações de e/s assíncronas somente quando estão em um estado de alerta.
ms.assetid: d996f1cc-eeab-456b-818b-5307a79effd9
title: E/s alertável
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fb830dfadb97051c47b2472eb3e7a3c2d6a0bd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105768767"
---
# <a name="alertable-io"></a><span data-ttu-id="00183-103">E/s alertável</span><span class="sxs-lookup"><span data-stu-id="00183-103">Alertable I/O</span></span>

<span data-ttu-id="00183-104">E/s de alerta é o método pelo qual os threads de aplicativo processam solicitações de e/s assíncronas somente quando estão em um estado de alerta.</span><span class="sxs-lookup"><span data-stu-id="00183-104">Alertable I/O is the method by which application threads process asynchronous I/O requests only when they are in an alertable state.</span></span>

<span data-ttu-id="00183-105">Para entender quando um thread está em um estado de alerta, considere o seguinte cenário:</span><span class="sxs-lookup"><span data-stu-id="00183-105">To understand when a thread is in an alertable state, consider the following scenario:</span></span>

1.  <span data-ttu-id="00183-106">Um thread inicia uma solicitação de leitura assíncrona chamando [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) com um ponteiro para uma função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="00183-106">A thread initiates an asynchronous read request by calling [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) with a pointer to a callback function.</span></span>
2.  <span data-ttu-id="00183-107">O thread inicia uma solicitação de gravação assíncrona chamando [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) com um ponteiro para uma função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="00183-107">The thread initiates an asynchronous write request by calling [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) with a pointer to a callback function.</span></span>
3.  <span data-ttu-id="00183-108">O thread chama uma função que busca uma linha de dados de um servidor de banco de dado remoto.</span><span class="sxs-lookup"><span data-stu-id="00183-108">The thread calls a function that fetches a row of data from a remote database server.</span></span>

<span data-ttu-id="00183-109">Nesse cenário, as chamadas para [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) e [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) provavelmente serão retornadas antes da chamada de função na etapa 3.</span><span class="sxs-lookup"><span data-stu-id="00183-109">In this scenario, the calls to [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) and [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) will most likely return before the function call in step 3.</span></span> <span data-ttu-id="00183-110">Quando isso ocorre, o kernel coloca os ponteiros para as funções de retorno de chamada na fila da APC (assíncrona de procedimento assíncrono) do thread.</span><span class="sxs-lookup"><span data-stu-id="00183-110">When they do, the kernel places the pointers to the callback functions on the thread's Asynchronous Procedure Call (APC) queue.</span></span> <span data-ttu-id="00183-111">O kernel mantém essa fila especificamente para manter os dados de solicitação de e/s retornados até que possa ser processado pelo thread correspondente.</span><span class="sxs-lookup"><span data-stu-id="00183-111">The kernel maintains this queue specifically to hold returned I/O request data until it can be processed by the corresponding thread.</span></span>

<span data-ttu-id="00183-112">Quando a busca de linha é concluída e o thread retorna da função, sua prioridade mais alta é processar as solicitações de e/s retornadas na fila chamando as funções de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="00183-112">When the row fetch is complete and the thread returns from the function, its highest priority is to process the returned I/O requests on the queue by calling the callback functions.</span></span> <span data-ttu-id="00183-113">Para fazer isso, ele deve inserir um estado de alerta.</span><span class="sxs-lookup"><span data-stu-id="00183-113">To do this, it must enter an alertable state.</span></span> <span data-ttu-id="00183-114">Um thread só pode fazer isso chamando uma das seguintes funções com os sinalizadores apropriados:</span><span class="sxs-lookup"><span data-stu-id="00183-114">A thread can only do this by calling one of the following functions with the appropriate flags:</span></span>

-   [<span data-ttu-id="00183-115">**SleepEx**</span><span class="sxs-lookup"><span data-stu-id="00183-115">**SleepEx**</span></span>](/windows/desktop/api/synchapi/nf-synchapi-sleepex)
-   [<span data-ttu-id="00183-116">**WaitForSingleObjectEx**</span><span class="sxs-lookup"><span data-stu-id="00183-116">**WaitForSingleObjectEx**</span></span>](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex)
-   [<span data-ttu-id="00183-117">**WaitForMultipleObjectsEx**</span><span class="sxs-lookup"><span data-stu-id="00183-117">**WaitForMultipleObjectsEx**</span></span>](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjectsex)
-   [<span data-ttu-id="00183-118">**SignalObjectAndWait**</span><span class="sxs-lookup"><span data-stu-id="00183-118">**SignalObjectAndWait**</span></span>](/windows/win32/api/synchapi/nf-synchapi-signalobjectandwait)
-   [<span data-ttu-id="00183-119">**MsgWaitForMultipleObjectsEx**</span><span class="sxs-lookup"><span data-stu-id="00183-119">**MsgWaitForMultipleObjectsEx**</span></span>](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjectsex)

<span data-ttu-id="00183-120">Quando o thread entra em um estado alertado, ocorrem os seguintes eventos:</span><span class="sxs-lookup"><span data-stu-id="00183-120">When the thread enters an alertable state, the following events occur:</span></span>

1.  <span data-ttu-id="00183-121">O kernel verifica a fila da APC do thread.</span><span class="sxs-lookup"><span data-stu-id="00183-121">The kernel checks the thread's APC queue.</span></span> <span data-ttu-id="00183-122">Se a fila contiver ponteiros de função de retorno de chamada, o kernel removerá o ponteiro da fila e o enviará para o thread.</span><span class="sxs-lookup"><span data-stu-id="00183-122">If the queue contains callback function pointers, the kernel removes the pointer from the queue and sends it to the thread.</span></span>
2.  <span data-ttu-id="00183-123">O thread executa a função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="00183-123">The thread executes the callback function.</span></span>
3.  <span data-ttu-id="00183-124">As etapas 1 e 2 são repetidas para cada ponteiro restante na fila.</span><span class="sxs-lookup"><span data-stu-id="00183-124">Steps 1 and 2 are repeated for each pointer remaining in the queue.</span></span>
4.  <span data-ttu-id="00183-125">Quando a fila está vazia, o thread retorna da função que a colocou em um estado de alerta.</span><span class="sxs-lookup"><span data-stu-id="00183-125">When the queue is empty, the thread returns from the function that placed it in an alertable state.</span></span>

<span data-ttu-id="00183-126">Nesse cenário, depois que o thread entrar em um estado de alerta, ele chamará as funções de retorno de chamada enviadas para [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) e [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex), em seguida, retornará da função que a colocou em um estado de alerta.</span><span class="sxs-lookup"><span data-stu-id="00183-126">In this scenario, once the thread enters an alertable state it will call the callback functions sent to [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) and [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex), then return from the function that placed it in an alertable state.</span></span>

<span data-ttu-id="00183-127">Se um thread entrar em um estado alertado enquanto sua fila da APC estiver vazia, a execução do thread será suspensa pelo kernel até que ocorra um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="00183-127">If a thread enters an alertable state while its APC queue is empty, the thread's execution will be suspended by the kernel until one of the following occurs:</span></span>

-   <span data-ttu-id="00183-128">O objeto de kernel que está sendo aguardado é sinalizado.</span><span class="sxs-lookup"><span data-stu-id="00183-128">The kernel object that is being waited on becomes signaled.</span></span>
-   <span data-ttu-id="00183-129">Um ponteiro de função de retorno de chamada é colocado na fila da APC.</span><span class="sxs-lookup"><span data-stu-id="00183-129">A callback function pointer is placed in the APC queue.</span></span>

<span data-ttu-id="00183-130">Um thread que usa e/s alerta solicitações de e/s assíncronas com mais eficiência do que quando simplesmente aguarda o sinalizador de evento na estrutura [**sobreposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) ser definido, e o mecanismo de e/s alertado é menos complicado do que [as portas de conclusão de e/s](i-o-completion-ports.md) a serem usadas.</span><span class="sxs-lookup"><span data-stu-id="00183-130">A thread that uses alertable I/O processes asynchronous I/O requests more efficiently than when they simply wait on the event flag in the [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure to be set, and the alertable I/O mechanism is less complicated than [I/O completion ports](i-o-completion-ports.md) to use.</span></span> <span data-ttu-id="00183-131">No entanto, a e/s alertável retorna o resultado da solicitação de e/s somente para o thread que a iniciou.</span><span class="sxs-lookup"><span data-stu-id="00183-131">However, alertable I/O returns the result of the I/O request only to the thread that initiated it.</span></span> <span data-ttu-id="00183-132">As portas de conclusão de e/s não têm essa limitação.</span><span class="sxs-lookup"><span data-stu-id="00183-132">I/O completion ports do not have this limitation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="00183-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="00183-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00183-134">Chamadas de procedimento assíncrono</span><span class="sxs-lookup"><span data-stu-id="00183-134">Asynchronous Procedure Calls</span></span>](/windows/desktop/Sync/asynchronous-procedure-calls)
</dt> </dl>

 

 
