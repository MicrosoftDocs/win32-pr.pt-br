---
title: Estágio de rasterizador
description: O estágio de rasterização converte as informações de vetor (compostas de formas ou primitivas) em uma imagem de rasterizador (composta de pixels) para fins de exibição de gráficos 3D em tempo real.
ms.assetid: efd3f819-7c63-4e1a-9923-8e7198354ec6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e746c5ace3512f36f9b9ad34d34a3ea578e1de36
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103917811"
---
# <a name="rasterizer-stage"></a><span data-ttu-id="1fdcb-103">Estágio de rasterizador</span><span class="sxs-lookup"><span data-stu-id="1fdcb-103">Rasterizer Stage</span></span>

<span data-ttu-id="1fdcb-104">O estágio de rasterização converte as informações de vetor (compostas de formas ou primitivas) em uma imagem de rasterizador (composta de pixels) para fins de exibição de gráficos 3D em tempo real.</span><span class="sxs-lookup"><span data-stu-id="1fdcb-104">The rasterization stage converts vector information (composed of shapes or primitives) into a raster image (composed of pixels) for the purpose of displaying real-time 3D graphics.</span></span>

<span data-ttu-id="1fdcb-105">Durante a rasterização, cada primitiva é convertida em pixels, enquanto interpola valores por vértice entre cada primitiva.</span><span class="sxs-lookup"><span data-stu-id="1fdcb-105">During rasterization, each primitive is converted into pixels, while interpolating per-vertex values across each primitive.</span></span> <span data-ttu-id="1fdcb-106">A rasterização inclui o recorte de vértices para o tronco de exibição, execução de uma divisão por z para fornecer perspectiva, mapeamento de primitivas para um visor 2D e determinação de como invocar o sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="1fdcb-106">Rasterization includes clipping vertices to the view frustum, performing a divide by z to provide perspective, mapping primitives to a 2D viewport, and determining how to invoke the pixel shader.</span></span> <span data-ttu-id="1fdcb-107">Embora o uso de um sombreador de pixel seja opcional, o estágio do rasterizador sempre realiza recorte, uma divisão de perspectiva para transformar os pontos em espaço homogêneo e mapeia os vértices para o visor.</span><span class="sxs-lookup"><span data-stu-id="1fdcb-107">While using a pixel shader is optional, the rasterizer stage always performs clipping, a perspective divide to transform the points into homogeneous space, and maps the vertices to the viewport.</span></span>

<span data-ttu-id="1fdcb-108">Os vértices (x, y, z, w), que entram no estágio do rasterizador, são considerados no espaço de clipe homogêneo.</span><span class="sxs-lookup"><span data-stu-id="1fdcb-108">Vertices (x,y,z,w), coming into the rasterizer stage are assumed to be in homogeneous clip-space.</span></span> <span data-ttu-id="1fdcb-109">Nesse espaço de coordenadas, o eixo X aponta para a direita, Y aponta para cima, Z aponta para longe da câmera.</span><span class="sxs-lookup"><span data-stu-id="1fdcb-109">In this coordinate space the X axis points right, Y points up and Z points away from camera.</span></span>

<span data-ttu-id="1fdcb-110">Você pode desabilitar a rasterização informando ao pipeline que não há um sombreador de pixel (defina o estágio do sombreador de pixel como **nulo** com [**ID3D11DeviceContext::P ssetshader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshader)) e desabilitando o teste de profundidade e de estêncil (defina **DepthEnable** e **StencilEnable** como **false** no [**estêncil de \_ profundidade D3D11 \_ \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)).</span><span class="sxs-lookup"><span data-stu-id="1fdcb-110">You may disable rasterization by telling the pipeline there is no pixel shader (set the pixel shader stage to **NULL** with [**ID3D11DeviceContext::PSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshader)), and disabling depth and stencil testing (set **DepthEnable** and **StencilEnable** to **FALSE** in [**D3D11\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)).</span></span> <span data-ttu-id="1fdcb-111">Enquanto estão desabilitados, os contadores do pipeline relacionados à rasterização não serão atualizados.</span><span class="sxs-lookup"><span data-stu-id="1fdcb-111">While disabled, rasterization-related pipeline counters will not update.</span></span> <span data-ttu-id="1fdcb-112">Também há uma descrição completa das regras de [rasterização](d3d10-graphics-programming-guide-rasterizer-stage-rules.md).</span><span class="sxs-lookup"><span data-stu-id="1fdcb-112">There is also a complete description of the [rasterization rules](d3d10-graphics-programming-guide-rasterizer-stage-rules.md).</span></span>

<span data-ttu-id="1fdcb-113">Em hardware que implementa otimizações hierárquicas de buffer Z, você pode habilitar o pré-carregamento do buffer z definindo o estágio do sombreador de pixel como **nulo** ao habilitar o teste de profundidade e de estêncil.</span><span class="sxs-lookup"><span data-stu-id="1fdcb-113">On hardware that implements hierarchical Z-buffer optimizations, you may enable preloading the z-buffer by setting the pixel shader stage to **NULL** while enabling depth and stencil testing.</span></span>


## <a name="in-this-section"></a><span data-ttu-id="1fdcb-114">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="1fdcb-114">In this section</span></span>



| <span data-ttu-id="1fdcb-115">Tópico</span><span class="sxs-lookup"><span data-stu-id="1fdcb-115">Topic</span></span>                                                                                                                         | <span data-ttu-id="1fdcb-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="1fdcb-116">Description</span></span>                                                                                                                                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1fdcb-117">Introdução com o estágio rasterizador</span><span class="sxs-lookup"><span data-stu-id="1fdcb-117">Getting Started with the Rasterizer Stage</span></span>](d3d10-graphics-programming-guide-rasterizer-stage-getting-started.md)<br/> | <span data-ttu-id="1fdcb-118">Esta seção descreve como definir o visor, o retângulo de tesoura, o estado do rasterizador e a várias amostras.</span><span class="sxs-lookup"><span data-stu-id="1fdcb-118">This section describes setting the viewport, the scissors rectangle, the rasterizer state, and multi-sampling.</span></span><br/>                                                                                                                                                                                                |
| [<span data-ttu-id="1fdcb-119">Regras de rasterização</span><span class="sxs-lookup"><span data-stu-id="1fdcb-119">Rasterization Rules</span></span>](d3d10-graphics-programming-guide-rasterizer-stage-rules.md)<br/>                                 | <span data-ttu-id="1fdcb-120">As regras de rasterização definem como os dados de vetor são mapeados nos dados de rasterização.</span><span class="sxs-lookup"><span data-stu-id="1fdcb-120">Rasterization rules define how vector data is mapped into raster data.</span></span> <span data-ttu-id="1fdcb-121">Os dados de rasterização são ajustados para locais de inteiro que são, em seguida, removidos e recortados (para desenhar o número mínimo de pixels) e atributos de por pixel são interpolados (de atributos de vértice) antes de serem passados para um sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="1fdcb-121">The raster data is snapped to integer locations that are then culled and clipped (to draw the minimum number of pixels), and per-pixel attributes are interpolated (from per-vertex attributes) before being passed to a pixel shader.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="1fdcb-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1fdcb-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1fdcb-123">Pipeline de gráficos</span><span class="sxs-lookup"><span data-stu-id="1fdcb-123">Graphics Pipeline</span></span>](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[<span data-ttu-id="1fdcb-124">Estágios de pipeline (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="1fdcb-124">Pipeline Stages (Direct3D 10)</span></span>](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

