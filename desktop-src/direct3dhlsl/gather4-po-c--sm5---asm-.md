---
title: gather4_po_c (SM5-ASM)
description: Comporta-se da mesma forma que gather4 \_ Po, exceto realiza a comparação em texels, semelhante ao exemplo \_ c.
ms.assetid: B128EEF3-3440-4F00-9792-20FB1AE075E9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36b07dcad08b4d117a453a3c97e461e6b9b4cab6
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104365264"
---
# <a name="gather4_po_c-sm5---asm"></a><span data-ttu-id="bb4d0-103">gather4 \_ po \_ c (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="bb4d0-103">gather4\_po\_c (sm5 - asm)</span></span>

<span data-ttu-id="bb4d0-104">Comporta-se da mesma forma que [**gather4 \_ po**](gather4-po--sm5---asm-.md), exceto realiza a comparação em texels, semelhante ao [**exemplo \_ c**](sample-c--sm4---asm-.md).</span><span class="sxs-lookup"><span data-stu-id="bb4d0-104">Behaves the same as [**gather4\_po**](gather4-po--sm5---asm-.md), except performs comparison on texels, similar to [**sample\_c**](sample-c--sm4---asm-.md).</span></span>



| <span data-ttu-id="bb4d0-105">gather4 \_ po \_ c dest \[ . Mask \] , srcAddress \[ . swizzle \] , srcOffset \[ . swizzle \] , srcResource \[ . swizzle \] , srcSampler \[ . R \] , srcReferenceValue</span><span class="sxs-lookup"><span data-stu-id="bb4d0-105">gather4\_po\_c dest\[.mask\], srcAddress\[.swizzle\], srcOffset\[.swizzle\], srcResource\[.swizzle\], srcSampler\[.R\], srcReferenceValue</span></span> |
|-------------------------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="bb4d0-106">Item</span><span class="sxs-lookup"><span data-stu-id="bb4d0-106">Item</span></span>                                                                                                                                       | <span data-ttu-id="bb4d0-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="bb4d0-107">Description</span></span>                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="bb4d0-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="bb4d0-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                                            | <span data-ttu-id="bb4d0-109">\[no \] endereço do resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="bb4d0-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="bb4d0-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span><span class="sxs-lookup"><span data-stu-id="bb4d0-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>                             | <span data-ttu-id="bb4d0-111">\[em \] um conjunto de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="bb4d0-111">\[in\] A set of texture coordinates.</span></span><br/>               |
| <span data-ttu-id="bb4d0-112"><span id="srcOffset"></span><span id="srcoffset"></span><span id="SRCOFFSET"></span>*srcOffset*</span><span class="sxs-lookup"><span data-stu-id="bb4d0-112"><span id="srcOffset"></span><span id="srcoffset"></span><span id="SRCOFFSET"></span>*srcOffset*</span></span><br/>                                 | <span data-ttu-id="bb4d0-113">\[no \] deslocamento.</span><span class="sxs-lookup"><span data-stu-id="bb4d0-113">\[in\] The offset.</span></span><br/>                                 |
| <span data-ttu-id="bb4d0-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="bb4d0-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/>                         | <span data-ttu-id="bb4d0-115">\[em \] um registro de textura.</span><span class="sxs-lookup"><span data-stu-id="bb4d0-115">\[in\] A texture register.</span></span><br/>                         |
| <span data-ttu-id="bb4d0-116"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span><span class="sxs-lookup"><span data-stu-id="bb4d0-116"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>                             | <span data-ttu-id="bb4d0-117">\[em \] um registro de amostra.</span><span class="sxs-lookup"><span data-stu-id="bb4d0-117">\[in\] A sampler register.</span></span><br/>                         |
| <span data-ttu-id="bb4d0-118"><span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srcReferenceValue*</span><span class="sxs-lookup"><span data-stu-id="bb4d0-118"><span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srcReferenceValue*</span></span><br/> | <span data-ttu-id="bb4d0-119">\[em \] um único componente selecionado.</span><span class="sxs-lookup"><span data-stu-id="bb4d0-119">\[in\] Single component selected.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="bb4d0-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="bb4d0-120">Remarks</span></span>

