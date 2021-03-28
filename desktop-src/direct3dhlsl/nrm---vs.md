---
title: NRM-vs
description: Normalizar um vetor 3D. | NRM-vs
ms.assetid: 735e9971-c0c3-4648-8362-58bda6fac46a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0e696277136826294392149c4b7430e4c75f9d9a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104172744"
---
# <a name="nrm---vs"></a><span data-ttu-id="d439d-104">NRM-vs</span><span class="sxs-lookup"><span data-stu-id="d439d-104">nrm - vs</span></span>

<span data-ttu-id="d439d-105">Normalizar um vetor 3D.</span><span class="sxs-lookup"><span data-stu-id="d439d-105">Normalize a 3D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="d439d-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="d439d-106">Syntax</span></span>



| <span data-ttu-id="d439d-107">NRM DST, src</span><span class="sxs-lookup"><span data-stu-id="d439d-107">nrm dst, src</span></span> |
|--------------|



 

<span data-ttu-id="d439d-108">onde</span><span class="sxs-lookup"><span data-stu-id="d439d-108">where</span></span>

-   <span data-ttu-id="d439d-109">DST é o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="d439d-109">dst is the destination register.</span></span>
-   <span data-ttu-id="d439d-110">src é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="d439d-110">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="d439d-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="d439d-111">Remarks</span></span>



| <span data-ttu-id="d439d-112">Versões do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="d439d-112">Vertex shader versions</span></span> | <span data-ttu-id="d439d-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="d439d-113">1\_1</span></span> | <span data-ttu-id="d439d-114">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d439d-114">2\_0</span></span> | <span data-ttu-id="d439d-115">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="d439d-115">2\_x</span></span> | <span data-ttu-id="d439d-116">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="d439d-116">2\_sw</span></span> | <span data-ttu-id="d439d-117">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d439d-117">3\_0</span></span> | <span data-ttu-id="d439d-118">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="d439d-118">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="d439d-119">nrm</span><span class="sxs-lookup"><span data-stu-id="d439d-119">nrm</span></span>                    |      | <span data-ttu-id="d439d-120">x</span><span class="sxs-lookup"><span data-stu-id="d439d-120">x</span></span>    | <span data-ttu-id="d439d-121">x</span><span class="sxs-lookup"><span data-stu-id="d439d-121">x</span></span>    | <span data-ttu-id="d439d-122">x</span><span class="sxs-lookup"><span data-stu-id="d439d-122">x</span></span>     | <span data-ttu-id="d439d-123">x</span><span class="sxs-lookup"><span data-stu-id="d439d-123">x</span></span>    | <span data-ttu-id="d439d-124">x</span><span class="sxs-lookup"><span data-stu-id="d439d-124">x</span></span>     |



 

<span data-ttu-id="d439d-125">Essa instrução funciona conceitualmente, conforme mostrado aqui.</span><span class="sxs-lookup"><span data-stu-id="d439d-125">This instruction works conceptually as shown here.</span></span>

<span data-ttu-id="d439d-126">squareRootOfTheSum = (src0. x \* src0. x + src0. y \* src0. y + src0. z \* src0. z)<sup>1/2</sup>;</span><span class="sxs-lookup"><span data-stu-id="d439d-126">squareRootOfTheSum = (src0.x\*src0.x + src0.y\*src0.y + src0.z\*src0.z)<sup>1/2</sup>;</span></span>


```
dest.x = src0.x * (1 / squareRootOfTheSum);
dest.y = src0.y * (1 / squareRootOfTheSum);
dest.z = src0.z * (1 / squareRootOfTheSum);
dest.w = src0.w * (1 / squareRootOfTheSum);
```



<span data-ttu-id="d439d-127">Os registros de dest e src não podem ser iguais.</span><span class="sxs-lookup"><span data-stu-id="d439d-127">The dest and src registers cannot be the same.</span></span> <span data-ttu-id="d439d-128">O registro do dest deve ser um registro temporário.</span><span class="sxs-lookup"><span data-stu-id="d439d-128">The dest register must be a temporary register.</span></span>

<span data-ttu-id="d439d-129">Essa instrução executa a interpolação linear com base na fórmula a seguir.</span><span class="sxs-lookup"><span data-stu-id="d439d-129">This instruction performs the linear interpolation based on the following formula.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="d439d-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d439d-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d439d-131">Instruções do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="d439d-131">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




