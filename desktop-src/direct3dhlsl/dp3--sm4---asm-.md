---
title: DP3 (sm4-ASM)
description: ponto de vetor tridimensional-produto de componentes RGB, POS-swizzle.
ms.assetid: 8E6EA6CD-B5BB-4D64-8846-F7B9F7135582
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2598053abed93675107f15af762e0844d4938fbf
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103823440"
---
# <a name="dp3-sm4---asm"></a><span data-ttu-id="6080f-103">DP3 (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="6080f-103">dp3 (sm4 - asm)</span></span>

<span data-ttu-id="6080f-104">ponto de vetor tridimensional-produto de componentes RGB, POS-swizzle.</span><span class="sxs-lookup"><span data-stu-id="6080f-104">3-dimensional vector dot-product of components rgb, POS-swizzle.</span></span>



| <span data-ttu-id="6080f-105">DP3 \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="6080f-105">dp3\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\],</span></span> |
|---------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="6080f-106">Item</span><span class="sxs-lookup"><span data-stu-id="6080f-106">Item</span></span>                                                            | <span data-ttu-id="6080f-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="6080f-107">Description</span></span>                                                                                                                           |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6080f-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="6080f-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="6080f-109">\[no \] resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="6080f-109">\[in\] The result of the operation.</span></span><br/> <span data-ttu-id="6080f-110">*dest*  =  *src0. r* \* *src1. r*  +  *src0. g* \* *src1. g*  +  *src0. b* \* *src1. b*</span><span class="sxs-lookup"><span data-stu-id="6080f-110">*dest* = *src0.r* \* *src1.r* + *src0.g* \* *src1.g* + *src0.b* \* *src1.b*</span></span><br/> |
| <span data-ttu-id="6080f-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="6080f-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="6080f-112">\[nos \] componentes do operação.</span><span class="sxs-lookup"><span data-stu-id="6080f-112">\[in\] The components in the opertation.</span></span><br/>                                                                                   |
| <span data-ttu-id="6080f-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="6080f-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="6080f-114">\[nos \] componentes do operação.</span><span class="sxs-lookup"><span data-stu-id="6080f-114">\[in\] The components in the opertation.</span></span><br/>                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="6080f-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="6080f-115">Remarks</span></span>

<span data-ttu-id="6080f-116">Resultado escalar replicado para componentes na máscara de gravação.</span><span class="sxs-lookup"><span data-stu-id="6080f-116">Scalar result replicated to components in write mask.</span></span>

<span data-ttu-id="6080f-117">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="6080f-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="6080f-118">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="6080f-118">Vertex Shader</span></span> | <span data-ttu-id="6080f-119">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="6080f-119">Geometry Shader</span></span> | <span data-ttu-id="6080f-120">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="6080f-120">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="6080f-121">x</span><span class="sxs-lookup"><span data-stu-id="6080f-121">x</span></span>             | <span data-ttu-id="6080f-122">x</span><span class="sxs-lookup"><span data-stu-id="6080f-122">x</span></span>               | <span data-ttu-id="6080f-123">x</span><span class="sxs-lookup"><span data-stu-id="6080f-123">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="6080f-124">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="6080f-124">Minimum Shader Model</span></span>

<span data-ttu-id="6080f-125">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="6080f-125">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="6080f-126">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="6080f-126">Shader Model</span></span>                                              | <span data-ttu-id="6080f-127">Com suporte</span><span class="sxs-lookup"><span data-stu-id="6080f-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="6080f-128">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="6080f-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="6080f-129">sim</span><span class="sxs-lookup"><span data-stu-id="6080f-129">yes</span></span>       |
| [<span data-ttu-id="6080f-130">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="6080f-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="6080f-131">sim</span><span class="sxs-lookup"><span data-stu-id="6080f-131">yes</span></span>       |
| [<span data-ttu-id="6080f-132">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="6080f-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="6080f-133">sim</span><span class="sxs-lookup"><span data-stu-id="6080f-133">yes</span></span>       |
| [<span data-ttu-id="6080f-134">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6080f-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="6080f-135">não</span><span class="sxs-lookup"><span data-stu-id="6080f-135">no</span></span>        |
| [<span data-ttu-id="6080f-136">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6080f-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="6080f-137">não</span><span class="sxs-lookup"><span data-stu-id="6080f-137">no</span></span>        |
| [<span data-ttu-id="6080f-138">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6080f-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="6080f-139">não</span><span class="sxs-lookup"><span data-stu-id="6080f-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="6080f-140">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6080f-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6080f-141">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6080f-141">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





