---
title: exp-vs
description: Fornece precisão total exponencial 2x. | exp-vs
ms.assetid: 3644046b-3257-4257-9880-146ca50f6b0b
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c5b49b69e1270075aef4368dedca5791c2784657
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104989240"
---
# <a name="exp---vs"></a><span data-ttu-id="c62ff-104">exp-vs</span><span class="sxs-lookup"><span data-stu-id="c62ff-104">exp - vs</span></span>

<span data-ttu-id="c62ff-105">Fornece a precisão total exponencial 2<sup>x</sup>.</span><span class="sxs-lookup"><span data-stu-id="c62ff-105">Provides full precision exponential 2<sup>x</sup>.</span></span>

## <a name="syntax"></a><span data-ttu-id="c62ff-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="c62ff-106">Syntax</span></span>



| <span data-ttu-id="c62ff-107">exp DST, src</span><span class="sxs-lookup"><span data-stu-id="c62ff-107">exp dst, src</span></span> |
|--------------|



 

<span data-ttu-id="c62ff-108">onde</span><span class="sxs-lookup"><span data-stu-id="c62ff-108">where</span></span>

-   <span data-ttu-id="c62ff-109">DST é o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="c62ff-109">dst is the destination register.</span></span>
-   <span data-ttu-id="c62ff-110">src é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="c62ff-110">src is a source register.</span></span> <span data-ttu-id="c62ff-111">O registro de origem requer uso explícito de replicate swizzle, ou seja, exatamente um dos componentes. x,. y,. z,. w swizzle (ou. r,. g,. b,. equivalentes) devem ser especificados.</span><span class="sxs-lookup"><span data-stu-id="c62ff-111">Source register requires explicit use of replicate swizzle, that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span> <span data-ttu-id="c62ff-112">Consulte [registro de origem Swizzling](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md).</span><span class="sxs-lookup"><span data-stu-id="c62ff-112">See [Source Register Swizzling](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c62ff-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="c62ff-113">Remarks</span></span>



| <span data-ttu-id="c62ff-114">Versões do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="c62ff-114">Vertex shader versions</span></span> | <span data-ttu-id="c62ff-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="c62ff-115">1\_1</span></span> | <span data-ttu-id="c62ff-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c62ff-116">2\_0</span></span> | <span data-ttu-id="c62ff-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="c62ff-117">2\_x</span></span> | <span data-ttu-id="c62ff-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="c62ff-118">2\_sw</span></span> | <span data-ttu-id="c62ff-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c62ff-119">3\_0</span></span> | <span data-ttu-id="c62ff-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="c62ff-120">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="c62ff-121">exp</span><span class="sxs-lookup"><span data-stu-id="c62ff-121">exp</span></span>                    | <span data-ttu-id="c62ff-122">x</span><span class="sxs-lookup"><span data-stu-id="c62ff-122">x</span></span>    | <span data-ttu-id="c62ff-123">x</span><span class="sxs-lookup"><span data-stu-id="c62ff-123">x</span></span>    | <span data-ttu-id="c62ff-124">x</span><span class="sxs-lookup"><span data-stu-id="c62ff-124">x</span></span>    | <span data-ttu-id="c62ff-125">x</span><span class="sxs-lookup"><span data-stu-id="c62ff-125">x</span></span>     | <span data-ttu-id="c62ff-126">x</span><span class="sxs-lookup"><span data-stu-id="c62ff-126">x</span></span>    | <span data-ttu-id="c62ff-127">x</span><span class="sxs-lookup"><span data-stu-id="c62ff-127">x</span></span>     |



 

<span data-ttu-id="c62ff-128">Essa instrução fornece pelo menos 21 bits de precisão.</span><span class="sxs-lookup"><span data-stu-id="c62ff-128">This instruction provides at least 21 bits of precision.</span></span>

<span data-ttu-id="c62ff-129">O fragmento de código a seguir mostra as operações executadas:</span><span class="sxs-lookup"><span data-stu-id="c62ff-129">The following code fragment shows the operations performed:</span></span>


```
dest.x = dest.y = dest.z = dest.w = (float)pow(2, src.replicateSwizzleComponent);
```



## <a name="related-topics"></a><span data-ttu-id="c62ff-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c62ff-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c62ff-131">Instruções do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="c62ff-131">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




