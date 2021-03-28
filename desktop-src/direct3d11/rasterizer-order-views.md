---
title: Exibições de ordem do rasterizador
description: As exibições ordenadas do rasterizador (ROVs) permitem que o código do sombreador de pixel marque as associações UAV com uma declaração que altera os requisitos normais para a ordem dos resultados do pipeline de gráficos para o UAVs.
ms.assetid: 7FCFCD28-E68D-4594-8879-937F57245507
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d891701aeaadd6f4474aeed8303d9b0046d1b656
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084764"
---
# <a name="rasterizer-order-views"></a><span data-ttu-id="1357c-103">Exibições de ordem do rasterizador</span><span class="sxs-lookup"><span data-stu-id="1357c-103">Rasterizer Order Views</span></span>

<span data-ttu-id="1357c-104">As exibições ordenadas do rasterizador (ROVs) permitem que o código do sombreador de pixel marque as associações UAV com uma declaração que altera os requisitos normais para a ordem dos resultados do pipeline de gráficos para o UAVs.</span><span class="sxs-lookup"><span data-stu-id="1357c-104">Rasterizer ordered views (ROVs) allow pixel shader code to mark UAV bindings with a declaration that alters the normal requirements for the order of graphics pipeline results for UAVs.</span></span> <span data-ttu-id="1357c-105">Isso permite que algoritmos de OIT (transparência independente de ordem) funcionem, o que fornece resultados de renderização muito melhores quando vários objetos transparentes estão em linha entre si em uma exibição.</span><span class="sxs-lookup"><span data-stu-id="1357c-105">This enables Order Independent Transparency (OIT) algorithms to work, which give much better rendering results when multiple transparent objects are in line with each other in a view.</span></span>

