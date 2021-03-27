---
title: Modelo de sombreador HLSL 5
description: Modelo de sombreador HLSL 5
ms.assetid: 072c1ff2-ca1b-427c-9969-aa24ebb4ee38
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b33b0e2f009b796eb0b8828cc195fb9543ba2b9b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823835"
---
# <a name="hlsl-shader-model-5"></a><span data-ttu-id="135b4-103">Modelo de sombreador HLSL 5</span><span class="sxs-lookup"><span data-stu-id="135b4-103">HLSL Shader Model 5</span></span>

<span data-ttu-id="135b4-104">Esta seção contém material de visão geral para a linguagem High-Level Shader, especificamente os novos recursos no Shader Model 5 introduzidos no Microsoft Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="135b4-104">This section contains overview material for the High-Level Shader Language, specifically the new features in shader model 5 introduced in Microsoft Direct3D 11.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="135b4-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="135b4-105">In This Section</span></span>



| <span data-ttu-id="135b4-106">Item</span><span class="sxs-lookup"><span data-stu-id="135b4-106">Item</span></span>                                                                                                                                                                                                               | <span data-ttu-id="135b4-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="135b4-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="135b4-108"><span id="Dynamic_Linking"></span><span id="dynamic_linking"></span><span id="DYNAMIC_LINKING"></span>[Vinculação dinâmica](overviews-direct3d-11-hlsl-dynamic-linking.md)</span><span class="sxs-lookup"><span data-stu-id="135b4-108"><span id="Dynamic_Linking"></span><span id="dynamic_linking"></span><span id="DYNAMIC_LINKING"></span>[Dynamic Linking](overviews-direct3d-11-hlsl-dynamic-linking.md)</span></span><br/>                                 | <span data-ttu-id="135b4-109">A vinculação dinâmica permite que o tempo de execução tome uma decisão no tempo de empate (em vez de em tempo de compilação) sobre qual caminho de código deve ser executado.</span><span class="sxs-lookup"><span data-stu-id="135b4-109">Dynamic linking allows the runtime to make a decision at draw-time (rather than compile-time) about which code path to run.</span></span> <span data-ttu-id="135b4-110">Isso reduz o problema de proliferação de sombreador causado por sombreadores com assinaturas de entrada quase idênticas.</span><span class="sxs-lookup"><span data-stu-id="135b4-110">This reduces the shader proliferation problem caused by shaders with nearly identical input signatures.</span></span><br/>                                                                                                                         |
| <span data-ttu-id="135b4-111"><span id="Geometry_Shader_Features"></span><span id="geometry_shader_features"></span><span id="GEOMETRY_SHADER_FEATURES"></span>[Recursos do sombreador de geometria](overviews-direct3d-11-hlsl-gs-features.md)</span><span class="sxs-lookup"><span data-stu-id="135b4-111"><span id="Geometry_Shader_Features"></span><span id="geometry_shader_features"></span><span id="GEOMETRY_SHADER_FEATURES"></span>[Geometry Shader Features](overviews-direct3d-11-hlsl-gs-features.md)</span></span><br/> | <span data-ttu-id="135b4-112">Novos recursos de sombreador de geometria, incluindo: instanciação, que fornece um aumento de desempenho quando a ordem de primitivos no fluxo não importa, e fluxos de saída de vários pontos, para que um sombreador possa gerar vértices em mais de um fluxo.</span><span class="sxs-lookup"><span data-stu-id="135b4-112">New geometry shader features including: instancing, which provides a performance boost when the order of primitives in the stream doesn't matter, and multiple point output streams so a shader can output vertices on more than one stream.</span></span><br/>                                                                                                                |
| <span data-ttu-id="135b4-113"><span id="Tessellation"></span><span id="tessellation"></span><span id="TESSELLATION"></span>[Mosaico](/windows/desktop/direct3d11/direct3d-11-advanced-stages-tessellation)</span><span class="sxs-lookup"><span data-stu-id="135b4-113"><span id="Tessellation"></span><span id="tessellation"></span><span id="TESSELLATION"></span>[Tessellation](/windows/desktop/direct3d11/direct3d-11-advanced-stages-tessellation)</span></span><br/>                                        | <span data-ttu-id="135b4-114">O tempo de execução do Direct3D 11 dá suporte a três novos estágios que implementam mosaico, que converte as superfícies de subdivisão de detalhe baixo em primitivos de detalhes mais altos na GPU.</span><span class="sxs-lookup"><span data-stu-id="135b4-114">The Direct3D 11 runtime supports three new stages that implement tessellation, which converts low-detail subdivision surfaces into higher-detail primitives on the GPU.</span></span> <span data-ttu-id="135b4-115">O bloco de mosaico organiza (ou decompõe) as superfícies de ordem superior em estruturas adequadas para renderização.</span><span class="sxs-lookup"><span data-stu-id="135b4-115">Tessellation tiles (or breaks up) high-order surfaces into suitable structures for rendering.</span></span> <span data-ttu-id="135b4-116">Os três estágios de mosaico são envoltória-Shader, Tessellator e estágios de sombreador de domínio.</span><span class="sxs-lookup"><span data-stu-id="135b4-116">The three tessellation stages are hull-shader, tessellator, and domain-shader stages.</span></span><br/> |



 

<span data-ttu-id="135b4-117">Além disso, a seção de referência aborda muitos novos elementos de API para o modelo de sombreador 5, incluindo: [atributos](d3d11-graphics-reference-sm5-attributes.md), [funções intrínsecas](d3d11-graphics-reference-sm5-intrinsics.md), [objetos e métodos do sombreador 5 e](d3d11-graphics-reference-sm5-objects.md) [valores do sistema](d3d11-graphics-reference-sm5-system-values.md).</span><span class="sxs-lookup"><span data-stu-id="135b4-117">In addition, the reference section covers many new API elements for shader model 5 including: [attributes](d3d11-graphics-reference-sm5-attributes.md), [intrinsic functions](d3d11-graphics-reference-sm5-intrinsics.md), [shader model 5 objects and methods](d3d11-graphics-reference-sm5-objects.md), and [system values](d3d11-graphics-reference-sm5-system-values.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="135b4-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="135b4-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="135b4-119">Guia de programação para HLSL</span><span class="sxs-lookup"><span data-stu-id="135b4-119">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

