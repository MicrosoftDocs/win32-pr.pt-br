---
title: CRS-vs
description: Computa um produto cruzado usando a regra do lado direito. | CRS-vs
ms.assetid: 102108f5-acc8-49ce-a84b-b8060decbaa7
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fee30fab91b4f491efd4311919245ec2cb98b555
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104298161"
---
# <a name="crs---vs"></a><span data-ttu-id="5a9c1-104">CRS-vs</span><span class="sxs-lookup"><span data-stu-id="5a9c1-104">crs - vs</span></span>

<span data-ttu-id="5a9c1-105">Computa um produto cruzado usando a regra do lado direito.</span><span class="sxs-lookup"><span data-stu-id="5a9c1-105">Computes a cross product using the right-hand rule.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a9c1-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="5a9c1-106">Syntax</span></span>



| <span data-ttu-id="5a9c1-107">CRS DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="5a9c1-107">crs dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="5a9c1-108">onde</span><span class="sxs-lookup"><span data-stu-id="5a9c1-108">where</span></span>

-   <span data-ttu-id="5a9c1-109">DST é o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="5a9c1-109">dst is the destination register.</span></span>
-   <span data-ttu-id="5a9c1-110">src0 é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="5a9c1-110">src0 is a source register.</span></span>
-   <span data-ttu-id="5a9c1-111">src1 é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="5a9c1-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a9c1-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="5a9c1-112">Remarks</span></span>



| <span data-ttu-id="5a9c1-113">Versões do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="5a9c1-113">Vertex shader versions</span></span> | <span data-ttu-id="5a9c1-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="5a9c1-114">1\_1</span></span> | <span data-ttu-id="5a9c1-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5a9c1-115">2\_0</span></span> | <span data-ttu-id="5a9c1-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="5a9c1-116">2\_x</span></span> | <span data-ttu-id="5a9c1-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="5a9c1-117">2\_sw</span></span> | <span data-ttu-id="5a9c1-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5a9c1-118">3\_0</span></span> | <span data-ttu-id="5a9c1-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="5a9c1-119">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="5a9c1-120">CRS</span><span class="sxs-lookup"><span data-stu-id="5a9c1-120">crs</span></span>                    |      | <span data-ttu-id="5a9c1-121">x</span><span class="sxs-lookup"><span data-stu-id="5a9c1-121">x</span></span>    | <span data-ttu-id="5a9c1-122">x</span><span class="sxs-lookup"><span data-stu-id="5a9c1-122">x</span></span>    | <span data-ttu-id="5a9c1-123">x</span><span class="sxs-lookup"><span data-stu-id="5a9c1-123">x</span></span>     | <span data-ttu-id="5a9c1-124">x</span><span class="sxs-lookup"><span data-stu-id="5a9c1-124">x</span></span>    | <span data-ttu-id="5a9c1-125">x</span><span class="sxs-lookup"><span data-stu-id="5a9c1-125">x</span></span>     |



 

<span data-ttu-id="5a9c1-126">Essa instrução funciona como mostrado aqui.</span><span class="sxs-lookup"><span data-stu-id="5a9c1-126">This instruction works as shown here.</span></span>


```
dest.x = src0.y * src1.z - src0.z * src1.y;
dest.y = src0.z * src1.x - src0.x * src1.z;
dest.z = src0.x * src1.y - src0.y * src1.x;
```



<span data-ttu-id="5a9c1-127">Algumas restrições ao uso:</span><span class="sxs-lookup"><span data-stu-id="5a9c1-127">Some restrictions on use:</span></span>

-   <span data-ttu-id="5a9c1-128">src0 não pode ser o mesmo registro que dest.</span><span class="sxs-lookup"><span data-stu-id="5a9c1-128">src0 cannot be the same register as dest.</span></span>
-   <span data-ttu-id="5a9c1-129">src1 não pode ser o mesmo registro que dest.</span><span class="sxs-lookup"><span data-stu-id="5a9c1-129">src1 cannot be the same register as dest.</span></span>
-   <span data-ttu-id="5a9c1-130">src0 não pode ter nenhum swizzle diferente do swizzle padrão (. xyzw).</span><span class="sxs-lookup"><span data-stu-id="5a9c1-130">src0 cannot have any swizzle other than the default swizzle (.xyzw).</span></span>
-   <span data-ttu-id="5a9c1-131">src1 não pode ter nenhum swizzle diferente do swizzle padrão (. xyzw).</span><span class="sxs-lookup"><span data-stu-id="5a9c1-131">src1 cannot have any swizzle other than the default swizzle (.xyzw).</span></span>
-   <span data-ttu-id="5a9c1-132">o dest precisa ter exatamente uma das sete máscaras a seguir:. x \| . y \| . z \| . XY \| . XZ \| . YZ \| . xyz.</span><span class="sxs-lookup"><span data-stu-id="5a9c1-132">dest has to have exactly one of the following seven masks: .x \| .y \| .z \| .xy \| .xz \| .yz \| .xyz.</span></span>
-   <span data-ttu-id="5a9c1-133">o dest deve ser um registro temporário.</span><span class="sxs-lookup"><span data-stu-id="5a9c1-133">dest must be a temporary register.</span></span>
-   <span data-ttu-id="5a9c1-134">dest não deve ser o mesmo registro que src0 ou src1</span><span class="sxs-lookup"><span data-stu-id="5a9c1-134">dest must not be the same register as src0 or src1</span></span>

## <a name="related-topics"></a><span data-ttu-id="5a9c1-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5a9c1-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5a9c1-136">Instruções do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="5a9c1-136">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




