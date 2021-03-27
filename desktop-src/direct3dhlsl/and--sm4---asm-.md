---
title: e (sm4-ASM)
description: AND bit a bit.
ms.assetid: 403DA289-E2CF-4736-8882-4131F884F777
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7ec9474322aafda2706502898902d01d0e13143
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103638883"
---
# <a name="and-sm4---asm"></a><span data-ttu-id="1097f-103">e (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="1097f-103">and (sm4 - asm)</span></span>

<span data-ttu-id="1097f-104">**E/**.</span><span class="sxs-lookup"><span data-stu-id="1097f-104">Bitwise **AND**.</span></span>



| <span data-ttu-id="1097f-105">e dest \[ . Mask \] , src0 \[ . swizzle \] , src1 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="1097f-105">and dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|-------------------------------------------------------|



 



| <span data-ttu-id="1097f-106">Item</span><span class="sxs-lookup"><span data-stu-id="1097f-106">Item</span></span>                                                            | <span data-ttu-id="1097f-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="1097f-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="1097f-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="1097f-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="1097f-109">\[no \] endereço do resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="1097f-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="1097f-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="1097f-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="1097f-111">\[no \] valor de 32 bits para **e** com *src1*.</span><span class="sxs-lookup"><span data-stu-id="1097f-111">\[in\] The 32-bit value to **AND** with *src1*.</span></span><br/>    |
| <span data-ttu-id="1097f-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="1097f-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="1097f-113">\[no \] valor de 32 bits para **e** com *src0*.</span><span class="sxs-lookup"><span data-stu-id="1097f-113">\[in\] The 32-bit value to **AND** with *src0*.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="1097f-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="1097f-114">Remarks</span></span>

<span data-ttu-id="1097f-115">Lógica de componente **e** de cada par de valores de 32 bits de *src0* e *src1*.</span><span class="sxs-lookup"><span data-stu-id="1097f-115">Component-wise logical **AND** of each pair of 32-bit values from *src0* and *src1*.</span></span> <span data-ttu-id="1097f-116">Os resultados de 32 bits são colocados no *dest*.</span><span class="sxs-lookup"><span data-stu-id="1097f-116">The 32-bit results are placed in *dest*.</span></span>

<span data-ttu-id="1097f-117">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="1097f-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="1097f-118">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="1097f-118">Vertex Shader</span></span> | <span data-ttu-id="1097f-119">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="1097f-119">Geometry Shader</span></span> | <span data-ttu-id="1097f-120">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="1097f-120">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="1097f-121">x</span><span class="sxs-lookup"><span data-stu-id="1097f-121">x</span></span>             | <span data-ttu-id="1097f-122">x</span><span class="sxs-lookup"><span data-stu-id="1097f-122">x</span></span>               | <span data-ttu-id="1097f-123">x</span><span class="sxs-lookup"><span data-stu-id="1097f-123">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="1097f-124">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="1097f-124">Minimum Shader Model</span></span>

<span data-ttu-id="1097f-125">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="1097f-125">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="1097f-126">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="1097f-126">Shader Model</span></span>                                              | <span data-ttu-id="1097f-127">Com suporte</span><span class="sxs-lookup"><span data-stu-id="1097f-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="1097f-128">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="1097f-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="1097f-129">sim</span><span class="sxs-lookup"><span data-stu-id="1097f-129">yes</span></span>       |
| [<span data-ttu-id="1097f-130">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="1097f-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="1097f-131">sim</span><span class="sxs-lookup"><span data-stu-id="1097f-131">yes</span></span>       |
| [<span data-ttu-id="1097f-132">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="1097f-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="1097f-133">sim</span><span class="sxs-lookup"><span data-stu-id="1097f-133">yes</span></span>       |
| [<span data-ttu-id="1097f-134">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1097f-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="1097f-135">não</span><span class="sxs-lookup"><span data-stu-id="1097f-135">no</span></span>        |
| [<span data-ttu-id="1097f-136">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1097f-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="1097f-137">não</span><span class="sxs-lookup"><span data-stu-id="1097f-137">no</span></span>        |
| [<span data-ttu-id="1097f-138">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1097f-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="1097f-139">não</span><span class="sxs-lookup"><span data-stu-id="1097f-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="1097f-140">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1097f-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1097f-141">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1097f-141">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





