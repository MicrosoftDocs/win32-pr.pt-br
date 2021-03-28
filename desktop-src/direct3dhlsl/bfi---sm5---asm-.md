---
title: BFI (SM5-ASM)
description: Dado um intervalo de bits do LSB de um número, coloque esse número de bits em outro número em qualquer deslocamento.
ms.assetid: BA84C882-A141-4AD2-8FD9-C60F1483FC65
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a14f8b9f6ef126ec3c6a31bf330dfd89cf0770c4
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104006902"
---
# <a name="bfi-sm5---asm"></a><span data-ttu-id="6c236-103">BFI (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="6c236-103">bfi (sm5 - asm)</span></span>

<span data-ttu-id="6c236-104">Dado um intervalo de bits do LSB de um número, coloque esse número de bits em outro número em qualquer deslocamento.</span><span class="sxs-lookup"><span data-stu-id="6c236-104">Given a bit range from the LSB of a number, place that number of bits in another number at any offset.</span></span>



| <span data-ttu-id="6c236-105">BFI dest \[ . Mask \] , src0 \[ . swizzle \] , src1 \[ . swizzle \] , src2 \[ . swizzle \] , src3 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="6c236-105">bfi dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\], src2\[.swizzle\], src3\[.swizzle\]</span></span> |
|-------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="6c236-106">Item</span><span class="sxs-lookup"><span data-stu-id="6c236-106">Item</span></span>                                                            | <span data-ttu-id="6c236-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="6c236-107">Description</span></span>                                                         |
|-----------------------------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="6c236-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="6c236-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="6c236-109">\[no \] endereço dos resultados.</span><span class="sxs-lookup"><span data-stu-id="6c236-109">\[in\] The address of the results.</span></span><br/>                       |
| <span data-ttu-id="6c236-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="6c236-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="6c236-111">\[na largura do campo de \] bits a ser tomada de *src2*.</span><span class="sxs-lookup"><span data-stu-id="6c236-111">\[in\] The bitfield width to take from *src2*.</span></span><br/>           |
| <span data-ttu-id="6c236-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="6c236-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="6c236-113">\[no \] deslocamento de campo de bits para substituição de partes em *src3*.</span><span class="sxs-lookup"><span data-stu-id="6c236-113">\[in\] The bitfield offset for replacing bits in *src3*.</span></span><br/> |
| <span data-ttu-id="6c236-114"><span id="src2"></span><span id="SRC2"></span>*src2*</span><span class="sxs-lookup"><span data-stu-id="6c236-114"><span id="src2"></span><span id="SRC2"></span>*src2*</span></span><br/> | <span data-ttu-id="6c236-115">\[no \] número do qual os bits são tirados.</span><span class="sxs-lookup"><span data-stu-id="6c236-115">\[in\] The number the bits are taken from.</span></span> <br/>              |
| <span data-ttu-id="6c236-116"><span id="src3"></span><span id="SRC3"></span>*src3*</span><span class="sxs-lookup"><span data-stu-id="6c236-116"><span id="src3"></span><span id="SRC3"></span>*src3*</span></span><br/> | <span data-ttu-id="6c236-117">\[no \] número com bits a serem substituídos.</span><span class="sxs-lookup"><span data-stu-id="6c236-117">\[in\] The number with bits to be replaced.</span></span><br/>              |



 

## <a name="remarks"></a><span data-ttu-id="6c236-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="6c236-118">Remarks</span></span>

<span data-ttu-id="6c236-119">Os LSB 5 bits de *src0* fornecem a largura do campo de bits (0-31) a ser tomada em *src2*.</span><span class="sxs-lookup"><span data-stu-id="6c236-119">The LSB 5 bits of *src0* provide the bitfield width (0-31) to take from *src2*.</span></span>

<span data-ttu-id="6c236-120">Os LSB 5 bits de *src1* fornecem o deslocamento de campo de bits (0-31) para iniciar a substituição de bit no número lido de *src3*.</span><span class="sxs-lookup"><span data-stu-id="6c236-120">The LSB 5 bits of *src1* provide the bitfield offset (0-31) to start replacing bits in the number read from *src3*.</span></span>

``` syntax
Given width, offset:
                bitmask = (((1 << width)-1) << offset) & 0xffffffff
                dest = ((src2 << offset) & bitmask) | (src3 & ~bitmask)
```

<span data-ttu-id="6c236-121">Essa instrução é usada para empacotar inteiros ou sinalizadores.</span><span class="sxs-lookup"><span data-stu-id="6c236-121">This instruction is used for packing integers or flags.</span></span>

<span data-ttu-id="6c236-122">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="6c236-122">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="6c236-123">Vértice</span><span class="sxs-lookup"><span data-stu-id="6c236-123">Vertex</span></span> | <span data-ttu-id="6c236-124">Envoltória</span><span class="sxs-lookup"><span data-stu-id="6c236-124">Hull</span></span> | <span data-ttu-id="6c236-125">Domínio</span><span class="sxs-lookup"><span data-stu-id="6c236-125">Domain</span></span> | <span data-ttu-id="6c236-126">Geometria</span><span class="sxs-lookup"><span data-stu-id="6c236-126">Geometry</span></span> | <span data-ttu-id="6c236-127">16x16</span><span class="sxs-lookup"><span data-stu-id="6c236-127">Pixel</span></span> | <span data-ttu-id="6c236-128">Computação</span><span class="sxs-lookup"><span data-stu-id="6c236-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="6c236-129">X</span><span class="sxs-lookup"><span data-stu-id="6c236-129">X</span></span>      | <span data-ttu-id="6c236-130">X</span><span class="sxs-lookup"><span data-stu-id="6c236-130">X</span></span>    | <span data-ttu-id="6c236-131">X</span><span class="sxs-lookup"><span data-stu-id="6c236-131">X</span></span>      | <span data-ttu-id="6c236-132">X</span><span class="sxs-lookup"><span data-stu-id="6c236-132">X</span></span>        | <span data-ttu-id="6c236-133">X</span><span class="sxs-lookup"><span data-stu-id="6c236-133">X</span></span>     | <span data-ttu-id="6c236-134">X</span><span class="sxs-lookup"><span data-stu-id="6c236-134">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="6c236-135">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="6c236-135">Minimum Shader Model</span></span>

<span data-ttu-id="6c236-136">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="6c236-136">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="6c236-137">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="6c236-137">Shader Model</span></span>                                              | <span data-ttu-id="6c236-138">Com suporte</span><span class="sxs-lookup"><span data-stu-id="6c236-138">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="6c236-139">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="6c236-139">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="6c236-140">sim</span><span class="sxs-lookup"><span data-stu-id="6c236-140">yes</span></span>       |
| [<span data-ttu-id="6c236-141">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="6c236-141">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="6c236-142">não</span><span class="sxs-lookup"><span data-stu-id="6c236-142">no</span></span>        |
| [<span data-ttu-id="6c236-143">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="6c236-143">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="6c236-144">não</span><span class="sxs-lookup"><span data-stu-id="6c236-144">no</span></span>        |
| [<span data-ttu-id="6c236-145">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6c236-145">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="6c236-146">não</span><span class="sxs-lookup"><span data-stu-id="6c236-146">no</span></span>        |
| [<span data-ttu-id="6c236-147">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6c236-147">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="6c236-148">não</span><span class="sxs-lookup"><span data-stu-id="6c236-148">no</span></span>        |
| [<span data-ttu-id="6c236-149">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6c236-149">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="6c236-150">não</span><span class="sxs-lookup"><span data-stu-id="6c236-150">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="6c236-151">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6c236-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6c236-152">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6c236-152">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





