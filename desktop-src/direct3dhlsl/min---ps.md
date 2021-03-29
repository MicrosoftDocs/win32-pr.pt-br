---
title: min-PS
description: Calcula o mínimo das fontes. | min-PS
ms.assetid: 2ee6208d-a353-4747-8037-c21dd1a05016
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3a735b38769a30e9dccf544785d931641469f5dc
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968404"
---
# <a name="min---ps"></a><span data-ttu-id="91301-104">min-PS</span><span class="sxs-lookup"><span data-stu-id="91301-104">min - ps</span></span>

<span data-ttu-id="91301-105">Calcula o mínimo das fontes.</span><span class="sxs-lookup"><span data-stu-id="91301-105">Calculates the minimum of the sources.</span></span>

## <a name="syntax"></a><span data-ttu-id="91301-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="91301-106">Syntax</span></span>



| <span data-ttu-id="91301-107">mínimo de DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="91301-107">min dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="91301-108">onde</span><span class="sxs-lookup"><span data-stu-id="91301-108">where</span></span>

-   <span data-ttu-id="91301-109">DST é o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="91301-109">dst is the destination register.</span></span>
-   <span data-ttu-id="91301-110">src0 é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="91301-110">src0 is a source register.</span></span>
-   <span data-ttu-id="91301-111">src1 é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="91301-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="91301-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="91301-112">Remarks</span></span>



| <span data-ttu-id="91301-113">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="91301-113">Pixel shader versions</span></span> | <span data-ttu-id="91301-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="91301-114">1\_1</span></span> | <span data-ttu-id="91301-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="91301-115">1\_2</span></span> | <span data-ttu-id="91301-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="91301-116">1\_3</span></span> | <span data-ttu-id="91301-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="91301-117">1\_4</span></span> | <span data-ttu-id="91301-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="91301-118">2\_0</span></span> | <span data-ttu-id="91301-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="91301-119">2\_x</span></span> | <span data-ttu-id="91301-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="91301-120">2\_sw</span></span> | <span data-ttu-id="91301-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="91301-121">3\_0</span></span> | <span data-ttu-id="91301-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="91301-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="91301-123">min</span><span class="sxs-lookup"><span data-stu-id="91301-123">min</span></span>                   |      |      |      |      | <span data-ttu-id="91301-124">x</span><span class="sxs-lookup"><span data-stu-id="91301-124">x</span></span>    | <span data-ttu-id="91301-125">x</span><span class="sxs-lookup"><span data-stu-id="91301-125">x</span></span>    | <span data-ttu-id="91301-126">x</span><span class="sxs-lookup"><span data-stu-id="91301-126">x</span></span>     | <span data-ttu-id="91301-127">x</span><span class="sxs-lookup"><span data-stu-id="91301-127">x</span></span>    | <span data-ttu-id="91301-128">x</span><span class="sxs-lookup"><span data-stu-id="91301-128">x</span></span>     |



 

<span data-ttu-id="91301-129">O trecho de código a seguir mostra as operações executadas.</span><span class="sxs-lookup"><span data-stu-id="91301-129">The following code snippet shows the operations performed.</span></span>


```
dest.x=(src0.x < src1.x) ? src0.x : src1.x;
dest.y=(src0.y < src1.y) ? src0.y : src1.y;
dest.z=(src0.z < src1.z) ? src0.z : src1.z;
dest.w=(src0.w < src1.w) ? src0.w : src1.w;
```



## <a name="related-topics"></a><span data-ttu-id="91301-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="91301-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91301-131">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="91301-131">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




