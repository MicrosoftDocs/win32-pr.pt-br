---
title: Configurando Depth-Stencil funcionalidade
description: Esta seção abrange as etapas para configurar o buffer de estêncil de profundidade e o estado de estêncil de profundidade para o estágio de fusão de saída.
ms.assetid: e8f52d5f-266f-4e2c-b38d-d7fd9e27fe1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65bf48b0ba9a782be25568ac3fc0569314dae76e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641460"
---
# <a name="configuring-depth-stencil-functionality"></a><span data-ttu-id="8d5e9-103">Configurando Depth-Stencil funcionalidade</span><span class="sxs-lookup"><span data-stu-id="8d5e9-103">Configuring Depth-Stencil Functionality</span></span>

<span data-ttu-id="8d5e9-104">Esta seção abrange as etapas para configurar o buffer de estêncil de profundidade e o estado de estêncil de profundidade para o estágio de fusão de saída.</span><span class="sxs-lookup"><span data-stu-id="8d5e9-104">This section covers the steps for setting up the depth-stencil buffer, and depth-stencil state for the output-merger stage.</span></span>

-   [<span data-ttu-id="8d5e9-105">Criar um recurso de Depth-Stencil</span><span class="sxs-lookup"><span data-stu-id="8d5e9-105">Create a Depth-Stencil Resource</span></span>](#create-a-depth-stencil-resource)
-   [<span data-ttu-id="8d5e9-106">Criar Depth-Stencil estado</span><span class="sxs-lookup"><span data-stu-id="8d5e9-106">Create Depth-Stencil State</span></span>](#create-depth-stencil-state)
-   [<span data-ttu-id="8d5e9-107">Associar dados de Depth-Stencil ao estágio de OM</span><span class="sxs-lookup"><span data-stu-id="8d5e9-107">Bind Depth-Stencil Data to the OM Stage</span></span>](#bind-depth-stencil-data-to-the-om-stage)

<span data-ttu-id="8d5e9-108">Assim que você souber como usar o buffer de estêncil de profundidade e o estado de estêncil de profundidade correspondente, consulte [técnicas avançadas de estêncil](#advanced-stencil-techniques).</span><span class="sxs-lookup"><span data-stu-id="8d5e9-108">Once you know how to use the depth-stencil buffer and the corresponding depth-stencil state, refer to [advanced-stencil techniques](#advanced-stencil-techniques).</span></span>

## <a name="create-a-depth-stencil-resource"></a><span data-ttu-id="8d5e9-109">Criar um recurso de Depth-Stencil</span><span class="sxs-lookup"><span data-stu-id="8d5e9-109">Create a Depth-Stencil Resource</span></span>

<span data-ttu-id="8d5e9-110">Crie o buffer de estêncil de profundidade usando um recurso de textura.</span><span class="sxs-lookup"><span data-stu-id="8d5e9-110">Create the depth-stencil buffer using a texture resource.</span></span>


```
ID3D11Texture2D* pDepthStencil = NULL;
D3D11_TEXTURE2D_DESC descDepth;
descDepth.Width = backBufferSurfaceDesc.Width;
descDepth.Height = backBufferSurfaceDesc.Height;
descDepth.MipLevels = 1;
descDepth.ArraySize = 1;
descDepth.Format = pDeviceSettings->d3d11.AutoDepthStencilFormat;
descDepth.SampleDesc.Count = 1;
descDepth.SampleDesc.Quality = 0;
descDepth.Usage = D3D11_USAGE_DEFAULT;
descDepth.BindFlags = D3D11_BIND_DEPTH_STENCIL;
descDepth.CPUAccessFlags = 0;
descDepth.MiscFlags = 0;
hr = pd3dDevice->CreateTexture2D( &descDepth, NULL, &pDepthStencil );
```



## <a name="create-depth-stencil-state"></a><span data-ttu-id="8d5e9-111">Criar estado de estêncil de profundidade</span><span class="sxs-lookup"><span data-stu-id="8d5e9-111">Create Depth-Stencil State</span></span>

<span data-ttu-id="8d5e9-112">O estado de estêncil de profundidade informa o estágio de fusão de saída sobre como realizar o [teste de profundidade e estêncil](d3d10-graphics-programming-guide-output-merger-stage.md).</span><span class="sxs-lookup"><span data-stu-id="8d5e9-112">The depth-stencil state tells the output-merger stage how to perform the [depth-stencil test](d3d10-graphics-programming-guide-output-merger-stage.md).</span></span> <span data-ttu-id="8d5e9-113">O teste de profundidade e estêncil determina se um determinado pixel deve ser desenhado.</span><span class="sxs-lookup"><span data-stu-id="8d5e9-113">The depth-stencil test determines whether or not a given pixel should be drawn.</span></span>


```
D3D11_DEPTH_STENCIL_DESC dsDesc;

// Depth test parameters
dsDesc.DepthEnable = true;
dsDesc.DepthWriteMask = D3D11_DEPTH_WRITE_MASK_ALL;
dsDesc.DepthFunc = D3D11_COMPARISON_LESS;

// Stencil test parameters
dsDesc.StencilEnable = true;
dsDesc.StencilReadMask = 0xFF;
dsDesc.StencilWriteMask = 0xFF;

// Stencil operations if pixel is front-facing
dsDesc.FrontFace.StencilFailOp = D3D11_STENCIL_OP_KEEP;
dsDesc.FrontFace.StencilDepthFailOp = D3D11_STENCIL_OP_INCR;
dsDesc.FrontFace.StencilPassOp = D3D11_STENCIL_OP_KEEP;
dsDesc.FrontFace.StencilFunc = D3D11_COMPARISON_ALWAYS;

// Stencil operations if pixel is back-facing
dsDesc.BackFace.StencilFailOp = D3D11_STENCIL_OP_KEEP;
dsDesc.BackFace.StencilDepthFailOp = D3D11_STENCIL_OP_DECR;
dsDesc.BackFace.StencilPassOp = D3D11_STENCIL_OP_KEEP;
dsDesc.BackFace.StencilFunc = D3D11_COMPARISON_ALWAYS;

// Create depth stencil state
ID3D11DepthStencilState * pDSState;
pd3dDevice->CreateDepthStencilState(&dsDesc, &pDSState);
```



<span data-ttu-id="8d5e9-114">DepthEnable e StencilEnable habilitam (e desabilitam) o teste de profundidade e de estêncil.</span><span class="sxs-lookup"><span data-stu-id="8d5e9-114">DepthEnable and StencilEnable enable (and disable) depth and stencil testing.</span></span> <span data-ttu-id="8d5e9-115">Defina DepthEnable como **false** para desabilitar o teste de profundidade e impedir a gravação no buffer de profundidade.</span><span class="sxs-lookup"><span data-stu-id="8d5e9-115">Set DepthEnable to **FALSE** to disable depth testing and prevent writing to the depth buffer.</span></span> <span data-ttu-id="8d5e9-116">Defina StencilEnable como **false** para desabilitar o teste de estêncil e impedir a gravação no buffer de estêncil (quando DepthEnable for **false** e StencilEnable for **true**, o teste de profundidade sempre passa na operação de estêncil).</span><span class="sxs-lookup"><span data-stu-id="8d5e9-116">Set StencilEnable to **FALSE** to disable stencil testing and prevent writing to the stencil buffer (when DepthEnable is **FALSE** and StencilEnable is **TRUE**, the depth test always passes in the stencil operation).</span></span>

<span data-ttu-id="8d5e9-117">O DepthEnable só afeta o estágio de mesclagem de saída-ele não afeta recorte, tendência de profundidade ou fixação MSS de valores antes que os dados sejam inseridos em um sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="8d5e9-117">DepthEnable only affects the output-merger stage - it does not affect clipping, depth bias, or clamping of values before the data is input to a pixel shader.</span></span>

## <a name="bind-depth-stencil-data-to-the-om-stage"></a><span data-ttu-id="8d5e9-118">Associar dados de estêncil de profundidade ao estágio de OM</span><span class="sxs-lookup"><span data-stu-id="8d5e9-118">Bind Depth-Stencil Data to the OM Stage</span></span>

<span data-ttu-id="8d5e9-119">Associar o estado de estêncil de profundidade.</span><span class="sxs-lookup"><span data-stu-id="8d5e9-119">Bind the depth-stencil state.</span></span>


```
// Bind depth stencil state
pDevice->OMSetDepthStencilState(pDSState, 1);
```



<span data-ttu-id="8d5e9-120">Associe o recurso de estêncil de profundidade usando um modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="8d5e9-120">Bind the depth-stencil resource using a view.</span></span>


```
D3D11_DEPTH_STENCIL_VIEW_DESC descDSV;
descDSV.Format = DXGI_FORMAT_D32_FLOAT_S8X24_UINT;
descDSV.ViewDimension = D3D11_DSV_DIMENSION_TEXTURE2D;
descDSV.Texture2D.MipSlice = 0;

// Create the depth stencil view
ID3D11DepthStencilView* pDSV;
hr = pd3dDevice->CreateDepthStencilView( pDepthStencil, // Depth stencil texture
                                         &descDSV, // Depth stencil desc
                                         &pDSV );  // [out] Depth stencil view

// Bind the depth stencil view
pd3dDeviceContext->OMSetRenderTargets( 1,          // One rendertarget view
                                &pRTV,      // Render target view, created earlier
                                pDSV );     // Depth stencil view for the render target
```



<span data-ttu-id="8d5e9-121">Uma matriz de exibições de destino de renderização pode ser passada em [**ID3D11DeviceContext:: OMSetRenderTargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargets), mas todas as exibições de destino de renderização corresponderão a uma exibição de estêncil de profundidade única.</span><span class="sxs-lookup"><span data-stu-id="8d5e9-121">An array of render-target views may be passed into [**ID3D11DeviceContext::OMSetRenderTargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargets), however all of those render-target views will correspond to a single depth stencil view.</span></span> <span data-ttu-id="8d5e9-122">A matriz de destino de renderização no Direct3D 11 é um recurso que permite que um aplicativo seja processado em vários destinos de renderização simultaneamente no nível primitivo.</span><span class="sxs-lookup"><span data-stu-id="8d5e9-122">The render target array in Direct3D 11 is a feature that enables an application to render onto multiple render targets simultaneously at the primitive level.</span></span> <span data-ttu-id="8d5e9-123">As matrizes de destino de renderização oferecem maior desempenho em relação à configuração individual de destinos de renderização com várias chamadas para **ID3D11DeviceContext:: OMSetRenderTargets** (essencialmente o método empregado no Direct3D 9).</span><span class="sxs-lookup"><span data-stu-id="8d5e9-123">Render target arrays offer increased performance over individually setting render targets with multiple calls to **ID3D11DeviceContext::OMSetRenderTargets** (essentially the method employed in Direct3D 9).</span></span>

<span data-ttu-id="8d5e9-124">Os destinos de renderização devem todos ser do mesmo tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="8d5e9-124">Render targets must all be the same type of resource.</span></span> <span data-ttu-id="8d5e9-125">Se a suavização de várias amostras for usada, todos os destinos de renderização associados e buffers de profundidade devem ter as mesmas contagens de amostra.</span><span class="sxs-lookup"><span data-stu-id="8d5e9-125">If multisample antialiasing is used, all bound render targets and depth buffers must have the same sample counts.</span></span>

<span data-ttu-id="8d5e9-126">Quando um buffer é usado como um destino de renderização, os testes de estêncil de profundidade e os destinos de renderização múltiplos não são permitidos.</span><span class="sxs-lookup"><span data-stu-id="8d5e9-126">When a buffer is used as a render target, depth-stencil testing and multiple render targets are not supported.</span></span>

-   <span data-ttu-id="8d5e9-127">Até 8 destinos de renderização podem ser vinculados ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="8d5e9-127">As many as 8 render targets can be bound simultaneously.</span></span>
-   <span data-ttu-id="8d5e9-128">Todos os destinos de renderização devem ter o mesmo tamanho em todas as dimensões (largura e altura e profundidade para 3D ou tamanho da matriz para \* tipos de matriz).</span><span class="sxs-lookup"><span data-stu-id="8d5e9-128">All render targets must have the same size in all dimensions (width and height, and depth for 3D or array size for \*Array types).</span></span>
-   <span data-ttu-id="8d5e9-129">Cada destino de renderização pode ter um formato de dados diferente.</span><span class="sxs-lookup"><span data-stu-id="8d5e9-129">Each render target may have a different data format.</span></span>
-   <span data-ttu-id="8d5e9-130">As máscaras de gravação controlam quais dados são gravados em um destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="8d5e9-130">Write masks control what data gets written to a render target.</span></span> <span data-ttu-id="8d5e9-131">As máscaras de gravação de saída controlam, a um nível de componente e de destino de renderização, quais dados são gravados nos destinos de renderização.</span><span class="sxs-lookup"><span data-stu-id="8d5e9-131">The output write masks control on a per-render target, per-component level what data gets written to the render target(s).</span></span>

## <a name="advanced-stencil-techniques"></a><span data-ttu-id="8d5e9-132">Técnicas avançadas de estêncil</span><span class="sxs-lookup"><span data-stu-id="8d5e9-132">Advanced Stencil Techniques</span></span>

<span data-ttu-id="8d5e9-133">A parte de estêncil do buffer de estêncil de profundidade pode ser usada para criar efeitos de renderização como composição, decalque e contornos.</span><span class="sxs-lookup"><span data-stu-id="8d5e9-133">The stencil portion of the depth-stencil buffer can be used for creating rendering effects such as compositing, decaling, and outlining.</span></span>

-   [<span data-ttu-id="8d5e9-134">Composição</span><span class="sxs-lookup"><span data-stu-id="8d5e9-134">Compositing</span></span>](#compositing)
-   [<span data-ttu-id="8d5e9-135">Decaling</span><span class="sxs-lookup"><span data-stu-id="8d5e9-135">Decaling</span></span>](#decaling)
-   [<span data-ttu-id="8d5e9-136">Contornos e silhuetas</span><span class="sxs-lookup"><span data-stu-id="8d5e9-136">Outlines and Silhouettes</span></span>](#outlines-and-silhouettes)
-   [<span data-ttu-id="8d5e9-137">Estêncil de duas pontas</span><span class="sxs-lookup"><span data-stu-id="8d5e9-137">Two-Sided Stencil</span></span>](#two-sided-stencil)
-   [<span data-ttu-id="8d5e9-138">Lendo o buffer de Depth-Stencil como uma textura</span><span class="sxs-lookup"><span data-stu-id="8d5e9-138">Reading the Depth-Stencil Buffer as a Texture</span></span>](#reading-the-depth-stencil-buffer-as-a-texture)

### <a name="compositing"></a><span data-ttu-id="8d5e9-139">Composição</span><span class="sxs-lookup"><span data-stu-id="8d5e9-139">Compositing</span></span>

<span data-ttu-id="8d5e9-140">Seu app pode usar o buffer de estêncil para compor imagens 2D ou 3D em uma cena 3D.</span><span class="sxs-lookup"><span data-stu-id="8d5e9-140">Your application can use the stencil buffer to composite 2D or 3D images onto a 3D scene.</span></span> <span data-ttu-id="8d5e9-141">Uma máscara no buffer de estêncil é usada para ocultar uma área da superfície de destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="8d5e9-141">A mask in the stencil buffer is used to occlude an area of the rendering target surface.</span></span> <span data-ttu-id="8d5e9-142">Informações armazenadas 2D, como texto ou bitmaps, podem então ser escritas na área obstruída.</span><span class="sxs-lookup"><span data-stu-id="8d5e9-142">Stored 2D information, such as text or bitmaps, can then be written to the occluded area.</span></span> <span data-ttu-id="8d5e9-143">Como alternativa, seu app pode renderizar objetos primitivos 3D adicionais para a região mascarada por estêncil da superfície do destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="8d5e9-143">Alternately, your application can render additional 3D primitives to the stencil-masked region of the rendering target surface.</span></span> <span data-ttu-id="8d5e9-144">Ele pode até mesmo renderizar uma cena inteira.</span><span class="sxs-lookup"><span data-stu-id="8d5e9-144">It can even render an entire scene.</span></span>

<span data-ttu-id="8d5e9-145">Jogos geralmente são compostos por diversas cenas 3D juntas.</span><span class="sxs-lookup"><span data-stu-id="8d5e9-145">Games often composite multiple 3D scenes together.</span></span> <span data-ttu-id="8d5e9-146">Por exemplo, jogos de direção normalmente exibem um espelho retrovisor.</span><span class="sxs-lookup"><span data-stu-id="8d5e9-146">For instance, driving games typically display a rear-view mirror.</span></span> <span data-ttu-id="8d5e9-147">O espelho contém o modo de exibição da cena 3D atrás do condutor.</span><span class="sxs-lookup"><span data-stu-id="8d5e9-147">The mirror contains the view of the 3D scene behind the driver.</span></span> <span data-ttu-id="8d5e9-148">Ele é essencialmente uma segunda cena 3D composta pela visão frontal do condutor.</span><span class="sxs-lookup"><span data-stu-id="8d5e9-148">It is essentially a second 3D scene composited with the driver's forward view.</span></span>

### <a name="decaling"></a><span data-ttu-id="8d5e9-149">Decalque</span><span class="sxs-lookup"><span data-stu-id="8d5e9-149">Decaling</span></span>

<span data-ttu-id="8d5e9-150">Aplicativos Direct3D usam decalque para controlar quais pixels de uma determinada imagem primitiva são desenhados na superfície de destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="8d5e9-150">Direct3D applications use decaling to control which pixels from a particular primitive image are drawn to the rendering target surface.</span></span> <span data-ttu-id="8d5e9-151">Os apps aplicam os decalques às imagens de objetos primitivos para permitir que polígonos coplanares sejam renderizados corretamente.</span><span class="sxs-lookup"><span data-stu-id="8d5e9-151">Applications apply decals to the images of primitives to enable coplanar polygons to render correctly.</span></span>

<span data-ttu-id="8d5e9-152">Por exemplo, ao aplicar marcas de pneus e linhas amarelas em uma estrada, as marcas devem aparecer diretamente sobre a pista.</span><span class="sxs-lookup"><span data-stu-id="8d5e9-152">For instance, when applying tire marks and yellow lines to a roadway, the markings should appear directly on top of the road.</span></span> <span data-ttu-id="8d5e9-153">No entanto, os valores z das marcas e da estrada são os mesmos.</span><span class="sxs-lookup"><span data-stu-id="8d5e9-153">However, the z values of the markings and the road are the same.</span></span> <span data-ttu-id="8d5e9-154">Portanto, o buffer de profundidade pode não produzir uma separação clara entre os dois.</span><span class="sxs-lookup"><span data-stu-id="8d5e9-154">Therefore, the depth buffer might not produce a clean separation between the two.</span></span> <span data-ttu-id="8d5e9-155">Alguns pixels da parte primitiva traseira podem ser renderizados na parte superior da parte primitiva frontal e vice-versa.</span><span class="sxs-lookup"><span data-stu-id="8d5e9-155">Some pixels in the back primitive may be rendered on top of the front primitive and vice versa.</span></span> <span data-ttu-id="8d5e9-156">A imagem resultante parece tremida de quadro a quadro.</span><span class="sxs-lookup"><span data-stu-id="8d5e9-156">The resulting image appears to shimmer from frame to frame.</span></span> <span data-ttu-id="8d5e9-157">Esse efeito é chamado luta z ou flimmering.</span><span class="sxs-lookup"><span data-stu-id="8d5e9-157">This effect is called z-fighting or flimmering.</span></span>

<span data-ttu-id="8d5e9-158">Para resolver esse problema, use um estêncil para mascarar a seção da parte traseira primitiva onde aparecerá o decalque.</span><span class="sxs-lookup"><span data-stu-id="8d5e9-158">To solve this problem, use a stencil to mask the section of the back primitive where the decal will appear.</span></span> <span data-ttu-id="8d5e9-159">Desligue o buffer z e renderize a imagem da parte primitiva dianteira na área sem máscara da superfície de destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="8d5e9-159">Turn off z-buffering and render the image of the front primitive into the masked-off area of the render-target surface.</span></span>

<span data-ttu-id="8d5e9-160">Várias mesclagens de textura podem ser usadas para resolver esse problema.</span><span class="sxs-lookup"><span data-stu-id="8d5e9-160">Multiple texture blending can be used to solve this problem.</span></span>

### <a name="outlines-and-silhouettes"></a><span data-ttu-id="8d5e9-161">Contornos e silhuetas</span><span class="sxs-lookup"><span data-stu-id="8d5e9-161">Outlines and Silhouettes</span></span>

<span data-ttu-id="8d5e9-162">Você pode usar o buffer de estêncil para efeitos mais abstratos, como contornos e silhuetas.</span><span class="sxs-lookup"><span data-stu-id="8d5e9-162">You can use the stencil buffer for more abstract effects, such as outlining and silhouetting.</span></span>

<span data-ttu-id="8d5e9-163">Se seu app realiza duas passagens de renderização - uma para gerar a máscara de estêncil e a segunda para aplicar a máscara de estêncil à imagem, mas com os primitivas um pouco menores na segunda passagem - a imagem resultante conterá apenas contorno da primitiva.</span><span class="sxs-lookup"><span data-stu-id="8d5e9-163">If your application does two render passes - one to generate the stencil mask and second to apply the stencil mask to the image, but with the primitives slightly smaller on the second pass - the resulting image will contain only the primitive's outline.</span></span> <span data-ttu-id="8d5e9-164">O app pode preencher a área com máscara de estêncil da imagem com uma cor sólida, dando à primitiva uma aparência em alto-relevo.</span><span class="sxs-lookup"><span data-stu-id="8d5e9-164">The application can then fill the stencil-masked area of the image with a solid color, giving the primitive an embossed look.</span></span>

<span data-ttu-id="8d5e9-165">Se a máscara de estêncial tiver o mesmo tamanho e formato da primitiva que está sendo renderizado, a imagem resultante terá um buraco onde o primitivo deveria estar.</span><span class="sxs-lookup"><span data-stu-id="8d5e9-165">If the stencil mask is the same size and shape as the primitive you are rendering, the resulting image contains a hole where the primitive should be.</span></span> <span data-ttu-id="8d5e9-166">Seu app poderá preencher o buraco com cor preta para produzir uma silhueta da primitiva.</span><span class="sxs-lookup"><span data-stu-id="8d5e9-166">Your application can then fill the hole with black to produce a silhouette of the primitive.</span></span>

### <a name="two-sided-stencil"></a><span data-ttu-id="8d5e9-167">Estêncil de dois lados</span><span class="sxs-lookup"><span data-stu-id="8d5e9-167">Two-Sided Stencil</span></span>

<span data-ttu-id="8d5e9-168">Os volumes de sombra são usados para desenhar sombras com o buffer de estêncil.</span><span class="sxs-lookup"><span data-stu-id="8d5e9-168">Shadow Volumes are used for drawing shadows with the stencil buffer.</span></span> <span data-ttu-id="8d5e9-169">O app calcula os volumes de sombra convertidos sobrepondo a geometria, calculando as bordas da silhueta e afastando-as da luz em um conjunto de volumes 3D.</span><span class="sxs-lookup"><span data-stu-id="8d5e9-169">The application computes the shadow volumes cast by occluding geometry, by computing the silhouette edges and extruding them away from the light into a set of 3D volumes.</span></span> <span data-ttu-id="8d5e9-170">Em seguida, esses volumes são renderizados duas vezes no buffer de estêncil.</span><span class="sxs-lookup"><span data-stu-id="8d5e9-170">These volumes are then rendered twice into the stencil buffer.</span></span>

<span data-ttu-id="8d5e9-171">A primeira renderização desenha polígonos voltados para frente e aumenta os valores de buffer de estêncil.</span><span class="sxs-lookup"><span data-stu-id="8d5e9-171">The first render draws forward-facing polygons, and increments the stencil-buffer values.</span></span> <span data-ttu-id="8d5e9-172">A segunda renderização desenha polígonos voltados para trás do volume de sombra e diminui os valores de buffer de estêncil.</span><span class="sxs-lookup"><span data-stu-id="8d5e9-172">The second render draws the back-facing polygons of the shadow volume, and decrements the stencil buffer values.</span></span> <span data-ttu-id="8d5e9-173">Normalmente, todos os valores incrementados e decrementados cancelam um ao outro. No entanto, a cena já foi renderizada com geometria normal, fazendo com que alguns pixels falhem no teste de buffer z, conforme o volume de sombra é renderizado.</span><span class="sxs-lookup"><span data-stu-id="8d5e9-173">Normally, all incremented and decremented values cancel each other out. However, the scene was already rendered with normal geometry causing some pixels to fail the z-buffer test as the shadow volume is rendered.</span></span> <span data-ttu-id="8d5e9-174">Os valores restantes no buffer de estêncil correspondem aos pixels que estão na sombra.</span><span class="sxs-lookup"><span data-stu-id="8d5e9-174">Values left in the stencil buffer correspond to pixels that are in the shadow.</span></span> <span data-ttu-id="8d5e9-175">Esse conteúdo restante do buffer de estêncil é usado como uma máscara, para fazer a combinação alfa de um quadrupleto preto grande e abrangente na cena.</span><span class="sxs-lookup"><span data-stu-id="8d5e9-175">These remaining stencil-buffer contents are used as a mask, to alpha-blend a large, all-encompassing black quad into the scene.</span></span> <span data-ttu-id="8d5e9-176">Com o buffer de estêncil atuando como uma máscara, o resultado será o escurecimento dos pixels que estão nas sombras.</span><span class="sxs-lookup"><span data-stu-id="8d5e9-176">With the stencil buffer acting as a mask, the result is to darken pixels that are in the shadows.</span></span>

<span data-ttu-id="8d5e9-177">Isso significa que a geometria de sombra é desenhada duas vezes por fonte de luz, exercendo assim pressão sobre a taxa de transferência de vértice da GPU.</span><span class="sxs-lookup"><span data-stu-id="8d5e9-177">This means that the shadow geometry is drawn twice per light source, hence putting pressure on the vertex throughput of the GPU.</span></span> <span data-ttu-id="8d5e9-178">O recurso de estêncil de dois lados foi projetado para atenuar essa situação.</span><span class="sxs-lookup"><span data-stu-id="8d5e9-178">The two-sided stencil feature has been designed to mitigate this situation.</span></span> <span data-ttu-id="8d5e9-179">Nesta abordagem, existem dois conjuntos de estado de estêncil (nomeados abaixo), um conjunto para os triângulos voltados para a frente e outro para os triângulos voltados para trás.</span><span class="sxs-lookup"><span data-stu-id="8d5e9-179">In this approach, there are two sets of stencil state (named below), one set each for the front-facing triangles and the other for the back-facing triangles.</span></span> <span data-ttu-id="8d5e9-180">Dessa forma, somente uma única passagem é desenhada por volume de sombra, por luz.</span><span class="sxs-lookup"><span data-stu-id="8d5e9-180">This way, only a single pass is drawn per shadow volume, per light.</span></span>

<span data-ttu-id="8d5e9-181">Um exemplo de implementação de estêncil de dois lados pode ser encontrado no [exemplo ShadowVolume10](https://msdn.microsoft.com/library/Ee416427(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="8d5e9-181">An example of two-sided stencil implementation can be found in the [ShadowVolume10 Sample](https://msdn.microsoft.com/library/Ee416427(v=VS.85).aspx).</span></span>

### <a name="reading-the-depth-stencil-buffer-as-a-texture"></a><span data-ttu-id="8d5e9-182">Ler o buffer de estêncil de profundidade como uma textura</span><span class="sxs-lookup"><span data-stu-id="8d5e9-182">Reading the Depth-Stencil Buffer as a Texture</span></span>

<span data-ttu-id="8d5e9-183">Um buffer de estêncil de profundidade inativo pode ser lido por um sombreador como uma textura.</span><span class="sxs-lookup"><span data-stu-id="8d5e9-183">An inactive depth-stencil buffer can be read by a shader as a texture.</span></span> <span data-ttu-id="8d5e9-184">Um app que lê um buffer de estêncil de profundidade como uma textura renderiza em duas passagens, a primeira passagem grava o buffer de estêncil de profundidade e a segunda passagem lê do buffer.</span><span class="sxs-lookup"><span data-stu-id="8d5e9-184">An application that reads a depth-stencil buffer as a texture renders in two passes, the first pass writes to the depth-stencil buffer and the second pass reads from the buffer.</span></span> <span data-ttu-id="8d5e9-185">Isso permite que um sombreador compare os valores de profundidade ou estêncil gravados anteriormente no buffer com o valor do pixel que está sendo renderizado atualmente.</span><span class="sxs-lookup"><span data-stu-id="8d5e9-185">This allows a shader to compare depth or stencil values previously written to the buffer against the value for the pixel currrently being rendered.</span></span> <span data-ttu-id="8d5e9-186">O resultado da comparação pode ser usado para criar efeitos, como o mapeamento de sombra ou partículas suaves em um sistema de partículas.</span><span class="sxs-lookup"><span data-stu-id="8d5e9-186">The result of the comparison can be used to create effects such as shadow mapping or soft particles in a particle system.</span></span>

<span data-ttu-id="8d5e9-187">Para criar um buffer de estêncil de profundidade que pode ser usado como um recurso de estêncil de profundidade e um recurso de sombreador, algumas alterações precisam ser feitas para o código de exemplo na seção [criar um Depth-Stencil recurso](#create-a-depth-stencil-resource) .</span><span class="sxs-lookup"><span data-stu-id="8d5e9-187">To create a depth-stencil buffer that can be used as both a depth-stencil resource and a shader resource a few changes need to be made to sample code in the [Create a Depth-Stencil Resource](#create-a-depth-stencil-resource) section.</span></span>

-   <span data-ttu-id="8d5e9-188">O recurso de estêncil de profundidade deve ter um formato não tipado, como o \_ formato dxgi \_ R32 \_ .</span><span class="sxs-lookup"><span data-stu-id="8d5e9-188">The depth-stencil resource must have a typeless format such as DXGI\_FORMAT\_R32\_TYPELESS.</span></span>
    ```
    descDepth.Format = DXGI_FORMAT_R32_TYPELESS;
    ```

    

-   <span data-ttu-id="8d5e9-189">O recurso de estêncil de profundidade deve usar os sinalizadores de associação de recurso do estêncil de profundidade de D3D10 \_ e do d3d10 BIND \_ \_ \_ \_ Shader \_ .</span><span class="sxs-lookup"><span data-stu-id="8d5e9-189">The depth-stencil resource must use both the D3D10\_BIND\_DEPTH\_STENCIL and D3D10\_BIND\_SHADER\_RESOURCE bind flags.</span></span>
    ```
    descDepth.BindFlags = D3D10_BIND_DEPTH_STENCIL | D3D10_BIND_SHADER_RESOURCE;
    ```

    

<span data-ttu-id="8d5e9-190">Além disso, um modo de exibição de recursos do sombreador precisa ser criado para o buffer de profundidade usando uma estrutura [**desc de exibição de \_ recursos do sombreador \_ \_ \_ D3D11**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_shader_resource_view_desc) e [**ID3D11Device:: CreateShaderResourceView**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createshaderresourceview).</span><span class="sxs-lookup"><span data-stu-id="8d5e9-190">In addition a shader resource view needs to be created for the depth buffer using a [**D3D11\_SHADER\_RESOURCE\_VIEW\_DESC**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_shader_resource_view_desc) structure and [**ID3D11Device::CreateShaderResourceView**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createshaderresourceview).</span></span> <span data-ttu-id="8d5e9-191">O modo de exibição de recursos do sombreador usará um formato tipado, como o **\_ formato dxgi \_ R32 \_ float** que é equivalente ao formato de tipo informativo especificado quando o recurso de estêncil de profundidade foi criado.</span><span class="sxs-lookup"><span data-stu-id="8d5e9-191">The shader resource view will use a typed format such as **DXGI\_FORMAT\_R32\_FLOAT** that is the equivalent to the typeless format specified when the depth-stencil resource was created.</span></span>

<span data-ttu-id="8d5e9-192">No primeiro processamento, passe o buffer de profundidade associado, conforme descrito na seção [associar dados Depth-Stencil à etapa de OM](#bind-depth-stencil-data-to-the-om-stage) .</span><span class="sxs-lookup"><span data-stu-id="8d5e9-192">In the first render pass the depth buffer is bound as described in the [Bind Depth-Stencil Data to the OM Stage](#bind-depth-stencil-data-to-the-om-stage) section.</span></span> <span data-ttu-id="8d5e9-193">Observe que o formato passado para [**a \_ exibição de estêncil de profundidade D3D11 \_ \_ \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_view_desc). O formato usará um formato tipado, como o **\_ formato dxgi \_ D32 \_ float**.</span><span class="sxs-lookup"><span data-stu-id="8d5e9-193">Note that the format passed to [**D3D11\_DEPTH\_STENCIL\_VIEW\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_view_desc).Format will use a typed format such as **DXGI\_FORMAT\_D32\_FLOAT**.</span></span> <span data-ttu-id="8d5e9-194">Após a primeira passagem de renderização, o buffer de profundidade conterá os valores de profundidade para a cena.</span><span class="sxs-lookup"><span data-stu-id="8d5e9-194">After the first render pass the depth buffer will contain the depth values for the scene.</span></span>

<span data-ttu-id="8d5e9-195">Na segunda passagem de renderização, a função [**ID3D11DeviceContext:: OMSetRenderTargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargets) é usada para definir a exibição de estêncil de profundidade como **nula** ou um recurso de estêncil de profundidade diferente e a exibição de recurso do sombreador é passada para o sombreador usando [**ID3D11EffectShaderResourceVariable:: setresource**](id3dx11effectshaderresourcevariable-setresource.md).</span><span class="sxs-lookup"><span data-stu-id="8d5e9-195">In the second render pass the [**ID3D11DeviceContext::OMSetRenderTargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargets) function is used to set the depth-stencil view to **NULL** or a different depth-stencil resource and the shader resource view is passed to the shader using [**ID3D11EffectShaderResourceVariable::SetResource**](id3dx11effectshaderresourcevariable-setresource.md).</span></span> <span data-ttu-id="8d5e9-196">Isso permite que o sombreador pesquise os valores de profundidade calculados na primeira passagem de renderização.</span><span class="sxs-lookup"><span data-stu-id="8d5e9-196">This allows the shader to look up the depth values calculated in the first rendering pass.</span></span> <span data-ttu-id="8d5e9-197">Observe que será necessário aplicar uma transformação para recuperar valores de profundidade se o ponto de vista da primeira passagem de renderização for diferente da segunda passagem de renderização.</span><span class="sxs-lookup"><span data-stu-id="8d5e9-197">Note that a transformation will need to be applied to retrieve depth values if the point of view of the first render pass is different from the second render pass.</span></span> <span data-ttu-id="8d5e9-198">Por exemplo, se uma técnica de mapeamento de sombra estiver sendo usada, a primeira passagem de renderização será da perspectiva de uma fonte de luz enquanto a segunda passagem de renderização irá da perspectiva do visualizador.</span><span class="sxs-lookup"><span data-stu-id="8d5e9-198">For example, if a shadow mapping technique is being used the first render pass will be from the perspective of a light source while the second render pass will from the viewer's perspective.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8d5e9-199">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8d5e9-199">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8d5e9-200">Estágio de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="8d5e9-200">Output-Merger Stage</span></span>](d3d10-graphics-programming-guide-output-merger-stage.md)
</dt> <dt>

[<span data-ttu-id="8d5e9-201">Estágios de pipeline (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="8d5e9-201">Pipeline Stages (Direct3D 10)</span></span>](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

 