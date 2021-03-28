---
title: break_comp-PS
description: Interromper o loop atual no ENDLOOP-PS ou endrep-PS mais próximo, com base em uma comparação por componente.
ms.assetid: d21e850f-05db-4a29-b15b-85bb1c1410d0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5088312a16102153ad78afffdcd9ea1275d34e0d
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104084265"
---
# <a name="break_comp---ps"></a><span data-ttu-id="b0939-103">interromper \_ comp-PS</span><span class="sxs-lookup"><span data-stu-id="b0939-103">break\_comp - ps</span></span>

<span data-ttu-id="b0939-104">Interromper o loop atual no [ENDLOOP-PS](endloop---ps.md) ou [endrep-PS](endrep---ps.md)mais próximo, com base em uma comparação por componente.</span><span class="sxs-lookup"><span data-stu-id="b0939-104">Break out of the current loop at the nearest [endloop - ps](endloop---ps.md) or [endrep - ps](endrep---ps.md), based on a per-component comparison.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0939-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b0939-105">Syntax</span></span>



| <span data-ttu-id="b0939-106">\_src0 de quebra de comp, src1</span><span class="sxs-lookup"><span data-stu-id="b0939-106">break\_comp src0, src1</span></span> |
|------------------------|



 

<span data-ttu-id="b0939-107">Em que:</span><span class="sxs-lookup"><span data-stu-id="b0939-107">Where:</span></span>

-   <span data-ttu-id="b0939-108">\_comp é uma comparação escalar (ou única) entre os dois registros de origem.</span><span class="sxs-lookup"><span data-stu-id="b0939-108">\_comp is a scalar (or single) comparison between the two source registers.</span></span> <span data-ttu-id="b0939-109">Pode ser um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="b0939-109">It can be one of the following:</span></span> 

    | <span data-ttu-id="b0939-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="b0939-110">Syntax</span></span> | <span data-ttu-id="b0939-111">Comparação</span><span class="sxs-lookup"><span data-stu-id="b0939-111">Comparison</span></span>            |
    |--------|-----------------------|
    | <span data-ttu-id="b0939-112">\_gt</span><span class="sxs-lookup"><span data-stu-id="b0939-112">\_gt</span></span>   | <span data-ttu-id="b0939-113">Maior que</span><span class="sxs-lookup"><span data-stu-id="b0939-113">Greater than</span></span>          |
    | <span data-ttu-id="b0939-114">\_lt</span><span class="sxs-lookup"><span data-stu-id="b0939-114">\_lt</span></span>   | <span data-ttu-id="b0939-115">Menor que</span><span class="sxs-lookup"><span data-stu-id="b0939-115">Less than</span></span>             |
    | <span data-ttu-id="b0939-116">\_GE</span><span class="sxs-lookup"><span data-stu-id="b0939-116">\_ge</span></span>   | <span data-ttu-id="b0939-117">Maior ou igual</span><span class="sxs-lookup"><span data-stu-id="b0939-117">Greater than or equal</span></span> |
    | <span data-ttu-id="b0939-118">\_quivo</span><span class="sxs-lookup"><span data-stu-id="b0939-118">\_le</span></span>   | <span data-ttu-id="b0939-119">Inferior ou igual</span><span class="sxs-lookup"><span data-stu-id="b0939-119">Less than or equal</span></span>    |
    | <span data-ttu-id="b0939-120">\_EQ</span><span class="sxs-lookup"><span data-stu-id="b0939-120">\_eq</span></span>   | <span data-ttu-id="b0939-121">Igual a</span><span class="sxs-lookup"><span data-stu-id="b0939-121">Equal to</span></span>              |
    | <span data-ttu-id="b0939-122">\_m</span><span class="sxs-lookup"><span data-stu-id="b0939-122">\_ne</span></span>   | <span data-ttu-id="b0939-123">Não igual a</span><span class="sxs-lookup"><span data-stu-id="b0939-123">Not equal to</span></span>          |

    

     

-   <span data-ttu-id="b0939-124">src0 é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="b0939-124">src0 is a source register.</span></span> <span data-ttu-id="b0939-125">Replicate swizzle será necessário se você selecionar um único componente.</span><span class="sxs-lookup"><span data-stu-id="b0939-125">Replicate swizzle is required if selecting a single component.</span></span>
-   <span data-ttu-id="b0939-126">src1 é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="b0939-126">src1 is a source register.</span></span> <span data-ttu-id="b0939-127">Replicate swizzle será necessário se você selecionar um único componente.</span><span class="sxs-lookup"><span data-stu-id="b0939-127">Replicate swizzle is required if selecting a single component.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0939-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="b0939-128">Remarks</span></span>

<span data-ttu-id="b0939-129">Essa instrução tem suporte nas versões a seguir.</span><span class="sxs-lookup"><span data-stu-id="b0939-129">This instruction is supported in the following versions.</span></span>



| <span data-ttu-id="b0939-130">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="b0939-130">Pixel shader versions</span></span> | <span data-ttu-id="b0939-131">1\_1</span><span class="sxs-lookup"><span data-stu-id="b0939-131">1\_1</span></span> | <span data-ttu-id="b0939-132">1\_2</span><span class="sxs-lookup"><span data-stu-id="b0939-132">1\_2</span></span> | <span data-ttu-id="b0939-133">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="b0939-133">1\_3</span></span> | <span data-ttu-id="b0939-134">1\_4</span><span class="sxs-lookup"><span data-stu-id="b0939-134">1\_4</span></span> | <span data-ttu-id="b0939-135">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b0939-135">2\_0</span></span> | <span data-ttu-id="b0939-136">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="b0939-136">2\_x</span></span> | <span data-ttu-id="b0939-137">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="b0939-137">2\_sw</span></span> | <span data-ttu-id="b0939-138">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b0939-138">3\_0</span></span> | <span data-ttu-id="b0939-139">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="b0939-139">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="b0939-140">interromper \_ comp</span><span class="sxs-lookup"><span data-stu-id="b0939-140">break\_comp</span></span>           |      |      |      |      |      | <span data-ttu-id="b0939-141">x</span><span class="sxs-lookup"><span data-stu-id="b0939-141">x</span></span>    | <span data-ttu-id="b0939-142">x</span><span class="sxs-lookup"><span data-stu-id="b0939-142">x</span></span>     | <span data-ttu-id="b0939-143">x</span><span class="sxs-lookup"><span data-stu-id="b0939-143">x</span></span>    | <span data-ttu-id="b0939-144">x</span><span class="sxs-lookup"><span data-stu-id="b0939-144">x</span></span>     |



 

<span data-ttu-id="b0939-145">Quando a comparação for verdadeira, ela será interrompida no loop atual, conforme mostrado.</span><span class="sxs-lookup"><span data-stu-id="b0939-145">When the comparison is true, it breaks out of the current loop, as shown.</span></span>


```
if (!(src0 comparison src1))
   jump to the corresponding endloop or endrep instruction;
```



## <a name="related-topics"></a><span data-ttu-id="b0939-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b0939-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0939-147">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="b0939-147">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




