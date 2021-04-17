---
description: Implemente multitarefas, prioridades de agendamento e trabalhe com processos, threads, pools de threads, objetos de trabalho e fibras. Use o agendamento do modo de usuário para agendar threads.
ms.assetid: 6bff848c-0c55-41e7-aff1-84c6b21a1b8d
title: Processos e threads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f469806a5f803910a773c78c9847d0f7b0ecc7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759607"
---
# <a name="processes-and-threads"></a><span data-ttu-id="dc609-104">Processos e threads</span><span class="sxs-lookup"><span data-stu-id="dc609-104">Processes and Threads</span></span>

<span data-ttu-id="dc609-105">Um aplicativo consiste em um ou mais processos.</span><span class="sxs-lookup"><span data-stu-id="dc609-105">An application consists of one or more processes.</span></span> <span data-ttu-id="dc609-106">Um *processo*, nos termos mais simples, é um programa em execução.</span><span class="sxs-lookup"><span data-stu-id="dc609-106">A *process*, in the simplest terms, is an executing program.</span></span> <span data-ttu-id="dc609-107">Um ou mais threads são executados no contexto do processo.</span><span class="sxs-lookup"><span data-stu-id="dc609-107">One or more threads run in the context of the process.</span></span> <span data-ttu-id="dc609-108">Um *thread* é a unidade básica para a qual o sistema operacional aloca o tempo do processador.</span><span class="sxs-lookup"><span data-stu-id="dc609-108">A *thread* is the basic unit to which the operating system allocates processor time.</span></span> <span data-ttu-id="dc609-109">Um thread pode executar qualquer parte do código do processo, incluindo partes que estão sendo executadas atualmente por outro thread.</span><span class="sxs-lookup"><span data-stu-id="dc609-109">A thread can execute any part of the process code, including parts currently being executed by another thread.</span></span>

<span data-ttu-id="dc609-110">Um *objeto de trabalho* permite que grupos de processos sejam gerenciados como uma unidade.</span><span class="sxs-lookup"><span data-stu-id="dc609-110">A *job object* allows groups of processes to be managed as a unit.</span></span> <span data-ttu-id="dc609-111">Os objetos de trabalho são objetos namable, protegíveis e compartilháveis que controlam os atributos dos processos associados a eles.</span><span class="sxs-lookup"><span data-stu-id="dc609-111">Job objects are namable, securable, sharable objects that control attributes of the processes associated with them.</span></span> <span data-ttu-id="dc609-112">As operações executadas no objeto de trabalho afetam todos os processos associados ao objeto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="dc609-112">Operations performed on the job object affect all processes associated with the job object.</span></span>

<span data-ttu-id="dc609-113">Um *pool de threads* é uma coleção de threads de trabalho que executam com eficiência retornos de chamada assíncronos em nome do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="dc609-113">A *thread pool* is a collection of worker threads that efficiently execute asynchronous callbacks on behalf of the application.</span></span> <span data-ttu-id="dc609-114">O pool de threads é usado principalmente para reduzir o número de threads do aplicativo e fornecer gerenciamento dos threads de trabalho.</span><span class="sxs-lookup"><span data-stu-id="dc609-114">The thread pool is primarily used to reduce the number of application threads and provide management of the worker threads.</span></span>

<span data-ttu-id="dc609-115">Uma *fibra* é uma unidade de execução que deve ser agendada manualmente pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="dc609-115">A *fiber* is a unit of execution that must be manually scheduled by the application.</span></span> <span data-ttu-id="dc609-116">Os fibras são executados no contexto dos threads que os agendam.</span><span class="sxs-lookup"><span data-stu-id="dc609-116">Fibers run in the context of the threads that schedule them.</span></span>

<span data-ttu-id="dc609-117">O ums ( *agendamento de modo de usuário* ) é um mecanismo leve que os aplicativos podem usar para agendar seus próprios threads.</span><span class="sxs-lookup"><span data-stu-id="dc609-117">*User-mode scheduling* (UMS) is a lightweight mechanism that applications can use to schedule their own threads.</span></span> <span data-ttu-id="dc609-118">Threads UMS diferem de [fibras](fibers.md) em que cada thread UMS tem seu próprio contexto de thread em vez de compartilhar o contexto de thread de um único thread.</span><span class="sxs-lookup"><span data-stu-id="dc609-118">UMS threads differ from [fibers](fibers.md) in that each UMS thread has its own thread context instead of sharing the thread context of a single thread.</span></span>

-   [<span data-ttu-id="dc609-119">O que há de novo em processos e threads</span><span class="sxs-lookup"><span data-stu-id="dc609-119">What's New in Processes and Threads</span></span>](what-s-new-in-processes-and-threads.md)
-   [<span data-ttu-id="dc609-120">Sobre Processos e Threads</span><span class="sxs-lookup"><span data-stu-id="dc609-120">About Processes and Threads</span></span>](about-processes-and-threads.md)
-   [<span data-ttu-id="dc609-121">Usando processos e threads</span><span class="sxs-lookup"><span data-stu-id="dc609-121">Using Processes and Threads</span></span>](using-processes-and-threads.md)
-   [<span data-ttu-id="dc609-122">Processo e referência de thread</span><span class="sxs-lookup"><span data-stu-id="dc609-122">Process and Thread Reference</span></span>](process-and-thread-reference.md)

 

 



