---
title: Texture3D
description: Texture3D
ms.assetid: a3640aac-b503-4716-8bc6-105e96bea03c
keywords:
- Texture3D HLSL
topic_type:
- apiref
api_name:
- Texture3D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 50b12f2184f6eca0fd7a68feb3e96d8d6fc65a61
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104006426"
---
# <a name="texture3d"></a><span data-ttu-id="fa43f-104">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fa43f-104">Texture3D</span></span>

<span data-ttu-id="fa43f-105">Tipo de Texture3D ([como ele existe no modelo de sombreador 4](dx-graphics-hlsl-to-type.md)) mais variáveis de recurso.</span><span class="sxs-lookup"><span data-stu-id="fa43f-105">Texture3D type ([as it exists in Shader Model 4](dx-graphics-hlsl-to-type.md)) plus resource variables.</span></span> <span data-ttu-id="fa43f-106">Esse objeto de textura dá suporte aos métodos a seguir, além dos métodos no sombreador modelo 4.</span><span class="sxs-lookup"><span data-stu-id="fa43f-106">This texture object supports the following methods in addition to the methods in Shader Model 4.</span></span>



| <span data-ttu-id="fa43f-107">Método</span><span class="sxs-lookup"><span data-stu-id="fa43f-107">Method</span></span>                                                                  | <span data-ttu-id="fa43f-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="fa43f-108">Description</span></span>                                                                                |
|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fa43f-109">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="fa43f-109">**GetDimensions**</span></span>](sm5-object-texture3d-getdimensions.md)             | <span data-ttu-id="fa43f-110">Obtém as dimensões do recurso.</span><span class="sxs-lookup"><span data-stu-id="fa43f-110">Gets the resource dimensions.</span></span>                                                              |
| [<span data-ttu-id="fa43f-111">**Carregamento**</span><span class="sxs-lookup"><span data-stu-id="fa43f-111">**Load**</span></span>](texture3d-load.md)                                          | <span data-ttu-id="fa43f-112">Lê dados de textura.</span><span class="sxs-lookup"><span data-stu-id="fa43f-112">Reads texture data.</span></span>                                                                        |
| <span data-ttu-id="fa43f-113">[**seqüencia. Operador\[\]\[\]**](sm5-object-texture3d-mipsoperatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="fa43f-113">[**mips.Operator\[\]\[\]**](sm5-object-texture3d-mipsoperatorindex.md)</span></span> | <span data-ttu-id="fa43f-114">Obtém uma variável de recurso somente leitura.</span><span class="sxs-lookup"><span data-stu-id="fa43f-114">Gets a read-only resource variable.</span></span>                                                        |
| <span data-ttu-id="fa43f-115">[**Operador\[\]**](sm5-object-texture3d-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="fa43f-115">[**Operator\[\]**](sm5-object-texture3d-operatorindex.md)</span></span>              | <span data-ttu-id="fa43f-116">Obtém uma variável de recurso somente leitura.</span><span class="sxs-lookup"><span data-stu-id="fa43f-116">Gets a read-only resource variable.</span></span>                                                        |
| [<span data-ttu-id="fa43f-117">**Nova**</span><span class="sxs-lookup"><span data-stu-id="fa43f-117">**Sample**</span></span>](texture3d-sample.md)                                      | <span data-ttu-id="fa43f-118">Amostra uma textura.</span><span class="sxs-lookup"><span data-stu-id="fa43f-118">Samples a texture.</span></span>                                                                         |
| [<span data-ttu-id="fa43f-119">**SampleBias**</span><span class="sxs-lookup"><span data-stu-id="fa43f-119">**SampleBias**</span></span>](texture3d-samplebias.md)                              | <span data-ttu-id="fa43f-120">Amostra uma textura, depois de aplicar o valor de tendência ao nível de mipmap.</span><span class="sxs-lookup"><span data-stu-id="fa43f-120">Samples a texture, after applying the bias value to the mipmap level.</span></span>                      |
| [<span data-ttu-id="fa43f-121">**SampleGrad**</span><span class="sxs-lookup"><span data-stu-id="fa43f-121">**SampleGrad**</span></span>](texture3d-samplegrad.md)                              | <span data-ttu-id="fa43f-122">Amostra uma textura usando um gradiente para influenciar a maneira como o local de exemplo é calculado.</span><span class="sxs-lookup"><span data-stu-id="fa43f-122">Samples a texture using a gradient to influence the way the sample location is calculated.</span></span> |
| [<span data-ttu-id="fa43f-123">**SampleLevel**</span><span class="sxs-lookup"><span data-stu-id="fa43f-123">**SampleLevel**</span></span>](texture3d-samplelevel.md)                            | <span data-ttu-id="fa43f-124">Amostra uma textura no nível de mipmap especificado.</span><span class="sxs-lookup"><span data-stu-id="fa43f-124">Samples a texture on the specified mipmap level.</span></span>                                           |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="fa43f-125">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="fa43f-125">Minimum Shader Model</span></span>

<span data-ttu-id="fa43f-126">Esse objeto tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="fa43f-126">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="fa43f-127">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="fa43f-127">Shader Model</span></span>                                                                | <span data-ttu-id="fa43f-128">Com suporte</span><span class="sxs-lookup"><span data-stu-id="fa43f-128">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="fa43f-129">[Modelo](d3d11-graphics-reference-sm5.md) de sombreador 5 e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="fa43f-129">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="fa43f-130">sim</span><span class="sxs-lookup"><span data-stu-id="fa43f-130">yes</span></span>       |



 

<span data-ttu-id="fa43f-131">Este objeto tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="fa43f-131">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="fa43f-132">Vértice</span><span class="sxs-lookup"><span data-stu-id="fa43f-132">Vertex</span></span> | <span data-ttu-id="fa43f-133">Envoltória</span><span class="sxs-lookup"><span data-stu-id="fa43f-133">Hull</span></span> | <span data-ttu-id="fa43f-134">Domínio</span><span class="sxs-lookup"><span data-stu-id="fa43f-134">Domain</span></span> | <span data-ttu-id="fa43f-135">Geometria</span><span class="sxs-lookup"><span data-stu-id="fa43f-135">Geometry</span></span> | <span data-ttu-id="fa43f-136">16x16</span><span class="sxs-lookup"><span data-stu-id="fa43f-136">Pixel</span></span> | <span data-ttu-id="fa43f-137">Computação</span><span class="sxs-lookup"><span data-stu-id="fa43f-137">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="fa43f-138">x</span><span class="sxs-lookup"><span data-stu-id="fa43f-138">x</span></span>      | <span data-ttu-id="fa43f-139">x</span><span class="sxs-lookup"><span data-stu-id="fa43f-139">x</span></span>    | <span data-ttu-id="fa43f-140">x</span><span class="sxs-lookup"><span data-stu-id="fa43f-140">x</span></span>      | <span data-ttu-id="fa43f-141">x</span><span class="sxs-lookup"><span data-stu-id="fa43f-141">x</span></span>        | <span data-ttu-id="fa43f-142">x</span><span class="sxs-lookup"><span data-stu-id="fa43f-142">x</span></span>     | <span data-ttu-id="fa43f-143">x</span><span class="sxs-lookup"><span data-stu-id="fa43f-143">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="fa43f-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="fa43f-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa43f-145">Objetos do Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="fa43f-145">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




