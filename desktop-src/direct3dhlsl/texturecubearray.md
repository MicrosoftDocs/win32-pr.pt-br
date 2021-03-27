---
title: Objeto TextureCubeArray
description: Tipo de TextureCubeArray (como ele existe no modelo de sombreador 4) mais variáveis de recurso. Esse objeto de textura dá suporte a esses métodos, além dos métodos no sombreador modelo 4.
ms.assetid: 62AAF0F9-D552-4FFA-B681-749D6DC205BD
keywords:
- Objeto TextureCubeArray HLSL
- Objeto TextureCubeArray HLSL, descrito
topic_type:
- apiref
api_name:
- TextureCubeArray
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e559214626fadbc08b8e9cd4d5568358f130779c
ms.sourcegitcommit: 5724b38883e518ac565e1b266defa85ad0941bb2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "104989124"
---
# <a name="texturecubearray-object"></a><span data-ttu-id="a9cff-106">Objeto TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="a9cff-106">TextureCubeArray object</span></span>

<span data-ttu-id="a9cff-107">Tipo de **TextureCubeArray** ([como ele existe no modelo de sombreador 4](dx-graphics-hlsl-to-type.md)) mais variáveis de recurso.</span><span class="sxs-lookup"><span data-stu-id="a9cff-107">**TextureCubeArray** type ([as it exists in Shader Model 4](dx-graphics-hlsl-to-type.md)) plus resource variables.</span></span> <span data-ttu-id="a9cff-108">Esse objeto de textura dá suporte a esses métodos, além dos métodos no sombreador modelo 4.</span><span class="sxs-lookup"><span data-stu-id="a9cff-108">This texture object supports these methods in addition to the methods in Shader Model 4.</span></span>

