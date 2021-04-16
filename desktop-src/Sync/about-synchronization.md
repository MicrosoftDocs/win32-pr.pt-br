---
description: Para sincronizar o acesso a um recurso, use um dos objetos de sincronização em uma das funções de espera.
ms.assetid: 0930bf12-6d5f-4f2c-914d-53e6e862d3bd
title: Sobre a sincronização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ad53dc8c309d8ec55f37cef5f78839348071477
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105750421"
---
# <a name="about-synchronization"></a><span data-ttu-id="12cfd-103">Sobre a sincronização</span><span class="sxs-lookup"><span data-stu-id="12cfd-103">About Synchronization</span></span>

<span data-ttu-id="12cfd-104">Para sincronizar o acesso a um recurso, use um dos [objetos de sincronização](synchronization-objects.md) em uma das [funções de espera](wait-functions.md).</span><span class="sxs-lookup"><span data-stu-id="12cfd-104">To synchronize access to a resource, use one of the [synchronization objects](synchronization-objects.md) in one of the [wait functions](wait-functions.md).</span></span> <span data-ttu-id="12cfd-105">O estado de um objeto de sincronização é *sinalizado* ou não *sinalizado*.</span><span class="sxs-lookup"><span data-stu-id="12cfd-105">The state of a synchronization object is either *signaled* or *nonsignaled*.</span></span> <span data-ttu-id="12cfd-106">As funções Wait permitem que um thread bloqueie sua própria execução até que um objeto não sinalizado especificado seja definido como o estado sinalizado.</span><span class="sxs-lookup"><span data-stu-id="12cfd-106">The wait functions allow a thread to block its own execution until a specified nonsignaled object is set to the signaled state.</span></span> <span data-ttu-id="12cfd-107">Para obter mais informações, consulte [sincronização entre processos](interprocess-synchronization.md).</span><span class="sxs-lookup"><span data-stu-id="12cfd-107">For more information, see [Interprocess Synchronization](interprocess-synchronization.md).</span></span>

<span data-ttu-id="12cfd-108">Veja a seguir outros mecanismos de sincronização:</span><span class="sxs-lookup"><span data-stu-id="12cfd-108">The following are other synchronization mechanisms:</span></span>

-   [<span data-ttu-id="12cfd-109">entrada e saída sobrepostas</span><span class="sxs-lookup"><span data-stu-id="12cfd-109">overlapped input and output</span></span>](synchronization-and-overlapped-input-and-output.md)
-   [<span data-ttu-id="12cfd-110">chamadas de procedimento assíncrono</span><span class="sxs-lookup"><span data-stu-id="12cfd-110">asynchronous procedure calls</span></span>](asynchronous-procedure-calls.md)
-   [<span data-ttu-id="12cfd-111">objetos de seção crítica</span><span class="sxs-lookup"><span data-stu-id="12cfd-111">critical section objects</span></span>](critical-section-objects.md)
-   [<span data-ttu-id="12cfd-112">variáveis de condição</span><span class="sxs-lookup"><span data-stu-id="12cfd-112">condition variables</span></span>](condition-variables.md)
-   [<span data-ttu-id="12cfd-113">bloqueios de leitor/gravador reduzidos</span><span class="sxs-lookup"><span data-stu-id="12cfd-113">slim reader/writer locks</span></span>](slim-reader-writer--srw--locks.md)
-   [<span data-ttu-id="12cfd-114">inicialização única</span><span class="sxs-lookup"><span data-stu-id="12cfd-114">one-time initialization</span></span>](one-time-initialization.md)
-   [<span data-ttu-id="12cfd-115">acesso de variável interbloqueada</span><span class="sxs-lookup"><span data-stu-id="12cfd-115">interlocked variable access</span></span>](interlocked-variable-access.md)
-   [<span data-ttu-id="12cfd-116">listas vinculadas isoladamente interbloqueadas</span><span class="sxs-lookup"><span data-stu-id="12cfd-116">interlocked singly linked lists</span></span>](interlocked-singly-linked-lists.md)
-   [<span data-ttu-id="12cfd-117">filas de timer</span><span class="sxs-lookup"><span data-stu-id="12cfd-117">timer queues</span></span>](timer-queues.md)
-   <span data-ttu-id="12cfd-118">a macro [**MemoryBarrier**](/windows/win32/api/winnt/nf-winnt-memorybarrier)</span><span class="sxs-lookup"><span data-stu-id="12cfd-118">the [**MemoryBarrier**](/windows/win32/api/winnt/nf-winnt-memorybarrier) macro</span></span>

<span data-ttu-id="12cfd-119">Para obter informações adicionais sobre sincronização, consulte [sincronização e problemas de multiprocessador](synchronization-and-multiprocessor-issues.md).</span><span class="sxs-lookup"><span data-stu-id="12cfd-119">For additional information on synchronization, see [Synchronization and Multiprocessor Issues](synchronization-and-multiprocessor-issues.md).</span></span>

 

 
