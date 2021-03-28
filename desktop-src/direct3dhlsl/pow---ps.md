---
title: pow-PS
description: Src0 (ABS de precisão completa) src1. | pow-PS
ms.assetid: 39037c51-a524-459c-8422-bd7831e2aa3d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 84be39ca8f2633482165d76eabfe0f5d0bb22161
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968330"
---
# <a name="pow---ps"></a><span data-ttu-id="26f37-104">pow-PS</span><span class="sxs-lookup"><span data-stu-id="26f37-104">pow - ps</span></span>

<span data-ttu-id="26f37-105">Src0 (ABS de precisão completa)<sup>src1</sup>.</span><span class="sxs-lookup"><span data-stu-id="26f37-105">Full precision abs(src0)<sup>src1</sup>.</span></span>

## <a name="syntax"></a><span data-ttu-id="26f37-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="26f37-106">Syntax</span></span>



| <span data-ttu-id="26f37-107">pow DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="26f37-107">pow dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="26f37-108">onde</span><span class="sxs-lookup"><span data-stu-id="26f37-108">where</span></span>

-   <span data-ttu-id="26f37-109">DST é o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="26f37-109">dst is the destination register.</span></span>
-   <span data-ttu-id="26f37-110">src0 é um registro de fonte de entrada.</span><span class="sxs-lookup"><span data-stu-id="26f37-110">src0 is an input source register.</span></span> <span data-ttu-id="26f37-111">O registro de origem requer uso explícito de replicate swizzle, ou seja, exatamente um dos componentes. x,. y,. z,. w swizzle (ou. r,. g,. b,. equivalentes) devem ser especificados.</span><span class="sxs-lookup"><span data-stu-id="26f37-111">Source register requires explicit use of replicate swizzle, that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>
-   <span data-ttu-id="26f37-112">src1 é um registro de fonte de entrada.</span><span class="sxs-lookup"><span data-stu-id="26f37-112">src1 is an input source register.</span></span> <span data-ttu-id="26f37-113">O registro de origem requer uso explícito de replicate swizzle, ou seja, exatamente um dos componentes. x,. y,. z,. w swizzle (ou. r,. g,. b,. equivalentes) devem ser especificados.</span><span class="sxs-lookup"><span data-stu-id="26f37-113">Source register requires explicit use of replicate swizzle, that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="26f37-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="26f37-114">Remarks</span></span>



| <span data-ttu-id="26f37-115">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="26f37-115">Pixel shader versions</span></span> | <span data-ttu-id="26f37-116">1\_1</span><span class="sxs-lookup"><span data-stu-id="26f37-116">1\_1</span></span> | <span data-ttu-id="26f37-117">1\_2</span><span class="sxs-lookup"><span data-stu-id="26f37-117">1\_2</span></span> | <span data-ttu-id="26f37-118">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="26f37-118">1\_3</span></span> | <span data-ttu-id="26f37-119">1\_4</span><span class="sxs-lookup"><span data-stu-id="26f37-119">1\_4</span></span> | <span data-ttu-id="26f37-120">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="26f37-120">2\_0</span></span> | <span data-ttu-id="26f37-121">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="26f37-121">2\_x</span></span> | <span data-ttu-id="26f37-122">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="26f37-122">2\_sw</span></span> | <span data-ttu-id="26f37-123">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="26f37-123">3\_0</span></span> | <span data-ttu-id="26f37-124">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="26f37-124">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="26f37-125">pow</span><span class="sxs-lookup"><span data-stu-id="26f37-125">pow</span></span>                   |      |      |      |      | <span data-ttu-id="26f37-126">x</span><span class="sxs-lookup"><span data-stu-id="26f37-126">x</span></span>    | <span data-ttu-id="26f37-127">x</span><span class="sxs-lookup"><span data-stu-id="26f37-127">x</span></span>    | <span data-ttu-id="26f37-128">x</span><span class="sxs-lookup"><span data-stu-id="26f37-128">x</span></span>     | <span data-ttu-id="26f37-129">x</span><span class="sxs-lookup"><span data-stu-id="26f37-129">x</span></span>    | <span data-ttu-id="26f37-130">x</span><span class="sxs-lookup"><span data-stu-id="26f37-130">x</span></span>     |



 

<span data-ttu-id="26f37-131">Essa instrução funciona da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="26f37-131">This instruction works as follows:</span></span>

<span data-ttu-id="26f37-132">dest. x = dest. y = dest. z = dest. w = \[ ABS (src0) \] <sup>src1</sup>;</span><span class="sxs-lookup"><span data-stu-id="26f37-132">dest.x = dest.y = dest.z = dest.w = \[abs(src0)\]<sup>src1</sup>;</span></span>

<span data-ttu-id="26f37-133">Essa é uma instrução escalar, portanto, os registros de origem devem ter replicar swizzles para indicar quais canais são usados.</span><span class="sxs-lookup"><span data-stu-id="26f37-133">This is a scalar instruction, therefore the source registers should have replicate swizzles to indicate which channels are used.</span></span>

<span data-ttu-id="26f37-134">A potência de entrada (src1) deve ser um escalar.</span><span class="sxs-lookup"><span data-stu-id="26f37-134">The input power (src1) must be a scalar.</span></span>

<span data-ttu-id="26f37-135">O resultado escalar é replicado para todos os quatro canais de saída.</span><span class="sxs-lookup"><span data-stu-id="26f37-135">The scalar result is replicated to all four output channels.</span></span>

<span data-ttu-id="26f37-136">Essa instrução pode ser expandida como exp ( \* log src1 (src0)).</span><span class="sxs-lookup"><span data-stu-id="26f37-136">This instruction could be expanded as exp(src1 \* log(src0)).</span></span>

<span data-ttu-id="26f37-137">O registro de hora de verão deve ser um registro temporário e não deve ser o mesmo registrado como src1.</span><span class="sxs-lookup"><span data-stu-id="26f37-137">The dst register should be a temporary register, and should not be the same register as src1.</span></span>

## <a name="related-topics"></a><span data-ttu-id="26f37-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="26f37-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26f37-139">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="26f37-139">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




