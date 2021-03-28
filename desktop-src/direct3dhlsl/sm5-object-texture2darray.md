---
title: Texture2DArray
description: Texture2DArray
ms.assetid: 78ab2feb-4d67-4f6f-bffe-48d55183ce28
keywords:
- Texture2DArray HLSL
topic_type:
- apiref
api_name:
- Texture2DArray
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f1aefa9171ed634934ea5e1306973fe3b22abdfa
ms.sourcegitcommit: 5724b38883e518ac565e1b266defa85ad0941bb2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "104968262"
---
# <a name="texture2darray"></a><span data-ttu-id="4e29e-104">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="4e29e-104">Texture2DArray</span></span>

<span data-ttu-id="4e29e-105">Tipo de Texture2DArray ([como ele existe no modelo de sombreador 4](dx-graphics-hlsl-to-type.md)) mais variáveis de recurso.</span><span class="sxs-lookup"><span data-stu-id="4e29e-105">Texture2DArray type ([as it exists in Shader Model 4](dx-graphics-hlsl-to-type.md)) plus resource variables.</span></span> <span data-ttu-id="4e29e-106">Esse objeto de textura dá suporte aos métodos a seguir, além dos métodos no sombreador modelo 4.</span><span class="sxs-lookup"><span data-stu-id="4e29e-106">This texture object supports the following methods in addition to the methods in Shader Model 4.</span></span>



