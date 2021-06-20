---
description: Saiba como usar a função CreateThread para criar um novo thread para um processo. Normalmente, os depurador precisam examinar ou alterar o conteúdo dos registros de um thread.
ms.assetid: df59eedd-45ec-4564-96a5-8cecb345cfcc
title: Funções de thread para depuração
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff168d4840032a6199ef03e0cf2117c8ea87f4d6
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112403979"
---
# <a name="thread-functions-for-debugging"></a><span data-ttu-id="11255-104">Funções de thread para depuração</span><span class="sxs-lookup"><span data-stu-id="11255-104">Thread Functions for Debugging</span></span>

<span data-ttu-id="11255-105">A [**função CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) cria um novo thread para um processo.</span><span class="sxs-lookup"><span data-stu-id="11255-105">The [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) function creates a new thread for a process.</span></span> <span data-ttu-id="11255-106">Normalmente, os depurador precisam examinar ou alterar o conteúdo dos registros de um thread.</span><span class="sxs-lookup"><span data-stu-id="11255-106">Debuggers typically need to examine or change the contents of a thread's registers.</span></span> <span data-ttu-id="11255-107">Para fazer isso, um depurador deve obter um tratamento para o thread usando a função [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) e especificando o acesso apropriado ao thread (THREAD GET CONTEXT, THREAD SET CONTEXT ou \_ \_ \_ \_ ambos).</span><span class="sxs-lookup"><span data-stu-id="11255-107">To accomplish this, a debugger must obtain a handle to the thread by using the [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) function and specifying the appropriate access to the thread (THREAD\_GET\_CONTEXT, THREAD\_SET\_CONTEXT, or both).</span></span> <span data-ttu-id="11255-108">A [**função OpenThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread) permite que um depurador obtenha o identificador de um thread existente.</span><span class="sxs-lookup"><span data-stu-id="11255-108">The [**OpenThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread) function enables a debugger to obtain the identifier of an existing thread.</span></span>

<span data-ttu-id="11255-109">Um processo com acesso apropriado a um thread pode examinar os registros do thread usando a função [**GetThreadContext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadcontext) e definir o conteúdo dos registros do thread usando a [**função SetThreadContext.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadcontext)</span><span class="sxs-lookup"><span data-stu-id="11255-109">A process with appropriate access to a thread can examine the thread's registers by using the [**GetThreadContext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadcontext) function and set the contents of the thread's registers by using the [**SetThreadContext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadcontext) function.</span></span>

<span data-ttu-id="11255-110">Um processo também pode obter acesso THREAD \_ SUSPEND RESUME a um \_ thread.</span><span class="sxs-lookup"><span data-stu-id="11255-110">A process can also obtain THREAD\_SUSPEND\_RESUME access to a thread.</span></span> <span data-ttu-id="11255-111">Esse tipo de acesso permite que um depurador controle a execução de um thread com as funções [**SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread) e [**ResumeThread.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread)</span><span class="sxs-lookup"><span data-stu-id="11255-111">This type of access enables a debugger to control a thread's execution with the [**SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread) and [**ResumeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) functions.</span></span> <span data-ttu-id="11255-112">Para obter mais informações sobre threads, consulte [Processos e threads.](../procthread/processes-and-threads.md)</span><span class="sxs-lookup"><span data-stu-id="11255-112">For more information about threads, see [Processes and Threads](../procthread/processes-and-threads.md).</span></span>

 

 
