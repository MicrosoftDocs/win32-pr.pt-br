---
title: div (sm4-ASM)
description: Divisão por componente.
ms.assetid: B086F069-8F43-4746-A6A5-8F4462212648
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d406c5e61b4615990b445abe169619227d22124c
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999093"
---
# <a name="div-sm4---asm"></a><span data-ttu-id="8290b-103">div (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="8290b-103">div (sm4 - asm)</span></span>

<span data-ttu-id="8290b-104">Divisão por componente.</span><span class="sxs-lookup"><span data-stu-id="8290b-104">Component-wise divide.</span></span>



| <span data-ttu-id="8290b-105">div \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle \] \[ - \] src1 \[ \_ ABS \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="8290b-105">div\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\] \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|-------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="8290b-106">Item</span><span class="sxs-lookup"><span data-stu-id="8290b-106">Item</span></span>                                                            | <span data-ttu-id="8290b-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="8290b-107">Description</span></span>                                    |
|-----------------------------------------------------------------|------------------------------------------------|
| <span data-ttu-id="8290b-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="8290b-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="8290b-109">\[no \] resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="8290b-109">\[in\] The result of the operation.</span></span><br/> |
| <span data-ttu-id="8290b-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="8290b-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="8290b-111">\[no \] dividendo.</span><span class="sxs-lookup"><span data-stu-id="8290b-111">\[in\] The dividend.</span></span><br/>                |
| <span data-ttu-id="8290b-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="8290b-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="8290b-113">\[no \] divisor.</span><span class="sxs-lookup"><span data-stu-id="8290b-113">\[in\] The divisor.</span></span><br/>                 |



 

## <a name="remarks"></a><span data-ttu-id="8290b-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="8290b-114">Remarks</span></span>

<span data-ttu-id="8290b-115">A tabela a seguir mostra os resultados obtidos ao executar a instrução com várias classes de números, supondo que nenhum estouro ou Subfluxo ocorra.</span><span class="sxs-lookup"><span data-stu-id="8290b-115">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span>

<span data-ttu-id="8290b-116">Você deve observar as duas implementações permitidas de divide: a/b e a \* (1/b).</span><span class="sxs-lookup"><span data-stu-id="8290b-116">You should note the two allowed implementations of divide: a/b and a\*(1/b).</span></span>

<span data-ttu-id="8290b-117">Um resultado disso é que há exceções à tabela abaixo para grandes valores de denominadores (maiores que 8.5070592 e + 37), em que 1/denominador é uma desnorma.</span><span class="sxs-lookup"><span data-stu-id="8290b-117">One outcome of this is that there are exceptions to the table below for large denominator values (greater than 8.5070592e+37), where 1/denominator is a denorm.</span></span> <span data-ttu-id="8290b-118">Como as implementações podem executar a divisão como um \* (1/b), em vez de a/b diretamente, e 1/ \[ grande valor \] é uma desnorma que poderia ser liberada, alguns casos na tabela produzirão resultados diferentes.</span><span class="sxs-lookup"><span data-stu-id="8290b-118">Because implementations may perform divide as a\*(1/b), instead of a/b directly, and 1/\[large value\] is a denorm that could get flushed, some cases in the table would produce different results.</span></span> <span data-ttu-id="8290b-119">Por exemplo, (+/-) INF/(+/-) \[ valor > 8.5070592 e + 37 \] podem produzir Nan em algumas implementações, mas (+/-) inf em outras implementações</span><span class="sxs-lookup"><span data-stu-id="8290b-119">For example, (+/-)INF / (+/-)\[value > 8.5070592e+37\] may produce NaN on some implementations, but (+/-)INF on other implementations</span></span>

<span data-ttu-id="8290b-120">Nesta tabela, F significa um número real finito.</span><span class="sxs-lookup"><span data-stu-id="8290b-120">In this table F means finite-real number.</span></span>



