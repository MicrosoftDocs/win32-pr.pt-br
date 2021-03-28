---
title: rótulo-PS
description: Marque a próxima instrução como tendo um índice de rótulo. | rótulo-PS
ms.assetid: 21afa062-c536-4891-ba69-ca5284b0539c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f3fb266b649642c82293e8310b6302c6763ddc27
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104989207"
---
# <a name="label---ps"></a><span data-ttu-id="7755b-104">rótulo-PS</span><span class="sxs-lookup"><span data-stu-id="7755b-104">label - ps</span></span>

<span data-ttu-id="7755b-105">Marque a próxima instrução como tendo um índice de rótulo.</span><span class="sxs-lookup"><span data-stu-id="7755b-105">Mark the next instruction as having a label index.</span></span>

## <a name="syntax"></a><span data-ttu-id="7755b-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="7755b-106">Syntax</span></span>



| <span data-ttu-id="7755b-107">rótulo l\#</span><span class="sxs-lookup"><span data-stu-id="7755b-107">label l\#</span></span> |
|-----------|



 

<span data-ttu-id="7755b-108">onde \# o identifica o número do rótulo.</span><span class="sxs-lookup"><span data-stu-id="7755b-108">where \# identifies the label number.</span></span>

<span data-ttu-id="7755b-109">Para \_ o PS 2 \_ x, o número do rótulo deve estar entre 0 e 15.</span><span class="sxs-lookup"><span data-stu-id="7755b-109">For ps\_2\_x, the label number must be between between 0 and 15.</span></span>

<span data-ttu-id="7755b-110">Para \_ \_ o software PS 2 SW, PS \_ 3 \_ 0 e PS \_ 3 \_ SW, o número do rótulo deve estar entre 0 e 2047.</span><span class="sxs-lookup"><span data-stu-id="7755b-110">For ps\_2\_sw, ps\_3\_0, and ps\_3\_sw, the label number must be between between 0 and 2047.</span></span>

## <a name="remarks"></a><span data-ttu-id="7755b-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="7755b-111">Remarks</span></span>



| <span data-ttu-id="7755b-112">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="7755b-112">Pixel shader versions</span></span> | <span data-ttu-id="7755b-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="7755b-113">1\_1</span></span> | <span data-ttu-id="7755b-114">1\_2</span><span class="sxs-lookup"><span data-stu-id="7755b-114">1\_2</span></span> | <span data-ttu-id="7755b-115">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="7755b-115">1\_3</span></span> | <span data-ttu-id="7755b-116">1\_4</span><span class="sxs-lookup"><span data-stu-id="7755b-116">1\_4</span></span> | <span data-ttu-id="7755b-117">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7755b-117">2\_0</span></span> | <span data-ttu-id="7755b-118">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="7755b-118">2\_x</span></span> | <span data-ttu-id="7755b-119">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="7755b-119">2\_sw</span></span> | <span data-ttu-id="7755b-120">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7755b-120">3\_0</span></span> | <span data-ttu-id="7755b-121">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="7755b-121">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="7755b-122">label</span><span class="sxs-lookup"><span data-stu-id="7755b-122">label</span></span>                 |      |      |      |      |      | <span data-ttu-id="7755b-123">x</span><span class="sxs-lookup"><span data-stu-id="7755b-123">x</span></span>    | <span data-ttu-id="7755b-124">x</span><span class="sxs-lookup"><span data-stu-id="7755b-124">x</span></span>     | <span data-ttu-id="7755b-125">x</span><span class="sxs-lookup"><span data-stu-id="7755b-125">x</span></span>    | <span data-ttu-id="7755b-126">x</span><span class="sxs-lookup"><span data-stu-id="7755b-126">x</span></span>     |



 

<span data-ttu-id="7755b-127">Esta instrução define um rótulo localizado na próxima instrução do sombreador.</span><span class="sxs-lookup"><span data-stu-id="7755b-127">This instruction defines a label located at the next shader instruction.</span></span> <span data-ttu-id="7755b-128">A instrução Label só pode ser apresentada diretamente após uma instrução [RET](ret---ps.md) (que define o fim da sub-rotina ou do programa principal anterior).</span><span class="sxs-lookup"><span data-stu-id="7755b-128">The label instruction can only be present directly after a [ret](ret---ps.md) instruction (which defines the end of the previous subroutine or main program).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7755b-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7755b-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7755b-130">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="7755b-130">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




