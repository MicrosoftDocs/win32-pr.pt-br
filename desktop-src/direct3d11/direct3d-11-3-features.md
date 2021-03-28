---
title: Recursos do Direct3D 11,3
description: As seções a seguir descrevem a funcionalidade que foi adicionada no Direct3D 11,3. Esses recursos também estão disponíveis no Direct3D 12.
ms.assetid: CA79A315-22C4-4141-8E66-89C0DCF29191
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc256b9b85dd807e2e6c923affdec496fe92e075
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104368961"
---
# <a name="direct3d-113-features"></a><span data-ttu-id="43e4e-104">Recursos do Direct3D 11,3</span><span class="sxs-lookup"><span data-stu-id="43e4e-104">Direct3D 11.3 Features</span></span>

<span data-ttu-id="43e4e-105">As seções a seguir descrevem a funcionalidade que foi adicionada no Direct3D 11,3.</span><span class="sxs-lookup"><span data-stu-id="43e4e-105">The following sections describe the functionality has been added in Direct3D 11.3.</span></span> <span data-ttu-id="43e4e-106">Esses recursos também estão disponíveis no Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="43e4e-106">These features are also available in Direct3D 12.</span></span>


## <a name="in-this-section"></a><span data-ttu-id="43e4e-107">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="43e4e-107">In this section</span></span>



| <span data-ttu-id="43e4e-108">Tópico</span><span class="sxs-lookup"><span data-stu-id="43e4e-108">Topic</span></span>                                                                                               | <span data-ttu-id="43e4e-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="43e4e-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="43e4e-110">Rasterização conservativa</span><span class="sxs-lookup"><span data-stu-id="43e4e-110">Conservative Rasterization</span></span>](conservative-rasterization.md)<br/>                             | <span data-ttu-id="43e4e-111">A rasterização conservadora adiciona alguma certeza à renderização de pixels, que é útil em particular aos algoritmos de detecção de colisão.</span><span class="sxs-lookup"><span data-stu-id="43e4e-111">Conservative rasterization adds some certainty to pixel rendering, which is helpful in particular to collision detection algorithms.</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="43e4e-112">Mapeamento de textura padrão</span><span class="sxs-lookup"><span data-stu-id="43e4e-112">Default Texture Mapping</span></span>](default-texture-mapping.md)<br/>                                   | <span data-ttu-id="43e4e-113">O uso de mapeamento de textura padrão reduz a cópia e o uso de memória ao compartilhar dados de imagem entre a GPU e a CPU.</span><span class="sxs-lookup"><span data-stu-id="43e4e-113">The use of default texture mapping reduces copying and memory usage while sharing image data between the GPU and the CPU.</span></span> <span data-ttu-id="43e4e-114">No entanto, ele só deve ser usado em situações específicas.</span><span class="sxs-lookup"><span data-stu-id="43e4e-114">However, it should only be used in specific situations.</span></span> <span data-ttu-id="43e4e-115">O layout swizzle padrão evita copiar ou swizzling dados em vários layouts.</span><span class="sxs-lookup"><span data-stu-id="43e4e-115">The standard swizzle layout avoids copying or swizzling data in multiple layouts.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="43e4e-116">Exibições de ordem do rasterizador</span><span class="sxs-lookup"><span data-stu-id="43e4e-116">Rasterizer Order Views</span></span>](rasterizer-order-views.md)<br/>                                     | <span data-ttu-id="43e4e-117">As exibições ordenadas do rasterizador (ROVs) permitem que o código do sombreador de pixel marque as associações UAV com uma declaração que altera os requisitos normais para a ordem dos resultados do pipeline de gráficos para o UAVs.</span><span class="sxs-lookup"><span data-stu-id="43e4e-117">Rasterizer ordered views (ROVs) allow pixel shader code to mark UAV bindings with a declaration that alters the normal requirements for the order of graphics pipeline results for UAVs.</span></span> <span data-ttu-id="43e4e-118">Isso permite que algoritmos de OIT (transparência independente de ordem) funcionem, o que fornece resultados de renderização muito melhores quando vários objetos transparentes estão em linha entre si em uma exibição.</span><span class="sxs-lookup"><span data-stu-id="43e4e-118">This enables Order Independent Transparency (OIT) algorithms to work, which give much better rendering results when multiple transparent objects are in line with each other in a view.</span></span> <br/> |
| [<span data-ttu-id="43e4e-119">Valor de referência de estêncil especificado pelo sombreador</span><span class="sxs-lookup"><span data-stu-id="43e4e-119">Shader Specified Stencil Reference Value</span></span>](shader-specified-stencil-reference-value.md)<br/> | <span data-ttu-id="43e4e-120">A habilitação de sombreadores de pixel para produzir o valor de referência do estêncil, em vez de usar o especificado pela API, permite um controle muito refinado sobre as operações de estêncil.</span><span class="sxs-lookup"><span data-stu-id="43e4e-120">Enabling pixel shaders to output the Stencil Reference Value, rather than using the API-specified one, enables a very fine granular control over stencil operations.</span></span><br/>                                                                                                                                                                                                              |
| [<span data-ttu-id="43e4e-121">Cargas de exibição de acesso não ordenado digitado</span><span class="sxs-lookup"><span data-stu-id="43e4e-121">Typed Unordered Access View Loads</span></span>](typed-unordered-access-view-loads.md)<br/>               | <span data-ttu-id="43e4e-122">A carga digitada UAV (exibição de acesso não ordenada) é a capacidade de um sombreador de ler de um UAV com um formato DXGI específico \_ .</span><span class="sxs-lookup"><span data-stu-id="43e4e-122">Unordered Access View (UAV) Typed Load is the ability for a shader to read from a UAV with a specific DXGI\_FORMAT.</span></span><br/>                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="43e4e-123">Arquitetura de memória unificada</span><span class="sxs-lookup"><span data-stu-id="43e4e-123">Unified Memory Architecture</span></span>](unified-memory-architecture.md)<br/>                           | <span data-ttu-id="43e4e-124">Consultar se há suporte para a uma (arquitetura de memória unificada) pode ajudar a determinar como lidar com alguns recursos.</span><span class="sxs-lookup"><span data-stu-id="43e4e-124">Querying for whether Unified Memory Architecture (UMA) is supported can help determine how to handle some resources.</span></span><br/>                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="43e4e-125">Alocação dinâmica de volumes de recursos</span><span class="sxs-lookup"><span data-stu-id="43e4e-125">Volume Tiled Resources</span></span>](volume-tiled-resources.md)<br/>                                     | <span data-ttu-id="43e4e-126">Texturas de volume (3D) podem ser usadas como recursos ao lado, observando que a resolução do bloco é tridimensional.</span><span class="sxs-lookup"><span data-stu-id="43e4e-126">Volume (3D) textures can be used as tiled resources, noting that tile resolution is three-dimensional.</span></span><br/>                                                                                                                                                                                                                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="43e4e-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="43e4e-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43e4e-128">O que há de novo no Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="43e4e-128">What's new in Direct3D 11</span></span>](dx-graphics-overviews-introduction.md)
</dt> </dl>

 

 





