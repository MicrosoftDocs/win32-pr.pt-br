---
title: Imin (sm4-ASM)
description: Inteiro de componente-Wise mínimo.
ms.assetid: 8EDD5503-76D5-4078-BFBA-1DA9260C6E68
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 942384e7a988e4919a483e09c75e476d5a6917ba
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104365262"
---
# <a name="imin-sm4---asm"></a><span data-ttu-id="b507b-103">Imin (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="b507b-103">imin (sm4 - asm)</span></span>

<span data-ttu-id="b507b-104">Inteiro de componente-Wise mínimo.</span><span class="sxs-lookup"><span data-stu-id="b507b-104">Component-wise integer minimum.</span></span>



| <span data-ttu-id="b507b-105">Imin dest \[ . Mask \] , \[  - \] src0 \[ . swizzle \] , \[ - \] src1 \[ . swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="b507b-105">imin dest\[.mask\], \[ -\]src0\[.swizzle\], \[-\]src1\[.swizzle\],</span></span> |
|--------------------------------------------------------------------|



 



| <span data-ttu-id="b507b-106">Item</span><span class="sxs-lookup"><span data-stu-id="b507b-106">Item</span></span>                                                            | <span data-ttu-id="b507b-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="b507b-107">Description</span></span>                                                                                             |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b507b-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="b507b-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="b507b-109">\[no \] resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="b507b-109">\[in\] The result of the operation.</span></span><br/> <span data-ttu-id="b507b-110">*dest*  =  *src0*  <  *src1* ?</span><span class="sxs-lookup"><span data-stu-id="b507b-110">*dest* = *src0* < *src1* ?</span></span> <span data-ttu-id="b507b-111">*src0* : *src1*</span><span class="sxs-lookup"><span data-stu-id="b507b-111">*src0* : *src1*</span></span><br/> |
| <span data-ttu-id="b507b-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="b507b-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="b507b-113">\[no \] valor a ser comparado com *src1*.</span><span class="sxs-lookup"><span data-stu-id="b507b-113">\[in\] The value to compare to *src1*.</span></span><br/>                                                       |
| <span data-ttu-id="b507b-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="b507b-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="b507b-115">\[no \] valor a ser comparado com *src0*.</span><span class="sxs-lookup"><span data-stu-id="b507b-115">\[in\] The value to compare to *src0*.</span></span><br/>                                                       |



 

## <a name="remarks"></a><span data-ttu-id="b507b-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="b507b-116">Remarks</span></span>

<span data-ttu-id="b507b-117">O modificador opcional Negate nos operandos de origem usa o complemento de 2 antes de executar a operação.</span><span class="sxs-lookup"><span data-stu-id="b507b-117">Optional negate modifier on source operands takes 2's complement before performing operation.</span></span>

<span data-ttu-id="b507b-118">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="b507b-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="b507b-119">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="b507b-119">Vertex Shader</span></span> | <span data-ttu-id="b507b-120">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="b507b-120">Geometry Shader</span></span> | <span data-ttu-id="b507b-121">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="b507b-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="b507b-122">x</span><span class="sxs-lookup"><span data-stu-id="b507b-122">x</span></span>             | <span data-ttu-id="b507b-123">x</span><span class="sxs-lookup"><span data-stu-id="b507b-123">x</span></span>               | <span data-ttu-id="b507b-124">x</span><span class="sxs-lookup"><span data-stu-id="b507b-124">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="b507b-125">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="b507b-125">Minimum Shader Model</span></span>

<span data-ttu-id="b507b-126">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="b507b-126">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="b507b-127">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="b507b-127">Shader Model</span></span>                                              | <span data-ttu-id="b507b-128">Com suporte</span><span class="sxs-lookup"><span data-stu-id="b507b-128">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="b507b-129">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="b507b-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="b507b-130">sim</span><span class="sxs-lookup"><span data-stu-id="b507b-130">yes</span></span>       |
| [<span data-ttu-id="b507b-131">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="b507b-131">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="b507b-132">sim</span><span class="sxs-lookup"><span data-stu-id="b507b-132">yes</span></span>       |
| [<span data-ttu-id="b507b-133">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="b507b-133">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="b507b-134">sim</span><span class="sxs-lookup"><span data-stu-id="b507b-134">yes</span></span>       |
| [<span data-ttu-id="b507b-135">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b507b-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="b507b-136">não</span><span class="sxs-lookup"><span data-stu-id="b507b-136">no</span></span>        |
| [<span data-ttu-id="b507b-137">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b507b-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="b507b-138">não</span><span class="sxs-lookup"><span data-stu-id="b507b-138">no</span></span>        |
| [<span data-ttu-id="b507b-139">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b507b-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="b507b-140">não</span><span class="sxs-lookup"><span data-stu-id="b507b-140">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="b507b-141">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b507b-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b507b-142">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b507b-142">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





