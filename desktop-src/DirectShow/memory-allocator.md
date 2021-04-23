---
description: Alocador de memória
ms.assetid: 2dc055a2-b77a-443d-b602-d9636cbe4db3
title: Alocador de memória
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e2412adb78be18ac8c14eb4706624424f97ff13
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909414"
---
# <a name="memory-allocator"></a><span data-ttu-id="37532-103">Alocador de memória</span><span class="sxs-lookup"><span data-stu-id="37532-103">Memory Allocator</span></span>

<span data-ttu-id="37532-104">O objeto alocador de memória aloca buffers para exemplos de mídia.</span><span class="sxs-lookup"><span data-stu-id="37532-104">The Memory Allocator object allocates buffers for media samples.</span></span> <span data-ttu-id="37532-105">Os filtros podem usar esse objeto para alocar buffers de memória compartilhada; no entanto, um filtro com requisitos especiais também pode implementar seu próprio objeto de alocador de memória.</span><span class="sxs-lookup"><span data-stu-id="37532-105">Filters can use this object to allocate shared memory buffers; however, a filter with special requirements can also implement its own memory allocator object.</span></span> <span data-ttu-id="37532-106">Crie esse objeto chamando **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="37532-106">Create this object by calling **CoCreateInstance**.</span></span>



| <span data-ttu-id="37532-107">Label</span><span class="sxs-lookup"><span data-stu-id="37532-107">Label</span></span> | <span data-ttu-id="37532-108">Valor</span><span class="sxs-lookup"><span data-stu-id="37532-108">Value</span></span> |
|------------------|----------------------------------------|
| <span data-ttu-id="37532-109">Identificador de classe</span><span class="sxs-lookup"><span data-stu-id="37532-109">Class Identifier</span></span> | <span data-ttu-id="37532-110">\_MEMORYALLOCATOR CLSID</span><span class="sxs-lookup"><span data-stu-id="37532-110">CLSID\_MemoryAllocator</span></span>                 |
| <span data-ttu-id="37532-111">Interfaces</span><span class="sxs-lookup"><span data-stu-id="37532-111">Interfaces</span></span>       | [<span data-ttu-id="37532-112">**IMemAllocator**</span><span class="sxs-lookup"><span data-stu-id="37532-112">**IMemAllocator**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imemallocator) |



 

## <a name="related-topics"></a><span data-ttu-id="37532-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="37532-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="37532-114">Objetos do DirectShow</span><span class="sxs-lookup"><span data-stu-id="37532-114">DirectShow Objects</span></span>](directshow-objects.md)
</dt> </dl>

 

 



