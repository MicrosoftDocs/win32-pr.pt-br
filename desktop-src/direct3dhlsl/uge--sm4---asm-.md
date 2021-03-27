---
title: uge (sm4-ASM)
description: Comparação de inteiros não assinados de vetor sem sinal com valor maior que ou-igual.
ms.assetid: CA8E19EC-619F-4C19-B6FD-91650B5DAF9F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4aecd9e39aa94c69acefff0f6a0fdf843cec5d8
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103823444"
---
# <a name="uge-sm4---asm"></a><span data-ttu-id="b012d-103">uge (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="b012d-103">uge (sm4 - asm)</span></span>

<span data-ttu-id="b012d-104">Comparação de inteiros não assinados de vetor sem sinal com valor maior que ou-igual.</span><span class="sxs-lookup"><span data-stu-id="b012d-104">Component-wise vector unsigned integer greater-than-or-equal comparison.</span></span>



| <span data-ttu-id="b012d-105">uge dest \[ . Mask \] , src0 \[ . swizzle \] , src1 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="b012d-105">uge dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|-------------------------------------------------------|



 



| <span data-ttu-id="b012d-106">Item</span><span class="sxs-lookup"><span data-stu-id="b012d-106">Item</span></span>                                                            | <span data-ttu-id="b012d-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="b012d-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="b012d-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="b012d-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="b012d-109">\[no \] endereço do resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="b012d-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="b012d-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="b012d-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="b012d-111">\[nos \] componentes para comparar com o *src1*.</span><span class="sxs-lookup"><span data-stu-id="b012d-111">\[in\] The components to compare to *src1*.</span></span><br/>        |
| <span data-ttu-id="b012d-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="b012d-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="b012d-113">\[nos \] componentes para comparar com o *src0*.</span><span class="sxs-lookup"><span data-stu-id="b012d-113">\[in\] The components to compare to *src0*.</span></span><br/>        |



 

## <a name="remarks"></a><span data-ttu-id="b012d-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="b012d-114">Remarks</span></span>

<span data-ttu-id="b012d-115">Essa instrução executa a comparação de inteiros sem sinal (*src0*  >=  *src1*) para cada componente e grava o resultado em *dest*.</span><span class="sxs-lookup"><span data-stu-id="b012d-115">This instruction performs the unsigned integer comparison (*src0* >= *src1*) for each component, and writes the result to *dest*.</span></span>

<span data-ttu-id="b012d-116">Se a comparação for verdadeira, 0xFFFFFFFF será retornado para esse componente.</span><span class="sxs-lookup"><span data-stu-id="b012d-116">If the comparison is true, then 0xFFFFFFFF is returned for that component.</span></span> <span data-ttu-id="b012d-117">Caso contrário, 0x0000000 será retornado.</span><span class="sxs-lookup"><span data-stu-id="b012d-117">Otherwise 0x0000000 is returned.</span></span>

<span data-ttu-id="b012d-118">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="b012d-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="b012d-119">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="b012d-119">Vertex Shader</span></span> | <span data-ttu-id="b012d-120">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="b012d-120">Geometry Shader</span></span> | <span data-ttu-id="b012d-121">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="b012d-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="b012d-122">x</span><span class="sxs-lookup"><span data-stu-id="b012d-122">x</span></span>             | <span data-ttu-id="b012d-123">x</span><span class="sxs-lookup"><span data-stu-id="b012d-123">x</span></span>               | <span data-ttu-id="b012d-124">x</span><span class="sxs-lookup"><span data-stu-id="b012d-124">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="b012d-125">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="b012d-125">Minimum Shader Model</span></span>

<span data-ttu-id="b012d-126">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="b012d-126">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="b012d-127">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="b012d-127">Shader Model</span></span>                                              | <span data-ttu-id="b012d-128">Com suporte</span><span class="sxs-lookup"><span data-stu-id="b012d-128">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="b012d-129">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="b012d-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="b012d-130">sim</span><span class="sxs-lookup"><span data-stu-id="b012d-130">yes</span></span>       |
| [<span data-ttu-id="b012d-131">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="b012d-131">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="b012d-132">sim</span><span class="sxs-lookup"><span data-stu-id="b012d-132">yes</span></span>       |
| [<span data-ttu-id="b012d-133">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="b012d-133">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="b012d-134">sim</span><span class="sxs-lookup"><span data-stu-id="b012d-134">yes</span></span>       |
| [<span data-ttu-id="b012d-135">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b012d-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="b012d-136">não</span><span class="sxs-lookup"><span data-stu-id="b012d-136">no</span></span>        |
| [<span data-ttu-id="b012d-137">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b012d-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="b012d-138">não</span><span class="sxs-lookup"><span data-stu-id="b012d-138">no</span></span>        |
| [<span data-ttu-id="b012d-139">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b012d-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="b012d-140">não</span><span class="sxs-lookup"><span data-stu-id="b012d-140">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="b012d-141">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b012d-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b012d-142">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b012d-142">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





