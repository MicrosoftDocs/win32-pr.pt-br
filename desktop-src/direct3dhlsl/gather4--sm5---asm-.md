---
title: gather4 (SM5-ASM)
description: Coleta os quatro texels que seriam usados em uma operação de filtragem de bi-linear e os empacota em um único registro. | gather4 (SM5-ASM)
ms.assetid: 5F93BB70-7696-48E4-BCD3-91D5D42FF63E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5657265738f12331afc7596286f02170de2a635
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104172694"
---
# <a name="gather4-sm5---asm"></a><span data-ttu-id="5fe71-104">gather4 (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="5fe71-104">gather4 (sm5 - asm)</span></span>

<span data-ttu-id="5fe71-105">Coleta os quatro texels que seriam usados em uma operação de filtragem de bi-linear e os empacota em um único registro.</span><span class="sxs-lookup"><span data-stu-id="5fe71-105">Gathers the four texels that would be used in a bi-linear filtering operation and packs them into a single register.</span></span> <span data-ttu-id="5fe71-106">Essa instrução só funciona com texturas 2D ou CubeMap, incluindo matrizes.</span><span class="sxs-lookup"><span data-stu-id="5fe71-106">This instruction only works with 2D or CubeMap textures, including arrays.</span></span> <span data-ttu-id="5fe71-107">Somente os modos de endereçamento da amostra são usados e o nível superior de qualquer pirâmide MIP é usado.</span><span class="sxs-lookup"><span data-stu-id="5fe71-107">Only the addressing modes of the sampler are used and the top level of any mip pyramid is used.</span></span>



| <span data-ttu-id="5fe71-108">gather4 \[ \_ aoffimmi (u, v) \] dest \[ . Mask \] , srcAddress \[ . swizzle \] , srcResource \[ . swizzle \] , srcSampler \[ . selecionar \_ componente\]</span><span class="sxs-lookup"><span data-stu-id="5fe71-108">gather4\[\_aoffimmi(u,v)\] dest\[.mask\], srcAddress\[.swizzle\], srcResource\[.swizzle\], srcSampler\[.select\_component\]</span></span> |
|-----------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="5fe71-109">Item</span><span class="sxs-lookup"><span data-stu-id="5fe71-109">Item</span></span>                                                                                                               | <span data-ttu-id="5fe71-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="5fe71-110">Description</span></span>                                                    |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="5fe71-111"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="5fe71-111"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="5fe71-112">\[no \] endereço dos resultados da operação.</span><span class="sxs-lookup"><span data-stu-id="5fe71-112">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="5fe71-113"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span><span class="sxs-lookup"><span data-stu-id="5fe71-113"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>     | <span data-ttu-id="5fe71-114">\[em \] um conjunto de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="5fe71-114">\[in\] A set of texture coordinates.</span></span><br/>                |
| <span data-ttu-id="5fe71-115"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="5fe71-115"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="5fe71-116">\[em \] um registro de textura.</span><span class="sxs-lookup"><span data-stu-id="5fe71-116">\[in\] A texture register.</span></span><br/>                          |
| <span data-ttu-id="5fe71-117"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span><span class="sxs-lookup"><span data-stu-id="5fe71-117"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>     | <span data-ttu-id="5fe71-118">\[em \] um registro de amostra.</span><span class="sxs-lookup"><span data-stu-id="5fe71-118">\[in\] A sampler register.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="5fe71-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="5fe71-119">Remarks</span></span>

