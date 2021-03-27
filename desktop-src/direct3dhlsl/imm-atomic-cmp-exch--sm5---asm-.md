---
title: imm_atomic_cmp_exch (SM5-ASM)
description: Comparação imediata e troca na memória.
ms.assetid: 317A69E1-0E0A-45C8-8E0A-B88659ADBECC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f63e1be030d7cce0d6f0a581788db39a599272b2
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103823460"
---
# <a name="imm_atomic_cmp_exch-sm5---asm"></a><span data-ttu-id="79df9-103">IMM \_ Atomic \_ CMP \_ Exch (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="79df9-103">imm\_atomic\_cmp\_exch (sm5 - asm)</span></span>

<span data-ttu-id="79df9-104">Comparação imediata e troca na memória.</span><span class="sxs-lookup"><span data-stu-id="79df9-104">Immediate compare and exchange to memory.</span></span>



| <span data-ttu-id="79df9-105">IMM \_ Atomic \_ CMP \_ Exch dst0 \[ . \_ máscara de componente único \_ \] , dst1, dstAddress \[ . swizzle \] , src0 \[ . Select \_ componente \] , \[ \_ componente src1. Select\]</span><span class="sxs-lookup"><span data-stu-id="79df9-105">imm\_atomic\_cmp\_exch dst0\[.single\_component\_mask\], dst1, dstAddress\[.swizzle\], src0\[.select\_component\], src1\[.select\_component\]</span></span> |
|-----------------------------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="79df9-106">Item</span><span class="sxs-lookup"><span data-stu-id="79df9-106">Item</span></span>                                                                                                           | <span data-ttu-id="79df9-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="79df9-107">Description</span></span>                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79df9-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="79df9-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                                | <span data-ttu-id="79df9-109">\[out \] contém *dst1* antes da gravação.</span><span class="sxs-lookup"><span data-stu-id="79df9-109">\[out\] Contains *dst1* before the write.</span></span><br/>                                                                              |
| <span data-ttu-id="79df9-110"><span id="dst1"></span><span id="DST1"></span>*dst1*</span><span class="sxs-lookup"><span data-stu-id="79df9-110"><span id="dst1"></span><span id="DST1"></span>*dst1*</span></span><br/>                                                | <span data-ttu-id="79df9-111">\[em \] um modo de exibição de acesso não ordenado (UAV) (u \# ).</span><span class="sxs-lookup"><span data-stu-id="79df9-111">\[in\] An unordered access view (UAV) (u\#).</span></span> <span data-ttu-id="79df9-112">No sombreador de computação, isso também pode ser memória compartilhada do grupo de threads (g \# ).</span><span class="sxs-lookup"><span data-stu-id="79df9-112">In the compute shader this can also be thread group shared memory (g\#).</span></span> <br/> |
| <span data-ttu-id="79df9-113"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span><span class="sxs-lookup"><span data-stu-id="79df9-113"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span></span><br/> | <span data-ttu-id="79df9-114">\[na \] memória de destino.</span><span class="sxs-lookup"><span data-stu-id="79df9-114">\[in\] The destination memory.</span></span><br/>                                                                                         |
| <span data-ttu-id="79df9-115"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="79df9-115"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                | <span data-ttu-id="79df9-116">\[no \] valor a ser comparado com *dst1*.</span><span class="sxs-lookup"><span data-stu-id="79df9-116">\[in\] The value to compare to *dst1*.</span></span><br/>                                                                                 |
| <span data-ttu-id="79df9-117"><span id="scr1"></span><span id="SCR1"></span>*scr1*</span><span class="sxs-lookup"><span data-stu-id="79df9-117"><span id="scr1"></span><span id="SCR1"></span>*scr1*</span></span><br/>                                                | <span data-ttu-id="79df9-118">\[no \] valor gravado na memória de destino, se os valores de comparação forem idênticos.</span><span class="sxs-lookup"><span data-stu-id="79df9-118">\[in\] The value written to the destination memory if the compared values are identical.</span></span><br/>                               |



 

<span data-ttu-id="79df9-119">Esta instrução executa um único componente de 32 bits Compare of operando *src0* com *dst1* em 32 bits por endereço de componente *dstAddress*.</span><span class="sxs-lookup"><span data-stu-id="79df9-119">This instruction performs a single component 32-bit value compare of operand *src0* with *dst1* at 32-bit per component address *dstAddress*.</span></span>

<span data-ttu-id="79df9-120">Se *dst1* for u \# , ele poderá ter sido declarado como RAW, tipado ou estruturado.</span><span class="sxs-lookup"><span data-stu-id="79df9-120">If *dst1* is a u\#, it may have been declared as raw, typed or structured.</span></span> <span data-ttu-id="79df9-121">Se digitado, ele deve ser declarado como UINT/Santo com o formato de recurso ligado sendo R32 \_ uint/ \_ Santo.</span><span class="sxs-lookup"><span data-stu-id="79df9-121">If typed, it must be declared as UINT/SINT with the bound resource format being R32\_UINT/\_SINT.</span></span>

<span data-ttu-id="79df9-122">Se *dst1* for g \# , ele deverá ser declarado como RAW ou Structured.</span><span class="sxs-lookup"><span data-stu-id="79df9-122">If *dst1* is g\#, it must be declared as raw or structured.</span></span>

<span data-ttu-id="79df9-123">Se os valores de comparação forem idênticos, o valor de 32 bits de componente único em *src1* será gravado na memória de destino.</span><span class="sxs-lookup"><span data-stu-id="79df9-123">If the compared values are identical, the single-component 32-bit value in *src1* is written to the destination memory.</span></span> <span data-ttu-id="79df9-124">Caso contrário, a memória de destino não será alterada.</span><span class="sxs-lookup"><span data-stu-id="79df9-124">Otherwise, the destination memory is not changed.</span></span>

<span data-ttu-id="79df9-125">O valor original de 32 bits na memória de destino é sempre gravado em *dst0*.</span><span class="sxs-lookup"><span data-stu-id="79df9-125">The original 32-bit value in the destination memory is always written to *dst0*.</span></span>

<span data-ttu-id="79df9-126">Toda a operação é executada atomicamente.</span><span class="sxs-lookup"><span data-stu-id="79df9-126">The entire operation is performed atomically.</span></span>

<span data-ttu-id="79df9-127">Se a invocação do sombreador estiver inativa, por exemplo, se o pixel tiver sido descartado anteriormente em sua execução, ou se uma invocação de pixel/amostra existir apenas para servir como um auxiliar para um pixel/amostra real para derivações, essa instrução não alterará a memória *dst1* e o valor retornado será indefinido.</span><span class="sxs-lookup"><span data-stu-id="79df9-127">If the shader invocation is inactive, for example if the pixel has been discarded earlier in its execution, or a pixel/sample invocation only exists to serve as a helper to a real pixel/sample for derivatives, this instruction does not alter the *dst1* memory at all, and the returned value is undefined.</span></span>

<span data-ttu-id="79df9-128">O endereçamento fora dos limites em u não \# faz nada a ser gravado na memória, exceto se o u \# for estruturado e o deslocamento de byte na estrutura (segundo componente do endereço) estiver causando o acesso fora dos limites, todo o conteúdo do UAV se tornará indefinido.</span><span class="sxs-lookup"><span data-stu-id="79df9-128">Out of bounds addressing on u\# causes nothing to be written to memory, except if the u\# is structured, and byte offset into the struct (second component of the address) is causing the out of bounds access, then the entire contents of the UAV become undefined.</span></span>

<span data-ttu-id="79df9-129">O endereçamento fora dos limites em u \# ou g \# faz com que um resultado indefinido seja retornado ao sombreador em *dst0*.</span><span class="sxs-lookup"><span data-stu-id="79df9-129">Out of bounds addressing on u\# or g\# causes an undefined result to be returned to the shader in *dst0*.</span></span>

<span data-ttu-id="79df9-130">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="79df9-130">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="79df9-131">Vértice</span><span class="sxs-lookup"><span data-stu-id="79df9-131">Vertex</span></span> | <span data-ttu-id="79df9-132">Envoltória</span><span class="sxs-lookup"><span data-stu-id="79df9-132">Hull</span></span> | <span data-ttu-id="79df9-133">Domínio</span><span class="sxs-lookup"><span data-stu-id="79df9-133">Domain</span></span> | <span data-ttu-id="79df9-134">Geometria</span><span class="sxs-lookup"><span data-stu-id="79df9-134">Geometry</span></span> | <span data-ttu-id="79df9-135">16x16</span><span class="sxs-lookup"><span data-stu-id="79df9-135">Pixel</span></span> | <span data-ttu-id="79df9-136">Computação</span><span class="sxs-lookup"><span data-stu-id="79df9-136">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="79df9-137">X</span><span class="sxs-lookup"><span data-stu-id="79df9-137">X</span></span>     | <span data-ttu-id="79df9-138">X</span><span class="sxs-lookup"><span data-stu-id="79df9-138">X</span></span>       |



 

<span data-ttu-id="79df9-139">Como UAVs estão disponíveis em todos os estágios do sombreador para o Direct3D 11,1, essa instrução se aplica a todos os estágios do sombreador para o tempo de execução do Direct3D 11,1, que está disponível a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="79df9-139">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="79df9-140">Vértice</span><span class="sxs-lookup"><span data-stu-id="79df9-140">Vertex</span></span> | <span data-ttu-id="79df9-141">Envoltória</span><span class="sxs-lookup"><span data-stu-id="79df9-141">Hull</span></span> | <span data-ttu-id="79df9-142">Domínio</span><span class="sxs-lookup"><span data-stu-id="79df9-142">Domain</span></span> | <span data-ttu-id="79df9-143">Geometria</span><span class="sxs-lookup"><span data-stu-id="79df9-143">Geometry</span></span> | <span data-ttu-id="79df9-144">16x16</span><span class="sxs-lookup"><span data-stu-id="79df9-144">Pixel</span></span> | <span data-ttu-id="79df9-145">Computação</span><span class="sxs-lookup"><span data-stu-id="79df9-145">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="79df9-146">X</span><span class="sxs-lookup"><span data-stu-id="79df9-146">X</span></span>      | <span data-ttu-id="79df9-147">X</span><span class="sxs-lookup"><span data-stu-id="79df9-147">X</span></span>    | <span data-ttu-id="79df9-148">X</span><span class="sxs-lookup"><span data-stu-id="79df9-148">X</span></span>      | <span data-ttu-id="79df9-149">X</span><span class="sxs-lookup"><span data-stu-id="79df9-149">X</span></span>        | <span data-ttu-id="79df9-150">X</span><span class="sxs-lookup"><span data-stu-id="79df9-150">X</span></span>     | <span data-ttu-id="79df9-151">X</span><span class="sxs-lookup"><span data-stu-id="79df9-151">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="79df9-152">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="79df9-152">Minimum Shader Model</span></span>

<span data-ttu-id="79df9-153">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="79df9-153">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="79df9-154">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="79df9-154">Shader Model</span></span>                                              | <span data-ttu-id="79df9-155">Com suporte</span><span class="sxs-lookup"><span data-stu-id="79df9-155">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="79df9-156">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="79df9-156">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="79df9-157">sim</span><span class="sxs-lookup"><span data-stu-id="79df9-157">yes</span></span>       |
| [<span data-ttu-id="79df9-158">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="79df9-158">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="79df9-159">não</span><span class="sxs-lookup"><span data-stu-id="79df9-159">no</span></span>        |
| [<span data-ttu-id="79df9-160">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="79df9-160">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="79df9-161">não</span><span class="sxs-lookup"><span data-stu-id="79df9-161">no</span></span>        |
| [<span data-ttu-id="79df9-162">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="79df9-162">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="79df9-163">não</span><span class="sxs-lookup"><span data-stu-id="79df9-163">no</span></span>        |
| [<span data-ttu-id="79df9-164">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="79df9-164">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="79df9-165">não</span><span class="sxs-lookup"><span data-stu-id="79df9-165">no</span></span>        |
| [<span data-ttu-id="79df9-166">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="79df9-166">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="79df9-167">não</span><span class="sxs-lookup"><span data-stu-id="79df9-167">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="79df9-168">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="79df9-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79df9-169">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="79df9-169">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





