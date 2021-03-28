---
title: breakp-vs
description: Interromper condicionalmente o loop atual no ENDLOOP-vs ou endrep-vs mais próximo. Use um dos componentes do registro de predicado como uma condição para determinar se deseja ou não realizar a instrução.
ms.assetid: 940252a0-6f6a-45d8-9d2f-315cc97686ca
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dbd0d5e20040bc2d353287eb4243c9e9d6d21dc8
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104006890"
---
# <a name="breakp---vs"></a><span data-ttu-id="117c3-103">breakp-vs</span><span class="sxs-lookup"><span data-stu-id="117c3-103">breakp - vs</span></span>

<span data-ttu-id="117c3-104">Interromper condicionalmente o loop atual no [ENDLOOP-vs](endloop---vs.md) ou [endrep-vs](endrep---vs.md)mais próximo. Use um dos componentes de registro de predicado como uma condição para determinar se deseja ou não realizar a instrução.</span><span class="sxs-lookup"><span data-stu-id="117c3-104">Conditionally break out of the current loop at the nearest [endloop - vs](endloop---vs.md) or [endrep - vs](endrep---vs.md). Use one of the components of the predicate register as a condition to determine whether or not to perform the instruction.</span></span>

## <a name="syntax"></a><span data-ttu-id="117c3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="117c3-105">Syntax</span></span>



| <span data-ttu-id="117c3-106">breakp \[ ! \] P0. w.x.y.</span><span class="sxs-lookup"><span data-stu-id="117c3-106">breakp \[!\]p0.{x\</span></span>|<span data-ttu-id="117c3-107">Iar</span><span class="sxs-lookup"><span data-stu-id="117c3-107">y\</span></span>|<span data-ttu-id="117c3-108">z</span><span class="sxs-lookup"><span data-stu-id="117c3-108">z\</span></span>|<span data-ttu-id="117c3-109">Mostrar</span><span class="sxs-lookup"><span data-stu-id="117c3-109">w}</span></span> |
|-----------------------------|



 

<span data-ttu-id="117c3-110">Em que:</span><span class="sxs-lookup"><span data-stu-id="117c3-110">Where:</span></span>

-   <span data-ttu-id="117c3-111">\[!\] booliano opcional não.</span><span class="sxs-lookup"><span data-stu-id="117c3-111">\[!\] optional boolean NOT.</span></span>
-   <span data-ttu-id="117c3-112">P0 é o registro de predicado.</span><span class="sxs-lookup"><span data-stu-id="117c3-112">p0 is the predicate register.</span></span> <span data-ttu-id="117c3-113">Consulte [registro de predicado](dx9-graphics-reference-asm-vs-registers-predicate.md).</span><span class="sxs-lookup"><span data-stu-id="117c3-113">See [Predicate Register](dx9-graphics-reference-asm-vs-registers-predicate.md).</span></span>
-   <span data-ttu-id="117c3-114">{x \| y \| z \| w} é o swizzle de replicação necessário em P0.</span><span class="sxs-lookup"><span data-stu-id="117c3-114">{x\|y\|z\|w} is the required replicate swizzle on p0.</span></span>

## <a name="remarks"></a><span data-ttu-id="117c3-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="117c3-115">Remarks</span></span>



| <span data-ttu-id="117c3-116">Versões do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="117c3-116">Vertex shader versions</span></span> | <span data-ttu-id="117c3-117">1\_1</span><span class="sxs-lookup"><span data-stu-id="117c3-117">1\_1</span></span> | <span data-ttu-id="117c3-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="117c3-118">2\_0</span></span> | <span data-ttu-id="117c3-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="117c3-119">2\_x</span></span> | <span data-ttu-id="117c3-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="117c3-120">2\_sw</span></span> | <span data-ttu-id="117c3-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="117c3-121">3\_0</span></span> | <span data-ttu-id="117c3-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="117c3-122">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="117c3-123">breakp</span><span class="sxs-lookup"><span data-stu-id="117c3-123">breakp</span></span>                 |      |      | <span data-ttu-id="117c3-124">x</span><span class="sxs-lookup"><span data-stu-id="117c3-124">x</span></span>    | <span data-ttu-id="117c3-125">x</span><span class="sxs-lookup"><span data-stu-id="117c3-125">x</span></span>     | <span data-ttu-id="117c3-126">x</span><span class="sxs-lookup"><span data-stu-id="117c3-126">x</span></span>    | <span data-ttu-id="117c3-127">x</span><span class="sxs-lookup"><span data-stu-id="117c3-127">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="117c3-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="117c3-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="117c3-129">Instruções do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="117c3-129">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




