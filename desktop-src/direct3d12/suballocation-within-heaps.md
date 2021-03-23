---
title: Subalocação dentro de heaps
description: Heaps de recursos transferem dados da CPU para a GPU (carregamento) e da GPU para a CPU (leitura de volta).
ms.assetid: 7E319BCF-FF3F-43CB-9C48-A9DD2A043592
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 701e68e31e698bbf2c955a252bd46876f45d6b7c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104873"
---
# <a name="suballocation-within-heaps"></a><span data-ttu-id="77589-103">Subalocação dentro de heaps</span><span class="sxs-lookup"><span data-stu-id="77589-103">Suballocation Within Heaps</span></span>

<span data-ttu-id="77589-104">Heaps de recursos transferem dados da CPU para a GPU (carregamento) e da GPU para a CPU (leitura de volta).</span><span class="sxs-lookup"><span data-stu-id="77589-104">Resource heaps transfer data from the CPU to the GPU (upload), and from the GPU to the CPU (read back).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="77589-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="77589-105">In this section</span></span>



| <span data-ttu-id="77589-106">Tópico</span><span class="sxs-lookup"><span data-stu-id="77589-106">Topic</span></span>                                                                                       | <span data-ttu-id="77589-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="77589-107">Description</span></span>                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="77589-108">Alias de memória e herança de dados</span><span class="sxs-lookup"><span data-stu-id="77589-108">Memory Aliasing and Data Inheritance</span></span>](memory-aliasing-and-data-inheritance.md)<br/> | <span data-ttu-id="77589-109">O recurso colocado e reservado pode alias de memória física em um heap.</span><span class="sxs-lookup"><span data-stu-id="77589-109">Placed and reserved resource may alias physical memory within a heap.</span></span> <span data-ttu-id="77589-110">Os recursos inseridos permitem mais cenários de herança de dados do que os recursos reservados quando o heap tem o sinalizador compartilhado definido ou quando os recursos com alias têm layouts de memória totalmente definidos.</span><span class="sxs-lookup"><span data-stu-id="77589-110">Placed resources enable more data inheritance scenarios than reserved resources when the heap has the shared flag set or when the aliased resources have fully defined memory layouts.</span></span> <br/> |
| [<span data-ttu-id="77589-111">Heaps compartilhados</span><span class="sxs-lookup"><span data-stu-id="77589-111">Shared Heaps</span></span>](shared-heaps.md)<br/>                                                 | <span data-ttu-id="77589-112">O compartilhamento é útil para arquiteturas de vários processos e multiadaptadores.</span><span class="sxs-lookup"><span data-stu-id="77589-112">Sharing is useful for multi-process and multi-adapter architectures.</span></span><br/>                                                                                                                                                                                          |



 

## <a name="related-topics"></a><span data-ttu-id="77589-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="77589-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77589-114">**ID3D12Device:: createheap**</span><span class="sxs-lookup"><span data-stu-id="77589-114">**ID3D12Device::CreateHeap**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createheap)
</dt> <dt>

[<span data-ttu-id="77589-115">**ID3D12Heap**</span><span class="sxs-lookup"><span data-stu-id="77589-115">**ID3D12Heap**</span></span>](/windows/desktop/api/d3d12/nn-d3d12-id3d12heap)
</dt> <dt>

[<span data-ttu-id="77589-116">Gerenciamento de memória</span><span class="sxs-lookup"><span data-stu-id="77589-116">Memory Management</span></span>](memory-management.md)
</dt> </dl>

 

 





