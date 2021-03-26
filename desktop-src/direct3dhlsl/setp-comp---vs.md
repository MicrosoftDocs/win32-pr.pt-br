---
title: setp_comp-vs
description: Defina o registro de predicado. | setp_comp-vs
ms.assetid: bfead3f8-f7fe-4fc1-939f-8e5fbc3e0adf
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 77d9e5f46e9fb8bbcfb96e56d13cd6f7cebfecc2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104370880"
---
# <a name="setp_comp---vs"></a><span data-ttu-id="48ff3-104">setp \_ comp-vs</span><span class="sxs-lookup"><span data-stu-id="48ff3-104">setp\_comp - vs</span></span>

<span data-ttu-id="48ff3-105">Defina o registro de predicado.</span><span class="sxs-lookup"><span data-stu-id="48ff3-105">Set the predicate register.</span></span>

## <a name="syntax"></a><span data-ttu-id="48ff3-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="48ff3-106">Syntax</span></span>



| <span data-ttu-id="48ff3-107">setp \_ comp DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="48ff3-107">setp\_comp dst, src0, src1</span></span> |
|----------------------------|



 

<span data-ttu-id="48ff3-108">Em que:</span><span class="sxs-lookup"><span data-stu-id="48ff3-108">Where:</span></span>

-   <span data-ttu-id="48ff3-109">\_comp é uma comparação por canal entre os dois registros de origem.</span><span class="sxs-lookup"><span data-stu-id="48ff3-109">\_comp is a per-channel comparison between the two source registers.</span></span> <span data-ttu-id="48ff3-110">Pode ser um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="48ff3-110">It can be one of the following:</span></span> 

    | <span data-ttu-id="48ff3-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="48ff3-111">Syntax</span></span> | <span data-ttu-id="48ff3-112">Comparação</span><span class="sxs-lookup"><span data-stu-id="48ff3-112">Comparison</span></span>            |
    |--------|-----------------------|
    | <span data-ttu-id="48ff3-113">\_gt</span><span class="sxs-lookup"><span data-stu-id="48ff3-113">\_gt</span></span>   | <span data-ttu-id="48ff3-114">Maior que</span><span class="sxs-lookup"><span data-stu-id="48ff3-114">Greater than</span></span>          |
    | <span data-ttu-id="48ff3-115">\_lt</span><span class="sxs-lookup"><span data-stu-id="48ff3-115">\_lt</span></span>   | <span data-ttu-id="48ff3-116">Menor que</span><span class="sxs-lookup"><span data-stu-id="48ff3-116">Less than</span></span>             |
    | <span data-ttu-id="48ff3-117">\_GE</span><span class="sxs-lookup"><span data-stu-id="48ff3-117">\_ge</span></span>   | <span data-ttu-id="48ff3-118">Maior ou igual</span><span class="sxs-lookup"><span data-stu-id="48ff3-118">Greater than or equal</span></span> |
    | <span data-ttu-id="48ff3-119">\_quivo</span><span class="sxs-lookup"><span data-stu-id="48ff3-119">\_le</span></span>   | <span data-ttu-id="48ff3-120">Inferior ou igual</span><span class="sxs-lookup"><span data-stu-id="48ff3-120">Less than or equal</span></span>    |
    | <span data-ttu-id="48ff3-121">\_EQ</span><span class="sxs-lookup"><span data-stu-id="48ff3-121">\_eq</span></span>   | <span data-ttu-id="48ff3-122">Igual a</span><span class="sxs-lookup"><span data-stu-id="48ff3-122">Equal to</span></span>              |
    | <span data-ttu-id="48ff3-123">\_m</span><span class="sxs-lookup"><span data-stu-id="48ff3-123">\_ne</span></span>   | <span data-ttu-id="48ff3-124">Não igual a</span><span class="sxs-lookup"><span data-stu-id="48ff3-124">Not equal to</span></span>          |

    

     

-   <span data-ttu-id="48ff3-125">DST é o [predicado Register](dx9-graphics-reference-asm-vs-registers-predicate.md) Register, P0.</span><span class="sxs-lookup"><span data-stu-id="48ff3-125">dst is the [Predicate Register](dx9-graphics-reference-asm-vs-registers-predicate.md) register, p0.</span></span>
-   <span data-ttu-id="48ff3-126">src0 é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="48ff3-126">src0 is a source register.</span></span>
-   <span data-ttu-id="48ff3-127">src1 é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="48ff3-127">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="48ff3-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="48ff3-128">Remarks</span></span>



