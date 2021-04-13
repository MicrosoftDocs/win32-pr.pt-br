---
description: Alocador de memória
ms.assetid: 2dc055a2-b77a-443d-b602-d9636cbe4db3
title: Alocador de memória
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be12e25886eda968a00b10386a6eac3fd36e7279
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500588"
---
# <a name="memory-allocator"></a><span data-ttu-id="5e946-103">Alocador de memória</span><span class="sxs-lookup"><span data-stu-id="5e946-103">Memory Allocator</span></span>

<span data-ttu-id="5e946-104">O objeto alocador de memória aloca buffers para exemplos de mídia.</span><span class="sxs-lookup"><span data-stu-id="5e946-104">The Memory Allocator object allocates buffers for media samples.</span></span> <span data-ttu-id="5e946-105">Os filtros podem usar esse objeto para alocar buffers de memória compartilhada; no entanto, um filtro com requisitos especiais também pode implementar seu próprio objeto de alocador de memória.</span><span class="sxs-lookup"><span data-stu-id="5e946-105">Filters can use this object to allocate shared memory buffers; however, a filter with special requirements can also implement its own memory allocator object.</span></span> <span data-ttu-id="5e946-106">Crie esse objeto chamando **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="5e946-106">Create this object by calling **CoCreateInstance**.</span></span>



|                  |                                        |
|------------------|----------------------------------------|
| <span data-ttu-id="5e946-107">Identificador de classe</span><span class="sxs-lookup"><span data-stu-id="5e946-107">Class Identifier</span></span> | <span data-ttu-id="5e946-108">\_MEMORYALLOCATOR CLSID</span><span class="sxs-lookup"><span data-stu-id="5e946-108">CLSID\_MemoryAllocator</span></span>                 |
| <span data-ttu-id="5e946-109">Interfaces</span><span class="sxs-lookup"><span data-stu-id="5e946-109">Interfaces</span></span>       | [<span data-ttu-id="5e946-110">**IMemAllocator**</span><span class="sxs-lookup"><span data-stu-id="5e946-110">**IMemAllocator**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imemallocator) |



 

## <a name="related-topics"></a><span data-ttu-id="5e946-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5e946-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5e946-112">Objetos do DirectShow</span><span class="sxs-lookup"><span data-stu-id="5e946-112">DirectShow Objects</span></span>](directshow-objects.md)
</dt> </dl>

 

 



