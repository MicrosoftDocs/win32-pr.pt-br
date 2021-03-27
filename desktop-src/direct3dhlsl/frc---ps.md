---
title: FRC-PS
description: Retorna a parte fracionária de cada componente de entrada. | FRC-PS
ms.assetid: 378bc516-c81e-4538-8d6f-987536b19467
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a16dd518333efa1dce878c1418547bc0527d1d64
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104298332"
---
# <a name="frc---ps"></a><span data-ttu-id="5ed91-104">FRC-PS</span><span class="sxs-lookup"><span data-stu-id="5ed91-104">frc - ps</span></span>

<span data-ttu-id="5ed91-105">Retorna a parte fracionária de cada componente de entrada.</span><span class="sxs-lookup"><span data-stu-id="5ed91-105">Returns the fractional portion of each input component.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ed91-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="5ed91-106">Syntax</span></span>



| <span data-ttu-id="5ed91-107">FRC DST, src</span><span class="sxs-lookup"><span data-stu-id="5ed91-107">frc dst, src</span></span> |
|--------------|



 

<span data-ttu-id="5ed91-108">onde</span><span class="sxs-lookup"><span data-stu-id="5ed91-108">where</span></span>

-   <span data-ttu-id="5ed91-109">DST é o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="5ed91-109">dst is the destination register.</span></span>
-   <span data-ttu-id="5ed91-110">src é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="5ed91-110">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ed91-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="5ed91-111">Remarks</span></span>



| <span data-ttu-id="5ed91-112">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="5ed91-112">Pixel shader versions</span></span> | <span data-ttu-id="5ed91-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="5ed91-113">1\_1</span></span> | <span data-ttu-id="5ed91-114">1\_2</span><span class="sxs-lookup"><span data-stu-id="5ed91-114">1\_2</span></span> | <span data-ttu-id="5ed91-115">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="5ed91-115">1\_3</span></span> | <span data-ttu-id="5ed91-116">1\_4</span><span class="sxs-lookup"><span data-stu-id="5ed91-116">1\_4</span></span> | <span data-ttu-id="5ed91-117">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5ed91-117">2\_0</span></span> | <span data-ttu-id="5ed91-118">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="5ed91-118">2\_x</span></span> | <span data-ttu-id="5ed91-119">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="5ed91-119">2\_sw</span></span> | <span data-ttu-id="5ed91-120">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5ed91-120">3\_0</span></span> | <span data-ttu-id="5ed91-121">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="5ed91-121">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="5ed91-122">frc</span><span class="sxs-lookup"><span data-stu-id="5ed91-122">frc</span></span>                   |      |      |      |      | <span data-ttu-id="5ed91-123">x</span><span class="sxs-lookup"><span data-stu-id="5ed91-123">x</span></span>    | <span data-ttu-id="5ed91-124">x</span><span class="sxs-lookup"><span data-stu-id="5ed91-124">x</span></span>    | <span data-ttu-id="5ed91-125">x</span><span class="sxs-lookup"><span data-stu-id="5ed91-125">x</span></span>     | <span data-ttu-id="5ed91-126">x</span><span class="sxs-lookup"><span data-stu-id="5ed91-126">x</span></span>    | <span data-ttu-id="5ed91-127">x</span><span class="sxs-lookup"><span data-stu-id="5ed91-127">x</span></span>     |



 

<span data-ttu-id="5ed91-128">O trecho de código a seguir mostra conceitualmente como a instrução Opera.</span><span class="sxs-lookup"><span data-stu-id="5ed91-128">The following code snippet shows conceptually how the instruction operates.</span></span>


```
dest.x = src.x - (float)floor(src.x);
dest.y = src.y - (float)floor(src.y);
dest.z = src.z - (float)floor(src.z);
dest.w = src.w - (float)floor(src.w);
```



<span data-ttu-id="5ed91-129">A função Floor converte o argumento passado para o maior inteiro que é menor que (ou igual a) do argumento.</span><span class="sxs-lookup"><span data-stu-id="5ed91-129">The floor function converts the argument passed in to the greatest integer that is less than (or equal to) the argument.</span></span> <span data-ttu-id="5ed91-130">Isso é convertido em um float e, em seguida, subtraído do o valor original.</span><span class="sxs-lookup"><span data-stu-id="5ed91-130">This is converted to a float and then subtracted fom the original value.</span></span> <span data-ttu-id="5ed91-131">O valor fracionário resultante varia de 0,0 a 1,0.</span><span class="sxs-lookup"><span data-stu-id="5ed91-131">The resulting fractional value ranges from 0.0 through 1.0.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5ed91-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5ed91-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ed91-133">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="5ed91-133">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




