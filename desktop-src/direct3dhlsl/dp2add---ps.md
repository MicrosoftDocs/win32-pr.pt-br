---
title: dp2add-PS
description: Executa um produto 2D dot e uma adição escalar.
ms.assetid: 4226ee34-2e68-4536-b171-68f3b967182e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 88d3d28cc64bdb7caa1b7456e87711c3dbee2b13
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104084257"
---
# <a name="dp2add---ps"></a><span data-ttu-id="73985-103">dp2add-PS</span><span class="sxs-lookup"><span data-stu-id="73985-103">dp2add - ps</span></span>

<span data-ttu-id="73985-104">Executa um produto 2D dot e uma adição escalar.</span><span class="sxs-lookup"><span data-stu-id="73985-104">Performs a 2D dot product and a scalar addition.</span></span>

## <a name="syntax"></a><span data-ttu-id="73985-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="73985-105">Syntax</span></span>


```
dp2add dst, src0, src1, src2.{x|y|z|w}
```



<span data-ttu-id="73985-106">Em que:</span><span class="sxs-lookup"><span data-stu-id="73985-106">Where:</span></span>

-   <span data-ttu-id="73985-107">o DST é um registro de destino.</span><span class="sxs-lookup"><span data-stu-id="73985-107">dst is a destination register.</span></span>
-   <span data-ttu-id="73985-108">src0, src1 e src2 são três registros de origem.</span><span class="sxs-lookup"><span data-stu-id="73985-108">src0, src1, and src2 are three source registers.</span></span>
-   <span data-ttu-id="73985-109">{x \| y \| z \| w} é o swizzle de replicação necessário em src2.</span><span class="sxs-lookup"><span data-stu-id="73985-109">{x\|y\|z\|w} is the required replicate swizzle on src2.</span></span>

## <a name="remarks"></a><span data-ttu-id="73985-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="73985-110">Remarks</span></span>



| <span data-ttu-id="73985-111">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="73985-111">Pixel shader versions</span></span> | <span data-ttu-id="73985-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="73985-112">1\_1</span></span> | <span data-ttu-id="73985-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="73985-113">1\_2</span></span> | <span data-ttu-id="73985-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="73985-114">1\_3</span></span> | <span data-ttu-id="73985-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="73985-115">1\_4</span></span> | <span data-ttu-id="73985-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="73985-116">2\_0</span></span> | <span data-ttu-id="73985-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="73985-117">2\_x</span></span> | <span data-ttu-id="73985-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="73985-118">2\_sw</span></span> | <span data-ttu-id="73985-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="73985-119">3\_0</span></span> | <span data-ttu-id="73985-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="73985-120">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="73985-121">dp2add</span><span class="sxs-lookup"><span data-stu-id="73985-121">dp2add</span></span>                |      |      |      |      | <span data-ttu-id="73985-122">x</span><span class="sxs-lookup"><span data-stu-id="73985-122">x</span></span>    | <span data-ttu-id="73985-123">x</span><span class="sxs-lookup"><span data-stu-id="73985-123">x</span></span>    | <span data-ttu-id="73985-124">x</span><span class="sxs-lookup"><span data-stu-id="73985-124">x</span></span>     | <span data-ttu-id="73985-125">x</span><span class="sxs-lookup"><span data-stu-id="73985-125">x</span></span>    | <span data-ttu-id="73985-126">x</span><span class="sxs-lookup"><span data-stu-id="73985-126">x</span></span>     |



 

<span data-ttu-id="73985-127">O valor escalar para Add é escolhido pelo swizzle replicate em src2.</span><span class="sxs-lookup"><span data-stu-id="73985-127">The scalar value for add is chosen by the replicate swizzle on src2.</span></span>

<span data-ttu-id="73985-128">O trecho de código a seguir mostra as operações executadas.</span><span class="sxs-lookup"><span data-stu-id="73985-128">The following code snippet shows the operations performed.</span></span>


```
dest = src0.r * src1.r + src0.g * src1.g + src2.replicate_swizzle
// The scalar result is replicated to the write mask components
```



## <a name="related-topics"></a><span data-ttu-id="73985-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="73985-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73985-130">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="73985-130">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




