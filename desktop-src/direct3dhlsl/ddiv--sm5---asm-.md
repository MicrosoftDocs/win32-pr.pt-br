---
title: DDIV (SM5-ASM)
description: Computa uma divisão de precisão dupla de um componente.
ms.assetid: 0A67FC35-7F2F-4258-83CE-1CA398E57952
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56f5c3aae9d416d24f41de8d8308c5a69be9d016
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104988567"
---
# <a name="ddiv-sm5---asm"></a><span data-ttu-id="a9f0d-103">DDIV (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="a9f0d-103">ddiv (sm5 - asm)</span></span>

<span data-ttu-id="a9f0d-104">Computa uma divisão de precisão dupla de um componente.</span><span class="sxs-lookup"><span data-stu-id="a9f0d-104">Computes a component-wise double-precision division.</span></span>



| <span data-ttu-id="a9f0d-105">DDIV \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle \] \[ - \] src1 \[ \_ ABS \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="a9f0d-105">ddiv\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\] \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="a9f0d-106">Item</span><span class="sxs-lookup"><span data-stu-id="a9f0d-106">Item</span></span>                                                            | <span data-ttu-id="a9f0d-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="a9f0d-107">Description</span></span>                                                                                   |
|-----------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9f0d-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="a9f0d-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="a9f0d-109">\[no \] resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="a9f0d-109">\[in\] The result of the operation.</span></span> <span data-ttu-id="a9f0d-110">O valor do resultado deve ser preciso para o 0,5 ULP.</span><span class="sxs-lookup"><span data-stu-id="a9f0d-110">The result value must be accurate to 0.5 ULP.</span></span> <br/> |
| <span data-ttu-id="a9f0d-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="a9f0d-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="a9f0d-112">\[no \] dividendo.</span><span class="sxs-lookup"><span data-stu-id="a9f0d-112">\[in\] The dividend.</span></span><br/>                                                               |
| <span data-ttu-id="a9f0d-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="a9f0d-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="a9f0d-114">\[no \] divisor.</span><span class="sxs-lookup"><span data-stu-id="a9f0d-114">\[in\] The divisor.</span></span><br/>                                                                |



 

## <a name="remarks"></a><span data-ttu-id="a9f0d-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="a9f0d-115">Remarks</span></span>

<span data-ttu-id="a9f0d-116">A instrução DDIV será emitida pelo compilador do HLSL sempre que o operador de divisão for usado com duplos.</span><span class="sxs-lookup"><span data-stu-id="a9f0d-116">The DDIV instruction will be emitted by the HLSL compiler whenever the division operator is used with doubles.</span></span> <span data-ttu-id="a9f0d-117">A precisão dessa instrução será necessária para ser 0,5 ULP.</span><span class="sxs-lookup"><span data-stu-id="a9f0d-117">The accuracy of this instruction will be required to be 0.5 ULP.</span></span>

<span data-ttu-id="a9f0d-118">Os sombreadores que usam essa instrução serão marcados com um sinalizador de sombreador que fará com que eles não sejam associados, a menos que todas as condições a seguir sejam atendidas.</span><span class="sxs-lookup"><span data-stu-id="a9f0d-118">Shaders that use this instruction will be marked with a shader flag that will cause them to fail to bind unless all the following conditions are met.</span></span>

-   <span data-ttu-id="a9f0d-119">O sistema dá suporte ao DirectX 11,1.</span><span class="sxs-lookup"><span data-stu-id="a9f0d-119">The system supports DirectX 11.1.</span></span>
-   <span data-ttu-id="a9f0d-120">O sistema inclui um Driver WDDM 1,2.</span><span class="sxs-lookup"><span data-stu-id="a9f0d-120">The system includes a WDDM 1.2 driver.</span></span>
-   <span data-ttu-id="a9f0d-121">O driver fornece suporte para essa instrução por meio de **Opções de D3D11 de dados de recursos do D3D11 \_ \_ \_ \_ . ExtendedDoublesShaderInstructions** definido como **true**.</span><span class="sxs-lookup"><span data-stu-id="a9f0d-121">The driver reports support for this instruction via **D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS.ExtendedDoublesShaderInstructions** set to **TRUE**.</span></span>

