---
title: samplepos (SM 4.1-ASM)
description: Consulta a posição de um exemplo em uma determinada exibição de recurso do sombreador ou no rasterizador.
ms.assetid: 5A53B342-3A1D-4016-ABF2-CA6236D562C9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 910a542dafddb8b855e218f8702c746220780d6e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104365276"
---
# <a name="samplepos-sm41---asm"></a><span data-ttu-id="d8e33-103">samplepos (SM 4.1-ASM)</span><span class="sxs-lookup"><span data-stu-id="d8e33-103">samplepos (sm4.1 - asm)</span></span>

<span data-ttu-id="d8e33-104">Consulta a posição de um exemplo em uma determinada exibição de recurso do sombreador ou no rasterizador.</span><span class="sxs-lookup"><span data-stu-id="d8e33-104">Queries the position of a sample in a given shader resource view or in the rasterizer.</span></span>



| <span data-ttu-id="d8e33-105">samplepos dest \[ . Mask \] , srcResource \[ . swizzle \] , sampleIndex (operando escalar)</span><span class="sxs-lookup"><span data-stu-id="d8e33-105">samplepos dest\[.mask\], srcResource\[.swizzle\], sampleIndex (scalar operand)</span></span> |
|--------------------------------------------------------------------------------|



 



| <span data-ttu-id="d8e33-106">Item</span><span class="sxs-lookup"><span data-stu-id="d8e33-106">Item</span></span>                                                                                                               | <span data-ttu-id="d8e33-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="d8e33-107">Description</span></span>                                                    |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="d8e33-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="d8e33-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="d8e33-109">\[no \] endereço dos resultados da operação.</span><span class="sxs-lookup"><span data-stu-id="d8e33-109">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="d8e33-110"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="d8e33-110"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="d8e33-111">\[no \] recurso do sombreador.</span><span class="sxs-lookup"><span data-stu-id="d8e33-111">\[in\] The shader resource.</span></span><br/>                         |
| <span data-ttu-id="d8e33-112"><span id="sampleIndex"></span><span id="sampleindex"></span><span id="SAMPLEINDEX"></span>*sampleIndex*</span><span class="sxs-lookup"><span data-stu-id="d8e33-112"><span id="sampleIndex"></span><span id="sampleindex"></span><span id="SAMPLEINDEX"></span>*sampleIndex*</span></span><br/> | <span data-ttu-id="d8e33-113">\[no \] índice do exemplo.</span><span class="sxs-lookup"><span data-stu-id="d8e33-113">\[in\] The index of the sample.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="d8e33-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="d8e33-114">Remarks</span></span>

<span data-ttu-id="d8e33-115">Essa instrução retorna a posição de exemplo 2D de *sampleIndex* de exemplo para o recurso fornecido.</span><span class="sxs-lookup"><span data-stu-id="d8e33-115">This instruction returns the 2D sample position of sample *sampleIndex* for the given resource.</span></span> <span data-ttu-id="d8e33-116">Ele é válido somente para recursos que podem ser carregados usando [**ld2dms**](ld2dms--sm4-1---asm-.md) , a menos que o rasterizador seja especificado como *srcResource*.</span><span class="sxs-lookup"><span data-stu-id="d8e33-116">It is valid only for resources that can be loaded using [**ld2dms**](ld2dms--sm4-1---asm-.md) unless the rasterizer is specified as *srcResource*.</span></span>

<span data-ttu-id="d8e33-117">*srcResource* pode ser um \# registro t (uma exibição de recurso do sombreador) ou um registro do rasterizador.</span><span class="sxs-lookup"><span data-stu-id="d8e33-117">*srcResource* can be a t\# register (a shader resource view) or a rasterizer register.</span></span>

<span data-ttu-id="d8e33-118">A instrução computa o vetor de ponto flutuante (XPosition, YPosition, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="d8e33-118">The instruction computes the floating point vector (Xposition, Yposition, 0, 0).</span></span>

<span data-ttu-id="d8e33-119">O swizzle no *srcResource* permite que os valores retornados sejam swizzled arbitrariamente antes de serem gravados no destino.</span><span class="sxs-lookup"><span data-stu-id="d8e33-119">The swizzle on *srcResource* allows the returned values to be swizzled arbitrarily before they are written to the destination.</span></span> <span data-ttu-id="d8e33-120">A posição de exemplo é relativa ao centro do pixel, com base no sistema de coordenadas de pixels.</span><span class="sxs-lookup"><span data-stu-id="d8e33-120">The sample position is relative to the pixel's center, based on the Pixel Coordinate System.</span></span>

<span data-ttu-id="d8e33-121">Se *sampleIndex* estiver fora dos limites, um vetor zero será retornado.</span><span class="sxs-lookup"><span data-stu-id="d8e33-121">If *sampleIndex* is out of bounds a zero vector is returned.</span></span> <span data-ttu-id="d8e33-122">Se não houver nenhum recurso associado ao slot especificado, 0 será retornado.</span><span class="sxs-lookup"><span data-stu-id="d8e33-122">If there is no resource bound to the specified slot, 0 is returned.</span></span>

<span data-ttu-id="d8e33-123">**samplepos** pode ser usado para coisas como resolvedores personalizados no código do sombreador.</span><span class="sxs-lookup"><span data-stu-id="d8e33-123">**samplepos** can be used for things like custom resolves in shader code.</span></span>

<span data-ttu-id="d8e33-124">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="d8e33-124">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="d8e33-125">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="d8e33-125">Vertex Shader</span></span> | <span data-ttu-id="d8e33-126">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="d8e33-126">Geometry Shader</span></span> | <span data-ttu-id="d8e33-127">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="d8e33-127">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               |                 | <span data-ttu-id="d8e33-128">x</span><span class="sxs-lookup"><span data-stu-id="d8e33-128">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d8e33-129">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="d8e33-129">Minimum Shader Model</span></span>

<span data-ttu-id="d8e33-130">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="d8e33-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="d8e33-131">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="d8e33-131">Shader Model</span></span>                                              | <span data-ttu-id="d8e33-132">Com suporte</span><span class="sxs-lookup"><span data-stu-id="d8e33-132">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="d8e33-133">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="d8e33-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="d8e33-134">sim</span><span class="sxs-lookup"><span data-stu-id="d8e33-134">yes</span></span>       |
| [<span data-ttu-id="d8e33-135">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="d8e33-135">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="d8e33-136">sim</span><span class="sxs-lookup"><span data-stu-id="d8e33-136">yes</span></span>       |
| [<span data-ttu-id="d8e33-137">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="d8e33-137">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="d8e33-138">não</span><span class="sxs-lookup"><span data-stu-id="d8e33-138">no</span></span>        |
| [<span data-ttu-id="d8e33-139">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d8e33-139">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="d8e33-140">não</span><span class="sxs-lookup"><span data-stu-id="d8e33-140">no</span></span>        |
| [<span data-ttu-id="d8e33-141">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d8e33-141">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="d8e33-142">não</span><span class="sxs-lookup"><span data-stu-id="d8e33-142">no</span></span>        |
| [<span data-ttu-id="d8e33-143">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d8e33-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="d8e33-144">não</span><span class="sxs-lookup"><span data-stu-id="d8e33-144">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="d8e33-145">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d8e33-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d8e33-146">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d8e33-146">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





