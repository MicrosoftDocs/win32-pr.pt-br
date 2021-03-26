---
title: RSQ-vs
description: Computa a raiz quadrada recíproca (somente positivo) do escalar de origem. | RSQ-vs
ms.assetid: 1ac37dad-0cea-41af-8dae-f299896462b1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f477d6f7d8a7ff94472c689bf5844183e2f016ee
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968462"
---
# <a name="rsq---vs"></a><span data-ttu-id="3e8b4-104">RSQ-vs</span><span class="sxs-lookup"><span data-stu-id="3e8b4-104">rsq - vs</span></span>

<span data-ttu-id="3e8b4-105">Computa a raiz quadrada recíproca (somente positivo) do escalar de origem.</span><span class="sxs-lookup"><span data-stu-id="3e8b4-105">Computes the reciprocal square root (positive only) of the source scalar.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e8b4-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="3e8b4-106">Syntax</span></span>



| <span data-ttu-id="3e8b4-107">RSQ DST, src</span><span class="sxs-lookup"><span data-stu-id="3e8b4-107">rsq dst, src</span></span> |
|--------------|



 

<span data-ttu-id="3e8b4-108">onde</span><span class="sxs-lookup"><span data-stu-id="3e8b4-108">where</span></span>

-   <span data-ttu-id="3e8b4-109">DST é o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="3e8b4-109">dst is the destination register.</span></span>
-   <span data-ttu-id="3e8b4-110">src é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="3e8b4-110">src is a source register.</span></span> <span data-ttu-id="3e8b4-111">O registro de origem requer uso explícito de replicate swizzle, ou seja, exatamente um dos componentes. x,. y,. z,. w swizzle (ou. r,. g,. b,. equivalentes) devem ser especificados.</span><span class="sxs-lookup"><span data-stu-id="3e8b4-111">Source register requires explicit use of replicate swizzle, that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e8b4-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="3e8b4-112">Remarks</span></span>



| <span data-ttu-id="3e8b4-113">Versões do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="3e8b4-113">Vertex shader versions</span></span> | <span data-ttu-id="3e8b4-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="3e8b4-114">1\_1</span></span> | <span data-ttu-id="3e8b4-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3e8b4-115">2\_0</span></span> | <span data-ttu-id="3e8b4-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="3e8b4-116">2\_x</span></span> | <span data-ttu-id="3e8b4-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="3e8b4-117">2\_sw</span></span> | <span data-ttu-id="3e8b4-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3e8b4-118">3\_0</span></span> | <span data-ttu-id="3e8b4-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="3e8b4-119">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="3e8b4-120">rsq</span><span class="sxs-lookup"><span data-stu-id="3e8b4-120">rsq</span></span>                    | <span data-ttu-id="3e8b4-121">x</span><span class="sxs-lookup"><span data-stu-id="3e8b4-121">x</span></span>    | <span data-ttu-id="3e8b4-122">x</span><span class="sxs-lookup"><span data-stu-id="3e8b4-122">x</span></span>    | <span data-ttu-id="3e8b4-123">x</span><span class="sxs-lookup"><span data-stu-id="3e8b4-123">x</span></span>    | <span data-ttu-id="3e8b4-124">x</span><span class="sxs-lookup"><span data-stu-id="3e8b4-124">x</span></span>     | <span data-ttu-id="3e8b4-125">x</span><span class="sxs-lookup"><span data-stu-id="3e8b4-125">x</span></span>    | <span data-ttu-id="3e8b4-126">x</span><span class="sxs-lookup"><span data-stu-id="3e8b4-126">x</span></span>     |



 

<span data-ttu-id="3e8b4-127">O fragmento de código a seguir mostra as operações executadas.</span><span class="sxs-lookup"><span data-stu-id="3e8b4-127">The following code fragment shows the operations performed.</span></span>


```
float f = abs(src0);
if (f == 0)
    f = FLT_MAX
else
{
    if (f != 1.0)
        f = 1.0/(float)sqrt(f);
}

dest.z = dest.y = dest.z = dest.w = f;
```



<span data-ttu-id="3e8b4-128">O valor absoluto é obtido antes do processamento.</span><span class="sxs-lookup"><span data-stu-id="3e8b4-128">The absolute value is taken before processing.</span></span>

<span data-ttu-id="3e8b4-129">A precisão deve ser pelo menos 1,0/(2 ²) erro absoluto durante o intervalo (1,0, 4,0) porque implementações comuns separam mantissa e expoente.</span><span class="sxs-lookup"><span data-stu-id="3e8b4-129">Precision should be at least 1.0/(2²²) absolute error over the range (1.0, 4.0) because common implementations will separate mantissa and exponent.</span></span>

<span data-ttu-id="3e8b4-130">Se a origem não tiver nenhum subscrito, o componente x será usado.</span><span class="sxs-lookup"><span data-stu-id="3e8b4-130">If source has no subscripts, the x-component is used.</span></span> <span data-ttu-id="3e8b4-131">A saída deve ser exatamente 1,0 se a entrada for exatamente 1,0.</span><span class="sxs-lookup"><span data-stu-id="3e8b4-131">The output must be exactly 1.0 if the input is exactly 1.0.</span></span> <span data-ttu-id="3e8b4-132">Uma fonte de 0,0 gera infinitos.</span><span class="sxs-lookup"><span data-stu-id="3e8b4-132">A source of 0.0 yields infinity.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3e8b4-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3e8b4-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e8b4-134">Instruções do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="3e8b4-134">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




