---
title: sub-vs
description: Subtrai fontes. | sub-vs
ms.assetid: ccd7ca57-05a9-4ee8-8bda-c8c875476aaf
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a4bf15522798e1da5ec0bde5b729f241ff9dabde
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103930415"
---
# <a name="sub---vs"></a><span data-ttu-id="4dd48-104">sub-vs</span><span class="sxs-lookup"><span data-stu-id="4dd48-104">sub - vs</span></span>

<span data-ttu-id="4dd48-105">Subtrai fontes.</span><span class="sxs-lookup"><span data-stu-id="4dd48-105">Subtracts sources.</span></span>

## <a name="syntax"></a><span data-ttu-id="4dd48-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="4dd48-106">Syntax</span></span>



| <span data-ttu-id="4dd48-107">subdst, src0, src1</span><span class="sxs-lookup"><span data-stu-id="4dd48-107">sub dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="4dd48-108">onde</span><span class="sxs-lookup"><span data-stu-id="4dd48-108">where</span></span>

-   <span data-ttu-id="4dd48-109">DST é o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="4dd48-109">dst is the destination register.</span></span>
-   <span data-ttu-id="4dd48-110">src0 é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="4dd48-110">src0 is a source register.</span></span>
-   <span data-ttu-id="4dd48-111">src1 é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="4dd48-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="4dd48-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="4dd48-112">Remarks</span></span>



| <span data-ttu-id="4dd48-113">Versões do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="4dd48-113">Vertex shader versions</span></span> | <span data-ttu-id="4dd48-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="4dd48-114">1\_1</span></span> | <span data-ttu-id="4dd48-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4dd48-115">2\_0</span></span> | <span data-ttu-id="4dd48-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="4dd48-116">2\_x</span></span> | <span data-ttu-id="4dd48-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="4dd48-117">2\_sw</span></span> | <span data-ttu-id="4dd48-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4dd48-118">3\_0</span></span> | <span data-ttu-id="4dd48-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="4dd48-119">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="4dd48-120">sub</span><span class="sxs-lookup"><span data-stu-id="4dd48-120">sub</span></span>                    | <span data-ttu-id="4dd48-121">x</span><span class="sxs-lookup"><span data-stu-id="4dd48-121">x</span></span>    | <span data-ttu-id="4dd48-122">x</span><span class="sxs-lookup"><span data-stu-id="4dd48-122">x</span></span>    | <span data-ttu-id="4dd48-123">x</span><span class="sxs-lookup"><span data-stu-id="4dd48-123">x</span></span>    | <span data-ttu-id="4dd48-124">x</span><span class="sxs-lookup"><span data-stu-id="4dd48-124">x</span></span>     | <span data-ttu-id="4dd48-125">x</span><span class="sxs-lookup"><span data-stu-id="4dd48-125">x</span></span>    | <span data-ttu-id="4dd48-126">x</span><span class="sxs-lookup"><span data-stu-id="4dd48-126">x</span></span>     |



 

<span data-ttu-id="4dd48-127">Essa instrução executa a subtração mostrada nesta fórmula.</span><span class="sxs-lookup"><span data-stu-id="4dd48-127">This instruction performs the subtraction shown in this formula.</span></span>


```
dest.x = src0.x - src1.x
dest.y = src0.y - src1.y
dest.z = src0.z - src1.z
dest.w = src0.w - src1.w
```



## <a name="related-topics"></a><span data-ttu-id="4dd48-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4dd48-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4dd48-129">Instruções do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="4dd48-129">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




