---
title: DDIV (SM5-ASM)
description: Computa uma divisão de precisão dupla de um componente.
ms.assetid: 0A67FC35-7F2F-4258-83CE-1CA398E57952
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81fc039b222b28a5fb1217d23c78470aff1739f7
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999153"
---
# <a name="ddiv-sm5---asm"></a><span data-ttu-id="e8f99-103">DDIV (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="e8f99-103">ddiv (sm5 - asm)</span></span>

<span data-ttu-id="e8f99-104">Computa uma divisão de precisão dupla de um componente.</span><span class="sxs-lookup"><span data-stu-id="e8f99-104">Computes a component-wise double-precision division.</span></span>



| <span data-ttu-id="e8f99-105">DDIV \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle \] \[ - \] src1 \[ \_ ABS \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="e8f99-105">ddiv\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\] \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="e8f99-106">Item</span><span class="sxs-lookup"><span data-stu-id="e8f99-106">Item</span></span>                                                            | <span data-ttu-id="e8f99-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="e8f99-107">Description</span></span>                                                                                   |
|-----------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8f99-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="e8f99-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="e8f99-109">\[no \] resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="e8f99-109">\[in\] The result of the operation.</span></span> <span data-ttu-id="e8f99-110">O valor do resultado deve ser preciso para o 0,5 ULP.</span><span class="sxs-lookup"><span data-stu-id="e8f99-110">The result value must be accurate to 0.5 ULP.</span></span> <br/> |
| <span data-ttu-id="e8f99-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="e8f99-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="e8f99-112">\[no \] dividendo.</span><span class="sxs-lookup"><span data-stu-id="e8f99-112">\[in\] The dividend.</span></span><br/>                                                               |
| <span data-ttu-id="e8f99-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="e8f99-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="e8f99-114">\[no \] divisor.</span><span class="sxs-lookup"><span data-stu-id="e8f99-114">\[in\] The divisor.</span></span><br/>                                                                |



 

## <a name="remarks"></a><span data-ttu-id="e8f99-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="e8f99-115">Remarks</span></span>

<span data-ttu-id="e8f99-116">A instrução DDIV será emitida pelo compilador do HLSL sempre que o operador de divisão for usado com duplos.</span><span class="sxs-lookup"><span data-stu-id="e8f99-116">The DDIV instruction will be emitted by the HLSL compiler whenever the division operator is used with doubles.</span></span> <span data-ttu-id="e8f99-117">A precisão dessa instrução será necessária para ser 0,5 ULP.</span><span class="sxs-lookup"><span data-stu-id="e8f99-117">The accuracy of this instruction will be required to be 0.5 ULP.</span></span>

<span data-ttu-id="e8f99-118">Os sombreadores que usam essa instrução serão marcados com um sinalizador de sombreador que fará com que eles não sejam associados, a menos que todas as condições a seguir sejam atendidas.</span><span class="sxs-lookup"><span data-stu-id="e8f99-118">Shaders that use this instruction will be marked with a shader flag that will cause them to fail to bind unless all the following conditions are met.</span></span>

-   <span data-ttu-id="e8f99-119">O sistema dá suporte ao DirectX 11,1.</span><span class="sxs-lookup"><span data-stu-id="e8f99-119">The system supports DirectX 11.1.</span></span>
-   <span data-ttu-id="e8f99-120">O sistema inclui um Driver WDDM 1,2.</span><span class="sxs-lookup"><span data-stu-id="e8f99-120">The system includes a WDDM 1.2 driver.</span></span>
-   <span data-ttu-id="e8f99-121">O driver fornece suporte para essa instrução por meio de **Opções de D3D11 de dados de recursos do D3D11 \_ \_ \_ \_ . ExtendedDoublesShaderInstructions** definido como **true**.</span><span class="sxs-lookup"><span data-stu-id="e8f99-121">The driver reports support for this instruction via **D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS.ExtendedDoublesShaderInstructions** set to **TRUE**.</span></span>

