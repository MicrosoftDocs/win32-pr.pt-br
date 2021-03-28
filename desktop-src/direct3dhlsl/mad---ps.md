---
title: Mad-PS
description: Multiplicar e adicionar instrução. Define o registro de destino como (src0 \ src1) + src2.
ms.assetid: 0bcf5dcc-3657-4ee0-9aeb-bd2d8feea7a6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b3570f5826f91b35b07478e1ea34940a27d706cf
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104365247"
---
# <a name="mad---ps"></a><span data-ttu-id="55619-104">Mad-PS</span><span class="sxs-lookup"><span data-stu-id="55619-104">mad - ps</span></span>

<span data-ttu-id="55619-105">Multiplicar e adicionar instrução.</span><span class="sxs-lookup"><span data-stu-id="55619-105">Multiply and add instruction.</span></span> <span data-ttu-id="55619-106">Define o registro de destino como (src0 \* src1) + src2.</span><span class="sxs-lookup"><span data-stu-id="55619-106">Sets the destination register to (src0 \* src1) + src2.</span></span>

## <a name="syntax"></a><span data-ttu-id="55619-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="55619-107">Syntax</span></span>



| <span data-ttu-id="55619-108">Mad DST, src0, src1, src2</span><span class="sxs-lookup"><span data-stu-id="55619-108">mad dst, src0, src1, src2</span></span> |
|---------------------------|



 

<span data-ttu-id="55619-109">onde</span><span class="sxs-lookup"><span data-stu-id="55619-109">where</span></span>

-   <span data-ttu-id="55619-110">DST é o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="55619-110">dst is the destination register.</span></span>
-   <span data-ttu-id="55619-111">src0 é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="55619-111">src0 is a source register.</span></span>
-   <span data-ttu-id="55619-112">src1 é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="55619-112">src1 is a source register.</span></span>
-   <span data-ttu-id="55619-113">src2 é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="55619-113">src2 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="55619-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="55619-114">Remarks</span></span>



| <span data-ttu-id="55619-115">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="55619-115">Pixel shader versions</span></span> | <span data-ttu-id="55619-116">1\_1</span><span class="sxs-lookup"><span data-stu-id="55619-116">1\_1</span></span> | <span data-ttu-id="55619-117">1\_2</span><span class="sxs-lookup"><span data-stu-id="55619-117">1\_2</span></span> | <span data-ttu-id="55619-118">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="55619-118">1\_3</span></span> | <span data-ttu-id="55619-119">1\_4</span><span class="sxs-lookup"><span data-stu-id="55619-119">1\_4</span></span> | <span data-ttu-id="55619-120">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="55619-120">2\_0</span></span> | <span data-ttu-id="55619-121">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="55619-121">2\_x</span></span> | <span data-ttu-id="55619-122">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="55619-122">2\_sw</span></span> | <span data-ttu-id="55619-123">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="55619-123">3\_0</span></span> | <span data-ttu-id="55619-124">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="55619-124">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="55619-125">Mad</span><span class="sxs-lookup"><span data-stu-id="55619-125">mad</span></span>                   | <span data-ttu-id="55619-126">x</span><span class="sxs-lookup"><span data-stu-id="55619-126">x</span></span>    | <span data-ttu-id="55619-127">x</span><span class="sxs-lookup"><span data-stu-id="55619-127">x</span></span>    | <span data-ttu-id="55619-128">x</span><span class="sxs-lookup"><span data-stu-id="55619-128">x</span></span>    | <span data-ttu-id="55619-129">x</span><span class="sxs-lookup"><span data-stu-id="55619-129">x</span></span>    | <span data-ttu-id="55619-130">x</span><span class="sxs-lookup"><span data-stu-id="55619-130">x</span></span>    | <span data-ttu-id="55619-131">x</span><span class="sxs-lookup"><span data-stu-id="55619-131">x</span></span>    | <span data-ttu-id="55619-132">x</span><span class="sxs-lookup"><span data-stu-id="55619-132">x</span></span>     | <span data-ttu-id="55619-133">x</span><span class="sxs-lookup"><span data-stu-id="55619-133">x</span></span>    | <span data-ttu-id="55619-134">x</span><span class="sxs-lookup"><span data-stu-id="55619-134">x</span></span>     |



 

<span data-ttu-id="55619-135">O trecho de código a seguir mostra as operações executadas.</span><span class="sxs-lookup"><span data-stu-id="55619-135">The following code snippet shows the operations performed.</span></span>


```
dest.x = src0.x * src1.x + src2.x;
dest.y = src0.y * src1.y + src2.y;
dest.z = src0.z * src1.z + src2.z;
dest.w = src0.w * src1.w + src2.w;
```



## <a name="related-topics"></a><span data-ttu-id="55619-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="55619-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55619-137">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="55619-137">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




