---
title: m3x3-PS
description: Multiplica um vetor de 3 componentes por uma matriz de 3x3. | m3x3-PS
ms.assetid: 71342e05-69a6-41f4-bafb-643f0ceb0a59
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4ac72acd2133c8b34393bdd1ab7de8aec1df4db5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968490"
---
# <a name="m3x3---ps"></a><span data-ttu-id="6e86d-104">m3x3-PS</span><span class="sxs-lookup"><span data-stu-id="6e86d-104">m3x3 - ps</span></span>

<span data-ttu-id="6e86d-105">Multiplica um vetor de 3 componentes por uma matriz de 3x3.</span><span class="sxs-lookup"><span data-stu-id="6e86d-105">Multiplies a 3-component vector by a 3x3 matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e86d-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="6e86d-106">Syntax</span></span>



| <span data-ttu-id="6e86d-107">m3x3 DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="6e86d-107">m3x3 dst, src0, src1</span></span> |
|----------------------|



 

<span data-ttu-id="6e86d-108">onde</span><span class="sxs-lookup"><span data-stu-id="6e86d-108">where</span></span>

-   <span data-ttu-id="6e86d-109">DST é o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="6e86d-109">dst is the destination register.</span></span> <span data-ttu-id="6e86d-110">O resultado é um vetor de 3 componentes.</span><span class="sxs-lookup"><span data-stu-id="6e86d-110">Result is a 3-component vector.</span></span>
-   <span data-ttu-id="6e86d-111">src0 é um registro de origem que representa um vetor de 3 componentes.</span><span class="sxs-lookup"><span data-stu-id="6e86d-111">src0 is a source register representing a 3-component vector.</span></span>
-   <span data-ttu-id="6e86d-112">src1 é um registro de origem que representa uma matriz 3x3, que corresponde ao primeiro de três registros consecutivos.</span><span class="sxs-lookup"><span data-stu-id="6e86d-112">src1 is a source register representing a 3x3 matrix, which corresponds to the first of 3 consecutive registers.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e86d-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="6e86d-113">Remarks</span></span>



| <span data-ttu-id="6e86d-114">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="6e86d-114">Pixel shader versions</span></span> | <span data-ttu-id="6e86d-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="6e86d-115">1\_1</span></span> | <span data-ttu-id="6e86d-116">1\_2</span><span class="sxs-lookup"><span data-stu-id="6e86d-116">1\_2</span></span> | <span data-ttu-id="6e86d-117">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="6e86d-117">1\_3</span></span> | <span data-ttu-id="6e86d-118">1\_4</span><span class="sxs-lookup"><span data-stu-id="6e86d-118">1\_4</span></span> | <span data-ttu-id="6e86d-119">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="6e86d-119">2\_0</span></span> | <span data-ttu-id="6e86d-120">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="6e86d-120">2\_x</span></span> | <span data-ttu-id="6e86d-121">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="6e86d-121">2\_sw</span></span> | <span data-ttu-id="6e86d-122">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="6e86d-122">3\_0</span></span> | <span data-ttu-id="6e86d-123">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="6e86d-123">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="6e86d-124">m3x3</span><span class="sxs-lookup"><span data-stu-id="6e86d-124">m3x3</span></span>                  |      |      |      |      | <span data-ttu-id="6e86d-125">x</span><span class="sxs-lookup"><span data-stu-id="6e86d-125">x</span></span>    | <span data-ttu-id="6e86d-126">x</span><span class="sxs-lookup"><span data-stu-id="6e86d-126">x</span></span>    | <span data-ttu-id="6e86d-127">x</span><span class="sxs-lookup"><span data-stu-id="6e86d-127">x</span></span>     | <span data-ttu-id="6e86d-128">x</span><span class="sxs-lookup"><span data-stu-id="6e86d-128">x</span></span>    | <span data-ttu-id="6e86d-129">x</span><span class="sxs-lookup"><span data-stu-id="6e86d-129">x</span></span>     |



 

<span data-ttu-id="6e86d-130">A máscara XYZ é necessária para o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="6e86d-130">The xyz mask is required for the destination register.</span></span> <span data-ttu-id="6e86d-131">Os modificadores de negação e swizzle são permitidos para src0, mas não para src1.</span><span class="sxs-lookup"><span data-stu-id="6e86d-131">Negate and swizzle modifiers are allowed for src0 but not for src1.</span></span>

<span data-ttu-id="6e86d-132">O trecho de código a seguir mostra as operações executadas.</span><span class="sxs-lookup"><span data-stu-id="6e86d-132">The following code snippet shows the operations performed.</span></span>


```
dest.x = (src0.x * src1.x) + (src0.y * src1.y) + (src0.z * src1.z);
dest.y = (src0.x * src2.x) + (src0.y * src2.y) + (src0.z * src2.z);
dest.z = (src0.x * src3.x) + (src0.y * src3.y) + (src0.z * src3.z);
```



<span data-ttu-id="6e86d-133">O vetor de entrada está no registro src0.</span><span class="sxs-lookup"><span data-stu-id="6e86d-133">The input vector is in register src0.</span></span> <span data-ttu-id="6e86d-134">A matriz de 3x3 de entrada está no registro src1 e nos próximos dois registros mais altos, conforme mostrado na expansão abaixo.</span><span class="sxs-lookup"><span data-stu-id="6e86d-134">The input 3x3 matrix is in register src1, and the next two higher registers, as shown in the expansion below.</span></span> <span data-ttu-id="6e86d-135">Um resultado 3D é produzido, deixando o outro elemento do registro de destino (dest. w) não afetado.</span><span class="sxs-lookup"><span data-stu-id="6e86d-135">A 3D result is produced, leaving the other element of the destination register (dest.w) unaffected.</span></span>

<span data-ttu-id="6e86d-136">Essa operação é normalmente usada para transformar vetores normais durante cálculos de iluminação.</span><span class="sxs-lookup"><span data-stu-id="6e86d-136">This operation is commonly used for transforming normal vectors during lighting computations.</span></span> <span data-ttu-id="6e86d-137">Essa instrução é implementada como um conjunto de produtos dot, conforme mostrado abaixo.</span><span class="sxs-lookup"><span data-stu-id="6e86d-137">This instruction is implemented as a set of dot products as shown below.</span></span>


```
m3x3 r0.xyz, r1, c0  which will be expanded to:

dp3   r0.x, r1, c0
dp3   r0.y, r1, c1
dp3   r0.z, r1, c2
```



## <a name="related-topics"></a><span data-ttu-id="6e86d-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6e86d-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e86d-139">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="6e86d-139">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




