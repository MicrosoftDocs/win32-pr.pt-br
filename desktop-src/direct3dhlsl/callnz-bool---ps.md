---
title: callnz bool-PS
description: Chamar se não for zero. Executa uma chamada condicional para a instrução marcada pelo índice de rótulo. | callnz bool-PS
ms.assetid: 1b9ff276-c2b8-46cc-96ac-a5b5455c5cc0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0516e62ce07c60866715591bc59123f38dc5c272
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104989259"
---
# <a name="callnz-bool---ps"></a><span data-ttu-id="c2ca5-105">callnz bool-PS</span><span class="sxs-lookup"><span data-stu-id="c2ca5-105">callnz bool - ps</span></span>

<span data-ttu-id="c2ca5-106">Chamar se não for zero.</span><span class="sxs-lookup"><span data-stu-id="c2ca5-106">Call if not zero.</span></span> <span data-ttu-id="c2ca5-107">Executa uma chamada condicional para a instrução marcada pelo índice de rótulo.</span><span class="sxs-lookup"><span data-stu-id="c2ca5-107">Performs a conditional call to the instruction marked by the label index.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2ca5-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c2ca5-108">Syntax</span></span>



| <span data-ttu-id="c2ca5-109">callnz l \# , \[ ! \] b\#</span><span class="sxs-lookup"><span data-stu-id="c2ca5-109">callnz l\#, \[!\]b\#</span></span> |
|----------------------|



 

<span data-ttu-id="c2ca5-110">Em que:</span><span class="sxs-lookup"><span data-stu-id="c2ca5-110">Where:</span></span>

-   <span data-ttu-id="c2ca5-111">l \# é um [rótulo-PS](label---ps.md) marcando o início da sub-rotina a ser chamada.</span><span class="sxs-lookup"><span data-stu-id="c2ca5-111">l\# is a [label - ps](label---ps.md) marking the beginning of the subroutine to be called.</span></span>
-   <span data-ttu-id="c2ca5-112">\[!\] é um modificador opcional de negação.</span><span class="sxs-lookup"><span data-stu-id="c2ca5-112">\[!\] is an optional negate modifier.</span></span>
-   <span data-ttu-id="c2ca5-113">b \# identifica um [registro booliano constante](dx9-graphics-reference-asm-ps-registers-constant-boolean.md).</span><span class="sxs-lookup"><span data-stu-id="c2ca5-113">b\# identifies a [Constant Boolean Register](dx9-graphics-reference-asm-ps-registers-constant-boolean.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c2ca5-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="c2ca5-114">Remarks</span></span>



| <span data-ttu-id="c2ca5-115">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="c2ca5-115">Pixel shader versions</span></span> | <span data-ttu-id="c2ca5-116">1\_1</span><span class="sxs-lookup"><span data-stu-id="c2ca5-116">1\_1</span></span> | <span data-ttu-id="c2ca5-117">1\_2</span><span class="sxs-lookup"><span data-stu-id="c2ca5-117">1\_2</span></span> | <span data-ttu-id="c2ca5-118">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="c2ca5-118">1\_3</span></span> | <span data-ttu-id="c2ca5-119">1\_4</span><span class="sxs-lookup"><span data-stu-id="c2ca5-119">1\_4</span></span> | <span data-ttu-id="c2ca5-120">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c2ca5-120">2\_0</span></span> | <span data-ttu-id="c2ca5-121">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="c2ca5-121">2\_x</span></span> | <span data-ttu-id="c2ca5-122">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="c2ca5-122">2\_sw</span></span> | <span data-ttu-id="c2ca5-123">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c2ca5-123">3\_0</span></span> | <span data-ttu-id="c2ca5-124">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="c2ca5-124">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="c2ca5-125">bool callnz</span><span class="sxs-lookup"><span data-stu-id="c2ca5-125">callnz bool</span></span>           |      |      |      |      |      | <span data-ttu-id="c2ca5-126">x</span><span class="sxs-lookup"><span data-stu-id="c2ca5-126">x</span></span>    | <span data-ttu-id="c2ca5-127">x</span><span class="sxs-lookup"><span data-stu-id="c2ca5-127">x</span></span>     | <span data-ttu-id="c2ca5-128">x</span><span class="sxs-lookup"><span data-stu-id="c2ca5-128">x</span></span>    | <span data-ttu-id="c2ca5-129">x</span><span class="sxs-lookup"><span data-stu-id="c2ca5-129">x</span></span>     |



 

<span data-ttu-id="c2ca5-130">Essa instrução faz o seguinte:</span><span class="sxs-lookup"><span data-stu-id="c2ca5-130">This instruction does the following:</span></span>


```
if (specified Boolean register is not zero)
{
    Push address of the next instruction to the return address stack
    Continue execution from the instruction marked by the label
}
```



## <a name="related-topics"></a><span data-ttu-id="c2ca5-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c2ca5-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2ca5-132">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="c2ca5-132">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




