---
title: if_comp-PS
description: Inicie um If bool-PS... else-PS... endif-PS Block, com uma condição baseada em valores que poderiam ser computados em um sombreador. Essa instrução é usada para ignorar um bloco de código, com base em uma condição.
ms.assetid: a641e347-df28-4a3f-a461-0b6aee758e59
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: db30983c83bc7d66e06befd07f4eb1dcdc9b21ea
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103638852"
---
# <a name="if_comp---ps"></a><span data-ttu-id="9b2ab-104">Se \_ comp-PS</span><span class="sxs-lookup"><span data-stu-id="9b2ab-104">if\_comp - ps</span></span>

<span data-ttu-id="9b2ab-105">Inicie um [If bool-PS](if-bool---ps.md)... [else-PS](else---ps.md)... [endif-PS](endif---ps.md) Block, com uma condição baseada em valores que poderiam ser computados em um sombreador.</span><span class="sxs-lookup"><span data-stu-id="9b2ab-105">Start an [if bool - ps](if-bool---ps.md)...[else - ps](else---ps.md)...[endif - ps](endif---ps.md) block, with a condition based on values that could be computed in a shader.</span></span> <span data-ttu-id="9b2ab-106">Essa instrução é usada para ignorar um bloco de código, com base em uma condição.</span><span class="sxs-lookup"><span data-stu-id="9b2ab-106">This instruction is used to skip a block of code, based on a condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b2ab-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="9b2ab-107">Syntax</span></span>



| <span data-ttu-id="9b2ab-108">Se \_ comp src0, src1</span><span class="sxs-lookup"><span data-stu-id="9b2ab-108">if\_comp src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="9b2ab-109">Em que:</span><span class="sxs-lookup"><span data-stu-id="9b2ab-109">Where:</span></span>

-   <span data-ttu-id="9b2ab-110">\_comp é uma comparação entre os dois registros de origem.</span><span class="sxs-lookup"><span data-stu-id="9b2ab-110">\_comp is a comparison between the two source registers.</span></span> <span data-ttu-id="9b2ab-111">Pode ser um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="9b2ab-111">It can be one of the following:</span></span> 

    | <span data-ttu-id="9b2ab-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="9b2ab-112">Syntax</span></span> | <span data-ttu-id="9b2ab-113">Comparação</span><span class="sxs-lookup"><span data-stu-id="9b2ab-113">Comparison</span></span>            |
    |--------|-----------------------|
    | <span data-ttu-id="9b2ab-114">\_gt</span><span class="sxs-lookup"><span data-stu-id="9b2ab-114">\_gt</span></span>   | <span data-ttu-id="9b2ab-115">Maior que</span><span class="sxs-lookup"><span data-stu-id="9b2ab-115">Greater than</span></span>          |
    | <span data-ttu-id="9b2ab-116">\_lt</span><span class="sxs-lookup"><span data-stu-id="9b2ab-116">\_lt</span></span>   | <span data-ttu-id="9b2ab-117">Menor que</span><span class="sxs-lookup"><span data-stu-id="9b2ab-117">Less than</span></span>             |
    | <span data-ttu-id="9b2ab-118">\_GE</span><span class="sxs-lookup"><span data-stu-id="9b2ab-118">\_ge</span></span>   | <span data-ttu-id="9b2ab-119">Maior ou igual</span><span class="sxs-lookup"><span data-stu-id="9b2ab-119">Greater than or equal</span></span> |
    | <span data-ttu-id="9b2ab-120">\_quivo</span><span class="sxs-lookup"><span data-stu-id="9b2ab-120">\_le</span></span>   | <span data-ttu-id="9b2ab-121">Inferior ou igual</span><span class="sxs-lookup"><span data-stu-id="9b2ab-121">Less than or equal</span></span>    |
    | <span data-ttu-id="9b2ab-122">\_EQ</span><span class="sxs-lookup"><span data-stu-id="9b2ab-122">\_eq</span></span>   | <span data-ttu-id="9b2ab-123">Igual a</span><span class="sxs-lookup"><span data-stu-id="9b2ab-123">Equal to</span></span>              |
    | <span data-ttu-id="9b2ab-124">\_m</span><span class="sxs-lookup"><span data-stu-id="9b2ab-124">\_ne</span></span>   | <span data-ttu-id="9b2ab-125">Não igual a</span><span class="sxs-lookup"><span data-stu-id="9b2ab-125">Not equal to</span></span>          |

    

     

-   <span data-ttu-id="9b2ab-126">src0 é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="9b2ab-126">src0 is a source register.</span></span> <span data-ttu-id="9b2ab-127">Replicate swizzle é necessário para selecionar um componente.</span><span class="sxs-lookup"><span data-stu-id="9b2ab-127">Replicate swizzle is required to select a component.</span></span>
-   <span data-ttu-id="9b2ab-128">src1 é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="9b2ab-128">src1 is a source register.</span></span> <span data-ttu-id="9b2ab-129">Replicate swizzle é necessário para selecionar um componente.</span><span class="sxs-lookup"><span data-stu-id="9b2ab-129">Replicate swizzle is required to select a component.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b2ab-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="9b2ab-130">Remarks</span></span>



