---
title: DP2 (sm4-ASM)
description: ponto de vetor bidimensional-produto dos componentes RG, POS-swizzle.
ms.assetid: E35F6A8B-6D8E-4660-B0F3-95B76BC19229
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4073def6cb315dc0268d1ce8e3f28039b9b2a69
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104365204"
---
# <a name="dp2-sm4---asm"></a><span data-ttu-id="04e82-103">DP2 (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="04e82-103">dp2 (sm4 - asm)</span></span>

<span data-ttu-id="04e82-104">ponto de vetor bidimensional-produto dos componentes RG, POS-swizzle.</span><span class="sxs-lookup"><span data-stu-id="04e82-104">2-dimensional vector dot-product of components rg, POS-swizzle.</span></span>



| <span data-ttu-id="04e82-105">DP2 \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="04e82-105">dp2\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="04e82-106">Item</span><span class="sxs-lookup"><span data-stu-id="04e82-106">Item</span></span>                                                            | <span data-ttu-id="04e82-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="04e82-107">Description</span></span>                                                                                                                    |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04e82-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="04e82-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="04e82-109">\[no \] endereço do resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="04e82-109">\[in\] The address of the result of the operation.</span></span> <br/> <span data-ttu-id="04e82-110">*dest*  =  *src0. r* \* *src1. r*  +  *src0. g* \* *src1. g*</span><span class="sxs-lookup"><span data-stu-id="04e82-110">*dest* = *src0.r* \* *src1.r* + *src0.g* \* *src1.g*</span></span><br/> |
| <span data-ttu-id="04e82-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="04e82-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="04e82-112">\[nos \] componentes na operação.</span><span class="sxs-lookup"><span data-stu-id="04e82-112">\[in\] The components in the operation.</span></span><br/>                                                                             |
| <span data-ttu-id="04e82-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="04e82-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="04e82-114">\[nos \] componentes na operação.</span><span class="sxs-lookup"><span data-stu-id="04e82-114">\[in\] The components in the operation.</span></span><br/>                                                                             |



 

## <a name="remarks"></a><span data-ttu-id="04e82-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="04e82-115">Remarks</span></span>

<span data-ttu-id="04e82-116">Resultado escalar replicado para componentes na máscara de gravação.</span><span class="sxs-lookup"><span data-stu-id="04e82-116">Scalar result replicated to components in write mask.</span></span>

<span data-ttu-id="04e82-117">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="04e82-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="04e82-118">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="04e82-118">Vertex Shader</span></span> | <span data-ttu-id="04e82-119">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="04e82-119">Geometry Shader</span></span> | <span data-ttu-id="04e82-120">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="04e82-120">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="04e82-121">x</span><span class="sxs-lookup"><span data-stu-id="04e82-121">x</span></span>             | <span data-ttu-id="04e82-122">x</span><span class="sxs-lookup"><span data-stu-id="04e82-122">x</span></span>               | <span data-ttu-id="04e82-123">x</span><span class="sxs-lookup"><span data-stu-id="04e82-123">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="04e82-124">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="04e82-124">Minimum Shader Model</span></span>

<span data-ttu-id="04e82-125">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="04e82-125">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="04e82-126">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="04e82-126">Shader Model</span></span>                                              | <span data-ttu-id="04e82-127">Com suporte</span><span class="sxs-lookup"><span data-stu-id="04e82-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="04e82-128">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="04e82-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="04e82-129">sim</span><span class="sxs-lookup"><span data-stu-id="04e82-129">yes</span></span>       |
| [<span data-ttu-id="04e82-130">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="04e82-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="04e82-131">sim</span><span class="sxs-lookup"><span data-stu-id="04e82-131">yes</span></span>       |
| [<span data-ttu-id="04e82-132">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="04e82-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="04e82-133">sim</span><span class="sxs-lookup"><span data-stu-id="04e82-133">yes</span></span>       |
| [<span data-ttu-id="04e82-134">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="04e82-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="04e82-135">não</span><span class="sxs-lookup"><span data-stu-id="04e82-135">no</span></span>        |
| [<span data-ttu-id="04e82-136">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="04e82-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="04e82-137">não</span><span class="sxs-lookup"><span data-stu-id="04e82-137">no</span></span>        |
| [<span data-ttu-id="04e82-138">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="04e82-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="04e82-139">não</span><span class="sxs-lookup"><span data-stu-id="04e82-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="04e82-140">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="04e82-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04e82-141">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="04e82-141">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