-   [<span data-ttu-id="a9cff-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="a9cff-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a9cff-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="a9cff-110">Methods</span></span>

<span data-ttu-id="a9cff-111">O objeto **TextureCubeArray** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="a9cff-111">The **TextureCubeArray** object has these methods.</span></span>



| <span data-ttu-id="a9cff-112">Método</span><span class="sxs-lookup"><span data-stu-id="a9cff-112">Method</span></span>                                                           | <span data-ttu-id="a9cff-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="a9cff-113">Description</span></span>                                                                                                                                              |
|:-----------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a9cff-114">**Gather**</span><span class="sxs-lookup"><span data-stu-id="a9cff-114">**Gather**</span></span>](texturecubearray-gather.md)                         | <span data-ttu-id="a9cff-115">Retorna os quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear.</span><span class="sxs-lookup"><span data-stu-id="a9cff-115">Returns the four texel values that would be used in a bi-linear filtering operation.</span></span><br/>                                                                |
| [<span data-ttu-id="a9cff-116">**GatherAlpha**</span><span class="sxs-lookup"><span data-stu-id="a9cff-116">**GatherAlpha**</span></span>](texturecubearray-gatheralpha.md)               | <span data-ttu-id="a9cff-117">Retorna os componentes alfa dos quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear.</span><span class="sxs-lookup"><span data-stu-id="a9cff-117">Returns the alpha components of the four texel values that would be used in a bi-linear filtering operation.</span></span><br/>                                        |
| [<span data-ttu-id="a9cff-118">**GatherBlue**</span><span class="sxs-lookup"><span data-stu-id="a9cff-118">**GatherBlue**</span></span>](texturecubearray-gatherblue.md)                 | <span data-ttu-id="a9cff-119">Retorna os componentes azuis dos quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear.</span><span class="sxs-lookup"><span data-stu-id="a9cff-119">Returns the blue components of the four texel values that would be used in a bi-linear filtering operation.</span></span><br/>                                         |
| [<span data-ttu-id="a9cff-120">**GatherCmp**</span><span class="sxs-lookup"><span data-stu-id="a9cff-120">**GatherCmp**</span></span>](texturecubearray-gathercmp.md)                   | <span data-ttu-id="a9cff-121">Para quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, o retorna a comparação contra um valor de comparação.</span><span class="sxs-lookup"><span data-stu-id="a9cff-121">For four texel values that would be used in a bi-linear filtering operation, returns their comparison against a compare value.</span></span><br/>                      |
| [<span data-ttu-id="a9cff-122">**GatherCmpAlpha**</span><span class="sxs-lookup"><span data-stu-id="a9cff-122">**GatherCmpAlpha**</span></span>](texturecubearray-gathercmpalpha.md)         | <span data-ttu-id="a9cff-123">Para quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, o retorna uma comparação de seu componente alfa em relação a um valor de comparação.</span><span class="sxs-lookup"><span data-stu-id="a9cff-123">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their alpha component against a compare value.</span></span><br/> |
| [<span data-ttu-id="a9cff-124">**GatherCmpBlue**</span><span class="sxs-lookup"><span data-stu-id="a9cff-124">**GatherCmpBlue**</span></span>](texturecubearray-gathercmpblue.md)           | <span data-ttu-id="a9cff-125">Para quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, o retorna uma comparação de seu componente azul em relação a um valor de comparação.</span><span class="sxs-lookup"><span data-stu-id="a9cff-125">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their blue component against a compare value.</span></span><br/>  |
| [<span data-ttu-id="a9cff-126">**GatherCmpGreen**</span><span class="sxs-lookup"><span data-stu-id="a9cff-126">**GatherCmpGreen**</span></span>](texturecubearray-gathercmpgreen.md)         | <span data-ttu-id="a9cff-127">Para quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, o retorna uma comparação de seu componente verde em relação a um valor de comparação.</span><span class="sxs-lookup"><span data-stu-id="a9cff-127">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their green component against a compare value.</span></span><br/> |
| [<span data-ttu-id="a9cff-128">**GatherCmpRed**</span><span class="sxs-lookup"><span data-stu-id="a9cff-128">**GatherCmpRed**</span></span>](texturecubearray-gathercmpred.md)             | <span data-ttu-id="a9cff-129">Para quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, o retorna uma comparação de seu componente vermelho em relação a um valor de comparação.</span><span class="sxs-lookup"><span data-stu-id="a9cff-129">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their red component against a compare value.</span></span><br/>   |
| [<span data-ttu-id="a9cff-130">**GatherGreen**</span><span class="sxs-lookup"><span data-stu-id="a9cff-130">**GatherGreen**</span></span>](texturecubearray-gathergreen.md)               | <span data-ttu-id="a9cff-131">Retorna os componentes verdes dos quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear.</span><span class="sxs-lookup"><span data-stu-id="a9cff-131">Returns the green components of the four texel values that would be used in a bi-linear filtering operation.</span></span><br/>                                        |
| [<span data-ttu-id="a9cff-132">**GatherRed**</span><span class="sxs-lookup"><span data-stu-id="a9cff-132">**GatherRed**</span></span>](texturecubearray-gatherred.md)                   | <span data-ttu-id="a9cff-133">Retorna os componentes vermelhos dos quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear.</span><span class="sxs-lookup"><span data-stu-id="a9cff-133">Returns the red components of the four texel values that would be used in a bi-linear filtering operation.</span></span><br/>                                          |
| [<span data-ttu-id="a9cff-134">**Nova**</span><span class="sxs-lookup"><span data-stu-id="a9cff-134">**Sample**</span></span>](texturecubearray-sample.md)                         | <span data-ttu-id="a9cff-135">Amostra uma textura.</span><span class="sxs-lookup"><span data-stu-id="a9cff-135">Samples a texture.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="a9cff-136">**SampleBias**</span><span class="sxs-lookup"><span data-stu-id="a9cff-136">**SampleBias**</span></span>](texturecubearray-samplebias.md)                 | <span data-ttu-id="a9cff-137">Amostra uma textura, depois de aplicar o valor de tendência ao nível de mipmap.</span><span class="sxs-lookup"><span data-stu-id="a9cff-137">Samples a texture, after applying the bias value to the mipmap level.</span></span><br/>                                                                               |
| [<span data-ttu-id="a9cff-138">**SampleCmp**</span><span class="sxs-lookup"><span data-stu-id="a9cff-138">**SampleCmp**</span></span>](texturecubearray-samplecmp.md)                   | <span data-ttu-id="a9cff-139">Amostra uma textura, usando um valor de comparação para rejeitar amostras.</span><span class="sxs-lookup"><span data-stu-id="a9cff-139">Samples a texture, using a comparison value to reject samples.</span></span><br/>                                                                                      |
| [<span data-ttu-id="a9cff-140">**SampleCmpLevelZero**</span><span class="sxs-lookup"><span data-stu-id="a9cff-140">**SampleCmpLevelZero**</span></span>](texturecubearray-samplecmplevelzero.md) | <span data-ttu-id="a9cff-141">Amostras de uma textura (somente mipmap nível 0), usando um valor de comparação para rejeitar amostras.</span><span class="sxs-lookup"><span data-stu-id="a9cff-141">Samples a texture (mipmap level 0 only), using a comparison value to reject samples.</span></span><br/>                                                                |
| [<span data-ttu-id="a9cff-142">**SampleGrad**</span><span class="sxs-lookup"><span data-stu-id="a9cff-142">**SampleGrad**</span></span>](texturecubearray-samplegrad.md)                 | <span data-ttu-id="a9cff-143">Amostra uma textura usando um gradiente para influenciar a maneira como o local de exemplo é calculado.</span><span class="sxs-lookup"><span data-stu-id="a9cff-143">Samples a texture using a gradient to influence the way the sample location is calculated.</span></span><br/>                                                          |
| [<span data-ttu-id="a9cff-144">**SampleLevel**</span><span class="sxs-lookup"><span data-stu-id="a9cff-144">**SampleLevel**</span></span>](texturecubearray-samplelevel.md)               | <span data-ttu-id="a9cff-145">Amostra uma textura no nível de mipmap especificado.</span><span class="sxs-lookup"><span data-stu-id="a9cff-145">Samples a texture on the specified mipmap level.</span></span><br/>                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="a9cff-146">Comentários</span><span class="sxs-lookup"><span data-stu-id="a9cff-146">Remarks</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="a9cff-147">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="a9cff-147">Minimum Shader Model</span></span>

