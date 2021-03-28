---
title: div (sm4-ASM)
description: Divisão por componente.
ms.assetid: B086F069-8F43-4746-A6A5-8F4462212648
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 332d494adc2cc9bebe2e714b47ff2c5a6b299966
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104006884"
---
# <a name="div-sm4---asm"></a><span data-ttu-id="90962-103">div (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="90962-103">div (sm4 - asm)</span></span>

<span data-ttu-id="90962-104">Divisão por componente.</span><span class="sxs-lookup"><span data-stu-id="90962-104">Component-wise divide.</span></span>



| <span data-ttu-id="90962-105">div \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle \] \[ - \] src1 \[ \_ ABS \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="90962-105">div\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\] \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|-------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="90962-106">Item</span><span class="sxs-lookup"><span data-stu-id="90962-106">Item</span></span>                                                            | <span data-ttu-id="90962-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="90962-107">Description</span></span>                                    |
|-----------------------------------------------------------------|------------------------------------------------|
| <span data-ttu-id="90962-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="90962-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="90962-109">\[no \] resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="90962-109">\[in\] The result of the operation.</span></span><br/> |
| <span data-ttu-id="90962-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="90962-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="90962-111">\[no \] dividendo.</span><span class="sxs-lookup"><span data-stu-id="90962-111">\[in\] The dividend.</span></span><br/>                |
| <span data-ttu-id="90962-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="90962-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="90962-113">\[no \] divisor.</span><span class="sxs-lookup"><span data-stu-id="90962-113">\[in\] The divisor.</span></span><br/>                 |



 

## <a name="remarks"></a><span data-ttu-id="90962-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="90962-114">Remarks</span></span>

<span data-ttu-id="90962-115">A tabela a seguir mostra os resultados obtidos ao executar a instrução com várias classes de números, supondo que nenhum estouro ou Subfluxo ocorra.</span><span class="sxs-lookup"><span data-stu-id="90962-115">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span>

<span data-ttu-id="90962-116">Você deve observar as duas implementações permitidas de divide: a/b e a \* (1/b).</span><span class="sxs-lookup"><span data-stu-id="90962-116">You should note the two allowed implementations of divide: a/b and a\*(1/b).</span></span>

<span data-ttu-id="90962-117">Um resultado disso é que há exceções à tabela abaixo para grandes valores de denominadores (maiores que 8.5070592 e + 37), em que 1/denominador é uma desnorma.</span><span class="sxs-lookup"><span data-stu-id="90962-117">One outcome of this is that there are exceptions to the table below for large denominator values (greater than 8.5070592e+37), where 1/denominator is a denorm.</span></span> <span data-ttu-id="90962-118">Como as implementações podem executar a divisão como um \* (1/b), em vez de a/b diretamente, e 1/ \[ grande valor \] é uma desnorma que poderia ser liberada, alguns casos na tabela produzirão resultados diferentes.</span><span class="sxs-lookup"><span data-stu-id="90962-118">Because implementations may perform divide as a\*(1/b), instead of a/b directly, and 1/\[large value\] is a denorm that could get flushed, some cases in the table would produce different results.</span></span> <span data-ttu-id="90962-119">Por exemplo, (+/-) INF/(+/-) \[ valor > 8.5070592 e + 37 \] podem produzir Nan em algumas implementações, mas (+/-) inf em outras implementações</span><span class="sxs-lookup"><span data-stu-id="90962-119">For example, (+/-)INF / (+/-)\[value > 8.5070592e+37\] may produce NaN on some implementations, but (+/-)INF on other implementations</span></span>

<span data-ttu-id="90962-120">Nesta tabela, F significa um número real finito.</span><span class="sxs-lookup"><span data-stu-id="90962-120">In this table F means finite-real number.</span></span>



