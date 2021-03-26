---
title: setp_comp-PS
description: Defina o registro de predicado. | setp_comp-PS
ms.assetid: a9acb685-f9aa-41f1-8ef1-6d104cb76a09
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a68da290ecb04e9cb7ae49c5525997fbf4c112a3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104172810"
---
# <a name="setp_comp---ps"></a><span data-ttu-id="3e50c-104">setp \_ comp-PS</span><span class="sxs-lookup"><span data-stu-id="3e50c-104">setp\_comp - ps</span></span>

<span data-ttu-id="3e50c-105">Defina o registro de predicado.</span><span class="sxs-lookup"><span data-stu-id="3e50c-105">Set the predicate register.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e50c-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="3e50c-106">Syntax</span></span>



| <span data-ttu-id="3e50c-107">setp \_ comp DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="3e50c-107">setp\_comp dst, src0, src1</span></span> |
|----------------------------|



 

<span data-ttu-id="3e50c-108">Em que:</span><span class="sxs-lookup"><span data-stu-id="3e50c-108">Where:</span></span>

-   <span data-ttu-id="3e50c-109">\_comp é uma comparação por canal entre os dois registros de origem.</span><span class="sxs-lookup"><span data-stu-id="3e50c-109">\_comp is a per-channel comparison between the two source registers.</span></span> <span data-ttu-id="3e50c-110">Pode ser um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="3e50c-110">It can be one of the following:</span></span> 

    | <span data-ttu-id="3e50c-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="3e50c-111">Syntax</span></span> | <span data-ttu-id="3e50c-112">Comparação</span><span class="sxs-lookup"><span data-stu-id="3e50c-112">Comparison</span></span>            |
    |--------|-----------------------|
    | <span data-ttu-id="3e50c-113">\_gt</span><span class="sxs-lookup"><span data-stu-id="3e50c-113">\_gt</span></span>   | <span data-ttu-id="3e50c-114">Maior que</span><span class="sxs-lookup"><span data-stu-id="3e50c-114">Greater than</span></span>          |
    | <span data-ttu-id="3e50c-115">\_lt</span><span class="sxs-lookup"><span data-stu-id="3e50c-115">\_lt</span></span>   | <span data-ttu-id="3e50c-116">Menor que</span><span class="sxs-lookup"><span data-stu-id="3e50c-116">Less than</span></span>             |
    | <span data-ttu-id="3e50c-117">\_GE</span><span class="sxs-lookup"><span data-stu-id="3e50c-117">\_ge</span></span>   | <span data-ttu-id="3e50c-118">Maior ou igual</span><span class="sxs-lookup"><span data-stu-id="3e50c-118">Greater than or equal</span></span> |
    | <span data-ttu-id="3e50c-119">\_quivo</span><span class="sxs-lookup"><span data-stu-id="3e50c-119">\_le</span></span>   | <span data-ttu-id="3e50c-120">Inferior ou igual</span><span class="sxs-lookup"><span data-stu-id="3e50c-120">Less than or equal</span></span>    |
    | <span data-ttu-id="3e50c-121">\_EQ</span><span class="sxs-lookup"><span data-stu-id="3e50c-121">\_eq</span></span>   | <span data-ttu-id="3e50c-122">Igual a</span><span class="sxs-lookup"><span data-stu-id="3e50c-122">Equal to</span></span>              |
    | <span data-ttu-id="3e50c-123">\_m</span><span class="sxs-lookup"><span data-stu-id="3e50c-123">\_ne</span></span>   | <span data-ttu-id="3e50c-124">Não igual a</span><span class="sxs-lookup"><span data-stu-id="3e50c-124">Not equal to</span></span>          |

    

     

-   <span data-ttu-id="3e50c-125">DST é o [predicado Register](dx9-graphics-reference-asm-ps-registers-predicate.md) Register, P0.</span><span class="sxs-lookup"><span data-stu-id="3e50c-125">dst is the [Predicate Register](dx9-graphics-reference-asm-ps-registers-predicate.md) register, p0.</span></span>
-   <span data-ttu-id="3e50c-126">src0 é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="3e50c-126">src0 is a source register.</span></span>
-   <span data-ttu-id="3e50c-127">src1 é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="3e50c-127">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e50c-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="3e50c-128">Remarks</span></span>



