---
title: NRM-PS
description: Normalizar um vetor 3D. | NRM-PS
ms.assetid: 4881037d-3ad1-4afb-b4ad-d615c6b8fe34
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 165f1b8fa6adce4ffba079eff025ed1a3d8ce61e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104298221"
---
# <a name="nrm---ps"></a><span data-ttu-id="866a3-104">NRM-PS</span><span class="sxs-lookup"><span data-stu-id="866a3-104">nrm - ps</span></span>

<span data-ttu-id="866a3-105">Normalizar um vetor 3D.</span><span class="sxs-lookup"><span data-stu-id="866a3-105">Normalize a 3D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="866a3-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="866a3-106">Syntax</span></span>



| <span data-ttu-id="866a3-107">NRM DST, src</span><span class="sxs-lookup"><span data-stu-id="866a3-107">nrm dst, src</span></span> |
|--------------|



 

<span data-ttu-id="866a3-108">onde</span><span class="sxs-lookup"><span data-stu-id="866a3-108">where</span></span>

-   <span data-ttu-id="866a3-109">DST é o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="866a3-109">dst is the destination register.</span></span>
-   <span data-ttu-id="866a3-110">src é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="866a3-110">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="866a3-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="866a3-111">Remarks</span></span>



| <span data-ttu-id="866a3-112">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="866a3-112">Pixel shader versions</span></span> | <span data-ttu-id="866a3-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="866a3-113">1\_1</span></span> | <span data-ttu-id="866a3-114">1\_2</span><span class="sxs-lookup"><span data-stu-id="866a3-114">1\_2</span></span> | <span data-ttu-id="866a3-115">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="866a3-115">1\_3</span></span> | <span data-ttu-id="866a3-116">1\_4</span><span class="sxs-lookup"><span data-stu-id="866a3-116">1\_4</span></span> | <span data-ttu-id="866a3-117">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="866a3-117">2\_0</span></span> | <span data-ttu-id="866a3-118">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="866a3-118">2\_x</span></span> | <span data-ttu-id="866a3-119">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="866a3-119">2\_sw</span></span> | <span data-ttu-id="866a3-120">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="866a3-120">3\_0</span></span> | <span data-ttu-id="866a3-121">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="866a3-121">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="866a3-122">nrm</span><span class="sxs-lookup"><span data-stu-id="866a3-122">nrm</span></span>                   |      |      |      |      | <span data-ttu-id="866a3-123">x</span><span class="sxs-lookup"><span data-stu-id="866a3-123">x</span></span>    | <span data-ttu-id="866a3-124">x</span><span class="sxs-lookup"><span data-stu-id="866a3-124">x</span></span>    | <span data-ttu-id="866a3-125">x</span><span class="sxs-lookup"><span data-stu-id="866a3-125">x</span></span>     | <span data-ttu-id="866a3-126">x</span><span class="sxs-lookup"><span data-stu-id="866a3-126">x</span></span>    | <span data-ttu-id="866a3-127">x</span><span class="sxs-lookup"><span data-stu-id="866a3-127">x</span></span>     |



 

<span data-ttu-id="866a3-128">Essa instrução funciona conceitualmente, conforme mostrado aqui.</span><span class="sxs-lookup"><span data-stu-id="866a3-128">This instruction works conceptually as shown here.</span></span>

<span data-ttu-id="866a3-129">squareRootOfTheSum = (src0. x \* src0. x + src0. y \* src0. y + src0. z \* src0. z)<sup>1/2</sup>;</span><span class="sxs-lookup"><span data-stu-id="866a3-129">squareRootOfTheSum = (src0.x\*src0.x + src0.y\*src0.y + src0.z\*src0.z)<sup>1/2</sup>;</span></span>


```
dest.x = src0.x * (1 / squareRootOfTheSum);
dest.y = src0.y * (1 / squareRootOfTheSum);
dest.z = src0.z * (1 / squareRootOfTheSum);
dest.w = src0.w * (1 / squareRootOfTheSum);
```



<span data-ttu-id="866a3-130">Os registros de dest e src não podem ser iguais.</span><span class="sxs-lookup"><span data-stu-id="866a3-130">The dest and src registers cannot be the same.</span></span> <span data-ttu-id="866a3-131">O registro do dest deve ser um registro temporário.</span><span class="sxs-lookup"><span data-stu-id="866a3-131">The dest register must be a temporary register.</span></span>

<span data-ttu-id="866a3-132">Essa instrução executa a interpolação linear com base na fórmula a seguir.</span><span class="sxs-lookup"><span data-stu-id="866a3-132">This instruction performs the linear interpolation based on the following formula.</span></span>


```
float f = src0.x*src0.x + src0.y*src0.y + src0.z*src0.z;
if (f != 0)
    f = (float)(1/sqrt(f));
else
    f = FLT_MAX;

dest.x = src0.x*f;
dest.y = src0.y*f;
dest.z = src0.z*f;
dest.w = src0.w*f;
```



## <a name="related-topics"></a><span data-ttu-id="866a3-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="866a3-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="866a3-134">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="866a3-134">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




