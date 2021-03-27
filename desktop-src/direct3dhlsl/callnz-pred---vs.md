---
title: callnz Pred – vs
description: Chame se não for zero, com um predicado. Executa uma chamada condicional para a instrução marcada pelo índice de rótulo. Predicação usa um valor booliano para determinar se não deve executar a instrução.
ms.assetid: 3417f3e3-7e73-4131-8069-09c0de1469a7
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e3c3de590dfee56013c76402c840a959e8f9306c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104006888"
---
# <a name="callnz-pred---vs"></a><span data-ttu-id="7cb61-105">callnz Pred – vs</span><span class="sxs-lookup"><span data-stu-id="7cb61-105">callnz pred - vs</span></span>

<span data-ttu-id="7cb61-106">Chame se não for zero, com um predicado.</span><span class="sxs-lookup"><span data-stu-id="7cb61-106">Call if not zero, with a predicate.</span></span> <span data-ttu-id="7cb61-107">Executa uma chamada condicional para a instrução marcada pelo índice de rótulo.</span><span class="sxs-lookup"><span data-stu-id="7cb61-107">Performs a conditional call to the instruction marked by the label index.</span></span> <span data-ttu-id="7cb61-108">Predicação usa um valor booliano para determinar se não deve executar a instrução.</span><span class="sxs-lookup"><span data-stu-id="7cb61-108">Predication uses a boolean value to determine whether of not to perform the instruction.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cb61-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="7cb61-109">Syntax</span></span>



| <span data-ttu-id="7cb61-110">callnz l \# , \[ ! \] P0. w.x.y.</span><span class="sxs-lookup"><span data-stu-id="7cb61-110">callnz l\#, \[!\]p0.{x\</span></span>|<span data-ttu-id="7cb61-111">Iar</span><span class="sxs-lookup"><span data-stu-id="7cb61-111">y\</span></span>|<span data-ttu-id="7cb61-112">z</span><span class="sxs-lookup"><span data-stu-id="7cb61-112">z\</span></span>|<span data-ttu-id="7cb61-113">Mostrar</span><span class="sxs-lookup"><span data-stu-id="7cb61-113">w}</span></span> |
|----------------------------------|



 

<span data-ttu-id="7cb61-114">em que:</span><span class="sxs-lookup"><span data-stu-id="7cb61-114">where:</span></span>

-   <span data-ttu-id="7cb61-115">l \# é um [rótulo-vs](label---vs.md) marcando o início da sub-rotina a ser chamada.</span><span class="sxs-lookup"><span data-stu-id="7cb61-115">l\# is a [label - vs](label---vs.md) marking the beginning of the subroutine to be called.</span></span>
-   <span data-ttu-id="7cb61-116">\[!\] é um modificador opcional de negação.</span><span class="sxs-lookup"><span data-stu-id="7cb61-116">\[!\] is an optional negate modifier.</span></span>
-   <span data-ttu-id="7cb61-117">P0 é o [registro de predicado](dx9-graphics-reference-asm-vs-registers-predicate.md).</span><span class="sxs-lookup"><span data-stu-id="7cb61-117">p0 is the [Predicate Register](dx9-graphics-reference-asm-vs-registers-predicate.md).</span></span>
-   <span data-ttu-id="7cb61-118">{x \| y \| z \| w} é o swizzle de replicação necessário em P0.</span><span class="sxs-lookup"><span data-stu-id="7cb61-118">{x\|y\|z\|w} is the required replicate swizzle on p0.</span></span>

## <a name="remarks"></a><span data-ttu-id="7cb61-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="7cb61-119">Remarks</span></span>



| <span data-ttu-id="7cb61-120">Versões do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="7cb61-120">Vertex shader versions</span></span> | <span data-ttu-id="7cb61-121">1\_1</span><span class="sxs-lookup"><span data-stu-id="7cb61-121">1\_1</span></span> | <span data-ttu-id="7cb61-122">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7cb61-122">2\_0</span></span> | <span data-ttu-id="7cb61-123">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="7cb61-123">2\_x</span></span> | <span data-ttu-id="7cb61-124">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="7cb61-124">2\_sw</span></span> | <span data-ttu-id="7cb61-125">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7cb61-125">3\_0</span></span> | <span data-ttu-id="7cb61-126">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="7cb61-126">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="7cb61-127">callnz Pred</span><span class="sxs-lookup"><span data-stu-id="7cb61-127">callnz pred</span></span>            |      |      | <span data-ttu-id="7cb61-128">x</span><span class="sxs-lookup"><span data-stu-id="7cb61-128">x</span></span>    | <span data-ttu-id="7cb61-129">x</span><span class="sxs-lookup"><span data-stu-id="7cb61-129">x</span></span>     | <span data-ttu-id="7cb61-130">x</span><span class="sxs-lookup"><span data-stu-id="7cb61-130">x</span></span>    | <span data-ttu-id="7cb61-131">x</span><span class="sxs-lookup"><span data-stu-id="7cb61-131">x</span></span>     |



 

<span data-ttu-id="7cb61-132">Essa instrução faz o seguinte:</span><span class="sxs-lookup"><span data-stu-id="7cb61-132">This instruction does the following:</span></span>


```
if (specified register component is not zero)
{
    Push address of the next instruction to the return address stack.
    Continue execution from the instruction marked by the label.
}
```



<span data-ttu-id="7cb61-133">Essa instrução consome um slot de instrução do sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="7cb61-133">This instruction consumes one vertex shader instruction slot.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7cb61-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7cb61-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7cb61-135">Instruções do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="7cb61-135">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




