---
title: Memória. CPP
description: No componente do provedor de exemplo, um exemplo de código que mostra a alocação de memória e a liberação está na Memory. cpp. As rotinas com suporte são listadas na tabela a seguir.
ms.assetid: dc5b3559-02fc-45e8-bbd0-482e4e3a7f8a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9add77dcdbbfc0ddab547cd537b352c9a68bdaf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105756490"
---
# <a name="memorycpp"></a><span data-ttu-id="61e57-104">Memória. CPP</span><span class="sxs-lookup"><span data-stu-id="61e57-104">MEMORY.CPP</span></span>

<span data-ttu-id="61e57-105">No componente do provedor de exemplo, um exemplo de código que mostra a alocação de memória e a liberação está na Memory. cpp.</span><span class="sxs-lookup"><span data-stu-id="61e57-105">In the example provider component, a code example showing memory allocation and freeing is in memory.cpp.</span></span> <span data-ttu-id="61e57-106">As rotinas com suporte são listadas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="61e57-106">Supported routines are listed in the following table.</span></span>



| <span data-ttu-id="61e57-107">Item</span><span class="sxs-lookup"><span data-stu-id="61e57-107">Item</span></span>                | <span data-ttu-id="61e57-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="61e57-108">Description</span></span>                                                           |
|---------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="61e57-109">**AllocProvMem**</span><span class="sxs-lookup"><span data-stu-id="61e57-109">**AllocProvMem**</span></span>    | <span data-ttu-id="61e57-110">Alocar memória especificada.</span><span class="sxs-lookup"><span data-stu-id="61e57-110">Allocate specified memory.</span></span>                                            |
| <span data-ttu-id="61e57-111">**FreeProvMem**</span><span class="sxs-lookup"><span data-stu-id="61e57-111">**FreeProvMem**</span></span>     | <span data-ttu-id="61e57-112">Memória livre indicada.</span><span class="sxs-lookup"><span data-stu-id="61e57-112">Free memory indicated.</span></span>                                                |
| <span data-ttu-id="61e57-113">**ReallocProvMem**</span><span class="sxs-lookup"><span data-stu-id="61e57-113">**ReallocProvMem**</span></span>  | <span data-ttu-id="61e57-114">Aloque memória contígua.</span><span class="sxs-lookup"><span data-stu-id="61e57-114">Allocate contiguous memory.</span></span>                                           |
| <span data-ttu-id="61e57-115">**AllocProvStr**</span><span class="sxs-lookup"><span data-stu-id="61e57-115">**AllocProvStr**</span></span>    | <span data-ttu-id="61e57-116">Aloque uma cadeia de caracteres LPWSTR.</span><span class="sxs-lookup"><span data-stu-id="61e57-116">Allocate an LPWSTR string.</span></span>                                            |
| <span data-ttu-id="61e57-117">**FreeProvStr**</span><span class="sxs-lookup"><span data-stu-id="61e57-117">**FreeProvStr**</span></span>     | <span data-ttu-id="61e57-118">Cadeia de caracteres gratuita se ainda não tiver sido liberada.</span><span class="sxs-lookup"><span data-stu-id="61e57-118">Free string if not already freed.</span></span>                                     |
| <span data-ttu-id="61e57-119">**ReallocProvStr**</span><span class="sxs-lookup"><span data-stu-id="61e57-119">**ReallocProvStr**</span></span>  | <span data-ttu-id="61e57-120">Aloque memória contígua.</span><span class="sxs-lookup"><span data-stu-id="61e57-120">Allocate contiguous memory.</span></span>                                           |
| <span data-ttu-id="61e57-121">**ProvAllocString**</span><span class="sxs-lookup"><span data-stu-id="61e57-121">**ProvAllocString**</span></span> | <span data-ttu-id="61e57-122">Verifica a cadeia de caracteres e o primeiro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="61e57-122">Verifies string and first parameter.</span></span> <span data-ttu-id="61e57-123">Se OK, executará a alocação.</span><span class="sxs-lookup"><span data-stu-id="61e57-123">If OK, then performs allocation.</span></span> |



 

 

 