| <span data-ttu-id="3e50c-129">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="3e50c-129">Pixel shader versions</span></span> | <span data-ttu-id="3e50c-130">1\_1</span><span class="sxs-lookup"><span data-stu-id="3e50c-130">1\_1</span></span> | <span data-ttu-id="3e50c-131">1\_2</span><span class="sxs-lookup"><span data-stu-id="3e50c-131">1\_2</span></span> | <span data-ttu-id="3e50c-132">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="3e50c-132">1\_3</span></span> | <span data-ttu-id="3e50c-133">1\_4</span><span class="sxs-lookup"><span data-stu-id="3e50c-133">1\_4</span></span> | <span data-ttu-id="3e50c-134">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3e50c-134">2\_0</span></span> | <span data-ttu-id="3e50c-135">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="3e50c-135">2\_x</span></span> | <span data-ttu-id="3e50c-136">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="3e50c-136">2\_sw</span></span> | <span data-ttu-id="3e50c-137">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3e50c-137">3\_0</span></span> | <span data-ttu-id="3e50c-138">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="3e50c-138">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="3e50c-139">comp de setp \_</span><span class="sxs-lookup"><span data-stu-id="3e50c-139">setp\_comp</span></span>            |      |      |      |      |      | <span data-ttu-id="3e50c-140">x</span><span class="sxs-lookup"><span data-stu-id="3e50c-140">x</span></span>    | <span data-ttu-id="3e50c-141">x</span><span class="sxs-lookup"><span data-stu-id="3e50c-141">x</span></span>     | <span data-ttu-id="3e50c-142">x</span><span class="sxs-lookup"><span data-stu-id="3e50c-142">x</span></span>    | <span data-ttu-id="3e50c-143">x</span><span class="sxs-lookup"><span data-stu-id="3e50c-143">x</span></span>     |



 

<span data-ttu-id="3e50c-144">Essa instrução Opera como:</span><span class="sxs-lookup"><span data-stu-id="3e50c-144">This instruction operates as:</span></span>


```
per channel in destination write mask
{
  dst.channel = src0.channel cmp src1.channel
}
```



<span data-ttu-id="3e50c-145">Para cada canal que pode ser gravado de acordo com a máscara de gravação de destino, salve o resultado booliano da operação de comparação entre os canais correspondentes de src0 e src1 (depois que o modificador de origem swizzles tiver sido resolvido).</span><span class="sxs-lookup"><span data-stu-id="3e50c-145">For each channel that can be written according to the destination write mask, save the boolean result of the comparison operation between the corresponding channels of src0 and src1 (after the source modifier swizzles have been resolved).</span></span>

<span data-ttu-id="3e50c-146">Os registros de origem permitem que swizzles de componente arbitrários sejam especificados.</span><span class="sxs-lookup"><span data-stu-id="3e50c-146">Source registers allow arbitrary component swizzles to be specified.</span></span>

<span data-ttu-id="3e50c-147">O registro de destino permite máscaras de gravação arbitrárias.</span><span class="sxs-lookup"><span data-stu-id="3e50c-147">The destination register allows arbitrary write masks.</span></span>

<span data-ttu-id="3e50c-148">O registro de hora de verão deve ser o registro de predicado.</span><span class="sxs-lookup"><span data-stu-id="3e50c-148">The dst register must be the predicate register.</span></span>

## <a name="applying-the-predicate-register"></a><span data-ttu-id="3e50c-149">Aplicando o registro de predicado</span><span class="sxs-lookup"><span data-stu-id="3e50c-149">Applying the Predicate Register</span></span>

<span data-ttu-id="3e50c-150">Depois que o registro de predicado tiver sido inicializado com setp \_ comp, ele poderá ser usado para controlar uma instrução por componente.</span><span class="sxs-lookup"><span data-stu-id="3e50c-150">Once the predicate register has been initialized with setp\_comp, it can be used to control an instruction per component.</span></span> <span data-ttu-id="3e50c-151">Esta é a sintaxe:</span><span class="sxs-lookup"><span data-stu-id="3e50c-151">Here's the syntax:</span></span>


```
([!]p0[.swizzle]) instruction dest, src0, ...
```



