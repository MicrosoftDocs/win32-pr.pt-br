---
title: m4x4-PS
description: Multiplica um vetor de 4 componentes por uma matriz 4x4. | m4x4-PS
ms.assetid: 2a9915a3-f396-4108-97f7-d70c5262ff59
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 93f2da73c45151f5287f3acf773efb4bd57d21e1
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968394"
---
# <a name="m4x4---ps"></a><span data-ttu-id="38dd9-104">m4x4-PS</span><span class="sxs-lookup"><span data-stu-id="38dd9-104">m4x4 - ps</span></span>

<span data-ttu-id="38dd9-105">Multiplica um vetor de 4 componentes por uma matriz 4x4.</span><span class="sxs-lookup"><span data-stu-id="38dd9-105">Multiplies a 4-component vector by a 4x4 matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="38dd9-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="38dd9-106">Syntax</span></span>



| <span data-ttu-id="38dd9-107">m4x4 DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="38dd9-107">m4x4 dst, src0, src1</span></span> |
|----------------------|



 

<span data-ttu-id="38dd9-108">onde</span><span class="sxs-lookup"><span data-stu-id="38dd9-108">where</span></span>

-   <span data-ttu-id="38dd9-109">DST é o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="38dd9-109">dst is the destination register.</span></span> <span data-ttu-id="38dd9-110">O resultado é um vetor de 4 componentes.</span><span class="sxs-lookup"><span data-stu-id="38dd9-110">Result is a 4-component vector.</span></span>
-   <span data-ttu-id="38dd9-111">src0 é um registro de origem que representa um vetor de 4 componentes.</span><span class="sxs-lookup"><span data-stu-id="38dd9-111">src0 is a source register representing a 4-component vector.</span></span>
-   <span data-ttu-id="38dd9-112">src1 é um registro de origem que representa uma matriz 4x4, que corresponde ao primeiro de quatro registradores consecutivos.</span><span class="sxs-lookup"><span data-stu-id="38dd9-112">src1 is a source register representing a 4x4 matrix, which corresponds to the first of 4 consecutive registers.</span></span>

## <a name="remarks"></a><span data-ttu-id="38dd9-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="38dd9-113">Remarks</span></span>



| <span data-ttu-id="38dd9-114">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="38dd9-114">Pixel shader versions</span></span> | <span data-ttu-id="38dd9-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="38dd9-115">1\_1</span></span> | <span data-ttu-id="38dd9-116">1\_2</span><span class="sxs-lookup"><span data-stu-id="38dd9-116">1\_2</span></span> | <span data-ttu-id="38dd9-117">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="38dd9-117">1\_3</span></span> | <span data-ttu-id="38dd9-118">1\_4</span><span class="sxs-lookup"><span data-stu-id="38dd9-118">1\_4</span></span> | <span data-ttu-id="38dd9-119">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="38dd9-119">2\_0</span></span> | <span data-ttu-id="38dd9-120">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="38dd9-120">2\_x</span></span> | <span data-ttu-id="38dd9-121">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="38dd9-121">2\_sw</span></span> | <span data-ttu-id="38dd9-122">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="38dd9-122">3\_0</span></span> | <span data-ttu-id="38dd9-123">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="38dd9-123">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="38dd9-124">m4x4</span><span class="sxs-lookup"><span data-stu-id="38dd9-124">m4x4</span></span>                  |      |      |      |      | <span data-ttu-id="38dd9-125">x</span><span class="sxs-lookup"><span data-stu-id="38dd9-125">x</span></span>    | <span data-ttu-id="38dd9-126">x</span><span class="sxs-lookup"><span data-stu-id="38dd9-126">x</span></span>    | <span data-ttu-id="38dd9-127">x</span><span class="sxs-lookup"><span data-stu-id="38dd9-127">x</span></span>     | <span data-ttu-id="38dd9-128">x</span><span class="sxs-lookup"><span data-stu-id="38dd9-128">x</span></span>    | <span data-ttu-id="38dd9-129">x</span><span class="sxs-lookup"><span data-stu-id="38dd9-129">x</span></span>     |



 

<span data-ttu-id="38dd9-130">A máscara xyzw (padrão) é necessária para o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="38dd9-130">The xyzw (default) mask is required for the destination register.</span></span> <span data-ttu-id="38dd9-131">Os modificadores de negação e swizzle são permitidos para src0, mas não para src1.</span><span class="sxs-lookup"><span data-stu-id="38dd9-131">Negate and swizzle modifiers are allowed for src0, but not for src1.</span></span>

<span data-ttu-id="38dd9-132">Os modificadores swizzle e negação são inválidos para o registro src0.</span><span class="sxs-lookup"><span data-stu-id="38dd9-132">Swizzle and negate modifiers are invalid for the src0 register.</span></span> <span data-ttu-id="38dd9-133">Os registros de horário de verão e src0 não podem ser iguais.</span><span class="sxs-lookup"><span data-stu-id="38dd9-133">The dst and src0 registers cannot be the same.</span></span>

<span data-ttu-id="38dd9-134">O trecho de código a seguir mostra as operações executadas.</span><span class="sxs-lookup"><span data-stu-id="38dd9-134">The following code snippet shows the operations performed.</span></span>


```
dest.x = (src0.x*src1.x) + (src0.y*src1.y) + (src0.z*src1.z) + (src0.w*src1.w);
dest.y = (src0.x*src2.x) + (src0.y*src2.y) + (src0.z*src2.z) + (src0.w*src2.w);
dest.z = (src0.x*src3.x) + (src0.y*src3.y) + (src0.z*src3.z) + (src0.w*src3.w);
dest.w = (src0.x*src4.x) + (src0.y*src4.y) + (src0.z*src4.z) + (src0.w*src4.w);
```



<span data-ttu-id="38dd9-135">O vetor de entrada está no registro src0.</span><span class="sxs-lookup"><span data-stu-id="38dd9-135">The input vector is in register src0.</span></span> <span data-ttu-id="38dd9-136">A matriz 4x4 de entrada está no registro src1 e nos próximos três registros mais altos, conforme mostrado na expansão abaixo.</span><span class="sxs-lookup"><span data-stu-id="38dd9-136">The input 4x4 matrix is in register src1, and the next three higher registers, as shown in the expansion below.</span></span>

<span data-ttu-id="38dd9-137">Essa operação é normalmente usada para transformar uma posição por uma matriz de projeção.</span><span class="sxs-lookup"><span data-stu-id="38dd9-137">This operation is commonly used for transforming a position by a projection matrix.</span></span> <span data-ttu-id="38dd9-138">Essa instrução é implementada como um conjunto de produtos dot, conforme mostrado aqui.</span><span class="sxs-lookup"><span data-stu-id="38dd9-138">This instruction is implemented as a set of dot products as shown here.</span></span>


```
m4x4   r0.xyzw, r1, c0    will be expanded to:

dp4   r0.x, r1, c0
dp4   r0.y, r1, c1
dp4   r0.z, r1, c2
dp4   r0.w, r1, c3
```



## <a name="related-topics"></a><span data-ttu-id="38dd9-139">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="38dd9-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38dd9-140">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="38dd9-140">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




