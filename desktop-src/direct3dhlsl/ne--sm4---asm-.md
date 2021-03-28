---
title: ne (sm4-ASM)
description: Comparação de ponto flutuante de vetor por componente sem igual.
ms.assetid: 5BED97D3-8FF6-4F1C-819B-DC8B4A4F2CCA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0e53ff726047bd1870e6c836f4508bdf87001b3
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104365233"
---
# <a name="ne-sm4---asm"></a><span data-ttu-id="7731a-103">ne (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="7731a-103">ne (sm4 - asm)</span></span>

<span data-ttu-id="7731a-104">Comparação de ponto flutuante de vetor por componente sem igual.</span><span class="sxs-lookup"><span data-stu-id="7731a-104">Component-wise vector floating point not-equal comparison.</span></span>



| <span data-ttu-id="7731a-105">ne dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="7731a-105">ne dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|----------------------------------------------------------------------------------|



 



| <span data-ttu-id="7731a-106">Item</span><span class="sxs-lookup"><span data-stu-id="7731a-106">Item</span></span>                                                            | <span data-ttu-id="7731a-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="7731a-107">Description</span></span>                                            |
|-----------------------------------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="7731a-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="7731a-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="7731a-109">\[no \] resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="7731a-109">\[in\] The result of the operation.</span></span><br/>         |
| <span data-ttu-id="7731a-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="7731a-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="7731a-111">\[nos \] componentes para comparar com o *src1*.</span><span class="sxs-lookup"><span data-stu-id="7731a-111">\[in\] The components to compare to *src1*.</span></span><br/> |
| <span data-ttu-id="7731a-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="7731a-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="7731a-113">\[nos \] componentes para comparar com o *src0*.</span><span class="sxs-lookup"><span data-stu-id="7731a-113">\[in\] The components to compare to *src0*.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7731a-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="7731a-114">Remarks</span></span>

<span data-ttu-id="7731a-115">Essa instrução executa a comparação de float (*src0* ! = *src1*) para cada componente e grava o resultado em *dest*.</span><span class="sxs-lookup"><span data-stu-id="7731a-115">This instruction performs the float comparison (*src0* != *src1*) for each component, and writes the result to *dest*.</span></span>

<span data-ttu-id="7731a-116">Se a comparação for verdadeira, 0xFFFFFFFF será retornado para esse componente.</span><span class="sxs-lookup"><span data-stu-id="7731a-116">If the comparison is true, then 0xFFFFFFFF is returned for that component.</span></span> <span data-ttu-id="7731a-117">Caso contrário, 0x0000000 será retornado.</span><span class="sxs-lookup"><span data-stu-id="7731a-117">Otherwise 0x0000000 is returned.</span></span>

<span data-ttu-id="7731a-118">As normas são liberadas antes da comparação com os registros de origem originais intocados.</span><span class="sxs-lookup"><span data-stu-id="7731a-118">Denorms are flushed before comparison with original source registers untouched.</span></span>

<span data-ttu-id="7731a-119">+ 0 é igual a-0.</span><span class="sxs-lookup"><span data-stu-id="7731a-119">+0 equals -0.</span></span>

<span data-ttu-id="7731a-120">A comparação com NaN retorna true.</span><span class="sxs-lookup"><span data-stu-id="7731a-120">Comparison with NaN returns true.</span></span>

<span data-ttu-id="7731a-121">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="7731a-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="7731a-122">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="7731a-122">Vertex Shader</span></span> | <span data-ttu-id="7731a-123">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="7731a-123">Geometry Shader</span></span> | <span data-ttu-id="7731a-124">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="7731a-124">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="7731a-125">x</span><span class="sxs-lookup"><span data-stu-id="7731a-125">x</span></span>             | <span data-ttu-id="7731a-126">x</span><span class="sxs-lookup"><span data-stu-id="7731a-126">x</span></span>               | <span data-ttu-id="7731a-127">x</span><span class="sxs-lookup"><span data-stu-id="7731a-127">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="7731a-128">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="7731a-128">Minimum Shader Model</span></span>

<span data-ttu-id="7731a-129">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="7731a-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="7731a-130">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="7731a-130">Shader Model</span></span>                                              | <span data-ttu-id="7731a-131">Com suporte</span><span class="sxs-lookup"><span data-stu-id="7731a-131">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="7731a-132">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="7731a-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="7731a-133">sim</span><span class="sxs-lookup"><span data-stu-id="7731a-133">yes</span></span>       |
| [<span data-ttu-id="7731a-134">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="7731a-134">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="7731a-135">sim</span><span class="sxs-lookup"><span data-stu-id="7731a-135">yes</span></span>       |
| [<span data-ttu-id="7731a-136">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="7731a-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="7731a-137">sim</span><span class="sxs-lookup"><span data-stu-id="7731a-137">yes</span></span>       |
| [<span data-ttu-id="7731a-138">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7731a-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="7731a-139">não</span><span class="sxs-lookup"><span data-stu-id="7731a-139">no</span></span>        |
| [<span data-ttu-id="7731a-140">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7731a-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="7731a-141">não</span><span class="sxs-lookup"><span data-stu-id="7731a-141">no</span></span>        |
| [<span data-ttu-id="7731a-142">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7731a-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="7731a-143">não</span><span class="sxs-lookup"><span data-stu-id="7731a-143">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="7731a-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7731a-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7731a-145">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7731a-145">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





