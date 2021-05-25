---
title: abs - ps
description: Calcula o valor absoluto. | abs - ps
ms.assetid: e97db550-2a03-421a-86f4-a6fc5f8e0bca
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f4f22261a114333ed77d67d7c0ac2738d3522054
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343322"
---
# <a name="abs---ps"></a><span data-ttu-id="cba5e-104">abs - ps</span><span class="sxs-lookup"><span data-stu-id="cba5e-104">abs - ps</span></span>

<span data-ttu-id="cba5e-105">Calcula o valor absoluto.</span><span class="sxs-lookup"><span data-stu-id="cba5e-105">Computes absolute value.</span></span>

## <a name="syntax"></a><span data-ttu-id="cba5e-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cba5e-106">Syntax</span></span>

<span data-ttu-id="cba5e-107">**abs dst, src**</span><span class="sxs-lookup"><span data-stu-id="cba5e-107">**abs dst, src**</span></span>

<span data-ttu-id="cba5e-108">onde</span><span class="sxs-lookup"><span data-stu-id="cba5e-108">where</span></span>

-   <span data-ttu-id="cba5e-109">dst é o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="cba5e-109">dst is the destination register.</span></span>
-   <span data-ttu-id="cba5e-110">src é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="cba5e-110">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="cba5e-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="cba5e-111">Remarks</span></span>



| <span data-ttu-id="cba5e-112">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="cba5e-112">Pixel shader versions</span></span> | <span data-ttu-id="cba5e-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="cba5e-113">1\_1</span></span> | <span data-ttu-id="cba5e-114">1\_2</span><span class="sxs-lookup"><span data-stu-id="cba5e-114">1\_2</span></span> | <span data-ttu-id="cba5e-115">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="cba5e-115">1\_3</span></span> | <span data-ttu-id="cba5e-116">1\_4</span><span class="sxs-lookup"><span data-stu-id="cba5e-116">1\_4</span></span> | <span data-ttu-id="cba5e-117">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="cba5e-117">2\_0</span></span> | <span data-ttu-id="cba5e-118">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="cba5e-118">2\_x</span></span> | <span data-ttu-id="cba5e-119">2 \_ sw</span><span class="sxs-lookup"><span data-stu-id="cba5e-119">2\_sw</span></span> | <span data-ttu-id="cba5e-120">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="cba5e-120">3\_0</span></span> | <span data-ttu-id="cba5e-121">3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="cba5e-121">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="cba5e-122">abs</span><span class="sxs-lookup"><span data-stu-id="cba5e-122">abs</span></span>                   |      |      |      |      | <span data-ttu-id="cba5e-123">x</span><span class="sxs-lookup"><span data-stu-id="cba5e-123">x</span></span>    | <span data-ttu-id="cba5e-124">x</span><span class="sxs-lookup"><span data-stu-id="cba5e-124">x</span></span>    | <span data-ttu-id="cba5e-125">x</span><span class="sxs-lookup"><span data-stu-id="cba5e-125">x</span></span>     | <span data-ttu-id="cba5e-126">x</span><span class="sxs-lookup"><span data-stu-id="cba5e-126">x</span></span>    | <span data-ttu-id="cba5e-127">x</span><span class="sxs-lookup"><span data-stu-id="cba5e-127">x</span></span>     |



 

<span data-ttu-id="cba5e-128">Essa instrução funciona conforme mostrado aqui.</span><span class="sxs-lookup"><span data-stu-id="cba5e-128">This instruction works as shown here.</span></span>


```
dest.x = abs(src.x)
dest.y = abs(src.y)
dest.z = abs(src.z)
dest.w = abs(src.w)
```



## <a name="instruction-information"></a><span data-ttu-id="cba5e-129">Informações de instrução</span><span class="sxs-lookup"><span data-stu-id="cba5e-129">Instruction Information</span></span>



| <span data-ttu-id="cba5e-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="cba5e-130">Requirement</span></span>                         | <span data-ttu-id="cba5e-131">Valor</span><span class="sxs-lookup"><span data-stu-id="cba5e-131">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="cba5e-132">Sistema operacional mínimo</span><span class="sxs-lookup"><span data-stu-id="cba5e-132">Minimum operating system</span></span> | <span data-ttu-id="cba5e-133">Windows 98</span><span class="sxs-lookup"><span data-stu-id="cba5e-133">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="cba5e-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="cba5e-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cba5e-135">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="cba5e-135">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




