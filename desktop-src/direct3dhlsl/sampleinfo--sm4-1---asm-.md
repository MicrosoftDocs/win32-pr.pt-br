---
title: sampleinfo (SM 4.1-ASM)
description: Consulta o número de amostras em uma determinada exibição de recurso do sombreador ou no rasterizador.
ms.assetid: 1F0968D7-01E9-4213-9F83-172B88374C3C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d307dbc8c79618a6401737874a9f6e060a899ccc
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103823467"
---
# <a name="sampleinfo-sm41---asm"></a><span data-ttu-id="7142b-103">sampleinfo (SM 4.1-ASM)</span><span class="sxs-lookup"><span data-stu-id="7142b-103">sampleinfo (sm4.1 - asm)</span></span>

<span data-ttu-id="7142b-104">Consulta o número de amostras em uma determinada exibição de recurso do sombreador ou no rasterizador.</span><span class="sxs-lookup"><span data-stu-id="7142b-104">Queries the number of samples in a given shader resource view or in the rasterizer.</span></span>



| <span data-ttu-id="7142b-105">\[\_\]dest \[ . Mask \] , srcResource \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="7142b-105">\[\_uint\] dest\[.mask\], srcResource\[.swizzle\]</span></span> |
|---------------------------------------------------|



 



| <span data-ttu-id="7142b-106">Item</span><span class="sxs-lookup"><span data-stu-id="7142b-106">Item</span></span>                                                                                                               | <span data-ttu-id="7142b-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="7142b-107">Description</span></span>                                                    |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="7142b-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="7142b-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="7142b-109">\[no \] endereço dos resultados da operação.</span><span class="sxs-lookup"><span data-stu-id="7142b-109">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="7142b-110"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="7142b-110"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="7142b-111">\[no \] recurso do sombreador.</span><span class="sxs-lookup"><span data-stu-id="7142b-111">\[in\] The shader resource.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="7142b-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="7142b-112">Remarks</span></span>

<span data-ttu-id="7142b-113">Essa instrução retorna o número de amostras para o recurso fornecido ou o rasterizador.</span><span class="sxs-lookup"><span data-stu-id="7142b-113">This instruction returns the number of samples for the given resource or the rasterizer.</span></span> <span data-ttu-id="7142b-114">Ele é válido somente para recursos que podem ser carregados usando [**ld2dms**](ld2dms--sm4-1---asm-.md) , a menos que o rasterizador seja especificado como *srcResource*.</span><span class="sxs-lookup"><span data-stu-id="7142b-114">It is valid only for resources that can be loaded using [**ld2dms**](ld2dms--sm4-1---asm-.md) unless the rasterizer is specified as *srcResource*.</span></span> <span data-ttu-id="7142b-115">*srcResource* poderia ser um \# registro t (uma exibição de recurso do sombreador) ou um registro do rasterizador.</span><span class="sxs-lookup"><span data-stu-id="7142b-115">*srcResource* could be a t\# register (a shader resource view) or a rasterizer register.</span></span>

<span data-ttu-id="7142b-116">A instrução computa o vetor (SampleCount, 0, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="7142b-116">The instruction computes the vector (SampleCount,0,0,0).</span></span>

<span data-ttu-id="7142b-117">O swizzle no *srcResource* permite que os valores retornados sejam swizzled arbitrariamente antes de serem gravados no destino.</span><span class="sxs-lookup"><span data-stu-id="7142b-117">The swizzle on *srcResource* allows the returned values to be swizzled arbitrarily before they are written to the destination.</span></span> <span data-ttu-id="7142b-118">O valor retornado é ponto flutuante, a menos que o \_ modificador uint seja usado; nesse caso, o valor retornado é inteiro.</span><span class="sxs-lookup"><span data-stu-id="7142b-118">The returned value is floating point, unless the \_uint modifier is used, in which case the returned value is integer.</span></span> <span data-ttu-id="7142b-119">Se não houver nenhum recurso associado ao slot especificado, 0 será retornado.</span><span class="sxs-lookup"><span data-stu-id="7142b-119">If there is no resource bound to the specified slot, 0 is returned.</span></span>

<span data-ttu-id="7142b-120">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="7142b-120">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="7142b-121">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="7142b-121">Vertex Shader</span></span> | <span data-ttu-id="7142b-122">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="7142b-122">Geometry Shader</span></span> | <span data-ttu-id="7142b-123">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="7142b-123">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="7142b-124">X</span><span class="sxs-lookup"><span data-stu-id="7142b-124">X</span></span>             | <span data-ttu-id="7142b-125">X</span><span class="sxs-lookup"><span data-stu-id="7142b-125">X</span></span>               | <span data-ttu-id="7142b-126">x</span><span class="sxs-lookup"><span data-stu-id="7142b-126">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="7142b-127">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="7142b-127">Minimum Shader Model</span></span>

<span data-ttu-id="7142b-128">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="7142b-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="7142b-129">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="7142b-129">Shader Model</span></span>                                              | <span data-ttu-id="7142b-130">Com suporte</span><span class="sxs-lookup"><span data-stu-id="7142b-130">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="7142b-131">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="7142b-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="7142b-132">sim</span><span class="sxs-lookup"><span data-stu-id="7142b-132">yes</span></span>       |
| [<span data-ttu-id="7142b-133">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="7142b-133">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="7142b-134">sim</span><span class="sxs-lookup"><span data-stu-id="7142b-134">yes</span></span>       |
| [<span data-ttu-id="7142b-135">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="7142b-135">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="7142b-136">não</span><span class="sxs-lookup"><span data-stu-id="7142b-136">no</span></span>        |
| [<span data-ttu-id="7142b-137">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7142b-137">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="7142b-138">não</span><span class="sxs-lookup"><span data-stu-id="7142b-138">no</span></span>        |
| [<span data-ttu-id="7142b-139">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7142b-139">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="7142b-140">não</span><span class="sxs-lookup"><span data-stu-id="7142b-140">no</span></span>        |
| [<span data-ttu-id="7142b-141">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7142b-141">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="7142b-142">não</span><span class="sxs-lookup"><span data-stu-id="7142b-142">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="7142b-143">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7142b-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7142b-144">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7142b-144">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





