---
title: break_comp-vs
description: Interromper condicionalmente o loop atual no ENDLOOP-vs ou endrep-vs mais próximo.
ms.assetid: 01745e03-874a-4594-b6ab-12db22d0cb4a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 631998aeba6612d945495d8115a74d00f7e657c7
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103823450"
---
# <a name="break_comp---vs"></a><span data-ttu-id="b3d3d-103">interromper \_ comp-vs</span><span class="sxs-lookup"><span data-stu-id="b3d3d-103">break\_comp - vs</span></span>

<span data-ttu-id="b3d3d-104">Interromper condicionalmente o loop atual no [ENDLOOP-vs](endloop---vs.md) ou [endrep-vs](endrep---vs.md)mais próximo.</span><span class="sxs-lookup"><span data-stu-id="b3d3d-104">Conditionally break out of the current loop at the nearest [endloop - vs](endloop---vs.md) or [endrep - vs](endrep---vs.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b3d3d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b3d3d-105">Syntax</span></span>



| <span data-ttu-id="b3d3d-106">\_src0 de quebra de comp, src1</span><span class="sxs-lookup"><span data-stu-id="b3d3d-106">break\_comp src0, src1</span></span> |
|------------------------|



 

<span data-ttu-id="b3d3d-107">Em que:</span><span class="sxs-lookup"><span data-stu-id="b3d3d-107">Where:</span></span>

-   <span data-ttu-id="b3d3d-108">\_comp é uma comparação entre os dois registros de origem.</span><span class="sxs-lookup"><span data-stu-id="b3d3d-108">\_comp is a comparison between the two source registers.</span></span> <span data-ttu-id="b3d3d-109">Pode ser um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="b3d3d-109">It can be one of the following:</span></span> 

    | <span data-ttu-id="b3d3d-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="b3d3d-110">Syntax</span></span> | <span data-ttu-id="b3d3d-111">Comparação</span><span class="sxs-lookup"><span data-stu-id="b3d3d-111">Comparison</span></span>            |
    |--------|-----------------------|
    | <span data-ttu-id="b3d3d-112">\_gt</span><span class="sxs-lookup"><span data-stu-id="b3d3d-112">\_gt</span></span>   | <span data-ttu-id="b3d3d-113">Maior que</span><span class="sxs-lookup"><span data-stu-id="b3d3d-113">Greater than</span></span>          |
    | <span data-ttu-id="b3d3d-114">\_lt</span><span class="sxs-lookup"><span data-stu-id="b3d3d-114">\_lt</span></span>   | <span data-ttu-id="b3d3d-115">Menor que</span><span class="sxs-lookup"><span data-stu-id="b3d3d-115">Less than</span></span>             |
    | <span data-ttu-id="b3d3d-116">\_GE</span><span class="sxs-lookup"><span data-stu-id="b3d3d-116">\_ge</span></span>   | <span data-ttu-id="b3d3d-117">Maior ou igual</span><span class="sxs-lookup"><span data-stu-id="b3d3d-117">Greater than or equal</span></span> |
    | <span data-ttu-id="b3d3d-118">\_quivo</span><span class="sxs-lookup"><span data-stu-id="b3d3d-118">\_le</span></span>   | <span data-ttu-id="b3d3d-119">Inferior ou igual</span><span class="sxs-lookup"><span data-stu-id="b3d3d-119">Less than or equal</span></span>    |
    | <span data-ttu-id="b3d3d-120">\_EQ</span><span class="sxs-lookup"><span data-stu-id="b3d3d-120">\_eq</span></span>   | <span data-ttu-id="b3d3d-121">Igual a</span><span class="sxs-lookup"><span data-stu-id="b3d3d-121">Equal to</span></span>              |
    | <span data-ttu-id="b3d3d-122">\_m</span><span class="sxs-lookup"><span data-stu-id="b3d3d-122">\_ne</span></span>   | <span data-ttu-id="b3d3d-123">Não igual a</span><span class="sxs-lookup"><span data-stu-id="b3d3d-123">Not equal to</span></span>          |

    

     

-   <span data-ttu-id="b3d3d-124">src0 é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="b3d3d-124">src0 is a source register.</span></span> <span data-ttu-id="b3d3d-125">Replicate swizzle é necessário para selecionar um único componente.</span><span class="sxs-lookup"><span data-stu-id="b3d3d-125">Replicate swizzle is required to select a single component.</span></span>
-   <span data-ttu-id="b3d3d-126">src1 é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="b3d3d-126">src1 is a source register.</span></span> <span data-ttu-id="b3d3d-127">Replicate swizzle é necessário para selecionar um único componente.</span><span class="sxs-lookup"><span data-stu-id="b3d3d-127">Replicate swizzle is required to select a single component.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3d3d-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="b3d3d-128">Remarks</span></span>

<span data-ttu-id="b3d3d-129">Essa instrução tem suporte nas versões a seguir.</span><span class="sxs-lookup"><span data-stu-id="b3d3d-129">This instruction is supported in the following versions.</span></span>



| <span data-ttu-id="b3d3d-130">Versões do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="b3d3d-130">Vertex shader versions</span></span> | <span data-ttu-id="b3d3d-131">1\_1</span><span class="sxs-lookup"><span data-stu-id="b3d3d-131">1\_1</span></span> | <span data-ttu-id="b3d3d-132">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b3d3d-132">2\_0</span></span> | <span data-ttu-id="b3d3d-133">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="b3d3d-133">2\_x</span></span> | <span data-ttu-id="b3d3d-134">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="b3d3d-134">2\_sw</span></span> | <span data-ttu-id="b3d3d-135">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b3d3d-135">3\_0</span></span> | <span data-ttu-id="b3d3d-136">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="b3d3d-136">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="b3d3d-137">interromper \_ comp</span><span class="sxs-lookup"><span data-stu-id="b3d3d-137">break\_comp</span></span>            |      |      | <span data-ttu-id="b3d3d-138">x</span><span class="sxs-lookup"><span data-stu-id="b3d3d-138">x</span></span>    | <span data-ttu-id="b3d3d-139">x</span><span class="sxs-lookup"><span data-stu-id="b3d3d-139">x</span></span>     | <span data-ttu-id="b3d3d-140">x</span><span class="sxs-lookup"><span data-stu-id="b3d3d-140">x</span></span>    | <span data-ttu-id="b3d3d-141">x</span><span class="sxs-lookup"><span data-stu-id="b3d3d-141">x</span></span>     |



 

<span data-ttu-id="b3d3d-142">Quando a comparação for verdadeira, ela será interrompida no loop atual, conforme mostrado.</span><span class="sxs-lookup"><span data-stu-id="b3d3d-142">When the comparison is true, it breaks out of the current loop, as shown.</span></span>


```
if (src0 comparison src1)
   jump to the corresponding endloop or endrep instruction;
```



## <a name="related-topics"></a><span data-ttu-id="b3d3d-143">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b3d3d-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3d3d-144">Instruções do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="b3d3d-144">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




