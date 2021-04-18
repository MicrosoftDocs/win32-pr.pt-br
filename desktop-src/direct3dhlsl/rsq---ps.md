---
title: RSQ-PS
description: Computa a raiz quadrada recíproca (somente positivo) do escalar de origem. | RSQ-PS
ms.assetid: deb1bd12-6347-4b1e-b21b-f3ef48da4c13
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 13777810c67ba38b2c8f47f0c0db0cf9b70771ad
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968400"
---
# <a name="rsq---ps"></a><span data-ttu-id="5b55d-104">RSQ-PS</span><span class="sxs-lookup"><span data-stu-id="5b55d-104">rsq - ps</span></span>

<span data-ttu-id="5b55d-105">Computa a raiz quadrada recíproca (somente positivo) do escalar de origem.</span><span class="sxs-lookup"><span data-stu-id="5b55d-105">Computes the reciprocal square root (positive only) of the source scalar.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b55d-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="5b55d-106">Syntax</span></span>



| <span data-ttu-id="5b55d-107">RSQ DST, src</span><span class="sxs-lookup"><span data-stu-id="5b55d-107">rsq dst, src</span></span> |
|--------------|



 

<span data-ttu-id="5b55d-108">onde</span><span class="sxs-lookup"><span data-stu-id="5b55d-108">where</span></span>

-   <span data-ttu-id="5b55d-109">DST é o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="5b55d-109">dst is the destination register.</span></span>
-   <span data-ttu-id="5b55d-110">src é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="5b55d-110">src is a source register.</span></span> <span data-ttu-id="5b55d-111">O registro de origem requer uso explícito de replicate swizzle, ou seja, exatamente um dos componentes. x,. y,. z,. w swizzle (ou. r,. g,. b,. equivalentes) devem ser especificados.</span><span class="sxs-lookup"><span data-stu-id="5b55d-111">Source register requires explicit use of replicate swizzle, that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b55d-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="5b55d-112">Remarks</span></span>



| <span data-ttu-id="5b55d-113">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="5b55d-113">Pixel shader versions</span></span> | <span data-ttu-id="5b55d-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="5b55d-114">1\_1</span></span> | <span data-ttu-id="5b55d-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="5b55d-115">1\_2</span></span> | <span data-ttu-id="5b55d-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="5b55d-116">1\_3</span></span> | <span data-ttu-id="5b55d-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="5b55d-117">1\_4</span></span> | <span data-ttu-id="5b55d-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5b55d-118">2\_0</span></span> | <span data-ttu-id="5b55d-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="5b55d-119">2\_x</span></span> | <span data-ttu-id="5b55d-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="5b55d-120">2\_sw</span></span> | <span data-ttu-id="5b55d-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5b55d-121">3\_0</span></span> | <span data-ttu-id="5b55d-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="5b55d-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="5b55d-123">rsq</span><span class="sxs-lookup"><span data-stu-id="5b55d-123">rsq</span></span>                   |      |      |      |      | <span data-ttu-id="5b55d-124">x</span><span class="sxs-lookup"><span data-stu-id="5b55d-124">x</span></span>    | <span data-ttu-id="5b55d-125">x</span><span class="sxs-lookup"><span data-stu-id="5b55d-125">x</span></span>    | <span data-ttu-id="5b55d-126">x</span><span class="sxs-lookup"><span data-stu-id="5b55d-126">x</span></span>     | <span data-ttu-id="5b55d-127">x</span><span class="sxs-lookup"><span data-stu-id="5b55d-127">x</span></span>    | <span data-ttu-id="5b55d-128">x</span><span class="sxs-lookup"><span data-stu-id="5b55d-128">x</span></span>     |



 

<span data-ttu-id="5b55d-129">O valor absoluto é obtido antes do processamento.</span><span class="sxs-lookup"><span data-stu-id="5b55d-129">The absolute value is taken before processing.</span></span>

<span data-ttu-id="5b55d-130">A precisão deve ser pelo menos 1,0/(2 ²) erro absoluto durante o intervalo (1,0, 4,0) porque implementações comuns separam mantissa e expoente.</span><span class="sxs-lookup"><span data-stu-id="5b55d-130">Precision should be at least 1.0/(2²²) absolute error over the range (1.0, 4.0) because common implementations will separate mantissa and exponent.</span></span>

<span data-ttu-id="5b55d-131">A saída deve ser exatamente 1,0 se a entrada for exatamente 1,0.</span><span class="sxs-lookup"><span data-stu-id="5b55d-131">The output must be exactly 1.0 if the input is exactly 1.0.</span></span> <span data-ttu-id="5b55d-132">Uma fonte de 0,0 gera infinitos.</span><span class="sxs-lookup"><span data-stu-id="5b55d-132">A source of 0.0 yields infinity.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5b55d-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5b55d-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5b55d-134">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="5b55d-134">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




