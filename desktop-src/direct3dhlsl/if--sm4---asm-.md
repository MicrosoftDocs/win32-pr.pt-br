---
title: If (sm4-ASM)
description: Branch baseado em lógico ou resultado.
ms.assetid: 9F4CF9E0-4D9D-4300-B432-432C560F34BB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 653c84be0d30a036bf93d852268e44bcca08bbcb
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104988554"
---
# <a name="if-sm4---asm"></a><span data-ttu-id="16bbc-103">If (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="16bbc-103">if (sm4 - asm)</span></span>

<span data-ttu-id="16bbc-104">Branch baseado em lógico ou resultado.</span><span class="sxs-lookup"><span data-stu-id="16bbc-104">Branch based on logical OR result.</span></span>



| <span data-ttu-id="16bbc-105">Se { \_ z </span><span class="sxs-lookup"><span data-stu-id="16bbc-105">if{\_z</span></span>\|<span data-ttu-id="16bbc-106">\_NZ} src0. Select \_ componente</span><span class="sxs-lookup"><span data-stu-id="16bbc-106">\_nz} src0.select\_component</span></span> |
|--------------------------------------|



 



| <span data-ttu-id="16bbc-107">Item</span><span class="sxs-lookup"><span data-stu-id="16bbc-107">Item</span></span>                                                            | <span data-ttu-id="16bbc-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="16bbc-108">Description</span></span>                                                              |
|-----------------------------------------------------------------|--------------------------------------------------------------------------|
| <span data-ttu-id="16bbc-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="16bbc-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="16bbc-110">\[in \] contém o componente no qual testar a condição.</span><span class="sxs-lookup"><span data-stu-id="16bbc-110">\[in\] Contains the component on which to test the condition.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="16bbc-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="16bbc-111">Remarks</span></span>

<span data-ttu-id="16bbc-112">O formato do token contém o deslocamento da instrução endif correspondente no sombreador como uma conveniência.</span><span class="sxs-lookup"><span data-stu-id="16bbc-112">The token format contains the offset of the corresponding endif instruction in the Shader as a convenience.</span></span>

<span data-ttu-id="16bbc-113">O exemplo a seguir mostra como usar essa instrução.</span><span class="sxs-lookup"><span data-stu-id="16bbc-113">The following example shows how to use this instruction.</span></span>

``` syntax
                if_z r0.x // if all bits in r0.x are zero
                   ...
                else // (optional)
                   ...
                endif
                if_nz r1.x // if any bit in r0.x is nonzero
                   ...
                else // (optional)
                   ...
                endif
```

### <a name="restrictions"></a><span data-ttu-id="16bbc-114">Restrições</span><span class="sxs-lookup"><span data-stu-id="16bbc-114">Restrictions</span></span>

-   <span data-ttu-id="16bbc-115">Os operandos de origem (se quatro vetores de componente) devem usar um seletor de componente único.</span><span class="sxs-lookup"><span data-stu-id="16bbc-115">The source operands (if 4 component vectors) must use a single component selector.</span></span>
-   <span data-ttu-id="16bbc-116">O registro de 32 bits fornecido pelo *src0* é testado em um nível de bit.</span><span class="sxs-lookup"><span data-stu-id="16bbc-116">The 32-bit register supplied by *src0* is tested at a bit level.</span></span> <span data-ttu-id="16bbc-117">Se qualquer bit for diferente de zero, **se \_ z** será true.</span><span class="sxs-lookup"><span data-stu-id="16bbc-117">If any bit is nonzero, **if\_z** will be true.</span></span> <span data-ttu-id="16bbc-118">Se todos os bits forem zero, **se \_ NZ** será true.</span><span class="sxs-lookup"><span data-stu-id="16bbc-118">If all bits are zero, **if\_nz** will be true.</span></span>
-   <span data-ttu-id="16bbc-119">Os blocos de controle de fluxo podem aninhar até 64 de profundidade por sub-rotina (e principal).</span><span class="sxs-lookup"><span data-stu-id="16bbc-119">Flow control blocks can nest up to 64 deep per subroutine (and main).</span></span> <span data-ttu-id="16bbc-120">O compilador HLSL não gerará sub-rotinas que excedam esse limite.</span><span class="sxs-lookup"><span data-stu-id="16bbc-120">The HLSL compiler will not generate subroutines that exceed this limit.</span></span> <span data-ttu-id="16bbc-121">O comportamento das instruções de fluxo de controle além de 64 níveis de profundidade (por sub-rotina) é indefinido.</span><span class="sxs-lookup"><span data-stu-id="16bbc-121">Behavior of control flow instructions beyond 64 levels deep (per subroutine) is undefined.</span></span>

<span data-ttu-id="16bbc-122">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="16bbc-122">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="16bbc-123">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="16bbc-123">Vertex Shader</span></span> | <span data-ttu-id="16bbc-124">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="16bbc-124">Geometry Shader</span></span> | <span data-ttu-id="16bbc-125">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="16bbc-125">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="16bbc-126">x</span><span class="sxs-lookup"><span data-stu-id="16bbc-126">x</span></span>             | <span data-ttu-id="16bbc-127">x</span><span class="sxs-lookup"><span data-stu-id="16bbc-127">x</span></span>               | <span data-ttu-id="16bbc-128">x</span><span class="sxs-lookup"><span data-stu-id="16bbc-128">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="16bbc-129">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="16bbc-129">Minimum Shader Model</span></span>

<span data-ttu-id="16bbc-130">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="16bbc-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="16bbc-131">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="16bbc-131">Shader Model</span></span>                                              | <span data-ttu-id="16bbc-132">Com suporte</span><span class="sxs-lookup"><span data-stu-id="16bbc-132">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="16bbc-133">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="16bbc-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="16bbc-134">sim</span><span class="sxs-lookup"><span data-stu-id="16bbc-134">yes</span></span>       |
| [<span data-ttu-id="16bbc-135">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="16bbc-135">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="16bbc-136">sim</span><span class="sxs-lookup"><span data-stu-id="16bbc-136">yes</span></span>       |
| [<span data-ttu-id="16bbc-137">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="16bbc-137">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="16bbc-138">sim</span><span class="sxs-lookup"><span data-stu-id="16bbc-138">yes</span></span>       |
| [<span data-ttu-id="16bbc-139">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="16bbc-139">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="16bbc-140">não</span><span class="sxs-lookup"><span data-stu-id="16bbc-140">no</span></span>        |
| [<span data-ttu-id="16bbc-141">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="16bbc-141">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="16bbc-142">não</span><span class="sxs-lookup"><span data-stu-id="16bbc-142">no</span></span>        |
| [<span data-ttu-id="16bbc-143">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="16bbc-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="16bbc-144">não</span><span class="sxs-lookup"><span data-stu-id="16bbc-144">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="16bbc-145">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="16bbc-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16bbc-146">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="16bbc-146">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





