---
title: LOD (SM 4.1-ASM)
description: Retorna o nível de detalhe (LOD) que seria usado para filtragem de textura.
ms.assetid: A5931203-8CD7-4FC9-A4A4-CA981F38C7A3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a1c1ca5a22a735945b76a60c175c665c5cf58fb
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103638872"
---
# <a name="lod-sm41---asm"></a><span data-ttu-id="ff1fb-103">LOD (SM 4.1-ASM)</span><span class="sxs-lookup"><span data-stu-id="ff1fb-103">lod (sm4.1 - asm)</span></span>

<span data-ttu-id="ff1fb-104">Retorna o nível de detalhe (LOD) que seria usado para filtragem de textura.</span><span class="sxs-lookup"><span data-stu-id="ff1fb-104">Returns the level of detail (LOD) that would be used for texture filtering.</span></span>



| <span data-ttu-id="ff1fb-105">LOD dest \[ . Mask \] , srcAddress \[ . swizzle \] , srcResource \[ . swizzle \] , srcSampler</span><span class="sxs-lookup"><span data-stu-id="ff1fb-105">lod dest\[.mask\], srcAddress\[.swizzle\], srcResource\[.swizzle\], srcSampler</span></span> |
|--------------------------------------------------------------------------------|



 



| <span data-ttu-id="ff1fb-106">Item</span><span class="sxs-lookup"><span data-stu-id="ff1fb-106">Item</span></span>                                                                                                               | <span data-ttu-id="ff1fb-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="ff1fb-107">Description</span></span>                                     |
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="ff1fb-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="ff1fb-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="ff1fb-109">\[no \] endereço dos resultados.</span><span class="sxs-lookup"><span data-stu-id="ff1fb-109">\[in\] The address of the results.</span></span><br/>   |
| <span data-ttu-id="ff1fb-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span><span class="sxs-lookup"><span data-stu-id="ff1fb-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>     | <span data-ttu-id="ff1fb-111">\[em \] um conjunto de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="ff1fb-111">\[in\] A set of texture coordinates.</span></span><br/> |
| <span data-ttu-id="ff1fb-112"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="ff1fb-112"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="ff1fb-113">\[em \] um registro de textura.</span><span class="sxs-lookup"><span data-stu-id="ff1fb-113">\[in\] A texture register.</span></span><br/>           |
| <span data-ttu-id="ff1fb-114"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span><span class="sxs-lookup"><span data-stu-id="ff1fb-114"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>     | <span data-ttu-id="ff1fb-115">\[em \] um registro de amostra.</span><span class="sxs-lookup"><span data-stu-id="ff1fb-115">\[in\] A sampler register.</span></span><br/>           |



 

## <a name="remarks"></a><span data-ttu-id="ff1fb-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="ff1fb-116">Remarks</span></span>

