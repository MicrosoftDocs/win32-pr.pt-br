---
title: Dadd (SM5-ASM)
description: Adição de precisão dupla por componente.
ms.assetid: 416F1103-E27B-4AFC-9ED1-492FF8A93492
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e217a03a5ba9e4da0d365bbfd15e4283f1a69cb
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104365192"
---
# <a name="dadd-sm5---asm"></a><span data-ttu-id="1115b-103">Dadd (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="1115b-103">dadd (sm5 - asm)</span></span>

<span data-ttu-id="1115b-104">Adição de precisão dupla por componente.</span><span class="sxs-lookup"><span data-stu-id="1115b-104">Component-wise double-precision add.</span></span>



| <span data-ttu-id="1115b-105">Dadd \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="1115b-105">dadd\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|---------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="1115b-106">Item</span><span class="sxs-lookup"><span data-stu-id="1115b-106">Item</span></span>                                                            | <span data-ttu-id="1115b-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="1115b-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="1115b-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="1115b-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="1115b-109">\[no \] endereço do resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="1115b-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="1115b-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="1115b-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="1115b-111">\[nos \] componentes a serem adicionados com *src1*.</span><span class="sxs-lookup"><span data-stu-id="1115b-111">\[in\] The components to add with *src1*.</span></span><br/>          |
| <span data-ttu-id="1115b-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="1115b-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="1115b-113">\[nos \] componentes a serem adicionados com *src0*</span><span class="sxs-lookup"><span data-stu-id="1115b-113">\[in\] The components to add with *src0*</span></span><br/>           |



 

## <a name="remarks"></a><span data-ttu-id="1115b-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="1115b-114">Remarks</span></span>

<span data-ttu-id="1115b-115">O swizzles válido para os parâmetros de origem são. xyzw,. xyxy,. zwxy,. zwzw.</span><span class="sxs-lookup"><span data-stu-id="1115b-115">The valid swizzles for the source parameters are .xyzw, .xyxy, .zwxy, .zwzw.</span></span> <span data-ttu-id="1115b-116">As máscaras de *destino* válidas são. XY,. zw e. xyzw.</span><span class="sxs-lookup"><span data-stu-id="1115b-116">The valid *dest* masks are .xy, .zw, and .xyzw.</span></span> <span data-ttu-id="1115b-117">Os seguintes mapeamentos são swizzle:</span><span class="sxs-lookup"><span data-stu-id="1115b-117">The following mappings are post-swizzle:</span></span>

