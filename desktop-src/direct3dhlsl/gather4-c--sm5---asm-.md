---
title: gather4_c (SM5-ASM)
description: O mesmo que gather4, exceto que esse instruting executa a comparação em texels, semelhante ao exemplo \_ c.
ms.assetid: 6265151A-36CE-4D31-B7B2-233CEEBDCF87
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35414aa2cd4d9f0686ab7a5cc17b94caa960cec1
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104988597"
---
# <a name="gather4_c-sm5---asm"></a><span data-ttu-id="f06d8-103">gather4 \_ c (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="f06d8-103">gather4\_c (sm5 - asm)</span></span>

<span data-ttu-id="f06d8-104">O mesmo que [**gather4**](gather4--sm5---asm-.md), exceto que esse instruting executa a comparação em texels, semelhante ao [**exemplo \_ c**](sample-c--sm4---asm-.md).</span><span class="sxs-lookup"><span data-stu-id="f06d8-104">Same as [**gather4**](gather4--sm5---asm-.md), except this instrution performs comparison on texels, similar to [**sample\_c**](sample-c--sm4---asm-.md).</span></span>



| <span data-ttu-id="f06d8-105">gather4 \_ c \[ \_ aoffimmi (u, v) \] dest \[ . Mask \] , srcAddress \[ . swizzle \] , srcResource \[ . swizzle \] , srcSampler \[ . R \] , srcReferenceValue</span><span class="sxs-lookup"><span data-stu-id="f06d8-105">gather4\_c\[\_aoffimmi(u,v)\] dest\[.mask\], srcAddress\[.swizzle\], srcResource\[.swizzle\], srcSampler\[.R\], srcReferenceValue</span></span> |
|-----------------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="f06d8-106">Item</span><span class="sxs-lookup"><span data-stu-id="f06d8-106">Item</span></span>                                                                                                                                       | <span data-ttu-id="f06d8-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="f06d8-107">Description</span></span>                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f06d8-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="f06d8-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                                            | <span data-ttu-id="f06d8-109">\[no \] endereço do resultado da operação</span><span class="sxs-lookup"><span data-stu-id="f06d8-109">\[in\] The address of the result of the operation</span></span><br/>                                    |
| <span data-ttu-id="f06d8-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span><span class="sxs-lookup"><span data-stu-id="f06d8-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>                             | <span data-ttu-id="f06d8-111">\[em \] um conjunto de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="f06d8-111">\[in\] A set of texture coordinates.</span></span><br/>                                                 |
| <span data-ttu-id="f06d8-112"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="f06d8-112"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/>                         | <span data-ttu-id="f06d8-113">\[em \] um registro de textura.</span><span class="sxs-lookup"><span data-stu-id="f06d8-113">\[in\] A texture register.</span></span><br/>                                                           |
| <span data-ttu-id="f06d8-114"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span><span class="sxs-lookup"><span data-stu-id="f06d8-114"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>                             | <span data-ttu-id="f06d8-115">\[em \] um registro de amostra.</span><span class="sxs-lookup"><span data-stu-id="f06d8-115">\[in\] A sampler register.</span></span><br/>                                                           |
| <span data-ttu-id="f06d8-116"><span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srcReferenceValue*</span><span class="sxs-lookup"><span data-stu-id="f06d8-116"><span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srcReferenceValue*</span></span><br/> | <span data-ttu-id="f06d8-117">\[em \] um registro com um único componente selecionado, que é usado na comparação.</span><span class="sxs-lookup"><span data-stu-id="f06d8-117">\[in\] A register with a single component selected, which is used in the comparison.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f06d8-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="f06d8-118">Remarks</span></span>

<span data-ttu-id="f06d8-119">Consulte [**exemplo \_ c**](sample-c--sm4---asm-.md) para obter uma descrição de como o *srcReferenceValue* é comparado com cada Texel buscada.</span><span class="sxs-lookup"><span data-stu-id="f06d8-119">See [**sample\_c**](sample-c--sm4---asm-.md) for a description of how *srcReferenceValue* gets compared against each fetched texel.</span></span> <span data-ttu-id="f06d8-120">Ao contrário do **exemplo \_ c**, **gather4 \_ c** retorna cada resultado da comparação, em vez de filtrá-los.</span><span class="sxs-lookup"><span data-stu-id="f06d8-120">Unlike **sample\_c**, **gather4\_c** returns each comparison result, rather than filtering them.</span></span>

<span data-ttu-id="f06d8-121">Para os cantos TextureCube, onde há três texels reais e a quarta deve ser sintetizada, a síntese deve ocorrer após a etapa de comparação.</span><span class="sxs-lookup"><span data-stu-id="f06d8-121">For TextureCube corners, where there are three real texels and a fourth must be synthesized, the synthesis must occur after the comparison step.</span></span> <span data-ttu-id="f06d8-122">Isso significa que o resultado de comparação retornado para o syntesized Texel pode ser 0, 0,33, 0,66 ou 1.</span><span class="sxs-lookup"><span data-stu-id="f06d8-122">This means the returned comparison result for the syntesized texel can be 0, 0.33 , 0.66 , or 1.</span></span> <span data-ttu-id="f06d8-123">Algumas implementações só podem retornar 0 ou 1 para o Texel sintetizado.</span><span class="sxs-lookup"><span data-stu-id="f06d8-123">Some implementations may only return either 0 or 1 for the synthesized texel.</span></span> <span data-ttu-id="f06d8-124">Além dessa listagem de possíveis resultados, o método para sintetizar o Texel não é especificado.</span><span class="sxs-lookup"><span data-stu-id="f06d8-124">Aside from this listing of possible results, the method for synthesizing the texel is unspecified.</span></span>

