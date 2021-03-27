---
title: if_comp-vs
description: Inicie um If bool-vs... else-vs... endif-vs Block, com uma condição baseada em valores que poderiam ser computados em um sombreador. Essa instrução é usada para ignorar um bloco de código, com base em uma condição.
ms.assetid: a3fe93c6-be26-4216-a601-3be52a74be06
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dadbe9620367efc75f821a711de89eb3498d247f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104988553"
---
# <a name="if_comp---vs"></a><span data-ttu-id="b8337-104">Se \_ comp-vs</span><span class="sxs-lookup"><span data-stu-id="b8337-104">if\_comp - vs</span></span>

<span data-ttu-id="b8337-105">Inicie um [If bool-vs](if-bool---vs.md)... [else-vs](else---vs.md)... [endif-vs](endif---vs.md) Block, com uma condição baseada em valores que poderiam ser computados em um sombreador.</span><span class="sxs-lookup"><span data-stu-id="b8337-105">Start an [if bool - vs](if-bool---vs.md)...[else - vs](else---vs.md)...[endif - vs](endif---vs.md) block, with a condition based on values that could be computed in a shader.</span></span> <span data-ttu-id="b8337-106">Essa instrução é usada para ignorar um bloco de código, com base em uma condição.</span><span class="sxs-lookup"><span data-stu-id="b8337-106">This instruction is used to skip a block of code, based on a condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8337-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b8337-107">Syntax</span></span>



| <span data-ttu-id="b8337-108">Se \_ comp src0, src1</span><span class="sxs-lookup"><span data-stu-id="b8337-108">if\_comp src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="b8337-109">Em que:</span><span class="sxs-lookup"><span data-stu-id="b8337-109">Where:</span></span>

-   <span data-ttu-id="b8337-110">\_comp é uma comparação entre os dois registros de origem.</span><span class="sxs-lookup"><span data-stu-id="b8337-110">\_comp is a comparison between the two source registers.</span></span> <span data-ttu-id="b8337-111">Pode ser um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="b8337-111">It can be one of the following:</span></span> 

    | <span data-ttu-id="b8337-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="b8337-112">Syntax</span></span> | <span data-ttu-id="b8337-113">Comparação</span><span class="sxs-lookup"><span data-stu-id="b8337-113">Comparison</span></span>            |
    |--------|-----------------------|
    | <span data-ttu-id="b8337-114">\_gt</span><span class="sxs-lookup"><span data-stu-id="b8337-114">\_gt</span></span>   | <span data-ttu-id="b8337-115">Maior que</span><span class="sxs-lookup"><span data-stu-id="b8337-115">Greater than</span></span>          |
    | <span data-ttu-id="b8337-116">\_lt</span><span class="sxs-lookup"><span data-stu-id="b8337-116">\_lt</span></span>   | <span data-ttu-id="b8337-117">Menor que</span><span class="sxs-lookup"><span data-stu-id="b8337-117">Less than</span></span>             |
    | <span data-ttu-id="b8337-118">\_GE</span><span class="sxs-lookup"><span data-stu-id="b8337-118">\_ge</span></span>   | <span data-ttu-id="b8337-119">Maior ou igual</span><span class="sxs-lookup"><span data-stu-id="b8337-119">Greater than or equal</span></span> |
    | <span data-ttu-id="b8337-120">\_quivo</span><span class="sxs-lookup"><span data-stu-id="b8337-120">\_le</span></span>   | <span data-ttu-id="b8337-121">Inferior ou igual</span><span class="sxs-lookup"><span data-stu-id="b8337-121">Less than or equal</span></span>    |
    | <span data-ttu-id="b8337-122">\_EQ</span><span class="sxs-lookup"><span data-stu-id="b8337-122">\_eq</span></span>   | <span data-ttu-id="b8337-123">Igual a</span><span class="sxs-lookup"><span data-stu-id="b8337-123">Equal to</span></span>              |
    | <span data-ttu-id="b8337-124">\_m</span><span class="sxs-lookup"><span data-stu-id="b8337-124">\_ne</span></span>   | <span data-ttu-id="b8337-125">Não igual a</span><span class="sxs-lookup"><span data-stu-id="b8337-125">Not equal to</span></span>          |

    

     

-   <span data-ttu-id="b8337-126">src0 é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="b8337-126">src0 is a source register.</span></span> <span data-ttu-id="b8337-127">Replicate swizzle é necessário para selecionar um componente.</span><span class="sxs-lookup"><span data-stu-id="b8337-127">Replicate swizzle is required to select a component.</span></span>
-   <span data-ttu-id="b8337-128">src1 é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="b8337-128">src1 is a source register.</span></span> <span data-ttu-id="b8337-129">Replicate swizzle é necessário para selecionar um componente.</span><span class="sxs-lookup"><span data-stu-id="b8337-129">Replicate swizzle is required to select a component.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8337-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="b8337-130">Remarks</span></span>



