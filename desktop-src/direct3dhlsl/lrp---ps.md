---
title: LRP-PS
description: Interpola linearmente entre o segundo e o terceiro registros de origem por uma proporção especificada no primeiro registro de origem. | LRP-PS
ms.assetid: b360f28e-cb2a-4403-a020-180524df6549
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: aec1ac23cc6c86f768d435e4c8169117c1bbe899
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104012056"
---
# <a name="lrp---ps"></a><span data-ttu-id="7cb51-104">LRP-PS</span><span class="sxs-lookup"><span data-stu-id="7cb51-104">lrp - ps</span></span>

<span data-ttu-id="7cb51-105">Interpola linearmente entre o segundo e o terceiro registros de origem por uma proporção especificada no primeiro registro de origem.</span><span class="sxs-lookup"><span data-stu-id="7cb51-105">Interpolates linearly between the second and third source registers by a proportion specified in the first source register.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cb51-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="7cb51-106">Syntax</span></span>



| <span data-ttu-id="7cb51-107">LRP DST, src0, src1, src2</span><span class="sxs-lookup"><span data-stu-id="7cb51-107">lrp dst, src0, src1, src2</span></span> |
|---------------------------|



 

<span data-ttu-id="7cb51-108">onde</span><span class="sxs-lookup"><span data-stu-id="7cb51-108">where</span></span>

-   <span data-ttu-id="7cb51-109">DST é o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="7cb51-109">dst is the destination register.</span></span>
-   <span data-ttu-id="7cb51-110">src0 é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="7cb51-110">src0 is a source register.</span></span>
-   <span data-ttu-id="7cb51-111">src1 é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="7cb51-111">src1 is a source register.</span></span>
-   <span data-ttu-id="7cb51-112">src2 é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="7cb51-112">src2 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="7cb51-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="7cb51-113">Remarks</span></span>



| <span data-ttu-id="7cb51-114">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="7cb51-114">Pixel shader versions</span></span> | <span data-ttu-id="7cb51-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="7cb51-115">1\_1</span></span> | <span data-ttu-id="7cb51-116">1\_2</span><span class="sxs-lookup"><span data-stu-id="7cb51-116">1\_2</span></span> | <span data-ttu-id="7cb51-117">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="7cb51-117">1\_3</span></span> | <span data-ttu-id="7cb51-118">1\_4</span><span class="sxs-lookup"><span data-stu-id="7cb51-118">1\_4</span></span> | <span data-ttu-id="7cb51-119">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7cb51-119">2\_0</span></span> | <span data-ttu-id="7cb51-120">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="7cb51-120">2\_x</span></span> | <span data-ttu-id="7cb51-121">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="7cb51-121">2\_sw</span></span> | <span data-ttu-id="7cb51-122">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7cb51-122">3\_0</span></span> | <span data-ttu-id="7cb51-123">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="7cb51-123">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="7cb51-124">lrp</span><span class="sxs-lookup"><span data-stu-id="7cb51-124">lrp</span></span>                   | <span data-ttu-id="7cb51-125">x</span><span class="sxs-lookup"><span data-stu-id="7cb51-125">x</span></span>    | <span data-ttu-id="7cb51-126">x</span><span class="sxs-lookup"><span data-stu-id="7cb51-126">x</span></span>    | <span data-ttu-id="7cb51-127">x</span><span class="sxs-lookup"><span data-stu-id="7cb51-127">x</span></span>    | <span data-ttu-id="7cb51-128">x</span><span class="sxs-lookup"><span data-stu-id="7cb51-128">x</span></span>    | <span data-ttu-id="7cb51-129">x</span><span class="sxs-lookup"><span data-stu-id="7cb51-129">x</span></span>    | <span data-ttu-id="7cb51-130">x</span><span class="sxs-lookup"><span data-stu-id="7cb51-130">x</span></span>    | <span data-ttu-id="7cb51-131">x</span><span class="sxs-lookup"><span data-stu-id="7cb51-131">x</span></span>     | <span data-ttu-id="7cb51-132">x</span><span class="sxs-lookup"><span data-stu-id="7cb51-132">x</span></span>    | <span data-ttu-id="7cb51-133">x</span><span class="sxs-lookup"><span data-stu-id="7cb51-133">x</span></span>     |



 

<span data-ttu-id="7cb51-134">Essa instrução executa a interpolação linear com base na fórmula a seguir.</span><span class="sxs-lookup"><span data-stu-id="7cb51-134">This instruction performs the linear interpolation based on the following formula.</span></span>


```
 
dest = src0 * src1 + (1-src0) * src2
// which is the same as
dest = src2 + src0 * (src1 - src2)
```



## <a name="related-topics"></a><span data-ttu-id="7cb51-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7cb51-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7cb51-136">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="7cb51-136">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




