---
title: Gerenciamento de memória no Direct3D 12
description: A mudança para o D3D12 envolve a sincronização adequada e o gerenciamento da residência de memória.
ms.assetid: 94D47EBB-8060-49F6-A1FF-8B7B98AD5363
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 037a2d75adcde6ff03adf2ccee8ce30d33d090c7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104358"
---
# <a name="memory-management-in-direct3d-12"></a><span data-ttu-id="a221e-103">Gerenciamento de memória no Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="a221e-103">Memory Management in Direct3D 12</span></span>

<span data-ttu-id="a221e-104">A mudança para o D3D12 envolve a sincronização adequada e o gerenciamento da residência de memória.</span><span class="sxs-lookup"><span data-stu-id="a221e-104">Moving to D3D12 involves doing proper synchronization and management of memory residency.</span></span> <span data-ttu-id="a221e-105">O gerenciamento de residência de memória significa que ainda mais sincronização deve ser feita.</span><span class="sxs-lookup"><span data-stu-id="a221e-105">Managing memory residency means even more synchronization must be done.</span></span> <span data-ttu-id="a221e-106">Esta seção aborda as estratégias de gerenciamento de memória e a subalocação dentro de heaps e buffers.</span><span class="sxs-lookup"><span data-stu-id="a221e-106">This section covers memory management strategies, and suballocation within heaps and buffers.</span></span>

-   [<span data-ttu-id="a221e-107">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="a221e-107">In this section</span></span>](#in-this-section)
-   [<span data-ttu-id="a221e-108">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a221e-108">Related topics</span></span>](#related-topics)

## <a name="in-this-section"></a><span data-ttu-id="a221e-109">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="a221e-109">In this section</span></span>



| <span data-ttu-id="a221e-110">Tópico</span><span class="sxs-lookup"><span data-stu-id="a221e-110">Topic</span></span>                                                                       | <span data-ttu-id="a221e-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="a221e-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a221e-112">Estratégias de gerenciamento de memória</span><span class="sxs-lookup"><span data-stu-id="a221e-112">Memory Management Strategies</span></span>](memory-management-strategies.md)<br/> | <span data-ttu-id="a221e-113">Um Gerenciador de memória para o Direct3D 12 poderia ficar muito complicado com todas as diferentes camadas de suporte, para adaptadores de uma ou discretas (não de uma) e com uma variedade considerável de diferenças de arquitetura entre os adaptadores de GPU.</span><span class="sxs-lookup"><span data-stu-id="a221e-113">A memory manager for Direct3D 12 could get very complicated quickly with all the different tiers of support, for UMA or discreet (non-UMA) adapters, and with a considerable range of architecture differences between GPU adapters.</span></span><br/> <span data-ttu-id="a221e-114">A estratégia recomendada para o gerenciamento de memória do Direct3D 12, descrita nesta seção, é "classificar, orçamento e fluxo".</span><span class="sxs-lookup"><span data-stu-id="a221e-114">The recommended strategy for Direct3D 12 memory management , described in this section, is "classify, budget and stream".</span></span><br/> |
| [<span data-ttu-id="a221e-115">Subalocação em buffers</span><span class="sxs-lookup"><span data-stu-id="a221e-115">Suballocation Within Buffers</span></span>](large-buffers.md)<br/>                | <span data-ttu-id="a221e-116">Os buffers têm todos os recursos necessários no D3D12 para que os aplicativos transfiram uma grande variedade de dados transitórios da CPU para a GPU.</span><span class="sxs-lookup"><span data-stu-id="a221e-116">Buffers have all the features necessary in D3D12 for applications to transfer a large range of transient data from the CPU to the GPU.</span></span> <span data-ttu-id="a221e-117">Esta seção aborda quatro cenários comuns para o uso e o gerenciamento de recursos e buffers.</span><span class="sxs-lookup"><span data-stu-id="a221e-117">This section covers four common scenarios for the use and management of resources and buffers.</span></span><br/>                                                                                                                                     |
| [<span data-ttu-id="a221e-118">Subalocação dentro de heaps</span><span class="sxs-lookup"><span data-stu-id="a221e-118">Suballocation Within Heaps</span></span>](suballocation-within-heaps.md)<br/>     | <span data-ttu-id="a221e-119">Heaps de recursos transferem dados da CPU para a GPU (carregamento) e da GPU para a CPU (leitura de volta).</span><span class="sxs-lookup"><span data-stu-id="a221e-119">Resource heaps transfer data from the CPU to the GPU (upload), and from the GPU to the CPU (read back).</span></span> <br/>                                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="a221e-120">Residência</span><span class="sxs-lookup"><span data-stu-id="a221e-120">Residency</span></span>](residency.md)<br/>                                       | <span data-ttu-id="a221e-121">Um objeto é considerado *residente* quando ele é acessível pela GPU.</span><span class="sxs-lookup"><span data-stu-id="a221e-121">An object is considered to be *resident* when it is accessible by the GPU.</span></span><br/>                                                                                                                                                                                                                                                                                                |



 

## <a name="related-topics"></a><span data-ttu-id="a221e-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a221e-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a221e-123">Guia de programação do Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="a221e-123">Direct3D 12 Programming Guide</span></span>](directx-12-programming-guide.md)
</dt> <dt>

[<span data-ttu-id="a221e-124">Associação de recursos</span><span class="sxs-lookup"><span data-stu-id="a221e-124">Resource Binding</span></span>](resource-binding.md)
</dt> </dl>

 

 