| <span data-ttu-id="4e29e-107">Método</span><span class="sxs-lookup"><span data-stu-id="4e29e-107">Method</span></span>                                                                      | <span data-ttu-id="4e29e-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="4e29e-108">Description</span></span>                                                                                                                                         |
|-----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4e29e-109">**Gather**</span><span class="sxs-lookup"><span data-stu-id="4e29e-109">**Gather**</span></span>](texture2darray-gather.md)                                      | <span data-ttu-id="4e29e-110">Retorna os quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear.</span><span class="sxs-lookup"><span data-stu-id="4e29e-110">Returns the four texel values that would be used in a bi-linear filtering operation.</span></span>                                                                |
| [<span data-ttu-id="4e29e-111">**GatherRed**</span><span class="sxs-lookup"><span data-stu-id="4e29e-111">**GatherRed**</span></span>](texture2darray-gatherred.md)                                | <span data-ttu-id="4e29e-112">Retorna os componentes vermelhos dos quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear.</span><span class="sxs-lookup"><span data-stu-id="4e29e-112">Returns the red components of the four texel values that would be used in a bi-linear filtering operation.</span></span>                                          |
| [<span data-ttu-id="4e29e-113">**GatherGreen**</span><span class="sxs-lookup"><span data-stu-id="4e29e-113">**GatherGreen**</span></span>](texture2darray-gathergreen.md)                            | <span data-ttu-id="4e29e-114">Retorna os componentes verdes dos quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear.</span><span class="sxs-lookup"><span data-stu-id="4e29e-114">Returns the green components of the four texel values that would be used in a bi-linear filtering operation.</span></span>                                        |
| [<span data-ttu-id="4e29e-115">**GatherBlue**</span><span class="sxs-lookup"><span data-stu-id="4e29e-115">**GatherBlue**</span></span>](texture2darray-gatherblue.md)                              | <span data-ttu-id="4e29e-116">Retorna os componentes azuis dos quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear.</span><span class="sxs-lookup"><span data-stu-id="4e29e-116">Returns the blue components of the four texel values that would be used in a bi-linear filtering operation.</span></span>                                         |
| [<span data-ttu-id="4e29e-117">**GatherAlpha**</span><span class="sxs-lookup"><span data-stu-id="4e29e-117">**GatherAlpha**</span></span>](texture2darray-gatheralpha.md)                            | <span data-ttu-id="4e29e-118">Retorna os componentes alfa dos quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear.</span><span class="sxs-lookup"><span data-stu-id="4e29e-118">Returns the alpha components of the four texel values that would be used in a bi-linear filtering operation.</span></span>                                        |
| [<span data-ttu-id="4e29e-119">**GatherCmp**</span><span class="sxs-lookup"><span data-stu-id="4e29e-119">**GatherCmp**</span></span>](texture2darray-gathercmp.md)                                | <span data-ttu-id="4e29e-120">Para quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, o retorna a comparação contra um valor de comparação.</span><span class="sxs-lookup"><span data-stu-id="4e29e-120">For four texel values that would be used in a bi-linear filtering operation, returns their comparison against a compare value.</span></span>                      |
| [<span data-ttu-id="4e29e-121">**GatherCmpRed**</span><span class="sxs-lookup"><span data-stu-id="4e29e-121">**GatherCmpRed**</span></span>](texture2darray-gathercmpred.md)                          | <span data-ttu-id="4e29e-122">Para quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, o retorna uma comparação de seu componente vermelho em relação a um valor de comparação.</span><span class="sxs-lookup"><span data-stu-id="4e29e-122">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their red component against a compare value.</span></span>   |
| [<span data-ttu-id="4e29e-123">**GatherCmpGreen**</span><span class="sxs-lookup"><span data-stu-id="4e29e-123">**GatherCmpGreen**</span></span>](texture2darray-gathercmpgreen.md)                      | <span data-ttu-id="4e29e-124">Para quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, o retorna uma comparação de seu componente verde em relação a um valor de comparação.</span><span class="sxs-lookup"><span data-stu-id="4e29e-124">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their green component against a compare value.</span></span> |
| [<span data-ttu-id="4e29e-125">**GatherCmpBlue**</span><span class="sxs-lookup"><span data-stu-id="4e29e-125">**GatherCmpBlue**</span></span>](texture2darray-gathercmpblue.md)                        | <span data-ttu-id="4e29e-126">Para quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, o retorna uma comparação de seu componente azul em relação a um valor de comparação.</span><span class="sxs-lookup"><span data-stu-id="4e29e-126">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their blue component against a compare value.</span></span>  |
| [<span data-ttu-id="4e29e-127">**GatherCmpAlpha**</span><span class="sxs-lookup"><span data-stu-id="4e29e-127">**GatherCmpAlpha**</span></span>](texture2darray-gathercmpalpha.md)                      | <span data-ttu-id="4e29e-128">Para quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, o retorna uma comparação de seu componente alfa em relação a um valor de comparação.</span><span class="sxs-lookup"><span data-stu-id="4e29e-128">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their alpha component against a compare value.</span></span> |
| [<span data-ttu-id="4e29e-129">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="4e29e-129">**GetDimensions**</span></span>](sm5-object-texture2darray-getdimensions.md)             | <span data-ttu-id="4e29e-130">Obtém as dimensões do recurso.</span><span class="sxs-lookup"><span data-stu-id="4e29e-130">Gets the resource dimensions.</span></span>                                                                                                                       |
| [<span data-ttu-id="4e29e-131">**Carregamento**</span><span class="sxs-lookup"><span data-stu-id="4e29e-131">**Load**</span></span>](texture2darray-load.md)                                          | <span data-ttu-id="4e29e-132">Lê dados de textura.</span><span class="sxs-lookup"><span data-stu-id="4e29e-132">Reads texture data.</span></span>                                                                                                                                 |
| <span data-ttu-id="4e29e-133">[**seqüencia. Operador\[\]\[\]**](sm5-object-texture2darray-mipsoperatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="4e29e-133">[**mips.Operator\[\]\[\]**](sm5-object-texture2darray-mipsoperatorindex.md)</span></span> | <span data-ttu-id="4e29e-134">Obtém uma variável de recurso somente leitura.</span><span class="sxs-lookup"><span data-stu-id="4e29e-134">Gets a read-only resource variable.</span></span>                                                                                                                 |
| <span data-ttu-id="4e29e-135">[**Operador\[\]**](sm5-object-texture2darray-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="4e29e-135">[**Operator\[\]**](sm5-object-texture2darray-operatorindex.md)</span></span>              | <span data-ttu-id="4e29e-136">Obtém uma variável de recurso somente leitura.</span><span class="sxs-lookup"><span data-stu-id="4e29e-136">Gets a read-only resource variable.</span></span>                                                                                                                 |
| [<span data-ttu-id="4e29e-137">**Nova**</span><span class="sxs-lookup"><span data-stu-id="4e29e-137">**Sample**</span></span>](texture2darray-sample.md)                                      | <span data-ttu-id="4e29e-138">Amostra uma textura.</span><span class="sxs-lookup"><span data-stu-id="4e29e-138">Samples a texture.</span></span>                                                                                                                                  |
| [<span data-ttu-id="4e29e-139">**SampleBias**</span><span class="sxs-lookup"><span data-stu-id="4e29e-139">**SampleBias**</span></span>](texture2darray-samplebias.md)                              | <span data-ttu-id="4e29e-140">Amostra uma textura, depois de aplicar o valor de tendência ao nível de mipmap.</span><span class="sxs-lookup"><span data-stu-id="4e29e-140">Samples a texture, after applying the bias value to the mipmap level.</span></span>                                                                               |
| [<span data-ttu-id="4e29e-141">**SampleCmp**</span><span class="sxs-lookup"><span data-stu-id="4e29e-141">**SampleCmp**</span></span>](texture2darray-samplecmp.md)                                | <span data-ttu-id="4e29e-142">Amostra uma textura, usando um valor de comparação para rejeitar amostras.</span><span class="sxs-lookup"><span data-stu-id="4e29e-142">Samples a texture, using a comparison value to reject samples.</span></span>                                                                                      |
| [<span data-ttu-id="4e29e-143">**SampleCmpLevelZero**</span><span class="sxs-lookup"><span data-stu-id="4e29e-143">**SampleCmpLevelZero**</span></span>](texture2darray-samplecmplevelzero.md)              | <span data-ttu-id="4e29e-144">Amostras de uma textura (somente mipmap nível 0), usando um valor de comparação para rejeitar amostras.</span><span class="sxs-lookup"><span data-stu-id="4e29e-144">Samples a texture (mipmap level 0 only), using a comparison value to reject samples.</span></span>                                                                |
| [<span data-ttu-id="4e29e-145">**SampleGrad**</span><span class="sxs-lookup"><span data-stu-id="4e29e-145">**SampleGrad**</span></span>](texture2darray-samplegrad.md)                              | <span data-ttu-id="4e29e-146">Amostra uma textura usando um gradiente para influenciar a maneira como o local de exemplo é calculado.</span><span class="sxs-lookup"><span data-stu-id="4e29e-146">Samples a texture using a gradient to influence the way the sample location is calculated.</span></span>                                                          |
| [<span data-ttu-id="4e29e-147">**SampleLevel**</span><span class="sxs-lookup"><span data-stu-id="4e29e-147">**SampleLevel**</span></span>](texture2darray-samplelevel.md)                            | <span data-ttu-id="4e29e-148">Amostra uma textura no nível de mipmap especificado.</span><span class="sxs-lookup"><span data-stu-id="4e29e-148">Samples a texture on the specified mipmap level.</span></span>                                                                                                    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="4e29e-149">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="4e29e-149">Minimum Shader Model</span></span>

<span data-ttu-id="4e29e-150">Esse objeto tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="4e29e-150">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="4e29e-151">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="4e29e-151">Shader Model</span></span>                                                                | <span data-ttu-id="4e29e-152">Com suporte</span><span class="sxs-lookup"><span data-stu-id="4e29e-152">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="4e29e-153">[Modelo](d3d11-graphics-reference-sm5.md) de sombreador 5 e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="4e29e-153">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="4e29e-154">sim</span><span class="sxs-lookup"><span data-stu-id="4e29e-154">yes</span></span>       |



 

<span data-ttu-id="4e29e-155">Este objeto tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="4e29e-155">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="4e29e-156">Vértice</span><span class="sxs-lookup"><span data-stu-id="4e29e-156">Vertex</span></span> | <span data-ttu-id="4e29e-157">Envoltória</span><span class="sxs-lookup"><span data-stu-id="4e29e-157">Hull</span></span> | <span data-ttu-id="4e29e-158">Domínio</span><span class="sxs-lookup"><span data-stu-id="4e29e-158">Domain</span></span> | <span data-ttu-id="4e29e-159">Geometria</span><span class="sxs-lookup"><span data-stu-id="4e29e-159">Geometry</span></span> | <span data-ttu-id="4e29e-160">16x16</span><span class="sxs-lookup"><span data-stu-id="4e29e-160">Pixel</span></span> | <span data-ttu-id="4e29e-161">Computação</span><span class="sxs-lookup"><span data-stu-id="4e29e-161">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="4e29e-162">x</span><span class="sxs-lookup"><span data-stu-id="4e29e-162">x</span></span>      | <span data-ttu-id="4e29e-163">x</span><span class="sxs-lookup"><span data-stu-id="4e29e-163">x</span></span>    | <span data-ttu-id="4e29e-164">x</span><span class="sxs-lookup"><span data-stu-id="4e29e-164">x</span></span>      | <span data-ttu-id="4e29e-165">x</span><span class="sxs-lookup"><span data-stu-id="4e29e-165">x</span></span>        | <span data-ttu-id="4e29e-166">x</span><span class="sxs-lookup"><span data-stu-id="4e29e-166">x</span></span>     | <span data-ttu-id="4e29e-167">x</span><span class="sxs-lookup"><span data-stu-id="4e29e-167">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="4e29e-168">Confira também</span><span class="sxs-lookup"><span data-stu-id="4e29e-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e29e-169">Objetos do Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="4e29e-169">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