<span data-ttu-id="a9cff-148">Esse objeto tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="a9cff-148">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="a9cff-149">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="a9cff-149">Shader Model</span></span>                                                                | <span data-ttu-id="a9cff-150">Com suporte</span><span class="sxs-lookup"><span data-stu-id="a9cff-150">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="a9cff-151">[Modelo](d3d11-graphics-reference-sm5.md) de sombreador 5 e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="a9cff-151">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="a9cff-152">sim</span><span class="sxs-lookup"><span data-stu-id="a9cff-152">yes</span></span>       |



 

<span data-ttu-id="a9cff-153">Este objeto tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="a9cff-153">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="a9cff-154">Vértice</span><span class="sxs-lookup"><span data-stu-id="a9cff-154">Vertex</span></span> | <span data-ttu-id="a9cff-155">Envoltória</span><span class="sxs-lookup"><span data-stu-id="a9cff-155">Hull</span></span> | <span data-ttu-id="a9cff-156">Domínio</span><span class="sxs-lookup"><span data-stu-id="a9cff-156">Domain</span></span> | <span data-ttu-id="a9cff-157">Geometria</span><span class="sxs-lookup"><span data-stu-id="a9cff-157">Geometry</span></span> | <span data-ttu-id="a9cff-158">16x16</span><span class="sxs-lookup"><span data-stu-id="a9cff-158">Pixel</span></span> | <span data-ttu-id="a9cff-159">Computação</span><span class="sxs-lookup"><span data-stu-id="a9cff-159">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="a9cff-160">x</span><span class="sxs-lookup"><span data-stu-id="a9cff-160">x</span></span>      | <span data-ttu-id="a9cff-161">x</span><span class="sxs-lookup"><span data-stu-id="a9cff-161">x</span></span>    | <span data-ttu-id="a9cff-162">x</span><span class="sxs-lookup"><span data-stu-id="a9cff-162">x</span></span>      | <span data-ttu-id="a9cff-163">x</span><span class="sxs-lookup"><span data-stu-id="a9cff-163">x</span></span>        | <span data-ttu-id="a9cff-164">x</span><span class="sxs-lookup"><span data-stu-id="a9cff-164">x</span></span>     | <span data-ttu-id="a9cff-165">x</span><span class="sxs-lookup"><span data-stu-id="a9cff-165">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="a9cff-166">Confira também</span><span class="sxs-lookup"><span data-stu-id="a9cff-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9cff-167">Objetos do Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="a9cff-167">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 





