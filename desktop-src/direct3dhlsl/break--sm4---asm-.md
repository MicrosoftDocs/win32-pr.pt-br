---
title: interrupção (sm4-ASM)
description: Move o ponto de execução para a instrução após o próximo loop Endou endswitch.
ms.assetid: 411FB361-FBD1-4180-8D81-2074BA8972B7
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06396d062e9126091052126737e3e05c58dbdb16
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104293567"
---
# <a name="break-sm4---asm"></a><span data-ttu-id="410ad-103">interrupção (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="410ad-103">break (sm4 - asm)</span></span>

<span data-ttu-id="410ad-104">Move o ponto de execução para a instrução após o próximo [loop](endloop--sm4---asm-.md) Endou [endswitch](endswitch--sm4---asm-.md).</span><span class="sxs-lookup"><span data-stu-id="410ad-104">Moves the point of execution to the instruction after the next [endloop](endloop--sm4---asm-.md) or [endswitch](endswitch--sm4---asm-.md).</span></span>



| <span data-ttu-id="410ad-105">break</span><span class="sxs-lookup"><span data-stu-id="410ad-105">break</span></span> |
|-------|



 

## <a name="remarks"></a><span data-ttu-id="410ad-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="410ad-106">Remarks</span></span>

<span data-ttu-id="410ad-107">O formato do token contém o deslocamento da instrução **ENDLOOP** ou **endswitch** correspondente no sombreador como uma conveniência.</span><span class="sxs-lookup"><span data-stu-id="410ad-107">The token format contains the offset of the corresponding **endloop** or **endswitch** instruction in the Shader as a convenience.</span></span>

<span data-ttu-id="410ad-108">O exemplo a seguir mostra a instrução **Break** .</span><span class="sxs-lookup"><span data-stu-id="410ad-108">The following example shows the **break** instruction.</span></span>


```
                loop
                    // example of termination condition
                    if_nz r0.x
                        break
                    endif
                    ...
                endloop
```



<span data-ttu-id="410ad-109">Essa instrução deve aparecer **em um loop ENDLOOP** /  ou em um **caso** em um  / **comutador** endswitch.</span><span class="sxs-lookup"><span data-stu-id="410ad-109">This instruction must appear within a **loop**/**endloop** or in a **case** in a **switch**/**endswitch**.</span></span>

<span data-ttu-id="410ad-110">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="410ad-110">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="410ad-111">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="410ad-111">Vertex Shader</span></span> | <span data-ttu-id="410ad-112">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="410ad-112">Geometry Shader</span></span> | <span data-ttu-id="410ad-113">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="410ad-113">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="410ad-114">x</span><span class="sxs-lookup"><span data-stu-id="410ad-114">x</span></span>             | <span data-ttu-id="410ad-115">x</span><span class="sxs-lookup"><span data-stu-id="410ad-115">x</span></span>               | <span data-ttu-id="410ad-116">x</span><span class="sxs-lookup"><span data-stu-id="410ad-116">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="410ad-117">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="410ad-117">Minimum Shader Model</span></span>

<span data-ttu-id="410ad-118">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="410ad-118">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="410ad-119">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="410ad-119">Shader Model</span></span>                                              | <span data-ttu-id="410ad-120">Com suporte</span><span class="sxs-lookup"><span data-stu-id="410ad-120">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="410ad-121">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="410ad-121">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="410ad-122">sim</span><span class="sxs-lookup"><span data-stu-id="410ad-122">yes</span></span>       |
| [<span data-ttu-id="410ad-123">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="410ad-123">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="410ad-124">sim</span><span class="sxs-lookup"><span data-stu-id="410ad-124">yes</span></span>       |
| [<span data-ttu-id="410ad-125">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="410ad-125">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="410ad-126">sim</span><span class="sxs-lookup"><span data-stu-id="410ad-126">yes</span></span>       |
| [<span data-ttu-id="410ad-127">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="410ad-127">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="410ad-128">não</span><span class="sxs-lookup"><span data-stu-id="410ad-128">no</span></span>        |
| [<span data-ttu-id="410ad-129">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="410ad-129">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="410ad-130">não</span><span class="sxs-lookup"><span data-stu-id="410ad-130">no</span></span>        |
| [<span data-ttu-id="410ad-131">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="410ad-131">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="410ad-132">não</span><span class="sxs-lookup"><span data-stu-id="410ad-132">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="410ad-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="410ad-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="410ad-134">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="410ad-134">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




