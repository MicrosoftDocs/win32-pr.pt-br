---
title: ftou (sm4-ASM)
description: Ponto flutuante para conversão de inteiro sem sinal.
ms.assetid: 0E3E090B-72C0-4CED-AFA5-2DDCF67D7263
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4a5e65e4bb9d4e71e4a2000f00861cf63e7c181
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104293561"
---
# <a name="ftou-sm4---asm"></a><span data-ttu-id="58bad-103">ftou (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="58bad-103">ftou (sm4 - asm)</span></span>

<span data-ttu-id="58bad-104">Ponto flutuante para conversão de inteiro sem sinal.</span><span class="sxs-lookup"><span data-stu-id="58bad-104">Floating point to unsigned integer conversion.</span></span>



| <span data-ttu-id="58bad-105">ftou dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="58bad-105">ftou dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|----------------------------------------------------|



 



| <span data-ttu-id="58bad-106">ftoi dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="58bad-106">ftoi dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|----------------------------------------------------|



 



| <span data-ttu-id="58bad-107">Item</span><span class="sxs-lookup"><span data-stu-id="58bad-107">Item</span></span>                                                            | <span data-ttu-id="58bad-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="58bad-108">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="58bad-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="58bad-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="58bad-110">\[no \] endereço do resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="58bad-110">\[in\] The address of the result of the operation.</span></span> <br/> |
| <span data-ttu-id="58bad-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="58bad-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="58bad-112">\[no \] valor a ser convertido.</span><span class="sxs-lookup"><span data-stu-id="58bad-112">\[in\] The value to convert.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="58bad-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="58bad-113">Remarks</span></span>

<span data-ttu-id="58bad-114">A conversão é executada por componente.</span><span class="sxs-lookup"><span data-stu-id="58bad-114">The conversion is performed per-component.</span></span> <span data-ttu-id="58bad-115">O arredondamento é sempre executado em direção a zero, seguindo a Convenção C para conversões de float para int.</span><span class="sxs-lookup"><span data-stu-id="58bad-115">Rounding is always performed towards zero, following the C convention for casts from float to int.</span></span>

<span data-ttu-id="58bad-116">Os aplicativos que exigem uma semântica de arredondamento diferente podem invocar as instruções de **arredondamento** antes da conversão para o número inteiro.</span><span class="sxs-lookup"><span data-stu-id="58bad-116">Applications that require different rounding semantics can invoke the **round** instructions before casting to integer.</span></span>

<span data-ttu-id="58bad-117">As entradas são clamped para o intervalo \[ 0,0 f... 4294967295.999 f \] antes da conversão, e os valores Nan de entrada produzem um resultado zero.</span><span class="sxs-lookup"><span data-stu-id="58bad-117">Inputs are clamped to the range \[0.0f ... 4294967295.999f\] prior to conversion, and input NaN values produce a zero result.</span></span>

<span data-ttu-id="58bad-118">Os modificadores de valor negado e absoluto opcionais são aplicados aos valores de origem antes da conversão.</span><span class="sxs-lookup"><span data-stu-id="58bad-118">Optional negate and absolute value modifiers are applied to the source values before conversion.</span></span>

<span data-ttu-id="58bad-119">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="58bad-119">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="58bad-120">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="58bad-120">Vertex Shader</span></span> | <span data-ttu-id="58bad-121">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="58bad-121">Geometry Shader</span></span> | <span data-ttu-id="58bad-122">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="58bad-122">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="58bad-123">x</span><span class="sxs-lookup"><span data-stu-id="58bad-123">x</span></span>             | <span data-ttu-id="58bad-124">x</span><span class="sxs-lookup"><span data-stu-id="58bad-124">x</span></span>               | <span data-ttu-id="58bad-125">x</span><span class="sxs-lookup"><span data-stu-id="58bad-125">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="58bad-126">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="58bad-126">Minimum Shader Model</span></span>

<span data-ttu-id="58bad-127">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="58bad-127">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="58bad-128">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="58bad-128">Shader Model</span></span>                                              | <span data-ttu-id="58bad-129">Com suporte</span><span class="sxs-lookup"><span data-stu-id="58bad-129">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="58bad-130">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="58bad-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="58bad-131">sim</span><span class="sxs-lookup"><span data-stu-id="58bad-131">yes</span></span>       |
| [<span data-ttu-id="58bad-132">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="58bad-132">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="58bad-133">sim</span><span class="sxs-lookup"><span data-stu-id="58bad-133">yes</span></span>       |
| [<span data-ttu-id="58bad-134">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="58bad-134">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="58bad-135">sim</span><span class="sxs-lookup"><span data-stu-id="58bad-135">yes</span></span>       |
| [<span data-ttu-id="58bad-136">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="58bad-136">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="58bad-137">não</span><span class="sxs-lookup"><span data-stu-id="58bad-137">no</span></span>        |
| [<span data-ttu-id="58bad-138">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="58bad-138">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="58bad-139">não</span><span class="sxs-lookup"><span data-stu-id="58bad-139">no</span></span>        |
| [<span data-ttu-id="58bad-140">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="58bad-140">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="58bad-141">não</span><span class="sxs-lookup"><span data-stu-id="58bad-141">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="58bad-142">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="58bad-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="58bad-143">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="58bad-143">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





