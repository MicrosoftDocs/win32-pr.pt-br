---
title: rótulo – vs
description: Marque a próxima instrução como tendo um índice de rótulo. | rótulo – vs
ms.assetid: e1aee8bc-4655-4bd5-8012-bd7a2d46e712
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6e2b72fe21301aa66d8428dc3696ceb3f12e6214
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104989245"
---
# <a name="label---vs"></a><span data-ttu-id="a361c-104">rótulo – vs</span><span class="sxs-lookup"><span data-stu-id="a361c-104">label - vs</span></span>

<span data-ttu-id="a361c-105">Marque a próxima instrução como tendo um índice de rótulo.</span><span class="sxs-lookup"><span data-stu-id="a361c-105">Mark the next instruction as having a label index.</span></span>

## <a name="syntax"></a><span data-ttu-id="a361c-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="a361c-106">Syntax</span></span>



| <span data-ttu-id="a361c-107">rótulo l\#</span><span class="sxs-lookup"><span data-stu-id="a361c-107">label l\#</span></span> |
|-----------|



 

<span data-ttu-id="a361c-108">onde \# o identifica o número do rótulo.</span><span class="sxs-lookup"><span data-stu-id="a361c-108">where \# identifies the label number.</span></span>

<span data-ttu-id="a361c-109">Para vs \_ 2 \_ 0 e vs \_ 2 \_ x, o número do rótulo deve estar entre 0 e 15.</span><span class="sxs-lookup"><span data-stu-id="a361c-109">For vs\_2\_0, and vs\_2\_x, the label number must be between between 0 and 15.</span></span>

<span data-ttu-id="a361c-110">Para \_ o vs 2 \_ SW, vs \_ 3 \_ 0 e vs \_ 3 \_ SW, o número do rótulo deve estar entre 0 e 2047.</span><span class="sxs-lookup"><span data-stu-id="a361c-110">For vs\_2\_sw, vs\_3\_0 and vs\_3\_sw, the label number must be between between 0 and 2047.</span></span>

## <a name="remarks"></a><span data-ttu-id="a361c-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="a361c-111">Remarks</span></span>



| <span data-ttu-id="a361c-112">Versões do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="a361c-112">Vertex shader versions</span></span> | <span data-ttu-id="a361c-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="a361c-113">1\_1</span></span> | <span data-ttu-id="a361c-114">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a361c-114">2\_0</span></span> | <span data-ttu-id="a361c-115">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="a361c-115">2\_x</span></span> | <span data-ttu-id="a361c-116">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="a361c-116">2\_sw</span></span> | <span data-ttu-id="a361c-117">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a361c-117">3\_0</span></span> | <span data-ttu-id="a361c-118">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="a361c-118">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="a361c-119">label</span><span class="sxs-lookup"><span data-stu-id="a361c-119">label</span></span>                  |      | <span data-ttu-id="a361c-120">x</span><span class="sxs-lookup"><span data-stu-id="a361c-120">x</span></span>    | <span data-ttu-id="a361c-121">x</span><span class="sxs-lookup"><span data-stu-id="a361c-121">x</span></span>    | <span data-ttu-id="a361c-122">x</span><span class="sxs-lookup"><span data-stu-id="a361c-122">x</span></span>     | <span data-ttu-id="a361c-123">x</span><span class="sxs-lookup"><span data-stu-id="a361c-123">x</span></span>    | <span data-ttu-id="a361c-124">x</span><span class="sxs-lookup"><span data-stu-id="a361c-124">x</span></span>     |



 

<span data-ttu-id="a361c-125">Esta instrução define um rótulo localizado na próxima instrução do sombreador.</span><span class="sxs-lookup"><span data-stu-id="a361c-125">This instruction defines a label located at the next shader instruction.</span></span> <span data-ttu-id="a361c-126">A instrução Label só pode ser apresentada diretamente após uma instrução [RET](ret---vs.md) (que define o fim da sub-rotina ou do programa principal anterior).</span><span class="sxs-lookup"><span data-stu-id="a361c-126">The label instruction can only be present directly after a [ret](ret---vs.md) instruction (which defines the end of the previous subroutine or main program).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a361c-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a361c-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a361c-128">Instruções do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="a361c-128">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




