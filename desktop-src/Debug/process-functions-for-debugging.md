---
description: A função CreateProcess permite que um depurador inicie um processo e depure-o.
ms.assetid: 7056e181-9bc5-4530-a7b8-d5ff1e345eef
title: Processar funções para depuração
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d31378a4115acfdd5a4a1836199b7387adeb6e3f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920281"
---
# <a name="process-functions-for-debugging"></a><span data-ttu-id="86f6a-103">Processar funções para depuração</span><span class="sxs-lookup"><span data-stu-id="86f6a-103">Process Functions for Debugging</span></span>

<span data-ttu-id="86f6a-104">A função [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) permite que um depurador inicie um processo e depure-o.</span><span class="sxs-lookup"><span data-stu-id="86f6a-104">The [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) function enables a debugger to start a process and debug it.</span></span> <span data-ttu-id="86f6a-105">O parâmetro *fdwCreate* de **CreateProcess** é usado para especificar o tipo de operação de depuração.</span><span class="sxs-lookup"><span data-stu-id="86f6a-105">The *fdwCreate* parameter of **CreateProcess** is used to specify the type of debugging operation.</span></span> <span data-ttu-id="86f6a-106">Se o sinalizador de processo de depuração \_ for especificado para o parâmetro, um depurador depurará o novo processo e todos os descendentes do processo, desde que os descendentes sejam criados sem o sinalizador de processo de depuração \_ .</span><span class="sxs-lookup"><span data-stu-id="86f6a-106">If the DEBUG\_PROCESS flag is specified for the parameter, a debugger debugs the new process and all of the process's descendants, provided that the descendants are created without the DEBUG\_PROCESS flag.</span></span>

<span data-ttu-id="86f6a-107">Se o processo de depuração \_ e a depuração \_ somente desses sinalizadores de \_ \_ processo forem especificados para *fdwCreate*, um depurador depurará o novo processo, mas nenhum de seus descendentes.</span><span class="sxs-lookup"><span data-stu-id="86f6a-107">If the DEBUG\_PROCESS and DEBUG\_ONLY\_THIS\_PROCESS flags are specified for *fdwCreate*, a debugger debugs the new process but none of its descendants.</span></span>

<span data-ttu-id="86f6a-108">Um depurador pode depurar outro criando um processo com o \_ sinalizador processo de depuração.</span><span class="sxs-lookup"><span data-stu-id="86f6a-108">One debugger can debug another by creating a process with the DEBUG\_PROCESS flag.</span></span> <span data-ttu-id="86f6a-109">O novo processo (o depurador que está sendo depurado) deve criar um processo com o \_ sinalizador de processo de depuração.</span><span class="sxs-lookup"><span data-stu-id="86f6a-109">The new process (the debugger being debugged) must then create a process with the DEBUG\_PROCESS flag.</span></span>

<span data-ttu-id="86f6a-110">A função [**OpenProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocess) permite que um depurador obtenha o identificador de um processo existente.</span><span class="sxs-lookup"><span data-stu-id="86f6a-110">The [**OpenProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocess) function enables a debugger to obtain the identifier of an existing process.</span></span> <span data-ttu-id="86f6a-111">(A função [**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess) usa esse identificador para anexar o depurador ao processo.) Normalmente, os depuradores abrem um processo com os sinalizadores de gravação da VM do processo de \_ \_ leitura e processamento da VM \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="86f6a-111">(The [**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess) function uses this identifier to attach the debugger to the process.) Typically, debuggers open a process with the PROCESS\_VM\_READ and PROCESS\_VM\_WRITE flags.</span></span> <span data-ttu-id="86f6a-112">O uso desses sinalizadores permite que o depurador Leia e grave na memória virtual do processo usando as funções [**ReadProcessMemory**](/windows/win32/api/memoryapi/nf-memoryapi-readprocessmemory) e [**WriteProcessMemory**](/windows/win32/api/memoryapi/nf-memoryapi-writeprocessmemory) .</span><span class="sxs-lookup"><span data-stu-id="86f6a-112">Using these flags enables the debugger to read from and write to the virtual memory of the process by using the [**ReadProcessMemory**](/windows/win32/api/memoryapi/nf-memoryapi-readprocessmemory) and [**WriteProcessMemory**](/windows/win32/api/memoryapi/nf-memoryapi-writeprocessmemory) functions.</span></span> <span data-ttu-id="86f6a-113">Para obter mais informações, consulte [**processos e threads**](../procthread/processes-and-threads.md).</span><span class="sxs-lookup"><span data-stu-id="86f6a-113">For more information, see [**Processes and Threads**](../procthread/processes-and-threads.md).</span></span>

 

 
