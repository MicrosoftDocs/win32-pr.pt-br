---
title: loop (sm4-ASM)
description: Especifica um loop que itera até que uma instrução break seja encontrada.
ms.assetid: 0BEFADF4-036E-4FDA-9681-10965D6BA9FC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 243bdf3b370d3505d787451162c22340acef3a45
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104988589"
---
# <a name="loop-sm4---asm"></a><span data-ttu-id="06c0a-103">loop (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="06c0a-103">loop (sm4 - asm)</span></span>

<span data-ttu-id="06c0a-104">Especifica um loop que itera até que uma instrução break seja encontrada.</span><span class="sxs-lookup"><span data-stu-id="06c0a-104">Specifies a loop which iterates until a break instruction is encountered.</span></span>



| <span data-ttu-id="06c0a-105">loop</span><span class="sxs-lookup"><span data-stu-id="06c0a-105">loop</span></span> |
|------|



 

## <a name="remarks"></a><span data-ttu-id="06c0a-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="06c0a-106">Remarks</span></span>

<span data-ttu-id="06c0a-107">o **loop** pode iterar indefinidamente, embora a execução geral do sombreador possa ser forçada a terminar depois que um número de instruções for executado.</span><span class="sxs-lookup"><span data-stu-id="06c0a-107">**loop** can iterate indefinitely, although overall execution of the Shader may be forced to terminate after some number of instructions are executed.</span></span>

<span data-ttu-id="06c0a-108">Os blocos de controle de fluxo podem aninhar até 64 de profundidade por sub-rotina e principal.</span><span class="sxs-lookup"><span data-stu-id="06c0a-108">Flow control blocks can nest up to 64 deep per subroutine and main.</span></span> <span data-ttu-id="06c0a-109">O compilador HLSL não gerará sub-rotinas que excedam esse limite.</span><span class="sxs-lookup"><span data-stu-id="06c0a-109">The HLSL compiler will not generate subroutines that exceed this limit.</span></span> <span data-ttu-id="06c0a-110">O comportamento das instruções de fluxo de controle além de 64 níveis de profundidade por sub-rotina é indefinido.</span><span class="sxs-lookup"><span data-stu-id="06c0a-110">Behavior of control flow instructions beyond 64 levels deep per subroutine is undefined.</span></span>

<span data-ttu-id="06c0a-111">O formato do token contém o deslocamento da instrução [ENDLOOP](endloop--sm4---asm-.md) correspondente no sombreador como uma conveniência.</span><span class="sxs-lookup"><span data-stu-id="06c0a-111">The token format contains the offset of the corresponding [endloop](endloop--sm4---asm-.md) instruction in the Shader as a convenience.</span></span>

<span data-ttu-id="06c0a-112">O exemplo a seguir mostra como usar a instrução loop.</span><span class="sxs-lookup"><span data-stu-id="06c0a-112">The following example shows how to use the loop instruction.</span></span>

``` syntax
                loop
                    // example of termination condition
                    if_nz r0.x
                        break
                    endif
                    ...
                endloop
```

<span data-ttu-id="06c0a-113">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="06c0a-113">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="06c0a-114">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="06c0a-114">Vertex Shader</span></span> | <span data-ttu-id="06c0a-115">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="06c0a-115">Geometry Shader</span></span> | <span data-ttu-id="06c0a-116">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="06c0a-116">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="06c0a-117">x</span><span class="sxs-lookup"><span data-stu-id="06c0a-117">x</span></span>             | <span data-ttu-id="06c0a-118">x</span><span class="sxs-lookup"><span data-stu-id="06c0a-118">x</span></span>               | <span data-ttu-id="06c0a-119">x</span><span class="sxs-lookup"><span data-stu-id="06c0a-119">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="06c0a-120">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="06c0a-120">Minimum Shader Model</span></span>

<span data-ttu-id="06c0a-121">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="06c0a-121">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="06c0a-122">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="06c0a-122">Shader Model</span></span>                                              | <span data-ttu-id="06c0a-123">Com suporte</span><span class="sxs-lookup"><span data-stu-id="06c0a-123">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="06c0a-124">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="06c0a-124">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="06c0a-125">sim</span><span class="sxs-lookup"><span data-stu-id="06c0a-125">yes</span></span>       |
| [<span data-ttu-id="06c0a-126">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="06c0a-126">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="06c0a-127">sim</span><span class="sxs-lookup"><span data-stu-id="06c0a-127">yes</span></span>       |
| [<span data-ttu-id="06c0a-128">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="06c0a-128">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="06c0a-129">sim</span><span class="sxs-lookup"><span data-stu-id="06c0a-129">yes</span></span>       |
| [<span data-ttu-id="06c0a-130">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="06c0a-130">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="06c0a-131">não</span><span class="sxs-lookup"><span data-stu-id="06c0a-131">no</span></span>        |
| [<span data-ttu-id="06c0a-132">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="06c0a-132">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="06c0a-133">não</span><span class="sxs-lookup"><span data-stu-id="06c0a-133">no</span></span>        |
| [<span data-ttu-id="06c0a-134">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="06c0a-134">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="06c0a-135">não</span><span class="sxs-lookup"><span data-stu-id="06c0a-135">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="06c0a-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="06c0a-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06c0a-137">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="06c0a-137">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




