---
title: Configurando a funcionalidade de mesclagem
description: As operações de mesclagem são executadas em cada saída de sombreador de pixel (valor RGBA) antes que o valor de saída seja gravado em um destino de renderização. Se a multiamostragem estiver habilitada, a mesclagem será feita em cada multiamostra; caso contrário, a mesclagem será executada em cada pixel.
ms.assetid: f5c79baf-7bd3-4f58-abe7-8e96cd6be9d3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08acf1ea286b29a1cb96873bbfe170c6f38699f7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104988661"
---
# <a name="configuring-blending-functionality"></a><span data-ttu-id="c1c25-104">Configurando a funcionalidade de mesclagem</span><span class="sxs-lookup"><span data-stu-id="c1c25-104">Configuring Blending Functionality</span></span>

<span data-ttu-id="c1c25-105">As operações de mesclagem são executadas em cada saída de sombreador de pixel (valor RGBA) antes que o valor de saída seja gravado em um destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="c1c25-105">Blending operations are performed on every pixel shader output (RGBA value) before the output value is written to a render target.</span></span> <span data-ttu-id="c1c25-106">Se a multiamostragem estiver habilitada, a mesclagem será feita em cada multiamostra; caso contrário, a mesclagem será executada em cada pixel.</span><span class="sxs-lookup"><span data-stu-id="c1c25-106">If multisampling is enabled, blending is done on each multisample; otherwise, blending is performed on each pixel.</span></span>

