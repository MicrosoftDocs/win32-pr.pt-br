---
title: ISHR (sm4-ASM)
description: Deslocamento aritmético à direita (extensão de assinatura). | ISHR (sm4-ASM)
ms.assetid: AFE46BBA-A6B2-4691-A3F4-A4141F1578DB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7516543c5501ed886c5c1fa98d093062e3099a0f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104989248"
---
# <a name="ishr-sm4---asm"></a><span data-ttu-id="30d2b-104">ISHR (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="30d2b-104">ishr (sm4 - asm)</span></span>

<span data-ttu-id="30d2b-105">Deslocamento aritmético à direita (extensão de assinatura).</span><span class="sxs-lookup"><span data-stu-id="30d2b-105">Arithmetic shift right (sign extending).</span></span>



| <span data-ttu-id="30d2b-106">ISHR dest \[ . Mask \] , src0 \[ . swizzle \] , o componente src1. Select \_</span><span class="sxs-lookup"><span data-stu-id="30d2b-106">ishr dest\[.mask\], src0\[.swizzle\], src1.select\_component</span></span> |
|--------------------------------------------------------------|



 



| <span data-ttu-id="30d2b-107">Item</span><span class="sxs-lookup"><span data-stu-id="30d2b-107">Item</span></span>                                                            | <span data-ttu-id="30d2b-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="30d2b-108">Description</span></span>                                             |
|-----------------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="30d2b-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="30d2b-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="30d2b-110">\[in \] contém o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="30d2b-110">\[in\] Contains the result of the operation.</span></span><br/> |
| <span data-ttu-id="30d2b-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="30d2b-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="30d2b-112">\[in \] contém o valor a ser deslocado.</span><span class="sxs-lookup"><span data-stu-id="30d2b-112">\[in\] Contains the value to be shifted.</span></span><br/>     |
| <span data-ttu-id="30d2b-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="30d2b-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="30d2b-114">\[in \] contém o valor de deslocamento.</span><span class="sxs-lookup"><span data-stu-id="30d2b-114">\[in\] Contains the shift amount.</span></span><br/>            |



 

## <a name="remarks"></a><span data-ttu-id="30d2b-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="30d2b-115">Remarks</span></span>

<span data-ttu-id="30d2b-116">Essa instrução executa uma mudança aritmética de componente de cada valor de 32 bits em *src0* à direita por um número de bits de inteiro sem sinal fornecido pelo LSB de 5 bits (0-31 intervalo) no *\_ componente src1. Select*, replicando o valor do bit 31.</span><span class="sxs-lookup"><span data-stu-id="30d2b-116">This instruction performs a component-wise arithmetic shift of each 32-bit value in *src0* right by an unsigned integer bit count provided by the LSB 5 bits (0-31 range) in *src1.select\_component*, replicating the value of bit 31.</span></span> <span data-ttu-id="30d2b-117">O resultado de 32 bits por componente é colocado no *dest*.</span><span class="sxs-lookup"><span data-stu-id="30d2b-117">The 32-bit per component result is placed in *dest*.</span></span> <span data-ttu-id="30d2b-118">A contagem é um valor escalar aplicado a todos os componentes.</span><span class="sxs-lookup"><span data-stu-id="30d2b-118">The count is a scalar value applied to all components.</span></span>

<span data-ttu-id="30d2b-119">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="30d2b-119">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="30d2b-120">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="30d2b-120">Vertex Shader</span></span> | <span data-ttu-id="30d2b-121">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="30d2b-121">Geometry Shader</span></span> | <span data-ttu-id="30d2b-122">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="30d2b-122">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="30d2b-123">x</span><span class="sxs-lookup"><span data-stu-id="30d2b-123">x</span></span>             | <span data-ttu-id="30d2b-124">x</span><span class="sxs-lookup"><span data-stu-id="30d2b-124">x</span></span>               | <span data-ttu-id="30d2b-125">x</span><span class="sxs-lookup"><span data-stu-id="30d2b-125">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="30d2b-126">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="30d2b-126">Minimum Shader Model</span></span>

<span data-ttu-id="30d2b-127">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="30d2b-127">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="30d2b-128">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="30d2b-128">Shader Model</span></span>                                              | <span data-ttu-id="30d2b-129">Com suporte</span><span class="sxs-lookup"><span data-stu-id="30d2b-129">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="30d2b-130">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="30d2b-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="30d2b-131">sim</span><span class="sxs-lookup"><span data-stu-id="30d2b-131">yes</span></span>       |
| [<span data-ttu-id="30d2b-132">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="30d2b-132">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="30d2b-133">sim</span><span class="sxs-lookup"><span data-stu-id="30d2b-133">yes</span></span>       |
| [<span data-ttu-id="30d2b-134">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="30d2b-134">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="30d2b-135">sim</span><span class="sxs-lookup"><span data-stu-id="30d2b-135">yes</span></span>       |
| [<span data-ttu-id="30d2b-136">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="30d2b-136">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="30d2b-137">não</span><span class="sxs-lookup"><span data-stu-id="30d2b-137">no</span></span>        |
| [<span data-ttu-id="30d2b-138">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="30d2b-138">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="30d2b-139">não</span><span class="sxs-lookup"><span data-stu-id="30d2b-139">no</span></span>        |
| [<span data-ttu-id="30d2b-140">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="30d2b-140">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="30d2b-141">não</span><span class="sxs-lookup"><span data-stu-id="30d2b-141">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="30d2b-142">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="30d2b-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="30d2b-143">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="30d2b-143">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