<span data-ttu-id="f06d8-125">Para formatos com componentes float32, se o valor que está sendo obtido for normalizado, ou +-INF, ele será usado na operação de comparação inalterada.</span><span class="sxs-lookup"><span data-stu-id="f06d8-125">For formats with float32 components, if the value being fetched is normalized, or +-INF, it is used in the comparison operation untouched.</span></span> <span data-ttu-id="f06d8-126">NaN é usado na operação de comparação como NaN, mas a representação de bit exata do NaN pode ser alterada.</span><span class="sxs-lookup"><span data-stu-id="f06d8-126">NaN is used in the comparison operation as NaN, but the exact bit representation of the NaN may be changed.</span></span> <span data-ttu-id="f06d8-127">As desnormas são liberadas para zero, indo para a comparação.</span><span class="sxs-lookup"><span data-stu-id="f06d8-127">Denorms are flushed to zero going into the comparison.</span></span> <span data-ttu-id="f06d8-128">Para TextureCubes, alguma síntese do 4º Texel ausente deve ocorrer nos cantos, portanto a noção de retorno de bits inalterado para o Texel sintetizado não se aplica.</span><span class="sxs-lookup"><span data-stu-id="f06d8-128">For TextureCubes, some synthesis of the missing 4th texel must occur at corners, so the notion of returning bits unchanged for the synthesized texel does not apply.</span></span>

<span data-ttu-id="f06d8-129">Os formatos com suporte para *gather4 \_ c* são iguais aos compatíveis com o *exemplo \_ c*.</span><span class="sxs-lookup"><span data-stu-id="f06d8-129">Formats supported for *gather4\_c* are same as those supported for *sample\_c*.</span></span> <span data-ttu-id="f06d8-130">Esses são formatos de componente único, portanto, o. R em *srcSampler*, em vez de um swizzle arbitrário.</span><span class="sxs-lookup"><span data-stu-id="f06d8-130">These are single-component formats, thus the .R on *srcSampler*, rather than an arbitrary swizzle.</span></span> <span data-ttu-id="f06d8-131">**gather4 \_ c** em um recurso não associado retorna 0.</span><span class="sxs-lookup"><span data-stu-id="f06d8-131">**gather4\_c** on an unbound resource returns 0.</span></span>

<span data-ttu-id="f06d8-132">Use esta instrução para filtrar o mapa de sombra personalizado.</span><span class="sxs-lookup"><span data-stu-id="f06d8-132">Use this instruction for custom shadow map filtering.</span></span>

<span data-ttu-id="f06d8-133">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="f06d8-133">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="f06d8-134">Vértice</span><span class="sxs-lookup"><span data-stu-id="f06d8-134">Vertex</span></span> | <span data-ttu-id="f06d8-135">Envoltória</span><span class="sxs-lookup"><span data-stu-id="f06d8-135">Hull</span></span> | <span data-ttu-id="f06d8-136">Domínio</span><span class="sxs-lookup"><span data-stu-id="f06d8-136">Domain</span></span> | <span data-ttu-id="f06d8-137">Geometria</span><span class="sxs-lookup"><span data-stu-id="f06d8-137">Geometry</span></span> | <span data-ttu-id="f06d8-138">16x16</span><span class="sxs-lookup"><span data-stu-id="f06d8-138">Pixel</span></span> | <span data-ttu-id="f06d8-139">Computação</span><span class="sxs-lookup"><span data-stu-id="f06d8-139">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="f06d8-140">X</span><span class="sxs-lookup"><span data-stu-id="f06d8-140">X</span></span>      | <span data-ttu-id="f06d8-141">X</span><span class="sxs-lookup"><span data-stu-id="f06d8-141">X</span></span>    | <span data-ttu-id="f06d8-142">X</span><span class="sxs-lookup"><span data-stu-id="f06d8-142">X</span></span>      | <span data-ttu-id="f06d8-143">X</span><span class="sxs-lookup"><span data-stu-id="f06d8-143">X</span></span>        | <span data-ttu-id="f06d8-144">X</span><span class="sxs-lookup"><span data-stu-id="f06d8-144">X</span></span>     | <span data-ttu-id="f06d8-145">X</span><span class="sxs-lookup"><span data-stu-id="f06d8-145">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="f06d8-146">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="f06d8-146">Minimum Shader Model</span></span>

<span data-ttu-id="f06d8-147">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="f06d8-147">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="f06d8-148">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="f06d8-148">Shader Model</span></span>                                              | <span data-ttu-id="f06d8-149">Com suporte</span><span class="sxs-lookup"><span data-stu-id="f06d8-149">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="f06d8-150">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="f06d8-150">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="f06d8-151">sim</span><span class="sxs-lookup"><span data-stu-id="f06d8-151">yes</span></span>       |
| [<span data-ttu-id="f06d8-152">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="f06d8-152">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="f06d8-153">não</span><span class="sxs-lookup"><span data-stu-id="f06d8-153">no</span></span>        |
| [<span data-ttu-id="f06d8-154">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="f06d8-154">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="f06d8-155">não</span><span class="sxs-lookup"><span data-stu-id="f06d8-155">no</span></span>        |
| [<span data-ttu-id="f06d8-156">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f06d8-156">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="f06d8-157">não</span><span class="sxs-lookup"><span data-stu-id="f06d8-157">no</span></span>        |
| [<span data-ttu-id="f06d8-158">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f06d8-158">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="f06d8-159">não</span><span class="sxs-lookup"><span data-stu-id="f06d8-159">no</span></span>        |
| [<span data-ttu-id="f06d8-160">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f06d8-160">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="f06d8-161">não</span><span class="sxs-lookup"><span data-stu-id="f06d8-161">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="f06d8-162">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f06d8-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f06d8-163">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f06d8-163">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





