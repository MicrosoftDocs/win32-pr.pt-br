---
title: sample_l (sm4-ASM)
description: Amostras de dados do elemento/textura especificado usando o endereço especificado e o modo de filtragem identificados pelo determinado exemplo. | sample_l (sm4-ASM)
ms.assetid: D285F63E-1026-45F1-9959-6F5AB2A27C95
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5acd83d81e4648cc9eae5f8e0166013dcca512a8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104298321"
---
# <a name="sample_l-sm4---asm"></a><span data-ttu-id="41763-104">exemplo \_ l (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="41763-104">sample\_l (sm4 - asm)</span></span>

<span data-ttu-id="41763-105">Amostras de dados do elemento/textura especificado usando o endereço especificado e o modo de filtragem identificados pelo determinado exemplo.</span><span class="sxs-lookup"><span data-stu-id="41763-105">Samples data from the specified Element/texture using the specified address and the filtering mode identified by the given sampler.</span></span>



| <span data-ttu-id="41763-106">exemplo \_ l \[ \_ aoffimmi (u, v, w) \] dest \[ . Mask \] , srcAddress \[ . swizzle \] , srcResource \[ . swizzle \] , srcSampler, srcLOD. selecionar \_ componente</span><span class="sxs-lookup"><span data-stu-id="41763-106">sample\_l\[\_aoffimmi(u,v,w)\] dest\[.mask\], srcAddress\[.swizzle\], srcResource\[.swizzle\], srcSampler, srcLOD.select\_component</span></span> |
|-------------------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="41763-107">Item</span><span class="sxs-lookup"><span data-stu-id="41763-107">Item</span></span>                                                                                                               | <span data-ttu-id="41763-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="41763-108">Description</span></span>                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41763-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="41763-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="41763-110">\[no \] endereço dos resultados da operação.</span><span class="sxs-lookup"><span data-stu-id="41763-110">\[in\] The address of the results of the operation.</span></span><br/>                                                             |
| <span data-ttu-id="41763-111"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span><span class="sxs-lookup"><span data-stu-id="41763-111"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>     | <span data-ttu-id="41763-112">\[em \] um conjunto de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="41763-112">\[in\] A set of texture coordinates.</span></span> <span data-ttu-id="41763-113">Para obter mais informações, consulte a instrução de [exemplo](sample--sm4---asm-.md) .</span><span class="sxs-lookup"><span data-stu-id="41763-113">For more information see the [sample](sample--sm4---asm-.md) instruction.</span></span><br/> |
| <span data-ttu-id="41763-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="41763-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="41763-115">\[em \] um registro de textura.</span><span class="sxs-lookup"><span data-stu-id="41763-115">\[in\] A texture register.</span></span> <span data-ttu-id="41763-116">Para obter mais informações, consulte a instrução de **exemplo** .</span><span class="sxs-lookup"><span data-stu-id="41763-116">For more information see the **sample** instruction.</span></span><br/>                                 |
| <span data-ttu-id="41763-117"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span><span class="sxs-lookup"><span data-stu-id="41763-117"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>     | <span data-ttu-id="41763-118">\[em \] um registro de amostra.</span><span class="sxs-lookup"><span data-stu-id="41763-118">\[in\] A sampler register.</span></span> <span data-ttu-id="41763-119">Para obter mais informações, consulte a instrução de **exemplo** .</span><span class="sxs-lookup"><span data-stu-id="41763-119">For more information see the **sample** instruction.</span></span><br/>                                 |
| <span data-ttu-id="41763-120"><span id="srcLOD"></span><span id="srclod"></span><span id="SRCLOD"></span>*srcLOD*</span><span class="sxs-lookup"><span data-stu-id="41763-120"><span id="srcLOD"></span><span id="srclod"></span><span id="SRCLOD"></span>*srcLOD*</span></span><br/>                     | <span data-ttu-id="41763-121">\[no \] LOD.</span><span class="sxs-lookup"><span data-stu-id="41763-121">\[in\] The LOD.</span></span><br/>                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="41763-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="41763-122">Remarks</span></span>

<span data-ttu-id="41763-123">Essa instrução é idêntica à [amostra](sample--sm4---asm-.md), exceto que LOD é fornecido diretamente pelo aplicativo como um valor escalar, que não representa anisotropy.</span><span class="sxs-lookup"><span data-stu-id="41763-123">This instruction is identical to [sample](sample--sm4---asm-.md), except that LOD is provided directly by the application as a scalar value, representing no anisotropy.</span></span> <span data-ttu-id="41763-124">Essa instrução está disponível em todos os estágios do sombreador progammable.</span><span class="sxs-lookup"><span data-stu-id="41763-124">This instruction is available in all progammable Shader stages.</span></span>

