---
title: Adicionar-vs
description: Adiciona dois vetores. | Adicionar-vs
ms.assetid: f66d3264-68be-4a4f-84fc-cc0f6c4245c9
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 678e7f815a819be2abf1d985516fe081d3c09c94
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103837728"
---
# <a name="add---vs"></a><span data-ttu-id="16bdd-104">Adicionar-vs</span><span class="sxs-lookup"><span data-stu-id="16bdd-104">add - vs</span></span>

<span data-ttu-id="16bdd-105">Adiciona dois vetores.</span><span class="sxs-lookup"><span data-stu-id="16bdd-105">Adds two vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="16bdd-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="16bdd-106">Syntax</span></span>



| <span data-ttu-id="16bdd-107">Adicionar DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="16bdd-107">add dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="16bdd-108">onde</span><span class="sxs-lookup"><span data-stu-id="16bdd-108">where</span></span>

-   <span data-ttu-id="16bdd-109">DST é o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="16bdd-109">dst is the destination register.</span></span>
-   <span data-ttu-id="16bdd-110">src0 é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="16bdd-110">src0 is a source register.</span></span>
-   <span data-ttu-id="16bdd-111">src1 é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="16bdd-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="16bdd-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="16bdd-112">Remarks</span></span>



| <span data-ttu-id="16bdd-113">Versões do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="16bdd-113">Vertex shader versions</span></span> | <span data-ttu-id="16bdd-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="16bdd-114">1\_1</span></span> | <span data-ttu-id="16bdd-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="16bdd-115">2\_0</span></span> | <span data-ttu-id="16bdd-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="16bdd-116">2\_x</span></span> | <span data-ttu-id="16bdd-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="16bdd-117">2\_sw</span></span> | <span data-ttu-id="16bdd-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="16bdd-118">3\_0</span></span> | <span data-ttu-id="16bdd-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="16bdd-119">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="16bdd-120">add</span><span class="sxs-lookup"><span data-stu-id="16bdd-120">add</span></span>                    | <span data-ttu-id="16bdd-121">x</span><span class="sxs-lookup"><span data-stu-id="16bdd-121">x</span></span>    | <span data-ttu-id="16bdd-122">x</span><span class="sxs-lookup"><span data-stu-id="16bdd-122">x</span></span>    | <span data-ttu-id="16bdd-123">x</span><span class="sxs-lookup"><span data-stu-id="16bdd-123">x</span></span>    | <span data-ttu-id="16bdd-124">x</span><span class="sxs-lookup"><span data-stu-id="16bdd-124">x</span></span>     | <span data-ttu-id="16bdd-125">x</span><span class="sxs-lookup"><span data-stu-id="16bdd-125">x</span></span>    | <span data-ttu-id="16bdd-126">x</span><span class="sxs-lookup"><span data-stu-id="16bdd-126">x</span></span>     |



 

<span data-ttu-id="16bdd-127">O fragmento de código a seguir mostra as operações executadas.</span><span class="sxs-lookup"><span data-stu-id="16bdd-127">The following code fragment shows the operations performed.</span></span>


```
dest.x = src0.x + src1.x;
dest.y = src0.y + src1.y;
dest.z = src0.z + src1.z;
dest.w = src0.w + src1.w;
```



## <a name="related-topics"></a><span data-ttu-id="16bdd-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="16bdd-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16bdd-129">Instruções do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="16bdd-129">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




