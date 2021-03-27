---
title: gather4_po (SM5-ASM)
description: Uma variante de gather4, mas em vez de dar suporte a um deslocamento imediato \-8.. 7 \, o deslocamento é fornecido como um parâmetro para a instrução e também tem um intervalo maior de \-32.. 31 \.
ms.assetid: A77A32B4-BD4F-46E7-9999-13EAA8A26974
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9197fee97645333d37d589db36c3774852b12229
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104967119"
---
# <a name="gather4_po-sm5---asm"></a><span data-ttu-id="0f83a-103">gather4 \_ po (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="0f83a-103">gather4\_po (sm5 - asm)</span></span>

<span data-ttu-id="0f83a-104">Uma variante de [gather4](gather4--sm5---asm-.md), mas em vez de dar suporte a um deslocamento imediato \[ -8.. 7 \] , o deslocamento é fornecido como um parâmetro para a instrução e também tem um intervalo maior de \[ -32.. 31 \] .</span><span class="sxs-lookup"><span data-stu-id="0f83a-104">A variant of [gather4](gather4--sm5---asm-.md), but instead of supporting an immediate offset \[-8..7\], the offset comes as a parameter to the instruction, and also has larger range of \[-32..31\].</span></span>



| <span data-ttu-id="0f83a-105">gather4 \_ po dest \[ . Mask \] , srcAddress \[ . swizzle \] , srcOffset \[ . swizzle \] , srcResource \[ . swizzle \] , srcSampler \[ . selecionar \_ componente\]</span><span class="sxs-lookup"><span data-stu-id="0f83a-105">gather4\_po dest\[.mask\], srcAddress\[.swizzle\], srcOffset\[.swizzle\], srcResource\[.swizzle\], srcSampler\[.select\_component\]</span></span> |
|-------------------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="0f83a-106">Item</span><span class="sxs-lookup"><span data-stu-id="0f83a-106">Item</span></span>                                                                                                               | <span data-ttu-id="0f83a-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="0f83a-107">Description</span></span>                                                   |
|--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="0f83a-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="0f83a-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="0f83a-109">\[no \] endereço do resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="0f83a-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="0f83a-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span><span class="sxs-lookup"><span data-stu-id="0f83a-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>     | <span data-ttu-id="0f83a-111">\[em \] um conjunto de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="0f83a-111">\[in\] A set of texture coordinates.</span></span><br/>               |
| <span data-ttu-id="0f83a-112"><span id="srcOffset"></span><span id="srcoffset"></span><span id="SRCOFFSET"></span>*srcOffset*</span><span class="sxs-lookup"><span data-stu-id="0f83a-112"><span id="srcOffset"></span><span id="srcoffset"></span><span id="SRCOFFSET"></span>*srcOffset*</span></span><br/>         | <span data-ttu-id="0f83a-113">\[no \] deslocamento.</span><span class="sxs-lookup"><span data-stu-id="0f83a-113">\[in\] The offset.</span></span><br/>                                 |
| <span data-ttu-id="0f83a-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="0f83a-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="0f83a-115">\[em \] um registro de textura.</span><span class="sxs-lookup"><span data-stu-id="0f83a-115">\[in\] A texture register.</span></span><br/>                         |
| <span data-ttu-id="0f83a-116"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span><span class="sxs-lookup"><span data-stu-id="0f83a-116"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>     | <span data-ttu-id="0f83a-117">\[em \] um registro de amostra.</span><span class="sxs-lookup"><span data-stu-id="0f83a-117">\[in\] A sampler register.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="0f83a-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="0f83a-118">Remarks</span></span>

<span data-ttu-id="0f83a-119">Os dois primeiros componentes do parâmetro de deslocamento de quatro vetores fornecem deslocamentos de inteiro de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="0f83a-119">The first two components of the 4-vector offset parameter supply 32-bit integer offsets.</span></span> <span data-ttu-id="0f83a-120">Os outros componentes desse parâmetro são ignorados.</span><span class="sxs-lookup"><span data-stu-id="0f83a-120">The other components of this parameter are ignored.</span></span>

<span data-ttu-id="0f83a-121">Os 6 bits menos significativos de cada valor de deslocamento são respeitados como um valor assinado, produzindo \[ -32.. 31 \] Range.</span><span class="sxs-lookup"><span data-stu-id="0f83a-121">The 6 least significant bits of each offset value is honored as a signed value, yielding \[-32..31\] range.</span></span>

<span data-ttu-id="0f83a-122">Essa instrução só funciona com texturas 2D, ao contrário de **gather4**, que também funciona com TextureCubes.</span><span class="sxs-lookup"><span data-stu-id="0f83a-122">This instruction only works with 2D textures, unlike **gather4**, which also works with TextureCubes.</span></span>

<span data-ttu-id="0f83a-123">Os únicos modos honrados na amostra são os modos de endereçamento.</span><span class="sxs-lookup"><span data-stu-id="0f83a-123">The only modes honored in the sampler are the addressing modes.</span></span> <span data-ttu-id="0f83a-124">Somente o MIP mais detalhado no modo de exibição de recursos é usado.</span><span class="sxs-lookup"><span data-stu-id="0f83a-124">Only the most detailed mip in the resource view is used.</span></span>

<span data-ttu-id="0f83a-125">Se o endereço cair em um Texel Center, isso não significa que o outro texels pode ser zerado.</span><span class="sxs-lookup"><span data-stu-id="0f83a-125">If the address falls on a texel center, this does not mean the other texels can be zeroed out.</span></span>

