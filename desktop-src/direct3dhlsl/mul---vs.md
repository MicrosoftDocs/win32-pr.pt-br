---
title: Mul-vs
description: Multiplica as fontes no destino. | Mul-vs
ms.assetid: 0b048cc2-b165-418f-893e-6dee28ca5ad3
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e33ac35831b19f771f4f5b64d94bcc47c6657db5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104989184"
---
# <a name="mul---vs"></a><span data-ttu-id="83d5f-104">Mul-vs</span><span class="sxs-lookup"><span data-stu-id="83d5f-104">mul - vs</span></span>

<span data-ttu-id="83d5f-105">Multiplica as fontes no destino.</span><span class="sxs-lookup"><span data-stu-id="83d5f-105">Multiplies sources into the destination.</span></span>

## <a name="syntax"></a><span data-ttu-id="83d5f-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="83d5f-106">Syntax</span></span>



| <span data-ttu-id="83d5f-107">Mul DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="83d5f-107">mul dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="83d5f-108">onde</span><span class="sxs-lookup"><span data-stu-id="83d5f-108">where</span></span>

-   <span data-ttu-id="83d5f-109">DST é o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="83d5f-109">dst is the destination register.</span></span>
-   <span data-ttu-id="83d5f-110">src0 é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="83d5f-110">src0 is a source register.</span></span>
-   <span data-ttu-id="83d5f-111">src1 é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="83d5f-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="83d5f-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="83d5f-112">Remarks</span></span>



| <span data-ttu-id="83d5f-113">Versões do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="83d5f-113">Vertex shader versions</span></span> | <span data-ttu-id="83d5f-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="83d5f-114">1\_1</span></span> | <span data-ttu-id="83d5f-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="83d5f-115">2\_0</span></span> | <span data-ttu-id="83d5f-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="83d5f-116">2\_x</span></span> | <span data-ttu-id="83d5f-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="83d5f-117">2\_sw</span></span> | <span data-ttu-id="83d5f-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="83d5f-118">3\_0</span></span> | <span data-ttu-id="83d5f-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="83d5f-119">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="83d5f-120">mul</span><span class="sxs-lookup"><span data-stu-id="83d5f-120">mul</span></span>                    | <span data-ttu-id="83d5f-121">x</span><span class="sxs-lookup"><span data-stu-id="83d5f-121">x</span></span>    | <span data-ttu-id="83d5f-122">x</span><span class="sxs-lookup"><span data-stu-id="83d5f-122">x</span></span>    | <span data-ttu-id="83d5f-123">x</span><span class="sxs-lookup"><span data-stu-id="83d5f-123">x</span></span>    | <span data-ttu-id="83d5f-124">x</span><span class="sxs-lookup"><span data-stu-id="83d5f-124">x</span></span>     | <span data-ttu-id="83d5f-125">x</span><span class="sxs-lookup"><span data-stu-id="83d5f-125">x</span></span>    | <span data-ttu-id="83d5f-126">x</span><span class="sxs-lookup"><span data-stu-id="83d5f-126">x</span></span>     |



 

<span data-ttu-id="83d5f-127">O fragmento de código a seguir mostra as operações executadas.</span><span class="sxs-lookup"><span data-stu-id="83d5f-127">The following code fragment shows the operations performed.</span></span>


```
dest.x = src0.x * src1.x;
dest.y = src0.y * src1.y;
dest.z = src0.z * src1.z;
dest.w = src0.w * src1.w;
```



## <a name="related-topics"></a><span data-ttu-id="83d5f-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="83d5f-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83d5f-129">Instruções do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="83d5f-129">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




