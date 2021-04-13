---
title: log-PS
description: ₂ de log de precisão total (x). | log-PS
ms.assetid: e540a082-5916-4111-b908-bb229c9e7dc8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a8face264d5221cf4b39f99260bec476ee5742f0
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968520"
---
# <a name="log---ps"></a><span data-ttu-id="00604-104">log-PS</span><span class="sxs-lookup"><span data-stu-id="00604-104">log - ps</span></span>

<span data-ttu-id="00604-105">₂ de log de precisão total (x).</span><span class="sxs-lookup"><span data-stu-id="00604-105">Full precision log₂(x).</span></span>

## <a name="syntax"></a><span data-ttu-id="00604-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="00604-106">Syntax</span></span>



| <span data-ttu-id="00604-107">hora de log, src</span><span class="sxs-lookup"><span data-stu-id="00604-107">log dst, src</span></span> |
|--------------|



 

<span data-ttu-id="00604-108">onde</span><span class="sxs-lookup"><span data-stu-id="00604-108">where</span></span>

-   <span data-ttu-id="00604-109">DST é o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="00604-109">dst is the destination register.</span></span>
-   <span data-ttu-id="00604-110">src é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="00604-110">src is a source register.</span></span> <span data-ttu-id="00604-111">O registro de origem requer uso explícito de replicate swizzle; ou seja, exatamente um dos componentes. x,. y,. z,. w swizzle (ou o. r,. g,. b,. equivalentes) deve ser especificado.</span><span class="sxs-lookup"><span data-stu-id="00604-111">Source register requires explicit use of replicate swizzle; that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="00604-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="00604-112">Remarks</span></span>



| <span data-ttu-id="00604-113">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="00604-113">Pixel shader versions</span></span> | <span data-ttu-id="00604-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="00604-114">1\_1</span></span> | <span data-ttu-id="00604-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="00604-115">1\_2</span></span> | <span data-ttu-id="00604-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="00604-116">1\_3</span></span> | <span data-ttu-id="00604-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="00604-117">1\_4</span></span> | <span data-ttu-id="00604-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="00604-118">2\_0</span></span> | <span data-ttu-id="00604-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="00604-119">2\_x</span></span> | <span data-ttu-id="00604-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="00604-120">2\_sw</span></span> | <span data-ttu-id="00604-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="00604-121">3\_0</span></span> | <span data-ttu-id="00604-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="00604-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="00604-123">log</span><span class="sxs-lookup"><span data-stu-id="00604-123">log</span></span>                   |      |      |      |      | <span data-ttu-id="00604-124">x</span><span class="sxs-lookup"><span data-stu-id="00604-124">x</span></span>    | <span data-ttu-id="00604-125">x</span><span class="sxs-lookup"><span data-stu-id="00604-125">x</span></span>    | <span data-ttu-id="00604-126">x</span><span class="sxs-lookup"><span data-stu-id="00604-126">x</span></span>     | <span data-ttu-id="00604-127">x</span><span class="sxs-lookup"><span data-stu-id="00604-127">x</span></span>    | <span data-ttu-id="00604-128">x</span><span class="sxs-lookup"><span data-stu-id="00604-128">x</span></span>     |



 

<span data-ttu-id="00604-129">O trecho de código a seguir mostra as operações executadas.</span><span class="sxs-lookup"><span data-stu-id="00604-129">The following code snippet shows the operations performed.</span></span>


```
float v = abs(src);
if (v != 0)
{
    dest.x = dest.y = dest.z = dest.w = 
        (float)(log(v)/log(2));  
}
else
{
    dest.x = dest.y = dest.z = dest.w = -FLT_MAX;
}
```



<span data-ttu-id="00604-130">Essa instrução aceita uma fonte escalar cujo bit de sinal é ignorado.</span><span class="sxs-lookup"><span data-stu-id="00604-130">This instruction accepts a scalar source whose sign bit is ignored.</span></span> <span data-ttu-id="00604-131">O resultado é replicado para todos os quatro canais.</span><span class="sxs-lookup"><span data-stu-id="00604-131">The result is replicated to all four channels.</span></span>

## <a name="related-topics"></a><span data-ttu-id="00604-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="00604-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00604-133">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="00604-133">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




