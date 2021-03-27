---
title: Swizzling de registro de origem (referência do HLSL PS)
description: Swizzling refere-se à capacidade de copiar qualquer componente de registro de origem para qualquer componente de registro temporário. Swizzling não afeta os dados de registro de origem. Antes de uma instrução ser executada, os dados em um registro de origem são copiados para um registro temporário.
ms.assetid: 27aee6a8-5185-4236-b3e4-44addf230c34
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4ffc655129740f112a3ade9eb40c0bbe29dfc1fb
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/23/2019
ms.locfileid: "104293610"
---
# <a name="source-register-swizzling-hlsl-ps-reference"></a><span data-ttu-id="86f73-105">Swizzling de registro de origem (referência do HLSL PS)</span><span class="sxs-lookup"><span data-stu-id="86f73-105">Source register swizzling (HLSL PS reference)</span></span>

<span data-ttu-id="86f73-106">Swizzling refere-se à capacidade de copiar qualquer componente de registro de origem para qualquer componente de registro temporário.</span><span class="sxs-lookup"><span data-stu-id="86f73-106">Swizzling refers to the ability to copy any source register component to any temporary register component.</span></span> <span data-ttu-id="86f73-107">Swizzling não afeta os dados de registro de origem.</span><span class="sxs-lookup"><span data-stu-id="86f73-107">Swizzling does not affect the source register data.</span></span> <span data-ttu-id="86f73-108">Antes de uma instrução ser executada, os dados em um registro de origem são copiados para um registro temporário.</span><span class="sxs-lookup"><span data-stu-id="86f73-108">Before an instruction runs, the data in a source register is copied to a temporary register.</span></span>

## <a name="source-swizzling"></a><span data-ttu-id="86f73-109">Swizzling de origem</span><span class="sxs-lookup"><span data-stu-id="86f73-109">Source Swizzling</span></span>

<span data-ttu-id="86f73-110">O swizzle de origem permite que o componente individual de um registro de origem assuma o valor de qualquer um dos quatro componentes do mesmo registro de origem antes que o registro seja lido para computação.</span><span class="sxs-lookup"><span data-stu-id="86f73-110">Source swizzle allows individual component of a source register to take on the value of any of the four components of the same source register before the register is read for computation.</span></span>

<span data-ttu-id="86f73-111">Por exemplo, o swizzle. zxxy significa:</span><span class="sxs-lookup"><span data-stu-id="86f73-111">For example, the .zxxy swizzle means:</span></span>

-   <span data-ttu-id="86f73-112">o componente. x assumirá o valor do componente. z</span><span class="sxs-lookup"><span data-stu-id="86f73-112">.x component will take on the value of .z component</span></span>
-   <span data-ttu-id="86f73-113">o componente. y assumirá o valor do componente. x</span><span class="sxs-lookup"><span data-stu-id="86f73-113">.y component will take on the value of .x component</span></span>
-   <span data-ttu-id="86f73-114">o componente. z assumirá o valor do componente. x</span><span class="sxs-lookup"><span data-stu-id="86f73-114">.z component will take on the value of .x component</span></span>
-   <span data-ttu-id="86f73-115">o componente. w assumirá o valor do componente. y</span><span class="sxs-lookup"><span data-stu-id="86f73-115">.w component will take on the value of .y component</span></span>

<span data-ttu-id="86f73-116">Os componentes podem aparecer em qualquer ordem.</span><span class="sxs-lookup"><span data-stu-id="86f73-116">The components can appear in any order.</span></span> <span data-ttu-id="86f73-117">Se menos de quatro componentes forem especificados, o último componente será repetido.</span><span class="sxs-lookup"><span data-stu-id="86f73-117">If fewer than four components are specified, the last component is repeated.</span></span> <span data-ttu-id="86f73-118">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="86f73-118">For example:</span></span>


```
.xy  = .xyyy
.wzx = .wzxx
.z   = .zzzz
```



<span data-ttu-id="86f73-119">Se nenhum componente for especificado, nenhum swizzling será aplicado.</span><span class="sxs-lookup"><span data-stu-id="86f73-119">If no component is specified, no swizzling is applied.</span></span>

<span data-ttu-id="86f73-120">Algumas instruções têm restrições para swizzle de origem.</span><span class="sxs-lookup"><span data-stu-id="86f73-120">Some instructions have restrictions for source swizzle.</span></span> <span data-ttu-id="86f73-121">Elas são listadas nas páginas de referência de instrução respeitadas.</span><span class="sxs-lookup"><span data-stu-id="86f73-121">They are listed in the respected instruction reference pages.</span></span>



