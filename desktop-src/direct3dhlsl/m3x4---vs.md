---
title: M3x4-vs
description: Multiplica um vetor de 3 componentes por uma matriz 3x4. | M3x4-vs
ms.assetid: 8bec1ac5-376b-4eae-ba82-b42a6c0e7c4e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a4018698dbe6ab986945a84c1fcf9ce0431bd0fc
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968339"
---
# <a name="m3x4---vs"></a><span data-ttu-id="d277d-104">M3x4-vs</span><span class="sxs-lookup"><span data-stu-id="d277d-104">m3x4 - vs</span></span>

<span data-ttu-id="d277d-105">Multiplica um vetor de 3 componentes por uma matriz 3x4.</span><span class="sxs-lookup"><span data-stu-id="d277d-105">Multiplies a 3-component vector by a 3x4 matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="d277d-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="d277d-106">Syntax</span></span>



| <span data-ttu-id="d277d-107">M3x4 DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="d277d-107">m3x4 dst, src0, src1</span></span> |
|----------------------|



 

<span data-ttu-id="d277d-108">onde</span><span class="sxs-lookup"><span data-stu-id="d277d-108">where</span></span>

-   <span data-ttu-id="d277d-109">DST é o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="d277d-109">dst is the destination register.</span></span> <span data-ttu-id="d277d-110">O resultado é um vetor de 4 componentes.</span><span class="sxs-lookup"><span data-stu-id="d277d-110">Result is a 4-component vector.</span></span>
-   <span data-ttu-id="d277d-111">src0 é um registro de origem que representa um vetor de 3 componentes.</span><span class="sxs-lookup"><span data-stu-id="d277d-111">src0 is a source register representing a 3-component vector.</span></span>
-   <span data-ttu-id="d277d-112">src1 é um registro de origem que representa uma matriz 3x4, que corresponde ao primeiro de quatro registradores consecutivos.</span><span class="sxs-lookup"><span data-stu-id="d277d-112">src1 is a source register representing a 3x4 matrix, which corresponds to the first of 4 consecutive registers.</span></span>

## <a name="remarks"></a><span data-ttu-id="d277d-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="d277d-113">Remarks</span></span>



| <span data-ttu-id="d277d-114">Versões do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="d277d-114">Vertex shader versions</span></span> | <span data-ttu-id="d277d-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="d277d-115">1\_1</span></span> | <span data-ttu-id="d277d-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d277d-116">2\_0</span></span> | <span data-ttu-id="d277d-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="d277d-117">2\_x</span></span> | <span data-ttu-id="d277d-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="d277d-118">2\_sw</span></span> | <span data-ttu-id="d277d-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d277d-119">3\_0</span></span> | <span data-ttu-id="d277d-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="d277d-120">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="d277d-121">m3x4</span><span class="sxs-lookup"><span data-stu-id="d277d-121">m3x4</span></span>                   | <span data-ttu-id="d277d-122">x</span><span class="sxs-lookup"><span data-stu-id="d277d-122">x</span></span>    | <span data-ttu-id="d277d-123">x</span><span class="sxs-lookup"><span data-stu-id="d277d-123">x</span></span>    | <span data-ttu-id="d277d-124">x</span><span class="sxs-lookup"><span data-stu-id="d277d-124">x</span></span>    | <span data-ttu-id="d277d-125">x</span><span class="sxs-lookup"><span data-stu-id="d277d-125">x</span></span>     | <span data-ttu-id="d277d-126">x</span><span class="sxs-lookup"><span data-stu-id="d277d-126">x</span></span>    | <span data-ttu-id="d277d-127">x</span><span class="sxs-lookup"><span data-stu-id="d277d-127">x</span></span>     |



 

<span data-ttu-id="d277d-128">A máscara xyzw (padrão) é necessária para o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="d277d-128">The xyzw (default) mask is required for the destination register.</span></span> <span data-ttu-id="d277d-129">Os modificadores de negação e swizzle são permitidos para src0, mas não para src1.</span><span class="sxs-lookup"><span data-stu-id="d277d-129">Negate and swizzle modifiers are allowed for src0 but not for src1.</span></span>

<span data-ttu-id="d277d-130">O fragmento de código a seguir mostra as operações executadas.</span><span class="sxs-lookup"><span data-stu-id="d277d-130">The following code fragment shows the operations performed.</span></span>


```
 
dest.x = (src0.x * src1.x) + (src0.y * src1.y) + (src0.z * src1.z);
dest.y = (src0.x * src2.x) + (src0.y * src2.y) + (src0.z * src2.z);
dest.z = (src0.x * src3.x) + (src0.y * src3.y) + (src0.z * src3.z);
dest.w = (src0.x * src4.x) + (src0.y * src4.y) + (src0.z * src4.z);
```



<span data-ttu-id="d277d-131">O vetor de entrada está no registro src0.</span><span class="sxs-lookup"><span data-stu-id="d277d-131">The input vector is in register src0.</span></span> <span data-ttu-id="d277d-132">A matriz 3x4 de entrada está no registro src1 e nos próximos três registros superiores, conforme mostrado na expansão abaixo.</span><span class="sxs-lookup"><span data-stu-id="d277d-132">The input 3x4 matrix is in register src1 and the next three higher registers, as shown in the expansion below.</span></span>

<span data-ttu-id="d277d-133">Essa operação é normalmente usada para transformar um vetor de posição por uma matriz que tem um efeito projetado, mas não aplica nenhuma tradução.</span><span class="sxs-lookup"><span data-stu-id="d277d-133">This operation is commonly used for transforming a position vector by a matrix that has a projective effect but applies no translation.</span></span> <span data-ttu-id="d277d-134">Essa instrução é implementada como um par de produtos de ponto, conforme mostrado aqui.</span><span class="sxs-lookup"><span data-stu-id="d277d-134">This instruction is implemented as a pair of dot products as shown here.</span></span>


```
m3x4   r0.xyzw, r1, c0   will be expanded to: 

dp3 r0.x, r1, c0
dp3 r0.y, r1, c1
dp3 r0.z, r1, c2
dp3 r0.w, r1, c3
```



## <a name="related-topics"></a><span data-ttu-id="d277d-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d277d-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d277d-136">Instruções do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="d277d-136">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




