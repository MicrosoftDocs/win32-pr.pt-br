---
title: M3X2-PS
description: Multiplica um vetor de 3 componentes por uma matriz 3x2. | M3X2-PS
ms.assetid: a88e6228-a61a-408c-8d89-a5706dd146d5
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 26532c78fa829b9c2a41f715b814ee8a0f44c879
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968519"
---
# <a name="m3x2---ps"></a><span data-ttu-id="7d45d-104">M3X2-PS</span><span class="sxs-lookup"><span data-stu-id="7d45d-104">m3x2 - ps</span></span>

<span data-ttu-id="7d45d-105">Multiplica um vetor de 3 componentes por uma matriz 3x2.</span><span class="sxs-lookup"><span data-stu-id="7d45d-105">Multiplies a 3-component vector by a 3x2 matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d45d-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="7d45d-106">Syntax</span></span>



| <span data-ttu-id="7d45d-107">M3X2 DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="7d45d-107">m3x2 dst, src0, src1</span></span> |
|----------------------|



 

<span data-ttu-id="7d45d-108">onde</span><span class="sxs-lookup"><span data-stu-id="7d45d-108">where</span></span>

-   <span data-ttu-id="7d45d-109">DST é o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="7d45d-109">dst is the destination register.</span></span> <span data-ttu-id="7d45d-110">O resultado é um vetor de 2 componentes.</span><span class="sxs-lookup"><span data-stu-id="7d45d-110">Result is a 2-component vector.</span></span>
-   <span data-ttu-id="7d45d-111">src0 é um registro de origem que representa um vetor de 3 componentes.</span><span class="sxs-lookup"><span data-stu-id="7d45d-111">src0 is a source register representing a 3-component vector.</span></span>
-   <span data-ttu-id="7d45d-112">src1 é um registro de origem que representa uma matriz 3x2, que corresponde ao primeiro de dois registros consecutivos.</span><span class="sxs-lookup"><span data-stu-id="7d45d-112">src1 is a source register representing a 3x2 matrix, which corresponds to the first of 2 consecutive registers.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d45d-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="7d45d-113">Remarks</span></span>



| <span data-ttu-id="7d45d-114">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="7d45d-114">Pixel shader versions</span></span> | <span data-ttu-id="7d45d-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="7d45d-115">1\_1</span></span> | <span data-ttu-id="7d45d-116">1\_2</span><span class="sxs-lookup"><span data-stu-id="7d45d-116">1\_2</span></span> | <span data-ttu-id="7d45d-117">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="7d45d-117">1\_3</span></span> | <span data-ttu-id="7d45d-118">1\_4</span><span class="sxs-lookup"><span data-stu-id="7d45d-118">1\_4</span></span> | <span data-ttu-id="7d45d-119">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7d45d-119">2\_0</span></span> | <span data-ttu-id="7d45d-120">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="7d45d-120">2\_x</span></span> | <span data-ttu-id="7d45d-121">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="7d45d-121">2\_sw</span></span> | <span data-ttu-id="7d45d-122">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7d45d-122">3\_0</span></span> | <span data-ttu-id="7d45d-123">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="7d45d-123">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="7d45d-124">m3x2</span><span class="sxs-lookup"><span data-stu-id="7d45d-124">m3x2</span></span>                  |      |      |      |      | <span data-ttu-id="7d45d-125">x</span><span class="sxs-lookup"><span data-stu-id="7d45d-125">x</span></span>    | <span data-ttu-id="7d45d-126">x</span><span class="sxs-lookup"><span data-stu-id="7d45d-126">x</span></span>    | <span data-ttu-id="7d45d-127">x</span><span class="sxs-lookup"><span data-stu-id="7d45d-127">x</span></span>     | <span data-ttu-id="7d45d-128">x</span><span class="sxs-lookup"><span data-stu-id="7d45d-128">x</span></span>    | <span data-ttu-id="7d45d-129">x</span><span class="sxs-lookup"><span data-stu-id="7d45d-129">x</span></span>     |



 

<span data-ttu-id="7d45d-130">A máscara XY é necessária para o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="7d45d-130">The xy mask is required for the destination register.</span></span> <span data-ttu-id="7d45d-131">Os modificadores de negação e swizzle são permitidos para src0, mas não para src1.</span><span class="sxs-lookup"><span data-stu-id="7d45d-131">Negate and swizzle modifiers are allowed for src0 but not for src1.</span></span>

<span data-ttu-id="7d45d-132">As equações a seguir mostram como a instrução Opera:</span><span class="sxs-lookup"><span data-stu-id="7d45d-132">The following equations show how the instruction operates:</span></span>


```
dest.x = (src0.x*src1.x) + (src0.y*src1.y) + (src0.z*src1.z);
dest.y = (src0.x*src2.x) + (src0.y*src2.y) + (src0.z*src2.z);
```



<span data-ttu-id="7d45d-133">O vetor de entrada está no registro src0.</span><span class="sxs-lookup"><span data-stu-id="7d45d-133">The input vector is in register src0.</span></span> <span data-ttu-id="7d45d-134">A matriz 3x2 de entrada está no registro src1 e no próximo registro mais alto no mesmo arquivo de registro, conforme mostrado na seguinte expansão.</span><span class="sxs-lookup"><span data-stu-id="7d45d-134">The input 3x2 matrix is in register src1 and the next higher register in the same register file, as shown in the following expansion.</span></span> <span data-ttu-id="7d45d-135">Um resultado 2D é produzido, deixando os outros elementos do registro de destino (dest. z e dest. w) não afetados.</span><span class="sxs-lookup"><span data-stu-id="7d45d-135">A 2D result is produced, leaving the other elements of the destination register (dest.z and dest.w) unaffected.</span></span>

<span data-ttu-id="7d45d-136">Essa operação é normalmente usada para transformações 2D.</span><span class="sxs-lookup"><span data-stu-id="7d45d-136">This operation is commonly used for 2D transforms.</span></span> <span data-ttu-id="7d45d-137">Essa instrução é implementada como um par de produtos de ponto, conforme mostrado aqui.</span><span class="sxs-lookup"><span data-stu-id="7d45d-137">This instruction is implemented as a pair of dot products as shown here.</span></span>


```
m3x2   r0.xy, r1, c0   which will be expanded to:

dp3   r0.x, r1, c0
dp3   r0.y, r1, c1
```



<span data-ttu-id="7d45d-138">Os modificadores swizzle e negação são inválidos para o registro src1.</span><span class="sxs-lookup"><span data-stu-id="7d45d-138">Swizzle and negate modifiers are invalid for the src1 register.</span></span> <span data-ttu-id="7d45d-139">O registro de horário de verão e src0, ou qualquer um dos registros de src1 + i, não pode ser o mesmo.</span><span class="sxs-lookup"><span data-stu-id="7d45d-139">The dst and src0 register, or any of src1+i registers, cannot be the same.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7d45d-140">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7d45d-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7d45d-141">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="7d45d-141">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