<span data-ttu-id="0f83a-126">O parâmetro *srcSampler* inclui o \[ componente. Select \_ \] , permitindo que qualquer componente individual de uma textura seja recuperado, incluindo o retorno de padrões para componentes ausentes.</span><span class="sxs-lookup"><span data-stu-id="0f83a-126">The *srcSampler* parameter includes \[.select\_component\], allowing any single component of a texture to be retrieved, including returning defaults for missing components.</span></span>

<span data-ttu-id="0f83a-127">Para formatos com componentes float32, se o valor que está sendo obtido for normalizado, desnormalizado, +-0 ou +-INF, ele será retornado ao sombreador inalterado.</span><span class="sxs-lookup"><span data-stu-id="0f83a-127">For formats with float32 components, if the value being fetched is normalized, denormalized, +-0 or +-INF, it is returned to the shader unaltered.</span></span> <span data-ttu-id="0f83a-128">NaN é retornado como NaN, mas a representação de bit exata do NaN pode ser alterada.</span><span class="sxs-lookup"><span data-stu-id="0f83a-128">NaN is returned as NaN, but the exact bit representation of the NaN may be changed.</span></span> <span data-ttu-id="0f83a-129">Para TextureCubes, alguma síntese do 4º Texel ausente deve ocorrer nos cantos, portanto, a noção de retornar bits inalterado para o Texel sintetizado não se aplica, e as desnormas podem ser liberadas.</span><span class="sxs-lookup"><span data-stu-id="0f83a-129">For TextureCubes, some synthesis of the missing 4th texel must occur at corners, so the notion of returning bits unchanged for the synthesized texel does not apply, and denorms could be flushed.</span></span>

<span data-ttu-id="0f83a-130">Use esta instrução para estender o intervalo de deslocamento de **gather4** para ser maior e programável.</span><span class="sxs-lookup"><span data-stu-id="0f83a-130">Use this instruction to extend offset range of **gather4** to be larger and programmable.</span></span> <span data-ttu-id="0f83a-131">O sufixo "po" no nome significa "deslocamento programável".</span><span class="sxs-lookup"><span data-stu-id="0f83a-131">The "po" suffix on the name means "programmable offset".</span></span>

<span data-ttu-id="0f83a-132">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="0f83a-132">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="0f83a-133">Vértice</span><span class="sxs-lookup"><span data-stu-id="0f83a-133">Vertex</span></span> | <span data-ttu-id="0f83a-134">Envoltória</span><span class="sxs-lookup"><span data-stu-id="0f83a-134">Hull</span></span> | <span data-ttu-id="0f83a-135">Domínio</span><span class="sxs-lookup"><span data-stu-id="0f83a-135">Domain</span></span> | <span data-ttu-id="0f83a-136">Geometria</span><span class="sxs-lookup"><span data-stu-id="0f83a-136">Geometry</span></span> | <span data-ttu-id="0f83a-137">16x16</span><span class="sxs-lookup"><span data-stu-id="0f83a-137">Pixel</span></span> | <span data-ttu-id="0f83a-138">Computação</span><span class="sxs-lookup"><span data-stu-id="0f83a-138">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="0f83a-139">X</span><span class="sxs-lookup"><span data-stu-id="0f83a-139">X</span></span>      | <span data-ttu-id="0f83a-140">X</span><span class="sxs-lookup"><span data-stu-id="0f83a-140">X</span></span>    | <span data-ttu-id="0f83a-141">X</span><span class="sxs-lookup"><span data-stu-id="0f83a-141">X</span></span>      | <span data-ttu-id="0f83a-142">X</span><span class="sxs-lookup"><span data-stu-id="0f83a-142">X</span></span>        | <span data-ttu-id="0f83a-143">X</span><span class="sxs-lookup"><span data-stu-id="0f83a-143">X</span></span>     | <span data-ttu-id="0f83a-144">X</span><span class="sxs-lookup"><span data-stu-id="0f83a-144">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="0f83a-145">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="0f83a-145">Minimum Shader Model</span></span>

<span data-ttu-id="0f83a-146">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="0f83a-146">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="0f83a-147">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="0f83a-147">Shader Model</span></span>                                              | <span data-ttu-id="0f83a-148">Com suporte</span><span class="sxs-lookup"><span data-stu-id="0f83a-148">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="0f83a-149">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="0f83a-149">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="0f83a-150">sim</span><span class="sxs-lookup"><span data-stu-id="0f83a-150">yes</span></span>       |
| [<span data-ttu-id="0f83a-151">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="0f83a-151">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="0f83a-152">não</span><span class="sxs-lookup"><span data-stu-id="0f83a-152">no</span></span>        |
| [<span data-ttu-id="0f83a-153">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="0f83a-153">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="0f83a-154">não</span><span class="sxs-lookup"><span data-stu-id="0f83a-154">no</span></span>        |
| [<span data-ttu-id="0f83a-155">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0f83a-155">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="0f83a-156">não</span><span class="sxs-lookup"><span data-stu-id="0f83a-156">no</span></span>        |
| [<span data-ttu-id="0f83a-157">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0f83a-157">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="0f83a-158">não</span><span class="sxs-lookup"><span data-stu-id="0f83a-158">no</span></span>        |
| [<span data-ttu-id="0f83a-159">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0f83a-159">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="0f83a-160">não</span><span class="sxs-lookup"><span data-stu-id="0f83a-160">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="0f83a-161">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0f83a-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f83a-162">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0f83a-162">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





