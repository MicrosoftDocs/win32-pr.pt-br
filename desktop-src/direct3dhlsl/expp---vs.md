---
title: expp-vs
description: Fornece precisão parcial exponencial 2x.
ms.assetid: ac080ac9-5dfd-49e4-92ea-50bb26844ff6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0d57e2723c90eee8df728aa540baeab86932e773
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103638870"
---
# <a name="expp---vs"></a><span data-ttu-id="76e8e-103">expp-vs</span><span class="sxs-lookup"><span data-stu-id="76e8e-103">expp - vs</span></span>

<span data-ttu-id="76e8e-104">Fornece o exponencial de precisão parcial 2<sup>x</sup>.</span><span class="sxs-lookup"><span data-stu-id="76e8e-104">Provides partial precision exponential 2<sup>x</sup>.</span></span>

## <a name="syntax"></a><span data-ttu-id="76e8e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="76e8e-105">Syntax</span></span>



| <span data-ttu-id="76e8e-106">expp DST, src. w.x.y.</span><span class="sxs-lookup"><span data-stu-id="76e8e-106">expp dst, src.{x\</span></span>|<span data-ttu-id="76e8e-107">Iar</span><span class="sxs-lookup"><span data-stu-id="76e8e-107">y\</span></span>|<span data-ttu-id="76e8e-108">z</span><span class="sxs-lookup"><span data-stu-id="76e8e-108">z\</span></span>|<span data-ttu-id="76e8e-109">Mostrar</span><span class="sxs-lookup"><span data-stu-id="76e8e-109">w}</span></span> |
|----------------------------|



 

<span data-ttu-id="76e8e-110">Em que:</span><span class="sxs-lookup"><span data-stu-id="76e8e-110">Where:</span></span>

-   <span data-ttu-id="76e8e-111">DST é o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="76e8e-111">dst is the destination register.</span></span>
-   <span data-ttu-id="76e8e-112">src é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="76e8e-112">src is a source register.</span></span> <span data-ttu-id="76e8e-113">O registro de origem requer uso explícito de replicate swizzle, ou seja, exatamente um dos componentes. x,. y,. z,. w swizzle (ou. r,. g,. b,. equivalentes) devem ser especificados.</span><span class="sxs-lookup"><span data-stu-id="76e8e-113">Source register requires explicit use of replicate swizzle, that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>
-   <span data-ttu-id="76e8e-114">{x \| y \| z \| w} é o swizzle de replicação necessário no registro de origem.</span><span class="sxs-lookup"><span data-stu-id="76e8e-114">{x\|y\|z\|w} is the required replicate swizzle on source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="76e8e-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="76e8e-115">Remarks</span></span>



| <span data-ttu-id="76e8e-116">Versões do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="76e8e-116">Vertex shader versions</span></span> | <span data-ttu-id="76e8e-117">1\_1</span><span class="sxs-lookup"><span data-stu-id="76e8e-117">1\_1</span></span> | <span data-ttu-id="76e8e-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="76e8e-118">2\_0</span></span> | <span data-ttu-id="76e8e-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="76e8e-119">2\_x</span></span> | <span data-ttu-id="76e8e-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="76e8e-120">2\_sw</span></span> | <span data-ttu-id="76e8e-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="76e8e-121">3\_0</span></span> | <span data-ttu-id="76e8e-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="76e8e-122">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="76e8e-123">expp</span><span class="sxs-lookup"><span data-stu-id="76e8e-123">expp</span></span>                   | <span data-ttu-id="76e8e-124">x</span><span class="sxs-lookup"><span data-stu-id="76e8e-124">x</span></span>    | <span data-ttu-id="76e8e-125">x</span><span class="sxs-lookup"><span data-stu-id="76e8e-125">x</span></span>    | <span data-ttu-id="76e8e-126">x</span><span class="sxs-lookup"><span data-stu-id="76e8e-126">x</span></span>    | <span data-ttu-id="76e8e-127">x</span><span class="sxs-lookup"><span data-stu-id="76e8e-127">x</span></span>     | <span data-ttu-id="76e8e-128">x</span><span class="sxs-lookup"><span data-stu-id="76e8e-128">x</span></span>    | <span data-ttu-id="76e8e-129">x</span><span class="sxs-lookup"><span data-stu-id="76e8e-129">x</span></span>     |



 

### <a name="vs_1_1"></a><span data-ttu-id="76e8e-130">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="76e8e-130">vs\_1\_1</span></span>

<span data-ttu-id="76e8e-131">A instrução [exp-vs](exp---vs.md) Opera de maneira diferente, dependendo das versões do sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="76e8e-131">The [exp - vs](exp---vs.md) instruction operates differently depending on vertex shader versions.</span></span>

<span data-ttu-id="76e8e-132">No vs \_ 1 \_ 1, a instrução expp fornece os seguintes resultados:</span><span class="sxs-lookup"><span data-stu-id="76e8e-132">In vs\_1\_1, the expp instruction gives the following results:</span></span>


```
v = the scalar value from the source register with a replicate swizzle

dest.x = pow(2, floor(v))
dest.y = v - floor(v)
dest.z = pow(2, v) (partial-precision)
dest.w = 1
```



<span data-ttu-id="76e8e-133">No vs \_ 2 \_ 0 e superior, a instrução expp fornece os seguintes resultados:</span><span class="sxs-lookup"><span data-stu-id="76e8e-133">In vs\_2\_0 and up, the expp instruction gives the following results:</span></span>


```
v = the scalar value from the source register with a replicate swizzle

dest.x = dest.y = dest.z = dest.y = pow(2, v) (partial-precision)
```



### <a name="vs_2_0"></a><span data-ttu-id="76e8e-134">vs \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="76e8e-134">vs\_2\_0</span></span>

<span data-ttu-id="76e8e-135">No vs \_ 2 \_ 0 e superior, a instrução funciona da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="76e8e-135">In vs\_2\_0 and up, the instruction works like this:</span></span>


```
float V = the scalar value from the source register with a replicate swizzle

dest.x = dest.y = dest.z = dest.y = pow( 2, V ) (partial-precision)
```



<span data-ttu-id="76e8e-136">A instrução fornece pelo menos 10 bits de precisão.</span><span class="sxs-lookup"><span data-stu-id="76e8e-136">The instruction provides at least 10 bits of precision.</span></span>

## <a name="related-topics"></a><span data-ttu-id="76e8e-137">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="76e8e-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76e8e-138">Instruções do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="76e8e-138">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




