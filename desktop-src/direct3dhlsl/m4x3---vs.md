---
title: m4x3-vs
description: Multiplica um vetor de 4 componentes por uma matriz 4x3. | m4x3-vs
ms.assetid: 12dd31bd-2078-44a1-912e-72c8f377bc4c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7608b1187cc90cf4914bdd42a197cc6044d53734
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968338"
---
# <a name="m4x3---vs"></a><span data-ttu-id="e34dd-104">m4x3-vs</span><span class="sxs-lookup"><span data-stu-id="e34dd-104">m4x3 - vs</span></span>

<span data-ttu-id="e34dd-105">Multiplica um vetor de 4 componentes por uma matriz 4x3.</span><span class="sxs-lookup"><span data-stu-id="e34dd-105">Multiplies a 4-component vector by a 4x3 matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="e34dd-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="e34dd-106">Syntax</span></span>



| <span data-ttu-id="e34dd-107">m4x3 DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="e34dd-107">m4x3 dst, src0, src1</span></span> |
|----------------------|



 

<span data-ttu-id="e34dd-108">onde</span><span class="sxs-lookup"><span data-stu-id="e34dd-108">where</span></span>

-   <span data-ttu-id="e34dd-109">DST é o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="e34dd-109">dst is the destination register.</span></span> <span data-ttu-id="e34dd-110">O resultado é um vetor de 3 componentes.</span><span class="sxs-lookup"><span data-stu-id="e34dd-110">Result is a 3-component vector.</span></span>
-   <span data-ttu-id="e34dd-111">src0 é um registro de origem que representa um vetor de 4 componentes.</span><span class="sxs-lookup"><span data-stu-id="e34dd-111">src0 is a source register representing a 4-component vector.</span></span>
-   <span data-ttu-id="e34dd-112">src1 é um registro de origem que representa uma matriz 4x3, que corresponde ao primeiro de três registros consecutivos.</span><span class="sxs-lookup"><span data-stu-id="e34dd-112">src1 is a source register representing a 4x3 matrix, which corresponds to the first of 3 consecutive registers.</span></span>

## <a name="remarks"></a><span data-ttu-id="e34dd-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="e34dd-113">Remarks</span></span>



| <span data-ttu-id="e34dd-114">Versões do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="e34dd-114">Vertex shader versions</span></span> | <span data-ttu-id="e34dd-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="e34dd-115">1\_1</span></span> | <span data-ttu-id="e34dd-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e34dd-116">2\_0</span></span> | <span data-ttu-id="e34dd-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="e34dd-117">2\_x</span></span> | <span data-ttu-id="e34dd-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="e34dd-118">2\_sw</span></span> | <span data-ttu-id="e34dd-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e34dd-119">3\_0</span></span> | <span data-ttu-id="e34dd-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="e34dd-120">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="e34dd-121">m4x3</span><span class="sxs-lookup"><span data-stu-id="e34dd-121">m4x3</span></span>                   | <span data-ttu-id="e34dd-122">x</span><span class="sxs-lookup"><span data-stu-id="e34dd-122">x</span></span>    | <span data-ttu-id="e34dd-123">x</span><span class="sxs-lookup"><span data-stu-id="e34dd-123">x</span></span>    | <span data-ttu-id="e34dd-124">x</span><span class="sxs-lookup"><span data-stu-id="e34dd-124">x</span></span>    | <span data-ttu-id="e34dd-125">x</span><span class="sxs-lookup"><span data-stu-id="e34dd-125">x</span></span>     | <span data-ttu-id="e34dd-126">x</span><span class="sxs-lookup"><span data-stu-id="e34dd-126">x</span></span>    | <span data-ttu-id="e34dd-127">x</span><span class="sxs-lookup"><span data-stu-id="e34dd-127">x</span></span>     |



 

<span data-ttu-id="e34dd-128">A máscara XYZ é necessária para o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="e34dd-128">The xyz mask is required for the destination register.</span></span> <span data-ttu-id="e34dd-129">Os modificadores de negação e swizzle são permitidos para src0, mas não para src1.</span><span class="sxs-lookup"><span data-stu-id="e34dd-129">Negate and swizzle modifiers are allowed for src0, but not for src1.</span></span>

<span data-ttu-id="e34dd-130">O fragmento de código a seguir mostra as operações executadas.</span><span class="sxs-lookup"><span data-stu-id="e34dd-130">The following code fragment shows the operations performed.</span></span>


```
dest.x = (src0.x * src1.x) + (src0.y * src1.y) + (src0.z * src1.z) + (src0.w * src1.w);
dest.y = (src0.x * src2.x) + (src0.y * src2.y) + (src0.z * src2.z) + (src0.w * src2.w);
dest.z = (src0.x * src3.x) + (src0.y * src3.y) + (src0.z * src3.z) + (src0.w * src3.w);
```



<span data-ttu-id="e34dd-131">O vetor de entrada está no registro src0.</span><span class="sxs-lookup"><span data-stu-id="e34dd-131">The input vector is in register src0.</span></span> <span data-ttu-id="e34dd-132">A matriz 4x3 de entrada está no registro src1 e nos próximos dois registros mais altos, conforme mostrado na expansão abaixo.</span><span class="sxs-lookup"><span data-stu-id="e34dd-132">The input 4x3 matrix is in register src1, and the next two higher registers, as shown in the expansion below.</span></span> <span data-ttu-id="e34dd-133">Um resultado 3D é produzido, deixando o outro elemento do registro de destino (dest. w) não afetado.</span><span class="sxs-lookup"><span data-stu-id="e34dd-133">A 3D result is produced, leaving the other element of the destination register (dest.w) unaffected.</span></span>

<span data-ttu-id="e34dd-134">Essa operação é normalmente usada para transformar um vetor de posição por uma matriz que não tem efeito projetado, como ocorre em transformações de espaço de modelo.</span><span class="sxs-lookup"><span data-stu-id="e34dd-134">This operation is commonly used for transforming a position vector by a matrix that has no projective effect, such as occurs in model-space transformations.</span></span> <span data-ttu-id="e34dd-135">Essa instrução é implementada como um par de produtos de ponto, conforme mostrado abaixo.</span><span class="sxs-lookup"><span data-stu-id="e34dd-135">This instruction is implemented as a pair of dot products as shown below.</span></span>


```
m4x3   r0.xyz, r1, c0    will be expanded to:

dp4   r0.x, r1, c0
dp4   r0.y, r1, c1
dp4   r0.z, r1, c2
```



<span data-ttu-id="e34dd-136">Os modificadores swizzle e negação são inválidos para o registro src1.</span><span class="sxs-lookup"><span data-stu-id="e34dd-136">Swizzle and negate modifiers are invalid for the src1 register.</span></span> <span data-ttu-id="e34dd-137">O registro de hora de verão e src0 não pode ser o mesmo.</span><span class="sxs-lookup"><span data-stu-id="e34dd-137">The dst and src0 register cannot be the same.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e34dd-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e34dd-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e34dd-139">Instruções do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="e34dd-139">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




