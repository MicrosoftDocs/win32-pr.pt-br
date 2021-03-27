---
title: Assembly do Shader Model 4
description: Assembly do Shader Model 4
ms.assetid: 2896e195-b48b-4ce9-9421-f5fa40674b5e
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 20c7ff5d2a171228223d52db28d3bae6007068c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005555"
---
# <a name="shader-model-4-assembly"></a><span data-ttu-id="8acc5-103">Assembly do Shader Model 4</span><span class="sxs-lookup"><span data-stu-id="8acc5-103">Shader Model 4 Assembly</span></span>

<span data-ttu-id="8acc5-104">O Shader Model 4 exige a programação de sombreadores no HLSL.</span><span class="sxs-lookup"><span data-stu-id="8acc5-104">Shader Model 4 requires you to program shaders in HLSL.</span></span> <span data-ttu-id="8acc5-105">No entanto, o compilador do sombreador compila o código HLSL no assembly que é executado no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8acc5-105">However, the shader compiler compiles the HLSL code into assembly that runs on the device.</span></span> <span data-ttu-id="8acc5-106">Se você estiver usando o PIX para Windows para depurar seus sombreadores, poderá optar por exibir o código do sombreador em HLSL ou assembly.</span><span class="sxs-lookup"><span data-stu-id="8acc5-106">If you are using PIX for Windows to debug your shaders, you can choose to display shader code in either HLSL or assembly.</span></span> <span data-ttu-id="8acc5-107">Esta seção lista as instruções de assembly do Shader Model 4 e do Shader Model 4,1 que você pode encontrar ao depurar um sombreador.</span><span class="sxs-lookup"><span data-stu-id="8acc5-107">This section lists the Shader Model 4 and Shader Model 4.1 assembly instructions that you may encounter when debugging a shader.</span></span>

<dl>

