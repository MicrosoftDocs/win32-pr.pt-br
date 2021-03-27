---
title: RET (sm4-ASM)
description: Instrução de retorno.
ms.assetid: 1B690036-99C5-441D-9DD3-E09D43E48AFF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d834cd9f32d6e38f40666ab235f705c0fc80513f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103638862"
---
# <a name="ret-sm4---asm"></a><span data-ttu-id="3179b-103">RET (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="3179b-103">ret (sm4 - asm)</span></span>

<span data-ttu-id="3179b-104">Instrução de retorno.</span><span class="sxs-lookup"><span data-stu-id="3179b-104">Return statement.</span></span>



| <span data-ttu-id="3179b-105">RET</span><span class="sxs-lookup"><span data-stu-id="3179b-105">ret</span></span> |
|-----|



 

## <a name="remarks"></a><span data-ttu-id="3179b-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="3179b-106">Remarks</span></span>

<span data-ttu-id="3179b-107">Se estiver dentro de uma sub-rotina, retorne à instrução após a chamada.</span><span class="sxs-lookup"><span data-stu-id="3179b-107">If within a subroutine, return to the instruction after the call.</span></span> <span data-ttu-id="3179b-108">Se não estiver dentro de uma sub-rotina, encerre a execução do programa.</span><span class="sxs-lookup"><span data-stu-id="3179b-108">If not inside a subroutine, terminate program execution.</span></span>

<span data-ttu-id="3179b-109">O exemplo a seguir mostra como usar essa instrução.</span><span class="sxs-lookup"><span data-stu-id="3179b-109">The following example shows how to use this instruction.</span></span>

``` syntax
 
               ...
                call l3
                ...
                ret
                label l3
                    ...
                ret
```

### <a name="restrictions"></a><span data-ttu-id="3179b-110">Restrições</span><span class="sxs-lookup"><span data-stu-id="3179b-110">Restrictions</span></span>

-   <span data-ttu-id="3179b-111">**RET** pode aparecer em qualquer lugar em um programa, várias vezes.</span><span class="sxs-lookup"><span data-stu-id="3179b-111">**ret** can appear anywhere in a program, any number of times.</span></span>
-   <span data-ttu-id="3179b-112">Se uma instrução de [rótulo](label--sm4---asm-.md) aparecer em um sombreador, ela deverá ser precedida por um comando **RET** que não esteja aninhado em nenhuma instrução de controle de fluxo.</span><span class="sxs-lookup"><span data-stu-id="3179b-112">If a [label](label--sm4---asm-.md) instruction appears in a Shader, it must be preceded by a **ret** command that is not nested in any flow control statements.</span></span>
-   <span data-ttu-id="3179b-113">Se houver sub-rotinas em um sombreador, a última instrução no sombreador deverá ser uma **RET**.</span><span class="sxs-lookup"><span data-stu-id="3179b-113">If there are subroutines in a Shader, the last instruction in the Shader must be a **ret**.</span></span>

<span data-ttu-id="3179b-114">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="3179b-114">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="3179b-115">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="3179b-115">Vertex Shader</span></span> | <span data-ttu-id="3179b-116">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="3179b-116">Geometry Shader</span></span> | <span data-ttu-id="3179b-117">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="3179b-117">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="3179b-118">x</span><span class="sxs-lookup"><span data-stu-id="3179b-118">x</span></span>             | <span data-ttu-id="3179b-119">x</span><span class="sxs-lookup"><span data-stu-id="3179b-119">x</span></span>               | <span data-ttu-id="3179b-120">x</span><span class="sxs-lookup"><span data-stu-id="3179b-120">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="3179b-121">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="3179b-121">Minimum Shader Model</span></span>

<span data-ttu-id="3179b-122">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="3179b-122">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="3179b-123">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="3179b-123">Shader Model</span></span>                                              | <span data-ttu-id="3179b-124">Com suporte</span><span class="sxs-lookup"><span data-stu-id="3179b-124">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="3179b-125">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="3179b-125">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="3179b-126">sim</span><span class="sxs-lookup"><span data-stu-id="3179b-126">yes</span></span>       |
| [<span data-ttu-id="3179b-127">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="3179b-127">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="3179b-128">sim</span><span class="sxs-lookup"><span data-stu-id="3179b-128">yes</span></span>       |
| [<span data-ttu-id="3179b-129">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="3179b-129">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="3179b-130">sim</span><span class="sxs-lookup"><span data-stu-id="3179b-130">yes</span></span>       |
| [<span data-ttu-id="3179b-131">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3179b-131">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="3179b-132">não</span><span class="sxs-lookup"><span data-stu-id="3179b-132">no</span></span>        |
| [<span data-ttu-id="3179b-133">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3179b-133">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="3179b-134">não</span><span class="sxs-lookup"><span data-stu-id="3179b-134">no</span></span>        |
| [<span data-ttu-id="3179b-135">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3179b-135">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="3179b-136">não</span><span class="sxs-lookup"><span data-stu-id="3179b-136">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="3179b-137">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3179b-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3179b-138">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3179b-138">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




