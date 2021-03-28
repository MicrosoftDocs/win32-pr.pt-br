---
title: utof (sm4-ASM)
description: Inteiro não assinado para conversão de ponto flutuante.
ms.assetid: 5A52C959-7B4C-4FA1-B29C-BCAF448419F8
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9283857df12a85819f0d191d13450e0311fdade
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104006922"
---
# <a name="utof-sm4---asm"></a><span data-ttu-id="e44bb-103">utof (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="e44bb-103">utof (sm4 - asm)</span></span>

<span data-ttu-id="e44bb-104">Inteiro não assinado para conversão de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="e44bb-104">Unsigned integer to floating point conversion.</span></span>



| <span data-ttu-id="e44bb-105">utof dest \[ . Mask \] , src0 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="e44bb-105">utof dest\[.mask\], src0\[.swizzle\]</span></span> |
|--------------------------------------|



 



| <span data-ttu-id="e44bb-106">Item</span><span class="sxs-lookup"><span data-stu-id="e44bb-106">Item</span></span>                                                            | <span data-ttu-id="e44bb-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="e44bb-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="e44bb-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="e44bb-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="e44bb-109">\[no \] endereço do resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="e44bb-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="e44bb-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="e44bb-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="e44bb-111">\[nos \] componentes a serem convertidos.</span><span class="sxs-lookup"><span data-stu-id="e44bb-111">\[in\] The components to convert.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="e44bb-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="e44bb-112">Remarks</span></span>

<span data-ttu-id="e44bb-113">*src0* deve conter um inteiro 4-tupla sem sinal de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="e44bb-113">*src0* must contain an unsigned 32-bit integer 4-tuple.</span></span> <span data-ttu-id="e44bb-114">Depois que a instrução for executada, o *dest* conterá um ponto flutuante de 4 tuplas.</span><span class="sxs-lookup"><span data-stu-id="e44bb-114">After the instruction executes, *dest* will contain a floating-point 4-tuple.</span></span> <span data-ttu-id="e44bb-115">A conversão é executada por componente.</span><span class="sxs-lookup"><span data-stu-id="e44bb-115">The conversion is performed per-component.</span></span>

<span data-ttu-id="e44bb-116">Quando um valor de entrada de inteiro é muito grande para ser representado exatamente no formato de ponto flutuante, Round para o modo de par mais próximo.</span><span class="sxs-lookup"><span data-stu-id="e44bb-116">When an integer input value is too large to be represented exactly in the floating point format, round to nearest even mode.</span></span>

<span data-ttu-id="e44bb-117">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="e44bb-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="e44bb-118">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="e44bb-118">Vertex Shader</span></span> | <span data-ttu-id="e44bb-119">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="e44bb-119">Geometry Shader</span></span> | <span data-ttu-id="e44bb-120">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="e44bb-120">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="e44bb-121">x</span><span class="sxs-lookup"><span data-stu-id="e44bb-121">x</span></span>             | <span data-ttu-id="e44bb-122">x</span><span class="sxs-lookup"><span data-stu-id="e44bb-122">x</span></span>               | <span data-ttu-id="e44bb-123">x</span><span class="sxs-lookup"><span data-stu-id="e44bb-123">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="e44bb-124">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="e44bb-124">Minimum Shader Model</span></span>

<span data-ttu-id="e44bb-125">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="e44bb-125">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="e44bb-126">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="e44bb-126">Shader Model</span></span>                                              | <span data-ttu-id="e44bb-127">Com suporte</span><span class="sxs-lookup"><span data-stu-id="e44bb-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="e44bb-128">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="e44bb-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="e44bb-129">sim</span><span class="sxs-lookup"><span data-stu-id="e44bb-129">yes</span></span>       |
| [<span data-ttu-id="e44bb-130">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="e44bb-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="e44bb-131">sim</span><span class="sxs-lookup"><span data-stu-id="e44bb-131">yes</span></span>       |
| [<span data-ttu-id="e44bb-132">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="e44bb-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="e44bb-133">sim</span><span class="sxs-lookup"><span data-stu-id="e44bb-133">yes</span></span>       |
| [<span data-ttu-id="e44bb-134">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e44bb-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="e44bb-135">não</span><span class="sxs-lookup"><span data-stu-id="e44bb-135">no</span></span>        |
| [<span data-ttu-id="e44bb-136">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e44bb-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="e44bb-137">não</span><span class="sxs-lookup"><span data-stu-id="e44bb-137">no</span></span>        |
| [<span data-ttu-id="e44bb-138">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e44bb-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="e44bb-139">não</span><span class="sxs-lookup"><span data-stu-id="e44bb-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="e44bb-140">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e44bb-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e44bb-141">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e44bb-141">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