<span data-ttu-id="bb4d0-121">Consulte [**exemplo \_ c**](sample-c--sm4---asm-.md) para obter informações sobre como o *srcReferenceValue* é comparado com cada Texel buscada.</span><span class="sxs-lookup"><span data-stu-id="bb4d0-121">See [**sample\_c**](sample-c--sm4---asm-.md) for information about how *srcReferenceValue* is compared against each fetched texel.</span></span> <span data-ttu-id="bb4d0-122">Ao contrário do **exemplo \_ c**, o *gather4 \_ po \_ c* retorna cada resultado da comparação, em vez de filtrá-los.</span><span class="sxs-lookup"><span data-stu-id="bb4d0-122">Unlike **sample\_c**, *gather4\_po\_c* returns each comparison result, rather than filtering them.</span></span>

<span data-ttu-id="bb4d0-123">Essa instrução, como o **gather4 \_ po**, funciona apenas com texturas 2D.</span><span class="sxs-lookup"><span data-stu-id="bb4d0-123">This instruction, like **gather4\_po**, only works with 2D textures.</span></span> <span data-ttu-id="bb4d0-124">Isso é diferente de [**gather4 \_ c**](gather4-c--sm5---asm-.md), que também funciona com TextureCubes.</span><span class="sxs-lookup"><span data-stu-id="bb4d0-124">This is unlike [**gather4\_c**](gather4-c--sm5---asm-.md), which also works with TextureCubes.</span></span>

<span data-ttu-id="bb4d0-125">Para formatos com componentes float32, se o valor que está sendo obtido for normalizado, ou +-INF, ele será usado na operação de comparação inalterada.</span><span class="sxs-lookup"><span data-stu-id="bb4d0-125">For formats with float32 components, if the value being fetched is normalized, or +-INF, it is used in the comparison operation untouched.</span></span> <span data-ttu-id="bb4d0-126">NaN é usado na operação de comparação como NaN, mas a representação de bit exata do NaN pode ser alterada.</span><span class="sxs-lookup"><span data-stu-id="bb4d0-126">NaN is used in the comparison operation as NaN, but the exact bit representation of the NaN may be changed.</span></span> <span data-ttu-id="bb4d0-127">As desnormas são liberadas para zero, indo para a comparação.</span><span class="sxs-lookup"><span data-stu-id="bb4d0-127">Denorms are flushed to zero going into the comparison.</span></span> <span data-ttu-id="bb4d0-128">Para TextureCubes, alguma síntese do 4º Texel ausente deve ocorrer nos cantos, portanto a noção de retorno de bits inalterado para o Texel sintetizado não se aplica.</span><span class="sxs-lookup"><span data-stu-id="bb4d0-128">For TextureCubes, some synthesis of the missing 4th texel must occur at corners, so the notion of returning bits unchanged for the synthesized texel does not apply.</span></span>

<span data-ttu-id="bb4d0-129">Os formatos com suporte para a **\_ OC \_ c gather4** são iguais aos compatíveis com o **exemplo \_ c**.</span><span class="sxs-lookup"><span data-stu-id="bb4d0-129">Formats supported for **gather4\_po\_c** are same as those supported for **sample\_c**.</span></span> <span data-ttu-id="bb4d0-130">Esses são formatos de componente único, portanto, o. R em srcSampler, em vez de um swizzle arbitrário.</span><span class="sxs-lookup"><span data-stu-id="bb4d0-130">These are single-component formats, thus the .R on srcSampler, rather than an arbitrary swizzle.</span></span>

