---
title: deriv_rty (sm4-ASM)
description: Equivalente de render-destino y de derivar \_ RTX.
ms.assetid: F78F2DBD-9428-4F34-85AD-276DF54C52D1
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2e4517782c687473b4789229334b4cafc94b989
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103823436"
---
# <a name="deriv_rty-sm4---asm"></a><span data-ttu-id="f32fd-103">derivar \_ rty (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="f32fd-103">deriv\_rty (sm4 - asm)</span></span>

<span data-ttu-id="f32fd-104">Equivalente de render-destino y de [derivar \_ RTX](deriv-rtx--sm4---asm-.md).</span><span class="sxs-lookup"><span data-stu-id="f32fd-104">Render-target y equivalent of [deriv\_rtx](deriv-rtx--sm4---asm-.md).</span></span>



| <span data-ttu-id="f32fd-105">deriva \_ rty \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="f32fd-105">deriv\_rty\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\],</span></span> |
|--------------------------------------------------------------------|



 



| <span data-ttu-id="f32fd-106">Item</span><span class="sxs-lookup"><span data-stu-id="f32fd-106">Item</span></span>                                                            | <span data-ttu-id="f32fd-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="f32fd-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="f32fd-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="f32fd-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="f32fd-109">\[no \] endereço do resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="f32fd-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="f32fd-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="f32fd-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="f32fd-111">\[no \] componente na operação.</span><span class="sxs-lookup"><span data-stu-id="f32fd-111">\[in\] The component in the operation.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="f32fd-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="f32fd-112">Remarks</span></span>

<span data-ttu-id="f32fd-113">Apenas um único par derivado x, y é calculado para cada carimbo 2x2 de pixels.</span><span class="sxs-lookup"><span data-stu-id="f32fd-113">Only a single x,y derivative pair is computed for each 2x2 stamp of pixels.</span></span>

<span data-ttu-id="f32fd-114">Esta operação é dependente de hardware.</span><span class="sxs-lookup"><span data-stu-id="f32fd-114">This operation is hardware dependent.</span></span>

<span data-ttu-id="f32fd-115">Implementação do rasterizador de referência para triângulos:</span><span class="sxs-lookup"><span data-stu-id="f32fd-115">Reference rasterizer implementation for triangles:</span></span>

-   <span data-ttu-id="f32fd-116">O sombreador de pixel sempre executa o sombreador sobre 2x2 de quatro pixels em atrelada (até mesmo por meio do controle de fluxo, mascarando pixels desabilitados).</span><span class="sxs-lookup"><span data-stu-id="f32fd-116">Pixel Shader always runs Shader over 2x2 quad of pixels in lockstep (even through flow control, masking disabled pixels).</span></span>
-   <span data-ttu-id="f32fd-117">Os quatro processadores sempre têm coordenadas de pixel numeradas (x e y) para o pixel superior esquerdo.</span><span class="sxs-lookup"><span data-stu-id="f32fd-117">Quads always have even numbered pixel coordinates (both x and y) for top-left pixel.</span></span>
-   <span data-ttu-id="f32fd-118">Os pixels fictícios ficam inativos primitivos se o primitivo for muito pequeno para preencher um 2x2 quádruplo.</span><span class="sxs-lookup"><span data-stu-id="f32fd-118">Dummy pixels run off primitive if primitive is too small to fill a 2x2 quad.</span></span>
-   <span data-ttu-id="f32fd-119">[derivar \_ RTX](deriv-rtx--sm4---asm-.md) é computado escolhendo primeiro 2 pixels: o pixel atual e o outro pixel com a mesma coordenada y do Quad.</span><span class="sxs-lookup"><span data-stu-id="f32fd-119">[deriv\_rtx](deriv-rtx--sm4---asm-.md) is computed by first choosing 2 pixels: the current pixel and the other pixel with the same y coordinate from the quad.</span></span> <span data-ttu-id="f32fd-120">Em seguida, o resultado é calculado como: *src0*(x estranho)- *src0*(até mesmo x pixel) \[ por componente\]</span><span class="sxs-lookup"><span data-stu-id="f32fd-120">Then, the result is calculated as: *src0*(odd x pixel) - *src0*(even x pixel) \[per-component\]</span></span>
-   <span data-ttu-id="f32fd-121">**derivar \_ rty** é computado escolhendo primeiro 2 pixels: o pixel atual e o outro pixel com a mesma coordenada x do Quad.</span><span class="sxs-lookup"><span data-stu-id="f32fd-121">**deriv\_rty** is computed by first choosing 2 pixels: the current pixel and the other pixel with the same x coordinate from the quad.</span></span> <span data-ttu-id="f32fd-122">Em seguida, o resultado é calculado como: *src0*(y x-pixel)- *src0*(mesmo y pixel) \[ por componente\]</span><span class="sxs-lookup"><span data-stu-id="f32fd-122">Then, the result is calculated as: *src0*(odd y pixel) - *src0*(even y pixel) \[per-component\]</span></span>

<span data-ttu-id="f32fd-123">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="f32fd-123">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="f32fd-124">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="f32fd-124">Vertex Shader</span></span> | <span data-ttu-id="f32fd-125">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="f32fd-125">Geometry Shader</span></span> | <span data-ttu-id="f32fd-126">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="f32fd-126">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               |                 | <span data-ttu-id="f32fd-127">x</span><span class="sxs-lookup"><span data-stu-id="f32fd-127">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="f32fd-128">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="f32fd-128">Minimum Shader Model</span></span>

<span data-ttu-id="f32fd-129">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="f32fd-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="f32fd-130">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="f32fd-130">Shader Model</span></span>                                              | <span data-ttu-id="f32fd-131">Com suporte</span><span class="sxs-lookup"><span data-stu-id="f32fd-131">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="f32fd-132">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="f32fd-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="f32fd-133">sim</span><span class="sxs-lookup"><span data-stu-id="f32fd-133">yes</span></span>       |
| [<span data-ttu-id="f32fd-134">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="f32fd-134">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="f32fd-135">sim</span><span class="sxs-lookup"><span data-stu-id="f32fd-135">yes</span></span>       |
| [<span data-ttu-id="f32fd-136">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="f32fd-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="f32fd-137">sim</span><span class="sxs-lookup"><span data-stu-id="f32fd-137">yes</span></span>       |
| [<span data-ttu-id="f32fd-138">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f32fd-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="f32fd-139">não</span><span class="sxs-lookup"><span data-stu-id="f32fd-139">no</span></span>        |
| [<span data-ttu-id="f32fd-140">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f32fd-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="f32fd-141">não</span><span class="sxs-lookup"><span data-stu-id="f32fd-141">no</span></span>        |
| [<span data-ttu-id="f32fd-142">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f32fd-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="f32fd-143">não</span><span class="sxs-lookup"><span data-stu-id="f32fd-143">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="f32fd-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f32fd-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f32fd-145">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f32fd-145">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





