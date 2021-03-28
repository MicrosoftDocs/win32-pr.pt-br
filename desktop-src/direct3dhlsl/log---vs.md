---
title: log-vs
description: ₂ de log de precisão total (x). | log-vs
ms.assetid: 53c91825-ec54-4b04-bf08-52d4b1c5122d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b9e0564ab5b38943017e61bde171d0db3060ca0c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104172764"
---
# <a name="log---vs"></a><span data-ttu-id="17c30-104">log-vs</span><span class="sxs-lookup"><span data-stu-id="17c30-104">log - vs</span></span>

<span data-ttu-id="17c30-105">₂ de log de precisão total (x).</span><span class="sxs-lookup"><span data-stu-id="17c30-105">Full precision log₂(x).</span></span>

## <a name="syntax"></a><span data-ttu-id="17c30-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="17c30-106">Syntax</span></span>



| <span data-ttu-id="17c30-107">hora de log, src</span><span class="sxs-lookup"><span data-stu-id="17c30-107">log dst, src</span></span> |
|--------------|



 

<span data-ttu-id="17c30-108">onde</span><span class="sxs-lookup"><span data-stu-id="17c30-108">where</span></span>

-   <span data-ttu-id="17c30-109">DST é o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="17c30-109">dst is the destination register.</span></span>
-   <span data-ttu-id="17c30-110">src é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="17c30-110">src is a source register.</span></span> <span data-ttu-id="17c30-111">O registro de origem requer uso explícito de replicate swizzle, ou seja, exatamente um dos componentes. x,. y,. z,. w swizzle (ou. r,. g,. b,. equivalentes) devem ser especificados.</span><span class="sxs-lookup"><span data-stu-id="17c30-111">Source register requires explicit use of replicate swizzle, that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="17c30-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="17c30-112">Remarks</span></span>



| <span data-ttu-id="17c30-113">Versões do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="17c30-113">Vertex shader versions</span></span> | <span data-ttu-id="17c30-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="17c30-114">1\_1</span></span> | <span data-ttu-id="17c30-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="17c30-115">2\_0</span></span> | <span data-ttu-id="17c30-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="17c30-116">2\_x</span></span> | <span data-ttu-id="17c30-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="17c30-117">2\_sw</span></span> | <span data-ttu-id="17c30-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="17c30-118">3\_0</span></span> | <span data-ttu-id="17c30-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="17c30-119">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="17c30-120">log</span><span class="sxs-lookup"><span data-stu-id="17c30-120">log</span></span>                    | <span data-ttu-id="17c30-121">x</span><span class="sxs-lookup"><span data-stu-id="17c30-121">x</span></span>    | <span data-ttu-id="17c30-122">x</span><span class="sxs-lookup"><span data-stu-id="17c30-122">x</span></span>    | <span data-ttu-id="17c30-123">x</span><span class="sxs-lookup"><span data-stu-id="17c30-123">x</span></span>    | <span data-ttu-id="17c30-124">x</span><span class="sxs-lookup"><span data-stu-id="17c30-124">x</span></span>     | <span data-ttu-id="17c30-125">x</span><span class="sxs-lookup"><span data-stu-id="17c30-125">x</span></span>    | <span data-ttu-id="17c30-126">x</span><span class="sxs-lookup"><span data-stu-id="17c30-126">x</span></span>     |



 

<span data-ttu-id="17c30-127">O fragmento de código a seguir mostra as operações executadas.</span><span class="sxs-lookup"><span data-stu-id="17c30-127">The following code fragment shows the operations performed.</span></span>


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



<span data-ttu-id="17c30-128">Essa instrução aceita uma fonte escalar cujo bit de sinal é ignorado.</span><span class="sxs-lookup"><span data-stu-id="17c30-128">This instruction accepts a scalar source whose sign bit is ignored.</span></span> <span data-ttu-id="17c30-129">O resultado é replicado para todos os quatro canais.</span><span class="sxs-lookup"><span data-stu-id="17c30-129">The result is replicated to all four channels.</span></span>

<span data-ttu-id="17c30-130">Essa instrução fornece 21 bits de precisão.</span><span class="sxs-lookup"><span data-stu-id="17c30-130">This instruction provides 21 bits of precision.</span></span>

## <a name="related-topics"></a><span data-ttu-id="17c30-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="17c30-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="17c30-132">Instruções do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="17c30-132">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




