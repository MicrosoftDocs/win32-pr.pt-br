---
title: dmul (SM5-ASM)
description: Multiplicação de precisão dupla por componente.
ms.assetid: 53AE27BE-2F4B-4C55-B496-D7122C00DC52
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a5d311cb5c958e8b7403197027c9854d1a93a64
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999083"
---
# <a name="dmul-sm5---asm"></a><span data-ttu-id="42cd5-103">dmul (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="42cd5-103">dmul (sm5 - asm)</span></span>

<span data-ttu-id="42cd5-104">Multiplicação de precisão dupla por componente.</span><span class="sxs-lookup"><span data-stu-id="42cd5-104">Component-wise double-precision multiply.</span></span>



| <span data-ttu-id="42cd5-105">dmul \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="42cd5-105">dmul\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|---------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="42cd5-106">Item</span><span class="sxs-lookup"><span data-stu-id="42cd5-106">Item</span></span>                                                            | <span data-ttu-id="42cd5-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="42cd5-107">Description</span></span>                                                                                        |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42cd5-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="42cd5-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="42cd5-109">\[no \] endereço do resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="42cd5-109">\[in\] The address of the result of the operation.</span></span><br/> <span data-ttu-id="42cd5-110">*dest*  =  *src0* \* *src1*</span><span class="sxs-lookup"><span data-stu-id="42cd5-110">*dest* = *src0* \* *src1*</span></span><br/> |
| <span data-ttu-id="42cd5-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="42cd5-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="42cd5-112">\[nos \] componentes para multiplicar com *src1*.</span><span class="sxs-lookup"><span data-stu-id="42cd5-112">\[in\] The components to multiply with *src1*.</span></span><br/>                                          |
| <span data-ttu-id="42cd5-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="42cd5-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="42cd5-114">\[nos \] componentes para multiplicar com *src0*.</span><span class="sxs-lookup"><span data-stu-id="42cd5-114">\[in\] The components to multiply with *src0*.</span></span><br/>                                          |



 

## <a name="remarks"></a><span data-ttu-id="42cd5-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="42cd5-115">Remarks</span></span>

<span data-ttu-id="42cd5-116">O swizzles válido para os parâmetros de origem são. xyzw,. xyxy,. zwxy,. zwzw.</span><span class="sxs-lookup"><span data-stu-id="42cd5-116">The valid swizzles for the source parameters are .xyzw, .xyxy, .zwxy, .zwzw.</span></span> <span data-ttu-id="42cd5-117">As máscaras de *destino* válidas são. XY,. zw e. xyzw.</span><span class="sxs-lookup"><span data-stu-id="42cd5-117">The valid *dest* masks are .xy, .zw, and .xyzw.</span></span> <span data-ttu-id="42cd5-118">Os seguintes mapeamentos *src* são swizzle:</span><span class="sxs-lookup"><span data-stu-id="42cd5-118">The following *src* mappings are post-swizzle:</span></span>

