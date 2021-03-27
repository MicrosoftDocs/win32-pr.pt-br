---
title: senão (sm4-ASM)
description: Inicia um bloco else.
ms.assetid: CFF25E78-D986-4EC5-B542-B3396EFF88E1
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e283a2621c916ac254daab9f055be0ffe1ba67d
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104967127"
---
# <a name="else-sm4---asm"></a><span data-ttu-id="a7dde-103">senão (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="a7dde-103">else (sm4 - asm)</span></span>

<span data-ttu-id="a7dde-104">Inicia um bloco **else** .</span><span class="sxs-lookup"><span data-stu-id="a7dde-104">Starts an **else** block.</span></span>



| <span data-ttu-id="a7dde-105">else</span><span class="sxs-lookup"><span data-stu-id="a7dde-105">else</span></span> |
|------|



 

## <a name="remarks"></a><span data-ttu-id="a7dde-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="a7dde-106">Remarks</span></span>

<span data-ttu-id="a7dde-107">O formato do token contém o deslocamento da instrução [endif](endif--sm4---asm-.md) correspondente no sombreador como uma conveniência.</span><span class="sxs-lookup"><span data-stu-id="a7dde-107">The token format contains the offset of the corresponding [endif](endif--sm4---asm-.md) instruction in the Shader as a convenience.</span></span>

<span data-ttu-id="a7dde-108">O exemplo a seguir mostra como usar a instrução **else** .</span><span class="sxs-lookup"><span data-stu-id="a7dde-108">The following example shows how to use the **else** instruction.</span></span>

``` syntax
                if     // any of the various forms of if* statements
                   ...
                else   // (optional)
                   ...
                endif
```

<span data-ttu-id="a7dde-109">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="a7dde-109">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="a7dde-110">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="a7dde-110">Vertex Shader</span></span> | <span data-ttu-id="a7dde-111">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="a7dde-111">Geometry Shader</span></span> | <span data-ttu-id="a7dde-112">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="a7dde-112">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="a7dde-113">x</span><span class="sxs-lookup"><span data-stu-id="a7dde-113">x</span></span>             | <span data-ttu-id="a7dde-114">x</span><span class="sxs-lookup"><span data-stu-id="a7dde-114">x</span></span>               | <span data-ttu-id="a7dde-115">x</span><span class="sxs-lookup"><span data-stu-id="a7dde-115">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="a7dde-116">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="a7dde-116">Minimum Shader Model</span></span>

<span data-ttu-id="a7dde-117">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="a7dde-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="a7dde-118">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="a7dde-118">Shader Model</span></span>                                              | <span data-ttu-id="a7dde-119">Com suporte</span><span class="sxs-lookup"><span data-stu-id="a7dde-119">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="a7dde-120">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="a7dde-120">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="a7dde-121">sim</span><span class="sxs-lookup"><span data-stu-id="a7dde-121">yes</span></span>       |
| [<span data-ttu-id="a7dde-122">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="a7dde-122">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="a7dde-123">sim</span><span class="sxs-lookup"><span data-stu-id="a7dde-123">yes</span></span>       |
| [<span data-ttu-id="a7dde-124">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="a7dde-124">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="a7dde-125">sim</span><span class="sxs-lookup"><span data-stu-id="a7dde-125">yes</span></span>       |
| [<span data-ttu-id="a7dde-126">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a7dde-126">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="a7dde-127">não</span><span class="sxs-lookup"><span data-stu-id="a7dde-127">no</span></span>        |
| [<span data-ttu-id="a7dde-128">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a7dde-128">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="a7dde-129">não</span><span class="sxs-lookup"><span data-stu-id="a7dde-129">no</span></span>        |
| [<span data-ttu-id="a7dde-130">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a7dde-130">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="a7dde-131">não</span><span class="sxs-lookup"><span data-stu-id="a7dde-131">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="a7dde-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a7dde-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a7dde-133">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a7dde-133">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




