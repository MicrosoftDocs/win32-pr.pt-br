---
title: Acesso ao pipeline para recursos lado a lado
description: Os recursos do lado do xadrez podem ser usados em modos de exibição de recurso de sombreador (SRV), exibições de destino de renderização (RTV), exibições de estêncil de profundidade (DSV) e exibições de acesso não ordenado (UAV), bem como alguns pontos de ligação em que as exibições não são usadas, como associações de buffer de vértice.
ms.assetid: D0BC0B6C-2325-4EAF-9E80-E748F58045B1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef4a183fcaee90d84985a09c83826a4ad0b6d646
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641588"
---
# <a name="pipeline-access-to-tiled-resources"></a><span data-ttu-id="28f60-103">Acesso ao pipeline para recursos lado a lado</span><span class="sxs-lookup"><span data-stu-id="28f60-103">Pipeline access to tiled resources</span></span>

<span data-ttu-id="28f60-104">Os recursos do lado do xadrez podem ser usados em modos de exibição de recurso de sombreador (SRV), exibições de destino de renderização (RTV), exibições de estêncil de profundidade (DSV) e exibições de acesso não ordenado (UAV), bem como alguns pontos de ligação em que as exibições não são usadas, como associações de buffer de vértice.</span><span class="sxs-lookup"><span data-stu-id="28f60-104">Tiled resources can be used in shader resource views (SRV), render target views (RTV), depth stencil views (DSV) and unordered access views (UAV), as well as some bind points where views aren't used, such as vertex buffer bindings.</span></span> <span data-ttu-id="28f60-105">Para obter a lista de associações com suporte, consulte [parâmetros de criação de recursos de lado e xadrez](tiled-resource-creation-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="28f60-105">For the list of supported bindings, see [Tiled resource creation parameters](tiled-resource-creation-parameters.md).</span></span> <span data-ttu-id="28f60-106">\*As operações de cópia também funcionam em recursos de lado.</span><span class="sxs-lookup"><span data-stu-id="28f60-106">Copy\* operations also work on tiled resources.</span></span>

<span data-ttu-id="28f60-107">Se várias coordenadas de bloco em um ou mais modos de exibição estiverem vinculadas ao mesmo local de memória, leituras e gravações de diferentes caminhos para a mesma memória ocorrerão em uma ordem de acesso de memória não determinística e não repetida.</span><span class="sxs-lookup"><span data-stu-id="28f60-107">If multiple tile coordinates in one or more views is bound to the same memory location, reads and writes from different paths to the same memory will occur in a non-deterministic and non-repeatable order of memory accesses.</span></span>

<span data-ttu-id="28f60-108">Se todos os blocos por trás de um volume de acesso de memória de um sombreador estiverem mapeados para blocos exclusivos, o comportamento será idêntico em todas as implementações para superfícies com o mesmo conteúdo da memória de maneira sem blocos.</span><span class="sxs-lookup"><span data-stu-id="28f60-108">If all tiles behind a memory access footprint from a shader are mapped to unique tiles, behavior is identical on all implementations to the surface having the same memory contents in a non-tiled fashion.</span></span>

<span data-ttu-id="28f60-109">Esta seção fornece mais informações sobre o acesso do pipeline a recursos de lado.</span><span class="sxs-lookup"><span data-stu-id="28f60-109">This section provides more info about pipeline access to tiled resources.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="28f60-110">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="28f60-110">In this section</span></span>



