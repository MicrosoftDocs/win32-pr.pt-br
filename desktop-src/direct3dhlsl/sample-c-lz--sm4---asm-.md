---
title: sample_c_lz (sm4-ASM)
description: Executa um filtro de comparação. Essa instrução se comporta como exemplo \_ c, exceto que LOD é 0 e derivações são ignoradas.
ms.assetid: 5F11F091-AF2F-4293-88C7-824F11FE01E4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24ec2889dd3ea4c86af51c8e36bf2e302c6ad4dd
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104365223"
---
# <a name="sample_c_lz-sm4---asm"></a><span data-ttu-id="c6144-104">exemplo \_ c \_ LZ (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="c6144-104">sample\_c\_lz (sm4 - asm)</span></span>

<span data-ttu-id="c6144-105">Executa um filtro de comparação.</span><span class="sxs-lookup"><span data-stu-id="c6144-105">Performs a comparison filter.</span></span> <span data-ttu-id="c6144-106">Essa instrução se comporta como [exemplo \_ c](sample-c--sm4---asm-.md), exceto que LOD é 0 e derivações são ignoradas.</span><span class="sxs-lookup"><span data-stu-id="c6144-106">This instruction behaves like [sample\_c](sample-c--sm4---asm-.md), except LOD is 0, and derivatives are ignored.</span></span>



| <span data-ttu-id="c6144-107">exemplo \_ c \_ LZ \[ \_ aoffimmi (u, v, w) \] dest \[ . Mask \] , srcAddress \[ . swizzle \] , srcResource. r,//deve ser. r swizzle srcSampler, srcReferenceValue//componente único selecionado</span><span class="sxs-lookup"><span data-stu-id="c6144-107">sample\_c\_lz\[\_aoffimmi(u,v,w)\] dest\[.mask\], srcAddress\[.swizzle\], srcResource.r, // must be .r swizzle srcSampler, srcReferenceValue // single component selected</span></span> |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="c6144-108">Item</span><span class="sxs-lookup"><span data-stu-id="c6144-108">Item</span></span>                                                                                                                                       | <span data-ttu-id="c6144-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="c6144-109">Description</span></span>                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6144-110"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="c6144-110"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                                            | <span data-ttu-id="c6144-111">\[no \] endereço dos resultados da operação.</span><span class="sxs-lookup"><span data-stu-id="c6144-111">\[in\] The address of the results of the operation.</span></span><br/>                                                             |
| <span data-ttu-id="c6144-112"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span><span class="sxs-lookup"><span data-stu-id="c6144-112"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>                             | <span data-ttu-id="c6144-113">\[em \] um conjunto de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="c6144-113">\[in\] A set of texture coordinates.</span></span> <span data-ttu-id="c6144-114">Para obter mais informações, consulte a instrução de [exemplo](sample--sm4---asm-.md) .</span><span class="sxs-lookup"><span data-stu-id="c6144-114">For more information see the [sample](sample--sm4---asm-.md) instruction.</span></span><br/> |
| <span data-ttu-id="c6144-115"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="c6144-115"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/>                         | <span data-ttu-id="c6144-116">\[em \] um registro de textura.</span><span class="sxs-lookup"><span data-stu-id="c6144-116">\[in\] A texture register.</span></span> <span data-ttu-id="c6144-117">Para obter mais informações, consulte a instrução de **exemplo** .</span><span class="sxs-lookup"><span data-stu-id="c6144-117">For more information see the **sample** instruction.</span></span><br/>                                 |
| <span data-ttu-id="c6144-118"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span><span class="sxs-lookup"><span data-stu-id="c6144-118"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>                             | <span data-ttu-id="c6144-119">\[em \] um registro de amostra.</span><span class="sxs-lookup"><span data-stu-id="c6144-119">\[in\] A sampler register.</span></span> <span data-ttu-id="c6144-120">Para obter mais informações, consulte a instrução de **exemplo** .</span><span class="sxs-lookup"><span data-stu-id="c6144-120">For more information see the **sample** instruction.</span></span><br/>                                 |
| <span data-ttu-id="c6144-121"><span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srcReferenceValue*</span><span class="sxs-lookup"><span data-stu-id="c6144-121"><span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srcReferenceValue*</span></span><br/> | <span data-ttu-id="c6144-122">\[em \] um registro com um único componente selecionado, que é usado na comparação.</span><span class="sxs-lookup"><span data-stu-id="c6144-122">\[in\] A register with a single component selected, which is used in the comparison.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="c6144-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="c6144-123">Remarks</span></span>

