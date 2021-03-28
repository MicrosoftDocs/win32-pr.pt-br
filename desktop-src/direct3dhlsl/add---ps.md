---
title: Adicionar-PS
description: Adiciona dois vetores. | Adicionar-PS
ms.assetid: f7d29a66-879b-4160-82fd-0a1b2076559a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f8c6ef7c14ac54610301f283d076751b0c4d4a5e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968293"
---
# <a name="add---ps"></a><span data-ttu-id="48899-104">Adicionar-PS</span><span class="sxs-lookup"><span data-stu-id="48899-104">add - ps</span></span>

<span data-ttu-id="48899-105">Adiciona dois vetores.</span><span class="sxs-lookup"><span data-stu-id="48899-105">Adds two vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="48899-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="48899-106">Syntax</span></span>



| <span data-ttu-id="48899-107">Adicionar DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="48899-107">add dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="48899-108">onde</span><span class="sxs-lookup"><span data-stu-id="48899-108">where</span></span>

-   <span data-ttu-id="48899-109">DST é o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="48899-109">dst is the destination register.</span></span>
-   <span data-ttu-id="48899-110">src0 é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="48899-110">src0 is a source register.</span></span>
-   <span data-ttu-id="48899-111">src1 é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="48899-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="48899-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="48899-112">Remarks</span></span>



| <span data-ttu-id="48899-113">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="48899-113">Pixel shader versions</span></span> | <span data-ttu-id="48899-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="48899-114">1\_1</span></span> | <span data-ttu-id="48899-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="48899-115">1\_2</span></span> | <span data-ttu-id="48899-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="48899-116">1\_3</span></span> | <span data-ttu-id="48899-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="48899-117">1\_4</span></span> | <span data-ttu-id="48899-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="48899-118">2\_0</span></span> | <span data-ttu-id="48899-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="48899-119">2\_x</span></span> | <span data-ttu-id="48899-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="48899-120">2\_sw</span></span> | <span data-ttu-id="48899-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="48899-121">3\_0</span></span> | <span data-ttu-id="48899-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="48899-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="48899-123">add</span><span class="sxs-lookup"><span data-stu-id="48899-123">add</span></span>                   | <span data-ttu-id="48899-124">x</span><span class="sxs-lookup"><span data-stu-id="48899-124">x</span></span>    | <span data-ttu-id="48899-125">x</span><span class="sxs-lookup"><span data-stu-id="48899-125">x</span></span>    | <span data-ttu-id="48899-126">x</span><span class="sxs-lookup"><span data-stu-id="48899-126">x</span></span>    | <span data-ttu-id="48899-127">x</span><span class="sxs-lookup"><span data-stu-id="48899-127">x</span></span>    | <span data-ttu-id="48899-128">x</span><span class="sxs-lookup"><span data-stu-id="48899-128">x</span></span>    | <span data-ttu-id="48899-129">x</span><span class="sxs-lookup"><span data-stu-id="48899-129">x</span></span>    | <span data-ttu-id="48899-130">x</span><span class="sxs-lookup"><span data-stu-id="48899-130">x</span></span>     | <span data-ttu-id="48899-131">x</span><span class="sxs-lookup"><span data-stu-id="48899-131">x</span></span>    | <span data-ttu-id="48899-132">x</span><span class="sxs-lookup"><span data-stu-id="48899-132">x</span></span>     |



 

<span data-ttu-id="48899-133">O trecho de código a seguir mostra as operações executadas.</span><span class="sxs-lookup"><span data-stu-id="48899-133">The following code snippet shows the operations performed.</span></span>


```
dest.x = src0.x + src1.x;
dest.y = src0.y + src1.y;
dest.z = src0.z + src1.z;
dest.w = src0.w + src1.w;
```



## <a name="instruction-information"></a><span data-ttu-id="48899-134">Informações de instrução</span><span class="sxs-lookup"><span data-stu-id="48899-134">Instruction Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="48899-135">Sistema operacional mínimo</span><span class="sxs-lookup"><span data-stu-id="48899-135">Minimum operating system</span></span> | <span data-ttu-id="48899-136">Windows 98</span><span class="sxs-lookup"><span data-stu-id="48899-136">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="48899-137">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="48899-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48899-138">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="48899-138">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