<span data-ttu-id="41763-125">o **exemplo \_ l amostra** a textura usando *SRCLOD* para ser a LOD.</span><span class="sxs-lookup"><span data-stu-id="41763-125">**sample\_l** samples the texture using *srcLOD* to be the LOD.</span></span> <span data-ttu-id="41763-126">Se o valor de LOD for <= 0, o zero'th (maior mapa) será escolhido, com o filtro de ampliação aplicado (se for aplicável com base no modo de filtro).</span><span class="sxs-lookup"><span data-stu-id="41763-126">If the LOD value is <= 0, the zero'th (biggest map) is chosen, with the magnify filter applied (if applicable based on the filter mode).</span></span> <span data-ttu-id="41763-127">Como *srcLOD* é um valor de ponto flutuante, o valor fracionário é usado para interpolar entre dois níveis MIP, se o filtro reduzir for linear ou com filtragem anisotropic.</span><span class="sxs-lookup"><span data-stu-id="41763-127">Because *srcLOD* is a floating point value, the fractional value is used to interpolate between two mip levels, if the minify filter is LINEAR or with anisotropic filtering.</span></span>

<span data-ttu-id="41763-128">o **exemplo \_ l** ignora as derivações de endereço, portanto, o comportamento de filtragem é puramente isotropic.</span><span class="sxs-lookup"><span data-stu-id="41763-128">**sample\_l** ignores address derivatives, so filtering behavior is purely isotropic.</span></span> <span data-ttu-id="41763-129">Como derivações são ignoradas, a filtragem de anisotropic se comporta como filtragem de isotropic.</span><span class="sxs-lookup"><span data-stu-id="41763-129">Because derivatives are ignored, anisotropic filtering behaves as isotropic filtering.</span></span>

<span data-ttu-id="41763-130">Os Estados de amostra MIPLODBIAS e MAX/MINMIPLEVEL são respeitados.</span><span class="sxs-lookup"><span data-stu-id="41763-130">Sampler states MIPLODBIAS and MAX/MINMIPLEVEL are honored.</span></span>

<span data-ttu-id="41763-131">Quando usado no sombreador de pixel, o **exemplo \_ l** indica que a escolha de LOD é por pixel, sem efeito de pixels vizinhos, por exemplo, no mesmo carimbo 2x2.</span><span class="sxs-lookup"><span data-stu-id="41763-131">When used in the Pixel Shader, **sample\_l** implies that the choice of LOD is per-pixel, with no effect from neighboring pixels, for example in the same 2x2 stamp.</span></span>

<span data-ttu-id="41763-132">A busca de um slot de entrada que não tem nada associado a ele retorna 0 para todos os componentes.</span><span class="sxs-lookup"><span data-stu-id="41763-132">Fetching from an input slot that has nothing bound to it returns 0 for all components.</span></span>

<span data-ttu-id="41763-133">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="41763-133">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="41763-134">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="41763-134">Vertex Shader</span></span> | <span data-ttu-id="41763-135">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="41763-135">Geometry Shader</span></span> | <span data-ttu-id="41763-136">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="41763-136">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="41763-137">X</span><span class="sxs-lookup"><span data-stu-id="41763-137">X</span></span>             | <span data-ttu-id="41763-138">X</span><span class="sxs-lookup"><span data-stu-id="41763-138">X</span></span>               | <span data-ttu-id="41763-139">x</span><span class="sxs-lookup"><span data-stu-id="41763-139">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="41763-140">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="41763-140">Minimum Shader Model</span></span>

<span data-ttu-id="41763-141">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="41763-141">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="41763-142">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="41763-142">Shader Model</span></span>                                              | <span data-ttu-id="41763-143">Com suporte</span><span class="sxs-lookup"><span data-stu-id="41763-143">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="41763-144">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="41763-144">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="41763-145">sim</span><span class="sxs-lookup"><span data-stu-id="41763-145">yes</span></span>       |
| [<span data-ttu-id="41763-146">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="41763-146">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="41763-147">sim</span><span class="sxs-lookup"><span data-stu-id="41763-147">yes</span></span>       |
| [<span data-ttu-id="41763-148">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="41763-148">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="41763-149">sim</span><span class="sxs-lookup"><span data-stu-id="41763-149">yes</span></span>       |
| [<span data-ttu-id="41763-150">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="41763-150">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="41763-151">não</span><span class="sxs-lookup"><span data-stu-id="41763-151">no</span></span>        |
| [<span data-ttu-id="41763-152">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="41763-152">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="41763-153">não</span><span class="sxs-lookup"><span data-stu-id="41763-153">no</span></span>        |
| [<span data-ttu-id="41763-154">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="41763-154">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="41763-155">não</span><span class="sxs-lookup"><span data-stu-id="41763-155">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="41763-156">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="41763-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41763-157">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="41763-157">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





