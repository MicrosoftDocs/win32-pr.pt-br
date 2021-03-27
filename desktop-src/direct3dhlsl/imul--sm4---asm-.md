---
title: imul (sm4-ASM)
description: Número inteiro com sinal multiplicado.
ms.assetid: DB95A38F-54E4-4BB6-81DF-CFFEBB4D425B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 997f62fc389ad1e0fb6b23dd6c419ff8b3933b41
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103638876"
---
# <a name="imul-sm4---asm"></a><span data-ttu-id="222ae-103">imul (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="222ae-103">imul (sm4 - asm)</span></span>

<span data-ttu-id="222ae-104">Número inteiro com sinal multiplicado.</span><span class="sxs-lookup"><span data-stu-id="222ae-104">Signed integer multiply.</span></span>



| <span data-ttu-id="222ae-105">imul destHI \[ . Mask \] , destLO \[ . Mask \] , \[ - \] src0 \[ . swizzle \] , \[ - \] src1 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="222ae-105">imul destHI\[.mask\], destLO\[.mask\], \[-\]src0\[.swizzle\], \[-\]src1\[.swizzle\]</span></span> |
|-------------------------------------------------------------------------------------|



 



| <span data-ttu-id="222ae-106">Item</span><span class="sxs-lookup"><span data-stu-id="222ae-106">Item</span></span>                                                                                           | <span data-ttu-id="222ae-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="222ae-107">Description</span></span>                                                      |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span data-ttu-id="222ae-108"><span id="destHI"></span><span id="desthi"></span><span id="DESTHI"></span>*destHI*</span><span class="sxs-lookup"><span data-stu-id="222ae-108"><span id="destHI"></span><span id="desthi"></span><span id="DESTHI"></span>*destHI*</span></span><br/> | <span data-ttu-id="222ae-109">\[no \] endereço dos altos 32 bits do resultado.</span><span class="sxs-lookup"><span data-stu-id="222ae-109">\[in\] The address of the high 32 bits of the result.</span></span><br/> |
| <span data-ttu-id="222ae-110"><span id="destLO"></span><span id="destlo"></span><span id="DESTLO"></span>*destLO*</span><span class="sxs-lookup"><span data-stu-id="222ae-110"><span id="destLO"></span><span id="destlo"></span><span id="DESTLO"></span>*destLO*</span></span><br/> | <span data-ttu-id="222ae-111">\[no \] endereço dos baixos 32 bits do resultado.</span><span class="sxs-lookup"><span data-stu-id="222ae-111">\[in\] The address of the low 32 bits of the result.</span></span><br/>  |
| <span data-ttu-id="222ae-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="222ae-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                | <span data-ttu-id="222ae-113">\[no \] valor para multiplicar com *src1*.</span><span class="sxs-lookup"><span data-stu-id="222ae-113">\[in\] The value to multiply with *src1*.</span></span><br/>             |
| <span data-ttu-id="222ae-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="222ae-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/>                                | <span data-ttu-id="222ae-115">\[no \] valor para multiplicar com *src0*.</span><span class="sxs-lookup"><span data-stu-id="222ae-115">\[in\] The value to multiply with *src0*.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="222ae-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="222ae-116">Remarks</span></span>

<span data-ttu-id="222ae-117">A multiplicação por componente dos operandos de 32 bits *src0* e *src1* (ambos são assinados), produzindo o resultado completo de 64 bits (por componente) correto.</span><span class="sxs-lookup"><span data-stu-id="222ae-117">Component-wise multiply of 32-bit operands *src0* and *src1* (both are signed), producing the correct full 64-bit (per component) result.</span></span> <span data-ttu-id="222ae-118">Os bits de 32 baixos (por componente) são colocados em *destLO*.</span><span class="sxs-lookup"><span data-stu-id="222ae-118">The low 32 bits (per component) are placed in *destLO*.</span></span> <span data-ttu-id="222ae-119">Os bits de 32 altos (por componente) são colocados em *destHI*.</span><span class="sxs-lookup"><span data-stu-id="222ae-119">The high 32 bits (per component) are placed in *destHI*.</span></span>

<span data-ttu-id="222ae-120">*DestHI* ou *destLO* pode ser especificado como NULL em vez de especificar um registro, se os bits de 32 altos ou baixos do resultado de 64 bits não forem necessários.</span><span class="sxs-lookup"><span data-stu-id="222ae-120">Either *destHI* or *destLO* may be specified as NULL instead of specifying a register, if the high or low 32 bits of the 64-bit result are not needed.</span></span>

<span data-ttu-id="222ae-121">O modificador opcional Negate nos operandos de origem usa o complemento de 2 antes de executar a operação aritmética.</span><span class="sxs-lookup"><span data-stu-id="222ae-121">Optional negate modifier on source operands takes 2's complement before performing arithmetic operation.</span></span>

<span data-ttu-id="222ae-122">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="222ae-122">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="222ae-123">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="222ae-123">Vertex Shader</span></span> | <span data-ttu-id="222ae-124">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="222ae-124">Geometry Shader</span></span> | <span data-ttu-id="222ae-125">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="222ae-125">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="222ae-126">x</span><span class="sxs-lookup"><span data-stu-id="222ae-126">x</span></span>             | <span data-ttu-id="222ae-127">x</span><span class="sxs-lookup"><span data-stu-id="222ae-127">x</span></span>               | <span data-ttu-id="222ae-128">x</span><span class="sxs-lookup"><span data-stu-id="222ae-128">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="222ae-129">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="222ae-129">Minimum Shader Model</span></span>

<span data-ttu-id="222ae-130">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="222ae-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="222ae-131">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="222ae-131">Shader Model</span></span>                                              | <span data-ttu-id="222ae-132">Com suporte</span><span class="sxs-lookup"><span data-stu-id="222ae-132">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="222ae-133">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="222ae-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="222ae-134">sim</span><span class="sxs-lookup"><span data-stu-id="222ae-134">yes</span></span>       |
| [<span data-ttu-id="222ae-135">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="222ae-135">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="222ae-136">sim</span><span class="sxs-lookup"><span data-stu-id="222ae-136">yes</span></span>       |
| [<span data-ttu-id="222ae-137">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="222ae-137">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="222ae-138">sim</span><span class="sxs-lookup"><span data-stu-id="222ae-138">yes</span></span>       |
| [<span data-ttu-id="222ae-139">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="222ae-139">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="222ae-140">não</span><span class="sxs-lookup"><span data-stu-id="222ae-140">no</span></span>        |
| [<span data-ttu-id="222ae-141">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="222ae-141">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="222ae-142">não</span><span class="sxs-lookup"><span data-stu-id="222ae-142">no</span></span>        |
| [<span data-ttu-id="222ae-143">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="222ae-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="222ae-144">não</span><span class="sxs-lookup"><span data-stu-id="222ae-144">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="222ae-145">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="222ae-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="222ae-146">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="222ae-146">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