| <span data-ttu-id="9b2ab-131">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="9b2ab-131">Pixel shader versions</span></span> | <span data-ttu-id="9b2ab-132">1\_1</span><span class="sxs-lookup"><span data-stu-id="9b2ab-132">1\_1</span></span> | <span data-ttu-id="9b2ab-133">1\_2</span><span class="sxs-lookup"><span data-stu-id="9b2ab-133">1\_2</span></span> | <span data-ttu-id="9b2ab-134">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="9b2ab-134">1\_3</span></span> | <span data-ttu-id="9b2ab-135">1\_4</span><span class="sxs-lookup"><span data-stu-id="9b2ab-135">1\_4</span></span> | <span data-ttu-id="9b2ab-136">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9b2ab-136">2\_0</span></span> | <span data-ttu-id="9b2ab-137">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="9b2ab-137">2\_x</span></span> | <span data-ttu-id="9b2ab-138">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="9b2ab-138">2\_sw</span></span> | <span data-ttu-id="9b2ab-139">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9b2ab-139">3\_0</span></span> | <span data-ttu-id="9b2ab-140">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="9b2ab-140">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="9b2ab-141">Se \_ comp</span><span class="sxs-lookup"><span data-stu-id="9b2ab-141">if\_comp</span></span>              |      |      |      |      |      | <span data-ttu-id="9b2ab-142">x</span><span class="sxs-lookup"><span data-stu-id="9b2ab-142">x</span></span>    | <span data-ttu-id="9b2ab-143">x</span><span class="sxs-lookup"><span data-stu-id="9b2ab-143">x</span></span>     | <span data-ttu-id="9b2ab-144">x</span><span class="sxs-lookup"><span data-stu-id="9b2ab-144">x</span></span>    | <span data-ttu-id="9b2ab-145">x</span><span class="sxs-lookup"><span data-stu-id="9b2ab-145">x</span></span>     |



 

<span data-ttu-id="9b2ab-146">Essa instrução é usada para ignorar um bloco de código, com base em uma condição.</span><span class="sxs-lookup"><span data-stu-id="9b2ab-146">This instruction is used to skip a block of code, based on a condition.</span></span>


```
if (src0 comparison src1)
   jump to the corresponding else or endif instruction;
```



<span data-ttu-id="9b2ab-147">Tenha cuidado ao usar os modos de comparação Equals e not Equals em números de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="9b2ab-147">Be careful using the equals and not equals comparison modes on floating point numbers.</span></span> <span data-ttu-id="9b2ab-148">Como o arredondamento ocorre durante cálculos de ponto flutuante, a comparação pode ser feita em relação a um valor de Épsilon (número pequeno de zeros) para evitar erros.</span><span class="sxs-lookup"><span data-stu-id="9b2ab-148">Because rounding occurs during during floating point calculations, the comparison can be done against an epsilon value (small nonzero number) to avoid errors.</span></span>

<span data-ttu-id="9b2ab-149">As restrições incluem:</span><span class="sxs-lookup"><span data-stu-id="9b2ab-149">Restrictions include:</span></span>

-   <span data-ttu-id="9b2ab-150">Se \_ comp... [else-PS](else---ps.md)... [endif-](endif---ps.md) os blocos PS (juntamente com os blocos predicados [If](if-bool---ps.md) ) podem ser aninhados até 24 camadas de profundidade.</span><span class="sxs-lookup"><span data-stu-id="9b2ab-150">if\_comp...[else - ps](else---ps.md)...[endif - ps](endif---ps.md) blocks (along with the predicated [if](if-bool---ps.md) blocks) can be nested up to 24 layers deep.</span></span>
-   <span data-ttu-id="9b2ab-151">os registros src0 e src1 exigem uma swizzle replicate.</span><span class="sxs-lookup"><span data-stu-id="9b2ab-151">src0 and src1 registers require a replicate swizzle.</span></span>
-   <span data-ttu-id="9b2ab-152">Se os \_ blocos de comp precisarem terminar com uma instrução [else-vs](else---vs.md) ou [endif-vs](endif---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="9b2ab-152">if\_comp blocks must end with an [else - vs](else---vs.md) or [endif - vs](endif---vs.md) instruction.</span></span>
-   <span data-ttu-id="9b2ab-153">Se \_ comp... [else-PS](else---ps.md)... [endif-os blocos de PS](endif---ps.md) não podem ampliar um bloco de loop.</span><span class="sxs-lookup"><span data-stu-id="9b2ab-153">if\_comp...[else - ps](else---ps.md)...[endif - ps](endif---ps.md) blocks cannot straddle a loop block.</span></span> <span data-ttu-id="9b2ab-154">O \_ bloco If comp deve estar completamente dentro ou fora do bloco loop.</span><span class="sxs-lookup"><span data-stu-id="9b2ab-154">The if\_comp block must be completely inside or outside the loop block.</span></span>

## <a name="example"></a><span data-ttu-id="9b2ab-155">Exemplo</span><span class="sxs-lookup"><span data-stu-id="9b2ab-155">Example</span></span>

<span data-ttu-id="9b2ab-156">Essa instrução fornece controle de fluxo dinâmico condicional.</span><span class="sxs-lookup"><span data-stu-id="9b2ab-156">This instruction provides conditional dynamic flow control.</span></span>


```
if_lt r3.x, r4.y
// Instructions to run if r3.x < r4.y

else
// Instructions to run otherwise

endif
```



## <a name="related-topics"></a><span data-ttu-id="9b2ab-157">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9b2ab-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b2ab-158">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="9b2ab-158">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




