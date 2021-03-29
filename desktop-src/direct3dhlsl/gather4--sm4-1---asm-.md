---
title: gather4 (SM 4.1-ASM)
description: Coleta os quatro texels que seriam usados em uma operação de filtragem de bi-linear e os empacota em um único registro. | gather4 (SM 4.1-ASM)
ms.assetid: 219B25AE-CBF9-4B68-B2DB-6D8C3C5B4CEA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84387bfe027e30b338b4701ec941a9d4e1b5e242
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968402"
---
# <a name="gather4-sm41---asm"></a><span data-ttu-id="d20f0-104">gather4 (SM 4.1-ASM)</span><span class="sxs-lookup"><span data-stu-id="d20f0-104">gather4 (sm4.1 - asm)</span></span>

<span data-ttu-id="d20f0-105">Coleta os quatro texels que seriam usados em uma operação de filtragem de bi-linear e os empacota em um único registro.</span><span class="sxs-lookup"><span data-stu-id="d20f0-105">Gathers the four texels that would be used in a bi-linear filtering operation and packs them into a single register.</span></span>



| <span data-ttu-id="d20f0-106">gather4 \[ \_ aoffimmi (u, v) \] dest \[ . Mask \] , srcAddress \[ . swizzle \] , srcResource \[ . swizzle \] srcSampler. r</span><span class="sxs-lookup"><span data-stu-id="d20f0-106">gather4\[\_aoffimmi(u,v)\] dest\[.mask\], srcAddress\[.swizzle\], srcResource\[.swizzle\] srcSampler.r</span></span> |
|--------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="d20f0-107">Item</span><span class="sxs-lookup"><span data-stu-id="d20f0-107">Item</span></span>                                                                                                               | <span data-ttu-id="d20f0-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="d20f0-108">Description</span></span>                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d20f0-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="d20f0-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="d20f0-110">\[no \] endereço do resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="d20f0-110">\[in\] The address of the result of the operation.</span></span><br/>                                                                                                       |
| <span data-ttu-id="d20f0-111"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span><span class="sxs-lookup"><span data-stu-id="d20f0-111"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>     | <span data-ttu-id="d20f0-112">\[in \] contém as coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="d20f0-112">\[in\] Contains the texture coordinates.</span></span> <br/>                                                                                                                |
| <span data-ttu-id="d20f0-113"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="d20f0-113"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="d20f0-114">\[em \] um registro de recurso.</span><span class="sxs-lookup"><span data-stu-id="d20f0-114">\[in\] A resource register.</span></span> <br/> <span data-ttu-id="d20f0-115">O swizzle permite que os valores retornados sejam swizzled arbitrariamente antes de serem gravados no *dest*.</span><span class="sxs-lookup"><span data-stu-id="d20f0-115">The swizzle allows the returned values to be swizzled arbitrarily before they are written to *dest*.</span></span> <br/>            |
| <span data-ttu-id="d20f0-116"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span><span class="sxs-lookup"><span data-stu-id="d20f0-116"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>     | <span data-ttu-id="d20f0-117">\[em \] um registro de amostra.</span><span class="sxs-lookup"><span data-stu-id="d20f0-117">\[in\] A sampler register.</span></span><br/> <span data-ttu-id="d20f0-118">Esse parâmetro deve ter um swizzle. r (vermelho), que indica que o valor do canal R é copiado para *dest*.</span><span class="sxs-lookup"><span data-stu-id="d20f0-118">This parameter must have a .r (red) swizzle, which indicates that the value of the R channel is copied to *dest*.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="d20f0-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="d20f0-119">Remarks</span></span>

<span data-ttu-id="d20f0-120">Esta operação só funciona com texturas 2D ou CubeMap de canal único.</span><span class="sxs-lookup"><span data-stu-id="d20f0-120">This operation only works with single channel 2D or CubeMap textures.</span></span> <span data-ttu-id="d20f0-121">Para texturas 2D, somente os modos de endereçamento da amostra são usados e o nível superior de qualquer pirâmide MIP é usado.</span><span class="sxs-lookup"><span data-stu-id="d20f0-121">For 2D textures only the addressing modes of the sampler are used and the top level of any mip pyramid is used.</span></span>

