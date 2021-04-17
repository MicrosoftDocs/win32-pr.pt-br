---
title: deriv_rtx (sm4-ASM)
description: Taxa de alteração de conteúdo de cada componente float32 de src0 (post-swizzle), com relação à direção de RenderTarget x (RTX) ou à direção de RenderTarget y.
ms.assetid: 2438DB36-C348-4854-AE1B-EC3C890B0B42
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21d4543805c02cf70d9c6b7856461c427788f616
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104365195"
---
# <a name="deriv_rtx-sm4---asm"></a><span data-ttu-id="5899d-103">derivar \_ RTX (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="5899d-103">deriv\_rtx (sm4 - asm)</span></span>

<span data-ttu-id="5899d-104">Taxa de alteração de conteúdo de cada componente float32 de *src0* (post-swizzle), com relação à direção de renderTarget x (RTX) ou à direção de renderTarget y.</span><span class="sxs-lookup"><span data-stu-id="5899d-104">Rate of change of contents of each float32 component of *src0* (post-swizzle), with regard to RenderTarget x direction (rtx) or RenderTarget y direction.</span></span>



| <span data-ttu-id="5899d-105">deriva \_ RTX \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="5899d-105">deriv\_rtx\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\],</span></span> |
|--------------------------------------------------------------------|



 



| <span data-ttu-id="5899d-106">Item</span><span class="sxs-lookup"><span data-stu-id="5899d-106">Item</span></span>                                                            | <span data-ttu-id="5899d-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="5899d-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="5899d-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="5899d-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="5899d-109">\[no \] endereço do resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="5899d-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="5899d-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="5899d-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="5899d-111">\[no \] componente na operação.</span><span class="sxs-lookup"><span data-stu-id="5899d-111">\[in\] The component in the operation.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="5899d-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="5899d-112">Remarks</span></span>

<span data-ttu-id="5899d-113">Apenas um único par derivado x, y é calculado para cada carimbo 2x2 de pixels.</span><span class="sxs-lookup"><span data-stu-id="5899d-113">Only a single x,y derivative pair is computed for each 2x2 stamp of pixels.</span></span>

<span data-ttu-id="5899d-114">Esta operação é dependente de hardware.</span><span class="sxs-lookup"><span data-stu-id="5899d-114">This operation is hardware dependent.</span></span>

<span data-ttu-id="5899d-115">Implementação do rasterizador de referência para triângulos:</span><span class="sxs-lookup"><span data-stu-id="5899d-115">Reference rasterizer implementation for triangles:</span></span>

-   <span data-ttu-id="5899d-116">O sombreador de pixel sempre executa o sombreador sobre 2x2 de quatro pixels em atrelada (até mesmo por meio do controle de fluxo, mascarando pixels desabilitados).</span><span class="sxs-lookup"><span data-stu-id="5899d-116">Pixel Shader always runs Shader over 2x2 quad of pixels in lockstep (even through flow control, masking disabled pixels).</span></span>
-   <span data-ttu-id="5899d-117">Os quatro processadores sempre têm coordenadas de pixel numeradas (x e y) para o pixel superior esquerdo.</span><span class="sxs-lookup"><span data-stu-id="5899d-117">Quads always have even numbered pixel coordinates (both x and y) for top-left pixel.</span></span>
-   <span data-ttu-id="5899d-118">Os pixels fictícios ficam inativos primitivos se o primitivo for muito pequeno para preencher um 2x2 quádruplo.</span><span class="sxs-lookup"><span data-stu-id="5899d-118">Dummy pixels run off primitive if primitive is too small to fill a 2x2 quad.</span></span>
-   <span data-ttu-id="5899d-119">**derivar \_ RTX** é computado escolhendo primeiro 2 pixels: o pixel atual e o outro pixel com a mesma coordenada y do Quad.</span><span class="sxs-lookup"><span data-stu-id="5899d-119">**deriv\_rtx** is computed by first choosing 2 pixels: the current pixel and the other pixel with the same y coordinate from the quad.</span></span> <span data-ttu-id="5899d-120">Em seguida, o resultado é calculado como: *src0*(x estranho)- *src0*(até mesmo x pixel) \[ por componente\]</span><span class="sxs-lookup"><span data-stu-id="5899d-120">Then, the result is calculated as: *src0*(odd x pixel) - *src0*(even x pixel) \[per-component\]</span></span>
-   <span data-ttu-id="5899d-121">[derivar \_ rty](deriv-rty--sm4---asm-.md) é computado escolhendo primeiro 2 pixels: o pixel atual e o outro pixel com a mesma coordenada x do Quad.</span><span class="sxs-lookup"><span data-stu-id="5899d-121">[deriv\_rty](deriv-rty--sm4---asm-.md) is computed by first choosing 2 pixels: the current pixel and the other pixel with the same x coordinate from the quad.</span></span> <span data-ttu-id="5899d-122">Em seguida, o resultado é calculado como: *src0*(y x-pixel)- *src0*(mesmo y pixel) \[ por componente\]</span><span class="sxs-lookup"><span data-stu-id="5899d-122">Then, the result is calculated as: *src0*(odd y pixel) - *src0*(even y pixel) \[per-component\]</span></span>

<span data-ttu-id="5899d-123">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="5899d-123">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="5899d-124">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="5899d-124">Vertex Shader</span></span> | <span data-ttu-id="5899d-125">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="5899d-125">Geometry Shader</span></span> | <span data-ttu-id="5899d-126">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="5899d-126">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               |                 | <span data-ttu-id="5899d-127">x</span><span class="sxs-lookup"><span data-stu-id="5899d-127">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="5899d-128">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="5899d-128">Minimum Shader Model</span></span>

<span data-ttu-id="5899d-129">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="5899d-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="5899d-130">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="5899d-130">Shader Model</span></span>                                              | <span data-ttu-id="5899d-131">Com suporte</span><span class="sxs-lookup"><span data-stu-id="5899d-131">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="5899d-132">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="5899d-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="5899d-133">sim</span><span class="sxs-lookup"><span data-stu-id="5899d-133">yes</span></span>       |
| [<span data-ttu-id="5899d-134">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="5899d-134">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="5899d-135">sim</span><span class="sxs-lookup"><span data-stu-id="5899d-135">yes</span></span>       |
| [<span data-ttu-id="5899d-136">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="5899d-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="5899d-137">sim</span><span class="sxs-lookup"><span data-stu-id="5899d-137">yes</span></span>       |
| [<span data-ttu-id="5899d-138">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5899d-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="5899d-139">não</span><span class="sxs-lookup"><span data-stu-id="5899d-139">no</span></span>        |
| [<span data-ttu-id="5899d-140">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5899d-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="5899d-141">não</span><span class="sxs-lookup"><span data-stu-id="5899d-141">no</span></span>        |
| [<span data-ttu-id="5899d-142">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5899d-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="5899d-143">não</span><span class="sxs-lookup"><span data-stu-id="5899d-143">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="5899d-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5899d-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5899d-145">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5899d-145">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





