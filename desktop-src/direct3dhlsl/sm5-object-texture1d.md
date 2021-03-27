---
title: Texture1D
description: Texture1D
ms.assetid: 5f6fd0e4-a73e-4d13-b3a0-c884b7912581
keywords:
- Texture1D HLSL
topic_type:
- apiref
api_name:
- Texture1D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8b8a60706ea2752109cdda9907ffe7c654efe531
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103916801"
---
# <a name="texture1d"></a><span data-ttu-id="4cdaf-104">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4cdaf-104">Texture1D</span></span>

<span data-ttu-id="4cdaf-105">Um tipo de textura 1D ([como ele existe no modelo de sombreador 4](dx-graphics-hlsl-to-type.md)) Além de variáveis de recurso.</span><span class="sxs-lookup"><span data-stu-id="4cdaf-105">A 1D texture type ([as it exists in Shader Model 4](dx-graphics-hlsl-to-type.md)) plus resource variables.</span></span> <span data-ttu-id="4cdaf-106">Esse objeto de textura dá suporte aos métodos a seguir, além dos métodos no sombreador modelo 4.</span><span class="sxs-lookup"><span data-stu-id="4cdaf-106">This texture object supports the following methods in addition to the methods in Shader Model 4.</span></span>



| <span data-ttu-id="4cdaf-107">Método</span><span class="sxs-lookup"><span data-stu-id="4cdaf-107">Method</span></span>                                                                  | <span data-ttu-id="4cdaf-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="4cdaf-108">Description</span></span>                                                                                |
|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4cdaf-109">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="4cdaf-109">**GetDimensions**</span></span>](sm5-object-texture1d-getdimensions.md)             | <span data-ttu-id="4cdaf-110">Obtém as dimensões do recurso.</span><span class="sxs-lookup"><span data-stu-id="4cdaf-110">Gets the resource dimensions.</span></span>                                                              |
| [<span data-ttu-id="4cdaf-111">**Carregamento**</span><span class="sxs-lookup"><span data-stu-id="4cdaf-111">**Load**</span></span>](texture1d-load.md)                                          | <span data-ttu-id="4cdaf-112">Lê dados de textura.</span><span class="sxs-lookup"><span data-stu-id="4cdaf-112">Reads texture data.</span></span>                                                                        |
| <span data-ttu-id="4cdaf-113">[**Operador\[\]**](sm5-object-texture1d-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="4cdaf-113">[**Operator\[\]**](sm5-object-texture1d-operatorindex.md)</span></span>              | <span data-ttu-id="4cdaf-114">Obtém uma variável de recurso somente leitura.</span><span class="sxs-lookup"><span data-stu-id="4cdaf-114">Gets a read-only resource variable.</span></span>                                                        |
| <span data-ttu-id="4cdaf-115">[**seqüencia. Operador\[\]\[\]**](sm5-object-texture1d-mipsoperatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="4cdaf-115">[**mips.Operator\[\]\[\]**](sm5-object-texture1d-mipsoperatorindex.md)</span></span> | <span data-ttu-id="4cdaf-116">Obtém uma variável de recurso somente leitura.</span><span class="sxs-lookup"><span data-stu-id="4cdaf-116">Gets a read-only resource variable.</span></span>                                                        |
| [<span data-ttu-id="4cdaf-117">**Nova**</span><span class="sxs-lookup"><span data-stu-id="4cdaf-117">**Sample**</span></span>](texture1d-sample.md)                                      | <span data-ttu-id="4cdaf-118">Amostra uma textura.</span><span class="sxs-lookup"><span data-stu-id="4cdaf-118">Samples a texture.</span></span>                                                                         |
| [<span data-ttu-id="4cdaf-119">**SampleBias**</span><span class="sxs-lookup"><span data-stu-id="4cdaf-119">**SampleBias**</span></span>](texture1d-samplebias.md)                              | <span data-ttu-id="4cdaf-120">Amostra uma textura, depois de aplicar o valor de tendência ao nível de mipmap.</span><span class="sxs-lookup"><span data-stu-id="4cdaf-120">Samples a texture, after applying the bias value to the mipmap level.</span></span>                      |
| [<span data-ttu-id="4cdaf-121">**SampleCmp**</span><span class="sxs-lookup"><span data-stu-id="4cdaf-121">**SampleCmp**</span></span>](texture1d-samplecmp.md)                                | <span data-ttu-id="4cdaf-122">Amostra uma textura, usando um valor de comparação para rejeitar amostras.</span><span class="sxs-lookup"><span data-stu-id="4cdaf-122">Samples a texture, using a comparison value to reject samples.</span></span>                             |
| [<span data-ttu-id="4cdaf-123">**SampleCmpLevelZero**</span><span class="sxs-lookup"><span data-stu-id="4cdaf-123">**SampleCmpLevelZero**</span></span>](texture1d-samplecmplevelzero.md)              | <span data-ttu-id="4cdaf-124">Amostras de uma textura (somente mipmap nível 0), usando um valor de comparação para rejeitar amostras.</span><span class="sxs-lookup"><span data-stu-id="4cdaf-124">Samples a texture (mipmap level 0 only), using a comparison value to reject samples.</span></span>       |
| [<span data-ttu-id="4cdaf-125">**SampleGrad**</span><span class="sxs-lookup"><span data-stu-id="4cdaf-125">**SampleGrad**</span></span>](texture1d-samplegrad.md)                              | <span data-ttu-id="4cdaf-126">Amostra uma textura usando um gradiente para influenciar a maneira como o local de exemplo é calculado.</span><span class="sxs-lookup"><span data-stu-id="4cdaf-126">Samples a texture using a gradient to influence the way the sample location is calculated.</span></span> |
| [<span data-ttu-id="4cdaf-127">**SampleLevel**</span><span class="sxs-lookup"><span data-stu-id="4cdaf-127">**SampleLevel**</span></span>](texture1d-samplelevel.md)                            | <span data-ttu-id="4cdaf-128">Amostra uma textura no nível de mipmap especificado.</span><span class="sxs-lookup"><span data-stu-id="4cdaf-128">Samples a texture on the specified mipmap level.</span></span>                                           |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="4cdaf-129">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="4cdaf-129">Minimum Shader Model</span></span>

<span data-ttu-id="4cdaf-130">Esse objeto tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="4cdaf-130">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="4cdaf-131">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="4cdaf-131">Shader Model</span></span>                                                                | <span data-ttu-id="4cdaf-132">Com suporte</span><span class="sxs-lookup"><span data-stu-id="4cdaf-132">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="4cdaf-133">[Modelo](d3d11-graphics-reference-sm5.md) de sombreador 5 e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="4cdaf-133">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="4cdaf-134">sim</span><span class="sxs-lookup"><span data-stu-id="4cdaf-134">yes</span></span>       |



 

<span data-ttu-id="4cdaf-135">Este objeto tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="4cdaf-135">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="4cdaf-136">Vértice</span><span class="sxs-lookup"><span data-stu-id="4cdaf-136">Vertex</span></span> | <span data-ttu-id="4cdaf-137">Envoltória</span><span class="sxs-lookup"><span data-stu-id="4cdaf-137">Hull</span></span> | <span data-ttu-id="4cdaf-138">Domínio</span><span class="sxs-lookup"><span data-stu-id="4cdaf-138">Domain</span></span> | <span data-ttu-id="4cdaf-139">Geometria</span><span class="sxs-lookup"><span data-stu-id="4cdaf-139">Geometry</span></span> | <span data-ttu-id="4cdaf-140">16x16</span><span class="sxs-lookup"><span data-stu-id="4cdaf-140">Pixel</span></span> | <span data-ttu-id="4cdaf-141">Computação</span><span class="sxs-lookup"><span data-stu-id="4cdaf-141">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="4cdaf-142">x</span><span class="sxs-lookup"><span data-stu-id="4cdaf-142">x</span></span>      | <span data-ttu-id="4cdaf-143">x</span><span class="sxs-lookup"><span data-stu-id="4cdaf-143">x</span></span>    | <span data-ttu-id="4cdaf-144">x</span><span class="sxs-lookup"><span data-stu-id="4cdaf-144">x</span></span>      | <span data-ttu-id="4cdaf-145">x</span><span class="sxs-lookup"><span data-stu-id="4cdaf-145">x</span></span>        | <span data-ttu-id="4cdaf-146">x</span><span class="sxs-lookup"><span data-stu-id="4cdaf-146">x</span></span>     | <span data-ttu-id="4cdaf-147">x</span><span class="sxs-lookup"><span data-stu-id="4cdaf-147">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="4cdaf-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="4cdaf-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cdaf-149">Objetos do Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="4cdaf-149">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




