---
title: Movimentação de processo
description: Um instantâneo que inclui a lista de processos contém informações sobre cada processo em execução no momento.
ms.assetid: 4fb55763-2206-48ad-8b1f-ed2c33b6f56b
keywords:
- enumerando
- Enumerando, processos
- processos
- processos, enumerando processos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbc95f0de4021ce3c355286376decbdecef2c883
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454173"
---
# <a name="process-walking"></a><span data-ttu-id="2c360-107">Movimentação de processo</span><span class="sxs-lookup"><span data-stu-id="2c360-107">Process Walking</span></span>

<span data-ttu-id="2c360-108">Um instantâneo que inclui a lista de processos contém informações sobre cada processo em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="2c360-108">A snapshot that includes the process list contains information about each currently executing process.</span></span> <span data-ttu-id="2c360-109">Você pode recuperar informações para o primeiro processo na lista usando a função [**Process32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32first) .</span><span class="sxs-lookup"><span data-stu-id="2c360-109">You can retrieve information for the first process in the list by using the [**Process32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32first) function.</span></span> <span data-ttu-id="2c360-110">Depois de recuperar o primeiro processo na lista, você pode atravessar a lista de processos para entradas subsequentes usando a função [**Process32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32next) .</span><span class="sxs-lookup"><span data-stu-id="2c360-110">After retrieving the first process in the list, you can traverse the process list for subsequent entries by using the [**Process32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32next) function.</span></span> <span data-ttu-id="2c360-111">**Process32First** e **Process32Next** preenchem uma estrutura [**PROCESSENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-processentry32) com informações sobre um processo no instantâneo.</span><span class="sxs-lookup"><span data-stu-id="2c360-111">**Process32First** and **Process32Next** fill a [**PROCESSENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-processentry32) structure with information about a process in the snapshot.</span></span> <span data-ttu-id="2c360-112">Para obter um exemplo, consulte [fazendo um instantâneo e exibindo processos](taking-a-snapshot-and-viewing-processes.md).</span><span class="sxs-lookup"><span data-stu-id="2c360-112">For an example, see [Taking a Snapshot and Viewing Processes](taking-a-snapshot-and-viewing-processes.md).</span></span>

<span data-ttu-id="2c360-113">Você pode recuperar um código de status de erro estendido para [**Process32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32first) e [**Process32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32next) usando a função [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .</span><span class="sxs-lookup"><span data-stu-id="2c360-113">You can retrieve an extended error status code for [**Process32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32first) and [**Process32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32next) by using the [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span>

<span data-ttu-id="2c360-114">Você pode ler a memória em um processo específico em um buffer usando a função [**Toolhelp32ReadProcessMemory**](/windows/desktop/api/TlHelp32/nf-tlhelp32-toolhelp32readprocessmemory) (ou a função [**VirtualQueryEx**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualqueryex) ).</span><span class="sxs-lookup"><span data-stu-id="2c360-114">You can read the memory in a specific process into a buffer by using the [**Toolhelp32ReadProcessMemory**](/windows/desktop/api/TlHelp32/nf-tlhelp32-toolhelp32readprocessmemory) function (or the [**VirtualQueryEx**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualqueryex) function).</span></span>

> [!Note]  
> <span data-ttu-id="2c360-115">O conteúdo dos membros **th32ProcessID** e **th32ParentProcessID** de [**PROCESSENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-processentry32) são identificadores de processo e pode ser usado por qualquer função que exija um identificador de processo.</span><span class="sxs-lookup"><span data-stu-id="2c360-115">The contents of the **th32ProcessID** and **th32ParentProcessID** members of [**PROCESSENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-processentry32) are process identifiers and can be used by any functions that require a process identifier.</span></span>

 

 

 