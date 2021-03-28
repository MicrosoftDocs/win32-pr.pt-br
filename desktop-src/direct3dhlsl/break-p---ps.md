---
title: breakp-PS
description: Interromper condicionalmente o loop atual no ENDLOOP-PS ou endrep-PS mais próximo. Use um dos componentes de registro de predicado como uma condição para determinar se deseja ou não realizar a instrução.
ms.assetid: be219239-fccb-4561-8b71-083c47ba915b
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6e358debb2377f08574997acd96c11f83d32e66c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104365244"
---
# <a name="breakp---ps"></a><span data-ttu-id="e1434-104">breakp-PS</span><span class="sxs-lookup"><span data-stu-id="e1434-104">breakp - ps</span></span>

<span data-ttu-id="e1434-105">Interromper condicionalmente o loop atual no [ENDLOOP-PS](endloop---ps.md) ou [endrep-PS](endrep---ps.md)mais próximo.</span><span class="sxs-lookup"><span data-stu-id="e1434-105">Conditionally break out of the current loop at the nearest [endloop - ps](endloop---ps.md) or [endrep - ps](endrep---ps.md).</span></span> <span data-ttu-id="e1434-106">Use um dos componentes de registro de predicado como uma condição para determinar se deseja ou não realizar a instrução.</span><span class="sxs-lookup"><span data-stu-id="e1434-106">Use one of the components of the predicate register as a condition to determine whether or not to perform the instruction.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1434-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e1434-107">Syntax</span></span>



| <span data-ttu-id="e1434-108">breakp \[ ! \] P0. w.x.y.</span><span class="sxs-lookup"><span data-stu-id="e1434-108">breakp \[!\]p0.{x\</span></span>|<span data-ttu-id="e1434-109">Iar</span><span class="sxs-lookup"><span data-stu-id="e1434-109">y\</span></span>|<span data-ttu-id="e1434-110">z</span><span class="sxs-lookup"><span data-stu-id="e1434-110">z\</span></span>|<span data-ttu-id="e1434-111">Mostrar</span><span class="sxs-lookup"><span data-stu-id="e1434-111">w}</span></span> |
|-----------------------------|



 

<span data-ttu-id="e1434-112">Em que:</span><span class="sxs-lookup"><span data-stu-id="e1434-112">Where:</span></span>

-   <span data-ttu-id="e1434-113">\[!\] é um modificador opcional de negação.</span><span class="sxs-lookup"><span data-stu-id="e1434-113">\[!\] is an optional negate modifier.</span></span>
-   <span data-ttu-id="e1434-114">P0 é o [registro de predicado](dx9-graphics-reference-asm-ps-registers-predicate.md).</span><span class="sxs-lookup"><span data-stu-id="e1434-114">p0 is the [Predicate Register](dx9-graphics-reference-asm-ps-registers-predicate.md).</span></span>
-   <span data-ttu-id="e1434-115">{x \| y \| z \| w} é o swizzle de replicação necessário em P0.</span><span class="sxs-lookup"><span data-stu-id="e1434-115">{x\|y\|z\|w} is the required replicate swizzle on p0.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1434-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="e1434-116">Remarks</span></span>



| <span data-ttu-id="e1434-117">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="e1434-117">Pixel shader versions</span></span> | <span data-ttu-id="e1434-118">1\_1</span><span class="sxs-lookup"><span data-stu-id="e1434-118">1\_1</span></span> | <span data-ttu-id="e1434-119">1\_2</span><span class="sxs-lookup"><span data-stu-id="e1434-119">1\_2</span></span> | <span data-ttu-id="e1434-120">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="e1434-120">1\_3</span></span> | <span data-ttu-id="e1434-121">1\_4</span><span class="sxs-lookup"><span data-stu-id="e1434-121">1\_4</span></span> | <span data-ttu-id="e1434-122">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e1434-122">2\_0</span></span> | <span data-ttu-id="e1434-123">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="e1434-123">2\_x</span></span> | <span data-ttu-id="e1434-124">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="e1434-124">2\_sw</span></span> | <span data-ttu-id="e1434-125">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e1434-125">3\_0</span></span> | <span data-ttu-id="e1434-126">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="e1434-126">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="e1434-127">breakp</span><span class="sxs-lookup"><span data-stu-id="e1434-127">breakp</span></span>                |      |      |      |      |      | <span data-ttu-id="e1434-128">x</span><span class="sxs-lookup"><span data-stu-id="e1434-128">x</span></span>    | <span data-ttu-id="e1434-129">x</span><span class="sxs-lookup"><span data-stu-id="e1434-129">x</span></span>     | <span data-ttu-id="e1434-130">x</span><span class="sxs-lookup"><span data-stu-id="e1434-130">x</span></span>    | <span data-ttu-id="e1434-131">x</span><span class="sxs-lookup"><span data-stu-id="e1434-131">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="e1434-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e1434-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1434-133">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="e1434-133">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