| <span data-ttu-id="8290b-121">**src0 src1->**</span><span class="sxs-lookup"><span data-stu-id="8290b-121">**src0 src1 ->**</span></span> | <span data-ttu-id="8290b-122">**-INF**</span><span class="sxs-lookup"><span data-stu-id="8290b-122">**-inf**</span></span> | <span data-ttu-id="8290b-123">**-F**</span><span class="sxs-lookup"><span data-stu-id="8290b-123">**-F**</span></span>     | <span data-ttu-id="8290b-124">**-desnorma**</span><span class="sxs-lookup"><span data-stu-id="8290b-124">**-denorm**</span></span> | <span data-ttu-id="8290b-125">**-0**</span><span class="sxs-lookup"><span data-stu-id="8290b-125">**-0**</span></span> | <span data-ttu-id="8290b-126">**+0**</span><span class="sxs-lookup"><span data-stu-id="8290b-126">**+0**</span></span> | <span data-ttu-id="8290b-127">**+ desnormativo**</span><span class="sxs-lookup"><span data-stu-id="8290b-127">**+denorm**</span></span> | <span data-ttu-id="8290b-128">**+ F**</span><span class="sxs-lookup"><span data-stu-id="8290b-128">**+F**</span></span>     | <span data-ttu-id="8290b-129">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="8290b-129">**+inf**</span></span> | <span data-ttu-id="8290b-130">**Nan**</span><span class="sxs-lookup"><span data-stu-id="8290b-130">**Nan**</span></span> |
|---------------------|----------|------------|-------------|--------|--------|-------------|------------|----------|---------|
| <span data-ttu-id="8290b-131">**-INF**</span><span class="sxs-lookup"><span data-stu-id="8290b-131">**-inf**</span></span>            | <span data-ttu-id="8290b-132">-inf</span><span class="sxs-lookup"><span data-stu-id="8290b-132">-inf</span></span>     | <span data-ttu-id="8290b-133">-inf</span><span class="sxs-lookup"><span data-stu-id="8290b-133">-inf</span></span>       | <span data-ttu-id="8290b-134">-inf</span><span class="sxs-lookup"><span data-stu-id="8290b-134">-inf</span></span>        | <span data-ttu-id="8290b-135">-inf</span><span class="sxs-lookup"><span data-stu-id="8290b-135">-inf</span></span>   | <span data-ttu-id="8290b-136">-inf</span><span class="sxs-lookup"><span data-stu-id="8290b-136">-inf</span></span>   | <span data-ttu-id="8290b-137">-inf</span><span class="sxs-lookup"><span data-stu-id="8290b-137">-inf</span></span>        | <span data-ttu-id="8290b-138">-inf</span><span class="sxs-lookup"><span data-stu-id="8290b-138">-inf</span></span>       | <span data-ttu-id="8290b-139">NaN</span><span class="sxs-lookup"><span data-stu-id="8290b-139">NaN</span></span>      | <span data-ttu-id="8290b-140">NaN</span><span class="sxs-lookup"><span data-stu-id="8290b-140">NaN</span></span>     |
| <span data-ttu-id="8290b-141">**-F**</span><span class="sxs-lookup"><span data-stu-id="8290b-141">**-F**</span></span>              | <span data-ttu-id="8290b-142">-inf</span><span class="sxs-lookup"><span data-stu-id="8290b-142">-inf</span></span>     | <span data-ttu-id="8290b-143">-F</span><span class="sxs-lookup"><span data-stu-id="8290b-143">-F</span></span>         | <span data-ttu-id="8290b-144">src0</span><span class="sxs-lookup"><span data-stu-id="8290b-144">src0</span></span>        | <span data-ttu-id="8290b-145">src0</span><span class="sxs-lookup"><span data-stu-id="8290b-145">src0</span></span>   | <span data-ttu-id="8290b-146">src0</span><span class="sxs-lookup"><span data-stu-id="8290b-146">src0</span></span>   | <span data-ttu-id="8290b-147">src0</span><span class="sxs-lookup"><span data-stu-id="8290b-147">src0</span></span>        | <span data-ttu-id="8290b-148">+-F ou +-0</span><span class="sxs-lookup"><span data-stu-id="8290b-148">+-F or +-0</span></span> | <span data-ttu-id="8290b-149">+inf</span><span class="sxs-lookup"><span data-stu-id="8290b-149">+inf</span></span>     | <span data-ttu-id="8290b-150">NaN</span><span class="sxs-lookup"><span data-stu-id="8290b-150">NaN</span></span>     |
| <span data-ttu-id="8290b-151">**-desnorma**</span><span class="sxs-lookup"><span data-stu-id="8290b-151">**-denorm**</span></span>         | <span data-ttu-id="8290b-152">-inf</span><span class="sxs-lookup"><span data-stu-id="8290b-152">-inf</span></span>     | <span data-ttu-id="8290b-153">src1</span><span class="sxs-lookup"><span data-stu-id="8290b-153">src1</span></span>       | <span data-ttu-id="8290b-154">-0</span><span class="sxs-lookup"><span data-stu-id="8290b-154">-0</span></span>          | <span data-ttu-id="8290b-155">-0</span><span class="sxs-lookup"><span data-stu-id="8290b-155">-0</span></span>     | <span data-ttu-id="8290b-156">+0</span><span class="sxs-lookup"><span data-stu-id="8290b-156">+0</span></span>     | <span data-ttu-id="8290b-157">+0</span><span class="sxs-lookup"><span data-stu-id="8290b-157">+0</span></span>          | <span data-ttu-id="8290b-158">src1</span><span class="sxs-lookup"><span data-stu-id="8290b-158">src1</span></span>       | <span data-ttu-id="8290b-159">+inf</span><span class="sxs-lookup"><span data-stu-id="8290b-159">+inf</span></span>     | <span data-ttu-id="8290b-160">NaN</span><span class="sxs-lookup"><span data-stu-id="8290b-160">NaN</span></span>     |
| <span data-ttu-id="8290b-161">**-0**</span><span class="sxs-lookup"><span data-stu-id="8290b-161">**-0**</span></span>              | <span data-ttu-id="8290b-162">-inf</span><span class="sxs-lookup"><span data-stu-id="8290b-162">-inf</span></span>     | <span data-ttu-id="8290b-163">src1</span><span class="sxs-lookup"><span data-stu-id="8290b-163">src1</span></span>       | <span data-ttu-id="8290b-164">-0</span><span class="sxs-lookup"><span data-stu-id="8290b-164">-0</span></span>          | <span data-ttu-id="8290b-165">-0</span><span class="sxs-lookup"><span data-stu-id="8290b-165">-0</span></span>     | <span data-ttu-id="8290b-166">+0</span><span class="sxs-lookup"><span data-stu-id="8290b-166">+0</span></span>     | <span data-ttu-id="8290b-167">+0</span><span class="sxs-lookup"><span data-stu-id="8290b-167">+0</span></span>          | <span data-ttu-id="8290b-168">src1</span><span class="sxs-lookup"><span data-stu-id="8290b-168">src1</span></span>       | <span data-ttu-id="8290b-169">+inf</span><span class="sxs-lookup"><span data-stu-id="8290b-169">+inf</span></span>     | <span data-ttu-id="8290b-170">NaN</span><span class="sxs-lookup"><span data-stu-id="8290b-170">NaN</span></span>     |
| <span data-ttu-id="8290b-171">**+0**</span><span class="sxs-lookup"><span data-stu-id="8290b-171">**+0**</span></span>              | <span data-ttu-id="8290b-172">-inf</span><span class="sxs-lookup"><span data-stu-id="8290b-172">-inf</span></span>     | <span data-ttu-id="8290b-173">src1</span><span class="sxs-lookup"><span data-stu-id="8290b-173">src1</span></span>       | <span data-ttu-id="8290b-174">+0</span><span class="sxs-lookup"><span data-stu-id="8290b-174">+0</span></span>          | <span data-ttu-id="8290b-175">+0</span><span class="sxs-lookup"><span data-stu-id="8290b-175">+0</span></span>     | <span data-ttu-id="8290b-176">+0</span><span class="sxs-lookup"><span data-stu-id="8290b-176">+0</span></span>     | <span data-ttu-id="8290b-177">+0</span><span class="sxs-lookup"><span data-stu-id="8290b-177">+0</span></span>          | <span data-ttu-id="8290b-178">src1</span><span class="sxs-lookup"><span data-stu-id="8290b-178">src1</span></span>       | <span data-ttu-id="8290b-179">+inf</span><span class="sxs-lookup"><span data-stu-id="8290b-179">+inf</span></span>     | <span data-ttu-id="8290b-180">NaN</span><span class="sxs-lookup"><span data-stu-id="8290b-180">NaN</span></span>     |
| <span data-ttu-id="8290b-181">**+ desnormativo**</span><span class="sxs-lookup"><span data-stu-id="8290b-181">**+denorm**</span></span>         | <span data-ttu-id="8290b-182">-inf</span><span class="sxs-lookup"><span data-stu-id="8290b-182">-inf</span></span>     | <span data-ttu-id="8290b-183">src1</span><span class="sxs-lookup"><span data-stu-id="8290b-183">src1</span></span>       | <span data-ttu-id="8290b-184">+0</span><span class="sxs-lookup"><span data-stu-id="8290b-184">+0</span></span>          | <span data-ttu-id="8290b-185">+0</span><span class="sxs-lookup"><span data-stu-id="8290b-185">+0</span></span>     | <span data-ttu-id="8290b-186">+0</span><span class="sxs-lookup"><span data-stu-id="8290b-186">+0</span></span>     | <span data-ttu-id="8290b-187">+0</span><span class="sxs-lookup"><span data-stu-id="8290b-187">+0</span></span>          | <span data-ttu-id="8290b-188">src1</span><span class="sxs-lookup"><span data-stu-id="8290b-188">src1</span></span>       | <span data-ttu-id="8290b-189">+inf</span><span class="sxs-lookup"><span data-stu-id="8290b-189">+inf</span></span>     | <span data-ttu-id="8290b-190">NaN</span><span class="sxs-lookup"><span data-stu-id="8290b-190">NaN</span></span>     |
| <span data-ttu-id="8290b-191">**+ F**</span><span class="sxs-lookup"><span data-stu-id="8290b-191">**+F**</span></span>              | <span data-ttu-id="8290b-192">-inf</span><span class="sxs-lookup"><span data-stu-id="8290b-192">-inf</span></span>     | <span data-ttu-id="8290b-193">+-F ou +-0</span><span class="sxs-lookup"><span data-stu-id="8290b-193">+-F or +-0</span></span> | <span data-ttu-id="8290b-194">src0</span><span class="sxs-lookup"><span data-stu-id="8290b-194">src0</span></span>        | <span data-ttu-id="8290b-195">src0</span><span class="sxs-lookup"><span data-stu-id="8290b-195">src0</span></span>   | <span data-ttu-id="8290b-196">src0</span><span class="sxs-lookup"><span data-stu-id="8290b-196">src0</span></span>   | <span data-ttu-id="8290b-197">src0</span><span class="sxs-lookup"><span data-stu-id="8290b-197">src0</span></span>        | <span data-ttu-id="8290b-198">+ F</span><span class="sxs-lookup"><span data-stu-id="8290b-198">+F</span></span>         | <span data-ttu-id="8290b-199">+inf</span><span class="sxs-lookup"><span data-stu-id="8290b-199">+inf</span></span>     | <span data-ttu-id="8290b-200">NaN</span><span class="sxs-lookup"><span data-stu-id="8290b-200">NaN</span></span>     |
| <span data-ttu-id="8290b-201">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="8290b-201">**+inf**</span></span>            | <span data-ttu-id="8290b-202">NaN</span><span class="sxs-lookup"><span data-stu-id="8290b-202">NaN</span></span>      | <span data-ttu-id="8290b-203">+inf</span><span class="sxs-lookup"><span data-stu-id="8290b-203">+inf</span></span>       | <span data-ttu-id="8290b-204">+inf</span><span class="sxs-lookup"><span data-stu-id="8290b-204">+inf</span></span>        | <span data-ttu-id="8290b-205">+inf</span><span class="sxs-lookup"><span data-stu-id="8290b-205">+inf</span></span>   | <span data-ttu-id="8290b-206">+inf</span><span class="sxs-lookup"><span data-stu-id="8290b-206">+inf</span></span>   | <span data-ttu-id="8290b-207">+inf</span><span class="sxs-lookup"><span data-stu-id="8290b-207">+inf</span></span>        | <span data-ttu-id="8290b-208">+inf</span><span class="sxs-lookup"><span data-stu-id="8290b-208">+inf</span></span>       | <span data-ttu-id="8290b-209">+inf</span><span class="sxs-lookup"><span data-stu-id="8290b-209">+inf</span></span>     | <span data-ttu-id="8290b-210">NaN</span><span class="sxs-lookup"><span data-stu-id="8290b-210">NaN</span></span>     |
| <span data-ttu-id="8290b-211">**NaN**</span><span class="sxs-lookup"><span data-stu-id="8290b-211">**NaN**</span></span>             | <span data-ttu-id="8290b-212">NaN</span><span class="sxs-lookup"><span data-stu-id="8290b-212">NaN</span></span>      | <span data-ttu-id="8290b-213">NaN</span><span class="sxs-lookup"><span data-stu-id="8290b-213">NaN</span></span>        | <span data-ttu-id="8290b-214">NaN</span><span class="sxs-lookup"><span data-stu-id="8290b-214">NaN</span></span>         | <span data-ttu-id="8290b-215">NaN</span><span class="sxs-lookup"><span data-stu-id="8290b-215">NaN</span></span>    | <span data-ttu-id="8290b-216">NaN</span><span class="sxs-lookup"><span data-stu-id="8290b-216">NaN</span></span>    | <span data-ttu-id="8290b-217">NaN</span><span class="sxs-lookup"><span data-stu-id="8290b-217">NaN</span></span>         | <span data-ttu-id="8290b-218">NaN</span><span class="sxs-lookup"><span data-stu-id="8290b-218">NaN</span></span>        | <span data-ttu-id="8290b-219">NaN</span><span class="sxs-lookup"><span data-stu-id="8290b-219">NaN</span></span>      | <span data-ttu-id="8290b-220">NaN</span><span class="sxs-lookup"><span data-stu-id="8290b-220">NaN</span></span>     |



 

