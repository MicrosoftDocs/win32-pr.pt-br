---
title: ABS-PS
description: Calcula o valor absoluto. | ABS-PS
ms.assetid: e97db550-2a03-421a-86f4-a6fc5f8e0bca
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 070a513aaa0d336d5ac404b1748fdd162edfd532
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104298080"
---
# <a name="abs---ps"></a><span data-ttu-id="fae44-104">ABS-PS</span><span class="sxs-lookup"><span data-stu-id="fae44-104">abs - ps</span></span>

<span data-ttu-id="fae44-105">Calcula o valor absoluto.</span><span class="sxs-lookup"><span data-stu-id="fae44-105">Computes absolute value.</span></span>

## <a name="syntax"></a><span data-ttu-id="fae44-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="fae44-106">Syntax</span></span>



|              |
|--------------|
| <span data-ttu-id="fae44-107">ABS DST, src</span><span class="sxs-lookup"><span data-stu-id="fae44-107">abs dst, src</span></span> |



 

<span data-ttu-id="fae44-108">onde</span><span class="sxs-lookup"><span data-stu-id="fae44-108">where</span></span>

-   <span data-ttu-id="fae44-109">DST é o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="fae44-109">dst is the destination register.</span></span>
-   <span data-ttu-id="fae44-110">src é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="fae44-110">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="fae44-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="fae44-111">Remarks</span></span>



|                       |      |      |      |      |      |      |       |      |       |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="fae44-112">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="fae44-112">Pixel shader versions</span></span> | <span data-ttu-id="fae44-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="fae44-113">1\_1</span></span> | <span data-ttu-id="fae44-114">1\_2</span><span class="sxs-lookup"><span data-stu-id="fae44-114">1\_2</span></span> | <span data-ttu-id="fae44-115">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="fae44-115">1\_3</span></span> | <span data-ttu-id="fae44-116">1\_4</span><span class="sxs-lookup"><span data-stu-id="fae44-116">1\_4</span></span> | <span data-ttu-id="fae44-117">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="fae44-117">2\_0</span></span> | <span data-ttu-id="fae44-118">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="fae44-118">2\_x</span></span> | <span data-ttu-id="fae44-119">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="fae44-119">2\_sw</span></span> | <span data-ttu-id="fae44-120">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="fae44-120">3\_0</span></span> | <span data-ttu-id="fae44-121">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="fae44-121">3\_sw</span></span> |
| <span data-ttu-id="fae44-122">abs</span><span class="sxs-lookup"><span data-stu-id="fae44-122">abs</span></span>                   |      |      |      |      | <span data-ttu-id="fae44-123">x</span><span class="sxs-lookup"><span data-stu-id="fae44-123">x</span></span>    | <span data-ttu-id="fae44-124">x</span><span class="sxs-lookup"><span data-stu-id="fae44-124">x</span></span>    | <span data-ttu-id="fae44-125">x</span><span class="sxs-lookup"><span data-stu-id="fae44-125">x</span></span>     | <span data-ttu-id="fae44-126">x</span><span class="sxs-lookup"><span data-stu-id="fae44-126">x</span></span>    | <span data-ttu-id="fae44-127">x</span><span class="sxs-lookup"><span data-stu-id="fae44-127">x</span></span>     |



 

<span data-ttu-id="fae44-128">Essa instrução funciona como mostrado aqui.</span><span class="sxs-lookup"><span data-stu-id="fae44-128">This instruction works as shown here.</span></span>


```
dest.x = abs(src.x)
dest.y = abs(src.y)
dest.z = abs(src.z)
dest.w = abs(src.w)
```



## <a name="instruction-information"></a><span data-ttu-id="fae44-129">Informações de instrução</span><span class="sxs-lookup"><span data-stu-id="fae44-129">Instruction Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="fae44-130">Sistema operacional mínimo</span><span class="sxs-lookup"><span data-stu-id="fae44-130">Minimum operating system</span></span> | <span data-ttu-id="fae44-131">Windows 98</span><span class="sxs-lookup"><span data-stu-id="fae44-131">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="fae44-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fae44-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fae44-133">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="fae44-133">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




