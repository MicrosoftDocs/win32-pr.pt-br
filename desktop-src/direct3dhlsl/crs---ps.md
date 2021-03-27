---
title: CRS-PS
description: Computa um produto cruzado usando a regra do lado direito. | CRS-PS
ms.assetid: 602fa7cc-4e2b-4d90-90d8-df00d5812c81
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b6098c8bf01bf0d8cce886276c1d1081720ea667
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104298162"
---
# <a name="crs---ps"></a><span data-ttu-id="8799d-104">CRS-PS</span><span class="sxs-lookup"><span data-stu-id="8799d-104">crs - ps</span></span>

<span data-ttu-id="8799d-105">Computa um produto cruzado usando a regra do lado direito.</span><span class="sxs-lookup"><span data-stu-id="8799d-105">Computes a cross product using the right-hand rule.</span></span>

## <a name="syntax"></a><span data-ttu-id="8799d-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="8799d-106">Syntax</span></span>



| <span data-ttu-id="8799d-107">CRS DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="8799d-107">crs dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="8799d-108">onde</span><span class="sxs-lookup"><span data-stu-id="8799d-108">where</span></span>

-   <span data-ttu-id="8799d-109">DST é o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="8799d-109">dst is the destination register.</span></span>
-   <span data-ttu-id="8799d-110">src0 é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="8799d-110">src0 is a source register.</span></span>
-   <span data-ttu-id="8799d-111">src1 é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="8799d-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="8799d-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="8799d-112">Remarks</span></span>



| <span data-ttu-id="8799d-113">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="8799d-113">Pixel shader versions</span></span> | <span data-ttu-id="8799d-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="8799d-114">1\_1</span></span> | <span data-ttu-id="8799d-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="8799d-115">1\_2</span></span> | <span data-ttu-id="8799d-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="8799d-116">1\_3</span></span> | <span data-ttu-id="8799d-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="8799d-117">1\_4</span></span> | <span data-ttu-id="8799d-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="8799d-118">2\_0</span></span> | <span data-ttu-id="8799d-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="8799d-119">2\_x</span></span> | <span data-ttu-id="8799d-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="8799d-120">2\_sw</span></span> | <span data-ttu-id="8799d-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="8799d-121">3\_0</span></span> | <span data-ttu-id="8799d-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="8799d-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="8799d-123">CRS</span><span class="sxs-lookup"><span data-stu-id="8799d-123">crs</span></span>                   |      |      |      |      | <span data-ttu-id="8799d-124">x</span><span class="sxs-lookup"><span data-stu-id="8799d-124">x</span></span>    | <span data-ttu-id="8799d-125">x</span><span class="sxs-lookup"><span data-stu-id="8799d-125">x</span></span>    | <span data-ttu-id="8799d-126">x</span><span class="sxs-lookup"><span data-stu-id="8799d-126">x</span></span>     | <span data-ttu-id="8799d-127">x</span><span class="sxs-lookup"><span data-stu-id="8799d-127">x</span></span>    | <span data-ttu-id="8799d-128">x</span><span class="sxs-lookup"><span data-stu-id="8799d-128">x</span></span>     |



 

<span data-ttu-id="8799d-129">Essa instrução funciona como mostrado aqui.</span><span class="sxs-lookup"><span data-stu-id="8799d-129">This instruction works as shown here.</span></span>


```
dest.x = src0.y * src1.z - src0.z * src1.y;
dest.y = src0.z * src1.x - src0.x * src1.z;
dest.z = src0.x * src1.y - src0.y * src1.x;
```



<span data-ttu-id="8799d-130">Algumas restrições ao uso:</span><span class="sxs-lookup"><span data-stu-id="8799d-130">Some restrictions on use:</span></span>

-   <span data-ttu-id="8799d-131">src0 não pode ser o mesmo registro que dest.</span><span class="sxs-lookup"><span data-stu-id="8799d-131">src0 cannot be the same register as dest.</span></span>
-   <span data-ttu-id="8799d-132">src1 não pode ser o mesmo registro que dest.</span><span class="sxs-lookup"><span data-stu-id="8799d-132">src1 cannot be the same register as dest.</span></span>
-   <span data-ttu-id="8799d-133">src0 não pode ter nenhum swizzle diferente do swizzle padrão (. xyzw).</span><span class="sxs-lookup"><span data-stu-id="8799d-133">src0 cannot have any swizzle other than the default swizzle (.xyzw).</span></span>
-   <span data-ttu-id="8799d-134">src1 não pode ter nenhum swizzle diferente do swizzle padrão (. xyzw).</span><span class="sxs-lookup"><span data-stu-id="8799d-134">src1 cannot have any swizzle other than the default swizzle (.xyzw).</span></span>
-   <span data-ttu-id="8799d-135">o dest precisa ter exatamente uma das sete máscaras a seguir:. x \| . y \| . z \| . XY \| . XZ \| . YZ \| . xyz.</span><span class="sxs-lookup"><span data-stu-id="8799d-135">dest has to have exactly one of the following seven masks: .x \| .y \| .z \| .xy \| .xz \| .yz \| .xyz.</span></span>
-   <span data-ttu-id="8799d-136">o dest deve ser um registro temporário.</span><span class="sxs-lookup"><span data-stu-id="8799d-136">dest must be a temporary register.</span></span>
-   <span data-ttu-id="8799d-137">dest não deve ser o mesmo registro que src0 ou src1</span><span class="sxs-lookup"><span data-stu-id="8799d-137">dest must not be the same register as src0 or src1</span></span>

## <a name="related-topics"></a><span data-ttu-id="8799d-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8799d-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8799d-139">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="8799d-139">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




