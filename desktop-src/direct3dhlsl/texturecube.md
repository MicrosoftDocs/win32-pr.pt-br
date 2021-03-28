---
title: Objeto TextureCube
description: Tipo de TextureCube (como ele existe no modelo de sombreador 4) mais variáveis de recurso. Esse objeto de textura dá suporte a esses métodos, além dos métodos no sombreador modelo 4.
ms.assetid: BC96D7BB-992E-48CC-A774-E211E1BB1720
keywords:
- Objeto TextureCube HLSL
- Objeto TextureCube HLSL, descrito
topic_type:
- apiref
api_name:
- TextureCube
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 939c79895ae1c24665fc70d6b6cf2ced19854e2b
ms.sourcegitcommit: 5724b38883e518ac565e1b266defa85ad0941bb2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "104091865"
---
# <a name="texturecube-object"></a><span data-ttu-id="6d922-106">Objeto TextureCube</span><span class="sxs-lookup"><span data-stu-id="6d922-106">TextureCube object</span></span>

<span data-ttu-id="6d922-107">Tipo de **TextureCube** ([como ele existe no modelo de sombreador 4](dx-graphics-hlsl-to-type.md)) mais variáveis de recurso.</span><span class="sxs-lookup"><span data-stu-id="6d922-107">**TextureCube** type ([as it exists in Shader Model 4](dx-graphics-hlsl-to-type.md)) plus resource variables.</span></span> <span data-ttu-id="6d922-108">Esse objeto de textura dá suporte a esses métodos, além dos métodos no sombreador modelo 4.</span><span class="sxs-lookup"><span data-stu-id="6d922-108">This texture object supports these methods in addition to the methods in Shader Model 4.</span></span>

