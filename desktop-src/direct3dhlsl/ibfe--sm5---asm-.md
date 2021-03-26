---
title: IBFE (SM5-ASM)
description: Dado um intervalo de bits em um número, mude esses bits para o LSB e assine a extensão do MSB do intervalo.
ms.assetid: 1ED39812-A89F-4325-82A0-DA2CCC55A99A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 805d5c1137e25d8b8fa560588b9e876ccc5c8748
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103638858"
---
# <a name="ibfe-sm5---asm"></a><span data-ttu-id="b56d1-103">IBFE (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="b56d1-103">ibfe (sm5 - asm)</span></span>

<span data-ttu-id="b56d1-104">Dado um intervalo de bits em um número, mude esses bits para o LSB e assine a extensão do MSB do intervalo.</span><span class="sxs-lookup"><span data-stu-id="b56d1-104">Given a range of bits in a number, shift those bits to the LSB and sign extend the MSB of the range.</span></span>



| <span data-ttu-id="b56d1-105">IBFE dest \[ . Mask \] , src0 \[ . swizzle \] , src1 \[ . swizzle \] , src2 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="b56d1-105">ibfe dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\], src2\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------|



 



| <span data-ttu-id="b56d1-106">Item</span><span class="sxs-lookup"><span data-stu-id="b56d1-106">Item</span></span>                                                            | <span data-ttu-id="b56d1-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="b56d1-107">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="b56d1-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="b56d1-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="b56d1-109">\[no \] endereço dos resultados da operação.</span><span class="sxs-lookup"><span data-stu-id="b56d1-109">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="b56d1-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="b56d1-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="b56d1-111">\[na \] largura do campo de bits.</span><span class="sxs-lookup"><span data-stu-id="b56d1-111">\[in\] The bitfield width.</span></span><br/>                          |
| <span data-ttu-id="b56d1-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="b56d1-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="b56d1-113">\[no \] deslocamento de campo de bits.</span><span class="sxs-lookup"><span data-stu-id="b56d1-113">\[in\] The bitfield offset.</span></span><br/>                         |
| <span data-ttu-id="b56d1-114"><span id="src2"></span><span id="SRC2"></span>*src2*</span><span class="sxs-lookup"><span data-stu-id="b56d1-114"><span id="src2"></span><span id="SRC2"></span>*src2*</span></span><br/> | <span data-ttu-id="b56d1-115">\[no \] valor a ser deslocado.</span><span class="sxs-lookup"><span data-stu-id="b56d1-115">\[in\] The value to shift.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="b56d1-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="b56d1-116">Remarks</span></span>

<span data-ttu-id="b56d1-117">Os LSB 5 bits de src0 fornecem a largura do campo de bits (0-31).</span><span class="sxs-lookup"><span data-stu-id="b56d1-117">The LSB 5 bits of src0 provide the bitfield width (0-31).</span></span>

<span data-ttu-id="b56d1-118">Os LSB 5 bits de src1 fornecem o deslocamento de campo de bits (0-31).</span><span class="sxs-lookup"><span data-stu-id="b56d1-118">The LSB 5 bits of src1 provide the bitfield offset (0-31).</span></span>

<span data-ttu-id="b56d1-119">O exemplo a seguir mostra como usar essa instrução.</span><span class="sxs-lookup"><span data-stu-id="b56d1-119">The following example shows how to use this instruction.</span></span>

``` syntax
        Given width, offset:
                if( width == 0 )
                {
                    dest = 0
                }
                else if( width + offset < 32 )
                {
                    shl dest, src2, 32-(width+offset)
                    ishr dest, dest, 32-width
                }
                else
                {
                    ishr dest, src2, offset
                }
```

<span data-ttu-id="b56d1-120">Use esta instrução para desempacotar os inteiros ou sinalizadores assinados.</span><span class="sxs-lookup"><span data-stu-id="b56d1-120">Use this instruction to unpack signed integers or flags.</span></span>

<span data-ttu-id="b56d1-121">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="b56d1-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="b56d1-122">Vértice</span><span class="sxs-lookup"><span data-stu-id="b56d1-122">Vertex</span></span> | <span data-ttu-id="b56d1-123">Envoltória</span><span class="sxs-lookup"><span data-stu-id="b56d1-123">Hull</span></span> | <span data-ttu-id="b56d1-124">Domínio</span><span class="sxs-lookup"><span data-stu-id="b56d1-124">Domain</span></span> | <span data-ttu-id="b56d1-125">Geometria</span><span class="sxs-lookup"><span data-stu-id="b56d1-125">Geometry</span></span> | <span data-ttu-id="b56d1-126">16x16</span><span class="sxs-lookup"><span data-stu-id="b56d1-126">Pixel</span></span> | <span data-ttu-id="b56d1-127">Computação</span><span class="sxs-lookup"><span data-stu-id="b56d1-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="b56d1-128">X</span><span class="sxs-lookup"><span data-stu-id="b56d1-128">X</span></span>      | <span data-ttu-id="b56d1-129">X</span><span class="sxs-lookup"><span data-stu-id="b56d1-129">X</span></span>    | <span data-ttu-id="b56d1-130">X</span><span class="sxs-lookup"><span data-stu-id="b56d1-130">X</span></span>      | <span data-ttu-id="b56d1-131">X</span><span class="sxs-lookup"><span data-stu-id="b56d1-131">X</span></span>        | <span data-ttu-id="b56d1-132">X</span><span class="sxs-lookup"><span data-stu-id="b56d1-132">X</span></span>     | <span data-ttu-id="b56d1-133">X</span><span class="sxs-lookup"><span data-stu-id="b56d1-133">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="b56d1-134">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="b56d1-134">Minimum Shader Model</span></span>

<span data-ttu-id="b56d1-135">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="b56d1-135">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="b56d1-136">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="b56d1-136">Shader Model</span></span>                                              | <span data-ttu-id="b56d1-137">Com suporte</span><span class="sxs-lookup"><span data-stu-id="b56d1-137">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="b56d1-138">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="b56d1-138">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="b56d1-139">sim</span><span class="sxs-lookup"><span data-stu-id="b56d1-139">yes</span></span>       |
| [<span data-ttu-id="b56d1-140">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="b56d1-140">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="b56d1-141">não</span><span class="sxs-lookup"><span data-stu-id="b56d1-141">no</span></span>        |
| [<span data-ttu-id="b56d1-142">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="b56d1-142">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="b56d1-143">não</span><span class="sxs-lookup"><span data-stu-id="b56d1-143">no</span></span>        |
| [<span data-ttu-id="b56d1-144">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b56d1-144">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="b56d1-145">não</span><span class="sxs-lookup"><span data-stu-id="b56d1-145">no</span></span>        |
| [<span data-ttu-id="b56d1-146">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b56d1-146">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="b56d1-147">não</span><span class="sxs-lookup"><span data-stu-id="b56d1-147">no</span></span>        |
| [<span data-ttu-id="b56d1-148">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b56d1-148">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="b56d1-149">não</span><span class="sxs-lookup"><span data-stu-id="b56d1-149">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="b56d1-150">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b56d1-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b56d1-151">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b56d1-151">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