<span data-ttu-id="a9f0d-122">A tabela a seguir mostra os resultados btained ao executar a instrução com várias classes de números, supondo que nenhum estouro ou Subfluxo ocorra.</span><span class="sxs-lookup"><span data-stu-id="a9f0d-122">The following table shows the results btained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span>

<span data-ttu-id="a9f0d-123">Nesta tabela, F significa um número real finito.</span><span class="sxs-lookup"><span data-stu-id="a9f0d-123">In this table F means finite-real number.</span></span>



|                     |          |        |          |        |        |          |        |          |         |
|---------------------|----------|--------|----------|--------|--------|----------|--------|----------|---------|
| <span data-ttu-id="a9f0d-124">**src0 src1->**</span><span class="sxs-lookup"><span data-stu-id="a9f0d-124">**src0 src1 ->**</span></span> | <span data-ttu-id="a9f0d-125">**-INF**</span><span class="sxs-lookup"><span data-stu-id="a9f0d-125">**-inf**</span></span> | <span data-ttu-id="a9f0d-126">**-F**</span><span class="sxs-lookup"><span data-stu-id="a9f0d-126">**-F**</span></span> | <span data-ttu-id="a9f0d-127">**-1,0**</span><span class="sxs-lookup"><span data-stu-id="a9f0d-127">**-1.0**</span></span> | <span data-ttu-id="a9f0d-128">**-0**</span><span class="sxs-lookup"><span data-stu-id="a9f0d-128">**-0**</span></span> | <span data-ttu-id="a9f0d-129">**+0**</span><span class="sxs-lookup"><span data-stu-id="a9f0d-129">**+0**</span></span> | <span data-ttu-id="a9f0d-130">**+ 1,0**</span><span class="sxs-lookup"><span data-stu-id="a9f0d-130">**+1.0**</span></span> | <span data-ttu-id="a9f0d-131">**+ F**</span><span class="sxs-lookup"><span data-stu-id="a9f0d-131">**+F**</span></span> | <span data-ttu-id="a9f0d-132">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="a9f0d-132">**+inf**</span></span> | <span data-ttu-id="a9f0d-133">**NaN**</span><span class="sxs-lookup"><span data-stu-id="a9f0d-133">**NaN**</span></span> |
| <span data-ttu-id="a9f0d-134">**-INF**</span><span class="sxs-lookup"><span data-stu-id="a9f0d-134">**-inf**</span></span>            | <span data-ttu-id="a9f0d-135">NaN</span><span class="sxs-lookup"><span data-stu-id="a9f0d-135">NaN</span></span>      | <span data-ttu-id="a9f0d-136">+inf</span><span class="sxs-lookup"><span data-stu-id="a9f0d-136">+inf</span></span>   | <span data-ttu-id="a9f0d-137">+inf</span><span class="sxs-lookup"><span data-stu-id="a9f0d-137">+inf</span></span>     | <span data-ttu-id="a9f0d-138">+inf</span><span class="sxs-lookup"><span data-stu-id="a9f0d-138">+inf</span></span>   | <span data-ttu-id="a9f0d-139">-inf</span><span class="sxs-lookup"><span data-stu-id="a9f0d-139">-inf</span></span>   | <span data-ttu-id="a9f0d-140">-inf</span><span class="sxs-lookup"><span data-stu-id="a9f0d-140">-inf</span></span>     | <span data-ttu-id="a9f0d-141">-inf</span><span class="sxs-lookup"><span data-stu-id="a9f0d-141">-inf</span></span>   | <span data-ttu-id="a9f0d-142">NaN</span><span class="sxs-lookup"><span data-stu-id="a9f0d-142">NaN</span></span>      | <span data-ttu-id="a9f0d-143">NaN</span><span class="sxs-lookup"><span data-stu-id="a9f0d-143">NaN</span></span>     |
| <span data-ttu-id="a9f0d-144">**-F**</span><span class="sxs-lookup"><span data-stu-id="a9f0d-144">**-F**</span></span>              | <span data-ttu-id="a9f0d-145">+0</span><span class="sxs-lookup"><span data-stu-id="a9f0d-145">+0</span></span>       | <span data-ttu-id="a9f0d-146">+ F</span><span class="sxs-lookup"><span data-stu-id="a9f0d-146">+F</span></span>     | <span data-ttu-id="a9f0d-147">-src0</span><span class="sxs-lookup"><span data-stu-id="a9f0d-147">-src0</span></span>    | <span data-ttu-id="a9f0d-148">+inf</span><span class="sxs-lookup"><span data-stu-id="a9f0d-148">+inf</span></span>   | <span data-ttu-id="a9f0d-149">-inf</span><span class="sxs-lookup"><span data-stu-id="a9f0d-149">-inf</span></span>   | <span data-ttu-id="a9f0d-150">src0</span><span class="sxs-lookup"><span data-stu-id="a9f0d-150">src0</span></span>     | <span data-ttu-id="a9f0d-151">-F</span><span class="sxs-lookup"><span data-stu-id="a9f0d-151">-F</span></span>     | <span data-ttu-id="a9f0d-152">-0</span><span class="sxs-lookup"><span data-stu-id="a9f0d-152">-0</span></span>       | <span data-ttu-id="a9f0d-153">NaN</span><span class="sxs-lookup"><span data-stu-id="a9f0d-153">NaN</span></span>     |
| <span data-ttu-id="a9f0d-154">**-0**</span><span class="sxs-lookup"><span data-stu-id="a9f0d-154">**-0**</span></span>              | <span data-ttu-id="a9f0d-155">+0</span><span class="sxs-lookup"><span data-stu-id="a9f0d-155">+0</span></span>       | <span data-ttu-id="a9f0d-156">+0</span><span class="sxs-lookup"><span data-stu-id="a9f0d-156">+0</span></span>     | <span data-ttu-id="a9f0d-157">+0</span><span class="sxs-lookup"><span data-stu-id="a9f0d-157">+0</span></span>       | <span data-ttu-id="a9f0d-158">NaN</span><span class="sxs-lookup"><span data-stu-id="a9f0d-158">NaN</span></span>    | <span data-ttu-id="a9f0d-159">NaN</span><span class="sxs-lookup"><span data-stu-id="a9f0d-159">NaN</span></span>    | <span data-ttu-id="a9f0d-160">-0</span><span class="sxs-lookup"><span data-stu-id="a9f0d-160">-0</span></span>       | <span data-ttu-id="a9f0d-161">-0</span><span class="sxs-lookup"><span data-stu-id="a9f0d-161">-0</span></span>     | <span data-ttu-id="a9f0d-162">-0</span><span class="sxs-lookup"><span data-stu-id="a9f0d-162">-0</span></span>       | <span data-ttu-id="a9f0d-163">NaN</span><span class="sxs-lookup"><span data-stu-id="a9f0d-163">NaN</span></span>     |
| <span data-ttu-id="a9f0d-164">**+0**</span><span class="sxs-lookup"><span data-stu-id="a9f0d-164">**+0**</span></span>              | <span data-ttu-id="a9f0d-165">-0</span><span class="sxs-lookup"><span data-stu-id="a9f0d-165">-0</span></span>       | <span data-ttu-id="a9f0d-166">-0</span><span class="sxs-lookup"><span data-stu-id="a9f0d-166">-0</span></span>     | <span data-ttu-id="a9f0d-167">-0</span><span class="sxs-lookup"><span data-stu-id="a9f0d-167">-0</span></span>       | <span data-ttu-id="a9f0d-168">NaN</span><span class="sxs-lookup"><span data-stu-id="a9f0d-168">NaN</span></span>    | <span data-ttu-id="a9f0d-169">NaN</span><span class="sxs-lookup"><span data-stu-id="a9f0d-169">NaN</span></span>    | <span data-ttu-id="a9f0d-170">+0</span><span class="sxs-lookup"><span data-stu-id="a9f0d-170">+0</span></span>       | <span data-ttu-id="a9f0d-171">+0</span><span class="sxs-lookup"><span data-stu-id="a9f0d-171">+0</span></span>     | <span data-ttu-id="a9f0d-172">+0</span><span class="sxs-lookup"><span data-stu-id="a9f0d-172">+0</span></span>       | <span data-ttu-id="a9f0d-173">NaN</span><span class="sxs-lookup"><span data-stu-id="a9f0d-173">NaN</span></span>     |
| <span data-ttu-id="a9f0d-174">**+ F**</span><span class="sxs-lookup"><span data-stu-id="a9f0d-174">**+F**</span></span>              | <span data-ttu-id="a9f0d-175">-0</span><span class="sxs-lookup"><span data-stu-id="a9f0d-175">-0</span></span>       | <span data-ttu-id="a9f0d-176">-F</span><span class="sxs-lookup"><span data-stu-id="a9f0d-176">-F</span></span>     | <span data-ttu-id="a9f0d-177">-src0</span><span class="sxs-lookup"><span data-stu-id="a9f0d-177">-src0</span></span>    | <span data-ttu-id="a9f0d-178">-inf</span><span class="sxs-lookup"><span data-stu-id="a9f0d-178">-inf</span></span>   | <span data-ttu-id="a9f0d-179">+inf</span><span class="sxs-lookup"><span data-stu-id="a9f0d-179">+inf</span></span>   | <span data-ttu-id="a9f0d-180">src0</span><span class="sxs-lookup"><span data-stu-id="a9f0d-180">src0</span></span>     | <span data-ttu-id="a9f0d-181">+ F</span><span class="sxs-lookup"><span data-stu-id="a9f0d-181">+F</span></span>     | <span data-ttu-id="a9f0d-182">+0</span><span class="sxs-lookup"><span data-stu-id="a9f0d-182">+0</span></span>       | <span data-ttu-id="a9f0d-183">NaN</span><span class="sxs-lookup"><span data-stu-id="a9f0d-183">NaN</span></span>     |
| <span data-ttu-id="a9f0d-184">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="a9f0d-184">**+inf**</span></span>            | <span data-ttu-id="a9f0d-185">NaN</span><span class="sxs-lookup"><span data-stu-id="a9f0d-185">NaN</span></span>      | <span data-ttu-id="a9f0d-186">-inf</span><span class="sxs-lookup"><span data-stu-id="a9f0d-186">-inf</span></span>   | <span data-ttu-id="a9f0d-187">-inf</span><span class="sxs-lookup"><span data-stu-id="a9f0d-187">-inf</span></span>     | <span data-ttu-id="a9f0d-188">-inf</span><span class="sxs-lookup"><span data-stu-id="a9f0d-188">-inf</span></span>   | <span data-ttu-id="a9f0d-189">+inf</span><span class="sxs-lookup"><span data-stu-id="a9f0d-189">+inf</span></span>   | <span data-ttu-id="a9f0d-190">+inf</span><span class="sxs-lookup"><span data-stu-id="a9f0d-190">+inf</span></span>     | <span data-ttu-id="a9f0d-191">+inf</span><span class="sxs-lookup"><span data-stu-id="a9f0d-191">+inf</span></span>   | <span data-ttu-id="a9f0d-192">NaN</span><span class="sxs-lookup"><span data-stu-id="a9f0d-192">NaN</span></span>      | <span data-ttu-id="a9f0d-193">NaN</span><span class="sxs-lookup"><span data-stu-id="a9f0d-193">NaN</span></span>     |
| <span data-ttu-id="a9f0d-194">**NaN**</span><span class="sxs-lookup"><span data-stu-id="a9f0d-194">**NaN**</span></span>             | <span data-ttu-id="a9f0d-195">NaN</span><span class="sxs-lookup"><span data-stu-id="a9f0d-195">NaN</span></span>      | <span data-ttu-id="a9f0d-196">NaN</span><span class="sxs-lookup"><span data-stu-id="a9f0d-196">NaN</span></span>    | <span data-ttu-id="a9f0d-197">NaN</span><span class="sxs-lookup"><span data-stu-id="a9f0d-197">NaN</span></span>      | <span data-ttu-id="a9f0d-198">NaN</span><span class="sxs-lookup"><span data-stu-id="a9f0d-198">NaN</span></span>    | <span data-ttu-id="a9f0d-199">NaN</span><span class="sxs-lookup"><span data-stu-id="a9f0d-199">NaN</span></span>    | <span data-ttu-id="a9f0d-200">NaN</span><span class="sxs-lookup"><span data-stu-id="a9f0d-200">NaN</span></span>      | <span data-ttu-id="a9f0d-201">NaN</span><span class="sxs-lookup"><span data-stu-id="a9f0d-201">NaN</span></span>    | <span data-ttu-id="a9f0d-202">NaN</span><span class="sxs-lookup"><span data-stu-id="a9f0d-202">NaN</span></span>      | <span data-ttu-id="a9f0d-203">NaN</span><span class="sxs-lookup"><span data-stu-id="a9f0d-203">NaN</span></span>     |



 

