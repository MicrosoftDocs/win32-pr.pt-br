---
title: FRC-vs
description: Retorna a parte fracionária de cada componente de entrada. | FRC-vs
ms.assetid: 6b6a4475-b665-4de0-9423-88ea8103e606
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6990d5489058d217888f34caf0305badc4cab46d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104298331"
---
# <a name="frc---vs"></a><span data-ttu-id="cce64-104">FRC-vs</span><span class="sxs-lookup"><span data-stu-id="cce64-104">frc - vs</span></span>

<span data-ttu-id="cce64-105">Retorna a parte fracionária de cada componente de entrada.</span><span class="sxs-lookup"><span data-stu-id="cce64-105">Returns the fractional portion of each input component.</span></span>

## <a name="syntax"></a><span data-ttu-id="cce64-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="cce64-106">Syntax</span></span>



| <span data-ttu-id="cce64-107">FRC DST, src</span><span class="sxs-lookup"><span data-stu-id="cce64-107">frc dst, src</span></span> |
|--------------|



 

<span data-ttu-id="cce64-108">onde</span><span class="sxs-lookup"><span data-stu-id="cce64-108">where</span></span>

-   <span data-ttu-id="cce64-109">DST é o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="cce64-109">dst is the destination register.</span></span>
-   <span data-ttu-id="cce64-110">src é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="cce64-110">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="cce64-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="cce64-111">Remarks</span></span>



| <span data-ttu-id="cce64-112">Versões do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="cce64-112">Vertex shader versions</span></span> | <span data-ttu-id="cce64-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="cce64-113">1\_1</span></span> | <span data-ttu-id="cce64-114">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="cce64-114">2\_0</span></span> | <span data-ttu-id="cce64-115">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="cce64-115">2\_x</span></span> | <span data-ttu-id="cce64-116">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="cce64-116">2\_sw</span></span> | <span data-ttu-id="cce64-117">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="cce64-117">3\_0</span></span> | <span data-ttu-id="cce64-118">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="cce64-118">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="cce64-119">frc</span><span class="sxs-lookup"><span data-stu-id="cce64-119">frc</span></span>                    | <span data-ttu-id="cce64-120">x</span><span class="sxs-lookup"><span data-stu-id="cce64-120">x</span></span>    | <span data-ttu-id="cce64-121">x</span><span class="sxs-lookup"><span data-stu-id="cce64-121">x</span></span>    | <span data-ttu-id="cce64-122">x</span><span class="sxs-lookup"><span data-stu-id="cce64-122">x</span></span>    | <span data-ttu-id="cce64-123">x</span><span class="sxs-lookup"><span data-stu-id="cce64-123">x</span></span>     | <span data-ttu-id="cce64-124">x</span><span class="sxs-lookup"><span data-stu-id="cce64-124">x</span></span>    | <span data-ttu-id="cce64-125">x</span><span class="sxs-lookup"><span data-stu-id="cce64-125">x</span></span>     |



 

<span data-ttu-id="cce64-126">O fragmento de código a seguir mostra conceitualmente como a instrução Opera.</span><span class="sxs-lookup"><span data-stu-id="cce64-126">The following code fragment shows conceptually how the instruction operates.</span></span>


```
dest.x = src.x - (float)floor(src.x);
dest.y = src.y - (float)floor(src.y);
dest.z = src.z - (float)floor(src.z);
dest.w = src.w - (float)floor(src.w);
```



<span data-ttu-id="cce64-127">A função Floor converte o argumento passado para o maior inteiro que é menor que (ou igual a) do argumento.</span><span class="sxs-lookup"><span data-stu-id="cce64-127">The floor function converts the argument passed in to the greatest integer that is less than (or equal to) the argument.</span></span> <span data-ttu-id="cce64-128">Isso é convertido em um float e, em seguida, subtraído do o valor original.</span><span class="sxs-lookup"><span data-stu-id="cce64-128">This is converted to a float and then subtracted fom the original value.</span></span> <span data-ttu-id="cce64-129">O valor fracionário resultante varia de 0,0 a 1,0.</span><span class="sxs-lookup"><span data-stu-id="cce64-129">The resulting fractional value ranges from 0.0 through 1.0.</span></span>

<span data-ttu-id="cce64-130">Para a versão 1 \_ 1, as máscaras de gravação permitidas são. s e. XY (. x não é permitido).</span><span class="sxs-lookup"><span data-stu-id="cce64-130">For version 1\_1, the allowable write masks are .y and .xy (.x is not allowed).</span></span>

## <a name="related-topics"></a><span data-ttu-id="cce64-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="cce64-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cce64-132">Instruções do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="cce64-132">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




