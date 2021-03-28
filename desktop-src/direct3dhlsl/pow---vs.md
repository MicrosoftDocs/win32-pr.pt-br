---
title: pow-vs
description: Src0 (ABS de precisão completa) src1. | pow-vs
ms.assetid: 51da86c6-bafa-42e0-90a5-d1545e39e600
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3263fa19015bc32c94ae714891c3bbb2128c9463
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104172662"
---
# <a name="pow---vs"></a><span data-ttu-id="101ad-104">pow-vs</span><span class="sxs-lookup"><span data-stu-id="101ad-104">pow - vs</span></span>

<span data-ttu-id="101ad-105">Src0 (ABS de precisão completa)<sup>src1</sup>.</span><span class="sxs-lookup"><span data-stu-id="101ad-105">Full precision abs(src0)<sup>src1</sup>.</span></span>

## <a name="syntax"></a><span data-ttu-id="101ad-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="101ad-106">Syntax</span></span>



| <span data-ttu-id="101ad-107">pow DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="101ad-107">pow dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="101ad-108">onde</span><span class="sxs-lookup"><span data-stu-id="101ad-108">where</span></span>

-   <span data-ttu-id="101ad-109">DST é o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="101ad-109">dst is the destination register.</span></span>
-   <span data-ttu-id="101ad-110">src0 é um registro de fonte de entrada.</span><span class="sxs-lookup"><span data-stu-id="101ad-110">src0 is an input source register.</span></span> <span data-ttu-id="101ad-111">O registro de origem requer uso explícito de replicate swizzle, ou seja, exatamente um dos componentes. x,. y,. z,. w swizzle (ou. r,. g,. b,. equivalentes) devem ser especificados.</span><span class="sxs-lookup"><span data-stu-id="101ad-111">Source register requires explicit use of replicate swizzle, that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>
-   <span data-ttu-id="101ad-112">src1 é um registro de fonte de entrada.</span><span class="sxs-lookup"><span data-stu-id="101ad-112">src1 is an input source register.</span></span> <span data-ttu-id="101ad-113">O registro de origem requer uso explícito de replicate swizzle, ou seja, exatamente um dos componentes. x,. y,. z,. w swizzle (ou. r,. g,. b,. equivalentes) devem ser especificados.</span><span class="sxs-lookup"><span data-stu-id="101ad-113">Source register requires explicit use of replicate swizzle, that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="101ad-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="101ad-114">Remarks</span></span>



| <span data-ttu-id="101ad-115">Versões do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="101ad-115">Vertex shader versions</span></span> | <span data-ttu-id="101ad-116">1\_1</span><span class="sxs-lookup"><span data-stu-id="101ad-116">1\_1</span></span> | <span data-ttu-id="101ad-117">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="101ad-117">2\_0</span></span> | <span data-ttu-id="101ad-118">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="101ad-118">2\_x</span></span> | <span data-ttu-id="101ad-119">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="101ad-119">2\_sw</span></span> | <span data-ttu-id="101ad-120">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="101ad-120">3\_0</span></span> | <span data-ttu-id="101ad-121">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="101ad-121">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="101ad-122">pow</span><span class="sxs-lookup"><span data-stu-id="101ad-122">pow</span></span>                    |      | <span data-ttu-id="101ad-123">x</span><span class="sxs-lookup"><span data-stu-id="101ad-123">x</span></span>    | <span data-ttu-id="101ad-124">x</span><span class="sxs-lookup"><span data-stu-id="101ad-124">x</span></span>    | <span data-ttu-id="101ad-125">x</span><span class="sxs-lookup"><span data-stu-id="101ad-125">x</span></span>     | <span data-ttu-id="101ad-126">x</span><span class="sxs-lookup"><span data-stu-id="101ad-126">x</span></span>    | <span data-ttu-id="101ad-127">x</span><span class="sxs-lookup"><span data-stu-id="101ad-127">x</span></span>     |



 

<span data-ttu-id="101ad-128">Essa instrução funciona como mostrado aqui.</span><span class="sxs-lookup"><span data-stu-id="101ad-128">This instruction works as shown here.</span></span>


```
dest = pow(abs(src0), src1);
```



<span data-ttu-id="101ad-129">Essa é uma instrução escalar, portanto, os registros de origem devem ter replicar swizzles para indicar quais canais são usados.</span><span class="sxs-lookup"><span data-stu-id="101ad-129">This is a scalar instruction, therefore the source registers should have replicate swizzles to indicate which channels are used.</span></span>

<span data-ttu-id="101ad-130">O resultado escalar é replicado para todos os quatro canais de saída.</span><span class="sxs-lookup"><span data-stu-id="101ad-130">The scalar result is replicated to all four output channels.</span></span>

<span data-ttu-id="101ad-131">Essa instrução pode ser expandida como exp ( \* log src1 (src0)).</span><span class="sxs-lookup"><span data-stu-id="101ad-131">This instruction could be expanded as exp(src1 \* log(src0)).</span></span>

<span data-ttu-id="101ad-132">A precisão não é inferior a 15 bits.</span><span class="sxs-lookup"><span data-stu-id="101ad-132">Precision is not lower than 15 bits.</span></span>

<span data-ttu-id="101ad-133">O registro do dest deve ser um registro temporário e não deve ser o mesmo registrado como src1.</span><span class="sxs-lookup"><span data-stu-id="101ad-133">The dest register should be a temporary register, and should not be the same register as src1.</span></span>

## <a name="related-topics"></a><span data-ttu-id="101ad-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="101ad-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="101ad-135">Instruções do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="101ad-135">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