| <span data-ttu-id="86f73-122">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="86f73-122">Pixel shader versions</span></span> | <span data-ttu-id="86f73-123">1\_1</span><span class="sxs-lookup"><span data-stu-id="86f73-123">1\_1</span></span> | <span data-ttu-id="86f73-124">1\_2</span><span class="sxs-lookup"><span data-stu-id="86f73-124">1\_2</span></span> | <span data-ttu-id="86f73-125">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="86f73-125">1\_3</span></span> | <span data-ttu-id="86f73-126">1\_4</span><span class="sxs-lookup"><span data-stu-id="86f73-126">1\_4</span></span> | <span data-ttu-id="86f73-127">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="86f73-127">2\_0</span></span> | <span data-ttu-id="86f73-128">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="86f73-128">2\_x</span></span> | <span data-ttu-id="86f73-129">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="86f73-129">2\_sw</span></span> | <span data-ttu-id="86f73-130">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="86f73-130">3\_0</span></span> | <span data-ttu-id="86f73-131">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="86f73-131">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="86f73-132">. x</span><span class="sxs-lookup"><span data-stu-id="86f73-132">.x</span></span>                    |      |      |      | <span data-ttu-id="86f73-133">x</span><span class="sxs-lookup"><span data-stu-id="86f73-133">x</span></span>    | <span data-ttu-id="86f73-134">x</span><span class="sxs-lookup"><span data-stu-id="86f73-134">x</span></span>    | <span data-ttu-id="86f73-135">x</span><span class="sxs-lookup"><span data-stu-id="86f73-135">x</span></span>    | <span data-ttu-id="86f73-136">x</span><span class="sxs-lookup"><span data-stu-id="86f73-136">x</span></span>     | <span data-ttu-id="86f73-137">x</span><span class="sxs-lookup"><span data-stu-id="86f73-137">x</span></span>    | <span data-ttu-id="86f73-138">x</span><span class="sxs-lookup"><span data-stu-id="86f73-138">x</span></span>     |
| <span data-ttu-id="86f73-139">. y</span><span class="sxs-lookup"><span data-stu-id="86f73-139">.y</span></span>                    |      |      |      | <span data-ttu-id="86f73-140">x</span><span class="sxs-lookup"><span data-stu-id="86f73-140">x</span></span>    | <span data-ttu-id="86f73-141">x</span><span class="sxs-lookup"><span data-stu-id="86f73-141">x</span></span>    | <span data-ttu-id="86f73-142">x</span><span class="sxs-lookup"><span data-stu-id="86f73-142">x</span></span>    | <span data-ttu-id="86f73-143">x</span><span class="sxs-lookup"><span data-stu-id="86f73-143">x</span></span>     | <span data-ttu-id="86f73-144">x</span><span class="sxs-lookup"><span data-stu-id="86f73-144">x</span></span>    | <span data-ttu-id="86f73-145">x</span><span class="sxs-lookup"><span data-stu-id="86f73-145">x</span></span>     |
| <span data-ttu-id="86f73-146">. z</span><span class="sxs-lookup"><span data-stu-id="86f73-146">.z</span></span>                    | <span data-ttu-id="86f73-147">w.x.y.\*</span><span class="sxs-lookup"><span data-stu-id="86f73-147">x\*</span></span>  | <span data-ttu-id="86f73-148">w.x.y.\*</span><span class="sxs-lookup"><span data-stu-id="86f73-148">x\*</span></span>  | <span data-ttu-id="86f73-149">x\*</span><span class="sxs-lookup"><span data-stu-id="86f73-149">x\*</span></span>  | <span data-ttu-id="86f73-150">x</span><span class="sxs-lookup"><span data-stu-id="86f73-150">x</span></span>    | <span data-ttu-id="86f73-151">x</span><span class="sxs-lookup"><span data-stu-id="86f73-151">x</span></span>    | <span data-ttu-id="86f73-152">x</span><span class="sxs-lookup"><span data-stu-id="86f73-152">x</span></span>    | <span data-ttu-id="86f73-153">x</span><span class="sxs-lookup"><span data-stu-id="86f73-153">x</span></span>     | <span data-ttu-id="86f73-154">x</span><span class="sxs-lookup"><span data-stu-id="86f73-154">x</span></span>    | <span data-ttu-id="86f73-155">x</span><span class="sxs-lookup"><span data-stu-id="86f73-155">x</span></span>     |
| <span data-ttu-id="86f73-156">. w</span><span class="sxs-lookup"><span data-stu-id="86f73-156">.w</span></span>                    | <span data-ttu-id="86f73-157">x</span><span class="sxs-lookup"><span data-stu-id="86f73-157">x</span></span>    | <span data-ttu-id="86f73-158">x</span><span class="sxs-lookup"><span data-stu-id="86f73-158">x</span></span>    | <span data-ttu-id="86f73-159">x</span><span class="sxs-lookup"><span data-stu-id="86f73-159">x</span></span>    | <span data-ttu-id="86f73-160">x</span><span class="sxs-lookup"><span data-stu-id="86f73-160">x</span></span>    | <span data-ttu-id="86f73-161">x</span><span class="sxs-lookup"><span data-stu-id="86f73-161">x</span></span>    | <span data-ttu-id="86f73-162">x</span><span class="sxs-lookup"><span data-stu-id="86f73-162">x</span></span>    | <span data-ttu-id="86f73-163">x</span><span class="sxs-lookup"><span data-stu-id="86f73-163">x</span></span>     | <span data-ttu-id="86f73-164">x</span><span class="sxs-lookup"><span data-stu-id="86f73-164">x</span></span>    | <span data-ttu-id="86f73-165">x</span><span class="sxs-lookup"><span data-stu-id="86f73-165">x</span></span>     |
| <span data-ttu-id="86f73-166">. xyzw (padrão)</span><span class="sxs-lookup"><span data-stu-id="86f73-166">.xyzw (default)</span></span>       | <span data-ttu-id="86f73-167">x</span><span class="sxs-lookup"><span data-stu-id="86f73-167">x</span></span>    | <span data-ttu-id="86f73-168">x</span><span class="sxs-lookup"><span data-stu-id="86f73-168">x</span></span>    | <span data-ttu-id="86f73-169">x</span><span class="sxs-lookup"><span data-stu-id="86f73-169">x</span></span>    | <span data-ttu-id="86f73-170">x</span><span class="sxs-lookup"><span data-stu-id="86f73-170">x</span></span>    | <span data-ttu-id="86f73-171">x</span><span class="sxs-lookup"><span data-stu-id="86f73-171">x</span></span>    | <span data-ttu-id="86f73-172">x</span><span class="sxs-lookup"><span data-stu-id="86f73-172">x</span></span>    | <span data-ttu-id="86f73-173">x</span><span class="sxs-lookup"><span data-stu-id="86f73-173">x</span></span>     | <span data-ttu-id="86f73-174">x</span><span class="sxs-lookup"><span data-stu-id="86f73-174">x</span></span>    | <span data-ttu-id="86f73-175">x</span><span class="sxs-lookup"><span data-stu-id="86f73-175">x</span></span>     |
| <span data-ttu-id="86f73-176">.yzxw</span><span class="sxs-lookup"><span data-stu-id="86f73-176">.yzxw</span></span>                 |      |      |      |      | <span data-ttu-id="86f73-177">x</span><span class="sxs-lookup"><span data-stu-id="86f73-177">x</span></span>    | <span data-ttu-id="86f73-178">x</span><span class="sxs-lookup"><span data-stu-id="86f73-178">x</span></span>    | <span data-ttu-id="86f73-179">x</span><span class="sxs-lookup"><span data-stu-id="86f73-179">x</span></span>     | <span data-ttu-id="86f73-180">x</span><span class="sxs-lookup"><span data-stu-id="86f73-180">x</span></span>    | <span data-ttu-id="86f73-181">x</span><span class="sxs-lookup"><span data-stu-id="86f73-181">x</span></span>     |
| <span data-ttu-id="86f73-182">.zxyw</span><span class="sxs-lookup"><span data-stu-id="86f73-182">.zxyw</span></span>                 |      |      |      |      | <span data-ttu-id="86f73-183">x</span><span class="sxs-lookup"><span data-stu-id="86f73-183">x</span></span>    | <span data-ttu-id="86f73-184">x</span><span class="sxs-lookup"><span data-stu-id="86f73-184">x</span></span>    | <span data-ttu-id="86f73-185">x</span><span class="sxs-lookup"><span data-stu-id="86f73-185">x</span></span>     | <span data-ttu-id="86f73-186">x</span><span class="sxs-lookup"><span data-stu-id="86f73-186">x</span></span>    | <span data-ttu-id="86f73-187">x</span><span class="sxs-lookup"><span data-stu-id="86f73-187">x</span></span>     |
| <span data-ttu-id="86f73-188">.wzyx</span><span class="sxs-lookup"><span data-stu-id="86f73-188">.wzyx</span></span>                 |      |      |      |      | <span data-ttu-id="86f73-189">x</span><span class="sxs-lookup"><span data-stu-id="86f73-189">x</span></span>    | <span data-ttu-id="86f73-190">x</span><span class="sxs-lookup"><span data-stu-id="86f73-190">x</span></span>    | <span data-ttu-id="86f73-191">x</span><span class="sxs-lookup"><span data-stu-id="86f73-191">x</span></span>     | <span data-ttu-id="86f73-192">x</span><span class="sxs-lookup"><span data-stu-id="86f73-192">x</span></span>    | <span data-ttu-id="86f73-193">x</span><span class="sxs-lookup"><span data-stu-id="86f73-193">x</span></span>     |
| <span data-ttu-id="86f73-194">swizzle arbitrário</span><span class="sxs-lookup"><span data-stu-id="86f73-194">arbitrary swizzle</span></span>     |      |      |      |      |      | <span data-ttu-id="86f73-195">x</span><span class="sxs-lookup"><span data-stu-id="86f73-195">x</span></span>    | <span data-ttu-id="86f73-196">x</span><span class="sxs-lookup"><span data-stu-id="86f73-196">x</span></span>     | <span data-ttu-id="86f73-197">x</span><span class="sxs-lookup"><span data-stu-id="86f73-197">x</span></span>    | <span data-ttu-id="86f73-198">x</span><span class="sxs-lookup"><span data-stu-id="86f73-198">x</span></span>     |



 

