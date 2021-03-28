---
title: LogP-vs
description: Precisão parcial LogP ₂ (x).
ms.assetid: 8547ca8a-7bde-4e41-9e65-f7fcd65454c1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0a261d63ad47dcf12728b8bcd0025ec578ede0b4
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104006897"
---
# <a name="logp---vs"></a><span data-ttu-id="b6329-103">LogP-vs</span><span class="sxs-lookup"><span data-stu-id="b6329-103">logp - vs</span></span>

<span data-ttu-id="b6329-104">Precisão parcial LogP ₂ (x).</span><span class="sxs-lookup"><span data-stu-id="b6329-104">Partial precision logp₂(x).</span></span>

## <a name="syntax"></a><span data-ttu-id="b6329-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b6329-105">Syntax</span></span>



| <span data-ttu-id="b6329-106">LogP DST, src</span><span class="sxs-lookup"><span data-stu-id="b6329-106">logp dst, src</span></span> |
|---------------|



 

<span data-ttu-id="b6329-107">onde</span><span class="sxs-lookup"><span data-stu-id="b6329-107">where</span></span>

-   <span data-ttu-id="b6329-108">DST é o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="b6329-108">dst is the destination register.</span></span>
-   <span data-ttu-id="b6329-109">src é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="b6329-109">src is a source register.</span></span> <span data-ttu-id="b6329-110">O registro de origem requer uso explícito de replicate swizzle, ou seja, exatamente um dos componentes. x,. y,. z,. w swizzle (ou. r,. g,. b,. equivalentes) devem ser especificados.</span><span class="sxs-lookup"><span data-stu-id="b6329-110">Source register requires explicit use of replicate swizzle, that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6329-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="b6329-111">Remarks</span></span>



| <span data-ttu-id="b6329-112">Versões do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="b6329-112">Vertex shader versions</span></span> | <span data-ttu-id="b6329-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="b6329-113">1\_1</span></span> | <span data-ttu-id="b6329-114">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b6329-114">2\_0</span></span> | <span data-ttu-id="b6329-115">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="b6329-115">2\_x</span></span> | <span data-ttu-id="b6329-116">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="b6329-116">2\_sw</span></span> | <span data-ttu-id="b6329-117">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b6329-117">3\_0</span></span> | <span data-ttu-id="b6329-118">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="b6329-118">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="b6329-119">logp</span><span class="sxs-lookup"><span data-stu-id="b6329-119">logp</span></span>                   | <span data-ttu-id="b6329-120">x</span><span class="sxs-lookup"><span data-stu-id="b6329-120">x</span></span>    | <span data-ttu-id="b6329-121">x</span><span class="sxs-lookup"><span data-stu-id="b6329-121">x</span></span>    | <span data-ttu-id="b6329-122">x</span><span class="sxs-lookup"><span data-stu-id="b6329-122">x</span></span>    | <span data-ttu-id="b6329-123">x</span><span class="sxs-lookup"><span data-stu-id="b6329-123">x</span></span>     | <span data-ttu-id="b6329-124">x</span><span class="sxs-lookup"><span data-stu-id="b6329-124">x</span></span>    | <span data-ttu-id="b6329-125">x</span><span class="sxs-lookup"><span data-stu-id="b6329-125">x</span></span>     |



 

<span data-ttu-id="b6329-126">O fragmento de código a seguir mostra as operações executadas.</span><span class="sxs-lookup"><span data-stu-id="b6329-126">The following code fragment shows the operations performed.</span></span>


```
float f = abs(src);
if (f != 0)
    dest.x = dest.y = dest.z = dest.w = (float)(log(f)/log(2));
else
    dest.x = dest.y = dest.z = dest.w = -FLT_MAX;   
```



<span data-ttu-id="b6329-127">Essa instrução fornece a precisão parcial da base 2 do logaritmo, até 10 bits.</span><span class="sxs-lookup"><span data-stu-id="b6329-127">This instruction provides logarithm base 2 partial precision, up to 10 bits.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b6329-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b6329-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b6329-129">Instruções do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="b6329-129">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