[<span data-ttu-id="8acc5-108">Modificadores de instrução</span><span class="sxs-lookup"><span data-stu-id="8acc5-108">Instruction Modifiers</span></span>](instruction-modifiers.md)  
[<span data-ttu-id="8acc5-109">add</span><span class="sxs-lookup"><span data-stu-id="8acc5-109">add</span></span>](add--sm4---asm-.md)  
[<span data-ttu-id="8acc5-110">and</span><span class="sxs-lookup"><span data-stu-id="8acc5-110">and</span></span>](and--sm4---asm-.md)  
[<span data-ttu-id="8acc5-111">break</span><span class="sxs-lookup"><span data-stu-id="8acc5-111">break</span></span>](break--sm4---asm-.md)  
[<span data-ttu-id="8acc5-112">breakc</span><span class="sxs-lookup"><span data-stu-id="8acc5-112">breakc</span></span>](breakc--sm4---asm-.md)  
[<span data-ttu-id="8acc5-113">call</span><span class="sxs-lookup"><span data-stu-id="8acc5-113">call</span></span>](call--sm4---asm-.md)  
[<span data-ttu-id="8acc5-114">callc</span><span class="sxs-lookup"><span data-stu-id="8acc5-114">callc</span></span>](callc--sm4---asm-.md)  
[<span data-ttu-id="8acc5-115">case</span><span class="sxs-lookup"><span data-stu-id="8acc5-115">case</span></span>](case--sm4---asm-.md)  
[<span data-ttu-id="8acc5-116">continua</span><span class="sxs-lookup"><span data-stu-id="8acc5-116">continue</span></span>](continue--sm4---asm-.md)  
[<span data-ttu-id="8acc5-117">continuec</span><span class="sxs-lookup"><span data-stu-id="8acc5-117">continuec</span></span>](continuec--sm4---asm-.md)  
[<span data-ttu-id="8acc5-118">migração</span><span class="sxs-lookup"><span data-stu-id="8acc5-118">cut</span></span>](cut--sm4---asm-.md)  
[<span data-ttu-id="8acc5-119">\_constantBuffer DCL</span><span class="sxs-lookup"><span data-stu-id="8acc5-119">dcl\_constantBuffer</span></span>](dcl-constantbuffer.md)  
[<span data-ttu-id="8acc5-120">\_globalFlags DCL</span><span class="sxs-lookup"><span data-stu-id="8acc5-120">dcl\_globalFlags</span></span>](dcl-globalflags.md)  
[<span data-ttu-id="8acc5-121">\_immediateConstantBuffer DCL</span><span class="sxs-lookup"><span data-stu-id="8acc5-121">dcl\_immediateConstantBuffer</span></span>](dcl-immediateconstantbuffer.md)  
[<span data-ttu-id="8acc5-122">\_indexableTemp DCL</span><span class="sxs-lookup"><span data-stu-id="8acc5-122">dcl\_indexableTemp</span></span>](dcl-indexabletemp.md)  
[<span data-ttu-id="8acc5-123">\_indexRange DCL</span><span class="sxs-lookup"><span data-stu-id="8acc5-123">dcl\_indexRange</span></span>](dcl-indexrange.md)  
[<span data-ttu-id="8acc5-124">\_entrada DCL</span><span class="sxs-lookup"><span data-stu-id="8acc5-124">dcl\_input</span></span>](dcl-input.md)  
[<span data-ttu-id="8acc5-125">\_VA de entrada de DCL \_</span><span class="sxs-lookup"><span data-stu-id="8acc5-125">dcl\_input\_sv</span></span>](dcl-input-sv.md)  
[<span data-ttu-id="8acc5-126">\_vPrim de entrada DCL</span><span class="sxs-lookup"><span data-stu-id="8acc5-126">dcl\_input vPrim</span></span>](dcl-input-vprim.md)  
[<span data-ttu-id="8acc5-127">\_maxOutputVertexCount DCL</span><span class="sxs-lookup"><span data-stu-id="8acc5-127">dcl\_maxOutputVertexCount</span></span>](dcl-maxoutputvertexcount.md)  
[<span data-ttu-id="8acc5-128">saída de DCL \_</span><span class="sxs-lookup"><span data-stu-id="8acc5-128">dcl\_output</span></span>](dcl-output.md)  
[<span data-ttu-id="8acc5-129">\_oDepth de saída de DCL \_</span><span class="sxs-lookup"><span data-stu-id="8acc5-129">dcl\_output\_oDepth</span></span>](dcl-output-odepth.md)  
[<span data-ttu-id="8acc5-130">\_SGV de saída de DCL \_</span><span class="sxs-lookup"><span data-stu-id="8acc5-130">dcl\_output\_sgv</span></span>](dcl-output-sgv.md)  
[<span data-ttu-id="8acc5-131">\_SIV de saída de DCL \_</span><span class="sxs-lookup"><span data-stu-id="8acc5-131">dcl\_output\_siv</span></span>](dcl-output-siv.md)  
[<span data-ttu-id="8acc5-132">\_outputTopology DCL</span><span class="sxs-lookup"><span data-stu-id="8acc5-132">dcl\_outputTopology</span></span>](dcl-outputtopology.md)  
[<span data-ttu-id="8acc5-133">\_recurso DCL</span><span class="sxs-lookup"><span data-stu-id="8acc5-133">dcl\_resource</span></span>](dcl-resource.md)  
[<span data-ttu-id="8acc5-134">amostra de DCL \_</span><span class="sxs-lookup"><span data-stu-id="8acc5-134">dcl\_sampler</span></span>](dcl-sampler.md)  
[<span data-ttu-id="8acc5-135">\_pretemps DCL</span><span class="sxs-lookup"><span data-stu-id="8acc5-135">dcl\_temps</span></span>](dcl-temps.md)  
[<span data-ttu-id="8acc5-136">default</span><span class="sxs-lookup"><span data-stu-id="8acc5-136">default</span></span>](default--sm4---asm-.md)  
[<span data-ttu-id="8acc5-137">derivar \_ RTX</span><span class="sxs-lookup"><span data-stu-id="8acc5-137">deriv\_rtx</span></span>](deriv-rtx--sm4---asm-.md)  
[<span data-ttu-id="8acc5-138">derivar \_ rty</span><span class="sxs-lookup"><span data-stu-id="8acc5-138">deriv\_rty</span></span>](deriv-rty--sm4---asm-.md)  
[<span data-ttu-id="8acc5-139">carte</span><span class="sxs-lookup"><span data-stu-id="8acc5-139">discard</span></span>](discard--sm4---asm-.md)  
[<span data-ttu-id="8acc5-140">div</span><span class="sxs-lookup"><span data-stu-id="8acc5-140">div</span></span>](div--sm4---asm-.md)  
[<span data-ttu-id="8acc5-141">dp2</span><span class="sxs-lookup"><span data-stu-id="8acc5-141">dp2</span></span>](dp2--sm4---asm-.md)  
[<span data-ttu-id="8acc5-142">dp3</span><span class="sxs-lookup"><span data-stu-id="8acc5-142">dp3</span></span>](dp3--sm4---asm-.md)  
[<span data-ttu-id="8acc5-143">dp4</span><span class="sxs-lookup"><span data-stu-id="8acc5-143">dp4</span></span>](dp4--sm4---asm-.md)  
[<span data-ttu-id="8acc5-144">senão</span><span class="sxs-lookup"><span data-stu-id="8acc5-144">else</span></span>](else--sm4---asm-.md)  
[<span data-ttu-id="8acc5-145">reflexão</span><span class="sxs-lookup"><span data-stu-id="8acc5-145">emit</span></span>](emit--sm4---asm-.md)  
[<span data-ttu-id="8acc5-146">emitThenCut</span><span class="sxs-lookup"><span data-stu-id="8acc5-146">emitThenCut</span></span>](emitthencut--sm4---asm-.md)  
[<span data-ttu-id="8acc5-147">endif</span><span class="sxs-lookup"><span data-stu-id="8acc5-147">endif</span></span>](endif--sm4---asm-.md)  
[<span data-ttu-id="8acc5-148">loop de fim</span><span class="sxs-lookup"><span data-stu-id="8acc5-148">endloop</span></span>](endloop--sm4---asm-.md)  
[<span data-ttu-id="8acc5-149">troca de</span><span class="sxs-lookup"><span data-stu-id="8acc5-149">endswitch</span></span>](endswitch--sm4---asm-.md)  
[<span data-ttu-id="8acc5-150">eq</span><span class="sxs-lookup"><span data-stu-id="8acc5-150">eq</span></span>](eq--sm4---asm-.md)  
[<span data-ttu-id="8acc5-151">exp</span><span class="sxs-lookup"><span data-stu-id="8acc5-151">exp</span></span>](exp--sm4---asm-.md)  
[<span data-ttu-id="8acc5-152">frc</span><span class="sxs-lookup"><span data-stu-id="8acc5-152">frc</span></span>](frc--sm4---asm-.md)  
[<span data-ttu-id="8acc5-153">ftoi</span><span class="sxs-lookup"><span data-stu-id="8acc5-153">ftoi</span></span>](ftoi--sm4---asm-.md)  
[<span data-ttu-id="8acc5-154">ftou</span><span class="sxs-lookup"><span data-stu-id="8acc5-154">ftou</span></span>](ftou--sm4---asm-.md)  
[<span data-ttu-id="8acc5-155">ge</span><span class="sxs-lookup"><span data-stu-id="8acc5-155">ge</span></span>](ge--sm4---asm-.md)  
[<span data-ttu-id="8acc5-156">IAdd</span><span class="sxs-lookup"><span data-stu-id="8acc5-156">iadd</span></span>](iadd--sm4---asm-.md)  
[<span data-ttu-id="8acc5-157">ibfe</span><span class="sxs-lookup"><span data-stu-id="8acc5-157">ibfe</span></span>](dne--sm5---asm-.md)  
[<span data-ttu-id="8acc5-158">ieq</span><span class="sxs-lookup"><span data-stu-id="8acc5-158">ieq</span></span>](ieq--sm4---asm-.md)  
[<span data-ttu-id="8acc5-159">if</span><span class="sxs-lookup"><span data-stu-id="8acc5-159">if</span></span>](if--sm4---asm-.md)  
[<span data-ttu-id="8acc5-160">ige</span><span class="sxs-lookup"><span data-stu-id="8acc5-160">ige</span></span>](ige--sm4---asm-.md)  
[<span data-ttu-id="8acc5-161">curso</span><span class="sxs-lookup"><span data-stu-id="8acc5-161">ilt</span></span>](ilt--sm4---asm-.md)  
[<span data-ttu-id="8acc5-162">imad</span><span class="sxs-lookup"><span data-stu-id="8acc5-162">imad</span></span>](imad--sm4---asm-.md)  
[<span data-ttu-id="8acc5-163">imin</span><span class="sxs-lookup"><span data-stu-id="8acc5-163">imin</span></span>](imin--sm4---asm-.md)  
[<span data-ttu-id="8acc5-164">imul</span><span class="sxs-lookup"><span data-stu-id="8acc5-164">imul</span></span>](imul--sm4---asm-.md)  
[<span data-ttu-id="8acc5-165">inha</span><span class="sxs-lookup"><span data-stu-id="8acc5-165">ine</span></span>](ine--sm4---asm-.md)  
[<span data-ttu-id="8acc5-166">ineg</span><span class="sxs-lookup"><span data-stu-id="8acc5-166">ineg</span></span>](ineg--sm4---asm-.md)  
[<span data-ttu-id="8acc5-167">ishl</span><span class="sxs-lookup"><span data-stu-id="8acc5-167">ishl</span></span>](ishl--sm4---asm-.md)  
[<span data-ttu-id="8acc5-168">ishr</span><span class="sxs-lookup"><span data-stu-id="8acc5-168">ishr</span></span>](ishr--sm4---asm-.md)  
[<span data-ttu-id="8acc5-169">itof</span><span class="sxs-lookup"><span data-stu-id="8acc5-169">itof</span></span>](itof--sm4---asm-.md)  
[<span data-ttu-id="8acc5-170">label</span><span class="sxs-lookup"><span data-stu-id="8acc5-170">label</span></span>](label--sm4---asm-.md)  
[<span data-ttu-id="8acc5-171">2</span><span class="sxs-lookup"><span data-stu-id="8acc5-171">ld</span></span>](ld--sm4---asm-.md)  
[<span data-ttu-id="8acc5-172">Façam</span><span class="sxs-lookup"><span data-stu-id="8acc5-172">log</span></span>](log--sm4---asm-.md)  
[<span data-ttu-id="8acc5-173">loop</span><span class="sxs-lookup"><span data-stu-id="8acc5-173">loop</span></span>](loop--sm4---asm-.md)  
[<span data-ttu-id="8acc5-174">lt</span><span class="sxs-lookup"><span data-stu-id="8acc5-174">lt</span></span>](lt--sm4---asm-.md)  
[<span data-ttu-id="8acc5-175">Mad</span><span class="sxs-lookup"><span data-stu-id="8acc5-175">mad</span></span>](mad--sm4---asm-.md)  
[<span data-ttu-id="8acc5-176">max</span><span class="sxs-lookup"><span data-stu-id="8acc5-176">max</span></span>](max--sm4---asm-.md)  
[<span data-ttu-id="8acc5-177">min</span><span class="sxs-lookup"><span data-stu-id="8acc5-177">min</span></span>](min--sm4---asm-.md)  
[<span data-ttu-id="8acc5-178">média</span><span class="sxs-lookup"><span data-stu-id="8acc5-178">mov</span></span>](mov--sm4---asm-.md)  
[<span data-ttu-id="8acc5-179">movc</span><span class="sxs-lookup"><span data-stu-id="8acc5-179">movc</span></span>](movc--sm4---asm-.md)  
[<span data-ttu-id="8acc5-180">mul</span><span class="sxs-lookup"><span data-stu-id="8acc5-180">mul</span></span>](mul--sm4---asm-.md)  
[<span data-ttu-id="8acc5-181">ne</span><span class="sxs-lookup"><span data-stu-id="8acc5-181">ne</span></span>](ne--sm4---asm-.md)  
[<span data-ttu-id="8acc5-182">Nop</span><span class="sxs-lookup"><span data-stu-id="8acc5-182">nop</span></span>](nop--sm4---asm-.md)  
[<span data-ttu-id="8acc5-183">not</span><span class="sxs-lookup"><span data-stu-id="8acc5-183">not</span></span>](not--sm4---asm-.md)  
[<span data-ttu-id="8acc5-184">or</span><span class="sxs-lookup"><span data-stu-id="8acc5-184">or</span></span>](or--sm4---asm-.md)  
[<span data-ttu-id="8acc5-185">ResInfo</span><span class="sxs-lookup"><span data-stu-id="8acc5-185">resinfo</span></span>](resinfo--sm4---asm-.md)  
[<span data-ttu-id="8acc5-186">RET</span><span class="sxs-lookup"><span data-stu-id="8acc5-186">ret</span></span>](ret--sm4---asm-.md)  
[<span data-ttu-id="8acc5-187">retc</span><span class="sxs-lookup"><span data-stu-id="8acc5-187">retc</span></span>](retc--sm4---asm-.md)  
[<span data-ttu-id="8acc5-188">arredondar \_ ne</span><span class="sxs-lookup"><span data-stu-id="8acc5-188">round\_ne</span></span>](round-ne--sm4---asm-.md)  
[<span data-ttu-id="8acc5-189">Ni de ida e volta \_</span><span class="sxs-lookup"><span data-stu-id="8acc5-189">round\_ni</span></span>](round-ni--sm4---asm-.md)  
[<span data-ttu-id="8acc5-190">PI arredondado \_</span><span class="sxs-lookup"><span data-stu-id="8acc5-190">round\_pi</span></span>](round-pi--sm4---asm-.md)  
[<span data-ttu-id="8acc5-191">arredondar \_ z</span><span class="sxs-lookup"><span data-stu-id="8acc5-191">round\_z</span></span>](round-z--sm4---asm-.md)  
[<span data-ttu-id="8acc5-192">rsq</span><span class="sxs-lookup"><span data-stu-id="8acc5-192">rsq</span></span>](rsq--sm4---asm-.md)  
[<span data-ttu-id="8acc5-193">Nova</span><span class="sxs-lookup"><span data-stu-id="8acc5-193">sample</span></span>](sample--sm4---asm-.md)  
[<span data-ttu-id="8acc5-194">exemplo \_ b</span><span class="sxs-lookup"><span data-stu-id="8acc5-194">sample\_b</span></span>](sample-b--sm4---asm-.md)  
[<span data-ttu-id="8acc5-195">exemplo \_ c</span><span class="sxs-lookup"><span data-stu-id="8acc5-195">sample\_c</span></span>](sample-c--sm4---asm-.md)  
[<span data-ttu-id="8acc5-196">exemplo \_ c \_ LZ</span><span class="sxs-lookup"><span data-stu-id="8acc5-196">sample\_c\_lz</span></span>](sample-c-lz--sm4---asm-.md)  
[<span data-ttu-id="8acc5-197">exemplo \_ d</span><span class="sxs-lookup"><span data-stu-id="8acc5-197">sample\_d</span></span>](sample-d--sm4---asm-.md)  
[<span data-ttu-id="8acc5-198">exemplo \_ l</span><span class="sxs-lookup"><span data-stu-id="8acc5-198">sample\_l</span></span>](sample-l--sm4---asm-.md)  
[<span data-ttu-id="8acc5-199">sincos</span><span class="sxs-lookup"><span data-stu-id="8acc5-199">sincos</span></span>](sincos--sm4---asm-.md)  
[<span data-ttu-id="8acc5-200">sqrt</span><span class="sxs-lookup"><span data-stu-id="8acc5-200">sqrt</span></span>](sqrt--sm4---asm-.md)  
[<span data-ttu-id="8acc5-201">switch</span><span class="sxs-lookup"><span data-stu-id="8acc5-201">switch</span></span>](switch--sm4---asm-.md)  
[<span data-ttu-id="8acc5-202">udiv</span><span class="sxs-lookup"><span data-stu-id="8acc5-202">udiv</span></span>](udiv--sm4---asm-.md)  
[<span data-ttu-id="8acc5-203">uge</span><span class="sxs-lookup"><span data-stu-id="8acc5-203">uge</span></span>](uge--sm4---asm-.md)  
[<span data-ttu-id="8acc5-204">ultados</span><span class="sxs-lookup"><span data-stu-id="8acc5-204">ult</span></span>](ult--sm4---asm-.md)  
[<span data-ttu-id="8acc5-205">umad</span><span class="sxs-lookup"><span data-stu-id="8acc5-205">umad</span></span>](umad--sm4---asm-.md)  
[<span data-ttu-id="8acc5-206">scanner</span><span class="sxs-lookup"><span data-stu-id="8acc5-206">umax</span></span>](umax--sm4---asm-.md)  
[<span data-ttu-id="8acc5-207">umin</span><span class="sxs-lookup"><span data-stu-id="8acc5-207">umin</span></span>](umin--sm4---asm-.md)  
[<span data-ttu-id="8acc5-208">umul</span><span class="sxs-lookup"><span data-stu-id="8acc5-208">umul</span></span>](umul--sm4---asm-.md)  
[<span data-ttu-id="8acc5-209">ushr</span><span class="sxs-lookup"><span data-stu-id="8acc5-209">ushr</span></span>](ushr--sm4---asm-.md)  
[<span data-ttu-id="8acc5-210">utof</span><span class="sxs-lookup"><span data-stu-id="8acc5-210">utof</span></span>](utof--sm4---asm-.md)  
[<span data-ttu-id="8acc5-211">XOR</span><span class="sxs-lookup"><span data-stu-id="8acc5-211">xor</span></span>](xor--sm4---asm-.md)  
</dl>

