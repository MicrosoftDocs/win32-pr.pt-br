---
title: IAdd (sm4-ASM)
description: Adição de inteiro.
ms.assetid: EF78EA65-DC16-469A-9E45-52844FF4BD93
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b593484aa7c1ef376bb5febf141b144ddef338e0
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104365267"
---
# <a name="iadd-sm4---asm"></a><span data-ttu-id="616d4-103">IAdd (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="616d4-103">iadd (sm4 - asm)</span></span>

<span data-ttu-id="616d4-104">Adição de inteiro.</span><span class="sxs-lookup"><span data-stu-id="616d4-104">Integer addition.</span></span>



| <span data-ttu-id="616d4-105">IAdd dest \[ . Mask \] , \[ - \] src0 \[ . swizzle \] , \[ - \] src1 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="616d4-105">iadd dest\[.mask\], \[-\]src0\[.swizzle\], \[-\]src1\[.swizzle\]</span></span> |
|------------------------------------------------------------------|



 



| <span data-ttu-id="616d4-106">Item</span><span class="sxs-lookup"><span data-stu-id="616d4-106">Item</span></span>                                                            | <span data-ttu-id="616d4-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="616d4-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="616d4-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="616d4-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="616d4-109">\[no \] endereço do resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="616d4-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="616d4-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="616d4-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="616d4-111">\[no \] número a ser adicionado ao *src1*.</span><span class="sxs-lookup"><span data-stu-id="616d4-111">\[in\] The number to be added to *src1*.</span></span><br/>           |
| <span data-ttu-id="616d4-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="616d4-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="616d4-113">\[no \] número a ser adicionado ao *src0*.</span><span class="sxs-lookup"><span data-stu-id="616d4-113">\[in\] The number to be added to *src0*.</span></span><br/>           |



 

## <a name="remarks"></a><span data-ttu-id="616d4-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="616d4-114">Remarks</span></span>

<span data-ttu-id="616d4-115">Adição de componente de operandos de 32 bits *src0* e *src1*, colocando o resultado de 32 bits correto no *dest*.</span><span class="sxs-lookup"><span data-stu-id="616d4-115">Component-wise add of 32-bit operands *src0* and *src1*, placing the correct 32-bit result in *dest*.</span></span> <span data-ttu-id="616d4-116">Nenhum transporte ou empréstimo além dos valores de 32 bits de cada componente é executado, portanto, essa instrução não é sensível à qualidade de seus operandos.</span><span class="sxs-lookup"><span data-stu-id="616d4-116">No carry or borrow beyond the 32-bit values of each component is performed, so this instruction is not sensitive to the signed-ness of its operands.</span></span>

<span data-ttu-id="616d4-117">O modificador opcional Negate nos operandos de origem usa o complemento de 2 antes de executar a operação.</span><span class="sxs-lookup"><span data-stu-id="616d4-117">Optional negate modifier on source operands takes 2's complement before performing operation.</span></span>

<span data-ttu-id="616d4-118">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="616d4-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="616d4-119">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="616d4-119">Vertex Shader</span></span> | <span data-ttu-id="616d4-120">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="616d4-120">Geometry Shader</span></span> | <span data-ttu-id="616d4-121">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="616d4-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="616d4-122">x</span><span class="sxs-lookup"><span data-stu-id="616d4-122">x</span></span>             | <span data-ttu-id="616d4-123">x</span><span class="sxs-lookup"><span data-stu-id="616d4-123">x</span></span>               | <span data-ttu-id="616d4-124">x</span><span class="sxs-lookup"><span data-stu-id="616d4-124">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="616d4-125">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="616d4-125">Minimum Shader Model</span></span>

<span data-ttu-id="616d4-126">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="616d4-126">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="616d4-127">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="616d4-127">Shader Model</span></span>                                              | <span data-ttu-id="616d4-128">Com suporte</span><span class="sxs-lookup"><span data-stu-id="616d4-128">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="616d4-129">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="616d4-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="616d4-130">sim</span><span class="sxs-lookup"><span data-stu-id="616d4-130">yes</span></span>       |
| [<span data-ttu-id="616d4-131">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="616d4-131">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="616d4-132">sim</span><span class="sxs-lookup"><span data-stu-id="616d4-132">yes</span></span>       |
| [<span data-ttu-id="616d4-133">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="616d4-133">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="616d4-134">sim</span><span class="sxs-lookup"><span data-stu-id="616d4-134">yes</span></span>       |
| [<span data-ttu-id="616d4-135">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="616d4-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="616d4-136">não</span><span class="sxs-lookup"><span data-stu-id="616d4-136">no</span></span>        |
| [<span data-ttu-id="616d4-137">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="616d4-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="616d4-138">não</span><span class="sxs-lookup"><span data-stu-id="616d4-138">no</span></span>        |
| [<span data-ttu-id="616d4-139">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="616d4-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="616d4-140">não</span><span class="sxs-lookup"><span data-stu-id="616d4-140">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="616d4-141">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="616d4-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="616d4-142">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="616d4-142">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





