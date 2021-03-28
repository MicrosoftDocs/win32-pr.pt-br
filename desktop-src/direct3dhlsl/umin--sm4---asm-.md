---
title: umin (sm4-ASM)
description: Mínimo de inteiro sem sinal de componente.
ms.assetid: 134B128F-7B47-4819-A576-80766EDB14C9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 059b9660e4969b252c867a009a920259c92bff18
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104084261"
---
# <a name="umin-sm4---asm"></a><span data-ttu-id="69595-103">umin (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="69595-103">umin (sm4 - asm)</span></span>

<span data-ttu-id="69595-104">Mínimo de inteiro sem sinal de componente.</span><span class="sxs-lookup"><span data-stu-id="69595-104">Component-wise unsigned integer minimum.</span></span>



| <span data-ttu-id="69595-105">umin dest \[ . Mask \] , src0 \[ . swizzle \] , src1 \[ . swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="69595-105">umin dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\],</span></span> |
|---------------------------------------------------------|



 



| <span data-ttu-id="69595-106">Item</span><span class="sxs-lookup"><span data-stu-id="69595-106">Item</span></span>                                                            | <span data-ttu-id="69595-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="69595-107">Description</span></span>                                                                                                            |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69595-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="69595-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="69595-109">\[no \] endereço do resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="69595-109">\[in\] The address of the result of the operation.</span></span><br/> <span data-ttu-id="69595-110">*dest*  =  *src0*  <  *src1* ?</span><span class="sxs-lookup"><span data-stu-id="69595-110">*dest* = *src0* < *src1* ?</span></span> <span data-ttu-id="69595-111">*src0* : *src1*</span><span class="sxs-lookup"><span data-stu-id="69595-111">*src0* : *src1*</span></span><br/> |
| <span data-ttu-id="69595-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="69595-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="69595-113">\[no \] valor a ser comparado com *src1*.</span><span class="sxs-lookup"><span data-stu-id="69595-113">\[in\] The value to compare to *src1*.</span></span><br/>                                                                      |
| <span data-ttu-id="69595-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="69595-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="69595-115">\[no \] valor a ser comparado com *src0*.</span><span class="sxs-lookup"><span data-stu-id="69595-115">\[in\] The value to compare to *src0*.</span></span><br/>                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="69595-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="69595-116">Remarks</span></span>

<span data-ttu-id="69595-117">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="69595-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="69595-118">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="69595-118">Vertex Shader</span></span> | <span data-ttu-id="69595-119">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="69595-119">Geometry Shader</span></span> | <span data-ttu-id="69595-120">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="69595-120">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="69595-121">x</span><span class="sxs-lookup"><span data-stu-id="69595-121">x</span></span>             | <span data-ttu-id="69595-122">x</span><span class="sxs-lookup"><span data-stu-id="69595-122">x</span></span>               | <span data-ttu-id="69595-123">x</span><span class="sxs-lookup"><span data-stu-id="69595-123">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="69595-124">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="69595-124">Minimum Shader Model</span></span>

<span data-ttu-id="69595-125">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="69595-125">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="69595-126">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="69595-126">Shader Model</span></span>                                              | <span data-ttu-id="69595-127">Com suporte</span><span class="sxs-lookup"><span data-stu-id="69595-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="69595-128">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="69595-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="69595-129">sim</span><span class="sxs-lookup"><span data-stu-id="69595-129">yes</span></span>       |
| [<span data-ttu-id="69595-130">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="69595-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="69595-131">sim</span><span class="sxs-lookup"><span data-stu-id="69595-131">yes</span></span>       |
| [<span data-ttu-id="69595-132">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="69595-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="69595-133">sim</span><span class="sxs-lookup"><span data-stu-id="69595-133">yes</span></span>       |
| [<span data-ttu-id="69595-134">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="69595-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="69595-135">não</span><span class="sxs-lookup"><span data-stu-id="69595-135">no</span></span>        |
| [<span data-ttu-id="69595-136">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="69595-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="69595-137">não</span><span class="sxs-lookup"><span data-stu-id="69595-137">no</span></span>        |
| [<span data-ttu-id="69595-138">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="69595-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="69595-139">não</span><span class="sxs-lookup"><span data-stu-id="69595-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="69595-140">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="69595-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="69595-141">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="69595-141">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





