---
title: XOR (sm4-ASM)
description: XOR bits.
ms.assetid: 6B949653-6DDA-402B-8ABE-B93858B68470
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7a998bd1e95793f463d7f234b464a542bed4fc0
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104365187"
---
# <a name="xor-sm4---asm"></a><span data-ttu-id="d287c-103">XOR (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="d287c-103">xor (sm4 - asm)</span></span>

<span data-ttu-id="d287c-104">XOR bits.</span><span class="sxs-lookup"><span data-stu-id="d287c-104">Bitwise xor.</span></span>



| <span data-ttu-id="d287c-105">XOR dest \[ . Mask \] , src0 \[ . swizzle \] , src1 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="d287c-105">xor dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|-------------------------------------------------------|



 



| <span data-ttu-id="d287c-106">Item</span><span class="sxs-lookup"><span data-stu-id="d287c-106">Item</span></span>                                                            | <span data-ttu-id="d287c-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="d287c-107">Description</span></span>                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d287c-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="d287c-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="d287c-109">\[no \] resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="d287c-109">\[in\] The result of the operation.</span></span><br/>       |
| <span data-ttu-id="d287c-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="d287c-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="d287c-111">\[nos \] componentes para XOR com *src1*.</span><span class="sxs-lookup"><span data-stu-id="d287c-111">\[in\] The components to XOR with *src1*.</span></span><br/> |
| <span data-ttu-id="d287c-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="d287c-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="d287c-113">\[nos \] componentes para XOR com *src0*.</span><span class="sxs-lookup"><span data-stu-id="d287c-113">\[in\] The components to XOR with *src0*.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d287c-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="d287c-114">Remarks</span></span>

<span data-ttu-id="d287c-115">Essa instrução executa um XOR lógico inteligente de componente de cada par de valores de 32 bits de *src0* e *src1*.</span><span class="sxs-lookup"><span data-stu-id="d287c-115">This instruction performs a component-wise logical XOR of each pair of 32-bit values from *src0* and *src1*.</span></span> <span data-ttu-id="d287c-116">os resultados de 32 bits são colocados no *dest*.</span><span class="sxs-lookup"><span data-stu-id="d287c-116">32-bit results are placed in *dest*.</span></span>

<span data-ttu-id="d287c-117">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="d287c-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="d287c-118">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="d287c-118">Vertex Shader</span></span> | <span data-ttu-id="d287c-119">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="d287c-119">Geometry Shader</span></span> | <span data-ttu-id="d287c-120">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="d287c-120">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="d287c-121">x</span><span class="sxs-lookup"><span data-stu-id="d287c-121">x</span></span>             | <span data-ttu-id="d287c-122">x</span><span class="sxs-lookup"><span data-stu-id="d287c-122">x</span></span>               | <span data-ttu-id="d287c-123">x</span><span class="sxs-lookup"><span data-stu-id="d287c-123">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d287c-124">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="d287c-124">Minimum Shader Model</span></span>

<span data-ttu-id="d287c-125">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="d287c-125">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="d287c-126">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="d287c-126">Shader Model</span></span>                                              | <span data-ttu-id="d287c-127">Com suporte</span><span class="sxs-lookup"><span data-stu-id="d287c-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="d287c-128">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="d287c-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="d287c-129">sim</span><span class="sxs-lookup"><span data-stu-id="d287c-129">yes</span></span>       |
| [<span data-ttu-id="d287c-130">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="d287c-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="d287c-131">sim</span><span class="sxs-lookup"><span data-stu-id="d287c-131">yes</span></span>       |
| [<span data-ttu-id="d287c-132">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="d287c-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="d287c-133">sim</span><span class="sxs-lookup"><span data-stu-id="d287c-133">yes</span></span>       |
| [<span data-ttu-id="d287c-134">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d287c-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="d287c-135">não</span><span class="sxs-lookup"><span data-stu-id="d287c-135">no</span></span>        |
| [<span data-ttu-id="d287c-136">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d287c-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="d287c-137">não</span><span class="sxs-lookup"><span data-stu-id="d287c-137">no</span></span>        |
| [<span data-ttu-id="d287c-138">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d287c-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="d287c-139">não</span><span class="sxs-lookup"><span data-stu-id="d287c-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="d287c-140">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d287c-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d287c-141">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d287c-141">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





