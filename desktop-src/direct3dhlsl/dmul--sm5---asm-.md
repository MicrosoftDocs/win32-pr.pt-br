---
title: dmul (SM5-ASM)
description: Multiplicação de precisão dupla por componente.
ms.assetid: 53AE27BE-2F4B-4C55-B496-D7122C00DC52
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18cce59ae237610b1038d90e02dff429812b4f00
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104988576"
---
# <a name="dmul-sm5---asm"></a><span data-ttu-id="61fd1-103">dmul (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="61fd1-103">dmul (sm5 - asm)</span></span>

<span data-ttu-id="61fd1-104">Multiplicação de precisão dupla por componente.</span><span class="sxs-lookup"><span data-stu-id="61fd1-104">Component-wise double-precision multiply.</span></span>



| <span data-ttu-id="61fd1-105">dmul \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="61fd1-105">dmul\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|---------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="61fd1-106">Item</span><span class="sxs-lookup"><span data-stu-id="61fd1-106">Item</span></span>                                                            | <span data-ttu-id="61fd1-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="61fd1-107">Description</span></span>                                                                                        |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61fd1-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="61fd1-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="61fd1-109">\[no \] endereço do resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="61fd1-109">\[in\] The address of the result of the operation.</span></span><br/> <span data-ttu-id="61fd1-110">*dest*  =  *src0* \* *src1*</span><span class="sxs-lookup"><span data-stu-id="61fd1-110">*dest* = *src0* \* *src1*</span></span><br/> |
| <span data-ttu-id="61fd1-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="61fd1-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="61fd1-112">\[nos \] componentes para multiplicar com *src1*.</span><span class="sxs-lookup"><span data-stu-id="61fd1-112">\[in\] The components to multiply with *src1*.</span></span><br/>                                          |
| <span data-ttu-id="61fd1-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="61fd1-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="61fd1-114">\[nos \] componentes para multiplicar com *src0*.</span><span class="sxs-lookup"><span data-stu-id="61fd1-114">\[in\] The components to multiply with *src0*.</span></span><br/>                                          |



 

## <a name="remarks"></a><span data-ttu-id="61fd1-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="61fd1-115">Remarks</span></span>

<span data-ttu-id="61fd1-116">O swizzles válido para os parâmetros de origem são. xyzw,. xyxy,. zwxy,. zwzw.</span><span class="sxs-lookup"><span data-stu-id="61fd1-116">The valid swizzles for the source parameters are .xyzw, .xyxy, .zwxy, .zwzw.</span></span> <span data-ttu-id="61fd1-117">As máscaras de *destino* válidas são. XY,. zw e. xyzw.</span><span class="sxs-lookup"><span data-stu-id="61fd1-117">The valid *dest* masks are .xy, .zw, and .xyzw.</span></span> <span data-ttu-id="61fd1-118">Os seguintes mapeamentos *src* são swizzle:</span><span class="sxs-lookup"><span data-stu-id="61fd1-118">The following *src* mappings are post-swizzle:</span></span>

