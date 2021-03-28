---
title: RCP-vs
description: Computa o recíproco do escalar de origem. | RCP-vs
ms.assetid: be638a42-b693-461d-ab0a-3a6c0fa1acfc
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 145a998cbca9dc3721d9c7d6ba251d539286a3f1
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968518"
---
# <a name="rcp---vs"></a><span data-ttu-id="16020-104">RCP-vs</span><span class="sxs-lookup"><span data-stu-id="16020-104">rcp - vs</span></span>

<span data-ttu-id="16020-105">Computa o recíproco do escalar de origem.</span><span class="sxs-lookup"><span data-stu-id="16020-105">Computes the reciprocal of the source scalar.</span></span>

## <a name="syntax"></a><span data-ttu-id="16020-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="16020-106">Syntax</span></span>



| <span data-ttu-id="16020-107">RCP DST, src</span><span class="sxs-lookup"><span data-stu-id="16020-107">rcp dst, src</span></span> |
|--------------|



 

<span data-ttu-id="16020-108">onde</span><span class="sxs-lookup"><span data-stu-id="16020-108">where</span></span>

-   <span data-ttu-id="16020-109">DST é o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="16020-109">dst is the destination register.</span></span>
-   <span data-ttu-id="16020-110">src é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="16020-110">src is a source register.</span></span> <span data-ttu-id="16020-111">O registro de origem requer uso explícito de replicate swizzle, ou seja, exatamente um dos componentes. x,. y,. z,. w swizzle (ou. r,. g,. b,. equivalentes) devem ser especificados.</span><span class="sxs-lookup"><span data-stu-id="16020-111">Source register requires explicit use of replicate swizzle, that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="16020-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="16020-112">Remarks</span></span>



| <span data-ttu-id="16020-113">Versões do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="16020-113">Vertex shader versions</span></span> | <span data-ttu-id="16020-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="16020-114">1\_1</span></span> | <span data-ttu-id="16020-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="16020-115">2\_0</span></span> | <span data-ttu-id="16020-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="16020-116">2\_x</span></span> | <span data-ttu-id="16020-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="16020-117">2\_sw</span></span> | <span data-ttu-id="16020-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="16020-118">3\_0</span></span> | <span data-ttu-id="16020-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="16020-119">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="16020-120">rcp</span><span class="sxs-lookup"><span data-stu-id="16020-120">rcp</span></span>                    | <span data-ttu-id="16020-121">x</span><span class="sxs-lookup"><span data-stu-id="16020-121">x</span></span>    | <span data-ttu-id="16020-122">x</span><span class="sxs-lookup"><span data-stu-id="16020-122">x</span></span>    | <span data-ttu-id="16020-123">x</span><span class="sxs-lookup"><span data-stu-id="16020-123">x</span></span>    | <span data-ttu-id="16020-124">x</span><span class="sxs-lookup"><span data-stu-id="16020-124">x</span></span>     | <span data-ttu-id="16020-125">x</span><span class="sxs-lookup"><span data-stu-id="16020-125">x</span></span>    | <span data-ttu-id="16020-126">x</span><span class="sxs-lookup"><span data-stu-id="16020-126">x</span></span>     |



 

<span data-ttu-id="16020-127">O fragmento de código a seguir mostra as operações executadas.</span><span class="sxs-lookup"><span data-stu-id="16020-127">The following code fragment shows the operations performed.</span></span>


```
float f = src0;
if(f == 0.0f)
{
    f = FLT_MAX;
}
else 
{
    if(f != 1.0)
    {
        f = 1/f;
    }
}

dest = f;
```



<span data-ttu-id="16020-128">A saída deve ser exatamente 1,0 se a entrada for exatamente 1,0.</span><span class="sxs-lookup"><span data-stu-id="16020-128">The output must be exactly 1.0 if the input is exactly 1.0.</span></span> <span data-ttu-id="16020-129">Uma fonte de 0,0 gera infinitos.</span><span class="sxs-lookup"><span data-stu-id="16020-129">A source of 0.0 yields infinity.</span></span>

<span data-ttu-id="16020-130">A precisão deve ser pelo menos 1,0/(2 ²) erro absoluto durante o intervalo (1,0, 2,0) porque implementações comuns separam mantissa e expoente.</span><span class="sxs-lookup"><span data-stu-id="16020-130">Precision should be at least 1.0/(2²²) absolute error over the range (1.0, 2.0) because common implementations will separate mantissa and exponent.</span></span>

<span data-ttu-id="16020-131">Se a origem não tiver nenhum subscrito, o componente x será usado.</span><span class="sxs-lookup"><span data-stu-id="16020-131">If the source has no subscripts, the x-component is used.</span></span>

## <a name="related-topics"></a><span data-ttu-id="16020-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="16020-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16020-133">Instruções do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="16020-133">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




