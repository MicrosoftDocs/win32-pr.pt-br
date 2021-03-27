---
title: imm_atomic_exch (SM5-ASM)
description: Troca atômica imediata para memória.
ms.assetid: D06AE57E-52A4-4579-84FF-7DE9E713A5E3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb38cd696af079c5ae7dc896db619b95dd1d1d6c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104084271"
---
# <a name="imm_atomic_exch-sm5---asm"></a><span data-ttu-id="e4fc6-103">\_ \_ SM5-ASM (IMM Atomic Exch)</span><span class="sxs-lookup"><span data-stu-id="e4fc6-103">imm\_atomic\_exch (sm5 - asm)</span></span>

<span data-ttu-id="e4fc6-104">Troca atômica imediata para memória.</span><span class="sxs-lookup"><span data-stu-id="e4fc6-104">Immediate atomic exchange to memory.</span></span>



| <span data-ttu-id="e4fc6-105">\_dst0 de Exch atômico do IMM \_ \[ . \_ \_ máscara de componente único \] , dst1, dstAddress \[ . swizzle \] , \[ componente src0. Select \_\]</span><span class="sxs-lookup"><span data-stu-id="e4fc6-105">imm\_atomic\_exch dst0\[.single\_component\_mask\], dst1, dstAddress\[.swizzle\], src0\[.select\_component\]</span></span> |
|--------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="e4fc6-106">Item</span><span class="sxs-lookup"><span data-stu-id="e4fc6-106">Item</span></span>                                                                                                           | <span data-ttu-id="e4fc6-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="e4fc6-107">Description</span></span>                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4fc6-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="e4fc6-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                                | <span data-ttu-id="e4fc6-109">\[in \] contém o valor de *dst1* antes da gravação.</span><span class="sxs-lookup"><span data-stu-id="e4fc6-109">\[in\] Contains the value from *dst1* before the write.</span></span><br/>                                                                |
| <span data-ttu-id="e4fc6-110"><span id="dst1"></span><span id="DST1"></span>*dst1*</span><span class="sxs-lookup"><span data-stu-id="e4fc6-110"><span id="dst1"></span><span id="DST1"></span>*dst1*</span></span><br/>                                                | <span data-ttu-id="e4fc6-111">\[em \] um modo de exibição de acesso não ordenado (UAV) (u \# ).</span><span class="sxs-lookup"><span data-stu-id="e4fc6-111">\[in\] An unordered access view (UAV) (u\#).</span></span> <span data-ttu-id="e4fc6-112">No sombreador de computação, isso também pode ser memória compartilhada do grupo de threads (g \# ).</span><span class="sxs-lookup"><span data-stu-id="e4fc6-112">In the Compute Shader this can also be Thread Group Shared Memory (g\#).</span></span> <br/> |
| <span data-ttu-id="e4fc6-113"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span><span class="sxs-lookup"><span data-stu-id="e4fc6-113"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span></span><br/> | <span data-ttu-id="e4fc6-114">\[no \] endereço de memória.</span><span class="sxs-lookup"><span data-stu-id="e4fc6-114">\[in\] The memory address.</span></span><br/>                                                                                             |
| <span data-ttu-id="e4fc6-115"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="e4fc6-115"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                | <span data-ttu-id="e4fc6-116">\[no \] valor a ser gravado em *Dst1* em *dstAddress*.</span><span class="sxs-lookup"><span data-stu-id="e4fc6-116">\[in\] The value to write to *dst1* at *dstAddress*.</span></span><br/>                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="e4fc6-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="e4fc6-117">Remarks</span></span>

<span data-ttu-id="e4fc6-118">Essa instrução executa um único componente de valor de 32 bits gravação de operando *src0* para *dst1* em 32 bits por endereço de componente *dstAddress*.</span><span class="sxs-lookup"><span data-stu-id="e4fc6-118">This instruction performs a single component 32-bit value write of operand *src0* to *dst1* at 32-bit per component address *dstAddress*.</span></span>

<span data-ttu-id="e4fc6-119">Se *dst1* for u \# , ele poderá ter sido declarado como RAW, tipado ou estruturado.</span><span class="sxs-lookup"><span data-stu-id="e4fc6-119">If *dst1* is a u\#, it may have been declared as raw, typed or structured.</span></span> <span data-ttu-id="e4fc6-120">Se digitado, ele deve ser declarado como UINT/Santo com o formato de recurso ligado sendo R32 \_ uint/ \_ Santo.</span><span class="sxs-lookup"><span data-stu-id="e4fc6-120">If typed, it must be declared as UINT/SINT with the bound resource format being R32\_UINT/\_SINT.</span></span>

<span data-ttu-id="e4fc6-121">Se *dst1* for g \# , ele deverá ser declarado como RAW ou Structured.</span><span class="sxs-lookup"><span data-stu-id="e4fc6-121">If *dst1* is g\#, it must be declared as raw or structured.</span></span>

<span data-ttu-id="e4fc6-122">O número de componentes extraídos do endereço é determinado pela dimensionalidade do recurso declarado em *dst1*.</span><span class="sxs-lookup"><span data-stu-id="e4fc6-122">The number of components taken from the address is determined by the dimensionality of the resource declared at *dst1*.</span></span>

<span data-ttu-id="e4fc6-123">O valor de 32 bits original na memória de destino é gravado em *dst0*.</span><span class="sxs-lookup"><span data-stu-id="e4fc6-123">The original 32-bit value in the destination memory is written to *dst0*.</span></span>

<span data-ttu-id="e4fc6-124">Toda a operação é executada atomicamente.</span><span class="sxs-lookup"><span data-stu-id="e4fc6-124">The entire operation is performed atomically.</span></span>

<span data-ttu-id="e4fc6-125">Se a invocação do sombreador estiver inativa, por exemplo, se o pixel tiver sido descartado anteriormente em sua execução, ou se uma invocação de pixel/amostra existir apenas para servir como um auxiliar para um pixel/amostra real para derivações, essa instrução não alterará a memória *dst1* e o valor retornado será indefinido.</span><span class="sxs-lookup"><span data-stu-id="e4fc6-125">If the shader invocation is inactive, for example if the pixel has been discarded earlier in its execution, or a pixel/sample invocation only exists to serve as a helper to a real pixel/sample for derivatives, this instruction does not alter the *dst1* memory at all, and the returned value is undefined.</span></span>

<span data-ttu-id="e4fc6-126">O endereçamento fora dos limites em u não \# faz nada a ser gravado na memória, exceto se o u \# for estruturado e o deslocamento de byte na estrutura (segundo componente do endereço) estiver causando o acesso fora dos limites, todo o conteúdo do UAV se tornará indefinido.</span><span class="sxs-lookup"><span data-stu-id="e4fc6-126">Out of bounds addressing on u\# causes nothing to be written to memory, except if the u\# is structured, and byte offset into the struct (second component of the address) is causing the out of bounds access, then the entire contents of the UAV become undefined.</span></span>

<span data-ttu-id="e4fc6-127">O endereçamento fora dos limites em u \# ou g \# faz com que um resultado indefinido seja retornado ao sombreador em *dst0*.</span><span class="sxs-lookup"><span data-stu-id="e4fc6-127">Out of bounds addressing on u\# or g\# causes an undefined result to be returned to the shader in *dst0*.</span></span>

<span data-ttu-id="e4fc6-128">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="e4fc6-128">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="e4fc6-129">Vértice</span><span class="sxs-lookup"><span data-stu-id="e4fc6-129">Vertex</span></span> | <span data-ttu-id="e4fc6-130">Envoltória</span><span class="sxs-lookup"><span data-stu-id="e4fc6-130">Hull</span></span> | <span data-ttu-id="e4fc6-131">Domínio</span><span class="sxs-lookup"><span data-stu-id="e4fc6-131">Domain</span></span> | <span data-ttu-id="e4fc6-132">Geometria</span><span class="sxs-lookup"><span data-stu-id="e4fc6-132">Geometry</span></span> | <span data-ttu-id="e4fc6-133">16x16</span><span class="sxs-lookup"><span data-stu-id="e4fc6-133">Pixel</span></span> | <span data-ttu-id="e4fc6-134">Computação</span><span class="sxs-lookup"><span data-stu-id="e4fc6-134">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="e4fc6-135">X</span><span class="sxs-lookup"><span data-stu-id="e4fc6-135">X</span></span>     | <span data-ttu-id="e4fc6-136">X</span><span class="sxs-lookup"><span data-stu-id="e4fc6-136">X</span></span>       |



 

<span data-ttu-id="e4fc6-137">Como UAVs estão disponíveis em todos os estágios do sombreador para o Direct3D 11,1, essa instrução se aplica a todos os estágios do sombreador para o tempo de execução do Direct3D 11,1, que está disponível a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="e4fc6-137">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="e4fc6-138">Vértice</span><span class="sxs-lookup"><span data-stu-id="e4fc6-138">Vertex</span></span> | <span data-ttu-id="e4fc6-139">Envoltória</span><span class="sxs-lookup"><span data-stu-id="e4fc6-139">Hull</span></span> | <span data-ttu-id="e4fc6-140">Domínio</span><span class="sxs-lookup"><span data-stu-id="e4fc6-140">Domain</span></span> | <span data-ttu-id="e4fc6-141">Geometria</span><span class="sxs-lookup"><span data-stu-id="e4fc6-141">Geometry</span></span> | <span data-ttu-id="e4fc6-142">16x16</span><span class="sxs-lookup"><span data-stu-id="e4fc6-142">Pixel</span></span> | <span data-ttu-id="e4fc6-143">Computação</span><span class="sxs-lookup"><span data-stu-id="e4fc6-143">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="e4fc6-144">X</span><span class="sxs-lookup"><span data-stu-id="e4fc6-144">X</span></span>      | <span data-ttu-id="e4fc6-145">X</span><span class="sxs-lookup"><span data-stu-id="e4fc6-145">X</span></span>    | <span data-ttu-id="e4fc6-146">X</span><span class="sxs-lookup"><span data-stu-id="e4fc6-146">X</span></span>      | <span data-ttu-id="e4fc6-147">X</span><span class="sxs-lookup"><span data-stu-id="e4fc6-147">X</span></span>        | <span data-ttu-id="e4fc6-148">X</span><span class="sxs-lookup"><span data-stu-id="e4fc6-148">X</span></span>     | <span data-ttu-id="e4fc6-149">X</span><span class="sxs-lookup"><span data-stu-id="e4fc6-149">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="e4fc6-150">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="e4fc6-150">Minimum Shader Model</span></span>

<span data-ttu-id="e4fc6-151">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="e4fc6-151">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="e4fc6-152">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="e4fc6-152">Shader Model</span></span>                                              | <span data-ttu-id="e4fc6-153">Com suporte</span><span class="sxs-lookup"><span data-stu-id="e4fc6-153">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="e4fc6-154">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="e4fc6-154">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="e4fc6-155">sim</span><span class="sxs-lookup"><span data-stu-id="e4fc6-155">yes</span></span>       |
| [<span data-ttu-id="e4fc6-156">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="e4fc6-156">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="e4fc6-157">não</span><span class="sxs-lookup"><span data-stu-id="e4fc6-157">no</span></span>        |
| [<span data-ttu-id="e4fc6-158">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="e4fc6-158">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="e4fc6-159">não</span><span class="sxs-lookup"><span data-stu-id="e4fc6-159">no</span></span>        |
| [<span data-ttu-id="e4fc6-160">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e4fc6-160">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="e4fc6-161">não</span><span class="sxs-lookup"><span data-stu-id="e4fc6-161">no</span></span>        |
| [<span data-ttu-id="e4fc6-162">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e4fc6-162">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="e4fc6-163">não</span><span class="sxs-lookup"><span data-stu-id="e4fc6-163">no</span></span>        |
| [<span data-ttu-id="e4fc6-164">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e4fc6-164">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="e4fc6-165">não</span><span class="sxs-lookup"><span data-stu-id="e4fc6-165">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="e4fc6-166">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e4fc6-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4fc6-167">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e4fc6-167">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





