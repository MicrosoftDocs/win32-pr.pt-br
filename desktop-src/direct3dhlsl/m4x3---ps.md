---
title: m4x3-PS
description: Multiplica um vetor de 4 componentes por uma matriz 4x3. | m4x3-PS
ms.assetid: cf9ae4c3-6cdf-4c6f-b34c-0ebd3c8a4123
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7787268906c2c9e92dc1e3fa1ec87c4af3079255
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968496"
---
# <a name="m4x3---ps"></a><span data-ttu-id="9a376-104">m4x3-PS</span><span class="sxs-lookup"><span data-stu-id="9a376-104">m4x3 - ps</span></span>

<span data-ttu-id="9a376-105">Multiplica um vetor de 4 componentes por uma matriz 4x3.</span><span class="sxs-lookup"><span data-stu-id="9a376-105">Multiplies a 4-component vector by a 4x3 matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a376-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="9a376-106">Syntax</span></span>



| <span data-ttu-id="9a376-107">m4x3 DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="9a376-107">m4x3 dst, src0, src1</span></span> |
|----------------------|



 

<span data-ttu-id="9a376-108">onde</span><span class="sxs-lookup"><span data-stu-id="9a376-108">where</span></span>

-   <span data-ttu-id="9a376-109">DST é o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="9a376-109">dst is the destination register.</span></span> <span data-ttu-id="9a376-110">O resultado é um vetor de 3 componentes.</span><span class="sxs-lookup"><span data-stu-id="9a376-110">Result is a 3-component vector.</span></span>
-   <span data-ttu-id="9a376-111">src0 é um registro de origem que representa um vetor de 4 componentes.</span><span class="sxs-lookup"><span data-stu-id="9a376-111">src0 is a source register representing a 4-component vector.</span></span>
-   <span data-ttu-id="9a376-112">src1 é um registro de origem que representa uma matriz 4x3, que corresponde ao primeiro de três registros consecutivos.</span><span class="sxs-lookup"><span data-stu-id="9a376-112">src1 is a source register representing a 4x3 matrix, which corresponds to the first of 3 consecutive registers.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a376-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="9a376-113">Remarks</span></span>



| <span data-ttu-id="9a376-114">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="9a376-114">Pixel shader versions</span></span> | <span data-ttu-id="9a376-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="9a376-115">1\_1</span></span> | <span data-ttu-id="9a376-116">1\_2</span><span class="sxs-lookup"><span data-stu-id="9a376-116">1\_2</span></span> | <span data-ttu-id="9a376-117">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="9a376-117">1\_3</span></span> | <span data-ttu-id="9a376-118">1\_4</span><span class="sxs-lookup"><span data-stu-id="9a376-118">1\_4</span></span> | <span data-ttu-id="9a376-119">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9a376-119">2\_0</span></span> | <span data-ttu-id="9a376-120">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="9a376-120">2\_x</span></span> | <span data-ttu-id="9a376-121">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="9a376-121">2\_sw</span></span> | <span data-ttu-id="9a376-122">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9a376-122">3\_0</span></span> | <span data-ttu-id="9a376-123">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="9a376-123">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="9a376-124">m4x3</span><span class="sxs-lookup"><span data-stu-id="9a376-124">m4x3</span></span>                  |      |      |      |      | <span data-ttu-id="9a376-125">x</span><span class="sxs-lookup"><span data-stu-id="9a376-125">x</span></span>    | <span data-ttu-id="9a376-126">x</span><span class="sxs-lookup"><span data-stu-id="9a376-126">x</span></span>    | <span data-ttu-id="9a376-127">x</span><span class="sxs-lookup"><span data-stu-id="9a376-127">x</span></span>     | <span data-ttu-id="9a376-128">x</span><span class="sxs-lookup"><span data-stu-id="9a376-128">x</span></span>    | <span data-ttu-id="9a376-129">x</span><span class="sxs-lookup"><span data-stu-id="9a376-129">x</span></span>     |



 

<span data-ttu-id="9a376-130">A máscara XYZ é necessária para o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="9a376-130">The xyz mask is required for the destination register.</span></span> <span data-ttu-id="9a376-131">Os modificadores de negação e swizzle são permitidos para src0, mas não para src1.</span><span class="sxs-lookup"><span data-stu-id="9a376-131">Negate and swizzle modifiers are allowed for src0, but not for src1.</span></span>

<span data-ttu-id="9a376-132">O trecho de código a seguir mostra as operações executadas.</span><span class="sxs-lookup"><span data-stu-id="9a376-132">The following code snippet shows the operations performed.</span></span>


```
dest.x = (src0.x*src1.x) + (src0.y*src1.y) + (src0.z*src1.z) + (src0.w*src1.w);
dest.y = (src0.x*src2.x) + (src0.y*src2.y) + (src0.z*src2.z) + (src0.w*src2.w);
dest.z = (src0.x*src3.x) + (src0.y*src3.y) + (src0.z*src3.z) + (src0.w*src3.w);
```



<span data-ttu-id="9a376-133">O vetor de entrada está no registro src0.</span><span class="sxs-lookup"><span data-stu-id="9a376-133">The input vector is in register src0.</span></span> <span data-ttu-id="9a376-134">A matriz 4x3 de entrada está no registro src1 e nos próximos dois registros mais altos, conforme mostrado na expansão abaixo.</span><span class="sxs-lookup"><span data-stu-id="9a376-134">The input 4x3 matrix is in register src1, and the next two higher registers, as shown in the expansion below.</span></span> <span data-ttu-id="9a376-135">Um resultado 3D é produzido, deixando o outro elemento do registro de destino (dest. w) não afetado.</span><span class="sxs-lookup"><span data-stu-id="9a376-135">A 3D result is produced, leaving the other element of the destination register (dest.w) unaffected.</span></span>

<span data-ttu-id="9a376-136">Essa operação é normalmente usada para transformar um vetor de posição por uma matriz que não tem efeito projetado, como ocorre em transformações de espaço de modelo.</span><span class="sxs-lookup"><span data-stu-id="9a376-136">This operation is commonly used for transforming a position vector by a matrix that has no projective effect, such as occurs in model-space transformations.</span></span> <span data-ttu-id="9a376-137">Essa instrução é implementada como um conjunto de produtos dot, conforme mostrado abaixo.</span><span class="sxs-lookup"><span data-stu-id="9a376-137">This instruction is implemented as a set of dot products as shown below.</span></span>


```
m4x3   r0.xyz, r1, c0    will be expanded to:

dp4   r0.x, r1, c0
dp4   r0.y, r1, c1
dp4   r0.z, r1, c2
```



<span data-ttu-id="9a376-138">Os modificadores swizzle e negação são inválidos para o registro src1.</span><span class="sxs-lookup"><span data-stu-id="9a376-138">Swizzle and negate modifiers are invalid for the src1 register.</span></span> <span data-ttu-id="9a376-139">O registro de hora de verão e src0 não pode ser o mesmo.</span><span class="sxs-lookup"><span data-stu-id="9a376-139">The dst and src0 register cannot be the same.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9a376-140">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9a376-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9a376-141">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="9a376-141">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