<span data-ttu-id="5fe71-120">Essa instrução se comporta como a instrução de [**exemplo**](sample--sm4---asm-.md) , mas uma amostra filtrada não é gerada.</span><span class="sxs-lookup"><span data-stu-id="5fe71-120">This instruction behaves like the [**sample**](sample--sm4---asm-.md) instruction, but a filtered sample is not generated.</span></span> <span data-ttu-id="5fe71-121">Os quatro exemplos que contribuiria para a filtragem são colocados em xyzw no sentido anti-horário do contador, começando com a amostra para a parte inferior esquerda do local consultado.</span><span class="sxs-lookup"><span data-stu-id="5fe71-121">The four samples that would contribute to filtering are placed into xyzw in counter clockwise order starting with the sample to the lower left of the queried location.</span></span> <span data-ttu-id="5fe71-122">Isso é o mesmo que a amostragem de ponto com deltas de coordenadas de textura (u, v) nos seguintes locais: (-, +), (+, +), (+,-), (-,-), em que a magnitude dos deltas sempre é meio Texel.</span><span class="sxs-lookup"><span data-stu-id="5fe71-122">This is the same as point sampling with (u,v) texture coordinate deltas at the following locations: (-,+),(+,+),(+,-),(-,-), where the magnitude of the deltas are always half a texel.</span></span>

<span data-ttu-id="5fe71-123">Para texturas CubeMap, quando uma superfície de bi linear abrange uma borda, texels da face vizinha é usado.</span><span class="sxs-lookup"><span data-stu-id="5fe71-123">For CubeMap textures, when a bi-linear footprint spans an edge, texels from the neighboring face are used.</span></span> <span data-ttu-id="5fe71-124">Os cantos usam as mesmas regras que a instrução de [**exemplo**](sample--sm4---asm-.md) ; ou seja, o canto desconhecido é considerado a média dos três cantos da face do ping.</span><span class="sxs-lookup"><span data-stu-id="5fe71-124">Corners use the same rules as the [**sample**](sample--sm4---asm-.md) instruction; that is, the unknown corner is considered the average of the three impinging face corners.</span></span>

<span data-ttu-id="5fe71-125">Há restrições de formato de textura que se aplicam a **gather4** que são expressas na lista de formatos.</span><span class="sxs-lookup"><span data-stu-id="5fe71-125">There are texture format restrictions that apply to **gather4** which are expressed in the format list.</span></span>

<span data-ttu-id="5fe71-126">O swizzle no *srcResource* permite que os valores retornados sejam swizzled arbitrariamente antes de serem gravados no destino.</span><span class="sxs-lookup"><span data-stu-id="5fe71-126">The swizzle on *srcResource* allows the returned values to be swizzled arbitrarily before they are written to the destination.</span></span>

<span data-ttu-id="5fe71-127">O componente. Select \_ em *srcSampler* escolhe qual componente da textura de origem (r/g/b/a) para ler 4 texels.</span><span class="sxs-lookup"><span data-stu-id="5fe71-127">The .select\_component on *srcSampler* chooses which component of the source texture (r/g/b/a) to read 4 texels from.</span></span>

<span data-ttu-id="5fe71-128">Para formatos com componentes float32, se o valor que está sendo obtido for normalizado, desnormalizado, +-0 ou +-INF, ele será retornado ao sombreador inalterado.</span><span class="sxs-lookup"><span data-stu-id="5fe71-128">For formats with float32 components, if the value being fetched is normalized, denormalized, +-0 or +-INF, it is returned to the shader unaltered.</span></span> <span data-ttu-id="5fe71-129">NaN é retornado como NaN, mas a representação de bit exata do NaN pode ser alterada.</span><span class="sxs-lookup"><span data-stu-id="5fe71-129">NaN is returned as NaN, but the exact bit representation of the NaN may be changed.</span></span> <span data-ttu-id="5fe71-130">Para TextureCubes, alguma síntese do 4º Texel ausente deve ocorrer nos cantos, portanto, retornar bits inalterados para o Texel sintetizado não se aplica, e as alterações podem ser liberadas.</span><span class="sxs-lookup"><span data-stu-id="5fe71-130">For TextureCubes, some synthesis of the missing 4th texel must occur at corners, so returning bits unchanged for the synthesized texel does not apply, and denorms could be flushed.</span></span>

