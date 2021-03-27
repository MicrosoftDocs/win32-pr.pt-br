---
title: sub-PS
description: Subtrai fontes. | sub-PS
ms.assetid: e130724f-63bf-4d7f-bc9f-6a4441a788b8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4998892aa06eff55632600a9c2f7fe359c11f830
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103663858"
---
# <a name="sub---ps"></a><span data-ttu-id="9571b-104">sub-PS</span><span class="sxs-lookup"><span data-stu-id="9571b-104">sub - ps</span></span>

<span data-ttu-id="9571b-105">Subtrai fontes.</span><span class="sxs-lookup"><span data-stu-id="9571b-105">Subtracts sources.</span></span>

## <a name="syntax"></a><span data-ttu-id="9571b-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="9571b-106">Syntax</span></span>



| <span data-ttu-id="9571b-107">subdst, src0, src1</span><span class="sxs-lookup"><span data-stu-id="9571b-107">sub dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="9571b-108">onde</span><span class="sxs-lookup"><span data-stu-id="9571b-108">where</span></span>

-   <span data-ttu-id="9571b-109">DST é o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="9571b-109">dst is the destination register.</span></span>
-   <span data-ttu-id="9571b-110">src0 é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="9571b-110">src0 is a source register.</span></span>
-   <span data-ttu-id="9571b-111">src1 é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="9571b-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="9571b-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="9571b-112">Remarks</span></span>



| <span data-ttu-id="9571b-113">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="9571b-113">Pixel shader versions</span></span> | <span data-ttu-id="9571b-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="9571b-114">1\_1</span></span> | <span data-ttu-id="9571b-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="9571b-115">1\_2</span></span> | <span data-ttu-id="9571b-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="9571b-116">1\_3</span></span> | <span data-ttu-id="9571b-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="9571b-117">1\_4</span></span> | <span data-ttu-id="9571b-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9571b-118">2\_0</span></span> | <span data-ttu-id="9571b-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="9571b-119">2\_x</span></span> | <span data-ttu-id="9571b-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="9571b-120">2\_sw</span></span> | <span data-ttu-id="9571b-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9571b-121">3\_0</span></span> | <span data-ttu-id="9571b-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="9571b-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="9571b-123">sub</span><span class="sxs-lookup"><span data-stu-id="9571b-123">sub</span></span>                   | <span data-ttu-id="9571b-124">x</span><span class="sxs-lookup"><span data-stu-id="9571b-124">x</span></span>    | <span data-ttu-id="9571b-125">x</span><span class="sxs-lookup"><span data-stu-id="9571b-125">x</span></span>    | <span data-ttu-id="9571b-126">x</span><span class="sxs-lookup"><span data-stu-id="9571b-126">x</span></span>    | <span data-ttu-id="9571b-127">x</span><span class="sxs-lookup"><span data-stu-id="9571b-127">x</span></span>    | <span data-ttu-id="9571b-128">x</span><span class="sxs-lookup"><span data-stu-id="9571b-128">x</span></span>    | <span data-ttu-id="9571b-129">x</span><span class="sxs-lookup"><span data-stu-id="9571b-129">x</span></span>    | <span data-ttu-id="9571b-130">x</span><span class="sxs-lookup"><span data-stu-id="9571b-130">x</span></span>     | <span data-ttu-id="9571b-131">x</span><span class="sxs-lookup"><span data-stu-id="9571b-131">x</span></span>    | <span data-ttu-id="9571b-132">x</span><span class="sxs-lookup"><span data-stu-id="9571b-132">x</span></span>     |



 

<span data-ttu-id="9571b-133">Essa instrução executa a subtração mostrada nesta fórmula.</span><span class="sxs-lookup"><span data-stu-id="9571b-133">This instruction performs the subtraction shown in this formula.</span></span>


```
dest = src0 - src1
```



## <a name="related-topics"></a><span data-ttu-id="9571b-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9571b-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9571b-135">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="9571b-135">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




