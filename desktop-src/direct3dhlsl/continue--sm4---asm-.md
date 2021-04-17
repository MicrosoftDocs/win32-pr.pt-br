---
title: continuar (sm4-ASM)
description: Continua a execução no início do loop atual.
ms.assetid: 3F0021B2-50D1-407C-9EE4-1CB679E184BF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc53b023e998fcf131a387fc009cfc8cb133ff6a
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104988579"
---
# <a name="continue-sm4---asm"></a><span data-ttu-id="8bc06-103">continuar (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="8bc06-103">continue (sm4 - asm)</span></span>

<span data-ttu-id="8bc06-104">Continua a execução no início do loop atual.</span><span class="sxs-lookup"><span data-stu-id="8bc06-104">Continues execution at the beginning of the current loop.</span></span>



| <span data-ttu-id="8bc06-105">continue</span><span class="sxs-lookup"><span data-stu-id="8bc06-105">continue</span></span> |
|----------|



 

## <a name="remarks"></a><span data-ttu-id="8bc06-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="8bc06-106">Remarks</span></span>

<span data-ttu-id="8bc06-107">**continue** pode ser usado somente dentro de um [loop](loop--sm4---asm-.md) ou [ENDLOOP](endloop--sm4---asm-.md).</span><span class="sxs-lookup"><span data-stu-id="8bc06-107">**continue** can be used only inside a [loop](loop--sm4---asm-.md) or [endloop](endloop--sm4---asm-.md).</span></span>

<span data-ttu-id="8bc06-108">O exemplo a seguir mostra como usar a instrução **continue** .</span><span class="sxs-lookup"><span data-stu-id="8bc06-108">The following example shows how to use the **continue** instruction.</span></span>


```
                loop
                    if_na r0.x
                        break
                    endif
                    if_z r1.x
                        ...
                        continue
                    endif
                    ...
                endloop
```



<span data-ttu-id="8bc06-109">O formato do token contém o deslocamento da instrução de loop correspondente no sombreador como uma conveniência.</span><span class="sxs-lookup"><span data-stu-id="8bc06-109">The token format contains the offset of the corresponding loop instruction in the Shader as a convenience.</span></span>

<span data-ttu-id="8bc06-110">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="8bc06-110">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="8bc06-111">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="8bc06-111">Vertex Shader</span></span> | <span data-ttu-id="8bc06-112">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="8bc06-112">Geometry Shader</span></span> | <span data-ttu-id="8bc06-113">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="8bc06-113">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="8bc06-114">x</span><span class="sxs-lookup"><span data-stu-id="8bc06-114">x</span></span>             | <span data-ttu-id="8bc06-115">x</span><span class="sxs-lookup"><span data-stu-id="8bc06-115">x</span></span>               | <span data-ttu-id="8bc06-116">x</span><span class="sxs-lookup"><span data-stu-id="8bc06-116">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="8bc06-117">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="8bc06-117">Minimum Shader Model</span></span>

<span data-ttu-id="8bc06-118">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="8bc06-118">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="8bc06-119">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="8bc06-119">Shader Model</span></span>                                              | <span data-ttu-id="8bc06-120">Com suporte</span><span class="sxs-lookup"><span data-stu-id="8bc06-120">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="8bc06-121">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="8bc06-121">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="8bc06-122">sim</span><span class="sxs-lookup"><span data-stu-id="8bc06-122">yes</span></span>       |
| [<span data-ttu-id="8bc06-123">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="8bc06-123">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="8bc06-124">sim</span><span class="sxs-lookup"><span data-stu-id="8bc06-124">yes</span></span>       |
| [<span data-ttu-id="8bc06-125">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="8bc06-125">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="8bc06-126">sim</span><span class="sxs-lookup"><span data-stu-id="8bc06-126">yes</span></span>       |
| [<span data-ttu-id="8bc06-127">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8bc06-127">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="8bc06-128">não</span><span class="sxs-lookup"><span data-stu-id="8bc06-128">no</span></span>        |
| [<span data-ttu-id="8bc06-129">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8bc06-129">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="8bc06-130">não</span><span class="sxs-lookup"><span data-stu-id="8bc06-130">no</span></span>        |
| [<span data-ttu-id="8bc06-131">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8bc06-131">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="8bc06-132">não</span><span class="sxs-lookup"><span data-stu-id="8bc06-132">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="8bc06-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8bc06-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8bc06-134">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8bc06-134">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




