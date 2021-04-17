---
title: Movimentação de thread
description: Um instantâneo que inclui a lista de threads contém informações sobre cada thread de cada processo em execução no momento.
ms.assetid: 2440b781-652d-4d73-b173-87504e7b49b5
keywords:
- enumerando
- Enumerando, threads
- threads
- threads, enumerando threads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32eff584aedaa3f6124cc358a4ee9d2a94962843
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105779874"
---
# <a name="thread-walking"></a><span data-ttu-id="4040f-107">Movimentação de thread</span><span class="sxs-lookup"><span data-stu-id="4040f-107">Thread Walking</span></span>

<span data-ttu-id="4040f-108">Um instantâneo que inclui a lista de threads contém informações sobre cada thread de cada processo em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="4040f-108">A snapshot that includes the thread list contains information about each thread of each currently executing process.</span></span> <span data-ttu-id="4040f-109">Você pode recuperar informações para o primeiro thread na lista usando a função [**Thread32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32first) .</span><span class="sxs-lookup"><span data-stu-id="4040f-109">You can retrieve information for the first thread in the list by using the [**Thread32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32first) function.</span></span> <span data-ttu-id="4040f-110">Depois de recuperar o primeiro thread na lista, você pode recuperar informações para threads subsequentes usando a função [**Thread32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32next) .</span><span class="sxs-lookup"><span data-stu-id="4040f-110">After retrieving the first thread in the list, you can retrieve information for subsequent threads by using the [**Thread32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32next) function.</span></span> <span data-ttu-id="4040f-111">**Thread32First** e **Thread32Next** preenchem uma estrutura [**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32) com informações sobre threads individuais no instantâneo.</span><span class="sxs-lookup"><span data-stu-id="4040f-111">**Thread32First** and **Thread32Next** fill a [**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32) structure with information about individual threads in the snapshot.</span></span>

<span data-ttu-id="4040f-112">Você pode enumerar os threads de um processo específico tirando um instantâneo que inclui os threads e, em seguida, atravessando a lista de threads, mantendo informações sobre os threads que têm o mesmo identificador de processo que o processo especificado.</span><span class="sxs-lookup"><span data-stu-id="4040f-112">You can enumerate the threads of a specific process by taking a snapshot that includes the threads and then by traversing the thread list, keeping information about the threads that have the same process identifier as the specified process.</span></span>

<span data-ttu-id="4040f-113">Você pode recuperar um código de status de erro estendido para [**Thread32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32first) e [**Thread32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32next) usando a função [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .</span><span class="sxs-lookup"><span data-stu-id="4040f-113">You can retrieve an extended error status code for [**Thread32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32first) and [**Thread32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32next) by using the [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span>

> [!Note]  
> <span data-ttu-id="4040f-114">O conteúdo do membro **th32ThreadID** de [**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32) é um identificador de thread e pode ser usado por qualquer função que exija um identificador de thread.</span><span class="sxs-lookup"><span data-stu-id="4040f-114">The contents of the **th32ThreadID** member of [**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32) is a thread identifier and can be used by any functions that require a thread identifier.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="4040f-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4040f-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4040f-116">Atravessando a lista de threads</span><span class="sxs-lookup"><span data-stu-id="4040f-116">Traversing the Thread List</span></span>](traversing-the-thread-list.md)
</dt> </dl>

 

 