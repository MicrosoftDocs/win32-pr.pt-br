---
description: Um sistema operacional multitarefa divide o tempo de processador disponível entre os processos ou threads que precisam dele.
ms.assetid: ac45bef6-f078-40ac-95f4-06bd61ff46c4
title: Multitarefa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d06c1d8d44f397f06923c793971bcb20f35b2b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296742"
---
# <a name="multitasking"></a><span data-ttu-id="fb5f6-103">Multitarefa</span><span class="sxs-lookup"><span data-stu-id="fb5f6-103">Multitasking</span></span>

<span data-ttu-id="fb5f6-104">Um sistema operacional multitarefa divide o tempo de processador disponível entre os processos ou threads que precisam dele.</span><span class="sxs-lookup"><span data-stu-id="fb5f6-104">A multitasking operating system divides the available processor time among the processes or threads that need it.</span></span> <span data-ttu-id="fb5f6-105">O sistema foi projetado para a Preemptive multitarefas; Ele aloca uma *fatia de tempo* de processador para cada thread que executa.</span><span class="sxs-lookup"><span data-stu-id="fb5f6-105">The system is designed for preemptive multitasking; it allocates a processor *time slice* to each thread it executes.</span></span> <span data-ttu-id="fb5f6-106">O thread atualmente em execução é suspenso quando sua fração de tempo expira, permitindo que outro thread seja executado.</span><span class="sxs-lookup"><span data-stu-id="fb5f6-106">The currently executing thread is suspended when its time slice elapses, allowing another thread to run.</span></span> <span data-ttu-id="fb5f6-107">Quando o sistema alterna de um thread para outro, ele salva o contexto do thread admitido e restaura o contexto salvo do próximo thread na fila.</span><span class="sxs-lookup"><span data-stu-id="fb5f6-107">When the system switches from one thread to another, it saves the context of the preempted thread and restores the saved context of the next thread in the queue.</span></span>

<span data-ttu-id="fb5f6-108">A duração da fração de tempo depende do sistema operacional e do processador.</span><span class="sxs-lookup"><span data-stu-id="fb5f6-108">The length of the time slice depends on the operating system and the processor.</span></span> <span data-ttu-id="fb5f6-109">Como cada fração de tempo é pequena (aproximadamente 20 milissegundos), vários threads parecem estar sendo executados ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="fb5f6-109">Because each time slice is small (approximately 20 milliseconds), multiple threads appear to be executing at the same time.</span></span> <span data-ttu-id="fb5f6-110">É esse o caso em sistemas de multiprocessador, em que os threads executáveis são distribuídos entre os processadores disponíveis.</span><span class="sxs-lookup"><span data-stu-id="fb5f6-110">This is actually the case on multiprocessor systems, where the executable threads are distributed among the available processors.</span></span> <span data-ttu-id="fb5f6-111">No entanto, é preciso ter cuidado ao usar vários threads em um aplicativo, pois o desempenho do sistema pode diminuir se houver muitos threads.</span><span class="sxs-lookup"><span data-stu-id="fb5f6-111">However, you must use caution when using multiple threads in an application, because system performance can decrease if there are too many threads.</span></span>

<span data-ttu-id="fb5f6-112">Para mais informações, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="fb5f6-112">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="fb5f6-113">Vantagens da multitarefa</span><span class="sxs-lookup"><span data-stu-id="fb5f6-113">Advantages of Multitasking</span></span>](advantages-of-multitasking.md)
-   [<span data-ttu-id="fb5f6-114">Quando usar multitarefa</span><span class="sxs-lookup"><span data-stu-id="fb5f6-114">When to Use Multitasking</span></span>](when-to-use-multitasking.md)
-   [<span data-ttu-id="fb5f6-115">Considerações sobre multitarefas</span><span class="sxs-lookup"><span data-stu-id="fb5f6-115">Multitasking Considerations</span></span>](multitasking-considerations.md)

 

 