## <a name="shader-model-41-assembly"></a><span data-ttu-id="8acc5-212">Assembly de modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="8acc5-212">Shader Model 4.1 Assembly</span></span>

<span data-ttu-id="8acc5-213">O Shader Model 4,1 dá suporte a todas as instruções do modelo de sombreador 4,0 e às seguintes instruções adicionais:</span><span class="sxs-lookup"><span data-stu-id="8acc5-213">Shader Model 4.1 supports all of the Shader Model 4.0 instructions and the following additional instructions:</span></span>

<dl>

[<span data-ttu-id="8acc5-214">gather4</span><span class="sxs-lookup"><span data-stu-id="8acc5-214">gather4</span></span>](gather4--sm4-1---asm-.md)  
[<span data-ttu-id="8acc5-215">ld2dms</span><span class="sxs-lookup"><span data-stu-id="8acc5-215">ld2dms</span></span>](ld2dms--sm4-1---asm-.md)  
[<span data-ttu-id="8acc5-216">lod</span><span class="sxs-lookup"><span data-stu-id="8acc5-216">lod</span></span>](lod--sm4-1---asm-.md)  
[<span data-ttu-id="8acc5-217">sampleinfo</span><span class="sxs-lookup"><span data-stu-id="8acc5-217">sampleinfo</span></span>](sampleinfo--sm4-1---asm-.md)  
[<span data-ttu-id="8acc5-218">samplepos</span><span class="sxs-lookup"><span data-stu-id="8acc5-218">samplepos</span></span>](samplepos--sm4-1---asm-.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="8acc5-219">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8acc5-219">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8acc5-220">Referência do sombreador ASM</span><span class="sxs-lookup"><span data-stu-id="8acc5-220">Asm Shader Reference</span></span>](dx9-graphics-reference-asm.md)
</dt> <dt>

[<span data-ttu-id="8acc5-221">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="8acc5-221">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




