---
title: callnz bool-vs
description: Chamar se não for zero. Executa uma chamada condicional para a instrução marcada pelo índice de rótulo. | callnz bool-vs
ms.assetid: 9be030b9-fa21-459f-bd6c-f34ad6f177fc
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f3932f4c5d50445b3220a0460a5c434a1ff8aae4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104989258"
---
# <a name="callnz-bool---vs"></a><span data-ttu-id="31610-105">callnz bool-vs</span><span class="sxs-lookup"><span data-stu-id="31610-105">callnz bool - vs</span></span>

<span data-ttu-id="31610-106">Chamar se não for zero.</span><span class="sxs-lookup"><span data-stu-id="31610-106">Call if not zero.</span></span> <span data-ttu-id="31610-107">Executa uma chamada condicional para a instrução marcada pelo índice de rótulo.</span><span class="sxs-lookup"><span data-stu-id="31610-107">Performs a conditional call to the instruction marked by the label index.</span></span>

## <a name="syntax"></a><span data-ttu-id="31610-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="31610-108">Syntax</span></span>



| <span data-ttu-id="31610-109">callnz l \# , \[ ! \] b\#</span><span class="sxs-lookup"><span data-stu-id="31610-109">callnz l\#, \[!\]b\#</span></span> |
|----------------------|



 

<span data-ttu-id="31610-110">em que:</span><span class="sxs-lookup"><span data-stu-id="31610-110">where:</span></span>

-   <span data-ttu-id="31610-111">Onde l \# é um [rótulo-vs](label---vs.md) marcando o início da sub-rotina a ser chamada.</span><span class="sxs-lookup"><span data-stu-id="31610-111">where l\# is a [label - vs](label---vs.md) marking the beginning of the subroutine to be called.</span></span>
-   <span data-ttu-id="31610-112">\[!\] é o modificador booliano NOT opcional.</span><span class="sxs-lookup"><span data-stu-id="31610-112">\[!\] is the optional boolean NOT modifier.</span></span>
-   <span data-ttu-id="31610-113">b \# identifica um [registro booliano constante](dx9-graphics-reference-asm-vs-registers-constant-boolean.md).</span><span class="sxs-lookup"><span data-stu-id="31610-113">b\# identifies a [Constant Boolean Register](dx9-graphics-reference-asm-vs-registers-constant-boolean.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="31610-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="31610-114">Remarks</span></span>



| <span data-ttu-id="31610-115">Versões do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="31610-115">Vertex shader versions</span></span> | <span data-ttu-id="31610-116">1\_1</span><span class="sxs-lookup"><span data-stu-id="31610-116">1\_1</span></span> | <span data-ttu-id="31610-117">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="31610-117">2\_0</span></span> | <span data-ttu-id="31610-118">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="31610-118">2\_x</span></span> | <span data-ttu-id="31610-119">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="31610-119">2\_sw</span></span> | <span data-ttu-id="31610-120">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="31610-120">3\_0</span></span> | <span data-ttu-id="31610-121">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="31610-121">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="31610-122">bool callnz</span><span class="sxs-lookup"><span data-stu-id="31610-122">callnz bool</span></span>            |      | <span data-ttu-id="31610-123">x</span><span class="sxs-lookup"><span data-stu-id="31610-123">x</span></span>    | <span data-ttu-id="31610-124">x</span><span class="sxs-lookup"><span data-stu-id="31610-124">x</span></span>    | <span data-ttu-id="31610-125">x</span><span class="sxs-lookup"><span data-stu-id="31610-125">x</span></span>     | <span data-ttu-id="31610-126">x</span><span class="sxs-lookup"><span data-stu-id="31610-126">x</span></span>    | <span data-ttu-id="31610-127">x</span><span class="sxs-lookup"><span data-stu-id="31610-127">x</span></span>     |



 

<span data-ttu-id="31610-128">Essa instrução faz o seguinte:</span><span class="sxs-lookup"><span data-stu-id="31610-128">This instruction does the following:</span></span>


```
if (specified boolean register is not zero)
{
    Push address of the next instruction to the return address stack.
    Continue execution from the instruction marked by the label.
}
```



<span data-ttu-id="31610-129">Essa instrução consome um slot de instrução do sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="31610-129">This instruction consumes one vertex shader instruction slot.</span></span>

## <a name="related-topics"></a><span data-ttu-id="31610-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="31610-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="31610-131">Instruções do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="31610-131">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




