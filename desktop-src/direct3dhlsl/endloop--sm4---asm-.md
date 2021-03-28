---
title: ENDLOOP (sm4-ASM)
description: Finaliza uma instrução de loop.
ms.assetid: 0BEFADF4-036E-4FDA-9681-10965D6BA9FC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 655fa6addd19a6ce9f6f6b20a2677ef43cb8b751
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104365178"
---
# <a name="endloop-sm4---asm"></a><span data-ttu-id="e7a20-103">ENDLOOP (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="e7a20-103">endloop (sm4 - asm)</span></span>

<span data-ttu-id="e7a20-104">Finaliza uma instrução de loop.</span><span class="sxs-lookup"><span data-stu-id="e7a20-104">Ends a loop statement.</span></span>



| <span data-ttu-id="e7a20-105">loop de fim</span><span class="sxs-lookup"><span data-stu-id="e7a20-105">endloop</span></span> |
|---------|



 

## <a name="remarks"></a><span data-ttu-id="e7a20-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="e7a20-106">Remarks</span></span>

<span data-ttu-id="e7a20-107">O exemplo a seguir mostra como usar essa instrução.</span><span class="sxs-lookup"><span data-stu-id="e7a20-107">The following example shows how to use this instruction.</span></span>

``` syntax
                loop
                    // example of termination condition
                    if_nz r0.x
                        break
                    endif
                    ...
                endloop
```

<span data-ttu-id="e7a20-108">O formato do token contém o deslocamento da instrução de loop correspondente no sombreador como uma conveniência.</span><span class="sxs-lookup"><span data-stu-id="e7a20-108">The token format contains the offset of the corresponding loop instruction in the Shader as a convenience.</span></span>

<span data-ttu-id="e7a20-109">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="e7a20-109">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="e7a20-110">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="e7a20-110">Vertex Shader</span></span> | <span data-ttu-id="e7a20-111">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="e7a20-111">Geometry Shader</span></span> | <span data-ttu-id="e7a20-112">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="e7a20-112">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="e7a20-113">x</span><span class="sxs-lookup"><span data-stu-id="e7a20-113">x</span></span>             | <span data-ttu-id="e7a20-114">x</span><span class="sxs-lookup"><span data-stu-id="e7a20-114">x</span></span>               | <span data-ttu-id="e7a20-115">x</span><span class="sxs-lookup"><span data-stu-id="e7a20-115">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="e7a20-116">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="e7a20-116">Minimum Shader Model</span></span>

<span data-ttu-id="e7a20-117">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="e7a20-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="e7a20-118">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="e7a20-118">Shader Model</span></span>                                              | <span data-ttu-id="e7a20-119">Com suporte</span><span class="sxs-lookup"><span data-stu-id="e7a20-119">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="e7a20-120">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="e7a20-120">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="e7a20-121">sim</span><span class="sxs-lookup"><span data-stu-id="e7a20-121">yes</span></span>       |
| [<span data-ttu-id="e7a20-122">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="e7a20-122">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="e7a20-123">sim</span><span class="sxs-lookup"><span data-stu-id="e7a20-123">yes</span></span>       |
| [<span data-ttu-id="e7a20-124">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="e7a20-124">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="e7a20-125">sim</span><span class="sxs-lookup"><span data-stu-id="e7a20-125">yes</span></span>       |
| [<span data-ttu-id="e7a20-126">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e7a20-126">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="e7a20-127">não</span><span class="sxs-lookup"><span data-stu-id="e7a20-127">no</span></span>        |
| [<span data-ttu-id="e7a20-128">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e7a20-128">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="e7a20-129">não</span><span class="sxs-lookup"><span data-stu-id="e7a20-129">no</span></span>        |
| [<span data-ttu-id="e7a20-130">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e7a20-130">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="e7a20-131">não</span><span class="sxs-lookup"><span data-stu-id="e7a20-131">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="e7a20-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e7a20-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e7a20-133">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e7a20-133">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




