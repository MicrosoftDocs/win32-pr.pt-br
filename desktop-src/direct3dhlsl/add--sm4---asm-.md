---
title: Adicionar (sm4-ASM)
description: Adição de 2 vetores por componente.
ms.assetid: 405A513C-B2DD-43B9-A86D-1D173B084C51
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e34f0a95ad9ee9ae4bdeed317eef133e3773311
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994973"
---
# <a name="add-sm4---asm"></a><span data-ttu-id="5593e-103">Adicionar (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="5593e-103">add (sm4 - asm)</span></span>

<span data-ttu-id="5593e-104">Adição de 2 vetores por componente.</span><span class="sxs-lookup"><span data-stu-id="5593e-104">Component-wise add of 2 vectors.</span></span>



| <span data-ttu-id="5593e-105">Adicione \[ \_ \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="5593e-105">add\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="5593e-106">Item</span><span class="sxs-lookup"><span data-stu-id="5593e-106">Item</span></span>                                                            | <span data-ttu-id="5593e-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="5593e-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="5593e-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="5593e-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="5593e-109">\[no \] endereço do resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="5593e-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="5593e-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="5593e-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="5593e-111">\[no \] vetor a ser adicionado ao *src1*.</span><span class="sxs-lookup"><span data-stu-id="5593e-111">\[in\] The vector to add to *src1*.</span></span><br/>                |
| <span data-ttu-id="5593e-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="5593e-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="5593e-113">\[no \] vetor a ser adicionado ao *src0*.</span><span class="sxs-lookup"><span data-stu-id="5593e-113">\[in\] The vector to add to *src0*.</span></span><br/>                |



 

## <a name="remarks"></a><span data-ttu-id="5593e-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="5593e-114">Remarks</span></span>

<span data-ttu-id="5593e-115">A tabela a seguir mostra os resultados obtidos ao executar a instrução com várias classes de números, supondo que nenhum estouro ou Subfluxo ocorra.</span><span class="sxs-lookup"><span data-stu-id="5593e-115">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span> <span data-ttu-id="5593e-116">F significa número real finito.</span><span class="sxs-lookup"><span data-stu-id="5593e-116">F means finite real number.</span></span>



| <span data-ttu-id="5593e-117">**src0 src1->**</span><span class="sxs-lookup"><span data-stu-id="5593e-117">**src0 src1->**</span></span> | <span data-ttu-id="5593e-118">**-INF**</span><span class="sxs-lookup"><span data-stu-id="5593e-118">**-inf**</span></span> | <span data-ttu-id="5593e-119">**-F**</span><span class="sxs-lookup"><span data-stu-id="5593e-119">**-F**</span></span>     | <span data-ttu-id="5593e-120">**-desnorma**</span><span class="sxs-lookup"><span data-stu-id="5593e-120">**-denorm**</span></span> | <span data-ttu-id="5593e-121">**-0**</span><span class="sxs-lookup"><span data-stu-id="5593e-121">**-0**</span></span> | <span data-ttu-id="5593e-122">**+0**</span><span class="sxs-lookup"><span data-stu-id="5593e-122">**+0**</span></span> | <span data-ttu-id="5593e-123">**desnormalização**</span><span class="sxs-lookup"><span data-stu-id="5593e-123">**denorm**</span></span> | <span data-ttu-id="5593e-124">**+ F**</span><span class="sxs-lookup"><span data-stu-id="5593e-124">**+F**</span></span>     | <span data-ttu-id="5593e-125">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="5593e-125">**+inf**</span></span> | <span data-ttu-id="5593e-126">**NaN**</span><span class="sxs-lookup"><span data-stu-id="5593e-126">**NaN**</span></span> |
|--------------------|----------|------------|-------------|--------|--------|------------|------------|----------|---------|
| <span data-ttu-id="5593e-127">**-INF**</span><span class="sxs-lookup"><span data-stu-id="5593e-127">**-inf**</span></span>           | <span data-ttu-id="5593e-128">-inf</span><span class="sxs-lookup"><span data-stu-id="5593e-128">-inf</span></span>     | <span data-ttu-id="5593e-129">-inf</span><span class="sxs-lookup"><span data-stu-id="5593e-129">-inf</span></span>       | <span data-ttu-id="5593e-130">-inf</span><span class="sxs-lookup"><span data-stu-id="5593e-130">-inf</span></span>        | <span data-ttu-id="5593e-131">-inf</span><span class="sxs-lookup"><span data-stu-id="5593e-131">-inf</span></span>   | <span data-ttu-id="5593e-132">-inf</span><span class="sxs-lookup"><span data-stu-id="5593e-132">-inf</span></span>   | <span data-ttu-id="5593e-133">-inf</span><span class="sxs-lookup"><span data-stu-id="5593e-133">-inf</span></span>       | <span data-ttu-id="5593e-134">-inf</span><span class="sxs-lookup"><span data-stu-id="5593e-134">-inf</span></span>       | <span data-ttu-id="5593e-135">NaN</span><span class="sxs-lookup"><span data-stu-id="5593e-135">NaN</span></span>      | <span data-ttu-id="5593e-136">NaN</span><span class="sxs-lookup"><span data-stu-id="5593e-136">NaN</span></span>     |
| <span data-ttu-id="5593e-137">**-F**</span><span class="sxs-lookup"><span data-stu-id="5593e-137">**-F**</span></span>             | <span data-ttu-id="5593e-138">-inf</span><span class="sxs-lookup"><span data-stu-id="5593e-138">-inf</span></span>     | <span data-ttu-id="5593e-139">-F</span><span class="sxs-lookup"><span data-stu-id="5593e-139">-F</span></span>         | <span data-ttu-id="5593e-140">src0</span><span class="sxs-lookup"><span data-stu-id="5593e-140">src0</span></span>        | <span data-ttu-id="5593e-141">src0</span><span class="sxs-lookup"><span data-stu-id="5593e-141">src0</span></span>   | <span data-ttu-id="5593e-142">src0</span><span class="sxs-lookup"><span data-stu-id="5593e-142">src0</span></span>   | <span data-ttu-id="5593e-143">src0</span><span class="sxs-lookup"><span data-stu-id="5593e-143">src0</span></span>       | <span data-ttu-id="5593e-144">+-F ou +-0</span><span class="sxs-lookup"><span data-stu-id="5593e-144">+-F or +-0</span></span> | <span data-ttu-id="5593e-145">+inf</span><span class="sxs-lookup"><span data-stu-id="5593e-145">+inf</span></span>     | <span data-ttu-id="5593e-146">NaN</span><span class="sxs-lookup"><span data-stu-id="5593e-146">NaN</span></span>     |
| <span data-ttu-id="5593e-147">**-desnorma**</span><span class="sxs-lookup"><span data-stu-id="5593e-147">**-denorm**</span></span>        | <span data-ttu-id="5593e-148">-inf</span><span class="sxs-lookup"><span data-stu-id="5593e-148">-inf</span></span>     | <span data-ttu-id="5593e-149">src1</span><span class="sxs-lookup"><span data-stu-id="5593e-149">src1</span></span>       | <span data-ttu-id="5593e-150">-0</span><span class="sxs-lookup"><span data-stu-id="5593e-150">-0</span></span>          | <span data-ttu-id="5593e-151">-0</span><span class="sxs-lookup"><span data-stu-id="5593e-151">-0</span></span>     | <span data-ttu-id="5593e-152">+0</span><span class="sxs-lookup"><span data-stu-id="5593e-152">+0</span></span>     | <span data-ttu-id="5593e-153">+0</span><span class="sxs-lookup"><span data-stu-id="5593e-153">+0</span></span>         | <span data-ttu-id="5593e-154">src1</span><span class="sxs-lookup"><span data-stu-id="5593e-154">src1</span></span>       | <span data-ttu-id="5593e-155">+inf</span><span class="sxs-lookup"><span data-stu-id="5593e-155">+inf</span></span>     | <span data-ttu-id="5593e-156">NaN</span><span class="sxs-lookup"><span data-stu-id="5593e-156">NaN</span></span>     |
| <span data-ttu-id="5593e-157">**-0**</span><span class="sxs-lookup"><span data-stu-id="5593e-157">**-0**</span></span>             | <span data-ttu-id="5593e-158">-inf</span><span class="sxs-lookup"><span data-stu-id="5593e-158">-inf</span></span>     | <span data-ttu-id="5593e-159">src1</span><span class="sxs-lookup"><span data-stu-id="5593e-159">src1</span></span>       | <span data-ttu-id="5593e-160">-0</span><span class="sxs-lookup"><span data-stu-id="5593e-160">-0</span></span>          | <span data-ttu-id="5593e-161">-0</span><span class="sxs-lookup"><span data-stu-id="5593e-161">-0</span></span>     | <span data-ttu-id="5593e-162">+0</span><span class="sxs-lookup"><span data-stu-id="5593e-162">+0</span></span>     | <span data-ttu-id="5593e-163">+0</span><span class="sxs-lookup"><span data-stu-id="5593e-163">+0</span></span>         | <span data-ttu-id="5593e-164">src1</span><span class="sxs-lookup"><span data-stu-id="5593e-164">src1</span></span>       | <span data-ttu-id="5593e-165">+inf</span><span class="sxs-lookup"><span data-stu-id="5593e-165">+inf</span></span>     | <span data-ttu-id="5593e-166">NaN</span><span class="sxs-lookup"><span data-stu-id="5593e-166">NaN</span></span>     |
| <span data-ttu-id="5593e-167">**+0**</span><span class="sxs-lookup"><span data-stu-id="5593e-167">**+0**</span></span>             | <span data-ttu-id="5593e-168">i-inf</span><span class="sxs-lookup"><span data-stu-id="5593e-168">i-inf</span></span>    | <span data-ttu-id="5593e-169">src1</span><span class="sxs-lookup"><span data-stu-id="5593e-169">src1</span></span>       | <span data-ttu-id="5593e-170">+0</span><span class="sxs-lookup"><span data-stu-id="5593e-170">+0</span></span>          | <span data-ttu-id="5593e-171">+0</span><span class="sxs-lookup"><span data-stu-id="5593e-171">+0</span></span>     | <span data-ttu-id="5593e-172">+0</span><span class="sxs-lookup"><span data-stu-id="5593e-172">+0</span></span>     | <span data-ttu-id="5593e-173">+0</span><span class="sxs-lookup"><span data-stu-id="5593e-173">+0</span></span>         | <span data-ttu-id="5593e-174">src1</span><span class="sxs-lookup"><span data-stu-id="5593e-174">src1</span></span>       | <span data-ttu-id="5593e-175">+inf</span><span class="sxs-lookup"><span data-stu-id="5593e-175">+inf</span></span>     | <span data-ttu-id="5593e-176">NaN</span><span class="sxs-lookup"><span data-stu-id="5593e-176">NaN</span></span>     |
| <span data-ttu-id="5593e-177">**+ desnormativo**</span><span class="sxs-lookup"><span data-stu-id="5593e-177">**+denorm**</span></span>        | <span data-ttu-id="5593e-178">-inf</span><span class="sxs-lookup"><span data-stu-id="5593e-178">-inf</span></span>     | <span data-ttu-id="5593e-179">src1</span><span class="sxs-lookup"><span data-stu-id="5593e-179">src1</span></span>       | <span data-ttu-id="5593e-180">+0</span><span class="sxs-lookup"><span data-stu-id="5593e-180">+0</span></span>          | <span data-ttu-id="5593e-181">+0</span><span class="sxs-lookup"><span data-stu-id="5593e-181">+0</span></span>     | <span data-ttu-id="5593e-182">+0</span><span class="sxs-lookup"><span data-stu-id="5593e-182">+0</span></span>     | <span data-ttu-id="5593e-183">+0</span><span class="sxs-lookup"><span data-stu-id="5593e-183">+0</span></span>         | <span data-ttu-id="5593e-184">src1</span><span class="sxs-lookup"><span data-stu-id="5593e-184">src1</span></span>       | <span data-ttu-id="5593e-185">+inf</span><span class="sxs-lookup"><span data-stu-id="5593e-185">+inf</span></span>     | <span data-ttu-id="5593e-186">NaN</span><span class="sxs-lookup"><span data-stu-id="5593e-186">NaN</span></span>     |
| <span data-ttu-id="5593e-187">**+ F**</span><span class="sxs-lookup"><span data-stu-id="5593e-187">**+F**</span></span>             | <span data-ttu-id="5593e-188">-inf</span><span class="sxs-lookup"><span data-stu-id="5593e-188">-inf</span></span>     | <span data-ttu-id="5593e-189">+-F ou +-0</span><span class="sxs-lookup"><span data-stu-id="5593e-189">+-F or +-0</span></span> | <span data-ttu-id="5593e-190">src0</span><span class="sxs-lookup"><span data-stu-id="5593e-190">src0</span></span>        | <span data-ttu-id="5593e-191">src0</span><span class="sxs-lookup"><span data-stu-id="5593e-191">src0</span></span>   | <span data-ttu-id="5593e-192">src0</span><span class="sxs-lookup"><span data-stu-id="5593e-192">src0</span></span>   | <span data-ttu-id="5593e-193">src0</span><span class="sxs-lookup"><span data-stu-id="5593e-193">src0</span></span>       | <span data-ttu-id="5593e-194">+ F</span><span class="sxs-lookup"><span data-stu-id="5593e-194">+F</span></span>         | <span data-ttu-id="5593e-195">+inf</span><span class="sxs-lookup"><span data-stu-id="5593e-195">+inf</span></span>     | <span data-ttu-id="5593e-196">NaN</span><span class="sxs-lookup"><span data-stu-id="5593e-196">NaN</span></span>     |
| <span data-ttu-id="5593e-197">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="5593e-197">**+inf**</span></span>           | <span data-ttu-id="5593e-198">NaN</span><span class="sxs-lookup"><span data-stu-id="5593e-198">NaN</span></span>      | <span data-ttu-id="5593e-199">+inf</span><span class="sxs-lookup"><span data-stu-id="5593e-199">+inf</span></span>       | <span data-ttu-id="5593e-200">+inf</span><span class="sxs-lookup"><span data-stu-id="5593e-200">+inf</span></span>        | <span data-ttu-id="5593e-201">+inf</span><span class="sxs-lookup"><span data-stu-id="5593e-201">+inf</span></span>   | <span data-ttu-id="5593e-202">+inf</span><span class="sxs-lookup"><span data-stu-id="5593e-202">+inf</span></span>   | <span data-ttu-id="5593e-203">+inf</span><span class="sxs-lookup"><span data-stu-id="5593e-203">+inf</span></span>       | <span data-ttu-id="5593e-204">+inf</span><span class="sxs-lookup"><span data-stu-id="5593e-204">+inf</span></span>       | <span data-ttu-id="5593e-205">+inf</span><span class="sxs-lookup"><span data-stu-id="5593e-205">+inf</span></span>     | <span data-ttu-id="5593e-206">NaN</span><span class="sxs-lookup"><span data-stu-id="5593e-206">NaN</span></span>     |
| <span data-ttu-id="5593e-207">**NaN**</span><span class="sxs-lookup"><span data-stu-id="5593e-207">**NaN**</span></span>            | <span data-ttu-id="5593e-208">NaN</span><span class="sxs-lookup"><span data-stu-id="5593e-208">NaN</span></span>      | <span data-ttu-id="5593e-209">NaN</span><span class="sxs-lookup"><span data-stu-id="5593e-209">NaN</span></span>        | <span data-ttu-id="5593e-210">NaN</span><span class="sxs-lookup"><span data-stu-id="5593e-210">NaN</span></span>         | <span data-ttu-id="5593e-211">NaN</span><span class="sxs-lookup"><span data-stu-id="5593e-211">NaN</span></span>    | <span data-ttu-id="5593e-212">NaN</span><span class="sxs-lookup"><span data-stu-id="5593e-212">NaN</span></span>    | <span data-ttu-id="5593e-213">NaN</span><span class="sxs-lookup"><span data-stu-id="5593e-213">NaN</span></span>        | <span data-ttu-id="5593e-214">NaN</span><span class="sxs-lookup"><span data-stu-id="5593e-214">NaN</span></span>        | <span data-ttu-id="5593e-215">NaN</span><span class="sxs-lookup"><span data-stu-id="5593e-215">NaN</span></span>      | <span data-ttu-id="5593e-216">NaN</span><span class="sxs-lookup"><span data-stu-id="5593e-216">NaN</span></span>     |



 

<span data-ttu-id="5593e-217">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="5593e-217">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="5593e-218">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="5593e-218">Vertex Shader</span></span> | <span data-ttu-id="5593e-219">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="5593e-219">Geometry Shader</span></span> | <span data-ttu-id="5593e-220">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="5593e-220">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="5593e-221">x</span><span class="sxs-lookup"><span data-stu-id="5593e-221">x</span></span>             | <span data-ttu-id="5593e-222">x</span><span class="sxs-lookup"><span data-stu-id="5593e-222">x</span></span>               | <span data-ttu-id="5593e-223">x</span><span class="sxs-lookup"><span data-stu-id="5593e-223">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="5593e-224">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="5593e-224">Minimum Shader Model</span></span>

<span data-ttu-id="5593e-225">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="5593e-225">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="5593e-226">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="5593e-226">Shader Model</span></span>                                              | <span data-ttu-id="5593e-227">Suportado</span><span class="sxs-lookup"><span data-stu-id="5593e-227">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="5593e-228">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="5593e-228">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="5593e-229">sim</span><span class="sxs-lookup"><span data-stu-id="5593e-229">yes</span></span>       |
| [<span data-ttu-id="5593e-230">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="5593e-230">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="5593e-231">sim</span><span class="sxs-lookup"><span data-stu-id="5593e-231">yes</span></span>       |
| [<span data-ttu-id="5593e-232">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="5593e-232">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="5593e-233">sim</span><span class="sxs-lookup"><span data-stu-id="5593e-233">yes</span></span>       |
| [<span data-ttu-id="5593e-234">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5593e-234">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="5593e-235">não</span><span class="sxs-lookup"><span data-stu-id="5593e-235">no</span></span>        |
| [<span data-ttu-id="5593e-236">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5593e-236">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="5593e-237">não</span><span class="sxs-lookup"><span data-stu-id="5593e-237">no</span></span>        |
| [<span data-ttu-id="5593e-238">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5593e-238">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="5593e-239">não</span><span class="sxs-lookup"><span data-stu-id="5593e-239">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="5593e-240">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5593e-240">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5593e-241">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5593e-241">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





