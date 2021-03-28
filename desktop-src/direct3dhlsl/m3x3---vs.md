---
title: m3x3-vs
description: Multiplica um vetor de 3 componentes por uma matriz de 3x3. | m3x3-vs
ms.assetid: 6a749ed0-097d-4354-bc70-fbcd879eafab
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e75cdb4b098b92ea358c32e40b3948c7ac73e0cf
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104370891"
---
# <a name="m3x3---vs"></a><span data-ttu-id="25ab0-104">m3x3-vs</span><span class="sxs-lookup"><span data-stu-id="25ab0-104">m3x3 - vs</span></span>

<span data-ttu-id="25ab0-105">Multiplica um vetor de 3 componentes por uma matriz de 3x3.</span><span class="sxs-lookup"><span data-stu-id="25ab0-105">Multiplies a 3-component vector by a 3x3 matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="25ab0-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="25ab0-106">Syntax</span></span>



| <span data-ttu-id="25ab0-107">m3x3 DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="25ab0-107">m3x3 dst, src0, src1</span></span> |
|----------------------|



 

<span data-ttu-id="25ab0-108">onde</span><span class="sxs-lookup"><span data-stu-id="25ab0-108">where</span></span>

-   <span data-ttu-id="25ab0-109">DST é o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="25ab0-109">dst is the destination register.</span></span> <span data-ttu-id="25ab0-110">O resultado é um vetor de 3 componentes.</span><span class="sxs-lookup"><span data-stu-id="25ab0-110">Result is a 3-component vector.</span></span>
-   <span data-ttu-id="25ab0-111">src0 é um registro de origem que representa um vetor de 3 componentes.</span><span class="sxs-lookup"><span data-stu-id="25ab0-111">src0 is a source register representing a 3-component vector.</span></span>
-   <span data-ttu-id="25ab0-112">src1 é um registro de origem que representa uma matriz 3x3, que corresponde ao primeiro de três registros consecutivos.</span><span class="sxs-lookup"><span data-stu-id="25ab0-112">src1 is a source register representing a 3x3 matrix, which corresponds to the first of 3 consecutive registers.</span></span>

## <a name="remarks"></a><span data-ttu-id="25ab0-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="25ab0-113">Remarks</span></span>



| <span data-ttu-id="25ab0-114">Versões do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="25ab0-114">Vertex shader versions</span></span> | <span data-ttu-id="25ab0-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="25ab0-115">1\_1</span></span> | <span data-ttu-id="25ab0-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="25ab0-116">2\_0</span></span> | <span data-ttu-id="25ab0-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="25ab0-117">2\_x</span></span> | <span data-ttu-id="25ab0-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="25ab0-118">2\_sw</span></span> | <span data-ttu-id="25ab0-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="25ab0-119">3\_0</span></span> | <span data-ttu-id="25ab0-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="25ab0-120">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="25ab0-121">m3x3</span><span class="sxs-lookup"><span data-stu-id="25ab0-121">m3x3</span></span>                   | <span data-ttu-id="25ab0-122">x</span><span class="sxs-lookup"><span data-stu-id="25ab0-122">x</span></span>    | <span data-ttu-id="25ab0-123">x</span><span class="sxs-lookup"><span data-stu-id="25ab0-123">x</span></span>    | <span data-ttu-id="25ab0-124">x</span><span class="sxs-lookup"><span data-stu-id="25ab0-124">x</span></span>    | <span data-ttu-id="25ab0-125">x</span><span class="sxs-lookup"><span data-stu-id="25ab0-125">x</span></span>     | <span data-ttu-id="25ab0-126">x</span><span class="sxs-lookup"><span data-stu-id="25ab0-126">x</span></span>    | <span data-ttu-id="25ab0-127">x</span><span class="sxs-lookup"><span data-stu-id="25ab0-127">x</span></span>     |



 

<span data-ttu-id="25ab0-128">A máscara XYZ é necessária para o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="25ab0-128">The xyz mask is required for the destination register.</span></span> <span data-ttu-id="25ab0-129">Os modificadores de negação e swizzle são permitidos para src0, mas não para src1.</span><span class="sxs-lookup"><span data-stu-id="25ab0-129">Negate and swizzle modifiers are allowed for src0 but not for src1.</span></span>

<span data-ttu-id="25ab0-130">O fragmento de código a seguir mostra as operações executadas.</span><span class="sxs-lookup"><span data-stu-id="25ab0-130">The following code fragment shows the operations performed.</span></span>


```
dest.x = (src0.x * src1.x) + (src0.y * src1.y) + (src0.z * src1.z);
dest.y = (src0.x * src2.x) + (src0.y * src2.y) + (src0.z * src2.z);
dest.z = (src0.x * src3.x) + (src0.y * src3.y) + (src0.z * src3.z);
```



<span data-ttu-id="25ab0-131">O vetor de entrada está no registro src0.</span><span class="sxs-lookup"><span data-stu-id="25ab0-131">The input vector is in register src0.</span></span> <span data-ttu-id="25ab0-132">A matriz de 3x3 de entrada está no registro src1 e nos próximos dois registros mais altos, conforme mostrado na expansão abaixo.</span><span class="sxs-lookup"><span data-stu-id="25ab0-132">The input 3x3 matrix is in register src1, and the next two higher registers, as shown in the expansion below.</span></span> <span data-ttu-id="25ab0-133">Um resultado 3D é produzido, deixando o outro elemento do registro de destino (dest. w) não afetado.</span><span class="sxs-lookup"><span data-stu-id="25ab0-133">A 3D result is produced, leaving the other element of the destination register (dest.w) unaffected.</span></span>

<span data-ttu-id="25ab0-134">Essa operação é normalmente usada para transformar vetores normais durante cálculos de iluminação.</span><span class="sxs-lookup"><span data-stu-id="25ab0-134">This operation is commonly used for transforming normal vectors during lighting computations.</span></span> <span data-ttu-id="25ab0-135">Essa instrução é implementada como um par de produtos de ponto, conforme mostrado abaixo.</span><span class="sxs-lookup"><span data-stu-id="25ab0-135">This instruction is implemented as a pair of dot products as shown below.</span></span>


```
m3x3 r0.xyz, r1, c0  which will be expanded to:

dp3   r0.x, r1, c0
dp3   r0.y, r1, c1
dp3   r0.z, r1, c2
```



## <a name="related-topics"></a><span data-ttu-id="25ab0-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="25ab0-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="25ab0-137">Instruções do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="25ab0-137">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




