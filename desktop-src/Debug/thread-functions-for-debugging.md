---
description: A função CreateThread cria um novo thread para um processo.
ms.assetid: df59eedd-45ec-4564-96a5-8cecb345cfcc
title: Funções de thread para depuração
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb5ab0865d5585656a5c22c24e2604032de8b888
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500955"
---
# <a name="thread-functions-for-debugging"></a><span data-ttu-id="6b452-103">Funções de thread para depuração</span><span class="sxs-lookup"><span data-stu-id="6b452-103">Thread Functions for Debugging</span></span>

<span data-ttu-id="6b452-104">A função [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) cria um novo thread para um processo.</span><span class="sxs-lookup"><span data-stu-id="6b452-104">The [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) function creates a new thread for a process.</span></span> <span data-ttu-id="6b452-105">Os depuradores normalmente precisam examinar ou alterar o conteúdo dos registros de um thread.</span><span class="sxs-lookup"><span data-stu-id="6b452-105">Debuggers typically need to examine or change the contents of a thread's registers.</span></span> <span data-ttu-id="6b452-106">Para fazer isso, um depurador deve obter um identificador para o thread usando a função [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) e especificando o acesso apropriado ao thread (contexto de obtenção de thread \_ \_ , \_ contexto de conjunto de threads \_ ou ambos).</span><span class="sxs-lookup"><span data-stu-id="6b452-106">To accomplish this, a debugger must obtain a handle to the thread by using the [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) function and specifying the appropriate access to the thread (THREAD\_GET\_CONTEXT, THREAD\_SET\_CONTEXT, or both).</span></span> <span data-ttu-id="6b452-107">A função [**OpenThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread) permite que um depurador obtenha o identificador de um thread existente.</span><span class="sxs-lookup"><span data-stu-id="6b452-107">The [**OpenThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread) function enables a debugger to obtain the identifier of an existing thread.</span></span>

<span data-ttu-id="6b452-108">Um processo com acesso apropriado a um thread pode examinar os registros do thread usando a função [**GetThreadContext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadcontext) e definir o conteúdo dos registros do thread usando a função [**SetThreadContext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadcontext) .</span><span class="sxs-lookup"><span data-stu-id="6b452-108">A process with appropriate access to a thread can examine the thread's registers by using the [**GetThreadContext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadcontext) function and set the contents of the thread's registers by using the [**SetThreadContext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadcontext) function.</span></span>

<span data-ttu-id="6b452-109">Um processo também pode obter \_ acesso de \_ retomada de thread de suspensão a um thread.</span><span class="sxs-lookup"><span data-stu-id="6b452-109">A process can also obtain THREAD\_SUSPEND\_RESUME access to a thread.</span></span> <span data-ttu-id="6b452-110">Esse tipo de acesso permite que um depurador controle a execução de um thread com as funções [**SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread) e [**ResumeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) .</span><span class="sxs-lookup"><span data-stu-id="6b452-110">This type of access enables a debugger to control a thread's execution with the [**SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread) and [**ResumeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) functions.</span></span> <span data-ttu-id="6b452-111">Para obter mais informações sobre threads, consulte [processos e threads](../procthread/processes-and-threads.md).</span><span class="sxs-lookup"><span data-stu-id="6b452-111">For more information about threads, see [Processes and Threads](../procthread/processes-and-threads.md).</span></span>

 

 
