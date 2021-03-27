---
title: lt (sm4-ASM)
description: Comparação de ponto flutuante de vetor por componente.
ms.assetid: DB10F654-4A98-4ED8-A3B4-CA9FE1DFE6CD
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67a727987e4eaee017137d62dbe12f8581540876
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104293571"
---
# <a name="lt-sm4---asm"></a><span data-ttu-id="c0d65-103">lt (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="c0d65-103">lt (sm4 - asm)</span></span>

<span data-ttu-id="c0d65-104">Comparação de ponto flutuante de vetor por componente.</span><span class="sxs-lookup"><span data-stu-id="c0d65-104">Component-wise vector floating point less-than comparison.</span></span>



| <span data-ttu-id="c0d65-105">lt dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="c0d65-105">lt dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|----------------------------------------------------------------------------------|



 



| <span data-ttu-id="c0d65-106">Item</span><span class="sxs-lookup"><span data-stu-id="c0d65-106">Item</span></span>                                                            | <span data-ttu-id="c0d65-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="c0d65-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="c0d65-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="c0d65-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="c0d65-109">\[no \] endereço do resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="c0d65-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="c0d65-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="c0d65-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="c0d65-111">\[no \] valor a ser comparado com *src1*.</span><span class="sxs-lookup"><span data-stu-id="c0d65-111">\[in\] The value to compare to *src1*.</span></span><br/>             |
| <span data-ttu-id="c0d65-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="c0d65-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="c0d65-113">\[no \] valor a ser comparado com *src0*.</span><span class="sxs-lookup"><span data-stu-id="c0d65-113">\[in\] The value to compare to *src0*.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="c0d65-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="c0d65-114">Remarks</span></span>

<span data-ttu-id="c0d65-115">Essa instrução executa a comparação de float (*src0*  <  *src1*) para cada componente e grava o resultado em *dest*.</span><span class="sxs-lookup"><span data-stu-id="c0d65-115">This instruction performs the float comparison (*src0* < *src1*) for each component, and writes the result to *dest*.</span></span>

<span data-ttu-id="c0d65-116">Se a comparação for verdadeira, 0xFFFFFFFF será retornado para esse componente.</span><span class="sxs-lookup"><span data-stu-id="c0d65-116">If the comparison is true, then 0xFFFFFFFF is returned for that component.</span></span> <span data-ttu-id="c0d65-117">Caso contrário, 0x0000000 será retornado</span><span class="sxs-lookup"><span data-stu-id="c0d65-117">Otherwise 0x0000000 is returned</span></span>

<span data-ttu-id="c0d65-118">As normas são liberadas antes da comparação; os registros originais de origem são inalterados.</span><span class="sxs-lookup"><span data-stu-id="c0d65-118">Denorms are flushed before comparison; original source registers are untouched.</span></span>

<span data-ttu-id="c0d65-119">+ 0 é igual a-0.</span><span class="sxs-lookup"><span data-stu-id="c0d65-119">+0 equals -0.</span></span>

<span data-ttu-id="c0d65-120">A comparação com NaN retorna false.</span><span class="sxs-lookup"><span data-stu-id="c0d65-120">Comparison with NaN returns false.</span></span>

<span data-ttu-id="c0d65-121">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="c0d65-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="c0d65-122">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="c0d65-122">Vertex Shader</span></span> | <span data-ttu-id="c0d65-123">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="c0d65-123">Geometry Shader</span></span> | <span data-ttu-id="c0d65-124">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="c0d65-124">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="c0d65-125">x</span><span class="sxs-lookup"><span data-stu-id="c0d65-125">x</span></span>             | <span data-ttu-id="c0d65-126">x</span><span class="sxs-lookup"><span data-stu-id="c0d65-126">x</span></span>               | <span data-ttu-id="c0d65-127">x</span><span class="sxs-lookup"><span data-stu-id="c0d65-127">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="c0d65-128">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="c0d65-128">Minimum Shader Model</span></span>

<span data-ttu-id="c0d65-129">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="c0d65-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="c0d65-130">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="c0d65-130">Shader Model</span></span>                                              | <span data-ttu-id="c0d65-131">Com suporte</span><span class="sxs-lookup"><span data-stu-id="c0d65-131">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="c0d65-132">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="c0d65-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="c0d65-133">sim</span><span class="sxs-lookup"><span data-stu-id="c0d65-133">yes</span></span>       |
| [<span data-ttu-id="c0d65-134">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="c0d65-134">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="c0d65-135">sim</span><span class="sxs-lookup"><span data-stu-id="c0d65-135">yes</span></span>       |
| [<span data-ttu-id="c0d65-136">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="c0d65-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="c0d65-137">sim</span><span class="sxs-lookup"><span data-stu-id="c0d65-137">yes</span></span>       |
| [<span data-ttu-id="c0d65-138">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c0d65-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="c0d65-139">não</span><span class="sxs-lookup"><span data-stu-id="c0d65-139">no</span></span>        |
| [<span data-ttu-id="c0d65-140">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c0d65-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="c0d65-141">não</span><span class="sxs-lookup"><span data-stu-id="c0d65-141">no</span></span>        |
| [<span data-ttu-id="c0d65-142">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c0d65-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="c0d65-143">não</span><span class="sxs-lookup"><span data-stu-id="c0d65-143">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="c0d65-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c0d65-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c0d65-145">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c0d65-145">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





