---
title: callnz Pred-PS
description: Chame com um predicado, se não for zero. Executa uma chamada condicional para a instrução marcada pelo índice de rótulo. Predicação usa um valor booliano para determinar se não deve executar a instrução.
ms.assetid: 9c839fc7-8b4d-4ca1-b30f-5c3f8fb45eae
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a04bd4b1bfa16d965a90b66e3956674ecb112590
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103916873"
---
# <a name="callnz-pred---ps"></a><span data-ttu-id="1bad8-105">callnz Pred-PS</span><span class="sxs-lookup"><span data-stu-id="1bad8-105">callnz pred - ps</span></span>

<span data-ttu-id="1bad8-106">Chame com um predicado, se não for zero.</span><span class="sxs-lookup"><span data-stu-id="1bad8-106">Call with a predicate, if not zero.</span></span> <span data-ttu-id="1bad8-107">Executa uma chamada condicional para a instrução marcada pelo índice de rótulo.</span><span class="sxs-lookup"><span data-stu-id="1bad8-107">Performs a conditional call to the instruction marked by the label index.</span></span> <span data-ttu-id="1bad8-108">Predicação usa um valor booliano para determinar se não deve executar a instrução.</span><span class="sxs-lookup"><span data-stu-id="1bad8-108">Predication uses a Boolean value to determine whether of not to perform the instruction.</span></span>

## <a name="syntax"></a><span data-ttu-id="1bad8-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="1bad8-109">Syntax</span></span>



| <span data-ttu-id="1bad8-110">callnz l \# , \[ ! \] P0. w.x.y.</span><span class="sxs-lookup"><span data-stu-id="1bad8-110">callnz l\#, \[!\]p0.{x\</span></span>|<span data-ttu-id="1bad8-111">Iar</span><span class="sxs-lookup"><span data-stu-id="1bad8-111">y\</span></span>|<span data-ttu-id="1bad8-112">z</span><span class="sxs-lookup"><span data-stu-id="1bad8-112">z\</span></span>|<span data-ttu-id="1bad8-113">Mostrar</span><span class="sxs-lookup"><span data-stu-id="1bad8-113">w}</span></span> |
|----------------------------------|



 

<span data-ttu-id="1bad8-114">Em que:</span><span class="sxs-lookup"><span data-stu-id="1bad8-114">Where:</span></span>

-   <span data-ttu-id="1bad8-115">em que l \# é um [rótulo-PS](label---ps.md) marcando o início da sub-rotina a ser chamada.</span><span class="sxs-lookup"><span data-stu-id="1bad8-115">where l\# is a [label - ps](label---ps.md) marking the beginning of the subroutine to be called.</span></span>
-   <span data-ttu-id="1bad8-116">\[!\] é um modificador opcional de negação.</span><span class="sxs-lookup"><span data-stu-id="1bad8-116">\[!\] is an optional negate modifier.</span></span>
-   <span data-ttu-id="1bad8-117">P0 é o registro de predicado.</span><span class="sxs-lookup"><span data-stu-id="1bad8-117">p0 is the predicate register.</span></span> <span data-ttu-id="1bad8-118">Consulte [registro de predicado](dx9-graphics-reference-asm-ps-registers-predicate.md).</span><span class="sxs-lookup"><span data-stu-id="1bad8-118">See [Predicate Register](dx9-graphics-reference-asm-ps-registers-predicate.md).</span></span>
-   <span data-ttu-id="1bad8-119">{x \| y \| z \| w} é o swizzle de replicação necessário em P0.</span><span class="sxs-lookup"><span data-stu-id="1bad8-119">{x\|y\|z\|w} is the required replicate swizzle on p0.</span></span>

## <a name="remarks"></a><span data-ttu-id="1bad8-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="1bad8-120">Remarks</span></span>



| <span data-ttu-id="1bad8-121">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="1bad8-121">Pixel shader versions</span></span> | <span data-ttu-id="1bad8-122">1\_1</span><span class="sxs-lookup"><span data-stu-id="1bad8-122">1\_1</span></span> | <span data-ttu-id="1bad8-123">1\_2</span><span class="sxs-lookup"><span data-stu-id="1bad8-123">1\_2</span></span> | <span data-ttu-id="1bad8-124">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="1bad8-124">1\_3</span></span> | <span data-ttu-id="1bad8-125">1\_4</span><span class="sxs-lookup"><span data-stu-id="1bad8-125">1\_4</span></span> | <span data-ttu-id="1bad8-126">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="1bad8-126">2\_0</span></span> | <span data-ttu-id="1bad8-127">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="1bad8-127">2\_x</span></span> | <span data-ttu-id="1bad8-128">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="1bad8-128">2\_sw</span></span> | <span data-ttu-id="1bad8-129">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="1bad8-129">3\_0</span></span> | <span data-ttu-id="1bad8-130">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="1bad8-130">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="1bad8-131">callnz Pred</span><span class="sxs-lookup"><span data-stu-id="1bad8-131">callnz pred</span></span>           |      |      |      |      |      | <span data-ttu-id="1bad8-132">x</span><span class="sxs-lookup"><span data-stu-id="1bad8-132">x</span></span>    | <span data-ttu-id="1bad8-133">x</span><span class="sxs-lookup"><span data-stu-id="1bad8-133">x</span></span>     | <span data-ttu-id="1bad8-134">x</span><span class="sxs-lookup"><span data-stu-id="1bad8-134">x</span></span>    | <span data-ttu-id="1bad8-135">x</span><span class="sxs-lookup"><span data-stu-id="1bad8-135">x</span></span>     |



 

<span data-ttu-id="1bad8-136">Essa instrução faz o seguinte:</span><span class="sxs-lookup"><span data-stu-id="1bad8-136">This instruction does the following:</span></span>


```
if (specified register component is not zero)
{
    Push address of the next instruction to the return address stack
    Continue execution from the instruction marked by the label
}
```



## <a name="related-topics"></a><span data-ttu-id="1bad8-137">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1bad8-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1bad8-138">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="1bad8-138">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