<span data-ttu-id="3e50c-152">Em que:</span><span class="sxs-lookup"><span data-stu-id="3e50c-152">Where:</span></span>

-   <span data-ttu-id="3e50c-153">\[!\] é um booliano opcional não</span><span class="sxs-lookup"><span data-stu-id="3e50c-153">\[!\] is an optional boolean NOT</span></span>
-   <span data-ttu-id="3e50c-154">P0 é o registro de predicado</span><span class="sxs-lookup"><span data-stu-id="3e50c-154">p0 is the predicate register</span></span>
-   <span data-ttu-id="3e50c-155">\[. swizzle \] é um swizzle opcional a ser aplicado ao conteúdo do predicado Register antes de usá-lo para mascarar a instrução.</span><span class="sxs-lookup"><span data-stu-id="3e50c-155">\[.swizzle\] is an optional swizzle to apply to the contents of the predicate register before using it to mask the instruction.</span></span> <span data-ttu-id="3e50c-156">Os swizzles disponíveis são:. xyzw (padrão quando nenhum especificado) ou qualquer replicar swizzle:. x/. r,. y/. g,. z/. b ou. a/. w.</span><span class="sxs-lookup"><span data-stu-id="3e50c-156">The available swizzles are: .xyzw (default when none specified), or any replicate swizzle: .x/.r, .y/.g, .z/.b or .a/.w.</span></span>
-   <span data-ttu-id="3e50c-157">instrução é qualquer instrução aritmetic ou de textura.</span><span class="sxs-lookup"><span data-stu-id="3e50c-157">instruction is any aritmetic, or texture instruction.</span></span> <span data-ttu-id="3e50c-158">Essa não pode ser uma instrução de controle de fluxo estática ou dinâmica.</span><span class="sxs-lookup"><span data-stu-id="3e50c-158">This cannot be a static or dynamic flow control instruction.</span></span>
-   <span data-ttu-id="3e50c-159">dest, src0,... os registros são exigidos pela instrução</span><span class="sxs-lookup"><span data-stu-id="3e50c-159">dest, src0, ... are the registers required by the instruction</span></span>

<span data-ttu-id="3e50c-160">Supondo que o registro de predicado tenha sido configurado com valores de componente (true, true, false, false), ele pode ser aplicado a esta instrução:</span><span class="sxs-lookup"><span data-stu-id="3e50c-160">Assuming the predicate register has been set up with (true, true, false, false) component values, it can be applied to this instruction:</span></span>


```
(p0) add r1, r2, r3
```



<span data-ttu-id="3e50c-161">para executar um componente 2, adicione.</span><span class="sxs-lookup"><span data-stu-id="3e50c-161">to perform a 2 component add.</span></span>


```
r1.x = r2.x + r3.x
r1.y = r2.y + r3.y
```



<span data-ttu-id="3e50c-162">Os componentes z e w de R1 não serão escritos, pois o registro de predicado continha false nos componentes z e w.</span><span class="sxs-lookup"><span data-stu-id="3e50c-162">The z and w components of r1 will not be written since the predicate register contained false in components z and w.</span></span>

<span data-ttu-id="3e50c-163">A aplicação do predicado Register a uma instrução aritmética ou de textura aumenta sua contagem de Slots de instrução em 1.</span><span class="sxs-lookup"><span data-stu-id="3e50c-163">Applying the predicate register to an arithmetic or texture instruction increases its instruction slot count by 1.</span></span>

<span data-ttu-id="3e50c-164">O registro de predicado também pode ser aplicado às instruções [Pred-PS](if-pred---ps.md), [callnz Pred-PS](callnz-pred---ps.md) e [breakp-PS](break-p---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="3e50c-164">The predicate register can also be applied to [if pred - ps](if-pred---ps.md), [callnz pred - ps](callnz-pred---ps.md) and [breakp - ps](break-p---ps.md) instructions.</span></span> <span data-ttu-id="3e50c-165">Essas instruções de controle de fluxo não têm nenhum aumento na contagem de Slots de instrução ao usar o registro de predicado.</span><span class="sxs-lookup"><span data-stu-id="3e50c-165">These flow control instructions do not have any increase in the instruction slot count when using the predicate register.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3e50c-166">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3e50c-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e50c-167">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="3e50c-167">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