| <span data-ttu-id="28f60-111">Tópico</span><span class="sxs-lookup"><span data-stu-id="28f60-111">Topic</span></span>                                                                                                              | <span data-ttu-id="28f60-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="28f60-112">Description</span></span>                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="28f60-113">Comportamento de SRV com blocos não mapeados</span><span class="sxs-lookup"><span data-stu-id="28f60-113">SRV behavior with non-mapped tiles</span></span>](srv-behavior-with-non-mapped-tiles.md)<br/>                            | <span data-ttu-id="28f60-114">O comportamento de leituras de modo de exibição (SRV) de recurso de sombreador que envolve blocos não mapeados depende do nível de suporte de hardware.</span><span class="sxs-lookup"><span data-stu-id="28f60-114">Behavior of shader resource view (SRV) reads that involve non-mapped tiles depends on the level of hardware support.</span></span> <br/>                                          |
| [<span data-ttu-id="28f60-115">Comportamento de UAV com blocos não mapeados</span><span class="sxs-lookup"><span data-stu-id="28f60-115">UAV behavior with non-mapped tiles</span></span>](uav-behavior-with-non-mapped-tiles.md)<br/>                            | <span data-ttu-id="28f60-116">O comportamento das leituras e gravações de modo de exibição de acesso não ordenado (UAV) depende do nível de suporte do hardware.</span><span class="sxs-lookup"><span data-stu-id="28f60-116">Behavior of unordered access view (UAV) reads and writes depends on the level of hardware support.</span></span> <br/>                                                            |
| [<span data-ttu-id="28f60-117">Comportamento de rasterizador com blocos não mapeados</span><span class="sxs-lookup"><span data-stu-id="28f60-117">Rasterizer behavior with non-mapped tiles</span></span>](rasterizer-behavior-with-non-mapped-tiles.md)<br/>              | <span data-ttu-id="28f60-118">Esta seção descreve o comportamento de rasterizador com blocos não mapeados.</span><span class="sxs-lookup"><span data-stu-id="28f60-118">This section describes rasterizer behavior with non-mapped tiles.</span></span><br/>                                                                                              |
| [<span data-ttu-id="28f60-119">Limitações de acesso de bloco com mapeamentos duplicados</span><span class="sxs-lookup"><span data-stu-id="28f60-119">Tile access limitations with duplicate mappings</span></span>](tile-access-limitations-with-duplicate-mappings-.md)<br/> | <span data-ttu-id="28f60-120">Esta seção descreve as limitações de acesso de bloco com mapeamentos duplicados.</span><span class="sxs-lookup"><span data-stu-id="28f60-120">This section describes tile access limitations with duplicate mappings.</span></span><br/>                                                                                        |
| [<span data-ttu-id="28f60-121">Recursos de amostragem de textura de recursos ao lado</span><span class="sxs-lookup"><span data-stu-id="28f60-121">Tiled resources texture sampling features</span></span>](tiled-resources-texture-sampling-features.md)<br/>              | <span data-ttu-id="28f60-122">Esta seção descreve os recursos de amostragem de textura de recursos com ladrilhos.</span><span class="sxs-lookup"><span data-stu-id="28f60-122">This section describes tiled resources texture sampling features.</span></span><br/>                                                                                              |
| [<span data-ttu-id="28f60-123">Exposição dos recursos do lado do HLSL</span><span class="sxs-lookup"><span data-stu-id="28f60-123">HLSL tiled resources exposure</span></span>](hlsl-tiled-resources-exposure.md)<br/>                                      | <span data-ttu-id="28f60-124">A nova sintaxe de HLSL (linguagem de sombreamento de alto nível) da Microsoft é necessária para dar suporte a recursos de lado do [sombreado no modelo de Shader](/windows/desktop/direct3dhlsl/d3d11-graphics-reference-sm5)</span><span class="sxs-lookup"><span data-stu-id="28f60-124">New Microsoft High Level Shader Language (HLSL) syntax is required to support tiled resources in [Shader Model 5](/windows/desktop/direct3dhlsl/d3d11-graphics-reference-sm5).</span></span> <br/> |



 

## <a name="related-topics"></a><span data-ttu-id="28f60-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="28f60-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28f60-126">Recursos em ladrilho</span><span class="sxs-lookup"><span data-stu-id="28f60-126">Tiled resources</span></span>](tiled-resources.md)
</dt> </dl>

 