<span data-ttu-id="86f73-199">\* Disponível somente se a máscara de gravação de destino for. w (. a).</span><span class="sxs-lookup"><span data-stu-id="86f73-199">\* Only available if destination write mask is .w (.a).</span></span>

## <a name="arbitrary-swizzle"></a><span data-ttu-id="86f73-200">Swizzle arbitrário</span><span class="sxs-lookup"><span data-stu-id="86f73-200">Arbitrary Swizzle</span></span>

<span data-ttu-id="86f73-201">Swizzles pode ser aplicado a registros de origem em uma ordem arbitrária; ou seja, qualquer registro de origem pode usar qualquer máscara de componente, em qualquer ordem.</span><span class="sxs-lookup"><span data-stu-id="86f73-201">Swizzles can be applied to source registers in an arbitrary order; that is, any source register can take any component mask, in any order.</span></span>

## <a name="replicate-swizzle"></a><span data-ttu-id="86f73-202">Replicar swizzle</span><span class="sxs-lookup"><span data-stu-id="86f73-202">Replicate Swizzle</span></span>

<span data-ttu-id="86f73-203">Replicate swizzle copia um componente para outro.</span><span class="sxs-lookup"><span data-stu-id="86f73-203">Replicate swizzle copies one component to another.</span></span> <span data-ttu-id="86f73-204">Isso é, exatamente um dos componentes. x,. y,. z,. w swizzle (ou o. r,. g,. b,. equivalentes) deve ser especificado.</span><span class="sxs-lookup"><span data-stu-id="86f73-204">This is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>

