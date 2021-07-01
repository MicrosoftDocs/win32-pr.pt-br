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
ms.openlocfilehash: 54092caf19a486b68b92ef63d992f11289a51c93
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/01/2021
ms.locfileid: "113130085"
---
# <a name="add---ps"></a><span data-ttu-id="b2e45-104">Adicionar-PS</span><span class="sxs-lookup"><span data-stu-id="b2e45-104">add - ps</span></span>

<span data-ttu-id="b2e45-105">Adiciona dois vetores.</span><span class="sxs-lookup"><span data-stu-id="b2e45-105">Adds two vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2e45-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b2e45-106">Syntax</span></span>



| <span data-ttu-id="b2e45-107">Adicionar DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="b2e45-107">add dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="b2e45-108">onde</span><span class="sxs-lookup"><span data-stu-id="b2e45-108">where</span></span>

-   <span data-ttu-id="b2e45-109">DST é o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="b2e45-109">dst is the destination register.</span></span>
-   <span data-ttu-id="b2e45-110">src0 é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="b2e45-110">src0 is a source register.</span></span>
-   <span data-ttu-id="b2e45-111">src1 é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="b2e45-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2e45-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="b2e45-112">Remarks</span></span>



| <span data-ttu-id="b2e45-113">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="b2e45-113">Pixel shader versions</span></span> | <span data-ttu-id="b2e45-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="b2e45-114">1\_1</span></span> | <span data-ttu-id="b2e45-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="b2e45-115">1\_2</span></span> | <span data-ttu-id="b2e45-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="b2e45-116">1\_3</span></span> | <span data-ttu-id="b2e45-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="b2e45-117">1\_4</span></span> | <span data-ttu-id="b2e45-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b2e45-118">2\_0</span></span> | <span data-ttu-id="b2e45-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="b2e45-119">2\_x</span></span> | <span data-ttu-id="b2e45-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="b2e45-120">2\_sw</span></span> | <span data-ttu-id="b2e45-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b2e45-121">3\_0</span></span> | <span data-ttu-id="b2e45-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="b2e45-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="b2e45-123">add</span><span class="sxs-lookup"><span data-stu-id="b2e45-123">add</span></span>                   | <span data-ttu-id="b2e45-124">x</span><span class="sxs-lookup"><span data-stu-id="b2e45-124">x</span></span>    | <span data-ttu-id="b2e45-125">x</span><span class="sxs-lookup"><span data-stu-id="b2e45-125">x</span></span>    | <span data-ttu-id="b2e45-126">x</span><span class="sxs-lookup"><span data-stu-id="b2e45-126">x</span></span>    | <span data-ttu-id="b2e45-127">x</span><span class="sxs-lookup"><span data-stu-id="b2e45-127">x</span></span>    | <span data-ttu-id="b2e45-128">x</span><span class="sxs-lookup"><span data-stu-id="b2e45-128">x</span></span>    | <span data-ttu-id="b2e45-129">x</span><span class="sxs-lookup"><span data-stu-id="b2e45-129">x</span></span>    | <span data-ttu-id="b2e45-130">x</span><span class="sxs-lookup"><span data-stu-id="b2e45-130">x</span></span>     | <span data-ttu-id="b2e45-131">x</span><span class="sxs-lookup"><span data-stu-id="b2e45-131">x</span></span>    | <span data-ttu-id="b2e45-132">x</span><span class="sxs-lookup"><span data-stu-id="b2e45-132">x</span></span>     |



 

<span data-ttu-id="b2e45-133">O trecho de código a seguir mostra as operações executadas.</span><span class="sxs-lookup"><span data-stu-id="b2e45-133">The following code snippet shows the operations performed.</span></span>


```
dest.x = src0.x + src1.x;
dest.y = src0.y + src1.y;
dest.z = src0.z + src1.z;
dest.w = src0.w + src1.w;
```



## <a name="instruction-information"></a><span data-ttu-id="b2e45-134">Informações de instrução</span><span class="sxs-lookup"><span data-stu-id="b2e45-134">Instruction Information</span></span>



|   <span data-ttu-id="b2e45-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2e45-135">Requirement</span></span>                       | <span data-ttu-id="b2e45-136">Valor</span><span class="sxs-lookup"><span data-stu-id="b2e45-136">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="b2e45-137">Sistema operacional mínimo</span><span class="sxs-lookup"><span data-stu-id="b2e45-137">Minimum operating system</span></span> | <span data-ttu-id="b2e45-138">Windows 98</span><span class="sxs-lookup"><span data-stu-id="b2e45-138">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="b2e45-139">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b2e45-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2e45-140">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="b2e45-140">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