<span data-ttu-id="5fe71-131">Para implementações de hardware, otimizações na filtragem biline tradicional que detectam exemplos diretamente em texels e ignoram a leitura de texels que teriam peso 0 não podem ser aproveitadas com essa instrução.</span><span class="sxs-lookup"><span data-stu-id="5fe71-131">For hardware implementations, optimizations in traditional bilinear filtering that detect samples directly on texels and skip reading of texels that would have weight 0 cannot be leveraged with this instruction.</span></span> <span data-ttu-id="5fe71-132">*gather4* sempre retorna todos os texels solicitados.</span><span class="sxs-lookup"><span data-stu-id="5fe71-132">*gather4* always returns all requested texels.</span></span>

<span data-ttu-id="5fe71-133">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="5fe71-133">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="5fe71-134">Vértice</span><span class="sxs-lookup"><span data-stu-id="5fe71-134">Vertex</span></span> | <span data-ttu-id="5fe71-135">Envoltória</span><span class="sxs-lookup"><span data-stu-id="5fe71-135">Hull</span></span> | <span data-ttu-id="5fe71-136">Domínio</span><span class="sxs-lookup"><span data-stu-id="5fe71-136">Domain</span></span> | <span data-ttu-id="5fe71-137">Geometria</span><span class="sxs-lookup"><span data-stu-id="5fe71-137">Geometry</span></span> | <span data-ttu-id="5fe71-138">16x16</span><span class="sxs-lookup"><span data-stu-id="5fe71-138">Pixel</span></span> | <span data-ttu-id="5fe71-139">Computação</span><span class="sxs-lookup"><span data-stu-id="5fe71-139">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="5fe71-140">X</span><span class="sxs-lookup"><span data-stu-id="5fe71-140">X</span></span>      | <span data-ttu-id="5fe71-141">X</span><span class="sxs-lookup"><span data-stu-id="5fe71-141">X</span></span>    | <span data-ttu-id="5fe71-142">X</span><span class="sxs-lookup"><span data-stu-id="5fe71-142">X</span></span>      | <span data-ttu-id="5fe71-143">X</span><span class="sxs-lookup"><span data-stu-id="5fe71-143">X</span></span>        | <span data-ttu-id="5fe71-144">X</span><span class="sxs-lookup"><span data-stu-id="5fe71-144">X</span></span>     | <span data-ttu-id="5fe71-145">X</span><span class="sxs-lookup"><span data-stu-id="5fe71-145">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="5fe71-146">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="5fe71-146">Minimum Shader Model</span></span>

<span data-ttu-id="5fe71-147">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="5fe71-147">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="5fe71-148">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="5fe71-148">Shader Model</span></span>                                              | <span data-ttu-id="5fe71-149">Com suporte</span><span class="sxs-lookup"><span data-stu-id="5fe71-149">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="5fe71-150">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="5fe71-150">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="5fe71-151">sim</span><span class="sxs-lookup"><span data-stu-id="5fe71-151">yes</span></span>       |
| [<span data-ttu-id="5fe71-152">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="5fe71-152">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="5fe71-153">não</span><span class="sxs-lookup"><span data-stu-id="5fe71-153">no</span></span>        |
| [<span data-ttu-id="5fe71-154">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="5fe71-154">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="5fe71-155">não</span><span class="sxs-lookup"><span data-stu-id="5fe71-155">no</span></span>        |
| [<span data-ttu-id="5fe71-156">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5fe71-156">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="5fe71-157">não</span><span class="sxs-lookup"><span data-stu-id="5fe71-157">no</span></span>        |
| [<span data-ttu-id="5fe71-158">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5fe71-158">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="5fe71-159">não</span><span class="sxs-lookup"><span data-stu-id="5fe71-159">no</span></span>        |
| [<span data-ttu-id="5fe71-160">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5fe71-160">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="5fe71-161">não</span><span class="sxs-lookup"><span data-stu-id="5fe71-161">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="5fe71-162">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5fe71-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5fe71-163">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5fe71-163">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