-   [<span data-ttu-id="6d922-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="6d922-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6d922-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="6d922-110">Methods</span></span>

<span data-ttu-id="6d922-111">O objeto **TextureCube** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="6d922-111">The **TextureCube** object has these methods.</span></span>



| <span data-ttu-id="6d922-112">Método</span><span class="sxs-lookup"><span data-stu-id="6d922-112">Method</span></span>                                                      | <span data-ttu-id="6d922-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="6d922-113">Description</span></span>                                                                                                                                             |
|:------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6d922-114">**Gather**</span><span class="sxs-lookup"><span data-stu-id="6d922-114">**Gather**</span></span>](texturecube-gather.md)                         | <span data-ttu-id="6d922-115">Retorna os quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear.</span><span class="sxs-lookup"><span data-stu-id="6d922-115">Returns the four texel values that would be used in a bi-linear filtering operation.</span></span><br/>                                                                |
| [<span data-ttu-id="6d922-116">**GatherAlpha**</span><span class="sxs-lookup"><span data-stu-id="6d922-116">**GatherAlpha**</span></span>](texturecube-gatheralpha.md)               | <span data-ttu-id="6d922-117">Retorna os componentes alfa dos quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear.</span><span class="sxs-lookup"><span data-stu-id="6d922-117">Returns the alpha components of the four texel values that would be used in a bi-linear filtering operation.</span></span><br/>                                        |
| [<span data-ttu-id="6d922-118">**GatherBlue**</span><span class="sxs-lookup"><span data-stu-id="6d922-118">**GatherBlue**</span></span>](texturecube-gatherblue.md)                 | <span data-ttu-id="6d922-119">Retorna os componentes azuis dos quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear.</span><span class="sxs-lookup"><span data-stu-id="6d922-119">Returns the blue components of the four texel values that would be used in a bi-linear filtering operation.</span></span><br/>                                         |
| [<span data-ttu-id="6d922-120">**GatherCmp**</span><span class="sxs-lookup"><span data-stu-id="6d922-120">**GatherCmp**</span></span>](texturecube-gathercmp.md)                   | <span data-ttu-id="6d922-121">Para quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, o retorna a comparação contra um valor de comparação.</span><span class="sxs-lookup"><span data-stu-id="6d922-121">For four texel values that would be used in a bi-linear filtering operation, returns their comparison against a compare value.</span></span><br/>                      |
| [<span data-ttu-id="6d922-122">**GatherCmpAlpha**</span><span class="sxs-lookup"><span data-stu-id="6d922-122">**GatherCmpAlpha**</span></span>](texturecube-gathercmpalpha.md)         | <span data-ttu-id="6d922-123">Para quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, o retorna uma comparação de seu componente alfa em relação a um valor de comparação.</span><span class="sxs-lookup"><span data-stu-id="6d922-123">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their alpha component against a compare value.</span></span><br/> |
| [<span data-ttu-id="6d922-124">**GatherCmpBlue**</span><span class="sxs-lookup"><span data-stu-id="6d922-124">**GatherCmpBlue**</span></span>](texturecube-gathercmpblue.md)           | <span data-ttu-id="6d922-125">Para quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, o retorna uma comparação de seu componente azul em relação a um valor de comparação.</span><span class="sxs-lookup"><span data-stu-id="6d922-125">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their blue component against a compare value.</span></span><br/>  |
| [<span data-ttu-id="6d922-126">**GatherCmpGreen**</span><span class="sxs-lookup"><span data-stu-id="6d922-126">**GatherCmpGreen**</span></span>](texturecube-gathercmpgreen.md)         | <span data-ttu-id="6d922-127">Para quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, o retorna uma comparação de seu componente verde em relação a um valor de comparação.</span><span class="sxs-lookup"><span data-stu-id="6d922-127">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their green component against a compare value.</span></span><br/> |
| [<span data-ttu-id="6d922-128">**GatherCmpRed**</span><span class="sxs-lookup"><span data-stu-id="6d922-128">**GatherCmpRed**</span></span>](texturecube-gathercmpred.md)             | <span data-ttu-id="6d922-129">Para quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, o retorna uma comparação de seu componente vermelho em relação a um valor de comparação.</span><span class="sxs-lookup"><span data-stu-id="6d922-129">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their red component against a compare value.</span></span><br/>   |
| [<span data-ttu-id="6d922-130">**GatherGreen**</span><span class="sxs-lookup"><span data-stu-id="6d922-130">**GatherGreen**</span></span>](texturecube-gathergreen.md)               | <span data-ttu-id="6d922-131">Retorna os componentes verdes dos quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear.</span><span class="sxs-lookup"><span data-stu-id="6d922-131">Returns the green components of the four texel values that would be used in a bi-linear filtering operation.</span></span><br/>                                        |
| [<span data-ttu-id="6d922-132">**GatherRed**</span><span class="sxs-lookup"><span data-stu-id="6d922-132">**GatherRed**</span></span>](texturecube-gatherred.md)                   | <span data-ttu-id="6d922-133">Retorna os componentes vermelhos dos quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear.</span><span class="sxs-lookup"><span data-stu-id="6d922-133">Returns the red components of the four texel values that would be used in a bi-linear filtering operation.</span></span><br/>                                          |
| [<span data-ttu-id="6d922-134">**Nova**</span><span class="sxs-lookup"><span data-stu-id="6d922-134">**Sample**</span></span>](texturecube-sample.md)                         | <span data-ttu-id="6d922-135">Amostra uma textura.</span><span class="sxs-lookup"><span data-stu-id="6d922-135">Samples a texture.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="6d922-136">**SampleBias**</span><span class="sxs-lookup"><span data-stu-id="6d922-136">**SampleBias**</span></span>](texturecube-samplebias.md)                 | <span data-ttu-id="6d922-137">Amostra uma textura, depois de aplicar o valor de tendência ao nível de mipmap.</span><span class="sxs-lookup"><span data-stu-id="6d922-137">Samples a texture, after applying the bias value to the mipmap level.</span></span><br/>                                                                               |
| [<span data-ttu-id="6d922-138">**SampleCmp**</span><span class="sxs-lookup"><span data-stu-id="6d922-138">**SampleCmp**</span></span>](texturecube-samplecmp.md)                   | <span data-ttu-id="6d922-139">Amostra uma textura, usando um valor de comparação para rejeitar amostras.</span><span class="sxs-lookup"><span data-stu-id="6d922-139">Samples a texture, using a comparison value to reject samples.</span></span><br/>                                                                                      |
| [<span data-ttu-id="6d922-140">**SampleCmpLevelZero**</span><span class="sxs-lookup"><span data-stu-id="6d922-140">**SampleCmpLevelZero**</span></span>](texturecube-samplecmplevelzero.md) | <span data-ttu-id="6d922-141">Amostras de uma textura (somente mipmap nível 0), usando um valor de comparação para rejeitar amostras.</span><span class="sxs-lookup"><span data-stu-id="6d922-141">Samples a texture (mipmap level 0 only), using a comparison value to reject samples.</span></span><br/>                                                                |
| [<span data-ttu-id="6d922-142">**SampleGrad**</span><span class="sxs-lookup"><span data-stu-id="6d922-142">**SampleGrad**</span></span>](texturecube-samplegrad.md)                 | <span data-ttu-id="6d922-143">Amostra uma textura usando um gradiente para influenciar a maneira como o local de exemplo é calculado.</span><span class="sxs-lookup"><span data-stu-id="6d922-143">Samples a texture using a gradient to influence the way the sample location is calculated.</span></span><br/>                                                          |
| [<span data-ttu-id="6d922-144">**SampleLevel**</span><span class="sxs-lookup"><span data-stu-id="6d922-144">**SampleLevel**</span></span>](texturecube-samplelevel.md)               | <span data-ttu-id="6d922-145">Amostra uma textura no nível de mipmap especificado.</span><span class="sxs-lookup"><span data-stu-id="6d922-145">Samples a texture on the specified mipmap level.</span></span><br/>                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="6d922-146">Comentários</span><span class="sxs-lookup"><span data-stu-id="6d922-146">Remarks</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="6d922-147">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="6d922-147">Minimum Shader Model</span></span>

