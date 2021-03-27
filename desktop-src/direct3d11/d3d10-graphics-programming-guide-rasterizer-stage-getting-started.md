---
title: Introdução com o estágio rasterizador
description: Esta seção descreve como definir o visor, o retângulo de tesoura, o estado do rasterizador e a várias amostras.
ms.assetid: d78c3845-76fd-4bd7-a603-bb1d8c66ac49
keywords:
- multiamostrando, estado do rasterizador (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac95a15221f6fd4bd422e96c0686816afb35d4e8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294086"
---
# <a name="getting-started-with-the-rasterizer-stage"></a><span data-ttu-id="1d58b-104">Introdução com o estágio rasterizador</span><span class="sxs-lookup"><span data-stu-id="1d58b-104">Getting Started with the Rasterizer Stage</span></span>

<span data-ttu-id="1d58b-105">Esta seção descreve como definir o visor, o retângulo de tesoura, o estado do rasterizador e a várias amostras.</span><span class="sxs-lookup"><span data-stu-id="1d58b-105">This section describes setting the viewport, the scissors rectangle, the rasterizer state, and multi-sampling.</span></span>

## <a name="set-the-viewport"></a><span data-ttu-id="1d58b-106">Definir o visor</span><span class="sxs-lookup"><span data-stu-id="1d58b-106">Set the Viewport</span></span>

<span data-ttu-id="1d58b-107">Um visor mapeia as posições de vértice (no espaço de clipe) para processar posições de destino.</span><span class="sxs-lookup"><span data-stu-id="1d58b-107">A viewport maps vertex positions (in clip space) into render target positions.</span></span> <span data-ttu-id="1d58b-108">Esta etapa dimensiona as posições 3D em espaço 2D.</span><span class="sxs-lookup"><span data-stu-id="1d58b-108">This step scales the 3D positions into 2D space.</span></span> <span data-ttu-id="1d58b-109">Um destino de renderização é orientado com os eixos Y apontando para baixo; Isso requer que as coordenadas Y sejam invertidas durante a escala do visor.</span><span class="sxs-lookup"><span data-stu-id="1d58b-109">A render target is oriented with the Y axes pointing down; this requires that the Y coordinates get flipped during the viewport scale.</span></span> <span data-ttu-id="1d58b-110">Além disso, as extensões x e y (intervalo dos valores x e y) são dimensionadas para se ajustarem ao tamanho do visor de acordo com as fórmulas a seguir:</span><span class="sxs-lookup"><span data-stu-id="1d58b-110">In addition, the x and y extents (range of the x and y values) are scaled to fit the viewport size according to the following formulas:</span></span>


```
X = (X + 1) * Viewport.Width * 0.5 + Viewport.TopLeftX
Y = (1 - Y) * Viewport.Height * 0.5 + Viewport.TopLeftY
Z = Viewport.MinDepth + Z * (Viewport.MaxDepth - Viewport.MinDepth) 
```



<span data-ttu-id="1d58b-111">O tutorial 1 cria um visor 640 × 480 usando o [**\_ visor D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_viewport) e chamando [**ID3D11DeviceContext:: RSSetViewports**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetviewports).</span><span class="sxs-lookup"><span data-stu-id="1d58b-111">Tutorial 1 creates a 640 × 480 viewport using [**D3D11\_VIEWPORT**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_viewport) and by calling [**ID3D11DeviceContext::RSSetViewports**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetviewports).</span></span>


```
    D3D11_VIEWPORT vp[1];
    vp[0].Width = 640.0f;
    vp[0].Height = 480.0f;
    vp[0].MinDepth = 0;
    vp[0].MaxDepth = 1;
    vp[0].TopLeftX = 0;
    vp[0].TopLeftY = 0;
    g_pd3dDevice->RSSetViewports( 1, vp );
```



<span data-ttu-id="1d58b-112">A descrição do visor especifica o tamanho do visor, o intervalo para mapear profundidade (usando *MinDepth* e *MaxDepth*) e o posicionamento da parte superior esquerda do visor.</span><span class="sxs-lookup"><span data-stu-id="1d58b-112">The viewport description specifies the size of the viewport, the range to map depth to (using *MinDepth* and *MaxDepth*), and the placement of the top left of the viewport.</span></span> <span data-ttu-id="1d58b-113">*MinDepth* deve ser menor ou igual a *MaxDepth*; o intervalo para *MinDepth* e *MaxDepth* está entre 0,0 e 1,0, inclusive.</span><span class="sxs-lookup"><span data-stu-id="1d58b-113">*MinDepth* must be less than or equal to *MaxDepth*; the range for both *MinDepth* and *MaxDepth* is between 0.0 and 1.0, inclusive.</span></span> <span data-ttu-id="1d58b-114">É comum que o visor mapeie para um destino de renderização, mas não é necessário; Além disso, o visor não precisa ter o mesmo tamanho ou posição que o destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="1d58b-114">It is common for the viewport to map to a render target but it is not necessary; additionally, the viewport does not have to have the same size or position as the render target.</span></span>

<span data-ttu-id="1d58b-115">Você pode criar uma matriz de visores, mas apenas um pode ser aplicado a uma saída primitiva do sombreador de geometria.</span><span class="sxs-lookup"><span data-stu-id="1d58b-115">You can create an array of viewports, but only one can be applied to a primitive output from the geometry shader.</span></span> <span data-ttu-id="1d58b-116">Somente um visor pode ser definido de modo ativo por vez.</span><span class="sxs-lookup"><span data-stu-id="1d58b-116">Only one viewport can be set active at a time.</span></span> <span data-ttu-id="1d58b-117">O pipeline usa um visor padrão (e um retângulo de mola, discutido na próxima seção) durante a rasterização.</span><span class="sxs-lookup"><span data-stu-id="1d58b-117">The pipeline uses a default viewport (and scissor rectangle, discussed in the next section) during rasterization.</span></span> <span data-ttu-id="1d58b-118">O padrão é sempre o primeiro visor (ou retângulo de mola) na matriz.</span><span class="sxs-lookup"><span data-stu-id="1d58b-118">The default is always the first viewport (or scissor rectangle) in the array.</span></span> <span data-ttu-id="1d58b-119">Para executar uma seleção por primitiva do visor no sombreador Geometry, especifique a semântica ViewportArrayIndex no componente de saída GS apropriado na declaração de assinatura de saída GS.</span><span class="sxs-lookup"><span data-stu-id="1d58b-119">To perform a per-primitive selection of the viewport in the geometry shader, specify the ViewportArrayIndex semantic on the appropriate GS output component in the GS output signature declaration.</span></span>

<span data-ttu-id="1d58b-120">O número máximo de visores (e retângulos de recorte) que podem ser vinculados ao estágio de rasterizador a qualquer momento é 16 (especificado pelo **\_ visor D3D11 \_ e \_ contagem de \_ objetos SCISSORRECT \_ \_ por \_ pipeline**).</span><span class="sxs-lookup"><span data-stu-id="1d58b-120">The maximum number of viewports (and scissor rectangles) that can be bound to the rasterizer stage at any one time is 16 (specified by **D3D11\_VIEWPORT\_AND\_SCISSORRECT\_OBJECT\_COUNT\_PER\_PIPELINE**).</span></span>

## <a name="set-the-scissor-rectangle"></a><span data-ttu-id="1d58b-121">Definir o retângulo da mola</span><span class="sxs-lookup"><span data-stu-id="1d58b-121">Set the Scissor Rectangle</span></span>

<span data-ttu-id="1d58b-122">Um retângulo de recorte dá a você outra oportunidade de reduzir o número de pixels que serão enviados para o estágio de fusão de saída.</span><span class="sxs-lookup"><span data-stu-id="1d58b-122">A scissor rectangle gives you another opportunity to reduce the number of pixels that will be sent to the output merger stage.</span></span> <span data-ttu-id="1d58b-123">Os pixels fora do retângulo da mola são descartados.</span><span class="sxs-lookup"><span data-stu-id="1d58b-123">Pixels outside of the scissor rectangle are discarded.</span></span> <span data-ttu-id="1d58b-124">O tamanho do retângulo da mola é especificado em inteiros.</span><span class="sxs-lookup"><span data-stu-id="1d58b-124">The size of the scissor rectangle is specified in integers.</span></span> <span data-ttu-id="1d58b-125">Somente um retângulo de recorte (baseado em *ViewportArrayIndex* na [semântica de valor do sistema](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)) pode ser aplicado a um triângulo durante a rasterização.</span><span class="sxs-lookup"><span data-stu-id="1d58b-125">Only one scissor rectangle (based on *ViewportArrayIndex* in [system value semantics](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)) can be applied to a triangle during rasterization.</span></span>

<span data-ttu-id="1d58b-126">Para habilitar o retângulo de mola, use o membro *ScissorEnable* (no [**D3D11 \_ rasterizador \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1)).</span><span class="sxs-lookup"><span data-stu-id="1d58b-126">To enable the scissor rectangle, use the *ScissorEnable* member (in [**D3D11\_RASTERIZER\_DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1)).</span></span> <span data-ttu-id="1d58b-127">O retângulo de tesoura padrão é um retângulo vazio; ou seja, todos os valores de RECT são 0.</span><span class="sxs-lookup"><span data-stu-id="1d58b-127">The default scissor rectangle is an empty rectangle; that is, all rect values are 0.</span></span> <span data-ttu-id="1d58b-128">Em outras palavras, se você não configurar o retângulo de corte e a tesoura estiver habilitada, você não enviará nenhum pixel para o estágio de mesclagem de saída.</span><span class="sxs-lookup"><span data-stu-id="1d58b-128">In other words, if you do not set up the scissor rectangle and scissor is enabled, you will not send any pixels to the output-merger stage.</span></span> <span data-ttu-id="1d58b-129">A configuração mais comum é inicializar o retângulo de mola até o tamanho do visor.</span><span class="sxs-lookup"><span data-stu-id="1d58b-129">The most common setup is to initialize the scissor rectangle to the size of the viewport.</span></span>

<span data-ttu-id="1d58b-130">Para definir uma matriz de retângulos de mola para o dispositivo, chame [**ID3D11DeviceContext:: RSSetScissorRects**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetscissorrects) com [**D3D11 \_ Rect**](d3d11-rect.md).</span><span class="sxs-lookup"><span data-stu-id="1d58b-130">To set an array of scissor rectangles to the device, call [**ID3D11DeviceContext::RSSetScissorRects**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetscissorrects) with [**D3D11\_RECT**](d3d11-rect.md).</span></span>


```
D3D11_RECT rects[1];
  rects[0].left = 0;
  rects[0].right = 640;
  rects[0].top = 0;
  rects[0].bottom = 480;

  D3DDevice->RSSetScissorRects( 1, rects );
```



<span data-ttu-id="1d58b-131">Esse método usa dois parâmetros: (1) o número de retângulos na matriz e (2) uma matriz de retângulos.</span><span class="sxs-lookup"><span data-stu-id="1d58b-131">This method takes two parameters: (1) the number of rectangles in the array and (2) an array of rectangles.</span></span>

<span data-ttu-id="1d58b-132">O pipeline usa um índice de retângulo de tesoura padrão durante a rasterização (o padrão é um retângulo de tamanho zero com recorte desabilitado).</span><span class="sxs-lookup"><span data-stu-id="1d58b-132">The pipeline uses a default scissor rectangle index during rasterization (the default is a zero-size rectangle with clipping disabled).</span></span> <span data-ttu-id="1d58b-133">Para substituir isso, especifique a \_ semântica ViewportArrayIndex de VA para um componente de saída GS na declaração de assinatura de saída GS.</span><span class="sxs-lookup"><span data-stu-id="1d58b-133">To override this, specify the SV\_ViewportArrayIndex semantic to a GS output component in the GS output signature declaration.</span></span> <span data-ttu-id="1d58b-134">Isso fará com que o estágio GS marque esse componente de saída GS como um componente gerado pelo sistema com essa semântica.</span><span class="sxs-lookup"><span data-stu-id="1d58b-134">This will cause the GS stage to mark this GS output component as a system-generated component with this semantic.</span></span> <span data-ttu-id="1d58b-135">O estágio rasterizador reconhece essa semântica e usará o parâmetro ao qual ele está anexado como o índice de retângulo de mola para acessar a matriz de retângulos de recorte.</span><span class="sxs-lookup"><span data-stu-id="1d58b-135">The rasterizer stage recognizes this semantic and will use the parameter it is attached to as the scissor rectangle index to access the array of scissor rectangles.</span></span> <span data-ttu-id="1d58b-136">Não se esqueça de instruir o estágio de rasterizador a usar o retângulo de recorte definido por meio da habilitação do valor *ScissorEnable* na descrição do rasterizador antes de criar o objeto rasterizador.</span><span class="sxs-lookup"><span data-stu-id="1d58b-136">Don't forget to tell the rasterizer stage to use the scissor rectangle that you define by enabling the *ScissorEnable* value in the rasterizer description before creating the rasterizer object.</span></span>

## <a name="set-rasterizer-state"></a><span data-ttu-id="1d58b-137">Definir estado do rasterizador</span><span class="sxs-lookup"><span data-stu-id="1d58b-137">Set Rasterizer State</span></span>

<span data-ttu-id="1d58b-138">Começando com o Direct3D 10, o estado do rasterizador é encapsulado em um objeto de estado do rasterizador.</span><span class="sxs-lookup"><span data-stu-id="1d58b-138">Beginning with Direct3D 10, rasterizer state is encapsulated in a rasterizer state object.</span></span> <span data-ttu-id="1d58b-139">Você pode criar até 4096 objetos de estado do rasterizador que podem ser definidos para o dispositivo passando um identificador para o objeto de estado.</span><span class="sxs-lookup"><span data-stu-id="1d58b-139">You may create up to 4096 rasterizer state objects which can then be set to the device by passing a handle to the state object.</span></span>

<span data-ttu-id="1d58b-140">Use [**ID3D11Device1:: CreateRasterizerState1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createrasterizerstate1) para criar um objeto de estado do rasterizador a partir de uma descrição do rasterizador (consulte [**D3D11 do \_ rasterizador \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1)).</span><span class="sxs-lookup"><span data-stu-id="1d58b-140">Use [**ID3D11Device1::CreateRasterizerState1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createrasterizerstate1) to create a rasterizer state object from a rasterizer description (see [**D3D11\_RASTERIZER\_DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1)).</span></span>


```
    ID3D11RasterizerState1 * g_pRasterState;

    D3D11_RASTERIZER_DESC1 rasterizerState;
    rasterizerState.FillMode = D3D11_FILL_SOLID;
    rasterizerState.CullMode = D3D11_CULL_FRONT;
    rasterizerState.FrontCounterClockwise = true;
    rasterizerState.DepthBias = false;
    rasterizerState.DepthBiasClamp = 0;
    rasterizerState.SlopeScaledDepthBias = 0;
    rasterizerState.DepthClipEnable = true;
    rasterizerState.ScissorEnable = true;
    rasterizerState.MultisampleEnable = false;
    rasterizerState.AntialiasedLineEnable = false;
    rasterizerState.ForcedSampleCount = 0;
    pd3dDevice->CreateRasterizerState1( &rasterizerState, &g_pRasterState );
```



<span data-ttu-id="1d58b-141">Esse conjunto de exemplo de estado realiza talvez a configuração mais básica do rasterizador:</span><span class="sxs-lookup"><span data-stu-id="1d58b-141">This example set of state accomplishes perhaps the most basic rasterizer setup:</span></span>

-   <span data-ttu-id="1d58b-142">Modo de preenchimento sólido</span><span class="sxs-lookup"><span data-stu-id="1d58b-142">Solid fill mode</span></span>
-   <span data-ttu-id="1d58b-143">Excluir ou remover faces traseiras; assumir a ordem de enrolamento no sentido anti-horário para primitivos</span><span class="sxs-lookup"><span data-stu-id="1d58b-143">Cull out or remove back faces; assume counter-clockwise winding order for primitives</span></span>
-   <span data-ttu-id="1d58b-144">Desativar a tendência de profundidade, mas habilitar o buffer de profundidade e habilitar o retângulo de mola</span><span class="sxs-lookup"><span data-stu-id="1d58b-144">Turn off depth bias but enable depth buffering and enable the scissor rectangle</span></span>
-   <span data-ttu-id="1d58b-145">Desligar a multiamostra e a suavização de linha</span><span class="sxs-lookup"><span data-stu-id="1d58b-145">Turn off multisampling and line anti-aliasing</span></span>

<span data-ttu-id="1d58b-146">Além disso, as operações básicas do rasterizador, sempre incluem o seguinte: recorte (para a exibição frustum), divisão em perspectiva e escala do visor.</span><span class="sxs-lookup"><span data-stu-id="1d58b-146">In addition, basic rasterizer operations, always include the following: clipping (to the view frustum), perspective divide, and the viewport scale.</span></span> <span data-ttu-id="1d58b-147">Depois de criar com êxito o objeto de estado do rasterizador, defina-o para o dispositivo da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="1d58b-147">After successfully creating the rasterizer state object, set it to the device like this:</span></span>


```
    pd3dDevice->RSSetState(g_pRasterState);
```



### <a name="multisampling"></a><span data-ttu-id="1d58b-148">Amostragem múltipla</span><span class="sxs-lookup"><span data-stu-id="1d58b-148">Multisampling</span></span>

<span data-ttu-id="1d58b-149">As amostras de multiamostragem são alguns ou todos os componentes de uma imagem em uma resolução mais alta (seguida pela redução da resolução original) para reduzir a forma mais visível de alias causada pelo desenho de bordas do polígono.</span><span class="sxs-lookup"><span data-stu-id="1d58b-149">Multisampling samples some or all of the components of an image at a higher resolution (followed by downsampling to the original resolution) to reduce the most visible form of aliasing caused by drawing polygon edges.</span></span> <span data-ttu-id="1d58b-150">Embora a multiamostração exija amostras de sub-pixel, a GPU moderna implementa multiamostrar para que um sombreador de pixel seja executado uma vez por pixel.</span><span class="sxs-lookup"><span data-stu-id="1d58b-150">Even though multisampling requires sub-pixel samples, modern GPU's implement multisampling so that a pixel shader runs once per pixel.</span></span> <span data-ttu-id="1d58b-151">Isso fornece uma compensação aceitável entre o desempenho (especialmente em um aplicativo vinculado à GPU) e a suavização da imagem final.</span><span class="sxs-lookup"><span data-stu-id="1d58b-151">This provides an acceptable tradeoff between performance (especially in a GPU bound application) and anti-aliasing the final image.</span></span>

<span data-ttu-id="1d58b-152">Para usar a multiamostragem, defina o campo habilitar na [**Descrição da rasterização**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1), crie um destino de renderização com uma amostra e leia o destino de renderização com um sombreador para resolver os exemplos em uma única cor de pixel ou chame [**ID3D11DeviceContext:: ResolveSubresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-resolvesubresource) para resolver os exemplos usando a placa de vídeo.</span><span class="sxs-lookup"><span data-stu-id="1d58b-152">To use multisampling, set the enable field in the [**rasterization description**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1), create a multisampled render target, and either read the render target with a shader to resolve the samples into a single pixel color or call [**ID3D11DeviceContext::ResolveSubresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-resolvesubresource) to resolve the samples using the video card.</span></span> <span data-ttu-id="1d58b-153">O cenário mais comum é desenhar para um ou mais destinos de renderização multiamostrados.</span><span class="sxs-lookup"><span data-stu-id="1d58b-153">The most common scenario is to draw to one or more multisampled render targets.</span></span>

<span data-ttu-id="1d58b-154">A multiamostragem é independente de ser usada ou não por uma máscara de exemplo, o [alfa-to-Coverage](d3d10-graphics-programming-guide-blend-state.md) é habilitado ou as operações de estêncil (que são sempre executadas por amostra).</span><span class="sxs-lookup"><span data-stu-id="1d58b-154">Multisampling is independent of whether or not a sample mask is used, [alpha-to-coverage](d3d10-graphics-programming-guide-blend-state.md) is enabled, or stencil operations (which are always performed per-sample).</span></span>

<span data-ttu-id="1d58b-155">O teste de profundidade é afetado por multiamostragem:</span><span class="sxs-lookup"><span data-stu-id="1d58b-155">Depth testing is affected by multisampling:</span></span>

-   <span data-ttu-id="1d58b-156">Quando a multiamostragem está habilitada, a profundidade é interpolada por amostra e o teste de profundidade/estêncil é feito por amostra; a cor de saída do sombreador de pixel é duplicada para todos os exemplos de passagem.</span><span class="sxs-lookup"><span data-stu-id="1d58b-156">When multisampling is enabled, depth is interpolated per sample and the depth/stencil test is done per sample; the pixel shader output color is duplicated for all passing samples.</span></span> <span data-ttu-id="1d58b-157">Se o sombreador de pixel gerar profundidade, o valor de profundidade será duplicado para todos os exemplos (embora esse cenário perca o benefício de uma multiamostragem).</span><span class="sxs-lookup"><span data-stu-id="1d58b-157">If the pixel shader outputs depth, the depth value is duplicated for all samples (although this scenario loses the benefit of multisampling).</span></span>
-   <span data-ttu-id="1d58b-158">Quando a multiamostração está desabilitada, o teste de profundidade/estêncil ainda é feito por amostra, mas a profundidade não é interpolada por amostra.</span><span class="sxs-lookup"><span data-stu-id="1d58b-158">When multisampling is disabled, depth/stencil testing is still done per-sample, but depth is not interpolated per-sample.</span></span>

<span data-ttu-id="1d58b-159">Não há restrições para misturar renderização de multiamostra e sem amostra em um único destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="1d58b-159">There are no restrictions for mixing multisampled and non-multisampled rendering within a single render target.</span></span> <span data-ttu-id="1d58b-160">Se você habilitar a multiamostrar e desenhar para um destino de renderização não multiamostrado, produzirá o mesmo resultado que se a multiamostragem não estivesse habilitada; a amostragem é feita com um único exemplo por pixel.</span><span class="sxs-lookup"><span data-stu-id="1d58b-160">If you enable multisampling and draw to a non-multisampled render target, you produce the same result as if multisampling were not enabled; sampling is done with a single sample per-pixel.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1d58b-161">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1d58b-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d58b-162">Estágio de rasterizador</span><span class="sxs-lookup"><span data-stu-id="1d58b-162">Rasterizer Stage</span></span>](d3d10-graphics-programming-guide-rasterizer-stage.md)
</dt> </dl>

 

 