<span data-ttu-id="ff1fb-117">Isso se comporta como a instrução de [exemplo](sample--sm4---asm-.md) , mas um exemplo filtrado não é gerado.</span><span class="sxs-lookup"><span data-stu-id="ff1fb-117">This behaves like the [sample](sample--sm4---asm-.md) instruction, but a filtered sample is not generated.</span></span> <span data-ttu-id="ff1fb-118">A instrução computa o seguinte vetor (ClampedLOD, NonClampedLOD, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="ff1fb-118">The instruction computes the following vector (ClampedLOD, NonClampedLOD, 0, 0).</span></span> <span data-ttu-id="ff1fb-119">NonClampedLOD é um valor LOD computado que ignora qualquer fixação MSS da amostra ou da textura (ou seja, pode retornar valores negativos). ClampedLOD é um valor LOD computado que seria usado pela instrução de **exemplo** real.</span><span class="sxs-lookup"><span data-stu-id="ff1fb-119">NonClampedLOD is a computed LOD value that ignores any clamping from either the sampler or the texture (ie: it can return negative values.) ClampedLOD is a computed LOD value that would be used by the actual **sample** instruction.</span></span> <span data-ttu-id="ff1fb-120">O swizzle no *srcResource* permite que os valores retornados sejam swizzled arbitrariamente antes de serem gravados no destino.</span><span class="sxs-lookup"><span data-stu-id="ff1fb-120">The swizzle on *srcResource* allows the returned values to be swizzled arbitrarily before they are written to the destination.</span></span>

<span data-ttu-id="ff1fb-121">Se não houver nenhum recurso associado ao slot especificado, 0 será retornado.</span><span class="sxs-lookup"><span data-stu-id="ff1fb-121">If there is no resource bound to the specified slot, 0 is returned.</span></span>

<span data-ttu-id="ff1fb-122">Se a amostra estiver usando a filtragem de anisotropic, o LOD deverá corresponder ao nível de MIP fracionário com base no eixo menor do espaço elíptico.</span><span class="sxs-lookup"><span data-stu-id="ff1fb-122">If the sampler is using anisotropic filtering the LOD should correspond to the fractional mip level based on the smaller axis of the elliptical footprint.</span></span>

<span data-ttu-id="ff1fb-123">Isso é válido para os seguintes tipos de textura: Texture1D, Texture2D, Texture3D e TextureCube.</span><span class="sxs-lookup"><span data-stu-id="ff1fb-123">This is valid for the following texture types: Texture1D, Texture2D, Texture3D and TextureCube.</span></span>

<span data-ttu-id="ff1fb-124">A instrução **LOD** não é definida quando usada com uma amostra que especifica a filtragem de MIP de ponto, especificamente, qualquer \_ enumeração de filtro d3d10 que termina no ponto de MIP \_ .</span><span class="sxs-lookup"><span data-stu-id="ff1fb-124">The **lod** instruction is not defined when used with a sampler that specifies point mip filtering, specifically, any D3D10\_FILTER enum that ends in MIP\_POINT.</span></span> <span data-ttu-id="ff1fb-125">(Um exemplo disso seria D3D10 \_ FILTRAR \_ o \_ ponto de MIP Mag mín \_ \_ .)</span><span class="sxs-lookup"><span data-stu-id="ff1fb-125">(An example of this would be D3D10\_FILTER\_MIN\_MAG\_MIP\_POINT.)</span></span>

<span data-ttu-id="ff1fb-126">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="ff1fb-126">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="ff1fb-127">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="ff1fb-127">Vertex Shader</span></span> | <span data-ttu-id="ff1fb-128">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="ff1fb-128">Geometry Shader</span></span> | <span data-ttu-id="ff1fb-129">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="ff1fb-129">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               |                 | <span data-ttu-id="ff1fb-130">x</span><span class="sxs-lookup"><span data-stu-id="ff1fb-130">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="ff1fb-131">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="ff1fb-131">Minimum Shader Model</span></span>

<span data-ttu-id="ff1fb-132">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="ff1fb-132">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="ff1fb-133">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="ff1fb-133">Shader Model</span></span>                                              | <span data-ttu-id="ff1fb-134">Com suporte</span><span class="sxs-lookup"><span data-stu-id="ff1fb-134">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="ff1fb-135">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="ff1fb-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="ff1fb-136">sim</span><span class="sxs-lookup"><span data-stu-id="ff1fb-136">yes</span></span>       |
| [<span data-ttu-id="ff1fb-137">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="ff1fb-137">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="ff1fb-138">sim</span><span class="sxs-lookup"><span data-stu-id="ff1fb-138">yes</span></span>       |
| [<span data-ttu-id="ff1fb-139">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="ff1fb-139">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="ff1fb-140">não</span><span class="sxs-lookup"><span data-stu-id="ff1fb-140">no</span></span>        |
| [<span data-ttu-id="ff1fb-141">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ff1fb-141">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="ff1fb-142">não</span><span class="sxs-lookup"><span data-stu-id="ff1fb-142">no</span></span>        |
| [<span data-ttu-id="ff1fb-143">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ff1fb-143">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="ff1fb-144">não</span><span class="sxs-lookup"><span data-stu-id="ff1fb-144">no</span></span>        |
| [<span data-ttu-id="ff1fb-145">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ff1fb-145">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="ff1fb-146">não</span><span class="sxs-lookup"><span data-stu-id="ff1fb-146">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="ff1fb-147">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ff1fb-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff1fb-148">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ff1fb-148">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





