---
title: M3x4-PS
description: Multiplica um vetor de 3 componentes por uma matriz 3x4. | M3x4-PS
ms.assetid: b749d3cd-2acf-450c-94f2-fea5e1c8f4d2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4c245f4765853301a7c8319c8038b9ed342e3715
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968502"
---
# <a name="m3x4---ps"></a><span data-ttu-id="fc234-104">M3x4-PS</span><span class="sxs-lookup"><span data-stu-id="fc234-104">m3x4 - ps</span></span>

<span data-ttu-id="fc234-105">Multiplica um vetor de 3 componentes por uma matriz 3x4.</span><span class="sxs-lookup"><span data-stu-id="fc234-105">Multiplies a 3-component vector by a 3x4 matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc234-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="fc234-106">Syntax</span></span>



| <span data-ttu-id="fc234-107">M3x4 DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="fc234-107">m3x4 dst, src0, src1</span></span> |
|----------------------|



 

<span data-ttu-id="fc234-108">onde</span><span class="sxs-lookup"><span data-stu-id="fc234-108">where</span></span>

-   <span data-ttu-id="fc234-109">DST é o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="fc234-109">dst is the destination register.</span></span> <span data-ttu-id="fc234-110">O resultado é um vetor de 4 componentes.</span><span class="sxs-lookup"><span data-stu-id="fc234-110">Result is a 4-component vector.</span></span>
-   <span data-ttu-id="fc234-111">src0 é um registro de origem que representa um vetor de 3 componentes.</span><span class="sxs-lookup"><span data-stu-id="fc234-111">src0 is a source register representing a 3-component vector.</span></span>
-   <span data-ttu-id="fc234-112">src1 é um registro de origem que representa uma matriz 3x4, que corresponde ao primeiro de quatro registradores consecutivos.</span><span class="sxs-lookup"><span data-stu-id="fc234-112">src1 is a source register representing a 3x4 matrix, which corresponds to the first of 4 consecutive registers.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc234-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="fc234-113">Remarks</span></span>



| <span data-ttu-id="fc234-114">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="fc234-114">Pixel shader versions</span></span> | <span data-ttu-id="fc234-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="fc234-115">1\_1</span></span> | <span data-ttu-id="fc234-116">1\_2</span><span class="sxs-lookup"><span data-stu-id="fc234-116">1\_2</span></span> | <span data-ttu-id="fc234-117">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="fc234-117">1\_3</span></span> | <span data-ttu-id="fc234-118">1\_4</span><span class="sxs-lookup"><span data-stu-id="fc234-118">1\_4</span></span> | <span data-ttu-id="fc234-119">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="fc234-119">2\_0</span></span> | <span data-ttu-id="fc234-120">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="fc234-120">2\_x</span></span> | <span data-ttu-id="fc234-121">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="fc234-121">2\_sw</span></span> | <span data-ttu-id="fc234-122">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="fc234-122">3\_0</span></span> | <span data-ttu-id="fc234-123">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="fc234-123">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="fc234-124">m3x4</span><span class="sxs-lookup"><span data-stu-id="fc234-124">m3x4</span></span>                  |      |      |      |      | <span data-ttu-id="fc234-125">x</span><span class="sxs-lookup"><span data-stu-id="fc234-125">x</span></span>    | <span data-ttu-id="fc234-126">x</span><span class="sxs-lookup"><span data-stu-id="fc234-126">x</span></span>    | <span data-ttu-id="fc234-127">x</span><span class="sxs-lookup"><span data-stu-id="fc234-127">x</span></span>     | <span data-ttu-id="fc234-128">x</span><span class="sxs-lookup"><span data-stu-id="fc234-128">x</span></span>    | <span data-ttu-id="fc234-129">x</span><span class="sxs-lookup"><span data-stu-id="fc234-129">x</span></span>     |



 

<span data-ttu-id="fc234-130">A máscara xyzw (padrão) é necessária para o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="fc234-130">The xyzw (default) mask is required for the destination register.</span></span> <span data-ttu-id="fc234-131">Os modificadores de negação e swizzle são permitidos para src0, mas não para src1.</span><span class="sxs-lookup"><span data-stu-id="fc234-131">Negate and swizzle modifiers are allowed for src0 but not for src1.</span></span>

<span data-ttu-id="fc234-132">O trecho de código a seguir mostra as operações executadas.</span><span class="sxs-lookup"><span data-stu-id="fc234-132">The following code snippet shows the operations performed.</span></span>


```
 
dest.x = (src0.x*src1.x) + (src0.y*src1.y) + (src0.z*src1.z);
dest.y = (src0.x*src2.x) + (src0.y*src2.y) + (src0.z*src2.z);
dest.z = (src0.x*src3.x) + (src0.y*src3.y) + (src0.z*src3.z);
dest.w = (src0.x*src4.x) + (src0.y*src4.y) + (src0.z*src4.z);
```



<span data-ttu-id="fc234-133">O vetor de entrada está no registro src0.</span><span class="sxs-lookup"><span data-stu-id="fc234-133">The input vector is in register src0.</span></span> <span data-ttu-id="fc234-134">A matriz 3x4 de entrada está no registro src1 e nos próximos dois registros mais altos, conforme mostrado na expansão abaixo.</span><span class="sxs-lookup"><span data-stu-id="fc234-134">The input 3x4 matrix is in register src1, and the next two higher registers, as shown in the expansion below.</span></span>

<span data-ttu-id="fc234-135">Essa operação é normalmente usada para transformar um vetor de posição por uma matriz que tem um efeito projetado, mas não aplica nenhuma tradução.</span><span class="sxs-lookup"><span data-stu-id="fc234-135">This operation is commonly used for transforming a position vector by a matrix that has a projective effect but applies no translation.</span></span> <span data-ttu-id="fc234-136">Essa instrução é implementada como um par de produtos de ponto, conforme mostrado aqui.</span><span class="sxs-lookup"><span data-stu-id="fc234-136">This instruction is implemented as a pair of dot products as shown here.</span></span>


```
m3x4   r0.xyzw, r1, c0   will be expanded to: 

dp3 r0.x, r1, c0
dp3 r0.y, r1, c1
dp3 r0.z, r1, c2
dp3 r0.w, r1, c3
```



## <a name="related-topics"></a><span data-ttu-id="fc234-137">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fc234-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc234-138">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="fc234-138">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