-   [<span data-ttu-id="c1c25-107">Criar o estado de mesclagem</span><span class="sxs-lookup"><span data-stu-id="c1c25-107">Create the Blend State</span></span>](#create-the-blend-state)
-   [<span data-ttu-id="c1c25-108">Associar o estado de mesclagem</span><span class="sxs-lookup"><span data-stu-id="c1c25-108">Bind the Blend State</span></span>](#bind-the-blend-state)
-   [<span data-ttu-id="c1c25-109">Tópicos de mesclagem avançada</span><span class="sxs-lookup"><span data-stu-id="c1c25-109">Advanced Blending Topics</span></span>](#advanced-blending-topics)
    -   [<span data-ttu-id="c1c25-110">De alfa para cobertura</span><span class="sxs-lookup"><span data-stu-id="c1c25-110">Alpha-To-Coverage</span></span>](#alpha-to-coverage)
    -   [<span data-ttu-id="c1c25-111">Mesclagem de saídas de sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="c1c25-111">Blending Pixel Shader Outputs</span></span>](#blending-pixel-shader-outputs)
-   [<span data-ttu-id="c1c25-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c1c25-112">Related topics</span></span>](#related-topics)

## <a name="create-the-blend-state"></a><span data-ttu-id="c1c25-113">Criar o estado de mesclagem</span><span class="sxs-lookup"><span data-stu-id="c1c25-113">Create the Blend State</span></span>

<span data-ttu-id="c1c25-114">O estado de mesclagem é uma coleção de Estados usados para controlar a mesclagem.</span><span class="sxs-lookup"><span data-stu-id="c1c25-114">The blend state is a collection of states used to control blending.</span></span> <span data-ttu-id="c1c25-115">Esses Estados (definidos no [**D3D11 \_ Blend \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_blend_desc1)) são usados para criar o objeto de estado de mistura chamando [**ID3D11Device1:: CreateBlendState1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createblendstate1).</span><span class="sxs-lookup"><span data-stu-id="c1c25-115">These states (defined in [**D3D11\_BLEND\_DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_blend_desc1)) are used to create the blend state object by calling [**ID3D11Device1::CreateBlendState1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createblendstate1).</span></span>

<span data-ttu-id="c1c25-116">Por exemplo, aqui está um exemplo muito simples de criação de estado de mesclagem que desabilita a mistura alfa e não usa mascaramento de pixel por componente.</span><span class="sxs-lookup"><span data-stu-id="c1c25-116">For instance, here is a very simple example of blend-state creation that disables alpha blending and uses no per-component pixel masking.</span></span>


```
ID3D11BlendState1* g_pBlendStateNoBlend = NULL;

D3D11_BLEND_DESC1 BlendState;
ZeroMemory(&BlendState, sizeof(D3D11_BLEND_DESC1));
BlendState.RenderTarget[0].BlendEnable = FALSE;
BlendState.RenderTarget[0].RenderTargetWriteMask = D3D11_COLOR_WRITE_ENABLE_ALL;
pd3dDevice->CreateBlendState1(&BlendState, &g_pBlendStateNoBlend);
```



<span data-ttu-id="c1c25-117">Este exemplo é semelhante ao [exemplo de HLSLWithoutFX10](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="c1c25-117">This example is similar to the [HLSLWithoutFX10 Sample](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx).</span></span>

## <a name="bind-the-blend-state"></a><span data-ttu-id="c1c25-118">Associar o estado de mesclagem</span><span class="sxs-lookup"><span data-stu-id="c1c25-118">Bind the Blend State</span></span>

<span data-ttu-id="c1c25-119">Depois de criar o objeto de estado de mesclagem, associe o objeto de estado de mesclagem ao estágio de mesclagem de saída chamando [**ID3D11DeviceContext:: OMSetBlendState**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetblendstate).</span><span class="sxs-lookup"><span data-stu-id="c1c25-119">After you create the blend-state object, bind the blend-state object to the output-merger stage by calling [**ID3D11DeviceContext::OMSetBlendState**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetblendstate).</span></span>


```
float blendFactor[4] = { 0.0f, 0.0f, 0.0f, 0.0f };
UINT sampleMask   = 0xffffffff;

pd3dDevice->OMSetBlendState(g_pBlendStateNoBlend, blendFactor, sampleMask);
```



<span data-ttu-id="c1c25-120">Essa API usa três parâmetros: o objeto de estado de mesclagem, um fator de mistura de quatro componentes e uma máscara de exemplo.</span><span class="sxs-lookup"><span data-stu-id="c1c25-120">This API takes three parameters: the blend-state object, a four-component blend factor, and a sample mask.</span></span> <span data-ttu-id="c1c25-121">Você pode passar **NULL** para o objeto de estado de mesclagem para especificar o estado de mesclagem padrão ou passar um objeto de estado de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="c1c25-121">You can pass in **NULL** for the blend-state object to specify the default blend state or pass in a blend-state object.</span></span> <span data-ttu-id="c1c25-122">Se você criou o objeto de estado de mesclagem com o fator de mesclagem do [**D3D11 \_ Blend \_ \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_blend) ou o [**fator de mistura do D3D11 \_ Blend \_ inv \_ \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_blend), você pode passar um fator de mistura para valores modulares para o sombreador de pixel, o destino de renderização ou ambos.</span><span class="sxs-lookup"><span data-stu-id="c1c25-122">If you created the blend-state object with [**D3D11\_BLEND\_BLEND\_FACTOR**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_blend) or [**D3D11\_BLEND\_INV\_BLEND\_FACTOR**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_blend), you can pass a blend factor to modulate values for the pixel shader, render target, or both.</span></span> <span data-ttu-id="c1c25-123">Se você não criou o objeto Blend-State com o fator de mistura do **D3D11 \_ Blend \_ \_** ou o **fator de mistura do D3D11 \_ Blend \_ inv \_ \_**, ainda é possível passar um fator de mistura não nulo, mas o estágio de mesclagem não usa o fator de mistura; o tempo de execução armazena o fator de mistura e, posteriormente, você pode chamar [**ID3D11DeviceContext:: OMGetBlendState**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omgetblendstate) para recuperar o fator de mistura.</span><span class="sxs-lookup"><span data-stu-id="c1c25-123">If you didn't create the blend-state object with **D3D11\_BLEND\_BLEND\_FACTOR** or **D3D11\_BLEND\_INV\_BLEND\_FACTOR**, you can still pass a non-NULL blend factor, but the blending stage does not use the blend factor; the runtime stores the blend factor, and you can later call [**ID3D11DeviceContext::OMGetBlendState**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omgetblendstate) to retrieve the blend factor.</span></span> <span data-ttu-id="c1c25-124">Se você passar **NULL**, o tempo de execução usará ou armazenará um fator de mistura igual a {1, 1, 1, 1}.</span><span class="sxs-lookup"><span data-stu-id="c1c25-124">If you pass **NULL**, the runtime uses or stores a blend factor equal to { 1, 1, 1, 1 }.</span></span> <span data-ttu-id="c1c25-125">A máscara de exemplo é uma máscara definida pelo usuário que determina como obter uma amostra do destino de renderização existente antes de atualizá-lo.</span><span class="sxs-lookup"><span data-stu-id="c1c25-125">The sample mask is a user-defined mask that determines how to sample the existing render target before updating it.</span></span> <span data-ttu-id="c1c25-126">A máscara de amostragem padrão é 0xFFFFFFFF, que designa a amostragem de ponto.</span><span class="sxs-lookup"><span data-stu-id="c1c25-126">The default sampling mask is 0xffffffff which designates point sampling.</span></span>

<span data-ttu-id="c1c25-127">Na maioria dos esquemas de buffer mais detalhados, o pixel mais próximo da câmera é aquele que é desenhado.</span><span class="sxs-lookup"><span data-stu-id="c1c25-127">In most depth buffering schemes, the pixel closest to the camera is the one that gets drawn.</span></span> <span data-ttu-id="c1c25-128">Ao [Configurar o estado de estêncil de profundidade](d3d10-graphics-programming-guide-depth-stencil.md), o membro **DepthFunc** do [**estêncil de profundidade D3D11 \_ \_ \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc) pode ser qualquer [**D3D11 de \_ comparação \_ Func**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_comparison_func).</span><span class="sxs-lookup"><span data-stu-id="c1c25-128">When [setting up the depth stencil state](d3d10-graphics-programming-guide-depth-stencil.md), the **DepthFunc** member of [**D3D11\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc) can be any [**D3D11\_COMPARISON\_FUNC**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_comparison_func).</span></span> <span data-ttu-id="c1c25-129">Normalmente, você desejaria que **DepthFunc** fosse **D3D11 de \_ comparação \_**, para que os pixels mais próximos da câmera substituam os pixels por trás deles.</span><span class="sxs-lookup"><span data-stu-id="c1c25-129">Normally, you would want **DepthFunc** to be **D3D11\_COMPARISON\_LESS**, so that the pixels closest to the camera will overwrite the pixels behind them.</span></span> <span data-ttu-id="c1c25-130">No entanto, dependendo das necessidades do seu aplicativo, qualquer uma das outras funções de comparação pode ser usada para fazer o teste de profundidade.</span><span class="sxs-lookup"><span data-stu-id="c1c25-130">However, depending on the needs of your application, any of the other comparison functions may be used to do the depth test.</span></span>

## <a name="advanced-blending-topics"></a><span data-ttu-id="c1c25-131">Tópicos de mesclagem avançada</span><span class="sxs-lookup"><span data-stu-id="c1c25-131">Advanced Blending Topics</span></span>

-   [<span data-ttu-id="c1c25-132">De alfa para cobertura</span><span class="sxs-lookup"><span data-stu-id="c1c25-132">Alpha-To-Coverage</span></span>](#alpha-to-coverage)
-   [<span data-ttu-id="c1c25-133">Mesclagem de saídas de sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="c1c25-133">Blending Pixel Shader Outputs</span></span>](#blending-pixel-shader-outputs)

### <a name="alpha-to-coverage"></a><span data-ttu-id="c1c25-134">De alfa para cobertura</span><span class="sxs-lookup"><span data-stu-id="c1c25-134">Alpha-To-Coverage</span></span>

<span data-ttu-id="c1c25-135">Alfa-to-Coverage é uma técnica de várias amostras que é mais útil para situações como folhagem densas em que há vários polígonos sobrepostos que usam transparência alfa para definir bordas dentro da superfície.</span><span class="sxs-lookup"><span data-stu-id="c1c25-135">Alpha-to-coverage is a multisampling technique that is most useful for situations such as dense foliage where there are several overlapping polygons that use alpha transparency to define edges within the surface.</span></span>

<span data-ttu-id="c1c25-136">Você pode usar o membro **AlphaToCoverageEnable** do [**D3D11 \_ Blend \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_blend_desc1) ou [**D3D11 \_ Blend \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc) para alternar se o tempo de execução converte o. um componente (alfa) do registro de saída [VA de \_ destino](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)0 do sombreador de pixel para uma máscara de cobertura de n etapas (dada um **renderTarget** de n amostras).</span><span class="sxs-lookup"><span data-stu-id="c1c25-136">You can use the **AlphaToCoverageEnable** member of [**D3D11\_BLEND\_DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_blend_desc1) or [**D3D11\_BLEND\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc) to toggle whether the runtime converts the .a component (alpha) of output register [SV\_Target](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)0 from the pixel shader to an n-step coverage mask (given an n-sample **RenderTarget**).</span></span> <span data-ttu-id="c1c25-137">O tempo de execução executa uma operação **and** dessa máscara com a cobertura de exemplo típica para o pixel na primitiva (além da máscara de exemplo) para determinar quais amostras atualizar em todos os **renderTarget** s ativos.</span><span class="sxs-lookup"><span data-stu-id="c1c25-137">The runtime performs an **AND** operation of this mask with the typical sample coverage for the pixel in the primitive (in addition to the sample mask) to determine which samples to update in all the active **RenderTarget** s.</span></span>

<span data-ttu-id="c1c25-138">Se o sombreador de pixel gerar a [ \_ cobertura da VA](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics), o tempo de execução desabilitará alfa para cobertura.</span><span class="sxs-lookup"><span data-stu-id="c1c25-138">If the pixel shader outputs [SV\_Coverage](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics), the runtime disables alpha-to-coverage.</span></span>

> [!Note]  
> <span data-ttu-id="c1c25-139">Em multiamostragens, o tempo de execução compartilha apenas uma cobertura para todos os **renderTarget** s.</span><span class="sxs-lookup"><span data-stu-id="c1c25-139">In multisampling, the runtime shares only one coverage for all **RenderTarget** s.</span></span> <span data-ttu-id="c1c25-140">O fato de que o tempo de execução lê e converte. a da saída [VA de \_ destino](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)0 para cobertura quando **AlphaToCoverageEnable** é true não altera o. um valor que vai para o Blender em **renderTarget** 0 (se um **renderTarget** for definido aqui).</span><span class="sxs-lookup"><span data-stu-id="c1c25-140">The fact that the runtime reads and converts .a from output [SV\_Target](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)0 to coverage when **AlphaToCoverageEnable** is TRUE does not change the .a value that goes to the blender at **RenderTarget** 0 (if a **RenderTarget** happens to be set there).</span></span> <span data-ttu-id="c1c25-141">Em geral, se você habilitar a Alpha-to-Coverage, não afetará como todas as saídas de cores de sombreadores de pixel interagem com **renderTarget** s por meio do [estágio de mesclagem de saída](d3d10-graphics-programming-guide-output-merger-stage.md) , exceto que o tempo de execução executa uma operação **and** da máscara de cobertura com a máscara de alfa para cobertura.</span><span class="sxs-lookup"><span data-stu-id="c1c25-141">In general, if you enable alpha-to-coverage, you don't affect how all color outputs from pixel shaders interact with **RenderTarget** s through the [output-merger stage](d3d10-graphics-programming-guide-output-merger-stage.md) except that the runtime performs an **AND** operation of the coverage mask with the alpha-to-coverage mask.</span></span> <span data-ttu-id="c1c25-142">Alfa-to-Coverage funciona de forma independente se o tempo de execução pode misturar **renderTarget** ou se você usa a mesclagem em **renderTarget**.</span><span class="sxs-lookup"><span data-stu-id="c1c25-142">Alpha-to-coverage works independently to whether the runtime can blend **RenderTarget** or whether you use blending on **RenderTarget**.</span></span>

 

<span data-ttu-id="c1c25-143">O hardware de gráficos não especifica precisamente exatamente como converte o pixel shader [VA \_ target](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)0. a (Alpha) em uma máscara de cobertura, exceto que alfa de 0 (ou menos) deve mapear para sem cobertura e alfa de 1 (ou superior) deve mapear para cobertura completa (antes de o tempo de execução executar uma operação **and** com cobertura primitiva real).</span><span class="sxs-lookup"><span data-stu-id="c1c25-143">Graphics hardware doesn't precisely specify exactly how it converts pixel shader [SV\_Target](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)0.a (alpha) to a coverage mask, except that alpha of 0 (or less) must map to no coverage and alpha of 1 (or greater) must map to full coverage (before the runtime performs an **AND** operation with actual primitive coverage).</span></span> <span data-ttu-id="c1c25-144">Como Alfa vai de 0 a 1, a cobertura resultante geralmente aumenta de forma monotônico.</span><span class="sxs-lookup"><span data-stu-id="c1c25-144">As alpha goes from 0 to 1, the resulting coverage should generally increase monotonically.</span></span> <span data-ttu-id="c1c25-145">No entanto, o hardware pode executar o pontilhamento de área para fornecer uma melhor quantificação de valores Alfa ao custo da resolução espacial e do ruído.</span><span class="sxs-lookup"><span data-stu-id="c1c25-145">However, hardware might perform area dithering to provide some better quantization of alpha values at the cost of spatial resolution and noise.</span></span> <span data-ttu-id="c1c25-146">Um valor alfa de NaN (não um número) resulta em uma máscara sem cobertura (zero).</span><span class="sxs-lookup"><span data-stu-id="c1c25-146">An alpha value of NaN (Not a Number) results in a no coverage (zero) mask.</span></span>

<span data-ttu-id="c1c25-147">A Alpha-to-Coverage também é tradicionalmente usada para transparência da porta de tela ou definindo silhuetas detalhadas para sprites opacos de outra forma.</span><span class="sxs-lookup"><span data-stu-id="c1c25-147">Alpha-to-coverage is also traditionally used for screen-door transparency or defining detailed silhouettes for otherwise opaque sprites.</span></span>

### <a name="blending-pixel-shader-outputs"></a><span data-ttu-id="c1c25-148">Mesclagem de saídas de sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="c1c25-148">Blending Pixel Shader Outputs</span></span>

<span data-ttu-id="c1c25-149">Esse recurso permite que a mesclagem de saída use as saídas do sombreador de pixel simultaneamente como fontes de entrada para uma operação de mesclagem com o destino de renderização único no slot 0.</span><span class="sxs-lookup"><span data-stu-id="c1c25-149">This feature enables the output merger to use both the pixel shader outputs simultaneously as input sources to a blending operation with the single render target at slot 0.</span></span>

<span data-ttu-id="c1c25-150">Este exemplo usa dois resultados e os combina em uma única passagem, combinando um no destino com uma multiplicação e o outro com um add:</span><span class="sxs-lookup"><span data-stu-id="c1c25-150">This example takes two results and combines them in a single pass, blending one into the destination with a multiply and the other with an add:</span></span>


```
SrcBlend = D3D11_BLEND_ONE;
DestBlend = D3D11_BLEND_SRC1_COLOR;
```



<span data-ttu-id="c1c25-151">Este exemplo configura a primeira saída do sombreador de pixel como a cor de origem e a segunda saída como um fator de mistura de componente por cor.</span><span class="sxs-lookup"><span data-stu-id="c1c25-151">This example configures the first pixel shader output as the source color and the second output as a per-color component blend factor.</span></span>


```
SrcBlend = D3D11_BLEND_SRC1_COLOR;
DestBlend = D3D11_BLEND_INV_SRC1_COLOR;
```



<span data-ttu-id="c1c25-152">Este exemplo ilustra como os fatores de mistura devem corresponder ao sombreador swizzles:</span><span class="sxs-lookup"><span data-stu-id="c1c25-152">This example illustrates how the blend factors must match the shader swizzles:</span></span>


```
SrcFactor = D3D11_BLEND_SRC1_ALPHA;
DestFactor = D3D11_BLEND_SRC_COLOR;
OutputWriteMask[0] = .ra; // pseudocode for setting the mask at
                          // RenderTarget slot 0 to .ra
```



<span data-ttu-id="c1c25-153">Juntos, os fatores de mistura e o código do sombreador sugerem que o sombreador de pixel é necessário para produzir pelo menos o0. r e o1. a.</span><span class="sxs-lookup"><span data-stu-id="c1c25-153">Together, the blend factors and the shader code imply that the pixel shader is required to output at least o0.r and o1.a.</span></span> <span data-ttu-id="c1c25-154">Os componentes de saída extra podem ser gerados pelo sombreador, mas seriam ignorados, menos componentes produzirão resultados indefinidos.</span><span class="sxs-lookup"><span data-stu-id="c1c25-154">Extra output components can be output by the shader but would be ignored, fewer components would produce undefined results.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c1c25-155">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c1c25-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1c25-156">Estágio de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="c1c25-156">Output-Merger Stage</span></span>](d3d10-graphics-programming-guide-output-merger-stage.md)
</dt> <dt>

[<span data-ttu-id="c1c25-157">Estágios de pipeline (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="c1c25-157">Pipeline Stages (Direct3D 10)</span></span>](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

 