-   <span data-ttu-id="42cd5-119">*dest* é um vec2 duplo entre (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="42cd5-119">*dest* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="42cd5-120">*src0* é um vec2 duplo entre (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="42cd5-120">*src0* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="42cd5-121">*src1* é um vec2 duplo entre (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="42cd5-121">*src1* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>

<span data-ttu-id="42cd5-122">A tabela a seguir mostra os resultados obtidos ao executar a instrução com várias classes de números, supondo que nenhum estouro ou Subfluxo ocorra.</span><span class="sxs-lookup"><span data-stu-id="42cd5-122">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span>

<span data-ttu-id="42cd5-123">F significa número real finito.</span><span class="sxs-lookup"><span data-stu-id="42cd5-123">F means finite-real number.</span></span>



| <span data-ttu-id="42cd5-124">**src0 src1->**</span><span class="sxs-lookup"><span data-stu-id="42cd5-124">**src0 src1->**</span></span> | <span data-ttu-id="42cd5-125">**-INF**</span><span class="sxs-lookup"><span data-stu-id="42cd5-125">**-inf**</span></span> | <span data-ttu-id="42cd5-126">**-F**</span><span class="sxs-lookup"><span data-stu-id="42cd5-126">**-F**</span></span> | <span data-ttu-id="42cd5-127">**-1,0**</span><span class="sxs-lookup"><span data-stu-id="42cd5-127">**-1.0**</span></span> | <span data-ttu-id="42cd5-128">**-0**</span><span class="sxs-lookup"><span data-stu-id="42cd5-128">**-0**</span></span> | <span data-ttu-id="42cd5-129">**+0**</span><span class="sxs-lookup"><span data-stu-id="42cd5-129">**+0**</span></span> | <span data-ttu-id="42cd5-130">**+ 1,0**</span><span class="sxs-lookup"><span data-stu-id="42cd5-130">**+1.0**</span></span> | <span data-ttu-id="42cd5-131">**+ F**</span><span class="sxs-lookup"><span data-stu-id="42cd5-131">**+F**</span></span> | <span data-ttu-id="42cd5-132">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="42cd5-132">**+inf**</span></span> | <span data-ttu-id="42cd5-133">**NaN**</span><span class="sxs-lookup"><span data-stu-id="42cd5-133">**NaN**</span></span> |
|--------------------|----------|--------|----------|--------|--------|----------|--------|----------|---------|
| <span data-ttu-id="42cd5-134">**-INF**</span><span class="sxs-lookup"><span data-stu-id="42cd5-134">**-inf**</span></span>           | <span data-ttu-id="42cd5-135">+inf</span><span class="sxs-lookup"><span data-stu-id="42cd5-135">+inf</span></span>     | <span data-ttu-id="42cd5-136">+inf</span><span class="sxs-lookup"><span data-stu-id="42cd5-136">+inf</span></span>   | <span data-ttu-id="42cd5-137">+inf</span><span class="sxs-lookup"><span data-stu-id="42cd5-137">+inf</span></span>     | <span data-ttu-id="42cd5-138">NaN</span><span class="sxs-lookup"><span data-stu-id="42cd5-138">NaN</span></span>    | <span data-ttu-id="42cd5-139">NaN</span><span class="sxs-lookup"><span data-stu-id="42cd5-139">NaN</span></span>    | <span data-ttu-id="42cd5-140">-inf</span><span class="sxs-lookup"><span data-stu-id="42cd5-140">-inf</span></span>     | <span data-ttu-id="42cd5-141">-inf</span><span class="sxs-lookup"><span data-stu-id="42cd5-141">-inf</span></span>   | <span data-ttu-id="42cd5-142">-inf</span><span class="sxs-lookup"><span data-stu-id="42cd5-142">-inf</span></span>     | <span data-ttu-id="42cd5-143">NaN</span><span class="sxs-lookup"><span data-stu-id="42cd5-143">NaN</span></span>     |
| <span data-ttu-id="42cd5-144">**-F**</span><span class="sxs-lookup"><span data-stu-id="42cd5-144">**-F**</span></span>             | <span data-ttu-id="42cd5-145">+inf</span><span class="sxs-lookup"><span data-stu-id="42cd5-145">+inf</span></span>     | <span data-ttu-id="42cd5-146">+ F</span><span class="sxs-lookup"><span data-stu-id="42cd5-146">+F</span></span>     | <span data-ttu-id="42cd5-147">-src0</span><span class="sxs-lookup"><span data-stu-id="42cd5-147">-src0</span></span>    | <span data-ttu-id="42cd5-148">+0</span><span class="sxs-lookup"><span data-stu-id="42cd5-148">+0</span></span>     | <span data-ttu-id="42cd5-149">-0</span><span class="sxs-lookup"><span data-stu-id="42cd5-149">-0</span></span>     | <span data-ttu-id="42cd5-150">src0</span><span class="sxs-lookup"><span data-stu-id="42cd5-150">src0</span></span>     | <span data-ttu-id="42cd5-151">-F</span><span class="sxs-lookup"><span data-stu-id="42cd5-151">-F</span></span>     | <span data-ttu-id="42cd5-152">-inf</span><span class="sxs-lookup"><span data-stu-id="42cd5-152">-inf</span></span>     | <span data-ttu-id="42cd5-153">NaN</span><span class="sxs-lookup"><span data-stu-id="42cd5-153">NaN</span></span>     |
| <span data-ttu-id="42cd5-154">**-1,0 f**</span><span class="sxs-lookup"><span data-stu-id="42cd5-154">**-1.0F**</span></span>          | <span data-ttu-id="42cd5-155">+inf</span><span class="sxs-lookup"><span data-stu-id="42cd5-155">+inf</span></span>     | <span data-ttu-id="42cd5-156">-src1</span><span class="sxs-lookup"><span data-stu-id="42cd5-156">-src1</span></span>  | <span data-ttu-id="42cd5-157">+ 1,0</span><span class="sxs-lookup"><span data-stu-id="42cd5-157">+1.0</span></span>     | <span data-ttu-id="42cd5-158">+0</span><span class="sxs-lookup"><span data-stu-id="42cd5-158">+0</span></span>     | <span data-ttu-id="42cd5-159">-0</span><span class="sxs-lookup"><span data-stu-id="42cd5-159">-0</span></span>     | <span data-ttu-id="42cd5-160">-1,0</span><span class="sxs-lookup"><span data-stu-id="42cd5-160">-1.0</span></span>     | <span data-ttu-id="42cd5-161">-src1</span><span class="sxs-lookup"><span data-stu-id="42cd5-161">-src1</span></span>  | <span data-ttu-id="42cd5-162">-inf</span><span class="sxs-lookup"><span data-stu-id="42cd5-162">-inf</span></span>     | <span data-ttu-id="42cd5-163">NaN</span><span class="sxs-lookup"><span data-stu-id="42cd5-163">NaN</span></span>     |
| <span data-ttu-id="42cd5-164">**-0**</span><span class="sxs-lookup"><span data-stu-id="42cd5-164">**-0**</span></span>             | <span data-ttu-id="42cd5-165">NaN</span><span class="sxs-lookup"><span data-stu-id="42cd5-165">NaN</span></span>      | <span data-ttu-id="42cd5-166">+0</span><span class="sxs-lookup"><span data-stu-id="42cd5-166">+0</span></span>     | <span data-ttu-id="42cd5-167">+0</span><span class="sxs-lookup"><span data-stu-id="42cd5-167">+0</span></span>       | <span data-ttu-id="42cd5-168">+0</span><span class="sxs-lookup"><span data-stu-id="42cd5-168">+0</span></span>     | <span data-ttu-id="42cd5-169">-0</span><span class="sxs-lookup"><span data-stu-id="42cd5-169">-0</span></span>     | <span data-ttu-id="42cd5-170">-0</span><span class="sxs-lookup"><span data-stu-id="42cd5-170">-0</span></span>       | <span data-ttu-id="42cd5-171">-0</span><span class="sxs-lookup"><span data-stu-id="42cd5-171">-0</span></span>     | <span data-ttu-id="42cd5-172">NaN</span><span class="sxs-lookup"><span data-stu-id="42cd5-172">NaN</span></span>      | <span data-ttu-id="42cd5-173">NaN</span><span class="sxs-lookup"><span data-stu-id="42cd5-173">NaN</span></span>     |
| <span data-ttu-id="42cd5-174">**+0**</span><span class="sxs-lookup"><span data-stu-id="42cd5-174">**+0**</span></span>             | <span data-ttu-id="42cd5-175">NaN</span><span class="sxs-lookup"><span data-stu-id="42cd5-175">NaN</span></span>      | <span data-ttu-id="42cd5-176">-0</span><span class="sxs-lookup"><span data-stu-id="42cd5-176">-0</span></span>     | <span data-ttu-id="42cd5-177">-0</span><span class="sxs-lookup"><span data-stu-id="42cd5-177">-0</span></span>       | <span data-ttu-id="42cd5-178">-0</span><span class="sxs-lookup"><span data-stu-id="42cd5-178">-0</span></span>     | <span data-ttu-id="42cd5-179">+0</span><span class="sxs-lookup"><span data-stu-id="42cd5-179">+0</span></span>     | <span data-ttu-id="42cd5-180">+0</span><span class="sxs-lookup"><span data-stu-id="42cd5-180">+0</span></span>       | <span data-ttu-id="42cd5-181">+0</span><span class="sxs-lookup"><span data-stu-id="42cd5-181">+0</span></span>     | <span data-ttu-id="42cd5-182">NaN</span><span class="sxs-lookup"><span data-stu-id="42cd5-182">NaN</span></span>      | <span data-ttu-id="42cd5-183">NaN</span><span class="sxs-lookup"><span data-stu-id="42cd5-183">NaN</span></span>     |
| <span data-ttu-id="42cd5-184">**+ 1,0**</span><span class="sxs-lookup"><span data-stu-id="42cd5-184">**+1.0**</span></span>           | <span data-ttu-id="42cd5-185">-inf</span><span class="sxs-lookup"><span data-stu-id="42cd5-185">-inf</span></span>     | <span data-ttu-id="42cd5-186">src1</span><span class="sxs-lookup"><span data-stu-id="42cd5-186">src1</span></span>   | <span data-ttu-id="42cd5-187">-1,0</span><span class="sxs-lookup"><span data-stu-id="42cd5-187">-1.0</span></span>     | <span data-ttu-id="42cd5-188">-0</span><span class="sxs-lookup"><span data-stu-id="42cd5-188">-0</span></span>     | <span data-ttu-id="42cd5-189">+0</span><span class="sxs-lookup"><span data-stu-id="42cd5-189">+0</span></span>     | <span data-ttu-id="42cd5-190">+1</span><span class="sxs-lookup"><span data-stu-id="42cd5-190">+1</span></span>       | <span data-ttu-id="42cd5-191">src1</span><span class="sxs-lookup"><span data-stu-id="42cd5-191">src1</span></span>   | <span data-ttu-id="42cd5-192">+inf</span><span class="sxs-lookup"><span data-stu-id="42cd5-192">+inf</span></span>     | <span data-ttu-id="42cd5-193">NaN</span><span class="sxs-lookup"><span data-stu-id="42cd5-193">NaN</span></span>     |
| <span data-ttu-id="42cd5-194">**+ F**</span><span class="sxs-lookup"><span data-stu-id="42cd5-194">**+F**</span></span>             | <span data-ttu-id="42cd5-195">-inf</span><span class="sxs-lookup"><span data-stu-id="42cd5-195">-inf</span></span>     | <span data-ttu-id="42cd5-196">-F</span><span class="sxs-lookup"><span data-stu-id="42cd5-196">-F</span></span>     | <span data-ttu-id="42cd5-197">-src0</span><span class="sxs-lookup"><span data-stu-id="42cd5-197">-src0</span></span>    | <span data-ttu-id="42cd5-198">-0</span><span class="sxs-lookup"><span data-stu-id="42cd5-198">-0</span></span>     | <span data-ttu-id="42cd5-199">+0</span><span class="sxs-lookup"><span data-stu-id="42cd5-199">+0</span></span>     | <span data-ttu-id="42cd5-200">src0</span><span class="sxs-lookup"><span data-stu-id="42cd5-200">src0</span></span>     | <span data-ttu-id="42cd5-201">+ F</span><span class="sxs-lookup"><span data-stu-id="42cd5-201">+F</span></span>     | <span data-ttu-id="42cd5-202">+inf</span><span class="sxs-lookup"><span data-stu-id="42cd5-202">+inf</span></span>     | <span data-ttu-id="42cd5-203">NaN</span><span class="sxs-lookup"><span data-stu-id="42cd5-203">NaN</span></span>     |
| <span data-ttu-id="42cd5-204">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="42cd5-204">**+inf**</span></span>           | <span data-ttu-id="42cd5-205">-inf</span><span class="sxs-lookup"><span data-stu-id="42cd5-205">-inf</span></span>     | <span data-ttu-id="42cd5-206">-inf</span><span class="sxs-lookup"><span data-stu-id="42cd5-206">-inf</span></span>   | <span data-ttu-id="42cd5-207">-inf</span><span class="sxs-lookup"><span data-stu-id="42cd5-207">-inf</span></span>     | <span data-ttu-id="42cd5-208">NaN</span><span class="sxs-lookup"><span data-stu-id="42cd5-208">NaN</span></span>    | <span data-ttu-id="42cd5-209">NaN</span><span class="sxs-lookup"><span data-stu-id="42cd5-209">NaN</span></span>    | <span data-ttu-id="42cd5-210">+inf</span><span class="sxs-lookup"><span data-stu-id="42cd5-210">+inf</span></span>     | <span data-ttu-id="42cd5-211">+inf</span><span class="sxs-lookup"><span data-stu-id="42cd5-211">+inf</span></span>   | <span data-ttu-id="42cd5-212">+inf</span><span class="sxs-lookup"><span data-stu-id="42cd5-212">+inf</span></span>     | <span data-ttu-id="42cd5-213">NaN</span><span class="sxs-lookup"><span data-stu-id="42cd5-213">NaN</span></span>     |
| <span data-ttu-id="42cd5-214">**NaN**</span><span class="sxs-lookup"><span data-stu-id="42cd5-214">**NaN**</span></span>            | <span data-ttu-id="42cd5-215">NaN</span><span class="sxs-lookup"><span data-stu-id="42cd5-215">NaN</span></span>      | <span data-ttu-id="42cd5-216">NaN</span><span class="sxs-lookup"><span data-stu-id="42cd5-216">NaN</span></span>    | <span data-ttu-id="42cd5-217">NaN</span><span class="sxs-lookup"><span data-stu-id="42cd5-217">NaN</span></span>      | <span data-ttu-id="42cd5-218">NaN</span><span class="sxs-lookup"><span data-stu-id="42cd5-218">NaN</span></span>    | <span data-ttu-id="42cd5-219">NaN</span><span class="sxs-lookup"><span data-stu-id="42cd5-219">NaN</span></span>    | <span data-ttu-id="42cd5-220">NaN</span><span class="sxs-lookup"><span data-stu-id="42cd5-220">NaN</span></span>      | <span data-ttu-id="42cd5-221">NaN</span><span class="sxs-lookup"><span data-stu-id="42cd5-221">NaN</span></span>    | <span data-ttu-id="42cd5-222">NaN</span><span class="sxs-lookup"><span data-stu-id="42cd5-222">NaN</span></span>      | <span data-ttu-id="42cd5-223">NaN</span><span class="sxs-lookup"><span data-stu-id="42cd5-223">NaN</span></span>     |



 

<span data-ttu-id="42cd5-224">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="42cd5-224">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="42cd5-225">Vértice</span><span class="sxs-lookup"><span data-stu-id="42cd5-225">Vertex</span></span> | <span data-ttu-id="42cd5-226">Envoltória</span><span class="sxs-lookup"><span data-stu-id="42cd5-226">Hull</span></span> | <span data-ttu-id="42cd5-227">Domain</span><span class="sxs-lookup"><span data-stu-id="42cd5-227">Domain</span></span> | <span data-ttu-id="42cd5-228">Geometria</span><span class="sxs-lookup"><span data-stu-id="42cd5-228">Geometry</span></span> | <span data-ttu-id="42cd5-229">16x16</span><span class="sxs-lookup"><span data-stu-id="42cd5-229">Pixel</span></span> | <span data-ttu-id="42cd5-230">Computação</span><span class="sxs-lookup"><span data-stu-id="42cd5-230">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="42cd5-231">X</span><span class="sxs-lookup"><span data-stu-id="42cd5-231">X</span></span>      | <span data-ttu-id="42cd5-232">X</span><span class="sxs-lookup"><span data-stu-id="42cd5-232">X</span></span>    | <span data-ttu-id="42cd5-233">X</span><span class="sxs-lookup"><span data-stu-id="42cd5-233">X</span></span>      | <span data-ttu-id="42cd5-234">X</span><span class="sxs-lookup"><span data-stu-id="42cd5-234">X</span></span>        | <span data-ttu-id="42cd5-235">X</span><span class="sxs-lookup"><span data-stu-id="42cd5-235">X</span></span>     | <span data-ttu-id="42cd5-236">X</span><span class="sxs-lookup"><span data-stu-id="42cd5-236">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="42cd5-237">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="42cd5-237">Minimum Shader Model</span></span>

<span data-ttu-id="42cd5-238">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="42cd5-238">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="42cd5-239">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="42cd5-239">Shader Model</span></span>                                              | <span data-ttu-id="42cd5-240">Suportado</span><span class="sxs-lookup"><span data-stu-id="42cd5-240">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="42cd5-241">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="42cd5-241">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="42cd5-242">sim</span><span class="sxs-lookup"><span data-stu-id="42cd5-242">yes</span></span>       |
| [<span data-ttu-id="42cd5-243">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="42cd5-243">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="42cd5-244">não</span><span class="sxs-lookup"><span data-stu-id="42cd5-244">no</span></span>        |
| [<span data-ttu-id="42cd5-245">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="42cd5-245">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="42cd5-246">não</span><span class="sxs-lookup"><span data-stu-id="42cd5-246">no</span></span>        |
| [<span data-ttu-id="42cd5-247">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="42cd5-247">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="42cd5-248">não</span><span class="sxs-lookup"><span data-stu-id="42cd5-248">no</span></span>        |
| [<span data-ttu-id="42cd5-249">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="42cd5-249">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="42cd5-250">não</span><span class="sxs-lookup"><span data-stu-id="42cd5-250">no</span></span>        |
| [<span data-ttu-id="42cd5-251">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="42cd5-251">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="42cd5-252">não</span><span class="sxs-lookup"><span data-stu-id="42cd5-252">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="42cd5-253">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="42cd5-253">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="42cd5-254">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="42cd5-254">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





