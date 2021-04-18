---
title: Adicionar (sm4-ASM)
description: Adição de 2 vetores por componente.
ms.assetid: 405A513C-B2DD-43B9-A86D-1D173B084C51
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5630b983c88da3ba512b5fece6202e0217b2ed39
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104498950"
---
# <a name="add-sm4---asm"></a><span data-ttu-id="a258b-103">Adicionar (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="a258b-103">add (sm4 - asm)</span></span>

<span data-ttu-id="a258b-104">Adição de 2 vetores por componente.</span><span class="sxs-lookup"><span data-stu-id="a258b-104">Component-wise add of 2 vectors.</span></span>



| <span data-ttu-id="a258b-105">Adicione \[ \_ \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="a258b-105">add\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="a258b-106">Item</span><span class="sxs-lookup"><span data-stu-id="a258b-106">Item</span></span>                                                            | <span data-ttu-id="a258b-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="a258b-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="a258b-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="a258b-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="a258b-109">\[no \] endereço do resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="a258b-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="a258b-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="a258b-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="a258b-111">\[no \] vetor a ser adicionado ao *src1*.</span><span class="sxs-lookup"><span data-stu-id="a258b-111">\[in\] The vector to add to *src1*.</span></span><br/>                |
| <span data-ttu-id="a258b-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="a258b-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="a258b-113">\[no \] vetor a ser adicionado ao *src0*.</span><span class="sxs-lookup"><span data-stu-id="a258b-113">\[in\] The vector to add to *src0*.</span></span><br/>                |



 

## <a name="remarks"></a><span data-ttu-id="a258b-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="a258b-114">Remarks</span></span>

<span data-ttu-id="a258b-115">A tabela a seguir mostra os resultados obtidos ao executar a instrução com várias classes de números, supondo que nenhum estouro ou Subfluxo ocorra.</span><span class="sxs-lookup"><span data-stu-id="a258b-115">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span> <span data-ttu-id="a258b-116">F significa número real finito.</span><span class="sxs-lookup"><span data-stu-id="a258b-116">F means finite real number.</span></span>



|                    |          |            |             |        |        |            |            |          |         |
|--------------------|----------|------------|-------------|--------|--------|------------|------------|----------|---------|
| <span data-ttu-id="a258b-117">**src0 src1->**</span><span class="sxs-lookup"><span data-stu-id="a258b-117">**src0 src1->**</span></span> | <span data-ttu-id="a258b-118">**-INF**</span><span class="sxs-lookup"><span data-stu-id="a258b-118">**-inf**</span></span> | <span data-ttu-id="a258b-119">**-F**</span><span class="sxs-lookup"><span data-stu-id="a258b-119">**-F**</span></span>     | <span data-ttu-id="a258b-120">**-desnorma**</span><span class="sxs-lookup"><span data-stu-id="a258b-120">**-denorm**</span></span> | <span data-ttu-id="a258b-121">**-0**</span><span class="sxs-lookup"><span data-stu-id="a258b-121">**-0**</span></span> | <span data-ttu-id="a258b-122">**+0**</span><span class="sxs-lookup"><span data-stu-id="a258b-122">**+0**</span></span> | <span data-ttu-id="a258b-123">**desnormalização**</span><span class="sxs-lookup"><span data-stu-id="a258b-123">**denorm**</span></span> | <span data-ttu-id="a258b-124">**+ F**</span><span class="sxs-lookup"><span data-stu-id="a258b-124">**+F**</span></span>     | <span data-ttu-id="a258b-125">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="a258b-125">**+inf**</span></span> | <span data-ttu-id="a258b-126">**NaN**</span><span class="sxs-lookup"><span data-stu-id="a258b-126">**NaN**</span></span> |
| <span data-ttu-id="a258b-127">**-INF**</span><span class="sxs-lookup"><span data-stu-id="a258b-127">**-inf**</span></span>           | <span data-ttu-id="a258b-128">-inf</span><span class="sxs-lookup"><span data-stu-id="a258b-128">-inf</span></span>     | <span data-ttu-id="a258b-129">-inf</span><span class="sxs-lookup"><span data-stu-id="a258b-129">-inf</span></span>       | <span data-ttu-id="a258b-130">-inf</span><span class="sxs-lookup"><span data-stu-id="a258b-130">-inf</span></span>        | <span data-ttu-id="a258b-131">-inf</span><span class="sxs-lookup"><span data-stu-id="a258b-131">-inf</span></span>   | <span data-ttu-id="a258b-132">-inf</span><span class="sxs-lookup"><span data-stu-id="a258b-132">-inf</span></span>   | <span data-ttu-id="a258b-133">-inf</span><span class="sxs-lookup"><span data-stu-id="a258b-133">-inf</span></span>       | <span data-ttu-id="a258b-134">-inf</span><span class="sxs-lookup"><span data-stu-id="a258b-134">-inf</span></span>       | <span data-ttu-id="a258b-135">NaN</span><span class="sxs-lookup"><span data-stu-id="a258b-135">NaN</span></span>      | <span data-ttu-id="a258b-136">NaN</span><span class="sxs-lookup"><span data-stu-id="a258b-136">NaN</span></span>     |
| <span data-ttu-id="a258b-137">**-F**</span><span class="sxs-lookup"><span data-stu-id="a258b-137">**-F**</span></span>             | <span data-ttu-id="a258b-138">-inf</span><span class="sxs-lookup"><span data-stu-id="a258b-138">-inf</span></span>     | <span data-ttu-id="a258b-139">-F</span><span class="sxs-lookup"><span data-stu-id="a258b-139">-F</span></span>         | <span data-ttu-id="a258b-140">src0</span><span class="sxs-lookup"><span data-stu-id="a258b-140">src0</span></span>        | <span data-ttu-id="a258b-141">src0</span><span class="sxs-lookup"><span data-stu-id="a258b-141">src0</span></span>   | <span data-ttu-id="a258b-142">src0</span><span class="sxs-lookup"><span data-stu-id="a258b-142">src0</span></span>   | <span data-ttu-id="a258b-143">src0</span><span class="sxs-lookup"><span data-stu-id="a258b-143">src0</span></span>       | <span data-ttu-id="a258b-144">+-F ou +-0</span><span class="sxs-lookup"><span data-stu-id="a258b-144">+-F or +-0</span></span> | <span data-ttu-id="a258b-145">+inf</span><span class="sxs-lookup"><span data-stu-id="a258b-145">+inf</span></span>     | <span data-ttu-id="a258b-146">NaN</span><span class="sxs-lookup"><span data-stu-id="a258b-146">NaN</span></span>     |
| <span data-ttu-id="a258b-147">**-desnorma**</span><span class="sxs-lookup"><span data-stu-id="a258b-147">**-denorm**</span></span>        | <span data-ttu-id="a258b-148">-inf</span><span class="sxs-lookup"><span data-stu-id="a258b-148">-inf</span></span>     | <span data-ttu-id="a258b-149">src1</span><span class="sxs-lookup"><span data-stu-id="a258b-149">src1</span></span>       | <span data-ttu-id="a258b-150">-0</span><span class="sxs-lookup"><span data-stu-id="a258b-150">-0</span></span>          | <span data-ttu-id="a258b-151">-0</span><span class="sxs-lookup"><span data-stu-id="a258b-151">-0</span></span>     | <span data-ttu-id="a258b-152">+0</span><span class="sxs-lookup"><span data-stu-id="a258b-152">+0</span></span>     | <span data-ttu-id="a258b-153">+0</span><span class="sxs-lookup"><span data-stu-id="a258b-153">+0</span></span>         | <span data-ttu-id="a258b-154">src1</span><span class="sxs-lookup"><span data-stu-id="a258b-154">src1</span></span>       | <span data-ttu-id="a258b-155">+inf</span><span class="sxs-lookup"><span data-stu-id="a258b-155">+inf</span></span>     | <span data-ttu-id="a258b-156">NaN</span><span class="sxs-lookup"><span data-stu-id="a258b-156">NaN</span></span>     |
| <span data-ttu-id="a258b-157">**-0**</span><span class="sxs-lookup"><span data-stu-id="a258b-157">**-0**</span></span>             | <span data-ttu-id="a258b-158">-inf</span><span class="sxs-lookup"><span data-stu-id="a258b-158">-inf</span></span>     | <span data-ttu-id="a258b-159">src1</span><span class="sxs-lookup"><span data-stu-id="a258b-159">src1</span></span>       | <span data-ttu-id="a258b-160">-0</span><span class="sxs-lookup"><span data-stu-id="a258b-160">-0</span></span>          | <span data-ttu-id="a258b-161">-0</span><span class="sxs-lookup"><span data-stu-id="a258b-161">-0</span></span>     | <span data-ttu-id="a258b-162">+0</span><span class="sxs-lookup"><span data-stu-id="a258b-162">+0</span></span>     | <span data-ttu-id="a258b-163">+0</span><span class="sxs-lookup"><span data-stu-id="a258b-163">+0</span></span>         | <span data-ttu-id="a258b-164">src1</span><span class="sxs-lookup"><span data-stu-id="a258b-164">src1</span></span>       | <span data-ttu-id="a258b-165">+inf</span><span class="sxs-lookup"><span data-stu-id="a258b-165">+inf</span></span>     | <span data-ttu-id="a258b-166">NaN</span><span class="sxs-lookup"><span data-stu-id="a258b-166">NaN</span></span>     |
| <span data-ttu-id="a258b-167">**+0**</span><span class="sxs-lookup"><span data-stu-id="a258b-167">**+0**</span></span>             | <span data-ttu-id="a258b-168">i-inf</span><span class="sxs-lookup"><span data-stu-id="a258b-168">i-inf</span></span>    | <span data-ttu-id="a258b-169">src1</span><span class="sxs-lookup"><span data-stu-id="a258b-169">src1</span></span>       | <span data-ttu-id="a258b-170">+0</span><span class="sxs-lookup"><span data-stu-id="a258b-170">+0</span></span>          | <span data-ttu-id="a258b-171">+0</span><span class="sxs-lookup"><span data-stu-id="a258b-171">+0</span></span>     | <span data-ttu-id="a258b-172">+0</span><span class="sxs-lookup"><span data-stu-id="a258b-172">+0</span></span>     | <span data-ttu-id="a258b-173">+0</span><span class="sxs-lookup"><span data-stu-id="a258b-173">+0</span></span>         | <span data-ttu-id="a258b-174">src1</span><span class="sxs-lookup"><span data-stu-id="a258b-174">src1</span></span>       | <span data-ttu-id="a258b-175">+inf</span><span class="sxs-lookup"><span data-stu-id="a258b-175">+inf</span></span>     | <span data-ttu-id="a258b-176">NaN</span><span class="sxs-lookup"><span data-stu-id="a258b-176">NaN</span></span>     |
| <span data-ttu-id="a258b-177">**+ desnormativo**</span><span class="sxs-lookup"><span data-stu-id="a258b-177">**+denorm**</span></span>        | <span data-ttu-id="a258b-178">-inf</span><span class="sxs-lookup"><span data-stu-id="a258b-178">-inf</span></span>     | <span data-ttu-id="a258b-179">src1</span><span class="sxs-lookup"><span data-stu-id="a258b-179">src1</span></span>       | <span data-ttu-id="a258b-180">+0</span><span class="sxs-lookup"><span data-stu-id="a258b-180">+0</span></span>          | <span data-ttu-id="a258b-181">+0</span><span class="sxs-lookup"><span data-stu-id="a258b-181">+0</span></span>     | <span data-ttu-id="a258b-182">+0</span><span class="sxs-lookup"><span data-stu-id="a258b-182">+0</span></span>     | <span data-ttu-id="a258b-183">+0</span><span class="sxs-lookup"><span data-stu-id="a258b-183">+0</span></span>         | <span data-ttu-id="a258b-184">src1</span><span class="sxs-lookup"><span data-stu-id="a258b-184">src1</span></span>       | <span data-ttu-id="a258b-185">+inf</span><span class="sxs-lookup"><span data-stu-id="a258b-185">+inf</span></span>     | <span data-ttu-id="a258b-186">NaN</span><span class="sxs-lookup"><span data-stu-id="a258b-186">NaN</span></span>     |
| <span data-ttu-id="a258b-187">**+ F**</span><span class="sxs-lookup"><span data-stu-id="a258b-187">**+F**</span></span>             | <span data-ttu-id="a258b-188">-inf</span><span class="sxs-lookup"><span data-stu-id="a258b-188">-inf</span></span>     | <span data-ttu-id="a258b-189">+-F ou +-0</span><span class="sxs-lookup"><span data-stu-id="a258b-189">+-F or +-0</span></span> | <span data-ttu-id="a258b-190">src0</span><span class="sxs-lookup"><span data-stu-id="a258b-190">src0</span></span>        | <span data-ttu-id="a258b-191">src0</span><span class="sxs-lookup"><span data-stu-id="a258b-191">src0</span></span>   | <span data-ttu-id="a258b-192">src0</span><span class="sxs-lookup"><span data-stu-id="a258b-192">src0</span></span>   | <span data-ttu-id="a258b-193">src0</span><span class="sxs-lookup"><span data-stu-id="a258b-193">src0</span></span>       | <span data-ttu-id="a258b-194">+ F</span><span class="sxs-lookup"><span data-stu-id="a258b-194">+F</span></span>         | <span data-ttu-id="a258b-195">+inf</span><span class="sxs-lookup"><span data-stu-id="a258b-195">+inf</span></span>     | <span data-ttu-id="a258b-196">NaN</span><span class="sxs-lookup"><span data-stu-id="a258b-196">NaN</span></span>     |
| <span data-ttu-id="a258b-197">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="a258b-197">**+inf**</span></span>           | <span data-ttu-id="a258b-198">NaN</span><span class="sxs-lookup"><span data-stu-id="a258b-198">NaN</span></span>      | <span data-ttu-id="a258b-199">+inf</span><span class="sxs-lookup"><span data-stu-id="a258b-199">+inf</span></span>       | <span data-ttu-id="a258b-200">+inf</span><span class="sxs-lookup"><span data-stu-id="a258b-200">+inf</span></span>        | <span data-ttu-id="a258b-201">+inf</span><span class="sxs-lookup"><span data-stu-id="a258b-201">+inf</span></span>   | <span data-ttu-id="a258b-202">+inf</span><span class="sxs-lookup"><span data-stu-id="a258b-202">+inf</span></span>   | <span data-ttu-id="a258b-203">+inf</span><span class="sxs-lookup"><span data-stu-id="a258b-203">+inf</span></span>       | <span data-ttu-id="a258b-204">+inf</span><span class="sxs-lookup"><span data-stu-id="a258b-204">+inf</span></span>       | <span data-ttu-id="a258b-205">+inf</span><span class="sxs-lookup"><span data-stu-id="a258b-205">+inf</span></span>     | <span data-ttu-id="a258b-206">NaN</span><span class="sxs-lookup"><span data-stu-id="a258b-206">NaN</span></span>     |
| <span data-ttu-id="a258b-207">**NaN**</span><span class="sxs-lookup"><span data-stu-id="a258b-207">**NaN**</span></span>            | <span data-ttu-id="a258b-208">NaN</span><span class="sxs-lookup"><span data-stu-id="a258b-208">NaN</span></span>      | <span data-ttu-id="a258b-209">NaN</span><span class="sxs-lookup"><span data-stu-id="a258b-209">NaN</span></span>        | <span data-ttu-id="a258b-210">NaN</span><span class="sxs-lookup"><span data-stu-id="a258b-210">NaN</span></span>         | <span data-ttu-id="a258b-211">NaN</span><span class="sxs-lookup"><span data-stu-id="a258b-211">NaN</span></span>    | <span data-ttu-id="a258b-212">NaN</span><span class="sxs-lookup"><span data-stu-id="a258b-212">NaN</span></span>    | <span data-ttu-id="a258b-213">NaN</span><span class="sxs-lookup"><span data-stu-id="a258b-213">NaN</span></span>        | <span data-ttu-id="a258b-214">NaN</span><span class="sxs-lookup"><span data-stu-id="a258b-214">NaN</span></span>        | <span data-ttu-id="a258b-215">NaN</span><span class="sxs-lookup"><span data-stu-id="a258b-215">NaN</span></span>      | <span data-ttu-id="a258b-216">NaN</span><span class="sxs-lookup"><span data-stu-id="a258b-216">NaN</span></span>     |



 

<span data-ttu-id="a258b-217">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="a258b-217">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="a258b-218">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="a258b-218">Vertex Shader</span></span> | <span data-ttu-id="a258b-219">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="a258b-219">Geometry Shader</span></span> | <span data-ttu-id="a258b-220">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="a258b-220">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="a258b-221">x</span><span class="sxs-lookup"><span data-stu-id="a258b-221">x</span></span>             | <span data-ttu-id="a258b-222">x</span><span class="sxs-lookup"><span data-stu-id="a258b-222">x</span></span>               | <span data-ttu-id="a258b-223">x</span><span class="sxs-lookup"><span data-stu-id="a258b-223">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="a258b-224">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="a258b-224">Minimum Shader Model</span></span>

<span data-ttu-id="a258b-225">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="a258b-225">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="a258b-226">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="a258b-226">Shader Model</span></span>                                              | <span data-ttu-id="a258b-227">Com suporte</span><span class="sxs-lookup"><span data-stu-id="a258b-227">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="a258b-228">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="a258b-228">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="a258b-229">sim</span><span class="sxs-lookup"><span data-stu-id="a258b-229">yes</span></span>       |
| [<span data-ttu-id="a258b-230">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="a258b-230">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="a258b-231">sim</span><span class="sxs-lookup"><span data-stu-id="a258b-231">yes</span></span>       |
| [<span data-ttu-id="a258b-232">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="a258b-232">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="a258b-233">sim</span><span class="sxs-lookup"><span data-stu-id="a258b-233">yes</span></span>       |
| [<span data-ttu-id="a258b-234">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a258b-234">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="a258b-235">não</span><span class="sxs-lookup"><span data-stu-id="a258b-235">no</span></span>        |
| [<span data-ttu-id="a258b-236">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a258b-236">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="a258b-237">não</span><span class="sxs-lookup"><span data-stu-id="a258b-237">no</span></span>        |
| [<span data-ttu-id="a258b-238">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a258b-238">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="a258b-239">não</span><span class="sxs-lookup"><span data-stu-id="a258b-239">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="a258b-240">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a258b-240">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a258b-241">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a258b-241">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





