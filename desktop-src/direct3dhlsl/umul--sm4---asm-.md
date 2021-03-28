---
title: umul (sm4-ASM)
description: Multiplicação de inteiro sem sinal.
ms.assetid: C84AF349-32E6-40C4-9973-BCFA73EFBF0B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 581696ef5aa7d027c30b4ae866d06401275ef4bc
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104365227"
---
# <a name="umul-sm4---asm"></a><span data-ttu-id="8d1f1-103">umul (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="8d1f1-103">umul (sm4 - asm)</span></span>

<span data-ttu-id="8d1f1-104">Multiplicação de inteiro sem sinal.</span><span class="sxs-lookup"><span data-stu-id="8d1f1-104">Unsigned integer multiply.</span></span>



| <span data-ttu-id="8d1f1-105">umul destHI \[ . Mask \] , destLO \[ . Mask \] , src0 \[ . swizzle \] , src1 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="8d1f1-105">umul destHI\[.mask\], destLO\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|---------------------------------------------------------------------------|



 



| <span data-ttu-id="8d1f1-106">Item</span><span class="sxs-lookup"><span data-stu-id="8d1f1-106">Item</span></span>                                                                                           | <span data-ttu-id="8d1f1-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="8d1f1-107">Description</span></span>                                                      |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span data-ttu-id="8d1f1-108"><span id="destHI"></span><span id="desthi"></span><span id="DESTHI"></span>*destHI*</span><span class="sxs-lookup"><span data-stu-id="8d1f1-108"><span id="destHI"></span><span id="desthi"></span><span id="DESTHI"></span>*destHI*</span></span><br/> | <span data-ttu-id="8d1f1-109">\[nos \] altos 32 bits do resultado, por componente.</span><span class="sxs-lookup"><span data-stu-id="8d1f1-109">\[in\] The high 32 bits of the result, per component.</span></span><br/> |
| <span data-ttu-id="8d1f1-110"><span id="destLO"></span><span id="destlo"></span><span id="DESTLO"></span>*destLO*</span><span class="sxs-lookup"><span data-stu-id="8d1f1-110"><span id="destLO"></span><span id="destlo"></span><span id="DESTLO"></span>*destLO*</span></span><br/> | <span data-ttu-id="8d1f1-111">\[nos \] poucos 32 bits do resultado, por componente.</span><span class="sxs-lookup"><span data-stu-id="8d1f1-111">\[in\] The low 32 bits of the result, per component.</span></span><br/>  |
| <span data-ttu-id="8d1f1-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="8d1f1-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                | <span data-ttu-id="8d1f1-113">\[nos \] componentes pelos quais multiplicar *src1*.</span><span class="sxs-lookup"><span data-stu-id="8d1f1-113">\[in\] The components by which to multiply *src1*.</span></span><br/>    |
| <span data-ttu-id="8d1f1-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="8d1f1-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/>                                | <span data-ttu-id="8d1f1-115">\[nos \] componentes pelos quais multiplicar *src0*.</span><span class="sxs-lookup"><span data-stu-id="8d1f1-115">\[in\] The components by which to multiply *src0*.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="8d1f1-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="8d1f1-116">Remarks</span></span>

<span data-ttu-id="8d1f1-117">Essa instrução executa uma multiplicação por componente de operandos de 32 bits não assinados *src0* e *src1*, produzindo o resultado de 64 de bits completo correto por componente.</span><span class="sxs-lookup"><span data-stu-id="8d1f1-117">This instruction performs a component-wise multiply of unsigned 32-bit operands *src0* and *src1*, producing the correct full 64-bit result per component.</span></span> <span data-ttu-id="8d1f1-118">Os baixos 32 bits por componente são colocados em *destLO*.</span><span class="sxs-lookup"><span data-stu-id="8d1f1-118">The low 32 bits per component are placed in *destLO*.</span></span> <span data-ttu-id="8d1f1-119">Os bits de 32 altos por componente são colocados em *destHI*.</span><span class="sxs-lookup"><span data-stu-id="8d1f1-119">The high 32 bits per component are placed in *destHI*.</span></span>

<span data-ttu-id="8d1f1-120">Você pode especificar *destHI* ou *destLO* como NULL em vez de especificar um registro se os bits de 32 altos ou baixos do resultado de 64 bits não forem necessários.</span><span class="sxs-lookup"><span data-stu-id="8d1f1-120">You can specify either *destHI* or *destLO* as NULL instead of specifying a register if the high or low 32 bits of the 64-bit result are not needed.</span></span>

<span data-ttu-id="8d1f1-121">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="8d1f1-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="8d1f1-122">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="8d1f1-122">Vertex Shader</span></span> | <span data-ttu-id="8d1f1-123">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="8d1f1-123">Geometry Shader</span></span> | <span data-ttu-id="8d1f1-124">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="8d1f1-124">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="8d1f1-125">x</span><span class="sxs-lookup"><span data-stu-id="8d1f1-125">x</span></span>             | <span data-ttu-id="8d1f1-126">x</span><span class="sxs-lookup"><span data-stu-id="8d1f1-126">x</span></span>               | <span data-ttu-id="8d1f1-127">x</span><span class="sxs-lookup"><span data-stu-id="8d1f1-127">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="8d1f1-128">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="8d1f1-128">Minimum Shader Model</span></span>

<span data-ttu-id="8d1f1-129">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="8d1f1-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="8d1f1-130">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="8d1f1-130">Shader Model</span></span>                                              | <span data-ttu-id="8d1f1-131">Com suporte</span><span class="sxs-lookup"><span data-stu-id="8d1f1-131">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="8d1f1-132">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="8d1f1-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="8d1f1-133">sim</span><span class="sxs-lookup"><span data-stu-id="8d1f1-133">yes</span></span>       |
| [<span data-ttu-id="8d1f1-134">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="8d1f1-134">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="8d1f1-135">sim</span><span class="sxs-lookup"><span data-stu-id="8d1f1-135">yes</span></span>       |
| [<span data-ttu-id="8d1f1-136">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="8d1f1-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="8d1f1-137">sim</span><span class="sxs-lookup"><span data-stu-id="8d1f1-137">yes</span></span>       |
| [<span data-ttu-id="8d1f1-138">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8d1f1-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="8d1f1-139">não</span><span class="sxs-lookup"><span data-stu-id="8d1f1-139">no</span></span>        |
| [<span data-ttu-id="8d1f1-140">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8d1f1-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="8d1f1-141">não</span><span class="sxs-lookup"><span data-stu-id="8d1f1-141">no</span></span>        |
| [<span data-ttu-id="8d1f1-142">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8d1f1-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="8d1f1-143">não</span><span class="sxs-lookup"><span data-stu-id="8d1f1-143">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="8d1f1-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8d1f1-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8d1f1-145">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8d1f1-145">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





