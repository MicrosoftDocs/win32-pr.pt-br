---
title: Texture1DArray
description: Texture1DArray
ms.assetid: 3d793423-3d79-48c1-aa78-f9d93b79e0b6
keywords:
- Texture1DArray HLSL
topic_type:
- apiref
api_name:
- Texture1DArray
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 39cea5692e29ead74ba20c4a35ab8d43a1b19d42
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104006656"
---
# <a name="texture1darray"></a><span data-ttu-id="b2af5-104">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="b2af5-104">Texture1DArray</span></span>

<span data-ttu-id="b2af5-105">Tipo de Texture1DArray ([como ele existe no modelo de sombreador 4](dx-graphics-hlsl-to-type.md)) mais variáveis de recurso.</span><span class="sxs-lookup"><span data-stu-id="b2af5-105">Texture1DArray type ([as it exists in Shader Model 4](dx-graphics-hlsl-to-type.md)) plus resource variables.</span></span> <span data-ttu-id="b2af5-106">Esse objeto de textura dá suporte aos métodos a seguir, além dos métodos no sombreador modelo 4.</span><span class="sxs-lookup"><span data-stu-id="b2af5-106">This texture object supports the following methods in addition to the methods in Shader Model 4.</span></span>



| <span data-ttu-id="b2af5-107">Método</span><span class="sxs-lookup"><span data-stu-id="b2af5-107">Method</span></span>                                                                       | <span data-ttu-id="b2af5-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="b2af5-108">Description</span></span>                                                                                |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b2af5-109">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="b2af5-109">**GetDimensions**</span></span>](sm5-object-texture1darray-getdimensions.md)             | <span data-ttu-id="b2af5-110">Obtém as dimensões do recurso.</span><span class="sxs-lookup"><span data-stu-id="b2af5-110">Gets the resource dimensions.</span></span>                                                              |
| [<span data-ttu-id="b2af5-111">**Carregamento**</span><span class="sxs-lookup"><span data-stu-id="b2af5-111">**Load**</span></span>](texture1darray-load.md)                                          | <span data-ttu-id="b2af5-112">Lê dados de textura.</span><span class="sxs-lookup"><span data-stu-id="b2af5-112">Reads texture data.</span></span>                                                                        |
| <span data-ttu-id="b2af5-113">[**seqüencia. Operador\[\]\[\]**](sm5-object-texture1darray-mipsoperatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="b2af5-113">[**mips.Operator\[\]\[\]**](sm5-object-texture1darray-mipsoperatorindex.md)</span></span> | <span data-ttu-id="b2af5-114">Obtém uma variável de recurso somente leitura.</span><span class="sxs-lookup"><span data-stu-id="b2af5-114">Gets a read-only resource variable.</span></span>                                                        |
| <span data-ttu-id="b2af5-115">[**Operador\[\]**](sm5-object-texture1darray-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="b2af5-115">[**Operator\[\]**](sm5-object-texture1darray-operatorindex.md)</span></span>              | <span data-ttu-id="b2af5-116">Obtém uma variável de recurso somente leitura.</span><span class="sxs-lookup"><span data-stu-id="b2af5-116">Gets a read-only resource variable.</span></span>                                                        |
| [<span data-ttu-id="b2af5-117">**Nova**</span><span class="sxs-lookup"><span data-stu-id="b2af5-117">**Sample**</span></span>](texture1darray-sample.md)                                      | <span data-ttu-id="b2af5-118">Amostra uma textura.</span><span class="sxs-lookup"><span data-stu-id="b2af5-118">Samples a texture.</span></span>                                                                         |
| [<span data-ttu-id="b2af5-119">**SampleBias**</span><span class="sxs-lookup"><span data-stu-id="b2af5-119">**SampleBias**</span></span>](texture1darray-samplebias.md)                              | <span data-ttu-id="b2af5-120">Amostra uma textura, depois de aplicar o valor de tendência ao nível de mipmap.</span><span class="sxs-lookup"><span data-stu-id="b2af5-120">Samples a texture, after applying the bias value to the mipmap level.</span></span>                      |
| [<span data-ttu-id="b2af5-121">**SampleCmp**</span><span class="sxs-lookup"><span data-stu-id="b2af5-121">**SampleCmp**</span></span>](texture1darray-samplecmp.md)                                | <span data-ttu-id="b2af5-122">Amostra uma textura, usando um valor de comparação para rejeitar amostras.</span><span class="sxs-lookup"><span data-stu-id="b2af5-122">Samples a texture, using a comparison value to reject samples.</span></span>                             |
| [<span data-ttu-id="b2af5-123">**SampleCmpLevelZero**</span><span class="sxs-lookup"><span data-stu-id="b2af5-123">**SampleCmpLevelZero**</span></span>](texture1darray-samplecmplevelzero.md)              | <span data-ttu-id="b2af5-124">Amostras de uma textura (somente mipmap nível 0), usando um valor de comparação para rejeitar amostras.</span><span class="sxs-lookup"><span data-stu-id="b2af5-124">Samples a texture (mipmap level 0 only), using a comparison value to reject samples.</span></span>       |
| [<span data-ttu-id="b2af5-125">**SampleGrad**</span><span class="sxs-lookup"><span data-stu-id="b2af5-125">**SampleGrad**</span></span>](texture1darray-samplegrad.md)                              | <span data-ttu-id="b2af5-126">Amostra uma textura usando um gradiente para influenciar a maneira como o local de exemplo é calculado.</span><span class="sxs-lookup"><span data-stu-id="b2af5-126">Samples a texture using a gradient to influence the way the sample location is calculated.</span></span> |
| [<span data-ttu-id="b2af5-127">**SampleLevel**</span><span class="sxs-lookup"><span data-stu-id="b2af5-127">**SampleLevel**</span></span>](texture1darray-samplelevel.md)                            | <span data-ttu-id="b2af5-128">Amostra uma textura no nível de mipmap especificado.</span><span class="sxs-lookup"><span data-stu-id="b2af5-128">Samples a texture on the specified mipmap level.</span></span>                                           |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="b2af5-129">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="b2af5-129">Minimum Shader Model</span></span>

<span data-ttu-id="b2af5-130">Esse objeto tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="b2af5-130">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="b2af5-131">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="b2af5-131">Shader Model</span></span>                                                                | <span data-ttu-id="b2af5-132">Com suporte</span><span class="sxs-lookup"><span data-stu-id="b2af5-132">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="b2af5-133">[Modelo](d3d11-graphics-reference-sm5.md) de sombreador 5 e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="b2af5-133">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="b2af5-134">sim</span><span class="sxs-lookup"><span data-stu-id="b2af5-134">yes</span></span>       |



 

<span data-ttu-id="b2af5-135">Este objeto tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="b2af5-135">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="b2af5-136">Vértice</span><span class="sxs-lookup"><span data-stu-id="b2af5-136">Vertex</span></span> | <span data-ttu-id="b2af5-137">Envoltória</span><span class="sxs-lookup"><span data-stu-id="b2af5-137">Hull</span></span> | <span data-ttu-id="b2af5-138">Domínio</span><span class="sxs-lookup"><span data-stu-id="b2af5-138">Domain</span></span> | <span data-ttu-id="b2af5-139">Geometria</span><span class="sxs-lookup"><span data-stu-id="b2af5-139">Geometry</span></span> | <span data-ttu-id="b2af5-140">16x16</span><span class="sxs-lookup"><span data-stu-id="b2af5-140">Pixel</span></span> | <span data-ttu-id="b2af5-141">Computação</span><span class="sxs-lookup"><span data-stu-id="b2af5-141">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="b2af5-142">x</span><span class="sxs-lookup"><span data-stu-id="b2af5-142">x</span></span>      | <span data-ttu-id="b2af5-143">x</span><span class="sxs-lookup"><span data-stu-id="b2af5-143">x</span></span>    | <span data-ttu-id="b2af5-144">x</span><span class="sxs-lookup"><span data-stu-id="b2af5-144">x</span></span>      | <span data-ttu-id="b2af5-145">x</span><span class="sxs-lookup"><span data-stu-id="b2af5-145">x</span></span>        | <span data-ttu-id="b2af5-146">x</span><span class="sxs-lookup"><span data-stu-id="b2af5-146">x</span></span>     | <span data-ttu-id="b2af5-147">x</span><span class="sxs-lookup"><span data-stu-id="b2af5-147">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="b2af5-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="b2af5-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2af5-149">Objetos do Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="b2af5-149">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




