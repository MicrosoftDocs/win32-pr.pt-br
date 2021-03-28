---
title: sample_d (sm4-ASM)
description: Amostras de dados do elemento/textura especificado usando o endereço especificado e o modo de filtragem identificados pelo determinado exemplo. | sample_d (sm4-ASM)
ms.assetid: 9CF57C4A-C0D1-4D57-A5EE-62BBBB291438
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abe2d3ad310c18ff2bb10e101c95e0267d534fed
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104989222"
---
# <a name="sample_d-sm4---asm"></a><span data-ttu-id="c97ea-104">exemplo \_ d (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="c97ea-104">sample\_d (sm4 - asm)</span></span>

<span data-ttu-id="c97ea-105">Amostras de dados do elemento/textura especificado usando o endereço especificado e o modo de filtragem identificados pelo determinado exemplo.</span><span class="sxs-lookup"><span data-stu-id="c97ea-105">Samples data from the specified Element/texture using the specified address and the filtering mode identified by the given sampler.</span></span>



| <span data-ttu-id="c97ea-106">ssample \_ d \[ \_ aoffimmi (u, v, w) \] dest \[ . Mask \] , srcAddress \[ . swizzle \] , srcResource \[ . swizzle \] , srcSampler, srcXDerivatives \[ . swizzle \] , srcYDerivatives \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="c97ea-106">ssample\_d\[\_aoffimmi(u,v,w)\] dest\[.mask\], srcAddress\[.swizzle\], srcResource\[.swizzle\], srcSampler, srcXDerivatives\[.swizzle\], srcYDerivatives\[.swizzle\]</span></span> |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="c97ea-107">Item</span><span class="sxs-lookup"><span data-stu-id="c97ea-107">Item</span></span>                                                                                                                               | <span data-ttu-id="c97ea-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="c97ea-108">Description</span></span>                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c97ea-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="c97ea-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                                    | <span data-ttu-id="c97ea-110">\[no \] endereço dos resultados da operação.</span><span class="sxs-lookup"><span data-stu-id="c97ea-110">\[in\] The address of the results of the operation.</span></span><br/>                                                                  |
| <span data-ttu-id="c97ea-111"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span><span class="sxs-lookup"><span data-stu-id="c97ea-111"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>                     | <span data-ttu-id="c97ea-112">\[em \] um conjunto de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="c97ea-112">\[in\] A set of texture coordinates.</span></span> <span data-ttu-id="c97ea-113">Para obter mais informações, consulte a instrução de [exemplo](sample--sm4---asm-.md) .</span><span class="sxs-lookup"><span data-stu-id="c97ea-113">For more information see the [sample](sample--sm4---asm-.md) instruction.</span></span><br/>      |
| <span data-ttu-id="c97ea-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="c97ea-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/>                 | <span data-ttu-id="c97ea-115">\[em \] um registro de textura.</span><span class="sxs-lookup"><span data-stu-id="c97ea-115">\[in\] A texture register.</span></span> <span data-ttu-id="c97ea-116">Para obter mais informações, consulte a instrução de **exemplo** .</span><span class="sxs-lookup"><span data-stu-id="c97ea-116">For more information see the **sample** instruction.</span></span><br/>                                      |
| <span data-ttu-id="c97ea-117"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span><span class="sxs-lookup"><span data-stu-id="c97ea-117"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>                     | <span data-ttu-id="c97ea-118">\[em \] um registro de amostra.</span><span class="sxs-lookup"><span data-stu-id="c97ea-118">\[in\] A sampler register.</span></span> <span data-ttu-id="c97ea-119">Para obter mais informações, consulte a instrução de **exemplo** .</span><span class="sxs-lookup"><span data-stu-id="c97ea-119">For more information see the **sample** instruction.</span></span><br/>                                      |
| <span data-ttu-id="c97ea-120"><span id="srcXDerivatives"></span><span id="srcxderivatives"></span><span id="SRCXDERIVATIVES"></span>*srcXDerivatives*</span><span class="sxs-lookup"><span data-stu-id="c97ea-120"><span id="srcXDerivatives"></span><span id="srcxderivatives"></span><span id="SRCXDERIVATIVES"></span>*srcXDerivatives*</span></span><br/> | <span data-ttu-id="c97ea-121">\[nas \] derivações do endereço de origem na direção x.</span><span class="sxs-lookup"><span data-stu-id="c97ea-121">\[in\] The derivatives for the source address in the x direction.</span></span> <span data-ttu-id="c97ea-122">Para obter mais informações, consulte a seção **comentários** .</span><span class="sxs-lookup"><span data-stu-id="c97ea-122">For more information, see the **Remarks** section.</span></span><br/> |
| <span data-ttu-id="c97ea-123"><span id="srcYDerivatives"></span><span id="srcyderivatives"></span><span id="SRCYDERIVATIVES"></span>*srcYDerivatives*</span><span class="sxs-lookup"><span data-stu-id="c97ea-123"><span id="srcYDerivatives"></span><span id="srcyderivatives"></span><span id="SRCYDERIVATIVES"></span>*srcYDerivatives*</span></span><br/> | <span data-ttu-id="c97ea-124">\[nas \] derivações do endereço de origem na direção y.</span><span class="sxs-lookup"><span data-stu-id="c97ea-124">\[in\] The derivatives for the source address in the y direction.</span></span> <span data-ttu-id="c97ea-125">Para obter mais informações, consulte a seção **comentários** .</span><span class="sxs-lookup"><span data-stu-id="c97ea-125">For more information, see the **Remarks** section.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c97ea-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="c97ea-126">Remarks</span></span>