| <span data-ttu-id="b8337-131">Versões do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="b8337-131">Vertex shader versions</span></span> | <span data-ttu-id="b8337-132">1\_1</span><span class="sxs-lookup"><span data-stu-id="b8337-132">1\_1</span></span> | <span data-ttu-id="b8337-133">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b8337-133">2\_0</span></span> | <span data-ttu-id="b8337-134">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="b8337-134">2\_x</span></span> | <span data-ttu-id="b8337-135">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="b8337-135">2\_sw</span></span> | <span data-ttu-id="b8337-136">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b8337-136">3\_0</span></span> | <span data-ttu-id="b8337-137">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="b8337-137">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="b8337-138">Se \_ comp</span><span class="sxs-lookup"><span data-stu-id="b8337-138">if\_comp</span></span>               |      |      | <span data-ttu-id="b8337-139">x</span><span class="sxs-lookup"><span data-stu-id="b8337-139">x</span></span>    | <span data-ttu-id="b8337-140">x</span><span class="sxs-lookup"><span data-stu-id="b8337-140">x</span></span>     | <span data-ttu-id="b8337-141">x</span><span class="sxs-lookup"><span data-stu-id="b8337-141">x</span></span>    | <span data-ttu-id="b8337-142">x</span><span class="sxs-lookup"><span data-stu-id="b8337-142">x</span></span>     |



 

<span data-ttu-id="b8337-143">Essa instrução é usada para ignorar um bloco de código, com base em uma condição.</span><span class="sxs-lookup"><span data-stu-id="b8337-143">This instruction is used to skip a block of code, based on a condition.</span></span>


```
if_lt src0, src1
   jump to the corresponding else or endif instruction;
```



<span data-ttu-id="b8337-144">Tenha cuidado ao usar os modos de comparação Equals e not Equals em números de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="b8337-144">Be careful using the equals and not equals comparison modes on floating point numbers.</span></span> <span data-ttu-id="b8337-145">Como o arredondamento ocorre durante cálculos de ponto flutuante, a comparação pode ser feita em relação a um valor de Épsilon (número pequeno de zeros) para evitar erros.</span><span class="sxs-lookup"><span data-stu-id="b8337-145">Because rounding occurs during during floating point calculations, the comparison can be done against an epsilon value (small nonzero number) to avoid errors.</span></span>

<span data-ttu-id="b8337-146">As restrições incluem:</span><span class="sxs-lookup"><span data-stu-id="b8337-146">Restrictions include:</span></span>

-   <span data-ttu-id="b8337-147">Se \_ comp... [else-vs](else---vs.md)... [endif – blocos vs](endif---vs.md) (juntamente com os blocos predicados If) podem ser aninhados até 24 camadas de profundidade.</span><span class="sxs-lookup"><span data-stu-id="b8337-147">if\_comp...[else - vs](else---vs.md)...[endif - vs](endif---vs.md) blocks (along with the predicated if blocks) can be nested up to 24 layers deep.</span></span>
-   <span data-ttu-id="b8337-148">os registros src0 e src1 exigem uma swizzle replicate.</span><span class="sxs-lookup"><span data-stu-id="b8337-148">src0 and src1 registers require a replicate swizzle.</span></span>
-   <span data-ttu-id="b8337-149">Se os \_ blocos de comp precisarem terminar com uma instrução [else-vs](else---vs.md) ou [endif-vs](endif---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="b8337-149">if\_comp blocks must end with an [else - vs](else---vs.md) or [endif - vs](endif---vs.md) instruction.</span></span>
-   <span data-ttu-id="b8337-150">Se \_ comp... [else-vs](else---vs.md)... [endif – blocos vs](endif---vs.md) não podem ampliar um bloco de loop.</span><span class="sxs-lookup"><span data-stu-id="b8337-150">if\_comp...[else - vs](else---vs.md)...[endif - vs](endif---vs.md) blocks cannot straddle a loop block.</span></span> <span data-ttu-id="b8337-151">O \_ bloco If comp deve estar completamente dentro ou fora do bloco [loop vs](loop---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="b8337-151">The if\_comp block must be completely inside, or outside the [loop - vs](loop---vs.md) block.</span></span>

## <a name="example"></a><span data-ttu-id="b8337-152">Exemplo</span><span class="sxs-lookup"><span data-stu-id="b8337-152">Example</span></span>

<span data-ttu-id="b8337-153">Essa instrução fornece controle de fluxo dinâmico condicional.</span><span class="sxs-lookup"><span data-stu-id="b8337-153">This instruction provides conditional dynamic flow control.</span></span>


```
if_lt r3.x, r4.y
// Instructions to run if r3.x < r4.y

else
// Instructions to run otherwise

endif
```



## <a name="related-topics"></a><span data-ttu-id="b8337-154">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b8337-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8337-155">Instruções do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="b8337-155">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




