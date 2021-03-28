---
title: Umax (sm4-ASM)
description: Máximo de inteiro sem sinal de componente.
ms.assetid: 86BCF7A7-99CA-481B-82B4-E0BA30963344
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ceb1fda620facce31132f56ed888d18022ca27ec
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104365228"
---
# <a name="umax-sm4---asm"></a><span data-ttu-id="2e381-103">Umax (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="2e381-103">umax (sm4 - asm)</span></span>

<span data-ttu-id="2e381-104">Máximo de inteiro sem sinal de componente.</span><span class="sxs-lookup"><span data-stu-id="2e381-104">Component-wise unsigned integer maximum.</span></span>



| <span data-ttu-id="2e381-105">Umax dest \[ . Mask \] , src0 \[ . swizzle \] , src1 \[ . swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="2e381-105">umax dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\],</span></span> |
|---------------------------------------------------------|



 



| <span data-ttu-id="2e381-106">Item</span><span class="sxs-lookup"><span data-stu-id="2e381-106">Item</span></span>                                                            | <span data-ttu-id="2e381-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="2e381-107">Description</span></span>                                                                                                            |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e381-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="2e381-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="2e381-109">\[no \] endereço do resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="2e381-109">\[in\] The address of the result of the operation.</span></span><br/> <span data-ttu-id="2e381-110">*dest*  =  *src0*  >  *src1* ?</span><span class="sxs-lookup"><span data-stu-id="2e381-110">*dest* = *src0* > *src1* ?</span></span> <span data-ttu-id="2e381-111">*src0* : *src1*</span><span class="sxs-lookup"><span data-stu-id="2e381-111">*src0* : *src1*</span></span><br/> |
| <span data-ttu-id="2e381-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="2e381-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="2e381-113">\[no \] valor a ser comparado com *src1*.</span><span class="sxs-lookup"><span data-stu-id="2e381-113">\[in\] The value to compare to *src1*.</span></span><br/>                                                                      |
| <span data-ttu-id="2e381-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="2e381-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="2e381-115">\[no \] valor a ser comparado com *src0*.</span><span class="sxs-lookup"><span data-stu-id="2e381-115">\[in\] The value to compare to *src0*.</span></span><br/>                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="2e381-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="2e381-116">Remarks</span></span>

<span data-ttu-id="2e381-117">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="2e381-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="2e381-118">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="2e381-118">Vertex Shader</span></span> | <span data-ttu-id="2e381-119">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="2e381-119">Geometry Shader</span></span> | <span data-ttu-id="2e381-120">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="2e381-120">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="2e381-121">x</span><span class="sxs-lookup"><span data-stu-id="2e381-121">x</span></span>             | <span data-ttu-id="2e381-122">x</span><span class="sxs-lookup"><span data-stu-id="2e381-122">x</span></span>               | <span data-ttu-id="2e381-123">x</span><span class="sxs-lookup"><span data-stu-id="2e381-123">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="2e381-124">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="2e381-124">Minimum Shader Model</span></span>

<span data-ttu-id="2e381-125">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="2e381-125">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="2e381-126">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="2e381-126">Shader Model</span></span>                                              | <span data-ttu-id="2e381-127">Com suporte</span><span class="sxs-lookup"><span data-stu-id="2e381-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="2e381-128">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="2e381-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="2e381-129">sim</span><span class="sxs-lookup"><span data-stu-id="2e381-129">yes</span></span>       |
| [<span data-ttu-id="2e381-130">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="2e381-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="2e381-131">sim</span><span class="sxs-lookup"><span data-stu-id="2e381-131">yes</span></span>       |
| [<span data-ttu-id="2e381-132">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="2e381-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="2e381-133">sim</span><span class="sxs-lookup"><span data-stu-id="2e381-133">yes</span></span>       |
| [<span data-ttu-id="2e381-134">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2e381-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="2e381-135">não</span><span class="sxs-lookup"><span data-stu-id="2e381-135">no</span></span>        |
| [<span data-ttu-id="2e381-136">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2e381-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="2e381-137">não</span><span class="sxs-lookup"><span data-stu-id="2e381-137">no</span></span>        |
| [<span data-ttu-id="2e381-138">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2e381-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="2e381-139">não</span><span class="sxs-lookup"><span data-stu-id="2e381-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="2e381-140">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2e381-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2e381-141">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2e381-141">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





