---
title: sample_c (sm4-ASM)
description: Executa um filtro de comparação.
ms.assetid: 59786ED2-48FB-494E-A5A4-F732D63BF01B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23563fe52bbc943e8756d04085b66d156ab259d7
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104988569"
---
# <a name="sample_c-sm4---asm"></a><span data-ttu-id="c669a-103">exemplo \_ c (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="c669a-103">sample\_c (sm4 - asm)</span></span>

<span data-ttu-id="c669a-104">Executa um filtro de comparação.</span><span class="sxs-lookup"><span data-stu-id="c669a-104">Performs a comparison filter.</span></span>



| <span data-ttu-id="c669a-105">exemplo \_ c \[ \_ aoffimmi (u, v, w) \] dest \[ . Mask \] , srcAddress \[ . swizzle \] , srcResource. r,//deve ser. r swizzle srcSampler, srcReferenceValue//componente único selecionado</span><span class="sxs-lookup"><span data-stu-id="c669a-105">sample\_c\[\_aoffimmi(u,v,w)\] dest\[.mask\], srcAddress\[.swizzle\], srcResource.r, // must be .r swizzle srcSampler, srcReferenceValue // single component selected</span></span> |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="c669a-106">Item</span><span class="sxs-lookup"><span data-stu-id="c669a-106">Item</span></span>                                                                                                                                       | <span data-ttu-id="c669a-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="c669a-107">Description</span></span>                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c669a-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="c669a-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                                            | <span data-ttu-id="c669a-109">\[no \] endereço dos resultados da operação.</span><span class="sxs-lookup"><span data-stu-id="c669a-109">\[in\] The address of the results of the operation.</span></span><br/>                                                             |
| <span data-ttu-id="c669a-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span><span class="sxs-lookup"><span data-stu-id="c669a-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>                             | <span data-ttu-id="c669a-111">\[em \] um conjunto de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="c669a-111">\[in\] A set of texture coordinates.</span></span> <span data-ttu-id="c669a-112">Para obter mais informações, consulte a instrução de [exemplo](sample--sm4---asm-.md) .</span><span class="sxs-lookup"><span data-stu-id="c669a-112">For more information see the [sample](sample--sm4---asm-.md) instruction.</span></span><br/> |
| <span data-ttu-id="c669a-113"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="c669a-113"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/>                         | <span data-ttu-id="c669a-114">\[em \] um registro de textura.</span><span class="sxs-lookup"><span data-stu-id="c669a-114">\[in\] A texture register.</span></span> <span data-ttu-id="c669a-115">Para obter mais informações, consulte a instrução de **exemplo** .</span><span class="sxs-lookup"><span data-stu-id="c669a-115">For more information see the **sample** instruction.</span></span><br/>                                 |
| <span data-ttu-id="c669a-116"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span><span class="sxs-lookup"><span data-stu-id="c669a-116"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>                             | <span data-ttu-id="c669a-117">\[em \] um registro de amostra.</span><span class="sxs-lookup"><span data-stu-id="c669a-117">\[in\] A sampler register.</span></span> <span data-ttu-id="c669a-118">Para obter mais informações, consulte a instrução de **exemplo** .</span><span class="sxs-lookup"><span data-stu-id="c669a-118">For more information see the **sample** instruction.</span></span><br/>                                 |
| <span data-ttu-id="c669a-119"><span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srcReferenceValue*</span><span class="sxs-lookup"><span data-stu-id="c669a-119"><span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srcReferenceValue*</span></span><br/> | <span data-ttu-id="c669a-120">\[em \] um registro com um único componente selecionado, que é usado na comparação.</span><span class="sxs-lookup"><span data-stu-id="c669a-120">\[in\] A register with a single component selected, which is used in the comparison.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="c669a-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="c669a-121">Remarks</span></span>

<span data-ttu-id="c669a-122">A principal finalidade dessa instrução é fornecer um bloco de construção para a filtragem de profundidade Percentage-Closer.</span><span class="sxs-lookup"><span data-stu-id="c669a-122">The primary purpose for this instruction is to provide a building-block for Percentage-Closer Depth filtering.</span></span> <span data-ttu-id="c669a-123">O "c" no **exemplo \_ c** significa comparação.</span><span class="sxs-lookup"><span data-stu-id="c669a-123">The "c" in **sample\_c** stands for Comparison.</span></span>