-   <span data-ttu-id="1115b-118">*dest* é um vec2 duplo entre (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="1115b-118">*dest* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="1115b-119">*src0* é um vec2 duplo entre (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="1115b-119">*src0* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="1115b-120">*src1* é um vec2 duplo entre (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="1115b-120">*src1* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>

<span data-ttu-id="1115b-121">A tabela a seguir mostra os resultados obtidos ao executar a instrução com várias classes de números, supondo que nenhum estouro ou Subfluxo ocorra.</span><span class="sxs-lookup"><span data-stu-id="1115b-121">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span>

<span data-ttu-id="1115b-122">F significa número real finito.</span><span class="sxs-lookup"><span data-stu-id="1115b-122">F means finite-real number.</span></span>



<table>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="1115b-123"><strong>src0</strong></span><span class="sxs-lookup"><span data-stu-id="1115b-123"><strong>src0</strong></span></span><br /><span data-ttu-id="1115b-124">
<strong>src1-></strong></span><span class="sxs-lookup"><span data-stu-id="1115b-124">
<strong>src1-></strong></span></span><br />
</dl></td>
<td><span data-ttu-id="1115b-125"><strong>-INF</strong></span><span class="sxs-lookup"><span data-stu-id="1115b-125"><strong>-inf</strong></span></span></td>
<td><span data-ttu-id="1115b-126"><strong>-F</strong></span><span class="sxs-lookup"><span data-stu-id="1115b-126"><strong>-F</strong></span></span></td>
<td><span data-ttu-id="1115b-127"><strong>-0</strong></span><span class="sxs-lookup"><span data-stu-id="1115b-127"><strong>-0</strong></span></span></td>
<td><span data-ttu-id="1115b-128"><strong>+0</strong></span><span class="sxs-lookup"><span data-stu-id="1115b-128"><strong>+0</strong></span></span></td>
<td><span data-ttu-id="1115b-129"><strong>+ F</strong></span><span class="sxs-lookup"><span data-stu-id="1115b-129"><strong>+F</strong></span></span></td>
<td><span data-ttu-id="1115b-130"><strong>+ INF</strong></span><span class="sxs-lookup"><span data-stu-id="1115b-130"><strong>+inf</strong></span></span></td>
<td><span data-ttu-id="1115b-131"><strong>NaN</strong></span><span class="sxs-lookup"><span data-stu-id="1115b-131"><strong>NaN</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1115b-132"><strong>-INF</strong></span><span class="sxs-lookup"><span data-stu-id="1115b-132"><strong>-inf</strong></span></span></td>
<td><span data-ttu-id="1115b-133">-inf</span><span class="sxs-lookup"><span data-stu-id="1115b-133">-inf</span></span></td>
<td><span data-ttu-id="1115b-134">-inf</span><span class="sxs-lookup"><span data-stu-id="1115b-134">-inf</span></span></td>
<td><span data-ttu-id="1115b-135">-inf</span><span class="sxs-lookup"><span data-stu-id="1115b-135">-inf</span></span></td>
<td><span data-ttu-id="1115b-136">-inf</span><span class="sxs-lookup"><span data-stu-id="1115b-136">-inf</span></span></td>
<td><span data-ttu-id="1115b-137">-inf</span><span class="sxs-lookup"><span data-stu-id="1115b-137">-inf</span></span></td>
<td><span data-ttu-id="1115b-138">NaN</span><span class="sxs-lookup"><span data-stu-id="1115b-138">NaN</span></span></td>
<td><span data-ttu-id="1115b-139">NaN</span><span class="sxs-lookup"><span data-stu-id="1115b-139">NaN</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1115b-140"><strong>-F</strong></span><span class="sxs-lookup"><span data-stu-id="1115b-140"><strong>-F</strong></span></span></td>
<td><span data-ttu-id="1115b-141">-inf</span><span class="sxs-lookup"><span data-stu-id="1115b-141">-inf</span></span></td>
<td><span data-ttu-id="1115b-142">-F</span><span class="sxs-lookup"><span data-stu-id="1115b-142">-F</span></span></td>
<td><span data-ttu-id="1115b-143">src0</span><span class="sxs-lookup"><span data-stu-id="1115b-143">src0</span></span></td>
<td><span data-ttu-id="1115b-144">src0</span><span class="sxs-lookup"><span data-stu-id="1115b-144">src0</span></span></td>
<td><span data-ttu-id="1115b-145">+-F ou +-0</span><span class="sxs-lookup"><span data-stu-id="1115b-145">+-F or +-0</span></span></td>
<td><span data-ttu-id="1115b-146">+inf</span><span class="sxs-lookup"><span data-stu-id="1115b-146">+inf</span></span></td>
<td><span data-ttu-id="1115b-147">NaN</span><span class="sxs-lookup"><span data-stu-id="1115b-147">NaN</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1115b-148"><strong>-0</strong></span><span class="sxs-lookup"><span data-stu-id="1115b-148"><strong>-0</strong></span></span></td>
<td><span data-ttu-id="1115b-149">-inf</span><span class="sxs-lookup"><span data-stu-id="1115b-149">-inf</span></span></td>
<td><span data-ttu-id="1115b-150">src1</span><span class="sxs-lookup"><span data-stu-id="1115b-150">src1</span></span></td>
<td><span data-ttu-id="1115b-151">-0</span><span class="sxs-lookup"><span data-stu-id="1115b-151">-0</span></span></td>
<td><span data-ttu-id="1115b-152">+0</span><span class="sxs-lookup"><span data-stu-id="1115b-152">+0</span></span></td>
<td><span data-ttu-id="1115b-153">src1</span><span class="sxs-lookup"><span data-stu-id="1115b-153">src1</span></span></td>
<td><span data-ttu-id="1115b-154">+inf</span><span class="sxs-lookup"><span data-stu-id="1115b-154">+inf</span></span></td>
<td><span data-ttu-id="1115b-155">NaN</span><span class="sxs-lookup"><span data-stu-id="1115b-155">NaN</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1115b-156"><strong>+0</strong></span><span class="sxs-lookup"><span data-stu-id="1115b-156"><strong>+0</strong></span></span></td>
<td><span data-ttu-id="1115b-157">-inf</span><span class="sxs-lookup"><span data-stu-id="1115b-157">-inf</span></span></td>
<td><span data-ttu-id="1115b-158">src1</span><span class="sxs-lookup"><span data-stu-id="1115b-158">src1</span></span></td>
<td><span data-ttu-id="1115b-159">+0</span><span class="sxs-lookup"><span data-stu-id="1115b-159">+0</span></span></td>
<td><span data-ttu-id="1115b-160">+0</span><span class="sxs-lookup"><span data-stu-id="1115b-160">+0</span></span></td>
<td><span data-ttu-id="1115b-161">src1</span><span class="sxs-lookup"><span data-stu-id="1115b-161">src1</span></span></td>
<td><span data-ttu-id="1115b-162">+inf</span><span class="sxs-lookup"><span data-stu-id="1115b-162">+inf</span></span></td>
<td><span data-ttu-id="1115b-163">NaN</span><span class="sxs-lookup"><span data-stu-id="1115b-163">NaN</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1115b-164"><strong>+ F</strong></span><span class="sxs-lookup"><span data-stu-id="1115b-164"><strong>+F</strong></span></span></td>
<td><span data-ttu-id="1115b-165">-inf</span><span class="sxs-lookup"><span data-stu-id="1115b-165">-inf</span></span></td>
<td><span data-ttu-id="1115b-166">+-F ou +-0</span><span class="sxs-lookup"><span data-stu-id="1115b-166">+-F or +-0</span></span></td>
<td><span data-ttu-id="1115b-167">src0</span><span class="sxs-lookup"><span data-stu-id="1115b-167">src0</span></span></td>
<td><span data-ttu-id="1115b-168">src0</span><span class="sxs-lookup"><span data-stu-id="1115b-168">src0</span></span></td>
<td><span data-ttu-id="1115b-169">+ F</span><span class="sxs-lookup"><span data-stu-id="1115b-169">+F</span></span></td>
<td><span data-ttu-id="1115b-170">+inf</span><span class="sxs-lookup"><span data-stu-id="1115b-170">+inf</span></span></td>
<td><span data-ttu-id="1115b-171">NaN</span><span class="sxs-lookup"><span data-stu-id="1115b-171">NaN</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1115b-172"><strong>+ INF</strong></span><span class="sxs-lookup"><span data-stu-id="1115b-172"><strong>+inf</strong></span></span></td>
<td><span data-ttu-id="1115b-173">NaN</span><span class="sxs-lookup"><span data-stu-id="1115b-173">NaN</span></span></td>
<td><span data-ttu-id="1115b-174">+inf</span><span class="sxs-lookup"><span data-stu-id="1115b-174">+inf</span></span></td>
<td><span data-ttu-id="1115b-175">+inf</span><span class="sxs-lookup"><span data-stu-id="1115b-175">+inf</span></span></td>
<td><span data-ttu-id="1115b-176">+inf</span><span class="sxs-lookup"><span data-stu-id="1115b-176">+inf</span></span></td>
<td><span data-ttu-id="1115b-177">+inf</span><span class="sxs-lookup"><span data-stu-id="1115b-177">+inf</span></span></td>
<td><span data-ttu-id="1115b-178">+inf</span><span class="sxs-lookup"><span data-stu-id="1115b-178">+inf</span></span></td>
<td><span data-ttu-id="1115b-179">NaN</span><span class="sxs-lookup"><span data-stu-id="1115b-179">NaN</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1115b-180"><strong>NaN</strong></span><span class="sxs-lookup"><span data-stu-id="1115b-180"><strong>NaN</strong></span></span></td>
<td><span data-ttu-id="1115b-181">NaN</span><span class="sxs-lookup"><span data-stu-id="1115b-181">NaN</span></span></td>
<td><span data-ttu-id="1115b-182">NaN</span><span class="sxs-lookup"><span data-stu-id="1115b-182">NaN</span></span></td>
<td><span data-ttu-id="1115b-183">NaN</span><span class="sxs-lookup"><span data-stu-id="1115b-183">NaN</span></span></td>
<td><span data-ttu-id="1115b-184">NaN</span><span class="sxs-lookup"><span data-stu-id="1115b-184">NaN</span></span></td>
<td><span data-ttu-id="1115b-185">NaN</span><span class="sxs-lookup"><span data-stu-id="1115b-185">NaN</span></span></td>
<td><span data-ttu-id="1115b-186">NaN</span><span class="sxs-lookup"><span data-stu-id="1115b-186">NaN</span></span></td>
<td><span data-ttu-id="1115b-187">NaN</span><span class="sxs-lookup"><span data-stu-id="1115b-187">NaN</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="1115b-188">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="1115b-188">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="1115b-189">Vértice</span><span class="sxs-lookup"><span data-stu-id="1115b-189">Vertex</span></span> | <span data-ttu-id="1115b-190">Envoltória</span><span class="sxs-lookup"><span data-stu-id="1115b-190">Hull</span></span> | <span data-ttu-id="1115b-191">Domínio</span><span class="sxs-lookup"><span data-stu-id="1115b-191">Domain</span></span> | <span data-ttu-id="1115b-192">Geometria</span><span class="sxs-lookup"><span data-stu-id="1115b-192">Geometry</span></span> | <span data-ttu-id="1115b-193">16x16</span><span class="sxs-lookup"><span data-stu-id="1115b-193">Pixel</span></span> | <span data-ttu-id="1115b-194">Computação</span><span class="sxs-lookup"><span data-stu-id="1115b-194">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="1115b-195">X</span><span class="sxs-lookup"><span data-stu-id="1115b-195">X</span></span>      | <span data-ttu-id="1115b-196">X</span><span class="sxs-lookup"><span data-stu-id="1115b-196">X</span></span>    | <span data-ttu-id="1115b-197">X</span><span class="sxs-lookup"><span data-stu-id="1115b-197">X</span></span>      | <span data-ttu-id="1115b-198">X</span><span class="sxs-lookup"><span data-stu-id="1115b-198">X</span></span>        | <span data-ttu-id="1115b-199">X</span><span class="sxs-lookup"><span data-stu-id="1115b-199">X</span></span>     | <span data-ttu-id="1115b-200">X</span><span class="sxs-lookup"><span data-stu-id="1115b-200">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="1115b-201">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="1115b-201">Minimum Shader Model</span></span>

<span data-ttu-id="1115b-202">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="1115b-202">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="1115b-203">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="1115b-203">Shader Model</span></span>                                              | <span data-ttu-id="1115b-204">Com suporte</span><span class="sxs-lookup"><span data-stu-id="1115b-204">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="1115b-205">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="1115b-205">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="1115b-206">sim</span><span class="sxs-lookup"><span data-stu-id="1115b-206">yes</span></span>       |
| [<span data-ttu-id="1115b-207">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="1115b-207">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="1115b-208">não</span><span class="sxs-lookup"><span data-stu-id="1115b-208">no</span></span>        |
| [<span data-ttu-id="1115b-209">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="1115b-209">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="1115b-210">não</span><span class="sxs-lookup"><span data-stu-id="1115b-210">no</span></span>        |
| [<span data-ttu-id="1115b-211">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1115b-211">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="1115b-212">não</span><span class="sxs-lookup"><span data-stu-id="1115b-212">no</span></span>        |
| [<span data-ttu-id="1115b-213">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1115b-213">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="1115b-214">não</span><span class="sxs-lookup"><span data-stu-id="1115b-214">no</span></span>        |
| [<span data-ttu-id="1115b-215">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1115b-215">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="1115b-216">não</span><span class="sxs-lookup"><span data-stu-id="1115b-216">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="1115b-217">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1115b-217">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1115b-218">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1115b-218">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





