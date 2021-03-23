---
title: Heaps de descritores
description: Um heap de descritor é uma coleção de alocações contíguas de descritores, uma alocação para cada descritor.
ms.assetid: 04d3facf-21ec-45ca-ad9b-78fdcddc7136
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f19821cff5e8730c376e5c80fef07e67974d31d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "74105049"
---
# <a name="descriptor-heaps"></a><span data-ttu-id="be00a-103">Heaps de descritores</span><span class="sxs-lookup"><span data-stu-id="be00a-103">Descriptor Heaps</span></span>

<span data-ttu-id="be00a-104">Um heap de descritor é uma coleção de alocações contíguas de descritores, uma alocação para cada descritor.</span><span class="sxs-lookup"><span data-stu-id="be00a-104">A descriptor heap is a collection of contiguous allocations of descriptors, one allocation for every descriptor.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="be00a-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="be00a-105">In this section</span></span>



| <span data-ttu-id="be00a-106">Tópico</span><span class="sxs-lookup"><span data-stu-id="be00a-106">Topic</span></span>                                                                                             | <span data-ttu-id="be00a-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="be00a-107">Description</span></span>                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="be00a-108">Visão geral de heaps de descritores</span><span class="sxs-lookup"><span data-stu-id="be00a-108">Descriptor Heaps Overview</span></span>](descriptor-heaps-overview.md)<br/>                             | <span data-ttu-id="be00a-109">Heaps de descritores contêm muitos tipos de objeto que não fazem parte de um PSO (objeto de estado de pipeline), como SRVs (exibições de recursos de sombreamento), UAVs (exibições de acesso não ordenado), CBVs (exibições de buffer de constantes) e amostras.</span><span class="sxs-lookup"><span data-stu-id="be00a-109">Descriptor heaps contain many object types that are not part of a Pipeline State Object (PSO), such as Shader Resource Views (SRVs), Unordered Access Views (UAVs), Constant Buffer Views (CBVs), and Samplers.</span></span> <br/>                |
| [<span data-ttu-id="be00a-110">Camadas de hardware</span><span class="sxs-lookup"><span data-stu-id="be00a-110">Hardware Tiers</span></span>](hardware-support.md)<br/>                                                 | <span data-ttu-id="be00a-111">Os níveis de hardware da camada 1 para a camada 3 têm recursos crescentes disponíveis para o pipeline.</span><span class="sxs-lookup"><span data-stu-id="be00a-111">The levels of hardware from Tier 1 to Tier 3 have increasing resources available to the pipeline.</span></span> <br/>                                                                                                                              |
| [<span data-ttu-id="be00a-112">Heaps de descritor visíveis do sombreador</span><span class="sxs-lookup"><span data-stu-id="be00a-112">Shader Visible Descriptor Heaps</span></span>](shader-visible-descriptor-heaps.md)<br/>                 | <span data-ttu-id="be00a-113">Heaps de descritores visíveis de sombreador, são heaps de descritores que podem ser referenciados por sombreadores por meio de tabelas de descritor.</span><span class="sxs-lookup"><span data-stu-id="be00a-113">Shader visible descriptor heaps, are descriptor heaps that can be referenced by shaders through descriptor tables.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="be00a-114">Heaps de descritor visíveis sem sombreador</span><span class="sxs-lookup"><span data-stu-id="be00a-114">Non Shader Visible Descriptor Heaps</span></span>](non-shader-visible-descriptor-heaps.md)<br/>         | <span data-ttu-id="be00a-115">Alguns heaps de descritores não podem ser referenciados por sombreadores por meio de tabelas de descritor, mas existem para auxiliar o aplicativo no preparo dos descritores antes de gravar uma lista de comandos ou porque nenhum heap visível de sombreador é necessário.</span><span class="sxs-lookup"><span data-stu-id="be00a-115">Some descriptor heaps cannot be referenced by shaders through descriptor tables, but exist either to assist the app in staging the descriptors prior to recording a command list or because no shader-visible heap is required.</span></span><br/> |
| [<span data-ttu-id="be00a-116">Criando heaps de descritor</span><span class="sxs-lookup"><span data-stu-id="be00a-116">Creating Descriptor Heaps</span></span>](creating-descriptor-heaps.md)<br/>                             | <span data-ttu-id="be00a-117">Para criar e configurar um heap de descritor, você deve selecionar um tipo de heap de descritor, determinar quantos descritores ele contém e definir sinalizadores que indiquem se a CPU está visível e/ou sombreador visível.</span><span class="sxs-lookup"><span data-stu-id="be00a-117">To create and configure a descriptor heap, you must select a descriptor heap type, determine how many descriptors it contains, and set flags that indicate whether it is CPU visible and/or shader visible.</span></span> <br/>                    |
| [<span data-ttu-id="be00a-118">Configurando e populando heaps de descritor</span><span class="sxs-lookup"><span data-stu-id="be00a-118">Setting and Populating Descriptor Heaps</span></span>](setting-descriptor-heaps.md)<br/>                | <span data-ttu-id="be00a-119">Os tipos de heap de descritores que podem ser definidos em uma lista de comandos são aqueles que contêm descritores para os quais as tabelas de descrição podem ser usadas (no máximo uma de cada vez).</span><span class="sxs-lookup"><span data-stu-id="be00a-119">The descriptor heap types that can be set on a command list are those that contain descriptors for which descriptor tables can be used (at most one of each at a time).</span></span> <br/>                                                        |
| [<span data-ttu-id="be00a-120">Resumo de configurabilidade de heap do descritor</span><span class="sxs-lookup"><span data-stu-id="be00a-120">Descriptor Heap Configurability Summary</span></span>](descriptor-heap-configurability-summary.md)<br/> | <span data-ttu-id="be00a-121">A tabela a seguir resume as informações sobre o sombreador e o suporte a heap sem sombreador visível.</span><span class="sxs-lookup"><span data-stu-id="be00a-121">The following table summarizes information about Shader and non-Shader visible heap support.</span></span><br/>                                                                                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="be00a-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="be00a-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="be00a-123">Descritores</span><span class="sxs-lookup"><span data-stu-id="be00a-123">Descriptors</span></span>](descriptors.md)
</dt> <dt>

[<span data-ttu-id="be00a-124">Tabelas de descritores</span><span class="sxs-lookup"><span data-stu-id="be00a-124">Descriptor Tables</span></span>](descriptor-tables.md)
</dt> <dt>

[<span data-ttu-id="be00a-125">**ID3D12DescriptorHeap**</span><span class="sxs-lookup"><span data-stu-id="be00a-125">**ID3D12DescriptorHeap**</span></span>](/windows/desktop/api/d3d12/nn-d3d12-id3d12descriptorheap)
</dt> <dt>

[<span data-ttu-id="be00a-126">Associação de recursos</span><span class="sxs-lookup"><span data-stu-id="be00a-126">Resource Binding</span></span>](resource-binding.md)
</dt> <dt>

[<span data-ttu-id="be00a-127">Assinaturas raiz</span><span class="sxs-lookup"><span data-stu-id="be00a-127">Root Signatures</span></span>](root-signatures.md)
</dt> </dl>

 

 