<span data-ttu-id="6d922-148">Esse objeto tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="6d922-148">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="6d922-149">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="6d922-149">Shader Model</span></span>                                                                | <span data-ttu-id="6d922-150">Com suporte</span><span class="sxs-lookup"><span data-stu-id="6d922-150">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="6d922-151">[Modelo](d3d11-graphics-reference-sm5.md) de sombreador 5 e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="6d922-151">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="6d922-152">sim</span><span class="sxs-lookup"><span data-stu-id="6d922-152">yes</span></span>       |



 

<span data-ttu-id="6d922-153">Este objeto tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="6d922-153">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="6d922-154">Vértice</span><span class="sxs-lookup"><span data-stu-id="6d922-154">Vertex</span></span> | <span data-ttu-id="6d922-155">Envoltória</span><span class="sxs-lookup"><span data-stu-id="6d922-155">Hull</span></span> | <span data-ttu-id="6d922-156">Domínio</span><span class="sxs-lookup"><span data-stu-id="6d922-156">Domain</span></span> | <span data-ttu-id="6d922-157">Geometria</span><span class="sxs-lookup"><span data-stu-id="6d922-157">Geometry</span></span> | <span data-ttu-id="6d922-158">16x16</span><span class="sxs-lookup"><span data-stu-id="6d922-158">Pixel</span></span> | <span data-ttu-id="6d922-159">Computação</span><span class="sxs-lookup"><span data-stu-id="6d922-159">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="6d922-160">x</span><span class="sxs-lookup"><span data-stu-id="6d922-160">x</span></span>      | <span data-ttu-id="6d922-161">x</span><span class="sxs-lookup"><span data-stu-id="6d922-161">x</span></span>    | <span data-ttu-id="6d922-162">x</span><span class="sxs-lookup"><span data-stu-id="6d922-162">x</span></span>      | <span data-ttu-id="6d922-163">x</span><span class="sxs-lookup"><span data-stu-id="6d922-163">x</span></span>        | <span data-ttu-id="6d922-164">x</span><span class="sxs-lookup"><span data-stu-id="6d922-164">x</span></span>     | <span data-ttu-id="6d922-165">x</span><span class="sxs-lookup"><span data-stu-id="6d922-165">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="6d922-166">Confira também</span><span class="sxs-lookup"><span data-stu-id="6d922-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d922-167">Objetos do Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="6d922-167">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 





