---
title: ubfe (SM5-ASM)
description: Dado um intervalo de bits em um número, mude esses bits para o LSB e defina os bits restantes como 0.
ms.assetid: CC6BE378-2726-47A2-8E23-B8151521F72D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43ebbe853ec1b53b452f32d79c9c2ec120e826b8
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103823446"
---
# <a name="ubfe-sm5---asm"></a><span data-ttu-id="c3859-103">ubfe (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="c3859-103">ubfe (sm5 - asm)</span></span>

<span data-ttu-id="c3859-104">Dado um intervalo de bits em um número, mude esses bits para o LSB e defina os bits restantes como 0.</span><span class="sxs-lookup"><span data-stu-id="c3859-104">Given a range of bits in a number, shift those bits to the LSB and set remaining bits to 0.</span></span>



| <span data-ttu-id="c3859-105">ubfe dest \[ . Mask \] , src0 \[ . swizzle \] , src1 \[ . swizzle \] , src2 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="c3859-105">ubfe dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\], src2\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------|



 



| <span data-ttu-id="c3859-106">Item</span><span class="sxs-lookup"><span data-stu-id="c3859-106">Item</span></span>                                                            | <span data-ttu-id="c3859-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="c3859-107">Description</span></span>                                                                    |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="c3859-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="c3859-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="c3859-109">\[in \] contém os resultados da instrução.</span><span class="sxs-lookup"><span data-stu-id="c3859-109">\[in\] Contains the results of the instruction.</span></span><br/>                     |
| <span data-ttu-id="c3859-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="c3859-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="c3859-111">\[nos \] LSB de 5 bits fornecem a largura do campo de bits (0-31).</span><span class="sxs-lookup"><span data-stu-id="c3859-111">\[in\] The LSB 5 bits provide the bitfield width (0-31).</span></span><br/>            |
| <span data-ttu-id="c3859-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="c3859-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="c3859-113">\[nos \] LSB 5 bits de *src1* fornecem o deslocamento de campo de bits (0-31).</span><span class="sxs-lookup"><span data-stu-id="c3859-113">\[in\] The LSB 5 bits of *src1* provide the bitfield offset (0-31).</span></span><br/> |
| <span data-ttu-id="c3859-114"><span id="src2"></span><span id="SRC2"></span>*src2*</span><span class="sxs-lookup"><span data-stu-id="c3859-114"><span id="src2"></span><span id="SRC2"></span>*src2*</span></span><br/> | <span data-ttu-id="c3859-115">\[no \] número a ser deslocado.</span><span class="sxs-lookup"><span data-stu-id="c3859-115">\[in\] The number to shift.</span></span><br/>                                         |



 

## <a name="remarks"></a><span data-ttu-id="c3859-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="c3859-116">Remarks</span></span>

``` syntax
 
        Given width, offset:
                if( width == 0 )
                {
                    dest = 0
                }
                else if( width + offset < 32 )
                {
                    shl dest, src2, 32-(width+offset)
                    ushr dest, dest, 32-width
                }
                else
                {
                    ushr dest, src2, offset
                }
```

<span data-ttu-id="c3859-117">Use esta instrução para desempacotar os números inteiros ou sinalizadores não assinados.</span><span class="sxs-lookup"><span data-stu-id="c3859-117">Use this instruction to unpack unsigned integers or flags.</span></span>

<span data-ttu-id="c3859-118">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="c3859-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="c3859-119">Vértice</span><span class="sxs-lookup"><span data-stu-id="c3859-119">Vertex</span></span> | <span data-ttu-id="c3859-120">Envoltória</span><span class="sxs-lookup"><span data-stu-id="c3859-120">Hull</span></span> | <span data-ttu-id="c3859-121">Domínio</span><span class="sxs-lookup"><span data-stu-id="c3859-121">Domain</span></span> | <span data-ttu-id="c3859-122">Geometria</span><span class="sxs-lookup"><span data-stu-id="c3859-122">Geometry</span></span> | <span data-ttu-id="c3859-123">16x16</span><span class="sxs-lookup"><span data-stu-id="c3859-123">Pixel</span></span> | <span data-ttu-id="c3859-124">Computação</span><span class="sxs-lookup"><span data-stu-id="c3859-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="c3859-125">X</span><span class="sxs-lookup"><span data-stu-id="c3859-125">X</span></span>      | <span data-ttu-id="c3859-126">X</span><span class="sxs-lookup"><span data-stu-id="c3859-126">X</span></span>    | <span data-ttu-id="c3859-127">X</span><span class="sxs-lookup"><span data-stu-id="c3859-127">X</span></span>      | <span data-ttu-id="c3859-128">X</span><span class="sxs-lookup"><span data-stu-id="c3859-128">X</span></span>        | <span data-ttu-id="c3859-129">X</span><span class="sxs-lookup"><span data-stu-id="c3859-129">X</span></span>     | <span data-ttu-id="c3859-130">X</span><span class="sxs-lookup"><span data-stu-id="c3859-130">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="c3859-131">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="c3859-131">Minimum Shader Model</span></span>

<span data-ttu-id="c3859-132">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="c3859-132">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="c3859-133">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="c3859-133">Shader Model</span></span>                                              | <span data-ttu-id="c3859-134">Com suporte</span><span class="sxs-lookup"><span data-stu-id="c3859-134">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="c3859-135">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="c3859-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="c3859-136">sim</span><span class="sxs-lookup"><span data-stu-id="c3859-136">yes</span></span>       |
| [<span data-ttu-id="c3859-137">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="c3859-137">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="c3859-138">não</span><span class="sxs-lookup"><span data-stu-id="c3859-138">no</span></span>        |
| [<span data-ttu-id="c3859-139">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="c3859-139">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="c3859-140">não</span><span class="sxs-lookup"><span data-stu-id="c3859-140">no</span></span>        |
| [<span data-ttu-id="c3859-141">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c3859-141">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="c3859-142">não</span><span class="sxs-lookup"><span data-stu-id="c3859-142">no</span></span>        |
| [<span data-ttu-id="c3859-143">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c3859-143">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="c3859-144">não</span><span class="sxs-lookup"><span data-stu-id="c3859-144">no</span></span>        |
| [<span data-ttu-id="c3859-145">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c3859-145">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="c3859-146">não</span><span class="sxs-lookup"><span data-stu-id="c3859-146">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="c3859-147">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c3859-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c3859-148">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c3859-148">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





