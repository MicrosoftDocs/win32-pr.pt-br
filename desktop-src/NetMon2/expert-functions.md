---
description: As funções auxiliares a seguir só podem ser chamadas por especialistas que exportam a função executar ou configurar.
ms.assetid: 6890087c-7c94-41ff-bb5c-4bf88a4e07cc
title: Funções de especialista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7441289008c7dcd647775c2932e210ccd09b24bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826843"
---
# <a name="expert-functions"></a><span data-ttu-id="1a6a4-103">Funções de especialista</span><span class="sxs-lookup"><span data-stu-id="1a6a4-103">Expert Functions</span></span>

<span data-ttu-id="1a6a4-104">As funções auxiliares a seguir só podem ser chamadas por especialistas que exportam a função [executar](run.md) ou [Configurar](configure.md) .</span><span class="sxs-lookup"><span data-stu-id="1a6a4-104">The following helper functions can only be called by experts that export the [Run](run.md) or [Configure](configure.md) function.</span></span>



| <span data-ttu-id="1a6a4-105">Função</span><span class="sxs-lookup"><span data-stu-id="1a6a4-105">Function</span></span>                                         | <span data-ttu-id="1a6a4-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="1a6a4-106">Description</span></span>                                                                             |
|--------------------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="1a6a4-107">ExpertGetFrame</span><span class="sxs-lookup"><span data-stu-id="1a6a4-107">ExpertGetFrame</span></span>](expertgetframe.md)             | <span data-ttu-id="1a6a4-108">Recupera um determinado quadro da captura.</span><span class="sxs-lookup"><span data-stu-id="1a6a4-108">Retrieves a given frame from the capture.</span></span>                                               |
| [<span data-ttu-id="1a6a4-109">ExpertIndicateStatus</span><span class="sxs-lookup"><span data-stu-id="1a6a4-109">ExpertIndicateStatus</span></span>](expertindicatestatus.md) | <span data-ttu-id="1a6a4-110">Indica a porcentagem de conclusão da análise de captura do especialista.</span><span class="sxs-lookup"><span data-stu-id="1a6a4-110">Indicates the percentage of completion of the expert's analysis of capture.</span></span>             |
| [<span data-ttu-id="1a6a4-111">ExpertGetStartupInfo</span><span class="sxs-lookup"><span data-stu-id="1a6a4-111">ExpertGetStartupInfo</span></span>](expertgetstartupinfo.md) | <span data-ttu-id="1a6a4-112">Recupera as informações de inicialização para o especialista.</span><span class="sxs-lookup"><span data-stu-id="1a6a4-112">Retrieves the startup information for the expert.</span></span>                                       |
| [<span data-ttu-id="1a6a4-113">ExpertMemorySize</span><span class="sxs-lookup"><span data-stu-id="1a6a4-113">ExpertMemorySize</span></span>](expertmemorysize.md)         | <span data-ttu-id="1a6a4-114">Recupera o tamanho da memória alocada por uma chamada para a função **ExpertAllocMemory** .</span><span class="sxs-lookup"><span data-stu-id="1a6a4-114">Retrieves the size of memory allocated by a call to the **ExpertAllocMemory** function.</span></span> |
| [<span data-ttu-id="1a6a4-115">ExpertSubmitEvent</span><span class="sxs-lookup"><span data-stu-id="1a6a4-115">ExpertSubmitEvent</span></span>](expertsubmitevent.md)       | <span data-ttu-id="1a6a4-116">Indica um problema e recupera informações sobre o problema, se houver.</span><span class="sxs-lookup"><span data-stu-id="1a6a4-116">Indicates a problem and retrieves information about the problem if one exists.</span></span>          |
| [<span data-ttu-id="1a6a4-117">ExpertAllocMemory</span><span class="sxs-lookup"><span data-stu-id="1a6a4-117">ExpertAllocMemory</span></span>](expertallocmemory.md)       | <span data-ttu-id="1a6a4-118">Aloca memória para o especialista.</span><span class="sxs-lookup"><span data-stu-id="1a6a4-118">Allocates memory for the expert.</span></span>                                                        |
| [<span data-ttu-id="1a6a4-119">ExpertReallocMemory</span><span class="sxs-lookup"><span data-stu-id="1a6a4-119">ExpertReallocMemory</span></span>](expertreallocmemory.md)   | <span data-ttu-id="1a6a4-120">Altera o tamanho da memória alocada pela função **ExpertAllocMemory** .</span><span class="sxs-lookup"><span data-stu-id="1a6a4-120">Changes the size of the memory allocated by the **ExpertAllocMemory** function.</span></span>         |
| [<span data-ttu-id="1a6a4-121">ExpertFreeMemory</span><span class="sxs-lookup"><span data-stu-id="1a6a4-121">ExpertFreeMemory</span></span>](expertfreememory.md)         | <span data-ttu-id="1a6a4-122">Libera memória alocada pelo especialista.</span><span class="sxs-lookup"><span data-stu-id="1a6a4-122">Frees memory allocated by the expert.</span></span>                                                   |



 

<span data-ttu-id="1a6a4-123">Para obter informações sobre funções de exportação, funções auxiliares que podem ser chamadas por especialistas e analisadores, estruturas e enumerações, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="1a6a4-123">For information about export functions, helper functions that can be called by experts and parsers, structures, and enumerations, see the following topics:</span></span>



| <span data-ttu-id="1a6a4-124">Para obter informações sobre</span><span class="sxs-lookup"><span data-stu-id="1a6a4-124">For information about</span></span>                                             | <span data-ttu-id="1a6a4-125">Consulte</span><span class="sxs-lookup"><span data-stu-id="1a6a4-125">See</span></span>                                                                          |
|-------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="1a6a4-126">Funções exportadas por especialistas</span><span class="sxs-lookup"><span data-stu-id="1a6a4-126">Functions that are exported by experts</span></span>                            | [<span data-ttu-id="1a6a4-127">Funções de exportação de DLL de especialista</span><span class="sxs-lookup"><span data-stu-id="1a6a4-127">Expert DLL Export Functions</span></span>](expert-dll-export-functions.md)               |
| <span data-ttu-id="1a6a4-128">Estruturas que são usadas por funções de especialista</span><span class="sxs-lookup"><span data-stu-id="1a6a4-128">Structures that are used by expert functions</span></span>                      | [<span data-ttu-id="1a6a4-129">Estruturas de especialistas</span><span class="sxs-lookup"><span data-stu-id="1a6a4-129">Expert Structures</span></span>](expert-structures.md)                                   |
| <span data-ttu-id="1a6a4-130">Enumerações usadas por estruturas e funções de especialistas</span><span class="sxs-lookup"><span data-stu-id="1a6a4-130">Enumerations used by expert structures and functions</span></span>              | [<span data-ttu-id="1a6a4-131">Enumerações de especialistas</span><span class="sxs-lookup"><span data-stu-id="1a6a4-131">Expert Enumerations</span></span>](expert-enumerations.md)                               |
| <span data-ttu-id="1a6a4-132">Funções auxiliares comuns que podem ser chamadas por especialistas e analisadores</span><span class="sxs-lookup"><span data-stu-id="1a6a4-132">Common helper functions that can be called by experts and parsers</span></span> | [<span data-ttu-id="1a6a4-133">Funções comuns de expert e parser</span><span class="sxs-lookup"><span data-stu-id="1a6a4-133">Expert and Parser Common Functions</span></span>](expert-and-parser-common-functions.md) |



 

 

 