<span data-ttu-id="8290b-221">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="8290b-221">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="8290b-222">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="8290b-222">Vertex Shader</span></span> | <span data-ttu-id="8290b-223">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="8290b-223">Geometry Shader</span></span> | <span data-ttu-id="8290b-224">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="8290b-224">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="8290b-225">x</span><span class="sxs-lookup"><span data-stu-id="8290b-225">x</span></span>             | <span data-ttu-id="8290b-226">x</span><span class="sxs-lookup"><span data-stu-id="8290b-226">x</span></span>               | <span data-ttu-id="8290b-227">x</span><span class="sxs-lookup"><span data-stu-id="8290b-227">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="8290b-228">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="8290b-228">Minimum Shader Model</span></span>

<span data-ttu-id="8290b-229">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="8290b-229">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="8290b-230">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="8290b-230">Shader Model</span></span>                                              | <span data-ttu-id="8290b-231">Suportado</span><span class="sxs-lookup"><span data-stu-id="8290b-231">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="8290b-232">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="8290b-232">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="8290b-233">sim</span><span class="sxs-lookup"><span data-stu-id="8290b-233">yes</span></span>       |
| [<span data-ttu-id="8290b-234">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="8290b-234">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="8290b-235">sim</span><span class="sxs-lookup"><span data-stu-id="8290b-235">yes</span></span>       |
| [<span data-ttu-id="8290b-236">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="8290b-236">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="8290b-237">sim</span><span class="sxs-lookup"><span data-stu-id="8290b-237">yes</span></span>       |
| [<span data-ttu-id="8290b-238">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8290b-238">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="8290b-239">não</span><span class="sxs-lookup"><span data-stu-id="8290b-239">no</span></span>        |
| [<span data-ttu-id="8290b-240">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8290b-240">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="8290b-241">não</span><span class="sxs-lookup"><span data-stu-id="8290b-241">no</span></span>        |
| [<span data-ttu-id="8290b-242">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8290b-242">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="8290b-243">não</span><span class="sxs-lookup"><span data-stu-id="8290b-243">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="8290b-244">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8290b-244">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8290b-245">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8290b-245">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





