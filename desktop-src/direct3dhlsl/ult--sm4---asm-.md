---
title: ultados (sm4-ASM)
description: Comparação de inteiros não assinados de vetor sem sinal de componente.
ms.assetid: DB10F654-4A98-4ED8-A3B4-CA9FE1DFE6CD
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 624c09d182e9ecfd4d1b603f6fd2c34b83d768ed
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104988571"
---
# <a name="ult-sm4---asm"></a><span data-ttu-id="c2d2c-103">ultados (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="c2d2c-103">ult (sm4 - asm)</span></span>

<span data-ttu-id="c2d2c-104">Comparação de inteiros não assinados de vetor sem sinal de componente.</span><span class="sxs-lookup"><span data-stu-id="c2d2c-104">Component-wise vector unsigned integer less-than comparison.</span></span>



| <span data-ttu-id="c2d2c-105">ultados dest \[ . Mask \] , src0 \[ . swizzle \] , src1 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="c2d2c-105">ult dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|-------------------------------------------------------|



 



| <span data-ttu-id="c2d2c-106">Item</span><span class="sxs-lookup"><span data-stu-id="c2d2c-106">Item</span></span>                                                            | <span data-ttu-id="c2d2c-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="c2d2c-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="c2d2c-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="c2d2c-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="c2d2c-109">\[no \] endereço do resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="c2d2c-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="c2d2c-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="c2d2c-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="c2d2c-111">\[no \] valor a ser comparado com *src1*.</span><span class="sxs-lookup"><span data-stu-id="c2d2c-111">\[in\] The value to compare to *src1*.</span></span><br/>             |
| <span data-ttu-id="c2d2c-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="c2d2c-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="c2d2c-113">\[no \] valor a ser comparado com *src1*.</span><span class="sxs-lookup"><span data-stu-id="c2d2c-113">\[in\] The value to compare to *src1*.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="c2d2c-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="c2d2c-114">Remarks</span></span>

<span data-ttu-id="c2d2c-115">Executa a comparação de inteiros sem sinal (*src0*  <  *src1*) para cada componente e grava o resultado em *dest*.</span><span class="sxs-lookup"><span data-stu-id="c2d2c-115">Performs the unsigned integer comparison (*src0* < *src1*) for each component, and writes the result to *dest*.</span></span>

<span data-ttu-id="c2d2c-116">Se a comparação for verdadeira, essa instrução retornará 0xFFFFFFFF para esse componente.</span><span class="sxs-lookup"><span data-stu-id="c2d2c-116">If the comparison is true, this instruction returns 0xFFFFFFFF for that component.</span></span> <span data-ttu-id="c2d2c-117">Caso contrário, ele retornará 0x0000000.</span><span class="sxs-lookup"><span data-stu-id="c2d2c-117">Otherwise it returns 0x0000000.</span></span>

<span data-ttu-id="c2d2c-118">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="c2d2c-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="c2d2c-119">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="c2d2c-119">Vertex Shader</span></span> | <span data-ttu-id="c2d2c-120">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="c2d2c-120">Geometry Shader</span></span> | <span data-ttu-id="c2d2c-121">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="c2d2c-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="c2d2c-122">x</span><span class="sxs-lookup"><span data-stu-id="c2d2c-122">x</span></span>             | <span data-ttu-id="c2d2c-123">x</span><span class="sxs-lookup"><span data-stu-id="c2d2c-123">x</span></span>               | <span data-ttu-id="c2d2c-124">x</span><span class="sxs-lookup"><span data-stu-id="c2d2c-124">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="c2d2c-125">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="c2d2c-125">Minimum Shader Model</span></span>

<span data-ttu-id="c2d2c-126">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="c2d2c-126">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="c2d2c-127">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="c2d2c-127">Shader Model</span></span>                                              | <span data-ttu-id="c2d2c-128">Com suporte</span><span class="sxs-lookup"><span data-stu-id="c2d2c-128">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="c2d2c-129">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="c2d2c-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="c2d2c-130">sim</span><span class="sxs-lookup"><span data-stu-id="c2d2c-130">yes</span></span>       |
| [<span data-ttu-id="c2d2c-131">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="c2d2c-131">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="c2d2c-132">sim</span><span class="sxs-lookup"><span data-stu-id="c2d2c-132">yes</span></span>       |
| [<span data-ttu-id="c2d2c-133">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="c2d2c-133">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="c2d2c-134">sim</span><span class="sxs-lookup"><span data-stu-id="c2d2c-134">yes</span></span>       |
| [<span data-ttu-id="c2d2c-135">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c2d2c-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="c2d2c-136">não</span><span class="sxs-lookup"><span data-stu-id="c2d2c-136">no</span></span>        |
| [<span data-ttu-id="c2d2c-137">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c2d2c-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="c2d2c-138">não</span><span class="sxs-lookup"><span data-stu-id="c2d2c-138">no</span></span>        |
| [<span data-ttu-id="c2d2c-139">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c2d2c-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="c2d2c-140">não</span><span class="sxs-lookup"><span data-stu-id="c2d2c-140">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="c2d2c-141">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c2d2c-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2d2c-142">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c2d2c-142">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





