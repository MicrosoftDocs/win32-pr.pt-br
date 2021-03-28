---
title: M3X2-vs
description: Multiplica um vetor de 3 componentes por uma matriz 3x2. | M3X2-vs
ms.assetid: 4ef3bd47-3e38-4d9d-a8f5-6ee9c08de69c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 870a8d4918870930faa536ead01dab2947d5faea
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104172681"
---
# <a name="m3x2---vs"></a><span data-ttu-id="7b29e-104">M3X2-vs</span><span class="sxs-lookup"><span data-stu-id="7b29e-104">m3x2 - vs</span></span>

<span data-ttu-id="7b29e-105">Multiplica um vetor de 3 componentes por uma matriz 3x2.</span><span class="sxs-lookup"><span data-stu-id="7b29e-105">Multiplies a 3-component vector by a 3x2 matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b29e-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="7b29e-106">Syntax</span></span>



| <span data-ttu-id="7b29e-107">M3X2 DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="7b29e-107">m3x2 dst, src0, src1</span></span> |
|----------------------|



 

<span data-ttu-id="7b29e-108">onde</span><span class="sxs-lookup"><span data-stu-id="7b29e-108">where</span></span>

-   <span data-ttu-id="7b29e-109">DST é o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="7b29e-109">dst is the destination register.</span></span> <span data-ttu-id="7b29e-110">O resultado é um vetor de 2 componentes.</span><span class="sxs-lookup"><span data-stu-id="7b29e-110">Result is a 2-component vector.</span></span>
-   <span data-ttu-id="7b29e-111">src0 é um registro de origem que representa um vetor de 3 componentes.</span><span class="sxs-lookup"><span data-stu-id="7b29e-111">src0 is a source register representing a 3-component vector.</span></span>
-   <span data-ttu-id="7b29e-112">src1 é um registro de origem que representa uma matriz 3x2, que corresponde ao primeiro de dois registros consecutivos.</span><span class="sxs-lookup"><span data-stu-id="7b29e-112">src1 is a source register representing a 3x2 matrix, which corresponds to the first of 2 consecutive registers.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b29e-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="7b29e-113">Remarks</span></span>



| <span data-ttu-id="7b29e-114">Versões do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="7b29e-114">Vertex shader versions</span></span> | <span data-ttu-id="7b29e-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="7b29e-115">1\_1</span></span> | <span data-ttu-id="7b29e-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7b29e-116">2\_0</span></span> | <span data-ttu-id="7b29e-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="7b29e-117">2\_x</span></span> | <span data-ttu-id="7b29e-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="7b29e-118">2\_sw</span></span> | <span data-ttu-id="7b29e-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7b29e-119">3\_0</span></span> | <span data-ttu-id="7b29e-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="7b29e-120">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="7b29e-121">m3x2</span><span class="sxs-lookup"><span data-stu-id="7b29e-121">m3x2</span></span>                   | <span data-ttu-id="7b29e-122">x</span><span class="sxs-lookup"><span data-stu-id="7b29e-122">x</span></span>    | <span data-ttu-id="7b29e-123">x</span><span class="sxs-lookup"><span data-stu-id="7b29e-123">x</span></span>    | <span data-ttu-id="7b29e-124">x</span><span class="sxs-lookup"><span data-stu-id="7b29e-124">x</span></span>    | <span data-ttu-id="7b29e-125">x</span><span class="sxs-lookup"><span data-stu-id="7b29e-125">x</span></span>     | <span data-ttu-id="7b29e-126">x</span><span class="sxs-lookup"><span data-stu-id="7b29e-126">x</span></span>    | <span data-ttu-id="7b29e-127">x</span><span class="sxs-lookup"><span data-stu-id="7b29e-127">x</span></span>     |



 

<span data-ttu-id="7b29e-128">A máscara XY é necessária para o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="7b29e-128">The xy mask is required for the destination register.</span></span> <span data-ttu-id="7b29e-129">Os modificadores de negação e swizzle são permitidos para src0, mas não para src1.</span><span class="sxs-lookup"><span data-stu-id="7b29e-129">Negate and swizzle modifiers are allowed for src0 but not for src1.</span></span>

<span data-ttu-id="7b29e-130">As equações a seguir mostram como a instrução Opera:</span><span class="sxs-lookup"><span data-stu-id="7b29e-130">The following equations show how the instruction operates:</span></span>


```
dest.x = (src0.x * src1.x) + (src0.x * src1.y) + (src0.x * src1.z);
dest.y = (src0.x * src2.x) + (src0.y * src2.y) + (src0.z * src2.z);
```



<span data-ttu-id="7b29e-131">O vetor de entrada está no registro src0.</span><span class="sxs-lookup"><span data-stu-id="7b29e-131">The input vector is in register src0.</span></span> <span data-ttu-id="7b29e-132">A matriz 3x2 de entrada está no registro src1 e no próximo registro mais alto no mesmo arquivo de registro, conforme mostrado na seguinte expansão.</span><span class="sxs-lookup"><span data-stu-id="7b29e-132">The input 3x2 matrix is in register src1 and the next higher register in the same register file, as shown in the following expansion.</span></span> <span data-ttu-id="7b29e-133">Um resultado 2D é produzido, deixando os outros elementos do registro de destino (dest. z e dest. w) não afetados.</span><span class="sxs-lookup"><span data-stu-id="7b29e-133">A 2D result is produced, leaving the other elements of the destination register (dest.z and dest.w) unaffected.</span></span>

<span data-ttu-id="7b29e-134">Essa operação é normalmente usada para transformações 2D.</span><span class="sxs-lookup"><span data-stu-id="7b29e-134">This operation is commonly used for 2D transforms.</span></span> <span data-ttu-id="7b29e-135">Essa instrução é implementada como um par de produtos de ponto, conforme mostrado aqui.</span><span class="sxs-lookup"><span data-stu-id="7b29e-135">This instruction is implemented as a pair of dot products as shown here.</span></span>


```
m3x2   r0.xy, r1, c0   which will be expanded to:

dp3   r0.x, r1, c0
dp3   r0.y, r1, c1
```



<span data-ttu-id="7b29e-136">Os modificadores swizzle e negação são inválidos para o registro src1.</span><span class="sxs-lookup"><span data-stu-id="7b29e-136">Swizzle and negate modifiers are invalid for the src1 register.</span></span> <span data-ttu-id="7b29e-137">O registro de dest e src0, ou qualquer um dos registros de src1 + i, não pode ser o mesmo.</span><span class="sxs-lookup"><span data-stu-id="7b29e-137">The dest and src0 register, or any of src1+i registers, cannot be the same.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7b29e-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7b29e-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b29e-139">Instruções do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="7b29e-139">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




