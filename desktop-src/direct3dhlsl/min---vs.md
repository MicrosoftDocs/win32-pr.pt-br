---
title: min-vs
description: Calcula o mínimo das fontes. | min-vs
ms.assetid: cecfe98b-8efd-4fbf-a7b5-d228de724e71
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: eda47b75398b8643f7010ff7468f72f4a7d8c199
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968456"
---
# <a name="min---vs"></a><span data-ttu-id="ee7a4-104">min-vs</span><span class="sxs-lookup"><span data-stu-id="ee7a4-104">min - vs</span></span>

<span data-ttu-id="ee7a4-105">Calcula o mínimo das fontes.</span><span class="sxs-lookup"><span data-stu-id="ee7a4-105">Calculates the minimum of the sources.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee7a4-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="ee7a4-106">Syntax</span></span>



| <span data-ttu-id="ee7a4-107">mínimo de DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="ee7a4-107">min dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="ee7a4-108">onde</span><span class="sxs-lookup"><span data-stu-id="ee7a4-108">where</span></span>

-   <span data-ttu-id="ee7a4-109">DST é o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="ee7a4-109">dst is the destination register.</span></span>
-   <span data-ttu-id="ee7a4-110">src0 é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="ee7a4-110">src0 is a source register.</span></span>
-   <span data-ttu-id="ee7a4-111">src1 é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="ee7a4-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee7a4-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="ee7a4-112">Remarks</span></span>



| <span data-ttu-id="ee7a4-113">Versões do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="ee7a4-113">Vertex shader versions</span></span> | <span data-ttu-id="ee7a4-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="ee7a4-114">1\_1</span></span> | <span data-ttu-id="ee7a4-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ee7a4-115">2\_0</span></span> | <span data-ttu-id="ee7a4-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="ee7a4-116">2\_x</span></span> | <span data-ttu-id="ee7a4-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="ee7a4-117">2\_sw</span></span> | <span data-ttu-id="ee7a4-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ee7a4-118">3\_0</span></span> | <span data-ttu-id="ee7a4-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="ee7a4-119">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="ee7a4-120">min</span><span class="sxs-lookup"><span data-stu-id="ee7a4-120">min</span></span>                    | <span data-ttu-id="ee7a4-121">x</span><span class="sxs-lookup"><span data-stu-id="ee7a4-121">x</span></span>    | <span data-ttu-id="ee7a4-122">x</span><span class="sxs-lookup"><span data-stu-id="ee7a4-122">x</span></span>    | <span data-ttu-id="ee7a4-123">x</span><span class="sxs-lookup"><span data-stu-id="ee7a4-123">x</span></span>    | <span data-ttu-id="ee7a4-124">x</span><span class="sxs-lookup"><span data-stu-id="ee7a4-124">x</span></span>     | <span data-ttu-id="ee7a4-125">x</span><span class="sxs-lookup"><span data-stu-id="ee7a4-125">x</span></span>    | <span data-ttu-id="ee7a4-126">x</span><span class="sxs-lookup"><span data-stu-id="ee7a4-126">x</span></span>     |



 

<span data-ttu-id="ee7a4-127">O fragmento de código a seguir mostra as operações executadas.</span><span class="sxs-lookup"><span data-stu-id="ee7a4-127">The following code fragment shows the operations performed.</span></span>


```
dest.x=(src0.x < src1.x) ? src0.x : src1.x;
dest.y=(src0.y < src1.y) ? src0.y : src1.y;
dest.z=(src0.z < src1.z) ? src0.z : src1.z;
dest.w=(src0.w < src1.w) ? src0.w : src1.w;
```



## <a name="related-topics"></a><span data-ttu-id="ee7a4-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ee7a4-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ee7a4-129">Instruções do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="ee7a4-129">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




