---
title: CMP-PS
description: Escolha src1 se src0 0. Caso contrário, escolha src2. A comparação é feita por canal.
ms.assetid: 8fabd548-3f5e-4b78-bf1e-16e4f1548ccd
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: da3da1062d02e995876a1f67e5c4e19518774760
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104006885"
---
# <a name="cmp---ps"></a><span data-ttu-id="78ab7-105">CMP-PS</span><span class="sxs-lookup"><span data-stu-id="78ab7-105">cmp - ps</span></span>

<span data-ttu-id="78ab7-106">Escolha src1 se src0 >= 0.</span><span class="sxs-lookup"><span data-stu-id="78ab7-106">Choose src1 if src0 >= 0.</span></span> <span data-ttu-id="78ab7-107">Caso contrário, escolha src2.</span><span class="sxs-lookup"><span data-stu-id="78ab7-107">Otherwise, choose src2.</span></span> <span data-ttu-id="78ab7-108">A comparação é feita por canal.</span><span class="sxs-lookup"><span data-stu-id="78ab7-108">The comparison is done per channel.</span></span>

## <a name="syntax"></a><span data-ttu-id="78ab7-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="78ab7-109">Syntax</span></span>



| <span data-ttu-id="78ab7-110">CMP DST, src0, src1, src2</span><span class="sxs-lookup"><span data-stu-id="78ab7-110">cmp dst, src0, src1, src2</span></span> |
|---------------------------|



 

<span data-ttu-id="78ab7-111">onde</span><span class="sxs-lookup"><span data-stu-id="78ab7-111">where</span></span>

-   <span data-ttu-id="78ab7-112">DST é o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="78ab7-112">dst is the destination register.</span></span>
-   <span data-ttu-id="78ab7-113">src0 é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="78ab7-113">src0 is a source register.</span></span>
-   <span data-ttu-id="78ab7-114">src1 é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="78ab7-114">src1 is a source register.</span></span>
-   <span data-ttu-id="78ab7-115">src2 é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="78ab7-115">src2 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="78ab7-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="78ab7-116">Remarks</span></span>



| <span data-ttu-id="78ab7-117">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="78ab7-117">Pixel shader versions</span></span> | <span data-ttu-id="78ab7-118">1\_1</span><span class="sxs-lookup"><span data-stu-id="78ab7-118">1\_1</span></span> | <span data-ttu-id="78ab7-119">1\_2</span><span class="sxs-lookup"><span data-stu-id="78ab7-119">1\_2</span></span> | <span data-ttu-id="78ab7-120">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="78ab7-120">1\_3</span></span> | <span data-ttu-id="78ab7-121">1\_4</span><span class="sxs-lookup"><span data-stu-id="78ab7-121">1\_4</span></span> | <span data-ttu-id="78ab7-122">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="78ab7-122">2\_0</span></span> | <span data-ttu-id="78ab7-123">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="78ab7-123">2\_x</span></span> | <span data-ttu-id="78ab7-124">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="78ab7-124">2\_sw</span></span> | <span data-ttu-id="78ab7-125">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="78ab7-125">3\_0</span></span> | <span data-ttu-id="78ab7-126">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="78ab7-126">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="78ab7-127">CMP</span><span class="sxs-lookup"><span data-stu-id="78ab7-127">cmp</span></span>                   |      | <span data-ttu-id="78ab7-128">x</span><span class="sxs-lookup"><span data-stu-id="78ab7-128">x</span></span>    | <span data-ttu-id="78ab7-129">x</span><span class="sxs-lookup"><span data-stu-id="78ab7-129">x</span></span>    | <span data-ttu-id="78ab7-130">x</span><span class="sxs-lookup"><span data-stu-id="78ab7-130">x</span></span>    | <span data-ttu-id="78ab7-131">x</span><span class="sxs-lookup"><span data-stu-id="78ab7-131">x</span></span>    | <span data-ttu-id="78ab7-132">x</span><span class="sxs-lookup"><span data-stu-id="78ab7-132">x</span></span>    | <span data-ttu-id="78ab7-133">x</span><span class="sxs-lookup"><span data-stu-id="78ab7-133">x</span></span>     | <span data-ttu-id="78ab7-134">x</span><span class="sxs-lookup"><span data-stu-id="78ab7-134">x</span></span>    | <span data-ttu-id="78ab7-135">x</span><span class="sxs-lookup"><span data-stu-id="78ab7-135">x</span></span>     |



 

<span data-ttu-id="78ab7-136">Há algumas limitações adicionais para as versões 1 \_ 2 e 1 \_ 3:</span><span class="sxs-lookup"><span data-stu-id="78ab7-136">There are a few additional limitations for versions 1\_2 and 1\_3:</span></span>

-   <span data-ttu-id="78ab7-137">Cada sombreador pode usar até três instruções CMP no máximo.</span><span class="sxs-lookup"><span data-stu-id="78ab7-137">Each shader can use up to a maximum of three cmp instructions.</span></span>
-   <span data-ttu-id="78ab7-138">O registro de destino não pode ser o mesmo que qualquer um dos registros de origem.</span><span class="sxs-lookup"><span data-stu-id="78ab7-138">The destination register cannot be the same as any of the source registers.</span></span>

<span data-ttu-id="78ab7-139">Este exemplo faz uma comparação de quatro canais.</span><span class="sxs-lookup"><span data-stu-id="78ab7-139">This example does a four-channel comparison.</span></span>


```
ps_1_4
def c0, -0.6, 0.6, 0, 0.6
def c1  0,0,0,0
def c2  1,1,1,1

mov r1, c1
mov r2, c2

cmp r0, c0, r1, r2   // r0 is assigned 1,0,0,0 based on the following:

// r0.x = c2.x because c0.x < 0
// r0.y = c1.y because c0.y >= 0
// r0.z = c1.z because c0.z >= 0
// r0.w = c1.w because c0.w >= 0
```



## <a name="related-topics"></a><span data-ttu-id="78ab7-140">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="78ab7-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78ab7-141">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="78ab7-141">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