<span data-ttu-id="e8f99-122">A tabela a seguir mostra os resultados btained ao executar a instrução com várias classes de números, supondo que nenhum estouro ou Subfluxo ocorra.</span><span class="sxs-lookup"><span data-stu-id="e8f99-122">The following table shows the results btained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span>

<span data-ttu-id="e8f99-123">Nesta tabela, F significa um número real finito.</span><span class="sxs-lookup"><span data-stu-id="e8f99-123">In this table F means finite-real number.</span></span>



| <span data-ttu-id="e8f99-124">**src0 src1->**</span><span class="sxs-lookup"><span data-stu-id="e8f99-124">**src0 src1 ->**</span></span> | <span data-ttu-id="e8f99-125">**-INF**</span><span class="sxs-lookup"><span data-stu-id="e8f99-125">**-inf**</span></span> | <span data-ttu-id="e8f99-126">**-F**</span><span class="sxs-lookup"><span data-stu-id="e8f99-126">**-F**</span></span> | <span data-ttu-id="e8f99-127">**-1,0**</span><span class="sxs-lookup"><span data-stu-id="e8f99-127">**-1.0**</span></span> | <span data-ttu-id="e8f99-128">**-0**</span><span class="sxs-lookup"><span data-stu-id="e8f99-128">**-0**</span></span> | <span data-ttu-id="e8f99-129">**+0**</span><span class="sxs-lookup"><span data-stu-id="e8f99-129">**+0**</span></span> | <span data-ttu-id="e8f99-130">**+ 1,0**</span><span class="sxs-lookup"><span data-stu-id="e8f99-130">**+1.0**</span></span> | <span data-ttu-id="e8f99-131">**+ F**</span><span class="sxs-lookup"><span data-stu-id="e8f99-131">**+F**</span></span> | <span data-ttu-id="e8f99-132">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="e8f99-132">**+inf**</span></span> | <span data-ttu-id="e8f99-133">**NaN**</span><span class="sxs-lookup"><span data-stu-id="e8f99-133">**NaN**</span></span> |
|---------------------|----------|--------|----------|--------|--------|----------|--------|----------|---------|
| <span data-ttu-id="e8f99-134">**-INF**</span><span class="sxs-lookup"><span data-stu-id="e8f99-134">**-inf**</span></span>            | <span data-ttu-id="e8f99-135">NaN</span><span class="sxs-lookup"><span data-stu-id="e8f99-135">NaN</span></span>      | <span data-ttu-id="e8f99-136">+inf</span><span class="sxs-lookup"><span data-stu-id="e8f99-136">+inf</span></span>   | <span data-ttu-id="e8f99-137">+inf</span><span class="sxs-lookup"><span data-stu-id="e8f99-137">+inf</span></span>     | <span data-ttu-id="e8f99-138">+inf</span><span class="sxs-lookup"><span data-stu-id="e8f99-138">+inf</span></span>   | <span data-ttu-id="e8f99-139">-inf</span><span class="sxs-lookup"><span data-stu-id="e8f99-139">-inf</span></span>   | <span data-ttu-id="e8f99-140">-inf</span><span class="sxs-lookup"><span data-stu-id="e8f99-140">-inf</span></span>     | <span data-ttu-id="e8f99-141">-inf</span><span class="sxs-lookup"><span data-stu-id="e8f99-141">-inf</span></span>   | <span data-ttu-id="e8f99-142">NaN</span><span class="sxs-lookup"><span data-stu-id="e8f99-142">NaN</span></span>      | <span data-ttu-id="e8f99-143">NaN</span><span class="sxs-lookup"><span data-stu-id="e8f99-143">NaN</span></span>     |
| <span data-ttu-id="e8f99-144">**-F**</span><span class="sxs-lookup"><span data-stu-id="e8f99-144">**-F**</span></span>              | <span data-ttu-id="e8f99-145">+0</span><span class="sxs-lookup"><span data-stu-id="e8f99-145">+0</span></span>       | <span data-ttu-id="e8f99-146">+ F</span><span class="sxs-lookup"><span data-stu-id="e8f99-146">+F</span></span>     | <span data-ttu-id="e8f99-147">-src0</span><span class="sxs-lookup"><span data-stu-id="e8f99-147">-src0</span></span>    | <span data-ttu-id="e8f99-148">+inf</span><span class="sxs-lookup"><span data-stu-id="e8f99-148">+inf</span></span>   | <span data-ttu-id="e8f99-149">-inf</span><span class="sxs-lookup"><span data-stu-id="e8f99-149">-inf</span></span>   | <span data-ttu-id="e8f99-150">src0</span><span class="sxs-lookup"><span data-stu-id="e8f99-150">src0</span></span>     | <span data-ttu-id="e8f99-151">-F</span><span class="sxs-lookup"><span data-stu-id="e8f99-151">-F</span></span>     | <span data-ttu-id="e8f99-152">-0</span><span class="sxs-lookup"><span data-stu-id="e8f99-152">-0</span></span>       | <span data-ttu-id="e8f99-153">NaN</span><span class="sxs-lookup"><span data-stu-id="e8f99-153">NaN</span></span>     |
| <span data-ttu-id="e8f99-154">**-0**</span><span class="sxs-lookup"><span data-stu-id="e8f99-154">**-0**</span></span>              | <span data-ttu-id="e8f99-155">+0</span><span class="sxs-lookup"><span data-stu-id="e8f99-155">+0</span></span>       | <span data-ttu-id="e8f99-156">+0</span><span class="sxs-lookup"><span data-stu-id="e8f99-156">+0</span></span>     | <span data-ttu-id="e8f99-157">+0</span><span class="sxs-lookup"><span data-stu-id="e8f99-157">+0</span></span>       | <span data-ttu-id="e8f99-158">NaN</span><span class="sxs-lookup"><span data-stu-id="e8f99-158">NaN</span></span>    | <span data-ttu-id="e8f99-159">NaN</span><span class="sxs-lookup"><span data-stu-id="e8f99-159">NaN</span></span>    | <span data-ttu-id="e8f99-160">-0</span><span class="sxs-lookup"><span data-stu-id="e8f99-160">-0</span></span>       | <span data-ttu-id="e8f99-161">-0</span><span class="sxs-lookup"><span data-stu-id="e8f99-161">-0</span></span>     | <span data-ttu-id="e8f99-162">-0</span><span class="sxs-lookup"><span data-stu-id="e8f99-162">-0</span></span>       | <span data-ttu-id="e8f99-163">NaN</span><span class="sxs-lookup"><span data-stu-id="e8f99-163">NaN</span></span>     |
| <span data-ttu-id="e8f99-164">**+0**</span><span class="sxs-lookup"><span data-stu-id="e8f99-164">**+0**</span></span>              | <span data-ttu-id="e8f99-165">-0</span><span class="sxs-lookup"><span data-stu-id="e8f99-165">-0</span></span>       | <span data-ttu-id="e8f99-166">-0</span><span class="sxs-lookup"><span data-stu-id="e8f99-166">-0</span></span>     | <span data-ttu-id="e8f99-167">-0</span><span class="sxs-lookup"><span data-stu-id="e8f99-167">-0</span></span>       | <span data-ttu-id="e8f99-168">NaN</span><span class="sxs-lookup"><span data-stu-id="e8f99-168">NaN</span></span>    | <span data-ttu-id="e8f99-169">NaN</span><span class="sxs-lookup"><span data-stu-id="e8f99-169">NaN</span></span>    | <span data-ttu-id="e8f99-170">+0</span><span class="sxs-lookup"><span data-stu-id="e8f99-170">+0</span></span>       | <span data-ttu-id="e8f99-171">+0</span><span class="sxs-lookup"><span data-stu-id="e8f99-171">+0</span></span>     | <span data-ttu-id="e8f99-172">+0</span><span class="sxs-lookup"><span data-stu-id="e8f99-172">+0</span></span>       | <span data-ttu-id="e8f99-173">NaN</span><span class="sxs-lookup"><span data-stu-id="e8f99-173">NaN</span></span>     |
| <span data-ttu-id="e8f99-174">**+ F**</span><span class="sxs-lookup"><span data-stu-id="e8f99-174">**+F**</span></span>              | <span data-ttu-id="e8f99-175">-0</span><span class="sxs-lookup"><span data-stu-id="e8f99-175">-0</span></span>       | <span data-ttu-id="e8f99-176">-F</span><span class="sxs-lookup"><span data-stu-id="e8f99-176">-F</span></span>     | <span data-ttu-id="e8f99-177">-src0</span><span class="sxs-lookup"><span data-stu-id="e8f99-177">-src0</span></span>    | <span data-ttu-id="e8f99-178">-inf</span><span class="sxs-lookup"><span data-stu-id="e8f99-178">-inf</span></span>   | <span data-ttu-id="e8f99-179">+inf</span><span class="sxs-lookup"><span data-stu-id="e8f99-179">+inf</span></span>   | <span data-ttu-id="e8f99-180">src0</span><span class="sxs-lookup"><span data-stu-id="e8f99-180">src0</span></span>     | <span data-ttu-id="e8f99-181">+ F</span><span class="sxs-lookup"><span data-stu-id="e8f99-181">+F</span></span>     | <span data-ttu-id="e8f99-182">+0</span><span class="sxs-lookup"><span data-stu-id="e8f99-182">+0</span></span>       | <span data-ttu-id="e8f99-183">NaN</span><span class="sxs-lookup"><span data-stu-id="e8f99-183">NaN</span></span>     |
| <span data-ttu-id="e8f99-184">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="e8f99-184">**+inf**</span></span>            | <span data-ttu-id="e8f99-185">NaN</span><span class="sxs-lookup"><span data-stu-id="e8f99-185">NaN</span></span>      | <span data-ttu-id="e8f99-186">-inf</span><span class="sxs-lookup"><span data-stu-id="e8f99-186">-inf</span></span>   | <span data-ttu-id="e8f99-187">-inf</span><span class="sxs-lookup"><span data-stu-id="e8f99-187">-inf</span></span>     | <span data-ttu-id="e8f99-188">-inf</span><span class="sxs-lookup"><span data-stu-id="e8f99-188">-inf</span></span>   | <span data-ttu-id="e8f99-189">+inf</span><span class="sxs-lookup"><span data-stu-id="e8f99-189">+inf</span></span>   | <span data-ttu-id="e8f99-190">+inf</span><span class="sxs-lookup"><span data-stu-id="e8f99-190">+inf</span></span>     | <span data-ttu-id="e8f99-191">+inf</span><span class="sxs-lookup"><span data-stu-id="e8f99-191">+inf</span></span>   | <span data-ttu-id="e8f99-192">NaN</span><span class="sxs-lookup"><span data-stu-id="e8f99-192">NaN</span></span>      | <span data-ttu-id="e8f99-193">NaN</span><span class="sxs-lookup"><span data-stu-id="e8f99-193">NaN</span></span>     |
| <span data-ttu-id="e8f99-194">**NaN**</span><span class="sxs-lookup"><span data-stu-id="e8f99-194">**NaN**</span></span>             | <span data-ttu-id="e8f99-195">NaN</span><span class="sxs-lookup"><span data-stu-id="e8f99-195">NaN</span></span>      | <span data-ttu-id="e8f99-196">NaN</span><span class="sxs-lookup"><span data-stu-id="e8f99-196">NaN</span></span>    | <span data-ttu-id="e8f99-197">NaN</span><span class="sxs-lookup"><span data-stu-id="e8f99-197">NaN</span></span>      | <span data-ttu-id="e8f99-198">NaN</span><span class="sxs-lookup"><span data-stu-id="e8f99-198">NaN</span></span>    | <span data-ttu-id="e8f99-199">NaN</span><span class="sxs-lookup"><span data-stu-id="e8f99-199">NaN</span></span>    | <span data-ttu-id="e8f99-200">NaN</span><span class="sxs-lookup"><span data-stu-id="e8f99-200">NaN</span></span>      | <span data-ttu-id="e8f99-201">NaN</span><span class="sxs-lookup"><span data-stu-id="e8f99-201">NaN</span></span>    | <span data-ttu-id="e8f99-202">NaN</span><span class="sxs-lookup"><span data-stu-id="e8f99-202">NaN</span></span>      | <span data-ttu-id="e8f99-203">NaN</span><span class="sxs-lookup"><span data-stu-id="e8f99-203">NaN</span></span>     |



 

