---
title: Texture2D
description: Texture2D
ms.assetid: e4f9cfd8-65e6-4375-8f87-736bca32cad4
keywords:
- Texture2D HLSL
topic_type:
- apiref
api_name:
- Texture2D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f0c9b73d66f1c5a38b077b241df8e5859b706e2f
ms.sourcegitcommit: 5724b38883e518ac565e1b266defa85ad0941bb2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "104968266"
---
# <a name="texture2d"></a><span data-ttu-id="02611-104">Texture2D</span><span class="sxs-lookup"><span data-stu-id="02611-104">Texture2D</span></span>

<span data-ttu-id="02611-105">Tipo de Texture2D ([como ele existe no modelo de sombreador 4](dx-graphics-hlsl-to-type.md)) mais variáveis de recurso.</span><span class="sxs-lookup"><span data-stu-id="02611-105">Texture2D type ([as it exists in Shader Model 4](dx-graphics-hlsl-to-type.md)) plus resource variables.</span></span> <span data-ttu-id="02611-106">Esse objeto de textura dá suporte aos métodos a seguir, além dos métodos no sombreador modelo 4.</span><span class="sxs-lookup"><span data-stu-id="02611-106">This texture object supports the following methods in addition to the methods in Shader Model 4.</span></span>



| <span data-ttu-id="02611-107">Método</span><span class="sxs-lookup"><span data-stu-id="02611-107">Method</span></span>                                                                 | <span data-ttu-id="02611-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="02611-108">Description</span></span>                                                                                                                                        |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="02611-109">**Gather**</span><span class="sxs-lookup"><span data-stu-id="02611-109">**Gather**</span></span>](texture2d-gather.md)                                      | <span data-ttu-id="02611-110">Retorna os quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear.</span><span class="sxs-lookup"><span data-stu-id="02611-110">Returns the four texel values that would be used in a bi-linear filtering operation.</span></span>                                                                |
| [<span data-ttu-id="02611-111">**GatherRed**</span><span class="sxs-lookup"><span data-stu-id="02611-111">**GatherRed**</span></span>](texture2d-gatherred.md)                                | <span data-ttu-id="02611-112">Retorna os componentes vermelhos dos quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear.</span><span class="sxs-lookup"><span data-stu-id="02611-112">Returns the red components of the four texel values that would be used in a bi-linear filtering operation.</span></span>                                          |
| [<span data-ttu-id="02611-113">**GatherGreen**</span><span class="sxs-lookup"><span data-stu-id="02611-113">**GatherGreen**</span></span>](texture2d-gathergreen.md)                            | <span data-ttu-id="02611-114">Retorna os componentes verdes dos quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear.</span><span class="sxs-lookup"><span data-stu-id="02611-114">Returns the green components of the four texel values that would be used in a bi-linear filtering operation.</span></span>                                        |
| [<span data-ttu-id="02611-115">**GatherBlue**</span><span class="sxs-lookup"><span data-stu-id="02611-115">**GatherBlue**</span></span>](texture2d-gatherblue.md)                              | <span data-ttu-id="02611-116">Retorna os componentes azuis dos quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear.</span><span class="sxs-lookup"><span data-stu-id="02611-116">Returns the blue components of the four texel values that would be used in a bi-linear filtering operation.</span></span>                                         |
| [<span data-ttu-id="02611-117">**GatherAlpha**</span><span class="sxs-lookup"><span data-stu-id="02611-117">**GatherAlpha**</span></span>](texture2d-gatheralpha.md)                            | <span data-ttu-id="02611-118">Retorna os componentes alfa dos quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear.</span><span class="sxs-lookup"><span data-stu-id="02611-118">Returns the alpha components of the four texel values that would be used in a bi-linear filtering operation.</span></span>                                        |
| [<span data-ttu-id="02611-119">**GatherCmp**</span><span class="sxs-lookup"><span data-stu-id="02611-119">**GatherCmp**</span></span>](texture2d-gathercmp.md)                                | <span data-ttu-id="02611-120">Para quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, o retorna a comparação contra um valor de comparação.</span><span class="sxs-lookup"><span data-stu-id="02611-120">For four texel values that would be used in a bi-linear filtering operation, returns their comparison against a compare value.</span></span>                      |
| [<span data-ttu-id="02611-121">**GatherCmpRed**</span><span class="sxs-lookup"><span data-stu-id="02611-121">**GatherCmpRed**</span></span>](texture2d-gathercmpred.md)                          | <span data-ttu-id="02611-122">Para quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, o retorna uma comparação de seu componente vermelho em relação a um valor de comparação.</span><span class="sxs-lookup"><span data-stu-id="02611-122">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their red component against a compare value.</span></span>   |
| [<span data-ttu-id="02611-123">**GatherCmpGreen**</span><span class="sxs-lookup"><span data-stu-id="02611-123">**GatherCmpGreen**</span></span>](texture2d-gathercmpgreen.md)                      | <span data-ttu-id="02611-124">Para quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, o retorna uma comparação de seu componente verde em relação a um valor de comparação.</span><span class="sxs-lookup"><span data-stu-id="02611-124">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their green component against a compare value.</span></span> |
| [<span data-ttu-id="02611-125">**GatherCmpBlue**</span><span class="sxs-lookup"><span data-stu-id="02611-125">**GatherCmpBlue**</span></span>](texture2d-gathercmpblue.md)                        | <span data-ttu-id="02611-126">Para quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, o retorna uma comparação de seu componente azul em relação a um valor de comparação.</span><span class="sxs-lookup"><span data-stu-id="02611-126">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their blue component against a compare value.</span></span>  |
| [<span data-ttu-id="02611-127">**GatherCmpAlpha**</span><span class="sxs-lookup"><span data-stu-id="02611-127">**GatherCmpAlpha**</span></span>](texture2d-gathercmpalpha.md)                      | <span data-ttu-id="02611-128">Para quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, o retorna uma comparação de seu componente alfa em relação a um valor de comparação.</span><span class="sxs-lookup"><span data-stu-id="02611-128">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their alpha component against a compare value.</span></span> |
| [<span data-ttu-id="02611-129">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="02611-129">**GetDimensions**</span></span>](sm5-object-texture2d-getdimensions.md)             | <span data-ttu-id="02611-130">Obtém as dimensões do recurso.</span><span class="sxs-lookup"><span data-stu-id="02611-130">Gets the resource dimensions.</span></span>                                                                                                                       |
| [<span data-ttu-id="02611-131">**Carregamento**</span><span class="sxs-lookup"><span data-stu-id="02611-131">**Load**</span></span>](texture2d-load.md)                                          | <span data-ttu-id="02611-132">Lê dados de textura.</span><span class="sxs-lookup"><span data-stu-id="02611-132">Reads texture data.</span></span>                                                                                                                                 |
| <span data-ttu-id="02611-133">[**seqüencia. Operador\[\]\[\]**](sm5-object-texture2d-mipsoperatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="02611-133">[**mips.Operator\[\]\[\]**](sm5-object-texture2d-mipsoperatorindex.md)</span></span> | <span data-ttu-id="02611-134">Obtém uma variável de recurso somente leitura.</span><span class="sxs-lookup"><span data-stu-id="02611-134">Gets a read-only resource variable.</span></span>                                                                                                                 |
| <span data-ttu-id="02611-135">[**Operador\[\]**](sm5-object-texture2d-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="02611-135">[**Operator\[\]**](sm5-object-texture2d-operatorindex.md)</span></span>              | <span data-ttu-id="02611-136">Obtém uma variável de recurso somente leitura.</span><span class="sxs-lookup"><span data-stu-id="02611-136">Gets a read-only resource variable.</span></span>                                                                                                                 |
| [<span data-ttu-id="02611-137">**Nova**</span><span class="sxs-lookup"><span data-stu-id="02611-137">**Sample**</span></span>](texture-sample-overload.md)                               | <span data-ttu-id="02611-138">Amostra uma textura.</span><span class="sxs-lookup"><span data-stu-id="02611-138">Samples a texture.</span></span>                                                                                                                                  |
| [<span data-ttu-id="02611-139">**SampleBias**</span><span class="sxs-lookup"><span data-stu-id="02611-139">**SampleBias**</span></span>](texture2d-samplebias.md)                              | <span data-ttu-id="02611-140">Amostra uma textura, depois de aplicar o valor de tendência ao nível de mipmap.</span><span class="sxs-lookup"><span data-stu-id="02611-140">Samples a texture, after applying the bias value to the mipmap level.</span></span>                                                                               |
| [<span data-ttu-id="02611-141">**SampleCmp**</span><span class="sxs-lookup"><span data-stu-id="02611-141">**SampleCmp**</span></span>](texture2d-samplecmp.md)                                | <span data-ttu-id="02611-142">Amostra uma textura, usando um valor de comparação para rejeitar amostras.</span><span class="sxs-lookup"><span data-stu-id="02611-142">Samples a texture, using a comparison value to reject samples.</span></span>                                                                                      |
| [<span data-ttu-id="02611-143">**SampleCmpLevelZero**</span><span class="sxs-lookup"><span data-stu-id="02611-143">**SampleCmpLevelZero**</span></span>](texture2d-samplecmplevelzero.md)              | <span data-ttu-id="02611-144">Amostras de uma textura (somente mipmap nível 0), usando um valor de comparação para rejeitar amostras.</span><span class="sxs-lookup"><span data-stu-id="02611-144">Samples a texture (mipmap level 0 only), using a comparison value to reject samples.</span></span>                                                                |
| [<span data-ttu-id="02611-145">**SampleGrad**</span><span class="sxs-lookup"><span data-stu-id="02611-145">**SampleGrad**</span></span>](texture2d-samplegrad.md)                              | <span data-ttu-id="02611-146">Amostra uma textura usando um gradiente para influenciar a maneira como o local de exemplo é calculado.</span><span class="sxs-lookup"><span data-stu-id="02611-146">Samples a texture using a gradient to influence the way the sample location is calculated.</span></span>                                                          |
| [<span data-ttu-id="02611-147">**SampleLevel**</span><span class="sxs-lookup"><span data-stu-id="02611-147">**SampleLevel**</span></span>](texture2d-samplelevel.md)                            | <span data-ttu-id="02611-148">Amostra uma textura no nível de mipmap especificado.</span><span class="sxs-lookup"><span data-stu-id="02611-148">Samples a texture on the specified mipmap level.</span></span>                                                                                                    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="02611-149">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="02611-149">Minimum Shader Model</span></span>

<span data-ttu-id="02611-150">Esse objeto tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="02611-150">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="02611-151">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="02611-151">Shader Model</span></span>                                                                | <span data-ttu-id="02611-152">Com suporte</span><span class="sxs-lookup"><span data-stu-id="02611-152">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="02611-153">[Modelo](d3d11-graphics-reference-sm5.md) de sombreador 5 e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="02611-153">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="02611-154">sim</span><span class="sxs-lookup"><span data-stu-id="02611-154">yes</span></span>       |



 

<span data-ttu-id="02611-155">Este objeto tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="02611-155">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="02611-156">Vértice</span><span class="sxs-lookup"><span data-stu-id="02611-156">Vertex</span></span> | <span data-ttu-id="02611-157">Envoltória</span><span class="sxs-lookup"><span data-stu-id="02611-157">Hull</span></span> | <span data-ttu-id="02611-158">Domínio</span><span class="sxs-lookup"><span data-stu-id="02611-158">Domain</span></span> | <span data-ttu-id="02611-159">Geometria</span><span class="sxs-lookup"><span data-stu-id="02611-159">Geometry</span></span> | <span data-ttu-id="02611-160">16x16</span><span class="sxs-lookup"><span data-stu-id="02611-160">Pixel</span></span> | <span data-ttu-id="02611-161">Computação</span><span class="sxs-lookup"><span data-stu-id="02611-161">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="02611-162">x</span><span class="sxs-lookup"><span data-stu-id="02611-162">x</span></span>      | <span data-ttu-id="02611-163">x</span><span class="sxs-lookup"><span data-stu-id="02611-163">x</span></span>    | <span data-ttu-id="02611-164">x</span><span class="sxs-lookup"><span data-stu-id="02611-164">x</span></span>      | <span data-ttu-id="02611-165">x</span><span class="sxs-lookup"><span data-stu-id="02611-165">x</span></span>        | <span data-ttu-id="02611-166">x</span><span class="sxs-lookup"><span data-stu-id="02611-166">x</span></span>     | <span data-ttu-id="02611-167">x</span><span class="sxs-lookup"><span data-stu-id="02611-167">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="02611-168">Confira também</span><span class="sxs-lookup"><span data-stu-id="02611-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02611-169">Objetos do Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="02611-169">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