<span data-ttu-id="c97ea-127">Essa instrução se comporta como a instrução de [exemplo](sample--sm4---asm-.md) , exceto que derivativos para o endereço de origem na direção x e a direção y são fornecidos por parâmetros extras, *srcXDerivatives* e *srcYDerivatives*, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="c97ea-127">This instruction behaves like the [sample](sample--sm4---asm-.md) instruction, except that derivatives for the source address in the x direction and the y direction are provided by extra parameters, *srcXDerivatives* and *srcYDerivatives*, respectively.</span></span> <span data-ttu-id="c97ea-128">Esses derivativos estão no espaço de coordenadas de textura normalizado.</span><span class="sxs-lookup"><span data-stu-id="c97ea-128">These derivatives are in normalized texture coordinate space.</span></span>

<span data-ttu-id="c97ea-129">Os componentes r, g e b de *srcXDerivatives* (pos-swizzle) fornecem du/DX, DV/DX e DW/DX.</span><span class="sxs-lookup"><span data-stu-id="c97ea-129">The r, g and b components of *srcXDerivatives* (POS-swizzle) provide du/dx, dv/dx and dw/dx.</span></span> <span data-ttu-id="c97ea-130">O componente ' a ' (POS-swizzle) é ignorado.</span><span class="sxs-lookup"><span data-stu-id="c97ea-130">The 'a' component (POS-swizzle) is ignored.</span></span>

<span data-ttu-id="c97ea-131">Os componentes r, g e b de *srcYDerivatives* (pos-swizzle) fornecem du/DY, DV/DY e DW/DY.</span><span class="sxs-lookup"><span data-stu-id="c97ea-131">The r, g and b components of *srcYDerivatives* (POS-swizzle) provide du/dy, dv/dy and dw/dy.</span></span> <span data-ttu-id="c97ea-132">O componente ' a ' (POS-swizzle) é ignorado.</span><span class="sxs-lookup"><span data-stu-id="c97ea-132">The 'a' component (POS-swizzle) is ignored.</span></span>

<span data-ttu-id="c97ea-133">Ao contrário da instrução de **exemplo** , que tem permissão para compartilhar um único cálculo de LOD em um carimbo 2x2, o **exemplo \_ d** deve calcular o LOD completamente de forma independente, por pixel, quando usado no sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="c97ea-133">Unlike the **sample** instruction, which is permitted to share a single LOD calculation across a 2x2 stamp, **sample\_d** must calculate LOD completely independently, per-pixel when used in the Pixel Shader.</span></span>