| <span data-ttu-id="48ff3-129">Versões do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="48ff3-129">Vertex shader versions</span></span> | <span data-ttu-id="48ff3-130">1\_1</span><span class="sxs-lookup"><span data-stu-id="48ff3-130">1\_1</span></span> | <span data-ttu-id="48ff3-131">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="48ff3-131">2\_0</span></span> | <span data-ttu-id="48ff3-132">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="48ff3-132">2\_x</span></span> | <span data-ttu-id="48ff3-133">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="48ff3-133">2\_sw</span></span> | <span data-ttu-id="48ff3-134">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="48ff3-134">3\_0</span></span> | <span data-ttu-id="48ff3-135">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="48ff3-135">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="48ff3-136">comp de setp \_</span><span class="sxs-lookup"><span data-stu-id="48ff3-136">setp\_comp</span></span>             |      |      | <span data-ttu-id="48ff3-137">x</span><span class="sxs-lookup"><span data-stu-id="48ff3-137">x</span></span>    | <span data-ttu-id="48ff3-138">x</span><span class="sxs-lookup"><span data-stu-id="48ff3-138">x</span></span>     | <span data-ttu-id="48ff3-139">x</span><span class="sxs-lookup"><span data-stu-id="48ff3-139">x</span></span>    | <span data-ttu-id="48ff3-140">x</span><span class="sxs-lookup"><span data-stu-id="48ff3-140">x</span></span>     |



 

<span data-ttu-id="48ff3-141">Essa instrução Opera como:</span><span class="sxs-lookup"><span data-stu-id="48ff3-141">This instruction operates as:</span></span>


```
per channel in destination write mask
{
  dst.channel = src0.channel cmp src1.channel
}
```



<span data-ttu-id="48ff3-142">Para cada canal que pode ser gravado de acordo com a máscara de gravação de destino, salve o resultado booliano da operação de comparação entre os canais correspondentes de src0 e src1 (depois que o modificador de origem swizzles tiver sido resolvido).</span><span class="sxs-lookup"><span data-stu-id="48ff3-142">For each channel that can be written according to the destination write mask, save the boolean result of the comparison operation between the corresponding channels of src0 and src1 (after the source modifier swizzles have been resolved).</span></span>

<span data-ttu-id="48ff3-143">Os registros de origem permitem que swizzles de componente arbitrários sejam especificados.</span><span class="sxs-lookup"><span data-stu-id="48ff3-143">Source registers allow arbitrary component swizzles to be specified.</span></span>

<span data-ttu-id="48ff3-144">O registro de destino permite máscaras de gravação arbitrárias.</span><span class="sxs-lookup"><span data-stu-id="48ff3-144">The destination register allows arbitrary write masks.</span></span>

<span data-ttu-id="48ff3-145">O registro do dest deve ser o predicado Register.</span><span class="sxs-lookup"><span data-stu-id="48ff3-145">The dest register must be the predicate register.</span></span>

## <a name="applying-the-predicate-register"></a><span data-ttu-id="48ff3-146">Aplicando o registro de predicado</span><span class="sxs-lookup"><span data-stu-id="48ff3-146">Applying the Predicate Register</span></span>

<span data-ttu-id="48ff3-147">Após o registro de predicado ter sido inicializado com setp, ele pode ser usado para controlar uma instrução por componente.</span><span class="sxs-lookup"><span data-stu-id="48ff3-147">Once the predicate register has been initialized with setp, it can be used to control an instruction per component.</span></span> <span data-ttu-id="48ff3-148">Esta é a sintaxe:</span><span class="sxs-lookup"><span data-stu-id="48ff3-148">Here's the syntax:</span></span>


```
([!]p0[.swizzle]) instruction dest, srcReg, ...
```



<span data-ttu-id="48ff3-149">Em que:</span><span class="sxs-lookup"><span data-stu-id="48ff3-149">Where:</span></span>