## <a name="related-topics"></a><span data-ttu-id="86f73-205">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="86f73-205">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="86f73-206">Modificadores de registro de origem do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="86f73-206">Pixel Shader Source Register Modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> <dt>

[<span data-ttu-id="86f73-207">PS \_ 1 \_ 1 \_ \_ PS \_ 1 \_ 2 PS 1 \_ \_ \_ \_ 3 \_ \_ PS \_ 1 \_ 4 registros</span><span class="sxs-lookup"><span data-stu-id="86f73-207">ps\_1\_1\_\_ps\_1\_2\_\_ps\_1\_3\_\_ps\_1\_4 Registers</span></span>](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)
</dt> <dt>

[<span data-ttu-id="86f73-208">\_registros PS 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="86f73-208">ps\_2\_0 Registers</span></span>](dx9-graphics-reference-asm-ps-registers-ps-2-0.md)
</dt> <dt>

[<span data-ttu-id="86f73-209">\_registros PS 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="86f73-209">ps\_2\_x Registers</span></span>](dx9-graphics-reference-asm-ps-registers-ps-2-x.md)
</dt> <dt>

[<span data-ttu-id="86f73-210">\_registros PS 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="86f73-210">ps\_3\_0 Registers</span></span>](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)
</dt> </dl>

 

 




