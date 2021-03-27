---
title: imm_atomic_imax (SM5-ASM)
description: Máx. de assinatura atômica imediata para memória. Retorna o valor na memória antes da operação de máximo.
ms.assetid: 360E542C-F3F6-4103-8A22-4914A5103D17
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8143073065955a00df412ecf453cc523d7e98493
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103916879"
---
# <a name="imm_atomic_imax-sm5---asm"></a><span data-ttu-id="9b38f-104">\_IMAX atômico \_ do IMM (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="9b38f-104">imm\_atomic\_imax (sm5 - asm)</span></span>

<span data-ttu-id="9b38f-105">Máx. de assinatura atômica imediata para memória.</span><span class="sxs-lookup"><span data-stu-id="9b38f-105">Immediate atomic signed max to memory.</span></span> <span data-ttu-id="9b38f-106">Retorna o valor na memória antes da operação de máximo.</span><span class="sxs-lookup"><span data-stu-id="9b38f-106">Returns value in memory before the max operation.</span></span>



| <span data-ttu-id="9b38f-107">IMM \_ Atomic \_ IMAX dst0 \[ . \_ \_ máscara de componente único \] , dst1, dstAddress \[ . swizzle \] , \[ \_ componente src0. Select\]</span><span class="sxs-lookup"><span data-stu-id="9b38f-107">imm\_atomic\_imax dst0\[.single\_component\_mask\], dst1, dstAddress\[.swizzle\], src0\[.select\_component\]</span></span> |
|--------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="9b38f-108">Item</span><span class="sxs-lookup"><span data-stu-id="9b38f-108">Item</span></span>                                                                                                           | <span data-ttu-id="9b38f-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="9b38f-109">Description</span></span>                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b38f-110"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="9b38f-110"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                                | <span data-ttu-id="9b38f-111">\[in \] contém o valor de *dst1* antes desta instrução.</span><span class="sxs-lookup"><span data-stu-id="9b38f-111">\[in\] Contains the value from *dst1* before this instruction.</span></span><br/>                                                         |
| <span data-ttu-id="9b38f-112"><span id="dst1"></span><span id="DST1"></span>*dst1*</span><span class="sxs-lookup"><span data-stu-id="9b38f-112"><span id="dst1"></span><span id="DST1"></span>*dst1*</span></span><br/>                                                | <span data-ttu-id="9b38f-113">\[em \] um modo de exibição de acesso não ordenado (UAV) (u \# ).</span><span class="sxs-lookup"><span data-stu-id="9b38f-113">\[in\] An unordered access view (UAV) (u\#).</span></span> <span data-ttu-id="9b38f-114">No sombreador de computação, isso também pode ser memória compartilhada do grupo de threads (g \# ).</span><span class="sxs-lookup"><span data-stu-id="9b38f-114">In the compute shader this can also be thread group shared memory (g\#).</span></span> <br/> |
| <span data-ttu-id="9b38f-115"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span><span class="sxs-lookup"><span data-stu-id="9b38f-115"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span></span><br/> | <span data-ttu-id="9b38f-116">\[no \] endereço de memória.</span><span class="sxs-lookup"><span data-stu-id="9b38f-116">\[in\] The memory address.</span></span><br/>                                                                                             |
| <span data-ttu-id="9b38f-117"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="9b38f-117"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                | <span data-ttu-id="9b38f-118">\[no \] valor a ser comparado com *Dst1* em *dstAddress*.</span><span class="sxs-lookup"><span data-stu-id="9b38f-118">\[in\] The value to compare to *dst1* at *dstAddress*.</span></span><br/>                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="9b38f-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="9b38f-119">Remarks</span></span>

<span data-ttu-id="9b38f-120">Essa instrução executa um único componente com o máximo de 32 bits com sinal de operando *src0* com *dst1* em 32 bits por endereço de componente *dstAddress*.</span><span class="sxs-lookup"><span data-stu-id="9b38f-120">This instruction performs a single component 32-bit signed maximum of operand *src0* with *dst1* at 32-bit per component address *dstAddress*.</span></span>

<span data-ttu-id="9b38f-121">Se *dst1* for u \# , ele poderá ter sido declarado como RAW, tipado ou estruturado.</span><span class="sxs-lookup"><span data-stu-id="9b38f-121">If *dst1* is a u\#, it may have been declared as raw, typed or structured.</span></span> <span data-ttu-id="9b38f-122">Se digitado, ele deve ser declarado como UINT/Santo com o formato de recurso ligado sendo R32 \_ uint/ \_ Santo.</span><span class="sxs-lookup"><span data-stu-id="9b38f-122">If typed, it must be declared as UINT/SINT with the bound resource format being R32\_UINT/\_SINT.</span></span>

<span data-ttu-id="9b38f-123">Se *dst1* for g \# , ele deverá ser declarado como RAW ou Structured.</span><span class="sxs-lookup"><span data-stu-id="9b38f-123">If *dst1* is g\#, it must be declared as raw or structured.</span></span>

<span data-ttu-id="9b38f-124">O valor em *dst1* Memory antes de Max é retornado para *dst0*.</span><span class="sxs-lookup"><span data-stu-id="9b38f-124">The value in *dst1* memory before max is returned to *dst0*.</span></span>

<span data-ttu-id="9b38f-125">O número de componentes extraídos do endereço é determinado pela dimensionalidade do *dst1*.</span><span class="sxs-lookup"><span data-stu-id="9b38f-125">The number of components taken from the address is determined by the dimensionality of *dst1*.</span></span>

<span data-ttu-id="9b38f-126">Toda a operação é executada atomicamente.</span><span class="sxs-lookup"><span data-stu-id="9b38f-126">The entire operation is performed atomically.</span></span>

<span data-ttu-id="9b38f-127">Se a invocação do sombreador estiver inativa, por exemplo, se o pixel tiver sido descartado anteriormente em sua execução, ou se uma invocação de pixel/amostra existir apenas para servir como um auxiliar para um pixel/amostra real para derivações, essa instrução não alterará a memória *dst1* e o valor retornado será indefinido.</span><span class="sxs-lookup"><span data-stu-id="9b38f-127">If the shader invocation is inactive, for example if the pixel has been discarded earlier in its execution, or a pixel/sample invocation only exists to serve as a helper to a real pixel/sample for derivatives, this instruction does not alter the *dst1* memory at all, and the returned value is undefined.</span></span>

<span data-ttu-id="9b38f-128">O endereçamento fora dos limites em u não \# faz nada a ser gravado na memória, exceto se o u \# for estruturado e o deslocamento de byte na estrutura (segundo componente do endereço) estiver causando o acesso fora dos limites, todo o conteúdo do UAV se tornará indefinido.</span><span class="sxs-lookup"><span data-stu-id="9b38f-128">Out of bounds addressing on u\# causes nothing to be written to memory, except if the u\# is structured, and byte offset into the struct (second component of the address) is causing the out of bounds access, then the entire contents of the UAV become undefined.</span></span>

<span data-ttu-id="9b38f-129">O endereçamento fora dos limites em u \# ou g \# faz com que um resultado indefinido seja retornado ao sombreador em *dst0*.</span><span class="sxs-lookup"><span data-stu-id="9b38f-129">Out of bounds addressing on u\# or g\# causes an undefined result to be returned to the shader in *dst0*.</span></span>

<span data-ttu-id="9b38f-130">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="9b38f-130">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="9b38f-131">Vértice</span><span class="sxs-lookup"><span data-stu-id="9b38f-131">Vertex</span></span> | <span data-ttu-id="9b38f-132">Envoltória</span><span class="sxs-lookup"><span data-stu-id="9b38f-132">Hull</span></span> | <span data-ttu-id="9b38f-133">Domínio</span><span class="sxs-lookup"><span data-stu-id="9b38f-133">Domain</span></span> | <span data-ttu-id="9b38f-134">Geometria</span><span class="sxs-lookup"><span data-stu-id="9b38f-134">Geometry</span></span> | <span data-ttu-id="9b38f-135">16x16</span><span class="sxs-lookup"><span data-stu-id="9b38f-135">Pixel</span></span> | <span data-ttu-id="9b38f-136">Computação</span><span class="sxs-lookup"><span data-stu-id="9b38f-136">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="9b38f-137">X</span><span class="sxs-lookup"><span data-stu-id="9b38f-137">X</span></span>     | <span data-ttu-id="9b38f-138">X</span><span class="sxs-lookup"><span data-stu-id="9b38f-138">X</span></span>       |



 

<span data-ttu-id="9b38f-139">Como UAVs estão disponíveis em todos os estágios do sombreador para o Direct3D 11,1, essa instrução se aplica a todos os estágios do sombreador para o tempo de execução do Direct3D 11,1, que está disponível a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="9b38f-139">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="9b38f-140">Vértice</span><span class="sxs-lookup"><span data-stu-id="9b38f-140">Vertex</span></span> | <span data-ttu-id="9b38f-141">Envoltória</span><span class="sxs-lookup"><span data-stu-id="9b38f-141">Hull</span></span> | <span data-ttu-id="9b38f-142">Domínio</span><span class="sxs-lookup"><span data-stu-id="9b38f-142">Domain</span></span> | <span data-ttu-id="9b38f-143">Geometria</span><span class="sxs-lookup"><span data-stu-id="9b38f-143">Geometry</span></span> | <span data-ttu-id="9b38f-144">16x16</span><span class="sxs-lookup"><span data-stu-id="9b38f-144">Pixel</span></span> | <span data-ttu-id="9b38f-145">Computação</span><span class="sxs-lookup"><span data-stu-id="9b38f-145">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="9b38f-146">X</span><span class="sxs-lookup"><span data-stu-id="9b38f-146">X</span></span>      | <span data-ttu-id="9b38f-147">X</span><span class="sxs-lookup"><span data-stu-id="9b38f-147">X</span></span>    | <span data-ttu-id="9b38f-148">X</span><span class="sxs-lookup"><span data-stu-id="9b38f-148">X</span></span>      | <span data-ttu-id="9b38f-149">X</span><span class="sxs-lookup"><span data-stu-id="9b38f-149">X</span></span>        | <span data-ttu-id="9b38f-150">X</span><span class="sxs-lookup"><span data-stu-id="9b38f-150">X</span></span>     | <span data-ttu-id="9b38f-151">X</span><span class="sxs-lookup"><span data-stu-id="9b38f-151">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="9b38f-152">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="9b38f-152">Minimum Shader Model</span></span>

<span data-ttu-id="9b38f-153">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="9b38f-153">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="9b38f-154">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="9b38f-154">Shader Model</span></span>                                              | <span data-ttu-id="9b38f-155">Com suporte</span><span class="sxs-lookup"><span data-stu-id="9b38f-155">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="9b38f-156">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="9b38f-156">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="9b38f-157">sim</span><span class="sxs-lookup"><span data-stu-id="9b38f-157">yes</span></span>       |
| [<span data-ttu-id="9b38f-158">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="9b38f-158">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="9b38f-159">não</span><span class="sxs-lookup"><span data-stu-id="9b38f-159">no</span></span>        |
| [<span data-ttu-id="9b38f-160">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="9b38f-160">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="9b38f-161">não</span><span class="sxs-lookup"><span data-stu-id="9b38f-161">no</span></span>        |
| [<span data-ttu-id="9b38f-162">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9b38f-162">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="9b38f-163">não</span><span class="sxs-lookup"><span data-stu-id="9b38f-163">no</span></span>        |
| [<span data-ttu-id="9b38f-164">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9b38f-164">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="9b38f-165">não</span><span class="sxs-lookup"><span data-stu-id="9b38f-165">no</span></span>        |
| [<span data-ttu-id="9b38f-166">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9b38f-166">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="9b38f-167">não</span><span class="sxs-lookup"><span data-stu-id="9b38f-167">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="9b38f-168">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9b38f-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b38f-169">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9b38f-169">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