-   [<span data-ttu-id="1357c-106">Visão geral</span><span class="sxs-lookup"><span data-stu-id="1357c-106">Overview</span></span>](#overview)
-   [<span data-ttu-id="1357c-107">Detalhes da implementação</span><span class="sxs-lookup"><span data-stu-id="1357c-107">Implementation details</span></span>](#implementation-details)
-   [<span data-ttu-id="1357c-108">Resumo da API</span><span class="sxs-lookup"><span data-stu-id="1357c-108">API summary</span></span>](#api-summary)
-   [<span data-ttu-id="1357c-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1357c-109">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="1357c-110">Visão geral</span><span class="sxs-lookup"><span data-stu-id="1357c-110">Overview</span></span>

<span data-ttu-id="1357c-111">Pipelines gráficos padrão podem ter problemas para compor corretamente várias texturas que contêm transparência.</span><span class="sxs-lookup"><span data-stu-id="1357c-111">Standard graphics pipelines may have trouble correctly compositing together multiple textures that contain transparency.</span></span> <span data-ttu-id="1357c-112">Objetos como isolamentos de fio, fumaça, fogo, vegetação e transparência de uso de vidro colorido para obter o efeito desejado.</span><span class="sxs-lookup"><span data-stu-id="1357c-112">Objects such as wire fences, smoke, fire, vegetation, and colored glass use transparency to get the desired effect.</span></span> <span data-ttu-id="1357c-113">Os problemas surgem quando várias texturas que contêm transparência estão alinhadas umas com as outras (fumaça na frente de uma cerca na frente de um prédio contendo vegetação, como um exemplo).</span><span class="sxs-lookup"><span data-stu-id="1357c-113">Problems arise when multiple textures that contain transparency are in line with each other (smoke in front of a fence in front of a glass building containing vegetation, as an example).</span></span> <span data-ttu-id="1357c-114">As exibições ordenadas do rasterizador (ROVs) permitem que os algoritmos subjacentes do OIT usem recursos do hardware para tentar resolver a ordem de transparência corretamente.</span><span class="sxs-lookup"><span data-stu-id="1357c-114">Rasterizer ordered views (ROVs) enable the underlying OIT algorithms to use features of the hardware to try to resolve the transparency order correctly.</span></span> <span data-ttu-id="1357c-115">A transparência é manipulada pelo sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="1357c-115">Transparency is handled by the pixel shader.</span></span>

<span data-ttu-id="1357c-116">As exibições ordenadas do rasterizador (ROVs) permitem que o código do sombreador de pixel marque as associações UAV com uma declaração que altera os requisitos normais para a ordem dos resultados do pipeline de gráficos para o UAVs.</span><span class="sxs-lookup"><span data-stu-id="1357c-116">Rasterizer ordered views (ROVs) allow pixel shader code to mark UAV bindings with a declaration that alters the normal requirements for the order of graphics pipeline results for UAVs.</span></span>

<span data-ttu-id="1357c-117">ROVs garante a ordem dos acessos UAV para qualquer par de invocações de sombreador de pixel sobrepostas.</span><span class="sxs-lookup"><span data-stu-id="1357c-117">ROVs guarantee the order of UAV accesses for any pair of overlapping pixel shader invocations.</span></span> <span data-ttu-id="1357c-118">Nesse caso, "sobreposto" significa que as invocações são geradas pelas mesmas chamadas de desenho e compartilham a mesma coordenada de pixel quando no modo de execução de frequência de pixels e o mesmo pixel e coordenada de exemplo no modo de frequência de amostra.</span><span class="sxs-lookup"><span data-stu-id="1357c-118">In this case “overlapping” means that the invocations are generated by the same draw calls and share the same pixel coordinate when in pixel-frequency execution mode, and the same pixel and sample coordinate in sample-frequency mode.</span></span>

<span data-ttu-id="1357c-119">A ordem em que a sobreposição de acessos ROV de invocações de sombreador de pixel são executadas é idêntica à ordem em que a geometria é enviada.</span><span class="sxs-lookup"><span data-stu-id="1357c-119">The order in which overlapping ROV accesses of pixel shader invocations are executed is identical to the order in which the geometry is submitted.</span></span> <span data-ttu-id="1357c-120">Isso significa que, para a sobreposição de invocações de sombreador de pixel, as gravações ROV executadas por uma invocação de sombreador de pixel devem estar disponíveis para serem lidas por uma invocação subsequente e não devem afetar as leituras por uma invocação anterior.</span><span class="sxs-lookup"><span data-stu-id="1357c-120">This means that, for overlapping pixel shader invocations, ROV writes performed by a pixel shader invocation must be available to be read by a subsequent invocation and must not affect reads by a previous invocation.</span></span> <span data-ttu-id="1357c-121">As leituras de ROV executadas por uma invocação de sombreador de pixel devem refletir as gravações por uma invocação anterior e não devem refletir as gravações por uma invocação subsequente.</span><span class="sxs-lookup"><span data-stu-id="1357c-121">ROV reads performed by a pixel shader invocation must reflect writes by a previous invocation and must not reflect writes by a subsequent invocation.</span></span> <span data-ttu-id="1357c-122">Isso é importante para UAVs porque eles são explicitamente omitidos das garantias de invariação de saída normalmente definidas pela ordem fixa de resultados de pipeline de gráficos.</span><span class="sxs-lookup"><span data-stu-id="1357c-122">This is important for UAVs because they are explicitly omitted from the output-invariance guarantees normally set by the fixed order of graphics pipeline results.</span></span>

## <a name="implementation-details"></a><span data-ttu-id="1357c-123">Detalhes de implementação</span><span class="sxs-lookup"><span data-stu-id="1357c-123">Implementation details</span></span>

<span data-ttu-id="1357c-124">As exibições ordenadas do rasterizador (ROVs) são declaradas com os novos objetos de HLSL (linguagem de sombreamento de alto nível) e estão disponíveis somente para o sombreador de pixel:</span><span class="sxs-lookup"><span data-stu-id="1357c-124">Rasterizer ordered views (ROVs) are declared with the following new High Level Shader Language (HLSL) objects, and are only available to the pixel shader:</span></span>

-   `RasterizerOrderedBuffer`
-   `RasterizerOrderedByteAddressBuffer`
-   `RasterizerOrderedStructuredBuffer`
-   `RasterizerOrderedTexture1D`
-   `RasterizerOrderedTexture1DArray`
-   `RasterizerOrderedTexture2D`
-   `RasterizerOrderedTexture2DArray`
-   `RasterizerOrderedTexture3D`

<span data-ttu-id="1357c-125">Use esses objetos da mesma maneira que outros objetos UAV (como, `RWBuffer` etc.).</span><span class="sxs-lookup"><span data-stu-id="1357c-125">Use these objects in the same manner as other UAV objects (such as `RWBuffer` etc.).</span></span>

## <a name="api-summary"></a><span data-ttu-id="1357c-126">Resumo da API</span><span class="sxs-lookup"><span data-stu-id="1357c-126">API summary</span></span>

<span data-ttu-id="1357c-127">ROVs são uma construção somente HLSL que aplica semântica de comportamento diferente ao UAVs.</span><span class="sxs-lookup"><span data-stu-id="1357c-127">ROVs are an HLSL-only construct that applies different behavior semantics to UAVs.</span></span> <span data-ttu-id="1357c-128">Todas as APIs relevantes para UAVs também são relevantes para ROVs.</span><span class="sxs-lookup"><span data-stu-id="1357c-128">All APIs relevant to UAVs are also relevant to ROVs.</span></span> <span data-ttu-id="1357c-129">Observe que o seguinte método, estruturas e classe auxiliar fazem referência ao rasterizador:</span><span class="sxs-lookup"><span data-stu-id="1357c-129">Note that the following method, structures, and helper class reference the rasterizer:</span></span>

-   <span data-ttu-id="1357c-130">[**D3D11 \_ RASTERIZAdor \_ DESC2**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_rasterizer_desc2) : estrutura que mantém a descrição do rasterizador, observando a \_ classe auxiliar do CD3D12 rasterizador \_ DESC2 para criar descrições do rasterizador.</span><span class="sxs-lookup"><span data-stu-id="1357c-130">[**D3D11\_RASTERIZER\_DESC2**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_rasterizer_desc2) : structure holding the rasterizer description, noting the CD3D12\_RASTERIZER\_DESC2 helper class for creating rasterizer descriptions.</span></span>
-   <span data-ttu-id="1357c-131">[**D3D11 \_ Dados de recurso \_ \_ D3D11 \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) : estrutura que contém o booliano `ROVsSupported` , indicando o suporte.</span><span class="sxs-lookup"><span data-stu-id="1357c-131">[**D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) : structure holding the boolean `ROVsSupported`, indicating the support.</span></span>
-   <span data-ttu-id="1357c-132">[**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) : método para acessar os recursos com suporte.</span><span class="sxs-lookup"><span data-stu-id="1357c-132">[**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) : method to access the supported features.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1357c-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1357c-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1357c-134">Recursos do Direct3D 11,3</span><span class="sxs-lookup"><span data-stu-id="1357c-134">Direct3D 11.3 Features</span></span>](direct3d-11-3-features.md)
</dt> <dt>

[<span data-ttu-id="1357c-135">Modelo do sombreador 5,1</span><span class="sxs-lookup"><span data-stu-id="1357c-135">Shader Model 5.1</span></span>](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> </dl>

 

 