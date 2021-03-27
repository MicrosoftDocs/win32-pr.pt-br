---
title: Umad (sm4-ASM)
description: Número de multiplicação e adição de inteiro não assinado.
ms.assetid: C0BE31CA-E01D-42C0-A660-E63727CE344F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce52925622cb2f6f7cf53dec0e3f6f65d3fdcb58
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103638866"
---
# <a name="umad-sm4---asm"></a><span data-ttu-id="56a12-103">Umad (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="56a12-103">umad (sm4 - asm)</span></span>

<span data-ttu-id="56a12-104">Número de multiplicação e adição de inteiro não assinado.</span><span class="sxs-lookup"><span data-stu-id="56a12-104">Unsigned integer multiply and add.</span></span>



| <span data-ttu-id="56a12-105">Umad dest \[ . Mask \] , src0 \[ . swizzle \] , src1 \[ . swizzle \] , src2 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="56a12-105">umad dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\], src2\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------|



 



| <span data-ttu-id="56a12-106">Item</span><span class="sxs-lookup"><span data-stu-id="56a12-106">Item</span></span>                                                            | <span data-ttu-id="56a12-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="56a12-107">Description</span></span>                                                             |
|-----------------------------------------------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="56a12-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="56a12-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="56a12-109">\[no \] endereço do resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="56a12-109">\[in\] The address of the result of the operation.</span></span><br/>           |
| <span data-ttu-id="56a12-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="56a12-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="56a12-111">\[no \] valor para multiplicar com *src1*.</span><span class="sxs-lookup"><span data-stu-id="56a12-111">\[in\] The value to multiply with *src1*.</span></span><br/>                    |
| <span data-ttu-id="56a12-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="56a12-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="56a12-113">\[no \] valor para multiplicar com *src1*.</span><span class="sxs-lookup"><span data-stu-id="56a12-113">\[in\] The value to multiply with *src1*.</span></span><br/>                     |
| <span data-ttu-id="56a12-114"><span id="src2"></span><span id="SRC2"></span>*src2*</span><span class="sxs-lookup"><span data-stu-id="56a12-114"><span id="src2"></span><span id="SRC2"></span>*src2*</span></span><br/> | <span data-ttu-id="56a12-115">\[no \] valor a ser adicionado ao produto de *src0* e *src1*.</span><span class="sxs-lookup"><span data-stu-id="56a12-115">\[in\] The value to add to the product of *src0* and *src1*.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="56a12-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="56a12-116">Remarks</span></span>

<span data-ttu-id="56a12-117">Componente [umul](umul--sm4---asm-.md) de operandos de 32 bits *src0* e *src1* não assinados, mantendo os poucos 32 bits, por componente, do resultado.</span><span class="sxs-lookup"><span data-stu-id="56a12-117">Component-wise [umul](umul--sm4---asm-.md) of 32-bit operands *src0* and *src1* unsigned, keeping the low 32-bits, per component, of the result.</span></span> <span data-ttu-id="56a12-118">Em seguida, essa instrução executa um [IAdd](iadd--sm4---asm-.md) de *src2*, produzindo o resultado de baixa de 32 bits (por componente) correto.</span><span class="sxs-lookup"><span data-stu-id="56a12-118">This instruction then performs an [iadd](iadd--sm4---asm-.md) of *src2*, producing the correct low 32-bit (per component) result.</span></span> <span data-ttu-id="56a12-119">Os resultados de 32 bits são colocados no *dest*.</span><span class="sxs-lookup"><span data-stu-id="56a12-119">The 32-bit results are placed in *dest*.</span></span>

<span data-ttu-id="56a12-120">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="56a12-120">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="56a12-121">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="56a12-121">Vertex Shader</span></span> | <span data-ttu-id="56a12-122">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="56a12-122">Geometry Shader</span></span> | <span data-ttu-id="56a12-123">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="56a12-123">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="56a12-124">x</span><span class="sxs-lookup"><span data-stu-id="56a12-124">x</span></span>             | <span data-ttu-id="56a12-125">x</span><span class="sxs-lookup"><span data-stu-id="56a12-125">x</span></span>               | <span data-ttu-id="56a12-126">x</span><span class="sxs-lookup"><span data-stu-id="56a12-126">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="56a12-127">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="56a12-127">Minimum Shader Model</span></span>

<span data-ttu-id="56a12-128">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="56a12-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="56a12-129">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="56a12-129">Shader Model</span></span>                                              | <span data-ttu-id="56a12-130">Com suporte</span><span class="sxs-lookup"><span data-stu-id="56a12-130">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="56a12-131">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="56a12-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="56a12-132">sim</span><span class="sxs-lookup"><span data-stu-id="56a12-132">yes</span></span>       |
| [<span data-ttu-id="56a12-133">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="56a12-133">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="56a12-134">sim</span><span class="sxs-lookup"><span data-stu-id="56a12-134">yes</span></span>       |
| [<span data-ttu-id="56a12-135">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="56a12-135">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="56a12-136">sim</span><span class="sxs-lookup"><span data-stu-id="56a12-136">yes</span></span>       |
| [<span data-ttu-id="56a12-137">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="56a12-137">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="56a12-138">não</span><span class="sxs-lookup"><span data-stu-id="56a12-138">no</span></span>        |
| [<span data-ttu-id="56a12-139">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="56a12-139">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="56a12-140">não</span><span class="sxs-lookup"><span data-stu-id="56a12-140">no</span></span>        |
| [<span data-ttu-id="56a12-141">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="56a12-141">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="56a12-142">não</span><span class="sxs-lookup"><span data-stu-id="56a12-142">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="56a12-143">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="56a12-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56a12-144">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="56a12-144">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