<span data-ttu-id="c97ea-134">Se as entradas derivadas para a **amostra \_ d** vieram de instruções de cálculo derivativo no sombreador de pixel e os valores incluírem inf/Nan, o comportamento do **exemplo \_ d** pode não corresponder à instrução de **exemplo** , que computa implicitamente a derivada.</span><span class="sxs-lookup"><span data-stu-id="c97ea-134">If the derivative inputs to **sample\_d** came from derivative calculation instructions in the Pixel Shader and the values include INF/NaN, the behavior of **sample\_d** may not match the **sample** instruction, which implicitly computes the derivative.</span></span> <span data-ttu-id="c97ea-135">Os valores INF/NaN podem afetar o cálculo de LOD de maneira diferente.</span><span class="sxs-lookup"><span data-stu-id="c97ea-135">The INF/NaN values may affect the LOD calculation differently.</span></span>

<span data-ttu-id="c97ea-136">A busca de um slot de entrada que não tem nada associado a ele retorna 0 para todos os componentes.</span><span class="sxs-lookup"><span data-stu-id="c97ea-136">Fetching from an input slot that has nothing bound to it returns 0 for all components.</span></span>

### <a name="restrictions"></a><span data-ttu-id="c97ea-137">Restrições</span><span class="sxs-lookup"><span data-stu-id="c97ea-137">Restrictions</span></span>

-   <span data-ttu-id="c97ea-138">o **exemplo \_ d** herda as mesmas restrições que a instrução de **exemplo** , além de uma restrição adicional abaixo para seus parâmetros adicionais.</span><span class="sxs-lookup"><span data-stu-id="c97ea-138">**sample\_d** inherits the same restrictions as the **sample** instruction, plus additional an restriction below for its additional parameters.</span></span>
-   <span data-ttu-id="c97ea-139">*srcXDerivatives* e *srcYDerivatives* devem ser temp (r \# /x \# ), constantBuffer (CB \# ), registros de entrada (v \# ) ou valor (es) imediato (s).</span><span class="sxs-lookup"><span data-stu-id="c97ea-139">*srcXDerivatives* and *srcYDerivatives* must be temp (r\#/x\#), constantBuffer (cb\#), input (v\#) registers or immediate value(s).</span></span>

<span data-ttu-id="c97ea-140">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="c97ea-140">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="c97ea-141">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="c97ea-141">Vertex Shader</span></span> | <span data-ttu-id="c97ea-142">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="c97ea-142">Geometry Shader</span></span> | <span data-ttu-id="c97ea-143">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="c97ea-143">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="c97ea-144">X</span><span class="sxs-lookup"><span data-stu-id="c97ea-144">X</span></span>             | <span data-ttu-id="c97ea-145">X</span><span class="sxs-lookup"><span data-stu-id="c97ea-145">X</span></span>               | <span data-ttu-id="c97ea-146">x</span><span class="sxs-lookup"><span data-stu-id="c97ea-146">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="c97ea-147">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="c97ea-147">Minimum Shader Model</span></span>

<span data-ttu-id="c97ea-148">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="c97ea-148">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="c97ea-149">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="c97ea-149">Shader Model</span></span>                                              | <span data-ttu-id="c97ea-150">Com suporte</span><span class="sxs-lookup"><span data-stu-id="c97ea-150">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="c97ea-151">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="c97ea-151">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="c97ea-152">sim</span><span class="sxs-lookup"><span data-stu-id="c97ea-152">yes</span></span>       |
| [<span data-ttu-id="c97ea-153">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="c97ea-153">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="c97ea-154">sim</span><span class="sxs-lookup"><span data-stu-id="c97ea-154">yes</span></span>       |
| [<span data-ttu-id="c97ea-155">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="c97ea-155">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="c97ea-156">sim</span><span class="sxs-lookup"><span data-stu-id="c97ea-156">yes</span></span>       |
| [<span data-ttu-id="c97ea-157">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c97ea-157">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="c97ea-158">não</span><span class="sxs-lookup"><span data-stu-id="c97ea-158">no</span></span>        |
| [<span data-ttu-id="c97ea-159">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c97ea-159">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="c97ea-160">não</span><span class="sxs-lookup"><span data-stu-id="c97ea-160">no</span></span>        |
| [<span data-ttu-id="c97ea-161">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c97ea-161">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="c97ea-162">não</span><span class="sxs-lookup"><span data-stu-id="c97ea-162">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="c97ea-163">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c97ea-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c97ea-164">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c97ea-164">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





