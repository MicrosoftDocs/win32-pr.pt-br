---
title: máximo de PS
description: Calcula o máximo das fontes. | máximo de PS
ms.assetid: 3d3bef5b-0ff7-441b-8681-a3f4cde0ae4f
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c6186f0bd57acd4862a62a4c0a30ae92118b75ce
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968538"
---
# <a name="max---ps"></a><span data-ttu-id="48bbd-104">máximo de PS</span><span class="sxs-lookup"><span data-stu-id="48bbd-104">max - ps</span></span>

<span data-ttu-id="48bbd-105">Calcula o máximo das fontes.</span><span class="sxs-lookup"><span data-stu-id="48bbd-105">Calculates the maximum of the sources.</span></span>

## <a name="syntax"></a><span data-ttu-id="48bbd-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="48bbd-106">Syntax</span></span>



| <span data-ttu-id="48bbd-107">máximo de DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="48bbd-107">max dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="48bbd-108">onde</span><span class="sxs-lookup"><span data-stu-id="48bbd-108">where</span></span>

-   <span data-ttu-id="48bbd-109">DST é o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="48bbd-109">dst is the destination register.</span></span>
-   <span data-ttu-id="48bbd-110">src0 é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="48bbd-110">src0 is a source register.</span></span>
-   <span data-ttu-id="48bbd-111">src1 é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="48bbd-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="48bbd-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="48bbd-112">Remarks</span></span>



| <span data-ttu-id="48bbd-113">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="48bbd-113">Pixel shader versions</span></span> | <span data-ttu-id="48bbd-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="48bbd-114">1\_1</span></span> | <span data-ttu-id="48bbd-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="48bbd-115">1\_2</span></span> | <span data-ttu-id="48bbd-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="48bbd-116">1\_3</span></span> | <span data-ttu-id="48bbd-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="48bbd-117">1\_4</span></span> | <span data-ttu-id="48bbd-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="48bbd-118">2\_0</span></span> | <span data-ttu-id="48bbd-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="48bbd-119">2\_x</span></span> | <span data-ttu-id="48bbd-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="48bbd-120">2\_sw</span></span> | <span data-ttu-id="48bbd-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="48bbd-121">3\_0</span></span> | <span data-ttu-id="48bbd-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="48bbd-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="48bbd-123">max</span><span class="sxs-lookup"><span data-stu-id="48bbd-123">max</span></span>                   |      |      |      |      | <span data-ttu-id="48bbd-124">x</span><span class="sxs-lookup"><span data-stu-id="48bbd-124">x</span></span>    | <span data-ttu-id="48bbd-125">x</span><span class="sxs-lookup"><span data-stu-id="48bbd-125">x</span></span>    | <span data-ttu-id="48bbd-126">x</span><span class="sxs-lookup"><span data-stu-id="48bbd-126">x</span></span>     | <span data-ttu-id="48bbd-127">x</span><span class="sxs-lookup"><span data-stu-id="48bbd-127">x</span></span>    | <span data-ttu-id="48bbd-128">x</span><span class="sxs-lookup"><span data-stu-id="48bbd-128">x</span></span>     |



 

<span data-ttu-id="48bbd-129">O trecho de código a seguir mostra as operações executadas.</span><span class="sxs-lookup"><span data-stu-id="48bbd-129">The following code snippet shows the operations performed.</span></span>


```
dest.x=(src0.x >= src1.x) ? src0.x : src1.x;
dest.y=(src0.y >= src1.y) ? src0.y : src1.y;
dest.z=(src0.z >= src1.z) ? src0.z : src1.z;
dest.w=(src0.w >= src1.w) ? src0.w : src1.w;
```



## <a name="related-topics"></a><span data-ttu-id="48bbd-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="48bbd-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48bbd-131">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="48bbd-131">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