<span data-ttu-id="e8f99-204">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="e8f99-204">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="e8f99-205">Vértice</span><span class="sxs-lookup"><span data-stu-id="e8f99-205">Vertex</span></span> | <span data-ttu-id="e8f99-206">Envoltória</span><span class="sxs-lookup"><span data-stu-id="e8f99-206">Hull</span></span> | <span data-ttu-id="e8f99-207">Domain</span><span class="sxs-lookup"><span data-stu-id="e8f99-207">Domain</span></span> | <span data-ttu-id="e8f99-208">Geometria</span><span class="sxs-lookup"><span data-stu-id="e8f99-208">Geometry</span></span> | <span data-ttu-id="e8f99-209">16x16</span><span class="sxs-lookup"><span data-stu-id="e8f99-209">Pixel</span></span> | <span data-ttu-id="e8f99-210">Computação</span><span class="sxs-lookup"><span data-stu-id="e8f99-210">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="e8f99-211">X</span><span class="sxs-lookup"><span data-stu-id="e8f99-211">X</span></span>      | <span data-ttu-id="e8f99-212">X</span><span class="sxs-lookup"><span data-stu-id="e8f99-212">X</span></span>    | <span data-ttu-id="e8f99-213">X</span><span class="sxs-lookup"><span data-stu-id="e8f99-213">X</span></span>      | <span data-ttu-id="e8f99-214">X</span><span class="sxs-lookup"><span data-stu-id="e8f99-214">X</span></span>        | <span data-ttu-id="e8f99-215">X</span><span class="sxs-lookup"><span data-stu-id="e8f99-215">X</span></span>     | <span data-ttu-id="e8f99-216">X</span><span class="sxs-lookup"><span data-stu-id="e8f99-216">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="e8f99-217">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="e8f99-217">Minimum Shader Model</span></span>

