---
title: usubb (SM5-ASM)
description: Subtração de inteiro sem sinal com empréstimo.
ms.assetid: 6D42E3CA-5A37-4194-AB42-7A2337C5AB9D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 111ffd134a75b8cfe19f63597cd80655201359c4
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104365191"
---
# <a name="usubb-sm5---asm"></a><span data-ttu-id="27aef-103">usubb (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="27aef-103">usubb (sm5 - asm)</span></span>

<span data-ttu-id="27aef-104">Subtração de inteiro sem sinal com empréstimo.</span><span class="sxs-lookup"><span data-stu-id="27aef-104">Unsigned integer subtract with borrow.</span></span>



| <span data-ttu-id="27aef-105">usubb dest0 \[ . Mask \] , dest1 \[ . Mask \] , src0 \[ . swizzle \] , src1 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="27aef-105">usubb dest0\[.mask\], dest1\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------|



 



| <span data-ttu-id="27aef-106">Item</span><span class="sxs-lookup"><span data-stu-id="27aef-106">Item</span></span>                                                               | <span data-ttu-id="27aef-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="27aef-107">Description</span></span>                                                                                       |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27aef-108"><span id="dest0"></span><span id="DEST0"></span>*dest0*</span><span class="sxs-lookup"><span data-stu-id="27aef-108"><span id="dest0"></span><span id="DEST0"></span>*dest0*</span></span><br/> | <span data-ttu-id="27aef-109">\[in \] contém os resultados de LSAB da instrução.</span><span class="sxs-lookup"><span data-stu-id="27aef-109">\[in\] Contains the LSAB results of the instruction.</span></span><br/>                                   |
| <span data-ttu-id="27aef-110"><span id="dest1"></span><span id="DEST1"></span>*dest1*</span><span class="sxs-lookup"><span data-stu-id="27aef-110"><span id="dest1"></span><span id="DEST1"></span>*dest1*</span></span><br/> | <span data-ttu-id="27aef-111">\[no \] componente correspondente de *dest0* que especifica se um empréstimo foi produzido.</span><span class="sxs-lookup"><span data-stu-id="27aef-111">\[in\] The corresponding component of *dest0* that specifies if a borrow was produced.</span></span><br/> |
| <span data-ttu-id="27aef-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="27aef-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>    | <span data-ttu-id="27aef-113">\[no \] valor do qual subtrair.</span><span class="sxs-lookup"><span data-stu-id="27aef-113">\[in\] The value from which to subtract.</span></span><br/>                                               |
| <span data-ttu-id="27aef-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="27aef-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/>    | <span data-ttu-id="27aef-115">\[no \] valor a ser subtraído de *src0*.</span><span class="sxs-lookup"><span data-stu-id="27aef-115">\[in\] The amount to subtract from *src0*.</span></span><br/>                                             |



 

## <a name="remarks"></a><span data-ttu-id="27aef-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="27aef-116">Remarks</span></span>

<span data-ttu-id="27aef-117">Essa instrução executa um subtração não assinado por componente de operandos de 32 bits *src1* de *src0*, colocando a parte LSB do resultado de 32 bits em *dest0*.</span><span class="sxs-lookup"><span data-stu-id="27aef-117">This instruction performs a component-wise unsigned subtract of 32-bit operands *src1* from *src0*, placing the LSB part of the 32-bit result in *dest0*.</span></span>

<span data-ttu-id="27aef-118">O componente correspondente no *dest1* será gravado com 1 se um empréstimo for produzido; caso contrário, 0.</span><span class="sxs-lookup"><span data-stu-id="27aef-118">The corresponding component in *dest1* is written with 1 if a borrow is produced, 0 otherwise.</span></span>

<span data-ttu-id="27aef-119">*dest1* pode ser nulo se o empréstimo não for necessário.</span><span class="sxs-lookup"><span data-stu-id="27aef-119">*dest1* can be NULL if the borrow is not needed.</span></span>

<span data-ttu-id="27aef-120">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="27aef-120">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="27aef-121">Vértice</span><span class="sxs-lookup"><span data-stu-id="27aef-121">Vertex</span></span> | <span data-ttu-id="27aef-122">Envoltória</span><span class="sxs-lookup"><span data-stu-id="27aef-122">Hull</span></span> | <span data-ttu-id="27aef-123">Domínio</span><span class="sxs-lookup"><span data-stu-id="27aef-123">Domain</span></span> | <span data-ttu-id="27aef-124">Geometria</span><span class="sxs-lookup"><span data-stu-id="27aef-124">Geometry</span></span> | <span data-ttu-id="27aef-125">16x16</span><span class="sxs-lookup"><span data-stu-id="27aef-125">Pixel</span></span> | <span data-ttu-id="27aef-126">Computação</span><span class="sxs-lookup"><span data-stu-id="27aef-126">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="27aef-127">X</span><span class="sxs-lookup"><span data-stu-id="27aef-127">X</span></span>      | <span data-ttu-id="27aef-128">X</span><span class="sxs-lookup"><span data-stu-id="27aef-128">X</span></span>    | <span data-ttu-id="27aef-129">X</span><span class="sxs-lookup"><span data-stu-id="27aef-129">X</span></span>      | <span data-ttu-id="27aef-130">X</span><span class="sxs-lookup"><span data-stu-id="27aef-130">X</span></span>        | <span data-ttu-id="27aef-131">X</span><span class="sxs-lookup"><span data-stu-id="27aef-131">X</span></span>     | <span data-ttu-id="27aef-132">X</span><span class="sxs-lookup"><span data-stu-id="27aef-132">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="27aef-133">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="27aef-133">Minimum Shader Model</span></span>

<span data-ttu-id="27aef-134">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="27aef-134">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="27aef-135">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="27aef-135">Shader Model</span></span>                                              | <span data-ttu-id="27aef-136">Com suporte</span><span class="sxs-lookup"><span data-stu-id="27aef-136">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="27aef-137">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="27aef-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="27aef-138">sim</span><span class="sxs-lookup"><span data-stu-id="27aef-138">yes</span></span>       |
| [<span data-ttu-id="27aef-139">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="27aef-139">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="27aef-140">não</span><span class="sxs-lookup"><span data-stu-id="27aef-140">no</span></span>        |
| [<span data-ttu-id="27aef-141">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="27aef-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="27aef-142">não</span><span class="sxs-lookup"><span data-stu-id="27aef-142">no</span></span>        |
| [<span data-ttu-id="27aef-143">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="27aef-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="27aef-144">não</span><span class="sxs-lookup"><span data-stu-id="27aef-144">no</span></span>        |
| [<span data-ttu-id="27aef-145">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="27aef-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="27aef-146">não</span><span class="sxs-lookup"><span data-stu-id="27aef-146">no</span></span>        |
| [<span data-ttu-id="27aef-147">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="27aef-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="27aef-148">não</span><span class="sxs-lookup"><span data-stu-id="27aef-148">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="27aef-149">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="27aef-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27aef-150">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="27aef-150">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





