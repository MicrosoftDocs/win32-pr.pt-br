---
title: Funções de ajuda da ferramenta
description: Lista as funções da biblioteca de ajuda da ferramenta.
ms.assetid: 83732bd6-f4cf-409d-ad17-86503d408dc3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54f9d95598f9b48343ea9731e1a826fb147a73a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006023"
---
# <a name="tool-help-functions"></a><span data-ttu-id="398f5-103">Funções de ajuda da ferramenta</span><span class="sxs-lookup"><span data-stu-id="398f5-103">Tool Help Functions</span></span>

<span data-ttu-id="398f5-104">As funções a seguir fazem parte da biblioteca de ajuda da ferramenta.</span><span class="sxs-lookup"><span data-stu-id="398f5-104">The following functions are part of the tool help library.</span></span>



| <span data-ttu-id="398f5-105">Função</span><span class="sxs-lookup"><span data-stu-id="398f5-105">Function</span></span>                                                           | <span data-ttu-id="398f5-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="398f5-106">Description</span></span>                                                                                                      |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="398f5-107">**CreateToolhelp32Snapshot**</span><span class="sxs-lookup"><span data-stu-id="398f5-107">**CreateToolhelp32Snapshot**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot)       | <span data-ttu-id="398f5-108">Tira um instantâneo dos processos especificados, bem como os heaps, módulos e threads usados por esses processos.</span><span class="sxs-lookup"><span data-stu-id="398f5-108">Takes a snapshot of the specified processes, as well as the heaps, modules, and threads used by these processes.</span></span> |
| [<span data-ttu-id="398f5-109">**Heap32First**</span><span class="sxs-lookup"><span data-stu-id="398f5-109">**Heap32First**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first)                                 | <span data-ttu-id="398f5-110">Recupera informações sobre o primeiro bloco de um heap que foi alocado por um processo.</span><span class="sxs-lookup"><span data-stu-id="398f5-110">Retrieves information about the first block of a heap that has been allocated by a process.</span></span>                      |
| [<span data-ttu-id="398f5-111">**Heap32ListFirst**</span><span class="sxs-lookup"><span data-stu-id="398f5-111">**Heap32ListFirst**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listfirst)                         | <span data-ttu-id="398f5-112">Recupera informações sobre o primeiro heap que foi alocado por um processo especificado.</span><span class="sxs-lookup"><span data-stu-id="398f5-112">Retrieves information about the first heap that has been allocated by a specified process.</span></span>                       |
| [<span data-ttu-id="398f5-113">**Heap32ListNext**</span><span class="sxs-lookup"><span data-stu-id="398f5-113">**Heap32ListNext**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listnext)                           | <span data-ttu-id="398f5-114">Recupera informações sobre o próximo heap que foi alocado por um processo.</span><span class="sxs-lookup"><span data-stu-id="398f5-114">Retrieves information about the next heap that has been allocated by a process.</span></span>                                  |
| [<span data-ttu-id="398f5-115">**Heap32Next**</span><span class="sxs-lookup"><span data-stu-id="398f5-115">**Heap32Next**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next)                                   | <span data-ttu-id="398f5-116">Recupera informações sobre o próximo bloco de um heap que foi alocado por um processo.</span><span class="sxs-lookup"><span data-stu-id="398f5-116">Retrieves information about the next block of a heap that has been allocated by a process.</span></span>                       |
| [<span data-ttu-id="398f5-117">**Module32First**</span><span class="sxs-lookup"><span data-stu-id="398f5-117">**Module32First**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32first)                             | <span data-ttu-id="398f5-118">Recupera informações sobre o primeiro módulo associado a um processo.</span><span class="sxs-lookup"><span data-stu-id="398f5-118">Retrieves information about the first module associated with a process.</span></span>                                          |
| [<span data-ttu-id="398f5-119">**Module32Next**</span><span class="sxs-lookup"><span data-stu-id="398f5-119">**Module32Next**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32next)                               | <span data-ttu-id="398f5-120">Recupera informações sobre o próximo módulo associado a um processo ou thread.</span><span class="sxs-lookup"><span data-stu-id="398f5-120">Retrieves information about the next module associated with a process or thread.</span></span>                                 |
| [<span data-ttu-id="398f5-121">**Process32First**</span><span class="sxs-lookup"><span data-stu-id="398f5-121">**Process32First**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32first)                           | <span data-ttu-id="398f5-122">Recupera informações sobre o primeiro processo encontrado em um instantâneo do sistema.</span><span class="sxs-lookup"><span data-stu-id="398f5-122">Retrieves information about the first process encountered in a system snapshot.</span></span>                                  |
| [<span data-ttu-id="398f5-123">**Process32Next**</span><span class="sxs-lookup"><span data-stu-id="398f5-123">**Process32Next**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32next)                             | <span data-ttu-id="398f5-124">Recupera informações sobre o próximo processo registrado em um instantâneo do sistema.</span><span class="sxs-lookup"><span data-stu-id="398f5-124">Retrieves information about the next process recorded in a system snapshot.</span></span>                                      |
| [<span data-ttu-id="398f5-125">**Thread32First**</span><span class="sxs-lookup"><span data-stu-id="398f5-125">**Thread32First**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32first)                             | <span data-ttu-id="398f5-126">Recupera informações sobre o primeiro thread de qualquer processo encontrado em um instantâneo do sistema.</span><span class="sxs-lookup"><span data-stu-id="398f5-126">Retrieves information about the first thread of any process encountered in a system snapshot.</span></span>                    |
| [<span data-ttu-id="398f5-127">**Thread32Next**</span><span class="sxs-lookup"><span data-stu-id="398f5-127">**Thread32Next**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32next)                               | <span data-ttu-id="398f5-128">Recupera informações sobre o próximo thread de qualquer processo encontrado no instantâneo de memória do sistema.</span><span class="sxs-lookup"><span data-stu-id="398f5-128">Retrieves information about the next thread of any process encountered in the system memory snapshot.</span></span>            |
| [<span data-ttu-id="398f5-129">**Toolhelp32ReadProcessMemory**</span><span class="sxs-lookup"><span data-stu-id="398f5-129">**Toolhelp32ReadProcessMemory**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-toolhelp32readprocessmemory) | <span data-ttu-id="398f5-130">Copia a memória alocada para outro processo em um buffer fornecido pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="398f5-130">Copies memory allocated to another process into an application-supplied buffer.</span></span>                                  |



 

 

 




