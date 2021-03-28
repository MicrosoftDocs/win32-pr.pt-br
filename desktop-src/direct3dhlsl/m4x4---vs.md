---
title: m4x4-vs
description: Multiplica um vetor de 4 componentes por uma matriz 4x4. | m4x4-vs
ms.assetid: 016100ac-e316-41fd-a606-271be7394a1a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 846802f46cd829b3e610ec016a546c5302895bd9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104172678"
---
# <a name="m4x4---vs"></a><span data-ttu-id="3e604-104">m4x4-vs</span><span class="sxs-lookup"><span data-stu-id="3e604-104">m4x4 - vs</span></span>

<span data-ttu-id="3e604-105">Multiplica um vetor de 4 componentes por uma matriz 4x4.</span><span class="sxs-lookup"><span data-stu-id="3e604-105">Multiplies a 4-component vector by a 4x4 matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e604-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="3e604-106">Syntax</span></span>



| <span data-ttu-id="3e604-107">m4x4 DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="3e604-107">m4x4 dst, src0, src1</span></span> |
|----------------------|



 

<span data-ttu-id="3e604-108">onde</span><span class="sxs-lookup"><span data-stu-id="3e604-108">where</span></span>

-   <span data-ttu-id="3e604-109">DST é o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="3e604-109">dst is the destination register.</span></span> <span data-ttu-id="3e604-110">O resultado é um vetor de 4 componentes.</span><span class="sxs-lookup"><span data-stu-id="3e604-110">Result is a 4-component vector.</span></span>
-   <span data-ttu-id="3e604-111">src0 é um registro de origem que representa um vetor de 4 componentes.</span><span class="sxs-lookup"><span data-stu-id="3e604-111">src0 is a source register representing a 4-component vector.</span></span>
-   <span data-ttu-id="3e604-112">src1 é um registro de origem que representa uma matriz 4x4, que corresponde ao primeiro de quatro registradores consecutivos.</span><span class="sxs-lookup"><span data-stu-id="3e604-112">src1 is a source register representing a 4x4 matrix, which corresponds to the first of 4 consecutive registers.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e604-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="3e604-113">Remarks</span></span>



| <span data-ttu-id="3e604-114">Versões do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="3e604-114">Vertex shader versions</span></span> | <span data-ttu-id="3e604-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="3e604-115">1\_1</span></span> | <span data-ttu-id="3e604-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3e604-116">2\_0</span></span> | <span data-ttu-id="3e604-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="3e604-117">2\_x</span></span> | <span data-ttu-id="3e604-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="3e604-118">2\_sw</span></span> | <span data-ttu-id="3e604-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3e604-119">3\_0</span></span> | <span data-ttu-id="3e604-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="3e604-120">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="3e604-121">m4x4</span><span class="sxs-lookup"><span data-stu-id="3e604-121">m4x4</span></span>                   | <span data-ttu-id="3e604-122">x</span><span class="sxs-lookup"><span data-stu-id="3e604-122">x</span></span>    | <span data-ttu-id="3e604-123">x</span><span class="sxs-lookup"><span data-stu-id="3e604-123">x</span></span>    | <span data-ttu-id="3e604-124">x</span><span class="sxs-lookup"><span data-stu-id="3e604-124">x</span></span>    | <span data-ttu-id="3e604-125">x</span><span class="sxs-lookup"><span data-stu-id="3e604-125">x</span></span>     | <span data-ttu-id="3e604-126">x</span><span class="sxs-lookup"><span data-stu-id="3e604-126">x</span></span>    | <span data-ttu-id="3e604-127">x</span><span class="sxs-lookup"><span data-stu-id="3e604-127">x</span></span>     |



 

<span data-ttu-id="3e604-128">A máscara xyzw (padrão) é necessária para o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="3e604-128">The xyzw (default) mask is required for the destination register.</span></span> <span data-ttu-id="3e604-129">Os modificadores de negação e swizzle são permitidos para src0, mas não para src1.</span><span class="sxs-lookup"><span data-stu-id="3e604-129">Negate and swizzle modifiers are allowed for src0, but not for src1.</span></span>

<span data-ttu-id="3e604-130">Os modificadores swizzle e negação são inválidos para o registro src0.</span><span class="sxs-lookup"><span data-stu-id="3e604-130">Swizzle and negate modifiers are invalid for the src0 register.</span></span> <span data-ttu-id="3e604-131">Os registros dest e src0 não podem ser iguais.</span><span class="sxs-lookup"><span data-stu-id="3e604-131">The dest and src0 registers cannot be the same.</span></span>

<span data-ttu-id="3e604-132">O fragmento de código a seguir mostra as operações executadas.</span><span class="sxs-lookup"><span data-stu-id="3e604-132">The following code fragment shows the operations performed.</span></span>


```
dest.x = (src0.x * src1.x) + (src0.y * src1.y) + (src0.z * src1.z) + 
        (src0.w * src1.w);
dest.y = (src0.x * src2.x) + (src0.y * src2.y) + (src0.z * src2.z) + 
        (src0.w * src2.w);
dest.z = (src0.x * src3.x) + (src0.y * src3.y) + (src0.z * src3.z) + 
        (src0.w * src3.w);
dest.w = (src0.x * src4.x) + (src0.y * src4.y) + (src0.z * src4.z) + 
        (src0.w * src4.w);
```



<span data-ttu-id="3e604-133">O vetor de entrada está no registro src0.</span><span class="sxs-lookup"><span data-stu-id="3e604-133">The input vector is in register src0.</span></span> <span data-ttu-id="3e604-134">A matriz 4x4 de entrada está no registro src1 e nos próximos três registros mais altos, conforme mostrado na expansão abaixo.</span><span class="sxs-lookup"><span data-stu-id="3e604-134">The input 4x4 matrix is in register src1, and the next three higher registers, as shown in the expansion below.</span></span>

<span data-ttu-id="3e604-135">Essa operação é normalmente usada para transformar uma posição por uma matriz de projeção.</span><span class="sxs-lookup"><span data-stu-id="3e604-135">This operation is commonly used for transforming a position by a projection matrix.</span></span> <span data-ttu-id="3e604-136">Essa instrução é implementada como uma série de produtos dot, conforme mostrado aqui.</span><span class="sxs-lookup"><span data-stu-id="3e604-136">This instruction is implemented as a series of dot products as shown here.</span></span>


```
m4x4   r0.xyzw, r1, c0    will be expanded to:

dp4   r0.x, r1, c0
dp4   r0.y, r1, c1
dp4   r0.z, r1, c2
dp4   r0.w, r1, c3
```



## <a name="related-topics"></a><span data-ttu-id="3e604-137">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3e604-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e604-138">Instruções do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="3e604-138">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