<span data-ttu-id="c6144-124">O "LZ" significa nível zero.</span><span class="sxs-lookup"><span data-stu-id="c6144-124">The "lz" stands for level-zero.</span></span> <span data-ttu-id="c6144-125">Como derivações são ignoradas, essa instrução está disponível em sombreadores além do sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="c6144-125">Because derivatives are ignored, this instruction is available in shaders other than the Pixel Shader.</span></span>

<span data-ttu-id="c6144-126">Se essa instrução for usada com uma textura mipmapped, LOD 0 será amostrado, a menos que a amostra tenha um LOD fixe que coloca o LOD em outro lugar ou se houver uma tendência de LOD, o que simplesmente se referiria a partir de 0.</span><span class="sxs-lookup"><span data-stu-id="c6144-126">If this instruction is used with a mipmapped texture, LOD 0 gets sampled, unless the sampler has an LOD clamp which places the LOD somewhere else, or if there is an LOD Bias, which would simply bias starting from 0.</span></span> <span data-ttu-id="c6144-127">Como derivações são ignoradas, a filtragem de anisotropic se comporta como filtragem de isotropic.</span><span class="sxs-lookup"><span data-stu-id="c6144-127">Because derivatives are ignored, anisotropic filtering behaves as isotropic filtering.</span></span>

<span data-ttu-id="c6144-128">Em sombreadores de pixel, essa instrução pode ser usada dentro do controle de fluxo variável quando as coordenadas de textura são derivadas no sombreador, ao contrário da **amostra \_ c**.</span><span class="sxs-lookup"><span data-stu-id="c6144-128">In Pixel Shaders, this instruction can be used inside varying flow control when the texture coordinates are derived in the shader, unlike **sample\_c**.</span></span>

<span data-ttu-id="c6144-129">A busca de um slot de entrada que não tem nada associado a ele retorna 0 para todos os componentes.</span><span class="sxs-lookup"><span data-stu-id="c6144-129">Fetching from an input slot that has nothing bound to it returns 0 for all components.</span></span>

<span data-ttu-id="c6144-130">Essa instrução está disponível em todos os sombreadores, não apenas no sombreador de pixel, para fins de consistência.</span><span class="sxs-lookup"><span data-stu-id="c6144-130">This instruction is available in all shaders, not just the Pixel Shader, for consistency.</span></span>



| <span data-ttu-id="c6144-131">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="c6144-131">Vertex Shader</span></span> | <span data-ttu-id="c6144-132">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="c6144-132">Geometry Shader</span></span> | <span data-ttu-id="c6144-133">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="c6144-133">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="c6144-134">X</span><span class="sxs-lookup"><span data-stu-id="c6144-134">X</span></span>             | <span data-ttu-id="c6144-135">X</span><span class="sxs-lookup"><span data-stu-id="c6144-135">X</span></span>               | <span data-ttu-id="c6144-136">x</span><span class="sxs-lookup"><span data-stu-id="c6144-136">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="c6144-137">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="c6144-137">Minimum Shader Model</span></span>

<span data-ttu-id="c6144-138">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="c6144-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="c6144-139">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="c6144-139">Shader Model</span></span>                                              | <span data-ttu-id="c6144-140">Com suporte</span><span class="sxs-lookup"><span data-stu-id="c6144-140">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="c6144-141">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="c6144-141">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="c6144-142">sim</span><span class="sxs-lookup"><span data-stu-id="c6144-142">yes</span></span>       |
| [<span data-ttu-id="c6144-143">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="c6144-143">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="c6144-144">sim</span><span class="sxs-lookup"><span data-stu-id="c6144-144">yes</span></span>       |
| [<span data-ttu-id="c6144-145">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="c6144-145">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="c6144-146">sim</span><span class="sxs-lookup"><span data-stu-id="c6144-146">yes</span></span>       |
| [<span data-ttu-id="c6144-147">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c6144-147">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="c6144-148">não</span><span class="sxs-lookup"><span data-stu-id="c6144-148">no</span></span>        |
| [<span data-ttu-id="c6144-149">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c6144-149">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="c6144-150">não</span><span class="sxs-lookup"><span data-stu-id="c6144-150">no</span></span>        |
| [<span data-ttu-id="c6144-151">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c6144-151">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="c6144-152">não</span><span class="sxs-lookup"><span data-stu-id="c6144-152">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="c6144-153">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c6144-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c6144-154">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c6144-154">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





