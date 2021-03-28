---
title: sample_b (sm4-ASM)
description: Amostras de dados do elemento/textura especificado usando o endereço especificado e o modo de filtragem identificados pelo determinado exemplo. | sample_b (sm4-ASM)
ms.assetid: FC0DF03E-9C21-4E88-96ED-EEFE86017E7C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72e82696ecc5b01847f87b39cbfeba0c665bcde4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104172811"
---
# <a name="sample_b-sm4---asm"></a><span data-ttu-id="ebc2c-104">exemplo \_ b (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="ebc2c-104">sample\_b (sm4 - asm)</span></span>

<span data-ttu-id="ebc2c-105">Amostras de dados do elemento/textura especificado usando o endereço especificado e o modo de filtragem identificados pelo determinado exemplo.</span><span class="sxs-lookup"><span data-stu-id="ebc2c-105">Samples data from the specified Element/texture using the specified address and the filtering mode identified by the given sampler.</span></span>



| <span data-ttu-id="ebc2c-106">exemplo \_ b \[ \_ aoffimmi (u, v, w) \] dest \[ . Mask \] , srcAddress \[ . swizzle \] , srcResource \[ . swizzle \] , srcSampler e srcLODBias. Select \_ componente</span><span class="sxs-lookup"><span data-stu-id="ebc2c-106">sample\_b\[\_aoffimmi(u,v,w)\] dest\[.mask\], srcAddress\[.swizzle\], srcResource\[.swizzle\], srcSampler, srcLODBias.select\_component</span></span> |
|-----------------------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="ebc2c-107">Item</span><span class="sxs-lookup"><span data-stu-id="ebc2c-107">Item</span></span>                                                                                                               | <span data-ttu-id="ebc2c-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="ebc2c-108">Description</span></span>                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ebc2c-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="ebc2c-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="ebc2c-110">\[no \] endereço do resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="ebc2c-110">\[in\] The address of the result of the operation.</span></span><br/>                                                              |
| <span data-ttu-id="ebc2c-111"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span><span class="sxs-lookup"><span data-stu-id="ebc2c-111"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>     | <span data-ttu-id="ebc2c-112">\[em \] um conjunto de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="ebc2c-112">\[in\] A set of texture coordinates.</span></span> <span data-ttu-id="ebc2c-113">Para obter mais informações, consulte a instrução de [exemplo](sample--sm4---asm-.md) .</span><span class="sxs-lookup"><span data-stu-id="ebc2c-113">For more information see the [sample](sample--sm4---asm-.md) instruction.</span></span><br/> |
| <span data-ttu-id="ebc2c-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="ebc2c-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="ebc2c-115">\[em \] um registro de textura.</span><span class="sxs-lookup"><span data-stu-id="ebc2c-115">\[in\] A texture register.</span></span> <span data-ttu-id="ebc2c-116">Para obter mais informações, consulte a instrução de **exemplo** .</span><span class="sxs-lookup"><span data-stu-id="ebc2c-116">For more information see the **sample** instruction.</span></span><br/>                                 |
| <span data-ttu-id="ebc2c-117"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span><span class="sxs-lookup"><span data-stu-id="ebc2c-117"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>     | <span data-ttu-id="ebc2c-118">\[em \] um registro de amostra.</span><span class="sxs-lookup"><span data-stu-id="ebc2c-118">\[in\] A sampler register.</span></span> <span data-ttu-id="ebc2c-119">Para obter mais informações, consulte a instrução de **exemplo** .</span><span class="sxs-lookup"><span data-stu-id="ebc2c-119">For more information see the **sample** instruction.</span></span><br/>                                 |
| <span data-ttu-id="ebc2c-120"><span id="srcLODBias"></span><span id="srclodbias"></span><span id="SRCLODBIAS"></span>*srcLODBias*</span><span class="sxs-lookup"><span data-stu-id="ebc2c-120"><span id="srcLODBias"></span><span id="srclodbias"></span><span id="SRCLODBIAS"></span>*srcLODBias*</span></span><br/>     | <span data-ttu-id="ebc2c-121">\[em \] consulte a seção **comentários** para obter informações sobre esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="ebc2c-121">\[in\] See the **Remarks** section for information about this parameter.</span></span><br/>                                        |



 

## <a name="remarks"></a><span data-ttu-id="ebc2c-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="ebc2c-122">Remarks</span></span>

<span data-ttu-id="ebc2c-123">Os dados de origem podem vir de qualquer tipo de recurso, além de buffers.</span><span class="sxs-lookup"><span data-stu-id="ebc2c-123">The source data may come from any Resource Type, other than Buffers.</span></span> <span data-ttu-id="ebc2c-124">Uma diferença adicional é aplicada ao nível de detalhes calculados como parte da execução da instrução.</span><span class="sxs-lookup"><span data-stu-id="ebc2c-124">An additional bias is applied to the level of detail computed as part of the instruction execution.</span></span>

