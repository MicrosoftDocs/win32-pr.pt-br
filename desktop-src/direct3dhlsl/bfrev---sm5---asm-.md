---
title: bfrev (SM5-ASM)
description: Inverta um número de 32 bits.
ms.assetid: 24F8209A-093E-4737-BF50-12F228024E9D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11bf0f07b6c66babf8e7f91108f86ba753420fc2
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104988593"
---
# <a name="bfrev-sm5---asm"></a><span data-ttu-id="bf0f1-103">bfrev (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="bf0f1-103">bfrev (sm5 - asm)</span></span>

<span data-ttu-id="bf0f1-104">Inverta um número de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="bf0f1-104">Reverse a 32-bit number.</span></span>



| <span data-ttu-id="bf0f1-105">bfrev dest \[ . Mask \] , src0 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="bf0f1-105">bfrev dest\[.mask\], src0\[.swizzle\]</span></span> |
|---------------------------------------|



 



| <span data-ttu-id="bf0f1-106">Item</span><span class="sxs-lookup"><span data-stu-id="bf0f1-106">Item</span></span>                                                            | <span data-ttu-id="bf0f1-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="bf0f1-107">Description</span></span>                                                  |
|-----------------------------------------------------------------|--------------------------------------------------------------|
| <span data-ttu-id="bf0f1-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="bf0f1-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="bf0f1-109">\[no \] endereço para *src0* com bits invertidos.</span><span class="sxs-lookup"><span data-stu-id="bf0f1-109">\[in\] The address for *src0* with bits reversed.</span></span><br/> |
| <span data-ttu-id="bf0f1-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="bf0f1-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="bf0f1-111">\[no \] número de 32 bits para reverter.</span><span class="sxs-lookup"><span data-stu-id="bf0f1-111">\[in\] The 32-bit number to reverse.</span></span><br/>              |



 

## <a name="remarks"></a><span data-ttu-id="bf0f1-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="bf0f1-112">Remarks</span></span>

<span data-ttu-id="bf0f1-113">Por exemplo, dado 0x12345678, o resultado seria 0x1e6a2c48.</span><span class="sxs-lookup"><span data-stu-id="bf0f1-113">For example, given 0x12345678 the result would be 0x1e6a2c48.</span></span>

<span data-ttu-id="bf0f1-114">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="bf0f1-114">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="bf0f1-115">Vértice</span><span class="sxs-lookup"><span data-stu-id="bf0f1-115">Vertex</span></span> | <span data-ttu-id="bf0f1-116">Envoltória</span><span class="sxs-lookup"><span data-stu-id="bf0f1-116">Hull</span></span> | <span data-ttu-id="bf0f1-117">Domínio</span><span class="sxs-lookup"><span data-stu-id="bf0f1-117">Domain</span></span> | <span data-ttu-id="bf0f1-118">Geometria</span><span class="sxs-lookup"><span data-stu-id="bf0f1-118">Geometry</span></span> | <span data-ttu-id="bf0f1-119">16x16</span><span class="sxs-lookup"><span data-stu-id="bf0f1-119">Pixel</span></span> | <span data-ttu-id="bf0f1-120">Computação</span><span class="sxs-lookup"><span data-stu-id="bf0f1-120">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="bf0f1-121">X</span><span class="sxs-lookup"><span data-stu-id="bf0f1-121">X</span></span>      | <span data-ttu-id="bf0f1-122">X</span><span class="sxs-lookup"><span data-stu-id="bf0f1-122">X</span></span>    | <span data-ttu-id="bf0f1-123">X</span><span class="sxs-lookup"><span data-stu-id="bf0f1-123">X</span></span>      | <span data-ttu-id="bf0f1-124">X</span><span class="sxs-lookup"><span data-stu-id="bf0f1-124">X</span></span>        | <span data-ttu-id="bf0f1-125">X</span><span class="sxs-lookup"><span data-stu-id="bf0f1-125">X</span></span>     | <span data-ttu-id="bf0f1-126">X</span><span class="sxs-lookup"><span data-stu-id="bf0f1-126">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="bf0f1-127">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="bf0f1-127">Minimum Shader Model</span></span>

<span data-ttu-id="bf0f1-128">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="bf0f1-128">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="bf0f1-129">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="bf0f1-129">Shader Model</span></span>                                              | <span data-ttu-id="bf0f1-130">Com suporte</span><span class="sxs-lookup"><span data-stu-id="bf0f1-130">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="bf0f1-131">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="bf0f1-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="bf0f1-132">sim</span><span class="sxs-lookup"><span data-stu-id="bf0f1-132">yes</span></span>       |
| [<span data-ttu-id="bf0f1-133">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="bf0f1-133">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="bf0f1-134">não</span><span class="sxs-lookup"><span data-stu-id="bf0f1-134">no</span></span>        |
| [<span data-ttu-id="bf0f1-135">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="bf0f1-135">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="bf0f1-136">não</span><span class="sxs-lookup"><span data-stu-id="bf0f1-136">no</span></span>        |
| [<span data-ttu-id="bf0f1-137">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bf0f1-137">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="bf0f1-138">não</span><span class="sxs-lookup"><span data-stu-id="bf0f1-138">no</span></span>        |
| [<span data-ttu-id="bf0f1-139">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bf0f1-139">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="bf0f1-140">não</span><span class="sxs-lookup"><span data-stu-id="bf0f1-140">no</span></span>        |
| [<span data-ttu-id="bf0f1-141">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bf0f1-141">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="bf0f1-142">não</span><span class="sxs-lookup"><span data-stu-id="bf0f1-142">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="bf0f1-143">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bf0f1-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf0f1-144">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bf0f1-144">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





