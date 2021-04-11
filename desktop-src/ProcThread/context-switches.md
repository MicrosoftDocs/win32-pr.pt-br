---
description: O Agendador mantém uma fila de threads executáveis para cada nível de prioridade.
ms.assetid: 82463d71-9cef-4608-b997-25dc9c1e1c0a
title: Opções de Contexto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7628ee9e659cdbc2369b5f69d25847e8864dbd62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169507"
---
# <a name="context-switches"></a><span data-ttu-id="64f04-103">Opções de Contexto</span><span class="sxs-lookup"><span data-stu-id="64f04-103">Context Switches</span></span>

<span data-ttu-id="64f04-104">O Agendador mantém uma fila de threads executáveis para cada nível de prioridade.</span><span class="sxs-lookup"><span data-stu-id="64f04-104">The scheduler maintains a queue of executable threads for each priority level.</span></span> <span data-ttu-id="64f04-105">Eles são conhecidos como *threads prontos*.</span><span class="sxs-lookup"><span data-stu-id="64f04-105">These are known as *ready threads*.</span></span> <span data-ttu-id="64f04-106">Quando um processador fica disponível, o sistema executa uma *alternância de contexto*.</span><span class="sxs-lookup"><span data-stu-id="64f04-106">When a processor becomes available, the system performs a *context switch*.</span></span> <span data-ttu-id="64f04-107">As etapas em uma alternância de contexto são:</span><span class="sxs-lookup"><span data-stu-id="64f04-107">The steps in a context switch are:</span></span>

1.  <span data-ttu-id="64f04-108">Salve o contexto do thread que acabou de ser executado.</span><span class="sxs-lookup"><span data-stu-id="64f04-108">Save the context of the thread that just finished executing.</span></span>
2.  <span data-ttu-id="64f04-109">Coloque o thread que acabou de ser executado no final da fila para sua prioridade.</span><span class="sxs-lookup"><span data-stu-id="64f04-109">Place the thread that just finished executing at the end of the queue for its priority.</span></span>
3.  <span data-ttu-id="64f04-110">Localize a fila de prioridade mais alta que contém threads prontos.</span><span class="sxs-lookup"><span data-stu-id="64f04-110">Find the highest priority queue that contains ready threads.</span></span>
4.  <span data-ttu-id="64f04-111">Remova o thread no cabeçalho da fila, carregue seu contexto e execute-o.</span><span class="sxs-lookup"><span data-stu-id="64f04-111">Remove the thread at the head of the queue, load its context, and execute it.</span></span>

<span data-ttu-id="64f04-112">As classes de threads a seguir não são threads prontos.</span><span class="sxs-lookup"><span data-stu-id="64f04-112">The following classes of threads are not ready threads.</span></span>

-   <span data-ttu-id="64f04-113">Threads criados com o \_ sinalizador criar suspenso</span><span class="sxs-lookup"><span data-stu-id="64f04-113">Threads created with the CREATE\_SUSPENDED flag</span></span>
-   <span data-ttu-id="64f04-114">Threads interrompidos durante a execução com a função [**SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread) ou [**SwitchToThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-switchtothread)</span><span class="sxs-lookup"><span data-stu-id="64f04-114">Threads halted during execution with the [**SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread) or [**SwitchToThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-switchtothread) function</span></span>
-   <span data-ttu-id="64f04-115">Threads aguardando um objeto de sincronização ou entrada.</span><span class="sxs-lookup"><span data-stu-id="64f04-115">Threads waiting for a synchronization object or input.</span></span>

<span data-ttu-id="64f04-116">Até que os threads que estão suspensos ou bloqueados se tornem prontos para serem executados, o Agendador não aloca nenhum tempo de processador a eles, independentemente de sua prioridade.</span><span class="sxs-lookup"><span data-stu-id="64f04-116">Until threads that are suspended or blocked become ready to run, the scheduler does not allocate any processor time to them, regardless of their priority.</span></span>

<span data-ttu-id="64f04-117">Os motivos mais comuns para uma alternância de contexto são:</span><span class="sxs-lookup"><span data-stu-id="64f04-117">The most common reasons for a context switch are:</span></span>

-   <span data-ttu-id="64f04-118">A fração de tempo esgotou.</span><span class="sxs-lookup"><span data-stu-id="64f04-118">The time slice has elapsed.</span></span>
-   <span data-ttu-id="64f04-119">Um thread com prioridade mais alta se tornou pronto para ser executado.</span><span class="sxs-lookup"><span data-stu-id="64f04-119">A thread with a higher priority has become ready to run.</span></span>
-   <span data-ttu-id="64f04-120">Um thread em execução precisa aguardar.</span><span class="sxs-lookup"><span data-stu-id="64f04-120">A running thread needs to wait.</span></span>

<span data-ttu-id="64f04-121">Quando um thread em execução precisa esperar, ele abandona o restante de sua fatia de tempo.</span><span class="sxs-lookup"><span data-stu-id="64f04-121">When a running thread needs to wait, it relinquishes the remainder of its time slice.</span></span>

 

 