<span data-ttu-id="c669a-124">Os operandos para a **amostra \_ c** são idênticos à instrução de [exemplo](sample--sm4---asm-.md) , exceto pelo fato de que há um operando de origem float32 adicional, *srcReferenceValue*, que deve ser um registro com um único componente selecionado ou um literal escalar.</span><span class="sxs-lookup"><span data-stu-id="c669a-124">The operands to **sample\_c** are identical to the [sample](sample--sm4---asm-.md) instruction, except that there is an additional float32 source operand, *srcReferenceValue*, which must be a register with single-component selected, or a scalar literal.</span></span>

<span data-ttu-id="c669a-125">O parâmetro *srcResource* deve ter um swizzle. r (vermelho).</span><span class="sxs-lookup"><span data-stu-id="c669a-125">The *srcResource* parameter must have a .r (red) swizzle.</span></span> <span data-ttu-id="c669a-126">o **exemplo \_ c** funciona exclusivamente no componente vermelho e retorna um único valor.</span><span class="sxs-lookup"><span data-stu-id="c669a-126">**sample\_c** operates exclusively on the red component, and returns a single value.</span></span> <span data-ttu-id="c669a-127">O. r swizzle em *srcResource* indica que o resultado escalar é replicado para todos os componentes.</span><span class="sxs-lookup"><span data-stu-id="c669a-127">The .r swizzle on *srcResource* indicates that the scalar result is replicated to all components.</span></span>

<span data-ttu-id="c669a-128">Quando um buffer de profundidade é definido como uma textura de entrada, o valor de profundidade aparece no componente vermelho.</span><span class="sxs-lookup"><span data-stu-id="c669a-128">When a Depth Buffer is set as an input texture, the depth value shows up in the red component.</span></span>

<span data-ttu-id="c669a-129">Se essa instrução for usada com um recurso que não seja um Texture1D/2D/2DArray/Cube/CubeArray, ele produzirá resultados indefinidos.</span><span class="sxs-lookup"><span data-stu-id="c669a-129">If this instruction is used with a Resource that is not a Texture1D/2D/2DArray/Cube/CubeArray, it produces undefined results.</span></span>

<span data-ttu-id="c669a-130">Quando essa instrução é executada, o hardware de amostragem usa o ComparisonFunction da amostra atual para comparar *srcReferenceValue* com o valor do componente vermelho para o recurso de origem em cada filtro "toque" (Texel) que o filtro de textura configurado atualmente abrange, com base nas coordenadas fornecidas em *srcAddress*.</span><span class="sxs-lookup"><span data-stu-id="c669a-130">When this instruction is executed, the sampling hardware uses the current Sampler's ComparisonFunction to compare *srcReferenceValue* against the Red component value for the source Resource at each filter "tap" location (texel) that the currently configured texture filter covers, based on the provided coordinates in *srcAddress*.</span></span>

<span data-ttu-id="c669a-131">A comparação ocorre depois que *srcReferenceValue* tem sido quantificado para a precisão do formato de textura, exatamente da mesma forma que z é quantificado para profundidade de buffer de intensidade antes da comparação de profundidade no teste de visibilidade da fusão de saída.</span><span class="sxs-lookup"><span data-stu-id="c669a-131">The comparison occurs after *srcReferenceValue* has been quantized to the precision of the texture format, in exactly the same way that z is quantized to depth buffer precision before Depth Comparison at the Output Merger visibility test.</span></span> <span data-ttu-id="c669a-132">Isso inclui um fixe para o intervalo de formato (por exemplo, \[ 0.. 1 \] para um formato UNORM).</span><span class="sxs-lookup"><span data-stu-id="c669a-132">This includes a clamp to the format range (e.g. \[0..1\] for a UNORM format).</span></span>

<span data-ttu-id="c669a-133">O componente vermelho do Texel de origem é comparado com o *srcReferenceValue* quantificado.</span><span class="sxs-lookup"><span data-stu-id="c669a-133">The source texel's Red component is compared against the quantized *srcReferenceValue*.</span></span> <span data-ttu-id="c669a-134">Para texels que estão fora do recurso, o valor do componente vermelho é determinado pela aplicação dos modos de endereço (e de BorderColor, se estiver no modo de borda) do amostra.</span><span class="sxs-lookup"><span data-stu-id="c669a-134">For texels that fall off the Resource, the Red component value is determined by applying the Address Modes (and BorderColorR if in Border mode) from the Sampler.</span></span> <span data-ttu-id="c669a-135">A comparação honra todas as regras de comparação de ponto flutuante D3D11, no caso de o formato de textura ser ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="c669a-135">The comparison honors all D3D11 floating point comparison rules, in the case the texture format is floating point.</span></span>

