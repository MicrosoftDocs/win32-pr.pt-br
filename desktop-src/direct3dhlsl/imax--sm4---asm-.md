---
title: IMAX (sm4-ASM)
description: Inteiro de componente-Wise.
ms.assetid: 005468AA-577E-441F-ACD5-37A691E62CDD
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc1bc6311573b1e7b39fbeaa93904203e7aae2ae
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104084255"
---
# <a name="imax-sm4---asm"></a><span data-ttu-id="33e66-103">IMAX (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="33e66-103">imax (sm4 - asm)</span></span>

<span data-ttu-id="33e66-104">Inteiro de componente-Wise.</span><span class="sxs-lookup"><span data-stu-id="33e66-104">Component-wise integer maximum.</span></span>



| <span data-ttu-id="33e66-105">IMAX dest \[ . Mask \] , \[  - \] src0 \[ . swizzle \] , \[ - \] src1 \[ . swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="33e66-105">imax dest\[.mask\], \[ -\]src0\[.swizzle\], \[-\]src1\[.swizzle\],</span></span> |
|--------------------------------------------------------------------|



 



| <span data-ttu-id="33e66-106">Item</span><span class="sxs-lookup"><span data-stu-id="33e66-106">Item</span></span>                                                            | <span data-ttu-id="33e66-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="33e66-107">Description</span></span>                                                                                             |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33e66-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="33e66-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="33e66-109">\[no \] resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="33e66-109">\[in\] The result of the operation.</span></span><br/> <span data-ttu-id="33e66-110">*dest*  =  *src0*  >  *src1* ?</span><span class="sxs-lookup"><span data-stu-id="33e66-110">*dest* = *src0* > *src1* ?</span></span> <span data-ttu-id="33e66-111">*src0* : *src1*</span><span class="sxs-lookup"><span data-stu-id="33e66-111">*src0* : *src1*</span></span><br/> |
| <span data-ttu-id="33e66-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="33e66-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="33e66-113">\[no \] valor a ser comparado com *src1*.</span><span class="sxs-lookup"><span data-stu-id="33e66-113">\[in\] The value to compare to *src1*.</span></span><br/>                                                       |
| <span data-ttu-id="33e66-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="33e66-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="33e66-115">\[no \] valor a ser comparado com *src0*.</span><span class="sxs-lookup"><span data-stu-id="33e66-115">\[in\] The value to compare to *src0*.</span></span><br/>                                                       |



 

## <a name="remarks"></a><span data-ttu-id="33e66-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="33e66-116">Remarks</span></span>

<span data-ttu-id="33e66-117">O modificador opcional Negate nos operandos de origem usa o complemento de 2 antes de executar a operação.</span><span class="sxs-lookup"><span data-stu-id="33e66-117">Optional negate modifier on source operands takes 2's complement before performing operation.</span></span>

<span data-ttu-id="33e66-118">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="33e66-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="33e66-119">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="33e66-119">Vertex Shader</span></span> | <span data-ttu-id="33e66-120">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="33e66-120">Geometry Shader</span></span> | <span data-ttu-id="33e66-121">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="33e66-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="33e66-122">x</span><span class="sxs-lookup"><span data-stu-id="33e66-122">x</span></span>             | <span data-ttu-id="33e66-123">x</span><span class="sxs-lookup"><span data-stu-id="33e66-123">x</span></span>               | <span data-ttu-id="33e66-124">x</span><span class="sxs-lookup"><span data-stu-id="33e66-124">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="33e66-125">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="33e66-125">Minimum Shader Model</span></span>

<span data-ttu-id="33e66-126">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="33e66-126">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="33e66-127">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="33e66-127">Shader Model</span></span>                                              | <span data-ttu-id="33e66-128">Com suporte</span><span class="sxs-lookup"><span data-stu-id="33e66-128">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="33e66-129">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="33e66-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="33e66-130">sim</span><span class="sxs-lookup"><span data-stu-id="33e66-130">yes</span></span>       |
| [<span data-ttu-id="33e66-131">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="33e66-131">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="33e66-132">sim</span><span class="sxs-lookup"><span data-stu-id="33e66-132">yes</span></span>       |
| [<span data-ttu-id="33e66-133">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="33e66-133">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="33e66-134">sim</span><span class="sxs-lookup"><span data-stu-id="33e66-134">yes</span></span>       |
| [<span data-ttu-id="33e66-135">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="33e66-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="33e66-136">não</span><span class="sxs-lookup"><span data-stu-id="33e66-136">no</span></span>        |
| [<span data-ttu-id="33e66-137">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="33e66-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="33e66-138">não</span><span class="sxs-lookup"><span data-stu-id="33e66-138">no</span></span>        |
| [<span data-ttu-id="33e66-139">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="33e66-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="33e66-140">não</span><span class="sxs-lookup"><span data-stu-id="33e66-140">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="33e66-141">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="33e66-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33e66-142">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="33e66-142">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





