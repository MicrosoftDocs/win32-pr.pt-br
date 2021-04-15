---
title: Imad (sm4-ASM)
description: Número inteiro de multiplicação e adição de inteiros assinados.
ms.assetid: 1C24AF49-AA32-4D3A-8478-C9BAC4FE7D77
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90db4cb0a36b0d3951e8b0490bb3ca08db8d5354
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104988559"
---
# <a name="imad-sm4---asm"></a><span data-ttu-id="42138-103">Imad (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="42138-103">imad (sm4 - asm)</span></span>

<span data-ttu-id="42138-104">Número inteiro de multiplicação e adição de inteiros assinados.</span><span class="sxs-lookup"><span data-stu-id="42138-104">Signed integer multiply and add.</span></span>



| <span data-ttu-id="42138-105">Imad dest \[ . Mask \] , \[ - \] src0 \[ . swizzle \] , \[ - \] src1 \[ . swizzle \] , \[ - \] src2 \[ . swizzle</span><span class="sxs-lookup"><span data-stu-id="42138-105">imad dest\[.mask\], \[-\]src0\[.swizzle\], \[-\]src1\[.swizzle\], \[-\]src2\[.swizzle</span></span> |
|---------------------------------------------------------------------------------------|



 



| <span data-ttu-id="42138-106">Item</span><span class="sxs-lookup"><span data-stu-id="42138-106">Item</span></span>                                                            | <span data-ttu-id="42138-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="42138-107">Description</span></span>                                                         |
|-----------------------------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="42138-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="42138-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="42138-109">\[no \] resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="42138-109">\[in\] The result of the operation.</span></span><br/>                      |
| <span data-ttu-id="42138-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="42138-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="42138-111">\[em \] valor para multiplicar com *src1*.</span><span class="sxs-lookup"><span data-stu-id="42138-111">\[in\] Value to multiply with *src1*.</span></span><br/>                    |
| <span data-ttu-id="42138-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="42138-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="42138-113">\[em \] valor para multiplicar com *src0*.</span><span class="sxs-lookup"><span data-stu-id="42138-113">\[in\] Value to multiply with *src0*.</span></span><br/>                    |
| <span data-ttu-id="42138-114"><span id="src2"></span><span id="SRC2"></span>*src2*</span><span class="sxs-lookup"><span data-stu-id="42138-114"><span id="src2"></span><span id="SRC2"></span>*src2*</span></span><br/> | <span data-ttu-id="42138-115">\[em \] valor para adicionar ao produto de *src0* e *src1*.</span><span class="sxs-lookup"><span data-stu-id="42138-115">\[in\] Value to add to the product of *src0* and *src1*.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="42138-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="42138-116">Remarks</span></span>

<span data-ttu-id="42138-117">Componente [imul](imul--sm4---asm-.md) de operandos de 32 bits *src0* e *src1* (assinados), mantendo os poucos 32 bits (por componente) do resultado, seguido por um [IAdd](iadd--sm4---asm-.md) de *src2*, produzindo o resultado de 32 bits (por componente) correto.</span><span class="sxs-lookup"><span data-stu-id="42138-117">Component-wise [imul](imul--sm4---asm-.md) of 32-bit operands *src0* and *src1* (signed), keeping low 32-bits (per component) of the result, followed by an [iadd](iadd--sm4---asm-.md) of *src2*, producing the correct low 32-bit (per component) result.</span></span> <span data-ttu-id="42138-118">Os resultados de 32 bits são colocados no *dest*.</span><span class="sxs-lookup"><span data-stu-id="42138-118">The 32-bit results are placed in *dest*.</span></span>

<span data-ttu-id="42138-119">O modificador opcional Negate nos operandos de origem usa o complemento de 2 antes de executar a operação aritmética.</span><span class="sxs-lookup"><span data-stu-id="42138-119">Optional negate modifier on source operands takes 2's complement before performing arithmetic operation.</span></span>

<span data-ttu-id="42138-120">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="42138-120">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="42138-121">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="42138-121">Vertex Shader</span></span> | <span data-ttu-id="42138-122">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="42138-122">Geometry Shader</span></span> | <span data-ttu-id="42138-123">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="42138-123">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="42138-124">x</span><span class="sxs-lookup"><span data-stu-id="42138-124">x</span></span>             | <span data-ttu-id="42138-125">x</span><span class="sxs-lookup"><span data-stu-id="42138-125">x</span></span>               | <span data-ttu-id="42138-126">x</span><span class="sxs-lookup"><span data-stu-id="42138-126">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="42138-127">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="42138-127">Minimum Shader Model</span></span>

<span data-ttu-id="42138-128">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="42138-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="42138-129">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="42138-129">Shader Model</span></span>                                              | <span data-ttu-id="42138-130">Com suporte</span><span class="sxs-lookup"><span data-stu-id="42138-130">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="42138-131">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="42138-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="42138-132">sim</span><span class="sxs-lookup"><span data-stu-id="42138-132">yes</span></span>       |
| [<span data-ttu-id="42138-133">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="42138-133">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="42138-134">sim</span><span class="sxs-lookup"><span data-stu-id="42138-134">yes</span></span>       |
| [<span data-ttu-id="42138-135">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="42138-135">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="42138-136">sim</span><span class="sxs-lookup"><span data-stu-id="42138-136">yes</span></span>       |
| [<span data-ttu-id="42138-137">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="42138-137">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="42138-138">não</span><span class="sxs-lookup"><span data-stu-id="42138-138">no</span></span>        |
| [<span data-ttu-id="42138-139">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="42138-139">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="42138-140">não</span><span class="sxs-lookup"><span data-stu-id="42138-140">no</span></span>        |
| [<span data-ttu-id="42138-141">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="42138-141">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="42138-142">não</span><span class="sxs-lookup"><span data-stu-id="42138-142">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="42138-143">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="42138-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="42138-144">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="42138-144">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





