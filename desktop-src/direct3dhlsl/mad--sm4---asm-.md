---
title: Mad (sm4-ASM)
description: Adição de multiplicação por componente.
ms.assetid: 1C24AF49-AA32-4D3A-8478-C9BAC4FE7D77
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d34823cdb3545f29426117b35903c97c08c5807
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104006877"
---
# <a name="mad-sm4---asm"></a><span data-ttu-id="c569d-103">Mad (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="c569d-103">mad (sm4 - asm)</span></span>

<span data-ttu-id="c569d-104">Adição de & de multiplicação por componente.</span><span class="sxs-lookup"><span data-stu-id="c569d-104">Component-wise multiply & add.</span></span>



| <span data-ttu-id="c569d-105">: Mad \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . swizzle \] , \[ - \] src2 \[ \_ ABS \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="c569d-105">:mad\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\], \[-\]src2\[\_abs\]\[.swizzle\]</span></span> |
|-----------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="c569d-106">Item</span><span class="sxs-lookup"><span data-stu-id="c569d-106">Item</span></span>                                                            | <span data-ttu-id="c569d-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="c569d-107">Description</span></span>                                                                                  |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c569d-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="c569d-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="c569d-109">\[no \] resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="c569d-109">\[in\] The result of the operation.</span></span><br/> <span data-ttu-id="c569d-110">*dest*  =  *src0* \* *src1*  +  *src2*</span><span class="sxs-lookup"><span data-stu-id="c569d-110">*dest* = *src0* \* *src1* + *src2*</span></span><br/> |
| <span data-ttu-id="c569d-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="c569d-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="c569d-112">\[no \] multiplicando.</span><span class="sxs-lookup"><span data-stu-id="c569d-112">\[in\] The multiplicand.</span></span><br/>                                                          |
| <span data-ttu-id="c569d-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="c569d-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="c569d-114">\[no \] multiplicador.</span><span class="sxs-lookup"><span data-stu-id="c569d-114">\[in\] The multiplier.</span></span><br/>                                                            |
| <span data-ttu-id="c569d-115"><span id="src2"></span><span id="SRC2"></span>*src2*</span><span class="sxs-lookup"><span data-stu-id="c569d-115"><span id="src2"></span><span id="SRC2"></span>*src2*</span></span><br/> | <span data-ttu-id="c569d-116">\[no \] adendo.</span><span class="sxs-lookup"><span data-stu-id="c569d-116">\[in\] The addend.</span></span><br/>                                                                |



 

## <a name="remarks"></a><span data-ttu-id="c569d-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="c569d-117">Remarks</span></span>

<span data-ttu-id="c569d-118">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="c569d-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="c569d-119">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="c569d-119">Vertex Shader</span></span> | <span data-ttu-id="c569d-120">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="c569d-120">Geometry Shader</span></span> | <span data-ttu-id="c569d-121">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="c569d-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="c569d-122">x</span><span class="sxs-lookup"><span data-stu-id="c569d-122">x</span></span>             | <span data-ttu-id="c569d-123">x</span><span class="sxs-lookup"><span data-stu-id="c569d-123">x</span></span>               | <span data-ttu-id="c569d-124">x</span><span class="sxs-lookup"><span data-stu-id="c569d-124">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="c569d-125">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="c569d-125">Minimum Shader Model</span></span>

<span data-ttu-id="c569d-126">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="c569d-126">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="c569d-127">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="c569d-127">Shader Model</span></span>                                              | <span data-ttu-id="c569d-128">Com suporte</span><span class="sxs-lookup"><span data-stu-id="c569d-128">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="c569d-129">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="c569d-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="c569d-130">sim</span><span class="sxs-lookup"><span data-stu-id="c569d-130">yes</span></span>       |
| [<span data-ttu-id="c569d-131">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="c569d-131">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="c569d-132">sim</span><span class="sxs-lookup"><span data-stu-id="c569d-132">yes</span></span>       |
| [<span data-ttu-id="c569d-133">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="c569d-133">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="c569d-134">sim</span><span class="sxs-lookup"><span data-stu-id="c569d-134">yes</span></span>       |
| [<span data-ttu-id="c569d-135">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c569d-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="c569d-136">não</span><span class="sxs-lookup"><span data-stu-id="c569d-136">no</span></span>        |
| [<span data-ttu-id="c569d-137">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c569d-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="c569d-138">não</span><span class="sxs-lookup"><span data-stu-id="c569d-138">no</span></span>        |
| [<span data-ttu-id="c569d-139">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c569d-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="c569d-140">não</span><span class="sxs-lookup"><span data-stu-id="c569d-140">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="c569d-141">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c569d-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c569d-142">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c569d-142">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