|                     |          |            |             |        |        |             |            |          |         |
|---------------------|----------|------------|-------------|--------|--------|-------------|------------|----------|---------|
| <span data-ttu-id="90962-121">**src0 src1->**</span><span class="sxs-lookup"><span data-stu-id="90962-121">**src0 src1 ->**</span></span> | <span data-ttu-id="90962-122">**-INF**</span><span class="sxs-lookup"><span data-stu-id="90962-122">**-inf**</span></span> | <span data-ttu-id="90962-123">**-F**</span><span class="sxs-lookup"><span data-stu-id="90962-123">**-F**</span></span>     | <span data-ttu-id="90962-124">**-desnorma**</span><span class="sxs-lookup"><span data-stu-id="90962-124">**-denorm**</span></span> | <span data-ttu-id="90962-125">**-0**</span><span class="sxs-lookup"><span data-stu-id="90962-125">**-0**</span></span> | <span data-ttu-id="90962-126">**+0**</span><span class="sxs-lookup"><span data-stu-id="90962-126">**+0**</span></span> | <span data-ttu-id="90962-127">**+ desnormativo**</span><span class="sxs-lookup"><span data-stu-id="90962-127">**+denorm**</span></span> | <span data-ttu-id="90962-128">**+ F**</span><span class="sxs-lookup"><span data-stu-id="90962-128">**+F**</span></span>     | <span data-ttu-id="90962-129">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="90962-129">**+inf**</span></span> | <span data-ttu-id="90962-130">**Nan**</span><span class="sxs-lookup"><span data-stu-id="90962-130">**Nan**</span></span> |
| <span data-ttu-id="90962-131">**-INF**</span><span class="sxs-lookup"><span data-stu-id="90962-131">**-inf**</span></span>            | <span data-ttu-id="90962-132">-inf</span><span class="sxs-lookup"><span data-stu-id="90962-132">-inf</span></span>     | <span data-ttu-id="90962-133">-inf</span><span class="sxs-lookup"><span data-stu-id="90962-133">-inf</span></span>       | <span data-ttu-id="90962-134">-inf</span><span class="sxs-lookup"><span data-stu-id="90962-134">-inf</span></span>        | <span data-ttu-id="90962-135">-inf</span><span class="sxs-lookup"><span data-stu-id="90962-135">-inf</span></span>   | <span data-ttu-id="90962-136">-inf</span><span class="sxs-lookup"><span data-stu-id="90962-136">-inf</span></span>   | <span data-ttu-id="90962-137">-inf</span><span class="sxs-lookup"><span data-stu-id="90962-137">-inf</span></span>        | <span data-ttu-id="90962-138">-inf</span><span class="sxs-lookup"><span data-stu-id="90962-138">-inf</span></span>       | <span data-ttu-id="90962-139">NaN</span><span class="sxs-lookup"><span data-stu-id="90962-139">NaN</span></span>      | <span data-ttu-id="90962-140">NaN</span><span class="sxs-lookup"><span data-stu-id="90962-140">NaN</span></span>     |
| <span data-ttu-id="90962-141">**-F**</span><span class="sxs-lookup"><span data-stu-id="90962-141">**-F**</span></span>              | <span data-ttu-id="90962-142">-inf</span><span class="sxs-lookup"><span data-stu-id="90962-142">-inf</span></span>     | <span data-ttu-id="90962-143">-F</span><span class="sxs-lookup"><span data-stu-id="90962-143">-F</span></span>         | <span data-ttu-id="90962-144">src0</span><span class="sxs-lookup"><span data-stu-id="90962-144">src0</span></span>        | <span data-ttu-id="90962-145">src0</span><span class="sxs-lookup"><span data-stu-id="90962-145">src0</span></span>   | <span data-ttu-id="90962-146">src0</span><span class="sxs-lookup"><span data-stu-id="90962-146">src0</span></span>   | <span data-ttu-id="90962-147">src0</span><span class="sxs-lookup"><span data-stu-id="90962-147">src0</span></span>        | <span data-ttu-id="90962-148">+-F ou +-0</span><span class="sxs-lookup"><span data-stu-id="90962-148">+-F or +-0</span></span> | <span data-ttu-id="90962-149">+inf</span><span class="sxs-lookup"><span data-stu-id="90962-149">+inf</span></span>     | <span data-ttu-id="90962-150">NaN</span><span class="sxs-lookup"><span data-stu-id="90962-150">NaN</span></span>     |
| <span data-ttu-id="90962-151">**-desnorma**</span><span class="sxs-lookup"><span data-stu-id="90962-151">**-denorm**</span></span>         | <span data-ttu-id="90962-152">-inf</span><span class="sxs-lookup"><span data-stu-id="90962-152">-inf</span></span>     | <span data-ttu-id="90962-153">src1</span><span class="sxs-lookup"><span data-stu-id="90962-153">src1</span></span>       | <span data-ttu-id="90962-154">-0</span><span class="sxs-lookup"><span data-stu-id="90962-154">-0</span></span>          | <span data-ttu-id="90962-155">-0</span><span class="sxs-lookup"><span data-stu-id="90962-155">-0</span></span>     | <span data-ttu-id="90962-156">+0</span><span class="sxs-lookup"><span data-stu-id="90962-156">+0</span></span>     | <span data-ttu-id="90962-157">+0</span><span class="sxs-lookup"><span data-stu-id="90962-157">+0</span></span>          | <span data-ttu-id="90962-158">src1</span><span class="sxs-lookup"><span data-stu-id="90962-158">src1</span></span>       | <span data-ttu-id="90962-159">+inf</span><span class="sxs-lookup"><span data-stu-id="90962-159">+inf</span></span>     | <span data-ttu-id="90962-160">NaN</span><span class="sxs-lookup"><span data-stu-id="90962-160">NaN</span></span>     |
| <span data-ttu-id="90962-161">**-0**</span><span class="sxs-lookup"><span data-stu-id="90962-161">**-0**</span></span>              | <span data-ttu-id="90962-162">-inf</span><span class="sxs-lookup"><span data-stu-id="90962-162">-inf</span></span>     | <span data-ttu-id="90962-163">src1</span><span class="sxs-lookup"><span data-stu-id="90962-163">src1</span></span>       | <span data-ttu-id="90962-164">-0</span><span class="sxs-lookup"><span data-stu-id="90962-164">-0</span></span>          | <span data-ttu-id="90962-165">-0</span><span class="sxs-lookup"><span data-stu-id="90962-165">-0</span></span>     | <span data-ttu-id="90962-166">+0</span><span class="sxs-lookup"><span data-stu-id="90962-166">+0</span></span>     | <span data-ttu-id="90962-167">+0</span><span class="sxs-lookup"><span data-stu-id="90962-167">+0</span></span>          | <span data-ttu-id="90962-168">src1</span><span class="sxs-lookup"><span data-stu-id="90962-168">src1</span></span>       | <span data-ttu-id="90962-169">+inf</span><span class="sxs-lookup"><span data-stu-id="90962-169">+inf</span></span>     | <span data-ttu-id="90962-170">NaN</span><span class="sxs-lookup"><span data-stu-id="90962-170">NaN</span></span>     |
| <span data-ttu-id="90962-171">**+0**</span><span class="sxs-lookup"><span data-stu-id="90962-171">**+0**</span></span>              | <span data-ttu-id="90962-172">-inf</span><span class="sxs-lookup"><span data-stu-id="90962-172">-inf</span></span>     | <span data-ttu-id="90962-173">src1</span><span class="sxs-lookup"><span data-stu-id="90962-173">src1</span></span>       | <span data-ttu-id="90962-174">+0</span><span class="sxs-lookup"><span data-stu-id="90962-174">+0</span></span>          | <span data-ttu-id="90962-175">+0</span><span class="sxs-lookup"><span data-stu-id="90962-175">+0</span></span>     | <span data-ttu-id="90962-176">+0</span><span class="sxs-lookup"><span data-stu-id="90962-176">+0</span></span>     | <span data-ttu-id="90962-177">+0</span><span class="sxs-lookup"><span data-stu-id="90962-177">+0</span></span>          | <span data-ttu-id="90962-178">src1</span><span class="sxs-lookup"><span data-stu-id="90962-178">src1</span></span>       | <span data-ttu-id="90962-179">+inf</span><span class="sxs-lookup"><span data-stu-id="90962-179">+inf</span></span>     | <span data-ttu-id="90962-180">NaN</span><span class="sxs-lookup"><span data-stu-id="90962-180">NaN</span></span>     |
| <span data-ttu-id="90962-181">**+ desnormativo**</span><span class="sxs-lookup"><span data-stu-id="90962-181">**+denorm**</span></span>         | <span data-ttu-id="90962-182">-inf</span><span class="sxs-lookup"><span data-stu-id="90962-182">-inf</span></span>     | <span data-ttu-id="90962-183">src1</span><span class="sxs-lookup"><span data-stu-id="90962-183">src1</span></span>       | <span data-ttu-id="90962-184">+0</span><span class="sxs-lookup"><span data-stu-id="90962-184">+0</span></span>          | <span data-ttu-id="90962-185">+0</span><span class="sxs-lookup"><span data-stu-id="90962-185">+0</span></span>     | <span data-ttu-id="90962-186">+0</span><span class="sxs-lookup"><span data-stu-id="90962-186">+0</span></span>     | <span data-ttu-id="90962-187">+0</span><span class="sxs-lookup"><span data-stu-id="90962-187">+0</span></span>          | <span data-ttu-id="90962-188">src1</span><span class="sxs-lookup"><span data-stu-id="90962-188">src1</span></span>       | <span data-ttu-id="90962-189">+inf</span><span class="sxs-lookup"><span data-stu-id="90962-189">+inf</span></span>     | <span data-ttu-id="90962-190">NaN</span><span class="sxs-lookup"><span data-stu-id="90962-190">NaN</span></span>     |
| <span data-ttu-id="90962-191">**+ F**</span><span class="sxs-lookup"><span data-stu-id="90962-191">**+F**</span></span>              | <span data-ttu-id="90962-192">-inf</span><span class="sxs-lookup"><span data-stu-id="90962-192">-inf</span></span>     | <span data-ttu-id="90962-193">+-F ou +-0</span><span class="sxs-lookup"><span data-stu-id="90962-193">+-F or +-0</span></span> | <span data-ttu-id="90962-194">src0</span><span class="sxs-lookup"><span data-stu-id="90962-194">src0</span></span>        | <span data-ttu-id="90962-195">src0</span><span class="sxs-lookup"><span data-stu-id="90962-195">src0</span></span>   | <span data-ttu-id="90962-196">src0</span><span class="sxs-lookup"><span data-stu-id="90962-196">src0</span></span>   | <span data-ttu-id="90962-197">src0</span><span class="sxs-lookup"><span data-stu-id="90962-197">src0</span></span>        | <span data-ttu-id="90962-198">+ F</span><span class="sxs-lookup"><span data-stu-id="90962-198">+F</span></span>         | <span data-ttu-id="90962-199">+inf</span><span class="sxs-lookup"><span data-stu-id="90962-199">+inf</span></span>     | <span data-ttu-id="90962-200">NaN</span><span class="sxs-lookup"><span data-stu-id="90962-200">NaN</span></span>     |
| <span data-ttu-id="90962-201">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="90962-201">**+inf**</span></span>            | <span data-ttu-id="90962-202">NaN</span><span class="sxs-lookup"><span data-stu-id="90962-202">NaN</span></span>      | <span data-ttu-id="90962-203">+inf</span><span class="sxs-lookup"><span data-stu-id="90962-203">+inf</span></span>       | <span data-ttu-id="90962-204">+inf</span><span class="sxs-lookup"><span data-stu-id="90962-204">+inf</span></span>        | <span data-ttu-id="90962-205">+inf</span><span class="sxs-lookup"><span data-stu-id="90962-205">+inf</span></span>   | <span data-ttu-id="90962-206">+inf</span><span class="sxs-lookup"><span data-stu-id="90962-206">+inf</span></span>   | <span data-ttu-id="90962-207">+inf</span><span class="sxs-lookup"><span data-stu-id="90962-207">+inf</span></span>        | <span data-ttu-id="90962-208">+inf</span><span class="sxs-lookup"><span data-stu-id="90962-208">+inf</span></span>       | <span data-ttu-id="90962-209">+inf</span><span class="sxs-lookup"><span data-stu-id="90962-209">+inf</span></span>     | <span data-ttu-id="90962-210">NaN</span><span class="sxs-lookup"><span data-stu-id="90962-210">NaN</span></span>     |
| <span data-ttu-id="90962-211">**NaN**</span><span class="sxs-lookup"><span data-stu-id="90962-211">**NaN**</span></span>             | <span data-ttu-id="90962-212">NaN</span><span class="sxs-lookup"><span data-stu-id="90962-212">NaN</span></span>      | <span data-ttu-id="90962-213">NaN</span><span class="sxs-lookup"><span data-stu-id="90962-213">NaN</span></span>        | <span data-ttu-id="90962-214">NaN</span><span class="sxs-lookup"><span data-stu-id="90962-214">NaN</span></span>         | <span data-ttu-id="90962-215">NaN</span><span class="sxs-lookup"><span data-stu-id="90962-215">NaN</span></span>    | <span data-ttu-id="90962-216">NaN</span><span class="sxs-lookup"><span data-stu-id="90962-216">NaN</span></span>    | <span data-ttu-id="90962-217">NaN</span><span class="sxs-lookup"><span data-stu-id="90962-217">NaN</span></span>         | <span data-ttu-id="90962-218">NaN</span><span class="sxs-lookup"><span data-stu-id="90962-218">NaN</span></span>        | <span data-ttu-id="90962-219">NaN</span><span class="sxs-lookup"><span data-stu-id="90962-219">NaN</span></span>      | <span data-ttu-id="90962-220">NaN</span><span class="sxs-lookup"><span data-stu-id="90962-220">NaN</span></span>     |



 