<span data-ttu-id="bb4d0-131">o **gather4 \_ po \_ c** em um recurso não associado retorna 0.</span><span class="sxs-lookup"><span data-stu-id="bb4d0-131">**gather4\_po\_c** on an unbound resource returns 0.</span></span>

<span data-ttu-id="bb4d0-132">Use este método para filtragem de mapa de sombra.</span><span class="sxs-lookup"><span data-stu-id="bb4d0-132">Use this method for shadow map filtering.</span></span>

<span data-ttu-id="bb4d0-133">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="bb4d0-133">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="bb4d0-134">Vértice</span><span class="sxs-lookup"><span data-stu-id="bb4d0-134">Vertex</span></span> | <span data-ttu-id="bb4d0-135">Envoltória</span><span class="sxs-lookup"><span data-stu-id="bb4d0-135">Hull</span></span> | <span data-ttu-id="bb4d0-136">Domínio</span><span class="sxs-lookup"><span data-stu-id="bb4d0-136">Domain</span></span> | <span data-ttu-id="bb4d0-137">Geometria</span><span class="sxs-lookup"><span data-stu-id="bb4d0-137">Geometry</span></span> | <span data-ttu-id="bb4d0-138">16x16</span><span class="sxs-lookup"><span data-stu-id="bb4d0-138">Pixel</span></span> | <span data-ttu-id="bb4d0-139">Computação</span><span class="sxs-lookup"><span data-stu-id="bb4d0-139">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="bb4d0-140">X</span><span class="sxs-lookup"><span data-stu-id="bb4d0-140">X</span></span>      | <span data-ttu-id="bb4d0-141">X</span><span class="sxs-lookup"><span data-stu-id="bb4d0-141">X</span></span>    | <span data-ttu-id="bb4d0-142">X</span><span class="sxs-lookup"><span data-stu-id="bb4d0-142">X</span></span>      | <span data-ttu-id="bb4d0-143">X</span><span class="sxs-lookup"><span data-stu-id="bb4d0-143">X</span></span>        | <span data-ttu-id="bb4d0-144">X</span><span class="sxs-lookup"><span data-stu-id="bb4d0-144">X</span></span>     | <span data-ttu-id="bb4d0-145">X</span><span class="sxs-lookup"><span data-stu-id="bb4d0-145">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="bb4d0-146">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="bb4d0-146">Minimum Shader Model</span></span>

<span data-ttu-id="bb4d0-147">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="bb4d0-147">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="bb4d0-148">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="bb4d0-148">Shader Model</span></span>                                              | <span data-ttu-id="bb4d0-149">Com suporte</span><span class="sxs-lookup"><span data-stu-id="bb4d0-149">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="bb4d0-150">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="bb4d0-150">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="bb4d0-151">sim</span><span class="sxs-lookup"><span data-stu-id="bb4d0-151">yes</span></span>       |
| [<span data-ttu-id="bb4d0-152">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="bb4d0-152">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="bb4d0-153">não</span><span class="sxs-lookup"><span data-stu-id="bb4d0-153">no</span></span>        |
| [<span data-ttu-id="bb4d0-154">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="bb4d0-154">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="bb4d0-155">não</span><span class="sxs-lookup"><span data-stu-id="bb4d0-155">no</span></span>        |
| [<span data-ttu-id="bb4d0-156">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bb4d0-156">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="bb4d0-157">não</span><span class="sxs-lookup"><span data-stu-id="bb4d0-157">no</span></span>        |
| [<span data-ttu-id="bb4d0-158">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bb4d0-158">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="bb4d0-159">não</span><span class="sxs-lookup"><span data-stu-id="bb4d0-159">no</span></span>        |
| [<span data-ttu-id="bb4d0-160">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bb4d0-160">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="bb4d0-161">não</span><span class="sxs-lookup"><span data-stu-id="bb4d0-161">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="bb4d0-162">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bb4d0-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bb4d0-163">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bb4d0-163">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





