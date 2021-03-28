---
title: RCP-PS
description: Computa o recíproco do escalar de origem. | RCP-PS
ms.assetid: d8dfc2b3-4404-47ec-aeaf-1adb7e7a342e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2df8ad2d673d96dced84630b1a641c7e4f27ceb2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968445"
---
# <a name="rcp---ps"></a><span data-ttu-id="1b220-104">RCP-PS</span><span class="sxs-lookup"><span data-stu-id="1b220-104">rcp - ps</span></span>

<span data-ttu-id="1b220-105">Computa o recíproco do escalar de origem.</span><span class="sxs-lookup"><span data-stu-id="1b220-105">Computes the reciprocal of the source scalar.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b220-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="1b220-106">Syntax</span></span>



| <span data-ttu-id="1b220-107">RCP DST, src</span><span class="sxs-lookup"><span data-stu-id="1b220-107">rcp dst, src</span></span> |
|--------------|



 

<span data-ttu-id="1b220-108">onde</span><span class="sxs-lookup"><span data-stu-id="1b220-108">where</span></span>

-   <span data-ttu-id="1b220-109">DST é o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="1b220-109">dst is the destination register.</span></span>
-   <span data-ttu-id="1b220-110">src é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="1b220-110">src is a source register.</span></span> <span data-ttu-id="1b220-111">O registro de origem requer uso explícito de replicate swizzle, ou seja, exatamente um dos componentes. x,. y,. z,. w swizzle (ou. r,. g,. b,. equivalentes) devem ser especificados.</span><span class="sxs-lookup"><span data-stu-id="1b220-111">Source register requires explicit use of replicate swizzle, that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b220-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="1b220-112">Remarks</span></span>



| <span data-ttu-id="1b220-113">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="1b220-113">Pixel shader versions</span></span> | <span data-ttu-id="1b220-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="1b220-114">1\_1</span></span> | <span data-ttu-id="1b220-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="1b220-115">1\_2</span></span> | <span data-ttu-id="1b220-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="1b220-116">1\_3</span></span> | <span data-ttu-id="1b220-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="1b220-117">1\_4</span></span> | <span data-ttu-id="1b220-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="1b220-118">2\_0</span></span> | <span data-ttu-id="1b220-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="1b220-119">2\_x</span></span> | <span data-ttu-id="1b220-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="1b220-120">2\_sw</span></span> | <span data-ttu-id="1b220-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="1b220-121">3\_0</span></span> | <span data-ttu-id="1b220-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="1b220-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="1b220-123">rcp</span><span class="sxs-lookup"><span data-stu-id="1b220-123">rcp</span></span>                   |      |      |      |      | <span data-ttu-id="1b220-124">x</span><span class="sxs-lookup"><span data-stu-id="1b220-124">x</span></span>    | <span data-ttu-id="1b220-125">x</span><span class="sxs-lookup"><span data-stu-id="1b220-125">x</span></span>    | <span data-ttu-id="1b220-126">x</span><span class="sxs-lookup"><span data-stu-id="1b220-126">x</span></span>     | <span data-ttu-id="1b220-127">x</span><span class="sxs-lookup"><span data-stu-id="1b220-127">x</span></span>    | <span data-ttu-id="1b220-128">x</span><span class="sxs-lookup"><span data-stu-id="1b220-128">x</span></span>     |



 

<span data-ttu-id="1b220-129">A saída deve ser exatamente 1,0 se a entrada for exatamente 1,0.</span><span class="sxs-lookup"><span data-stu-id="1b220-129">The output must be exactly 1.0 if the input is exactly 1.0.</span></span> <span data-ttu-id="1b220-130">Uma fonte de 0,0 gera infinitos.</span><span class="sxs-lookup"><span data-stu-id="1b220-130">A source of 0.0 yields infinity.</span></span>

<span data-ttu-id="1b220-131">O resultado escalar é replicado para todos os canais na máscara de gravação de destino.</span><span class="sxs-lookup"><span data-stu-id="1b220-131">The scalar result is replicated to all channels in the destination write mask.</span></span>

<span data-ttu-id="1b220-132">A precisão deve ser pelo menos 1,0/(2 ²) erro absoluto durante o intervalo (1,0, 2,0) porque implementações comuns separam mantissa e expoente.</span><span class="sxs-lookup"><span data-stu-id="1b220-132">Precision should be at least 1.0/(2²²) absolute error over the range (1.0, 2.0) because common implementations will separate mantissa and exponent.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1b220-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1b220-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b220-134">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="1b220-134">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