<span data-ttu-id="a9f0d-204">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="a9f0d-204">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="a9f0d-205">Vértice</span><span class="sxs-lookup"><span data-stu-id="a9f0d-205">Vertex</span></span> | <span data-ttu-id="a9f0d-206">Envoltória</span><span class="sxs-lookup"><span data-stu-id="a9f0d-206">Hull</span></span> | <span data-ttu-id="a9f0d-207">Domínio</span><span class="sxs-lookup"><span data-stu-id="a9f0d-207">Domain</span></span> | <span data-ttu-id="a9f0d-208">Geometria</span><span class="sxs-lookup"><span data-stu-id="a9f0d-208">Geometry</span></span> | <span data-ttu-id="a9f0d-209">16x16</span><span class="sxs-lookup"><span data-stu-id="a9f0d-209">Pixel</span></span> | <span data-ttu-id="a9f0d-210">Computação</span><span class="sxs-lookup"><span data-stu-id="a9f0d-210">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="a9f0d-211">X</span><span class="sxs-lookup"><span data-stu-id="a9f0d-211">X</span></span>      | <span data-ttu-id="a9f0d-212">X</span><span class="sxs-lookup"><span data-stu-id="a9f0d-212">X</span></span>    | <span data-ttu-id="a9f0d-213">X</span><span class="sxs-lookup"><span data-stu-id="a9f0d-213">X</span></span>      | <span data-ttu-id="a9f0d-214">X</span><span class="sxs-lookup"><span data-stu-id="a9f0d-214">X</span></span>        | <span data-ttu-id="a9f0d-215">X</span><span class="sxs-lookup"><span data-stu-id="a9f0d-215">X</span></span>     | <span data-ttu-id="a9f0d-216">X</span><span class="sxs-lookup"><span data-stu-id="a9f0d-216">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="a9f0d-217">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="a9f0d-217">Minimum Shader Model</span></span>

