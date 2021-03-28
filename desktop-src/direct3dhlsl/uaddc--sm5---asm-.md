---
title: uaddc (SM5-ASM)
description: Adição de inteiro sem sinal com transporte.
ms.assetid: 1007253C-F920-4003-B266-D124A255F731
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f57f75be617e32c15212207110851520a7a281e2
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104498942"
---
# <a name="uaddc-sm5---asm"></a><span data-ttu-id="83bfb-103">uaddc (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="83bfb-103">uaddc (sm5 - asm)</span></span>

<span data-ttu-id="83bfb-104">Adição de inteiro sem sinal com transporte.</span><span class="sxs-lookup"><span data-stu-id="83bfb-104">Unsigned integer add with carry.</span></span>



| <span data-ttu-id="83bfb-105">uaddc dest0 \[ . Mask \] , dest1 \[ . Mask \] , src0 \[ . swizzle \] , src1 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="83bfb-105">uaddc dest0\[.mask\], dest1\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------|



 



| <span data-ttu-id="83bfb-106">Item</span><span class="sxs-lookup"><span data-stu-id="83bfb-106">Item</span></span>                                                               | <span data-ttu-id="83bfb-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="83bfb-107">Description</span></span>                                            |
|--------------------------------------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="83bfb-108"><span id="dest0"></span><span id="DEST0"></span>*dest0*</span><span class="sxs-lookup"><span data-stu-id="83bfb-108"><span id="dest0"></span><span id="DEST0"></span>*dest0*</span></span><br/> | <span data-ttu-id="83bfb-109">\[em \] endereço do resultado.</span><span class="sxs-lookup"><span data-stu-id="83bfb-109">\[in\] Address of the result.</span></span><br/>               |
| <span data-ttu-id="83bfb-110"><span id="dest1"></span><span id="DEST1"></span>*dest1*</span><span class="sxs-lookup"><span data-stu-id="83bfb-110"><span id="dest1"></span><span id="DEST1"></span>*dest1*</span></span><br/> | <span data-ttu-id="83bfb-111">\[em \] 1, se a execução for produzida.</span><span class="sxs-lookup"><span data-stu-id="83bfb-111">\[in\] 1 if carry is produced.</span></span> <span data-ttu-id="83bfb-112">Caso contrário, 0.</span><span class="sxs-lookup"><span data-stu-id="83bfb-112">Otherwise 0.</span></span><br/> |
| <span data-ttu-id="83bfb-113"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="83bfb-113"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>    | <span data-ttu-id="83bfb-114">\[no \] operando de 32 bits a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="83bfb-114">\[in\] 32-bit operand to be added.</span></span><br/>          |
| <span data-ttu-id="83bfb-115"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="83bfb-115"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/>    | <span data-ttu-id="83bfb-116">\[no \] operando de 32 bits a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="83bfb-116">\[in\] 32-bit operand to be added.</span></span><br/>          |



 

## <a name="remarks"></a><span data-ttu-id="83bfb-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="83bfb-117">Remarks</span></span>

<span data-ttu-id="83bfb-118">*dest1* pode ser nulo se o transporte não for necessário.</span><span class="sxs-lookup"><span data-stu-id="83bfb-118">*dest1* can be NULL if the carry is not needed.</span></span>

<span data-ttu-id="83bfb-119">Use esta instrução para aritmética de alta precisão.</span><span class="sxs-lookup"><span data-stu-id="83bfb-119">Use this instruction for high precision arithmetic.</span></span>

<span data-ttu-id="83bfb-120">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="83bfb-120">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="83bfb-121">Vértice</span><span class="sxs-lookup"><span data-stu-id="83bfb-121">Vertex</span></span> | <span data-ttu-id="83bfb-122">Envoltória</span><span class="sxs-lookup"><span data-stu-id="83bfb-122">Hull</span></span> | <span data-ttu-id="83bfb-123">Domínio</span><span class="sxs-lookup"><span data-stu-id="83bfb-123">Domain</span></span> | <span data-ttu-id="83bfb-124">Geometria</span><span class="sxs-lookup"><span data-stu-id="83bfb-124">Geometry</span></span> | <span data-ttu-id="83bfb-125">16x16</span><span class="sxs-lookup"><span data-stu-id="83bfb-125">Pixel</span></span> | <span data-ttu-id="83bfb-126">Computação</span><span class="sxs-lookup"><span data-stu-id="83bfb-126">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="83bfb-127">X</span><span class="sxs-lookup"><span data-stu-id="83bfb-127">X</span></span>      | <span data-ttu-id="83bfb-128">X</span><span class="sxs-lookup"><span data-stu-id="83bfb-128">X</span></span>    | <span data-ttu-id="83bfb-129">X</span><span class="sxs-lookup"><span data-stu-id="83bfb-129">X</span></span>      | <span data-ttu-id="83bfb-130">X</span><span class="sxs-lookup"><span data-stu-id="83bfb-130">X</span></span>        | <span data-ttu-id="83bfb-131">X</span><span class="sxs-lookup"><span data-stu-id="83bfb-131">X</span></span>     | <span data-ttu-id="83bfb-132">X</span><span class="sxs-lookup"><span data-stu-id="83bfb-132">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="83bfb-133">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="83bfb-133">Minimum Shader Model</span></span>

<span data-ttu-id="83bfb-134">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="83bfb-134">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="83bfb-135">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="83bfb-135">Shader Model</span></span>                                              | <span data-ttu-id="83bfb-136">Com suporte</span><span class="sxs-lookup"><span data-stu-id="83bfb-136">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="83bfb-137">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="83bfb-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="83bfb-138">sim</span><span class="sxs-lookup"><span data-stu-id="83bfb-138">yes</span></span>       |
| [<span data-ttu-id="83bfb-139">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="83bfb-139">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="83bfb-140">não</span><span class="sxs-lookup"><span data-stu-id="83bfb-140">no</span></span>        |
| [<span data-ttu-id="83bfb-141">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="83bfb-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="83bfb-142">não</span><span class="sxs-lookup"><span data-stu-id="83bfb-142">no</span></span>        |
| [<span data-ttu-id="83bfb-143">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="83bfb-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="83bfb-144">não</span><span class="sxs-lookup"><span data-stu-id="83bfb-144">no</span></span>        |
| [<span data-ttu-id="83bfb-145">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="83bfb-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="83bfb-146">não</span><span class="sxs-lookup"><span data-stu-id="83bfb-146">no</span></span>        |
| [<span data-ttu-id="83bfb-147">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="83bfb-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="83bfb-148">não</span><span class="sxs-lookup"><span data-stu-id="83bfb-148">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="83bfb-149">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="83bfb-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83bfb-150">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="83bfb-150">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