-   <span data-ttu-id="61fd1-119">*dest* é um vec2 duplo entre (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="61fd1-119">*dest* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="61fd1-120">*src0* é um vec2 duplo entre (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="61fd1-120">*src0* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="61fd1-121">*src1* é um vec2 duplo entre (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="61fd1-121">*src1* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>

<span data-ttu-id="61fd1-122">A tabela a seguir mostra os resultados obtidos ao executar a instrução com várias classes de números, supondo que nenhum estouro ou Subfluxo ocorra.</span><span class="sxs-lookup"><span data-stu-id="61fd1-122">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span>

<span data-ttu-id="61fd1-123">F significa número real finito.</span><span class="sxs-lookup"><span data-stu-id="61fd1-123">F means finite-real number.</span></span>



|                    |          |        |          |        |        |          |        |          |         |
|--------------------|----------|--------|----------|--------|--------|----------|--------|----------|---------|
| <span data-ttu-id="61fd1-124">**src0 src1->**</span><span class="sxs-lookup"><span data-stu-id="61fd1-124">**src0 src1->**</span></span> | <span data-ttu-id="61fd1-125">**-INF**</span><span class="sxs-lookup"><span data-stu-id="61fd1-125">**-inf**</span></span> | <span data-ttu-id="61fd1-126">**-F**</span><span class="sxs-lookup"><span data-stu-id="61fd1-126">**-F**</span></span> | <span data-ttu-id="61fd1-127">**-1,0**</span><span class="sxs-lookup"><span data-stu-id="61fd1-127">**-1.0**</span></span> | <span data-ttu-id="61fd1-128">**-0**</span><span class="sxs-lookup"><span data-stu-id="61fd1-128">**-0**</span></span> | <span data-ttu-id="61fd1-129">**+0**</span><span class="sxs-lookup"><span data-stu-id="61fd1-129">**+0**</span></span> | <span data-ttu-id="61fd1-130">**+ 1,0**</span><span class="sxs-lookup"><span data-stu-id="61fd1-130">**+1.0**</span></span> | <span data-ttu-id="61fd1-131">**+ F**</span><span class="sxs-lookup"><span data-stu-id="61fd1-131">**+F**</span></span> | <span data-ttu-id="61fd1-132">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="61fd1-132">**+inf**</span></span> | <span data-ttu-id="61fd1-133">**NaN**</span><span class="sxs-lookup"><span data-stu-id="61fd1-133">**NaN**</span></span> |
| <span data-ttu-id="61fd1-134">**-INF**</span><span class="sxs-lookup"><span data-stu-id="61fd1-134">**-inf**</span></span>           | <span data-ttu-id="61fd1-135">+inf</span><span class="sxs-lookup"><span data-stu-id="61fd1-135">+inf</span></span>     | <span data-ttu-id="61fd1-136">+inf</span><span class="sxs-lookup"><span data-stu-id="61fd1-136">+inf</span></span>   | <span data-ttu-id="61fd1-137">+inf</span><span class="sxs-lookup"><span data-stu-id="61fd1-137">+inf</span></span>     | <span data-ttu-id="61fd1-138">NaN</span><span class="sxs-lookup"><span data-stu-id="61fd1-138">NaN</span></span>    | <span data-ttu-id="61fd1-139">NaN</span><span class="sxs-lookup"><span data-stu-id="61fd1-139">NaN</span></span>    | <span data-ttu-id="61fd1-140">-inf</span><span class="sxs-lookup"><span data-stu-id="61fd1-140">-inf</span></span>     | <span data-ttu-id="61fd1-141">-inf</span><span class="sxs-lookup"><span data-stu-id="61fd1-141">-inf</span></span>   | <span data-ttu-id="61fd1-142">-inf</span><span class="sxs-lookup"><span data-stu-id="61fd1-142">-inf</span></span>     | <span data-ttu-id="61fd1-143">NaN</span><span class="sxs-lookup"><span data-stu-id="61fd1-143">NaN</span></span>     |
| <span data-ttu-id="61fd1-144">**-F**</span><span class="sxs-lookup"><span data-stu-id="61fd1-144">**-F**</span></span>             | <span data-ttu-id="61fd1-145">+inf</span><span class="sxs-lookup"><span data-stu-id="61fd1-145">+inf</span></span>     | <span data-ttu-id="61fd1-146">+ F</span><span class="sxs-lookup"><span data-stu-id="61fd1-146">+F</span></span>     | <span data-ttu-id="61fd1-147">-src0</span><span class="sxs-lookup"><span data-stu-id="61fd1-147">-src0</span></span>    | <span data-ttu-id="61fd1-148">+0</span><span class="sxs-lookup"><span data-stu-id="61fd1-148">+0</span></span>     | <span data-ttu-id="61fd1-149">-0</span><span class="sxs-lookup"><span data-stu-id="61fd1-149">-0</span></span>     | <span data-ttu-id="61fd1-150">src0</span><span class="sxs-lookup"><span data-stu-id="61fd1-150">src0</span></span>     | <span data-ttu-id="61fd1-151">-F</span><span class="sxs-lookup"><span data-stu-id="61fd1-151">-F</span></span>     | <span data-ttu-id="61fd1-152">-inf</span><span class="sxs-lookup"><span data-stu-id="61fd1-152">-inf</span></span>     | <span data-ttu-id="61fd1-153">NaN</span><span class="sxs-lookup"><span data-stu-id="61fd1-153">NaN</span></span>     |
| <span data-ttu-id="61fd1-154">**-1,0 f**</span><span class="sxs-lookup"><span data-stu-id="61fd1-154">**-1.0F**</span></span>          | <span data-ttu-id="61fd1-155">+inf</span><span class="sxs-lookup"><span data-stu-id="61fd1-155">+inf</span></span>     | <span data-ttu-id="61fd1-156">-src1</span><span class="sxs-lookup"><span data-stu-id="61fd1-156">-src1</span></span>  | <span data-ttu-id="61fd1-157">+ 1,0</span><span class="sxs-lookup"><span data-stu-id="61fd1-157">+1.0</span></span>     | <span data-ttu-id="61fd1-158">+0</span><span class="sxs-lookup"><span data-stu-id="61fd1-158">+0</span></span>     | <span data-ttu-id="61fd1-159">-0</span><span class="sxs-lookup"><span data-stu-id="61fd1-159">-0</span></span>     | <span data-ttu-id="61fd1-160">-1,0</span><span class="sxs-lookup"><span data-stu-id="61fd1-160">-1.0</span></span>     | <span data-ttu-id="61fd1-161">-src1</span><span class="sxs-lookup"><span data-stu-id="61fd1-161">-src1</span></span>  | <span data-ttu-id="61fd1-162">-inf</span><span class="sxs-lookup"><span data-stu-id="61fd1-162">-inf</span></span>     | <span data-ttu-id="61fd1-163">NaN</span><span class="sxs-lookup"><span data-stu-id="61fd1-163">NaN</span></span>     |
| <span data-ttu-id="61fd1-164">**-0**</span><span class="sxs-lookup"><span data-stu-id="61fd1-164">**-0**</span></span>             | <span data-ttu-id="61fd1-165">NaN</span><span class="sxs-lookup"><span data-stu-id="61fd1-165">NaN</span></span>      | <span data-ttu-id="61fd1-166">+0</span><span class="sxs-lookup"><span data-stu-id="61fd1-166">+0</span></span>     | <span data-ttu-id="61fd1-167">+0</span><span class="sxs-lookup"><span data-stu-id="61fd1-167">+0</span></span>       | <span data-ttu-id="61fd1-168">+0</span><span class="sxs-lookup"><span data-stu-id="61fd1-168">+0</span></span>     | <span data-ttu-id="61fd1-169">-0</span><span class="sxs-lookup"><span data-stu-id="61fd1-169">-0</span></span>     | <span data-ttu-id="61fd1-170">-0</span><span class="sxs-lookup"><span data-stu-id="61fd1-170">-0</span></span>       | <span data-ttu-id="61fd1-171">-0</span><span class="sxs-lookup"><span data-stu-id="61fd1-171">-0</span></span>     | <span data-ttu-id="61fd1-172">NaN</span><span class="sxs-lookup"><span data-stu-id="61fd1-172">NaN</span></span>      | <span data-ttu-id="61fd1-173">NaN</span><span class="sxs-lookup"><span data-stu-id="61fd1-173">NaN</span></span>     |
| <span data-ttu-id="61fd1-174">**+0**</span><span class="sxs-lookup"><span data-stu-id="61fd1-174">**+0**</span></span>             | <span data-ttu-id="61fd1-175">NaN</span><span class="sxs-lookup"><span data-stu-id="61fd1-175">NaN</span></span>      | <span data-ttu-id="61fd1-176">-0</span><span class="sxs-lookup"><span data-stu-id="61fd1-176">-0</span></span>     | <span data-ttu-id="61fd1-177">-0</span><span class="sxs-lookup"><span data-stu-id="61fd1-177">-0</span></span>       | <span data-ttu-id="61fd1-178">-0</span><span class="sxs-lookup"><span data-stu-id="61fd1-178">-0</span></span>     | <span data-ttu-id="61fd1-179">+0</span><span class="sxs-lookup"><span data-stu-id="61fd1-179">+0</span></span>     | <span data-ttu-id="61fd1-180">+0</span><span class="sxs-lookup"><span data-stu-id="61fd1-180">+0</span></span>       | <span data-ttu-id="61fd1-181">+0</span><span class="sxs-lookup"><span data-stu-id="61fd1-181">+0</span></span>     | <span data-ttu-id="61fd1-182">NaN</span><span class="sxs-lookup"><span data-stu-id="61fd1-182">NaN</span></span>      | <span data-ttu-id="61fd1-183">NaN</span><span class="sxs-lookup"><span data-stu-id="61fd1-183">NaN</span></span>     |
| <span data-ttu-id="61fd1-184">**+ 1,0**</span><span class="sxs-lookup"><span data-stu-id="61fd1-184">**+1.0**</span></span>           | <span data-ttu-id="61fd1-185">-inf</span><span class="sxs-lookup"><span data-stu-id="61fd1-185">-inf</span></span>     | <span data-ttu-id="61fd1-186">src1</span><span class="sxs-lookup"><span data-stu-id="61fd1-186">src1</span></span>   | <span data-ttu-id="61fd1-187">-1,0</span><span class="sxs-lookup"><span data-stu-id="61fd1-187">-1.0</span></span>     | <span data-ttu-id="61fd1-188">-0</span><span class="sxs-lookup"><span data-stu-id="61fd1-188">-0</span></span>     | <span data-ttu-id="61fd1-189">+0</span><span class="sxs-lookup"><span data-stu-id="61fd1-189">+0</span></span>     | <span data-ttu-id="61fd1-190">+1</span><span class="sxs-lookup"><span data-stu-id="61fd1-190">+1</span></span>       | <span data-ttu-id="61fd1-191">src1</span><span class="sxs-lookup"><span data-stu-id="61fd1-191">src1</span></span>   | <span data-ttu-id="61fd1-192">+inf</span><span class="sxs-lookup"><span data-stu-id="61fd1-192">+inf</span></span>     | <span data-ttu-id="61fd1-193">NaN</span><span class="sxs-lookup"><span data-stu-id="61fd1-193">NaN</span></span>     |
| <span data-ttu-id="61fd1-194">**+ F**</span><span class="sxs-lookup"><span data-stu-id="61fd1-194">**+F**</span></span>             | <span data-ttu-id="61fd1-195">-inf</span><span class="sxs-lookup"><span data-stu-id="61fd1-195">-inf</span></span>     | <span data-ttu-id="61fd1-196">-F</span><span class="sxs-lookup"><span data-stu-id="61fd1-196">-F</span></span>     | <span data-ttu-id="61fd1-197">-src0</span><span class="sxs-lookup"><span data-stu-id="61fd1-197">-src0</span></span>    | <span data-ttu-id="61fd1-198">-0</span><span class="sxs-lookup"><span data-stu-id="61fd1-198">-0</span></span>     | <span data-ttu-id="61fd1-199">+0</span><span class="sxs-lookup"><span data-stu-id="61fd1-199">+0</span></span>     | <span data-ttu-id="61fd1-200">src0</span><span class="sxs-lookup"><span data-stu-id="61fd1-200">src0</span></span>     | <span data-ttu-id="61fd1-201">+ F</span><span class="sxs-lookup"><span data-stu-id="61fd1-201">+F</span></span>     | <span data-ttu-id="61fd1-202">+inf</span><span class="sxs-lookup"><span data-stu-id="61fd1-202">+inf</span></span>     | <span data-ttu-id="61fd1-203">NaN</span><span class="sxs-lookup"><span data-stu-id="61fd1-203">NaN</span></span>     |
| <span data-ttu-id="61fd1-204">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="61fd1-204">**+inf**</span></span>           | <span data-ttu-id="61fd1-205">-inf</span><span class="sxs-lookup"><span data-stu-id="61fd1-205">-inf</span></span>     | <span data-ttu-id="61fd1-206">-inf</span><span class="sxs-lookup"><span data-stu-id="61fd1-206">-inf</span></span>   | <span data-ttu-id="61fd1-207">-inf</span><span class="sxs-lookup"><span data-stu-id="61fd1-207">-inf</span></span>     | <span data-ttu-id="61fd1-208">NaN</span><span class="sxs-lookup"><span data-stu-id="61fd1-208">NaN</span></span>    | <span data-ttu-id="61fd1-209">NaN</span><span class="sxs-lookup"><span data-stu-id="61fd1-209">NaN</span></span>    | <span data-ttu-id="61fd1-210">+inf</span><span class="sxs-lookup"><span data-stu-id="61fd1-210">+inf</span></span>     | <span data-ttu-id="61fd1-211">+inf</span><span class="sxs-lookup"><span data-stu-id="61fd1-211">+inf</span></span>   | <span data-ttu-id="61fd1-212">+inf</span><span class="sxs-lookup"><span data-stu-id="61fd1-212">+inf</span></span>     | <span data-ttu-id="61fd1-213">NaN</span><span class="sxs-lookup"><span data-stu-id="61fd1-213">NaN</span></span>     |
| <span data-ttu-id="61fd1-214">**NaN**</span><span class="sxs-lookup"><span data-stu-id="61fd1-214">**NaN**</span></span>            | <span data-ttu-id="61fd1-215">NaN</span><span class="sxs-lookup"><span data-stu-id="61fd1-215">NaN</span></span>      | <span data-ttu-id="61fd1-216">NaN</span><span class="sxs-lookup"><span data-stu-id="61fd1-216">NaN</span></span>    | <span data-ttu-id="61fd1-217">NaN</span><span class="sxs-lookup"><span data-stu-id="61fd1-217">NaN</span></span>      | <span data-ttu-id="61fd1-218">NaN</span><span class="sxs-lookup"><span data-stu-id="61fd1-218">NaN</span></span>    | <span data-ttu-id="61fd1-219">NaN</span><span class="sxs-lookup"><span data-stu-id="61fd1-219">NaN</span></span>    | <span data-ttu-id="61fd1-220">NaN</span><span class="sxs-lookup"><span data-stu-id="61fd1-220">NaN</span></span>      | <span data-ttu-id="61fd1-221">NaN</span><span class="sxs-lookup"><span data-stu-id="61fd1-221">NaN</span></span>    | <span data-ttu-id="61fd1-222">NaN</span><span class="sxs-lookup"><span data-stu-id="61fd1-222">NaN</span></span>      | <span data-ttu-id="61fd1-223">NaN</span><span class="sxs-lookup"><span data-stu-id="61fd1-223">NaN</span></span>     |



 

<span data-ttu-id="61fd1-224">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="61fd1-224">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="61fd1-225">Vértice</span><span class="sxs-lookup"><span data-stu-id="61fd1-225">Vertex</span></span> | <span data-ttu-id="61fd1-226">Envoltória</span><span class="sxs-lookup"><span data-stu-id="61fd1-226">Hull</span></span> | <span data-ttu-id="61fd1-227">Domínio</span><span class="sxs-lookup"><span data-stu-id="61fd1-227">Domain</span></span> | <span data-ttu-id="61fd1-228">Geometria</span><span class="sxs-lookup"><span data-stu-id="61fd1-228">Geometry</span></span> | <span data-ttu-id="61fd1-229">16x16</span><span class="sxs-lookup"><span data-stu-id="61fd1-229">Pixel</span></span> | <span data-ttu-id="61fd1-230">Computação</span><span class="sxs-lookup"><span data-stu-id="61fd1-230">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="61fd1-231">X</span><span class="sxs-lookup"><span data-stu-id="61fd1-231">X</span></span>      | <span data-ttu-id="61fd1-232">X</span><span class="sxs-lookup"><span data-stu-id="61fd1-232">X</span></span>    | <span data-ttu-id="61fd1-233">X</span><span class="sxs-lookup"><span data-stu-id="61fd1-233">X</span></span>      | <span data-ttu-id="61fd1-234">X</span><span class="sxs-lookup"><span data-stu-id="61fd1-234">X</span></span>        | <span data-ttu-id="61fd1-235">X</span><span class="sxs-lookup"><span data-stu-id="61fd1-235">X</span></span>     | <span data-ttu-id="61fd1-236">X</span><span class="sxs-lookup"><span data-stu-id="61fd1-236">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="61fd1-237">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="61fd1-237">Minimum Shader Model</span></span>

<span data-ttu-id="61fd1-238">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="61fd1-238">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="61fd1-239">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="61fd1-239">Shader Model</span></span>                                              | <span data-ttu-id="61fd1-240">Com suporte</span><span class="sxs-lookup"><span data-stu-id="61fd1-240">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="61fd1-241">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="61fd1-241">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="61fd1-242">sim</span><span class="sxs-lookup"><span data-stu-id="61fd1-242">yes</span></span>       |
| [<span data-ttu-id="61fd1-243">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="61fd1-243">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="61fd1-244">não</span><span class="sxs-lookup"><span data-stu-id="61fd1-244">no</span></span>        |
| [<span data-ttu-id="61fd1-245">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="61fd1-245">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="61fd1-246">não</span><span class="sxs-lookup"><span data-stu-id="61fd1-246">no</span></span>        |
| [<span data-ttu-id="61fd1-247">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="61fd1-247">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="61fd1-248">não</span><span class="sxs-lookup"><span data-stu-id="61fd1-248">no</span></span>        |
| [<span data-ttu-id="61fd1-249">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="61fd1-249">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="61fd1-250">não</span><span class="sxs-lookup"><span data-stu-id="61fd1-250">no</span></span>        |
| [<span data-ttu-id="61fd1-251">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="61fd1-251">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="61fd1-252">não</span><span class="sxs-lookup"><span data-stu-id="61fd1-252">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="61fd1-253">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="61fd1-253">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61fd1-254">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="61fd1-254">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