<span data-ttu-id="a9f0d-218">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="a9f0d-218">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="a9f0d-219">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="a9f0d-219">Shader Model</span></span>                                              | <span data-ttu-id="a9f0d-220">Com suporte</span><span class="sxs-lookup"><span data-stu-id="a9f0d-220">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="a9f0d-221">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="a9f0d-221">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="a9f0d-222">sim</span><span class="sxs-lookup"><span data-stu-id="a9f0d-222">yes</span></span>       |
| [<span data-ttu-id="a9f0d-223">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="a9f0d-223">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="a9f0d-224">não</span><span class="sxs-lookup"><span data-stu-id="a9f0d-224">no</span></span>        |
| [<span data-ttu-id="a9f0d-225">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="a9f0d-225">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="a9f0d-226">não</span><span class="sxs-lookup"><span data-stu-id="a9f0d-226">no</span></span>        |
| [<span data-ttu-id="a9f0d-227">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a9f0d-227">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="a9f0d-228">não</span><span class="sxs-lookup"><span data-stu-id="a9f0d-228">no</span></span>        |
| [<span data-ttu-id="a9f0d-229">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a9f0d-229">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="a9f0d-230">não</span><span class="sxs-lookup"><span data-stu-id="a9f0d-230">no</span></span>        |
| [<span data-ttu-id="a9f0d-231">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a9f0d-231">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="a9f0d-232">não</span><span class="sxs-lookup"><span data-stu-id="a9f0d-232">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="a9f0d-233">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a9f0d-233">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9f0d-234">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a9f0d-234">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





