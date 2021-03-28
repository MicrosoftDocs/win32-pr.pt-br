---
title: DP4-PS
description: Computa o produto de quatro componentes do ponto dos registros de origem. | DP4-PS
ms.assetid: 83ef6097-cacf-4498-842b-3eb03e57bd6f
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2562259af164b8680d54e9a120abaa405fd781c5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104012012"
---
# <a name="dp4---ps"></a><span data-ttu-id="db5e8-104">DP4-PS</span><span class="sxs-lookup"><span data-stu-id="db5e8-104">dp4 - ps</span></span>

<span data-ttu-id="db5e8-105">Computa o produto de quatro componentes do ponto dos registros de origem.</span><span class="sxs-lookup"><span data-stu-id="db5e8-105">Computes the four-component dot product of the source registers.</span></span>

## <a name="syntax"></a><span data-ttu-id="db5e8-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="db5e8-106">Syntax</span></span>



| <span data-ttu-id="db5e8-107">DP4 DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="db5e8-107">dp4 dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="db5e8-108">onde</span><span class="sxs-lookup"><span data-stu-id="db5e8-108">where</span></span>

-   <span data-ttu-id="db5e8-109">DST é o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="db5e8-109">dst is the destination register.</span></span>
-   <span data-ttu-id="db5e8-110">src0 é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="db5e8-110">src0 is a source register.</span></span>
-   <span data-ttu-id="db5e8-111">src1 é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="db5e8-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="db5e8-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="db5e8-112">Remarks</span></span>



| <span data-ttu-id="db5e8-113">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="db5e8-113">Pixel shader versions</span></span> | <span data-ttu-id="db5e8-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="db5e8-114">1\_1</span></span> | <span data-ttu-id="db5e8-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="db5e8-115">1\_2</span></span> | <span data-ttu-id="db5e8-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="db5e8-116">1\_3</span></span> | <span data-ttu-id="db5e8-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="db5e8-117">1\_4</span></span> | <span data-ttu-id="db5e8-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="db5e8-118">2\_0</span></span> | <span data-ttu-id="db5e8-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="db5e8-119">2\_x</span></span> | <span data-ttu-id="db5e8-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="db5e8-120">2\_sw</span></span> | <span data-ttu-id="db5e8-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="db5e8-121">3\_0</span></span> | <span data-ttu-id="db5e8-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="db5e8-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="db5e8-123">dp4</span><span class="sxs-lookup"><span data-stu-id="db5e8-123">dp4</span></span>                   |      | <span data-ttu-id="db5e8-124">x</span><span class="sxs-lookup"><span data-stu-id="db5e8-124">x</span></span>    | <span data-ttu-id="db5e8-125">x</span><span class="sxs-lookup"><span data-stu-id="db5e8-125">x</span></span>    | <span data-ttu-id="db5e8-126">x</span><span class="sxs-lookup"><span data-stu-id="db5e8-126">x</span></span>    | <span data-ttu-id="db5e8-127">x</span><span class="sxs-lookup"><span data-stu-id="db5e8-127">x</span></span>    | <span data-ttu-id="db5e8-128">x</span><span class="sxs-lookup"><span data-stu-id="db5e8-128">x</span></span>    | <span data-ttu-id="db5e8-129">x</span><span class="sxs-lookup"><span data-stu-id="db5e8-129">x</span></span>     | <span data-ttu-id="db5e8-130">x</span><span class="sxs-lookup"><span data-stu-id="db5e8-130">x</span></span>    | <span data-ttu-id="db5e8-131">x</span><span class="sxs-lookup"><span data-stu-id="db5e8-131">x</span></span>     |



 

<span data-ttu-id="db5e8-132">O trecho de código a seguir mostra as operações executadas:</span><span class="sxs-lookup"><span data-stu-id="db5e8-132">The following code snippet shows the operations performed:</span></span>


```
dest.x = dest.y = dest.z = dest.w = 
    (src0.x * src1.x) + (src0.y * src1.y) + 
    (src0.z * src1.z) + (src0.w * src1.w);
```



<span data-ttu-id="db5e8-133">Limitações para PS \_ 1 \_ 2 e PS \_ 1 \_ 3:</span><span class="sxs-lookup"><span data-stu-id="db5e8-133">Limitations for ps\_1\_2 and ps\_1\_3:</span></span>

-   <span data-ttu-id="db5e8-134">Cada sombreador pode usar até quatro instruções DP4.</span><span class="sxs-lookup"><span data-stu-id="db5e8-134">Each shader can use up to a maximum of four dp4 instructions.</span></span>
-   <span data-ttu-id="db5e8-135">Cada instrução DP4 conta como duas instruções aritméticas.</span><span class="sxs-lookup"><span data-stu-id="db5e8-135">Each dp4 instruction counts as two arithmetic instructions.</span></span>

<span data-ttu-id="db5e8-136">Limitações para \_ as versões 1 X:</span><span class="sxs-lookup"><span data-stu-id="db5e8-136">Limitations for 1\_X versions:</span></span>

-   <span data-ttu-id="db5e8-137">Essa instrução não pode ser emitida em conjunto porque DP4 é executado no pipeline de vetor e alfa.</span><span class="sxs-lookup"><span data-stu-id="db5e8-137">This instruction cannot be co-issued because dp4 runs in both the vector and alpha pipeline.</span></span>

## <a name="related-topics"></a><span data-ttu-id="db5e8-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="db5e8-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db5e8-139">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="db5e8-139">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