<span data-ttu-id="90962-221">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="90962-221">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="90962-222">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="90962-222">Vertex Shader</span></span> | <span data-ttu-id="90962-223">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="90962-223">Geometry Shader</span></span> | <span data-ttu-id="90962-224">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="90962-224">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="90962-225">x</span><span class="sxs-lookup"><span data-stu-id="90962-225">x</span></span>             | <span data-ttu-id="90962-226">x</span><span class="sxs-lookup"><span data-stu-id="90962-226">x</span></span>               | <span data-ttu-id="90962-227">x</span><span class="sxs-lookup"><span data-stu-id="90962-227">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="90962-228">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="90962-228">Minimum Shader Model</span></span>

<span data-ttu-id="90962-229">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="90962-229">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="90962-230">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="90962-230">Shader Model</span></span>                                              | <span data-ttu-id="90962-231">Com suporte</span><span class="sxs-lookup"><span data-stu-id="90962-231">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="90962-232">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="90962-232">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="90962-233">sim</span><span class="sxs-lookup"><span data-stu-id="90962-233">yes</span></span>       |
| [<span data-ttu-id="90962-234">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="90962-234">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="90962-235">sim</span><span class="sxs-lookup"><span data-stu-id="90962-235">yes</span></span>       |
| [<span data-ttu-id="90962-236">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="90962-236">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="90962-237">sim</span><span class="sxs-lookup"><span data-stu-id="90962-237">yes</span></span>       |
| [<span data-ttu-id="90962-238">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="90962-238">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="90962-239">não</span><span class="sxs-lookup"><span data-stu-id="90962-239">no</span></span>        |
| [<span data-ttu-id="90962-240">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="90962-240">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="90962-241">não</span><span class="sxs-lookup"><span data-stu-id="90962-241">no</span></span>        |
| [<span data-ttu-id="90962-242">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="90962-242">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="90962-243">não</span><span class="sxs-lookup"><span data-stu-id="90962-243">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="90962-244">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="90962-244">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90962-245">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="90962-245">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





