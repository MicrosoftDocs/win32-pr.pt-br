---
title: máx.-vs
description: Calcula o máximo das fontes. | máx.-vs
ms.assetid: 93fb8fb2-c722-43e5-bfe4-a2e9d3cd2049
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 923da795210fe2be62a6dd84a53f0127fef21077
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968449"
---
# <a name="max---vs"></a><span data-ttu-id="cdee6-104">máx.-vs</span><span class="sxs-lookup"><span data-stu-id="cdee6-104">max - vs</span></span>

<span data-ttu-id="cdee6-105">Calcula o máximo das fontes.</span><span class="sxs-lookup"><span data-stu-id="cdee6-105">Calculates the maximum of the sources.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdee6-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="cdee6-106">Syntax</span></span>



| <span data-ttu-id="cdee6-107">máximo de DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="cdee6-107">max dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="cdee6-108">onde</span><span class="sxs-lookup"><span data-stu-id="cdee6-108">where</span></span>

-   <span data-ttu-id="cdee6-109">DST é o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="cdee6-109">dst is the destination register.</span></span>
-   <span data-ttu-id="cdee6-110">src0 é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="cdee6-110">src0 is a source register.</span></span>
-   <span data-ttu-id="cdee6-111">src1 é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="cdee6-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="cdee6-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="cdee6-112">Remarks</span></span>



| <span data-ttu-id="cdee6-113">Versões do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="cdee6-113">Vertex shader versions</span></span> | <span data-ttu-id="cdee6-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="cdee6-114">1\_1</span></span> | <span data-ttu-id="cdee6-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="cdee6-115">2\_0</span></span> | <span data-ttu-id="cdee6-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="cdee6-116">2\_x</span></span> | <span data-ttu-id="cdee6-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="cdee6-117">2\_sw</span></span> | <span data-ttu-id="cdee6-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="cdee6-118">3\_0</span></span> | <span data-ttu-id="cdee6-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="cdee6-119">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="cdee6-120">max</span><span class="sxs-lookup"><span data-stu-id="cdee6-120">max</span></span>                    | <span data-ttu-id="cdee6-121">x</span><span class="sxs-lookup"><span data-stu-id="cdee6-121">x</span></span>    | <span data-ttu-id="cdee6-122">x</span><span class="sxs-lookup"><span data-stu-id="cdee6-122">x</span></span>    | <span data-ttu-id="cdee6-123">x</span><span class="sxs-lookup"><span data-stu-id="cdee6-123">x</span></span>    | <span data-ttu-id="cdee6-124">x</span><span class="sxs-lookup"><span data-stu-id="cdee6-124">x</span></span>     | <span data-ttu-id="cdee6-125">x</span><span class="sxs-lookup"><span data-stu-id="cdee6-125">x</span></span>    | <span data-ttu-id="cdee6-126">x</span><span class="sxs-lookup"><span data-stu-id="cdee6-126">x</span></span>     |



 

<span data-ttu-id="cdee6-127">O fragmento de código a seguir mostra as operações executadas.</span><span class="sxs-lookup"><span data-stu-id="cdee6-127">The following code fragment shows the operations performed.</span></span>


```
dest.x=(src0.x >= src1.x) ? src0.x : src1.x;
dest.y=(src0.y >= src1.y) ? src0.y : src1.y;
dest.z=(src0.z >= src1.z) ? src0.z : src1.z;
dest.w=(src0.w >= src1.w) ? src0.w : src1.w;
```



## <a name="related-topics"></a><span data-ttu-id="cdee6-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="cdee6-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cdee6-129">Instruções do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="cdee6-129">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




