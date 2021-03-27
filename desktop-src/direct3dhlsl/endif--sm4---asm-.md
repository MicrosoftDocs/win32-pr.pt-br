---
title: endif (sm4-ASM)
description: Encerra uma instrução If.
ms.assetid: 9F4CF9E0-4D9D-4300-B432-432C560F34BB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d3fa6cf0efd395843212f6bacac478285e496c2
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104006860"
---
# <a name="endif-sm4---asm"></a><span data-ttu-id="96b04-103">endif (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="96b04-103">endif (sm4 - asm)</span></span>

<span data-ttu-id="96b04-104">Encerra uma instrução [If](if--sm4---asm-.md) .</span><span class="sxs-lookup"><span data-stu-id="96b04-104">Ends an [if](if--sm4---asm-.md) statement.</span></span>



| <span data-ttu-id="96b04-105">endif</span><span class="sxs-lookup"><span data-stu-id="96b04-105">endif</span></span> |
|-------|



 

## <a name="remarks"></a><span data-ttu-id="96b04-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="96b04-106">Remarks</span></span>

<span data-ttu-id="96b04-107">O exemplo a seguir mostra como usar a instrução endif.</span><span class="sxs-lookup"><span data-stu-id="96b04-107">The following example shows how to use the endif instruction.</span></span>

``` syntax
                if     // any of the various forms of if* statements
                   ...
                else   // (optional)
                   ...
                endif
```

<span data-ttu-id="96b04-108">O formato do token contém o deslocamento da instrução **If** correspondente no sombreador como uma conveniência.</span><span class="sxs-lookup"><span data-stu-id="96b04-108">The token format contains the offset of the corresponding **if** instruction in the Shader as a convenience.</span></span>

<span data-ttu-id="96b04-109">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="96b04-109">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="96b04-110">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="96b04-110">Vertex Shader</span></span> | <span data-ttu-id="96b04-111">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="96b04-111">Geometry Shader</span></span> | <span data-ttu-id="96b04-112">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="96b04-112">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="96b04-113">x</span><span class="sxs-lookup"><span data-stu-id="96b04-113">x</span></span>             | <span data-ttu-id="96b04-114">x</span><span class="sxs-lookup"><span data-stu-id="96b04-114">x</span></span>               | <span data-ttu-id="96b04-115">x</span><span class="sxs-lookup"><span data-stu-id="96b04-115">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="96b04-116">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="96b04-116">Minimum Shader Model</span></span>

<span data-ttu-id="96b04-117">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="96b04-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="96b04-118">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="96b04-118">Shader Model</span></span>                                              | <span data-ttu-id="96b04-119">Com suporte</span><span class="sxs-lookup"><span data-stu-id="96b04-119">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="96b04-120">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="96b04-120">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="96b04-121">sim</span><span class="sxs-lookup"><span data-stu-id="96b04-121">yes</span></span>       |
| [<span data-ttu-id="96b04-122">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="96b04-122">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="96b04-123">sim</span><span class="sxs-lookup"><span data-stu-id="96b04-123">yes</span></span>       |
| [<span data-ttu-id="96b04-124">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="96b04-124">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="96b04-125">sim</span><span class="sxs-lookup"><span data-stu-id="96b04-125">yes</span></span>       |
| [<span data-ttu-id="96b04-126">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="96b04-126">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="96b04-127">não</span><span class="sxs-lookup"><span data-stu-id="96b04-127">no</span></span>        |
| [<span data-ttu-id="96b04-128">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="96b04-128">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="96b04-129">não</span><span class="sxs-lookup"><span data-stu-id="96b04-129">no</span></span>        |
| [<span data-ttu-id="96b04-130">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="96b04-130">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="96b04-131">não</span><span class="sxs-lookup"><span data-stu-id="96b04-131">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="96b04-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="96b04-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="96b04-133">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="96b04-133">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