<span data-ttu-id="e8f99-218">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="e8f99-218">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="e8f99-219">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="e8f99-219">Shader Model</span></span>                                              | <span data-ttu-id="e8f99-220">Suportado</span><span class="sxs-lookup"><span data-stu-id="e8f99-220">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="e8f99-221">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="e8f99-221">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="e8f99-222">sim</span><span class="sxs-lookup"><span data-stu-id="e8f99-222">yes</span></span>       |
| [<span data-ttu-id="e8f99-223">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="e8f99-223">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="e8f99-224">não</span><span class="sxs-lookup"><span data-stu-id="e8f99-224">no</span></span>        |
| [<span data-ttu-id="e8f99-225">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="e8f99-225">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="e8f99-226">não</span><span class="sxs-lookup"><span data-stu-id="e8f99-226">no</span></span>        |
| [<span data-ttu-id="e8f99-227">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e8f99-227">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="e8f99-228">não</span><span class="sxs-lookup"><span data-stu-id="e8f99-228">no</span></span>        |
| [<span data-ttu-id="e8f99-229">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e8f99-229">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="e8f99-230">não</span><span class="sxs-lookup"><span data-stu-id="e8f99-230">no</span></span>        |
| [<span data-ttu-id="e8f99-231">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e8f99-231">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="e8f99-232">não</span><span class="sxs-lookup"><span data-stu-id="e8f99-232">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="e8f99-233">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e8f99-233">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8f99-234">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e8f99-234">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