<span data-ttu-id="ebc2c-125">Essa instrução se comporta como a instrução de [exemplo](sample--sm4---asm-.md) com a adição de aplicar o valor *srcLODBias* especificado ao nível de valor de detalhe calculado como parte da execução de instrução antes de selecionar o (s) mapa (es) MIP.</span><span class="sxs-lookup"><span data-stu-id="ebc2c-125">This instruction behaves like the [sample](sample--sm4---asm-.md) instruction with the addition of applying the specified *srcLODBias* value to the level of detail value computed as part of the instruction execution prior to selecting the mip map(s).</span></span> <span data-ttu-id="ebc2c-126">O valor de *srcLODBias* é adicionado ao LOD computado por pixel, juntamente com o valor de MipLODBias de amostra, antes do fixe para MinLOD e MaxLOD.</span><span class="sxs-lookup"><span data-stu-id="ebc2c-126">The *srcLODBias* value is added to the computed LOD on a per-pixel basis, along with the sampler MipLODBias value, prior to the clamp to MinLOD and MaxLOD.</span></span>

### <a name="restrictions"></a><span data-ttu-id="ebc2c-127">Restrições</span><span class="sxs-lookup"><span data-stu-id="ebc2c-127">Restrictions</span></span>

-   <span data-ttu-id="ebc2c-128">o **exemplo \_ b** herda as mesmas restrições que a instrução de [exemplo](sample--sm4---asm-.md) , além de restrições adicionais para seu parâmetro adicional.</span><span class="sxs-lookup"><span data-stu-id="ebc2c-128">**sample\_b** inherits the same restrictions as the [sample](sample--sm4---asm-.md) instruction, plus additional restrictions for its additional parameter.</span></span>
-   <span data-ttu-id="ebc2c-129">O intervalo de *srcLODBias* é (-16.0 f a 15.99 f); os valores fora desse intervalo produzirão resultados indefinidos.</span><span class="sxs-lookup"><span data-stu-id="ebc2c-129">The range of *srcLODBias* is (-16.0f to 15.99f); values outside of this range will produce undefined results.</span></span>
-   <span data-ttu-id="ebc2c-130">*srcLODBias* deve usar um seletor de componente único se não for um escalar imediato.</span><span class="sxs-lookup"><span data-stu-id="ebc2c-130">*srcLODBias* must use a single component selector if it is not a scalar immediate.</span></span>

<span data-ttu-id="ebc2c-131">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="ebc2c-131">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="ebc2c-132">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="ebc2c-132">Vertex Shader</span></span> | <span data-ttu-id="ebc2c-133">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="ebc2c-133">Geometry Shader</span></span> | <span data-ttu-id="ebc2c-134">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="ebc2c-134">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               |                 | <span data-ttu-id="ebc2c-135">x</span><span class="sxs-lookup"><span data-stu-id="ebc2c-135">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="ebc2c-136">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="ebc2c-136">Minimum Shader Model</span></span>

<span data-ttu-id="ebc2c-137">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="ebc2c-137">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="ebc2c-138">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="ebc2c-138">Shader Model</span></span>                                              | <span data-ttu-id="ebc2c-139">Com suporte</span><span class="sxs-lookup"><span data-stu-id="ebc2c-139">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="ebc2c-140">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="ebc2c-140">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="ebc2c-141">sim</span><span class="sxs-lookup"><span data-stu-id="ebc2c-141">yes</span></span>       |
| [<span data-ttu-id="ebc2c-142">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="ebc2c-142">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="ebc2c-143">sim</span><span class="sxs-lookup"><span data-stu-id="ebc2c-143">yes</span></span>       |
| [<span data-ttu-id="ebc2c-144">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="ebc2c-144">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="ebc2c-145">sim</span><span class="sxs-lookup"><span data-stu-id="ebc2c-145">yes</span></span>       |
| [<span data-ttu-id="ebc2c-146">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ebc2c-146">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="ebc2c-147">não</span><span class="sxs-lookup"><span data-stu-id="ebc2c-147">no</span></span>        |
| [<span data-ttu-id="ebc2c-148">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ebc2c-148">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="ebc2c-149">não</span><span class="sxs-lookup"><span data-stu-id="ebc2c-149">no</span></span>        |
| [<span data-ttu-id="ebc2c-150">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ebc2c-150">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="ebc2c-151">não</span><span class="sxs-lookup"><span data-stu-id="ebc2c-151">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="ebc2c-152">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ebc2c-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ebc2c-153">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ebc2c-153">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





