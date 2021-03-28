---
title: exp-PS
description: Fornece precisão total exponencial 2x. | exp-PS
ms.assetid: 09e4446f-4149-4ec8-b3e3-2045b55bd591
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: acd7c50c1f0d6ff08ee5d66e50fdd3e56939f0d9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104011996"
---
# <a name="exp---ps"></a><span data-ttu-id="9ca0b-104">exp-PS</span><span class="sxs-lookup"><span data-stu-id="9ca0b-104">exp - ps</span></span>

<span data-ttu-id="9ca0b-105">Fornece a precisão total exponencial 2<sup>x</sup>.</span><span class="sxs-lookup"><span data-stu-id="9ca0b-105">Provides full precision exponential 2<sup>x</sup>.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ca0b-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="9ca0b-106">Syntax</span></span>



| <span data-ttu-id="9ca0b-107">exp DST, src</span><span class="sxs-lookup"><span data-stu-id="9ca0b-107">exp dst, src</span></span> |
|--------------|



 

<span data-ttu-id="9ca0b-108">onde</span><span class="sxs-lookup"><span data-stu-id="9ca0b-108">where</span></span>

-   <span data-ttu-id="9ca0b-109">DST é o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="9ca0b-109">dst is the destination register.</span></span>
-   <span data-ttu-id="9ca0b-110">src é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="9ca0b-110">src is a source register.</span></span> <span data-ttu-id="9ca0b-111">O registro de origem requer uso explícito de replicate swizzle; ou seja, exatamente um dos componentes. x,. y,. z,. w swizzle (ou o. r,. g,. b,. equivalentes) deve ser especificado.</span><span class="sxs-lookup"><span data-stu-id="9ca0b-111">Source register requires explicit use of replicate swizzle; that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span> <span data-ttu-id="9ca0b-112">Consulte [registro de origem Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md).</span><span class="sxs-lookup"><span data-stu-id="9ca0b-112">See [Source Register Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9ca0b-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="9ca0b-113">Remarks</span></span>



| <span data-ttu-id="9ca0b-114">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="9ca0b-114">Pixel shader versions</span></span> | <span data-ttu-id="9ca0b-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="9ca0b-115">1\_1</span></span> | <span data-ttu-id="9ca0b-116">1\_2</span><span class="sxs-lookup"><span data-stu-id="9ca0b-116">1\_2</span></span> | <span data-ttu-id="9ca0b-117">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="9ca0b-117">1\_3</span></span> | <span data-ttu-id="9ca0b-118">1\_4</span><span class="sxs-lookup"><span data-stu-id="9ca0b-118">1\_4</span></span> | <span data-ttu-id="9ca0b-119">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9ca0b-119">2\_0</span></span> | <span data-ttu-id="9ca0b-120">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="9ca0b-120">2\_x</span></span> | <span data-ttu-id="9ca0b-121">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="9ca0b-121">2\_sw</span></span> | <span data-ttu-id="9ca0b-122">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9ca0b-122">3\_0</span></span> | <span data-ttu-id="9ca0b-123">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="9ca0b-123">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="9ca0b-124">exp</span><span class="sxs-lookup"><span data-stu-id="9ca0b-124">exp</span></span>                   |      |      |      |      | <span data-ttu-id="9ca0b-125">x</span><span class="sxs-lookup"><span data-stu-id="9ca0b-125">x</span></span>    | <span data-ttu-id="9ca0b-126">x</span><span class="sxs-lookup"><span data-stu-id="9ca0b-126">x</span></span>    | <span data-ttu-id="9ca0b-127">x</span><span class="sxs-lookup"><span data-stu-id="9ca0b-127">x</span></span>     | <span data-ttu-id="9ca0b-128">x</span><span class="sxs-lookup"><span data-stu-id="9ca0b-128">x</span></span>    | <span data-ttu-id="9ca0b-129">x</span><span class="sxs-lookup"><span data-stu-id="9ca0b-129">x</span></span>     |



 

<span data-ttu-id="9ca0b-130">O trecho de código a seguir mostra as operações executadas:</span><span class="sxs-lookup"><span data-stu-id="9ca0b-130">The following code snippet shows the operations performed:</span></span>


```
dest.x = dest.y = dest.z = dest.w = (float)pow(2, src.replicateSwizzleComponent);
```



## <a name="related-topics"></a><span data-ttu-id="9ca0b-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9ca0b-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ca0b-132">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="9ca0b-132">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




