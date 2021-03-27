---
title: itof (sm4-ASM)
description: Inteiro assinado para conversão de ponto flutuante.
ms.assetid: 60652168-25FA-4084-8CC1-73F12984ECED
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f9d262f65801cd2caa0e6432b335ce32fff0d4e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103823452"
---
# <a name="itof-sm4---asm"></a><span data-ttu-id="60038-103">itof (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="60038-103">itof (sm4 - asm)</span></span>

<span data-ttu-id="60038-104">Inteiro assinado para conversão de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="60038-104">Signed integer to floating point conversion.</span></span>



| <span data-ttu-id="60038-105">itof dest \[ . Mask \] , \[ - \] src0 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="60038-105">itof dest\[.mask\], \[-\]src0\[.swizzle\]</span></span> |
|-------------------------------------------|



 



| <span data-ttu-id="60038-106">Item</span><span class="sxs-lookup"><span data-stu-id="60038-106">Item</span></span>                                                            | <span data-ttu-id="60038-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="60038-107">Description</span></span>                                             |
|-----------------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="60038-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="60038-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="60038-109">\[in \] contém o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="60038-109">\[in\] Contains the result of the operation.</span></span><br/> |
| <span data-ttu-id="60038-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="60038-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="60038-111">\[in \] contém o valor a ser convertido.</span><span class="sxs-lookup"><span data-stu-id="60038-111">\[in\] Contains the value to convert.</span></span><br/>        |



 

## <a name="remarks"></a><span data-ttu-id="60038-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="60038-112">Remarks</span></span>

<span data-ttu-id="60038-113">Essa instrução de conversão de inteiro em float assinada pressupõe que *src0* contém uma tupla de 4 bits de número inteiro de 32-bit assinado.</span><span class="sxs-lookup"><span data-stu-id="60038-113">This signed integer-to-float conversion instruction assumes that *src0* contains a signed 32-bit integer 4-tuple.</span></span> <span data-ttu-id="60038-114">Depois que a instrução for executada, o *dest* conterá um ponto flutuante de 4 tuplas.</span><span class="sxs-lookup"><span data-stu-id="60038-114">After the instruction executes, *dest* will contain a floating-point 4-tuple.</span></span>

<span data-ttu-id="60038-115">A conversão é executada por componente.</span><span class="sxs-lookup"><span data-stu-id="60038-115">The conversion is performed per-component.</span></span>

<span data-ttu-id="60038-116">Quando um valor de entrada de inteiro é muito grande em magnitude para ser representado exatamente no formato de ponto flutuante, o arredondamento para o modo de par mais próximo é altamente recomendado, mas não obrigatório.</span><span class="sxs-lookup"><span data-stu-id="60038-116">When an integer input value is too large in magnitude to be represented exactly in the floating point format, rounding to nearest even mode is strongly recommended but not required.</span></span>

<span data-ttu-id="60038-117">O modificador opcional Negate no operando de origem usa o complemento de 2 antes de executar a operação aritmética.</span><span class="sxs-lookup"><span data-stu-id="60038-117">The optional negate modifier on source operand takes 2's complement before performing arithmetic operation.</span></span>

<span data-ttu-id="60038-118">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="60038-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="60038-119">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="60038-119">Vertex Shader</span></span> | <span data-ttu-id="60038-120">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="60038-120">Geometry Shader</span></span> | <span data-ttu-id="60038-121">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="60038-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="60038-122">x</span><span class="sxs-lookup"><span data-stu-id="60038-122">x</span></span>             | <span data-ttu-id="60038-123">x</span><span class="sxs-lookup"><span data-stu-id="60038-123">x</span></span>               | <span data-ttu-id="60038-124">x</span><span class="sxs-lookup"><span data-stu-id="60038-124">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="60038-125">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="60038-125">Minimum Shader Model</span></span>

<span data-ttu-id="60038-126">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="60038-126">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="60038-127">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="60038-127">Shader Model</span></span>                                              | <span data-ttu-id="60038-128">Com suporte</span><span class="sxs-lookup"><span data-stu-id="60038-128">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="60038-129">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="60038-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="60038-130">sim</span><span class="sxs-lookup"><span data-stu-id="60038-130">yes</span></span>       |
| [<span data-ttu-id="60038-131">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="60038-131">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="60038-132">sim</span><span class="sxs-lookup"><span data-stu-id="60038-132">yes</span></span>       |
| [<span data-ttu-id="60038-133">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="60038-133">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="60038-134">sim</span><span class="sxs-lookup"><span data-stu-id="60038-134">yes</span></span>       |
| [<span data-ttu-id="60038-135">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="60038-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="60038-136">não</span><span class="sxs-lookup"><span data-stu-id="60038-136">no</span></span>        |
| [<span data-ttu-id="60038-137">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="60038-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="60038-138">não</span><span class="sxs-lookup"><span data-stu-id="60038-138">no</span></span>        |
| [<span data-ttu-id="60038-139">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="60038-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="60038-140">não</span><span class="sxs-lookup"><span data-stu-id="60038-140">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="60038-141">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="60038-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60038-142">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="60038-142">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