-   <span data-ttu-id="48ff3-150">\[!\] é um booliano opcional não</span><span class="sxs-lookup"><span data-stu-id="48ff3-150">\[!\] is an optional boolean NOT</span></span>
-   <span data-ttu-id="48ff3-151">P0 é o registro de predicado</span><span class="sxs-lookup"><span data-stu-id="48ff3-151">p0 is the predicate register</span></span>
-   <span data-ttu-id="48ff3-152">\[. swizzle \] é um swizzle opcional a ser aplicado ao conteúdo do predicado Register antes de usá-lo para mascarar a instrução.</span><span class="sxs-lookup"><span data-stu-id="48ff3-152">\[.swizzle\] is an optional swizzle to apply to the contents of the predicate register before using it to mask the instruction.</span></span> <span data-ttu-id="48ff3-153">Os swizzles disponíveis são:. xyzw (padrão quando nenhum especificado) ou qualquer replicar swizzle:. x/. r,. y/. g,. z/. b ou. a/. w.</span><span class="sxs-lookup"><span data-stu-id="48ff3-153">The available swizzles are: .xyzw (default when none specified), or any replicate swizzle: .x/.r, .y/.g, .z/.b or .a/.w.</span></span>
-   <span data-ttu-id="48ff3-154">instrução é qualquer instrução aritmetic ou de textura.</span><span class="sxs-lookup"><span data-stu-id="48ff3-154">instruction is any aritmetic, or texture instruction.</span></span> <span data-ttu-id="48ff3-155">Essa não pode ser uma instrução de controle de fluxo estática ou dinâmica.</span><span class="sxs-lookup"><span data-stu-id="48ff3-155">This cannot be a static or dynamic flow control instruction.</span></span>
-   <span data-ttu-id="48ff3-156">dest, srcReg,... os registros são exigidos pela instrução</span><span class="sxs-lookup"><span data-stu-id="48ff3-156">dest, srcReg, ... are the registers required by the instruction</span></span>

<span data-ttu-id="48ff3-157">Supondo que o registro de predicado tenha sido configurado com valores de componente (true, true, false, false), ele pode ser aplicado a esta instrução:</span><span class="sxs-lookup"><span data-stu-id="48ff3-157">Assuming the predicate register has been set up with (true, true, false, false) component values, it can be applied to this instruction:</span></span>


```
// given r0 = 0,0,1,1
// given r1 = 1,1,0,0
setp_le p0, r0, r1
(p0) add r2, r3, r4
```



<span data-ttu-id="48ff3-158">para executar um componente 2, adicione.</span><span class="sxs-lookup"><span data-stu-id="48ff3-158">to perform a 2 component add.</span></span>


```
r2.x = r3.x + r4.x
r2.y = r3.y + r4.y
```



<span data-ttu-id="48ff3-159">Os componentes x e y do R2 não serão gravados, pois o registro de predicado continha false nos componentes z e w.</span><span class="sxs-lookup"><span data-stu-id="48ff3-159">The x and y components of r2 will not be written since the predicate register contained false in components z and w.</span></span>

<span data-ttu-id="48ff3-160">A aplicação do predicado Register a uma instrução aritmética ou de textura aumenta sua contagem de Slots de instrução em 1.</span><span class="sxs-lookup"><span data-stu-id="48ff3-160">Applying the predicate register to an arithmetic or texture instruction increases its instruction slot count by 1.</span></span>

<span data-ttu-id="48ff3-161">O registro de predicado também pode ser aplicado a instruções [If Pred-vs](if-pred---vs.md), [callnz Pred-vs](callnz-pred---vs.md) e [breakp-vs](breakp---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="48ff3-161">The predicate register can also be applied to [if pred - vs](if-pred---vs.md), [callnz pred - vs](callnz-pred---vs.md) and [breakp - vs](breakp---vs.md) instructions.</span></span> <span data-ttu-id="48ff3-162">Essas instruções de controle de fluxo não têm nenhum aumento na contagem de Slots de instrução ao usar o registro de predicado.</span><span class="sxs-lookup"><span data-stu-id="48ff3-162">These flow control instructions do not have any increase in the instruction slot count when using the predicate register.</span></span>

## <a name="related-topics"></a><span data-ttu-id="48ff3-163">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="48ff3-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48ff3-164">Instruções do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="48ff3-164">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




