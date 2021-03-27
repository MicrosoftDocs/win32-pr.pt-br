---
title: ILT (sm4-ASM)
description: Comparação de números inteiros de vetor por componente-que.
ms.assetid: 5F06E568-6234-4778-8169-D8352FAB5297
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2c2e5e47272412bb483e4782e9a6c35e971293c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104293557"
---
# <a name="ilt-sm4---asm"></a><span data-ttu-id="65c85-103">ILT (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="65c85-103">ilt (sm4 - asm)</span></span>

<span data-ttu-id="65c85-104">Comparação de números inteiros de vetor por componente-que.</span><span class="sxs-lookup"><span data-stu-id="65c85-104">Component-wise vector integer less-than comparison.</span></span>



| <span data-ttu-id="65c85-105">dest \[ . máscara \] , src0 \[ . swizzle \] , src1 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="65c85-105">ilt dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|-------------------------------------------------------|



 



| <span data-ttu-id="65c85-106">Item</span><span class="sxs-lookup"><span data-stu-id="65c85-106">Item</span></span>                                                            | <span data-ttu-id="65c85-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="65c85-107">Description</span></span>                                       |
|-----------------------------------------------------------------|---------------------------------------------------|
| <span data-ttu-id="65c85-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="65c85-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="65c85-109">O resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="65c85-109">The result of the operation.</span></span><br/>           |
| <span data-ttu-id="65c85-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="65c85-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="65c85-111">\[no \] valor a ser comparado com *src1*.</span><span class="sxs-lookup"><span data-stu-id="65c85-111">\[in\] The value to compare to *src1*.</span></span><br/> |
| <span data-ttu-id="65c85-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="65c85-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="65c85-113">\[no \] valor a ser comparado com *src0*.</span><span class="sxs-lookup"><span data-stu-id="65c85-113">\[in\] The value to compare to *src0*.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="65c85-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="65c85-114">Remarks</span></span>

<span data-ttu-id="65c85-115">Executa a comparação de inteiros *(src0*  <  *src1*) para cada componente e grava o resultado em *dest*.</span><span class="sxs-lookup"><span data-stu-id="65c85-115">Performs the integer comparison *(src0* < *src1*) for each component, and writes the result to *dest*.</span></span>

<span data-ttu-id="65c85-116">Se a comparação for verdadeira, 0xFFFFFFFF será retornado para esse componente.</span><span class="sxs-lookup"><span data-stu-id="65c85-116">If the comparison is true, then 0xFFFFFFFF is returned for that component.</span></span> <span data-ttu-id="65c85-117">Caso contrário, 0x0000000 será retornado.</span><span class="sxs-lookup"><span data-stu-id="65c85-117">Otherwise 0x0000000 is returned.</span></span>

<span data-ttu-id="65c85-118">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="65c85-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="65c85-119">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="65c85-119">Vertex Shader</span></span> | <span data-ttu-id="65c85-120">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="65c85-120">Geometry Shader</span></span> | <span data-ttu-id="65c85-121">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="65c85-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="65c85-122">x</span><span class="sxs-lookup"><span data-stu-id="65c85-122">x</span></span>             | <span data-ttu-id="65c85-123">x</span><span class="sxs-lookup"><span data-stu-id="65c85-123">x</span></span>               | <span data-ttu-id="65c85-124">x</span><span class="sxs-lookup"><span data-stu-id="65c85-124">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="65c85-125">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="65c85-125">Minimum Shader Model</span></span>



| <span data-ttu-id="65c85-126">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="65c85-126">Shader Model</span></span>                                              | <span data-ttu-id="65c85-127">Com suporte</span><span class="sxs-lookup"><span data-stu-id="65c85-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="65c85-128">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="65c85-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="65c85-129">sim</span><span class="sxs-lookup"><span data-stu-id="65c85-129">yes</span></span>       |
| [<span data-ttu-id="65c85-130">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="65c85-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="65c85-131">sim</span><span class="sxs-lookup"><span data-stu-id="65c85-131">yes</span></span>       |
| [<span data-ttu-id="65c85-132">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="65c85-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="65c85-133">sim</span><span class="sxs-lookup"><span data-stu-id="65c85-133">yes</span></span>       |
| [<span data-ttu-id="65c85-134">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="65c85-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="65c85-135">não</span><span class="sxs-lookup"><span data-stu-id="65c85-135">no</span></span>        |
| [<span data-ttu-id="65c85-136">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="65c85-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="65c85-137">não</span><span class="sxs-lookup"><span data-stu-id="65c85-137">no</span></span>        |
| [<span data-ttu-id="65c85-138">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="65c85-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="65c85-139">não</span><span class="sxs-lookup"><span data-stu-id="65c85-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="65c85-140">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="65c85-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="65c85-141">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="65c85-141">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





