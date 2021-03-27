---
title: DST-vs
description: Calcula um vetor de distância. | DST-vs
ms.assetid: 4315a29f-58e7-427f-aaa0-1fe1a81eb392
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e41c1da0eae001d314e2682a3295a0b88b993ee1
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103837743"
---
# <a name="dst---vs"></a><span data-ttu-id="8a408-104">DST-vs</span><span class="sxs-lookup"><span data-stu-id="8a408-104">dst - vs</span></span>

<span data-ttu-id="8a408-105">Calcula um vetor de distância.</span><span class="sxs-lookup"><span data-stu-id="8a408-105">Calculates a distance vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a408-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="8a408-106">Syntax</span></span>



| <span data-ttu-id="8a408-107">destino do DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="8a408-107">dst dest, src0, src1</span></span> |
|----------------------|



 

<span data-ttu-id="8a408-108">onde</span><span class="sxs-lookup"><span data-stu-id="8a408-108">where</span></span>

-   <span data-ttu-id="8a408-109">dest é o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="8a408-109">dest is the destination register.</span></span>
-   <span data-ttu-id="8a408-110">src0 é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="8a408-110">src0 is a source register.</span></span>
-   <span data-ttu-id="8a408-111">src1 é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="8a408-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a408-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="8a408-112">Remarks</span></span>



| <span data-ttu-id="8a408-113">Versões do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="8a408-113">Vertex shader versions</span></span> | <span data-ttu-id="8a408-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="8a408-114">1\_1</span></span> | <span data-ttu-id="8a408-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="8a408-115">2\_0</span></span> | <span data-ttu-id="8a408-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="8a408-116">2\_x</span></span> | <span data-ttu-id="8a408-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="8a408-117">2\_sw</span></span> | <span data-ttu-id="8a408-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="8a408-118">3\_0</span></span> | <span data-ttu-id="8a408-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="8a408-119">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="8a408-120">DST</span><span class="sxs-lookup"><span data-stu-id="8a408-120">dst</span></span>                    | <span data-ttu-id="8a408-121">x</span><span class="sxs-lookup"><span data-stu-id="8a408-121">x</span></span>    | <span data-ttu-id="8a408-122">x</span><span class="sxs-lookup"><span data-stu-id="8a408-122">x</span></span>    | <span data-ttu-id="8a408-123">x</span><span class="sxs-lookup"><span data-stu-id="8a408-123">x</span></span>    | <span data-ttu-id="8a408-124">x</span><span class="sxs-lookup"><span data-stu-id="8a408-124">x</span></span>     | <span data-ttu-id="8a408-125">x</span><span class="sxs-lookup"><span data-stu-id="8a408-125">x</span></span>    | <span data-ttu-id="8a408-126">x</span><span class="sxs-lookup"><span data-stu-id="8a408-126">x</span></span>     |



 

<span data-ttu-id="8a408-127">O fragmento de código a seguir mostra as operações executadas:</span><span class="sxs-lookup"><span data-stu-id="8a408-127">The following code fragment shows the operations performed:</span></span>


```
dest.x = 1;
dest.y = src0.y * src1.y;
dest.z = src0.z;
dest.w = src1.w;
```



<span data-ttu-id="8a408-128">O primeiro operando de origem (src0) é considerado como o vetor (ignorado, d d \* , d \* d, ignorado) e o segundo operando de origem (src1) é considerado como o vetor (ignorado, 1/d, ignorado, 1/d).</span><span class="sxs-lookup"><span data-stu-id="8a408-128">The first source operand (src0) is assumed to be the vector (ignored, d\*d, d\*d, ignored) and the second source operand (src1) is assumed to be the vector (ignored, 1/d, ignored, 1/d).</span></span> <span data-ttu-id="8a408-129">O destino (dest) é o vetor de resultado (1, d, d \* d, 1/d).</span><span class="sxs-lookup"><span data-stu-id="8a408-129">The destination (dest) is the result vector (1, d, d\*d, 1/d).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8a408-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8a408-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a408-131">Instruções do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="8a408-131">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