<span data-ttu-id="c669a-136">Cada comparação que passa retorna 1,0 f como o valor do componente vermelho para o Texel e cada comparação que falha retorna 0,0 f como o valor vermelho para a textura.</span><span class="sxs-lookup"><span data-stu-id="c669a-136">Each comparison that passes returns 1.0f as the Red component value for the texel, and each comparison that fails returns 0.0f as the Red value for the texture.</span></span> <span data-ttu-id="c669a-137">Em seguida, a filtragem ocorre exatamente conforme especificado pelos Estados de amostra, operando apenas no componente vermelho e retornando um único resultado de filtro escalar de volta para o sombreador, replicado para todos os componentes de *dest* mascarados.</span><span class="sxs-lookup"><span data-stu-id="c669a-137">Filtering then occurs exactly as specified by the Sampler states, operating only in the Red component, and returning a single scalar filter result back to the Shader, replicated to all masked *dest* components.</span></span>

<span data-ttu-id="c669a-138">O uso da **amostra \_ c** é ortogonal a todos os outros controles de filtragem de uso geral.</span><span class="sxs-lookup"><span data-stu-id="c669a-138">The use of **sample\_c** is orthogonal to all other general purpose filtering controls.</span></span> <span data-ttu-id="c669a-139">o **exemplo \_ c** funciona diretamente com os outros modos de filtro de uso geral.</span><span class="sxs-lookup"><span data-stu-id="c669a-139">**sample\_c** works seamlessly with the other general purpose filter modes.</span></span> <span data-ttu-id="c669a-140">o **exemplo \_ c** altera o comportamento dos filtros de uso geral, de modo que os valores que estão sendo filtrados se tornem 1,0 f ou 0,0 f devido aos resultados da comparação.</span><span class="sxs-lookup"><span data-stu-id="c669a-140">**sample\_c** changes the behavior of the general purpose filters such that the values being filtered all become 1.0f or 0.0f due to comparison results.</span></span>

<span data-ttu-id="c669a-141">A busca de um slot de entrada que não tem nada associado a ele retorna 0 para todos os componentes.</span><span class="sxs-lookup"><span data-stu-id="c669a-141">Fetching from an input slot that has nothing bound to it returns 0 for all components.</span></span>

<span data-ttu-id="c669a-142">Para obter mais informações, consulte a instrução de [exemplo](sample--sm4---asm-.md) .</span><span class="sxs-lookup"><span data-stu-id="c669a-142">For more information, see the [sample](sample--sm4---asm-.md) instruction.</span></span>

<span data-ttu-id="c669a-143">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="c669a-143">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="c669a-144">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="c669a-144">Vertex Shader</span></span> | <span data-ttu-id="c669a-145">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="c669a-145">Geometry Shader</span></span> | <span data-ttu-id="c669a-146">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="c669a-146">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               |                 | <span data-ttu-id="c669a-147">x</span><span class="sxs-lookup"><span data-stu-id="c669a-147">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="c669a-148">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="c669a-148">Minimum Shader Model</span></span>

<span data-ttu-id="c669a-149">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="c669a-149">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="c669a-150">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="c669a-150">Shader Model</span></span>                                              | <span data-ttu-id="c669a-151">Com suporte</span><span class="sxs-lookup"><span data-stu-id="c669a-151">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="c669a-152">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="c669a-152">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="c669a-153">sim</span><span class="sxs-lookup"><span data-stu-id="c669a-153">yes</span></span>       |
| [<span data-ttu-id="c669a-154">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="c669a-154">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="c669a-155">sim</span><span class="sxs-lookup"><span data-stu-id="c669a-155">yes</span></span>       |
| [<span data-ttu-id="c669a-156">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="c669a-156">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="c669a-157">sim</span><span class="sxs-lookup"><span data-stu-id="c669a-157">yes</span></span>       |
| [<span data-ttu-id="c669a-158">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c669a-158">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="c669a-159">não</span><span class="sxs-lookup"><span data-stu-id="c669a-159">no</span></span>        |
| [<span data-ttu-id="c669a-160">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c669a-160">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="c669a-161">não</span><span class="sxs-lookup"><span data-stu-id="c669a-161">no</span></span>        |
| [<span data-ttu-id="c669a-162">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c669a-162">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="c669a-163">não</span><span class="sxs-lookup"><span data-stu-id="c669a-163">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="c669a-164">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c669a-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c669a-165">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c669a-165">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