<span data-ttu-id="d20f0-122">Essa instrução se comporta como a instrução de [exemplo](sample--sm4---asm-.md) , mas uma amostra filtrada não é gerada.</span><span class="sxs-lookup"><span data-stu-id="d20f0-122">This instruction behaves like the [sample](sample--sm4---asm-.md) instruction, but a filtered sample is not generated.</span></span> <span data-ttu-id="d20f0-123">Os quatro exemplos que contribuiria para a filtragem são colocados em xyzw no sentido anti-horário do contador, começando com a amostra para a parte inferior esquerda do local consultado.</span><span class="sxs-lookup"><span data-stu-id="d20f0-123">The four samples that would contribute to filtering are placed into xyzw in counter clockwise order starting with the sample to the lower left of the queried location.</span></span> <span data-ttu-id="d20f0-124">Isso é o mesmo que a amostragem de ponto com deltas de coordenadas de textura (u, v) nos seguintes locais: (-, +), (+, +), (+,-), (-,-), em que a magnitude dos deltas sempre é meio Texel.</span><span class="sxs-lookup"><span data-stu-id="d20f0-124">This is the same as point sampling with (u,v) texture coordinate deltas at the following locations: (-,+),(+,+),(+,-),(-,-), where the magnitude of the deltas are always half a texel.</span></span>

<span data-ttu-id="d20f0-125">Para texturas CubeMap quando um espaço de bi linear abrange um texels de borda da face vizinha, é usado.</span><span class="sxs-lookup"><span data-stu-id="d20f0-125">For CubeMap textures when a bi-linear footprint spans an edge texels from the neighboring face are used.</span></span> <span data-ttu-id="d20f0-126">Os cantos usam as mesmas regras que a instrução de **exemplo** ; Esse é o canto desconhecido, que é considerado a média dos três cantos da face de ping.</span><span class="sxs-lookup"><span data-stu-id="d20f0-126">Corners use the same rules as the **sample** instruction; that is the unkown corner is considered the average of the three impinging face corners.</span></span>

<span data-ttu-id="d20f0-127">As restrições de formato de textura que se aplicam às instruções de **exemplo** também se aplicam à instrução **gather4** .</span><span class="sxs-lookup"><span data-stu-id="d20f0-127">The texture format restrictions that apply to the **sample** instructions also apply to the **gather4** instruction.</span></span>

<span data-ttu-id="d20f0-128">Para implementações de hardware, otimizações na filtragem biline tradicional que detectam exemplos diretamente em texels e ignoram a leitura de texels que teriam peso 0 não podem ser aproveitadas com **gather4**.</span><span class="sxs-lookup"><span data-stu-id="d20f0-128">For hardware implementations, optimizations in traditional bilinear filtering that detect samples directly on texels and skip reading of texels that would have weight 0 cannot be leveraged with **gather4**.</span></span> <span data-ttu-id="d20f0-129">**gather4** sempre retorna todos os texels solicitados.</span><span class="sxs-lookup"><span data-stu-id="d20f0-129">**gather4** always returns all requested texels.</span></span>

<span data-ttu-id="d20f0-130">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="d20f0-130">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="d20f0-131">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="d20f0-131">Vertex Shader</span></span> | <span data-ttu-id="d20f0-132">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="d20f0-132">Geometry Shader</span></span> | <span data-ttu-id="d20f0-133">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="d20f0-133">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="d20f0-134">x</span><span class="sxs-lookup"><span data-stu-id="d20f0-134">x</span></span>             | <span data-ttu-id="d20f0-135">x</span><span class="sxs-lookup"><span data-stu-id="d20f0-135">x</span></span>               | <span data-ttu-id="d20f0-136">x</span><span class="sxs-lookup"><span data-stu-id="d20f0-136">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d20f0-137">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="d20f0-137">Minimum Shader Model</span></span>

<span data-ttu-id="d20f0-138">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="d20f0-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="d20f0-139">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="d20f0-139">Shader Model</span></span>                                              | <span data-ttu-id="d20f0-140">Com suporte</span><span class="sxs-lookup"><span data-stu-id="d20f0-140">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="d20f0-141">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="d20f0-141">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="d20f0-142">sim</span><span class="sxs-lookup"><span data-stu-id="d20f0-142">yes</span></span>       |
| [<span data-ttu-id="d20f0-143">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="d20f0-143">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="d20f0-144">sim</span><span class="sxs-lookup"><span data-stu-id="d20f0-144">yes</span></span>       |
| [<span data-ttu-id="d20f0-145">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="d20f0-145">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="d20f0-146">não</span><span class="sxs-lookup"><span data-stu-id="d20f0-146">no</span></span>        |
| [<span data-ttu-id="d20f0-147">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d20f0-147">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="d20f0-148">não</span><span class="sxs-lookup"><span data-stu-id="d20f0-148">no</span></span>        |
| [<span data-ttu-id="d20f0-149">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d20f0-149">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="d20f0-150">não</span><span class="sxs-lookup"><span data-stu-id="d20f0-150">no</span></span>        |
| [<span data-ttu-id="d20f0-151">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d20f0-151">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="d20f0-152">não</span><span class="sxs-lookup"><span data-stu-id="d20f0-152">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="d20f0-153">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d20f0-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d20f0-154">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d20f0-154">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





