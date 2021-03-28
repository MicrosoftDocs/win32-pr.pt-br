---
title: imm_atomic_iadd (SM5-ASM)
description: Número inteiro atômico imediato adicione à memória. Retorna o valor na memória antes da adição.
ms.assetid: 24136B4C-D37C-4449-A318-57145BB8D8E9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2695e23707fb61cd576748e2e83829cd7dc65259
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104365261"
---
# <a name="imm_atomic_iadd-sm5---asm"></a><span data-ttu-id="b7bbc-104">\_IAdd atômico \_ do IMM (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="b7bbc-104">imm\_atomic\_iadd (sm5 - asm)</span></span>

<span data-ttu-id="b7bbc-105">Número inteiro atômico imediato adicione à memória.</span><span class="sxs-lookup"><span data-stu-id="b7bbc-105">Immediate atomic integer add to memory.</span></span> <span data-ttu-id="b7bbc-106">Retorna o valor na memória antes da adição.</span><span class="sxs-lookup"><span data-stu-id="b7bbc-106">Returns the value in memory before the add.</span></span>



| <span data-ttu-id="b7bbc-107">IMM \_ Atomic \_ IAdd dst0 \[ . \_ \_ máscara de componente único \] , dst1, dstAddress \[ . swizzle \] , \[ \_ componente src0. Select\]</span><span class="sxs-lookup"><span data-stu-id="b7bbc-107">imm\_atomic\_iadd dst0\[.single\_component\_mask\], dst1, dstAddress\[.swizzle\], src0\[.select\_component\]</span></span> |
|--------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="b7bbc-108">Item</span><span class="sxs-lookup"><span data-stu-id="b7bbc-108">Item</span></span>                                                                                                           | <span data-ttu-id="b7bbc-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="b7bbc-109">Description</span></span>                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7bbc-110"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="b7bbc-110"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                                | <span data-ttu-id="b7bbc-111">\[in \] contém o valor em *dst1* antes da gravação.</span><span class="sxs-lookup"><span data-stu-id="b7bbc-111">\[in\] Contains the value in *dst1* before the write.</span></span> <br/>                                                                           |
| <span data-ttu-id="b7bbc-112"><span id="dst1"></span><span id="DST1"></span>*dst1*</span><span class="sxs-lookup"><span data-stu-id="b7bbc-112"><span id="dst1"></span><span id="DST1"></span>*dst1*</span></span><br/>                                                | <span data-ttu-id="b7bbc-113">Esse valor deve ser uma exibição de acesso não ordenada (UAV) (u \# ).</span><span class="sxs-lookup"><span data-stu-id="b7bbc-113">This value must be an unordered access view (UAV) (u\#).</span></span> <span data-ttu-id="b7bbc-114">No sombreador de computação, ele também pode ser a memória compartilhada do grupo de threads (g \# ).</span><span class="sxs-lookup"><span data-stu-id="b7bbc-114">In the compute shader it can also be thread group shared memory (g\#).</span></span> <br/> |
| <span data-ttu-id="b7bbc-115"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span><span class="sxs-lookup"><span data-stu-id="b7bbc-115"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span></span><br/> | <span data-ttu-id="b7bbc-116">\[na \] memória naddress.</span><span class="sxs-lookup"><span data-stu-id="b7bbc-116">\[in\] The memory naddress.</span></span><br/>                                                                                                      |
| <span data-ttu-id="b7bbc-117"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="b7bbc-117"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                | <span data-ttu-id="b7bbc-118">\[no \] valor a ser adicionado ao *dst1*.</span><span class="sxs-lookup"><span data-stu-id="b7bbc-118">\[in\] The value to add to *dst1*.</span></span><br/>                                                                                               |



 

## <a name="remarks"></a><span data-ttu-id="b7bbc-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="b7bbc-119">Remarks</span></span>

<span data-ttu-id="b7bbc-120">Essa instrução executa um único componente de *src0* de operando inteiro de 32 bits, com *dst1* em 32 bits por endereço de componente *dstAddress*.</span><span class="sxs-lookup"><span data-stu-id="b7bbc-120">This instruction performs a single component 32-bit integer add of operand *src0* with *dst1* at 32-bit per component address *dstAddress*.</span></span> <span data-ttu-id="b7bbc-121">Não é sensível à assinatura.</span><span class="sxs-lookup"><span data-stu-id="b7bbc-121">It is insensitive to sign.</span></span>

<span data-ttu-id="b7bbc-122">Se *dst1* for u \# , ele poderá ter sido declarado como RAW, tipado ou estruturado.</span><span class="sxs-lookup"><span data-stu-id="b7bbc-122">If *dst1* is a u\#, it may have been declared as raw, typed or structured.</span></span> <span data-ttu-id="b7bbc-123">Se digitado, ele deve ser declarado como UINT/Santo com o formato de recurso ligado sendo R32 \_ uint/ \_ Santo.</span><span class="sxs-lookup"><span data-stu-id="b7bbc-123">If typed, it must be declared as UINT/SINT with the bound resource format being R32\_UINT/\_SINT.</span></span>

<span data-ttu-id="b7bbc-124">Se *dst1* for g \# , ele deverá ser declarado como RAW ou Structured.</span><span class="sxs-lookup"><span data-stu-id="b7bbc-124">If *dst1* is g\#, it must be declared as raw or structured.</span></span>

<span data-ttu-id="b7bbc-125">O valor na memória *dst1* antes da adição é retornado para *dst0*.</span><span class="sxs-lookup"><span data-stu-id="b7bbc-125">The value in *dst1* memory before addition is returned to *dst0*.</span></span>

<span data-ttu-id="b7bbc-126">O número de componentes extraídos do endereço é determinado pela dimensionalidade do *dst1*.</span><span class="sxs-lookup"><span data-stu-id="b7bbc-126">The number of components taken from the address is determined by the dimensionality of *dst1*.</span></span>

<span data-ttu-id="b7bbc-127">Toda a operação é executada atomicamente.</span><span class="sxs-lookup"><span data-stu-id="b7bbc-127">The entire operation is performed atomically.</span></span>

<span data-ttu-id="b7bbc-128">Se a invocação do sombreador estiver inativa, por exemplo, se o pixel tiver sido descartado anteriormente em sua execução, ou se uma invocação de pixel/amostra existir apenas para servir como um auxiliar para um pixel/amostra real para derivações, essa instrução não alterará a memória *dst1* e o valor retornado será indefinido.</span><span class="sxs-lookup"><span data-stu-id="b7bbc-128">If the shader invocation is inactive, for example if the pixel has been discarded earlier in its execution, or a pixel/sample invocation only exists to serve as a helper to a real pixel/sample for derivatives, this instruction does not alter the *dst1* memory at all, and the returned value is undefined.</span></span>

<span data-ttu-id="b7bbc-129">O endereçamento fora dos limites em u não \# faz nada a ser gravado na memória, exceto se o u \# for estruturado e o deslocamento de byte na estrutura (segundo componente do endereço) estiver causando o acesso fora dos limites, todo o conteúdo do UAV se tornará indefinido.</span><span class="sxs-lookup"><span data-stu-id="b7bbc-129">Out of bounds addressing on u\# causes nothing to be written to memory, except if the u\# is structured, and byte offset into the struct (second component of the address) is causing the out of bounds access, then the entire contents of the UAV become undefined.</span></span>

<span data-ttu-id="b7bbc-130">O endereçamento fora dos limites em u \# ou g \# faz com que um resultado indefinido seja retornado ao sombreador em *dst0*.</span><span class="sxs-lookup"><span data-stu-id="b7bbc-130">Out of bounds addressing on u\# or g\# causes an undefined result to be returned to the shader in *dst0*.</span></span>

<span data-ttu-id="b7bbc-131">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="b7bbc-131">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="b7bbc-132">Vértice</span><span class="sxs-lookup"><span data-stu-id="b7bbc-132">Vertex</span></span> | <span data-ttu-id="b7bbc-133">Envoltória</span><span class="sxs-lookup"><span data-stu-id="b7bbc-133">Hull</span></span> | <span data-ttu-id="b7bbc-134">Domínio</span><span class="sxs-lookup"><span data-stu-id="b7bbc-134">Domain</span></span> | <span data-ttu-id="b7bbc-135">Geometria</span><span class="sxs-lookup"><span data-stu-id="b7bbc-135">Geometry</span></span> | <span data-ttu-id="b7bbc-136">16x16</span><span class="sxs-lookup"><span data-stu-id="b7bbc-136">Pixel</span></span> | <span data-ttu-id="b7bbc-137">Computação</span><span class="sxs-lookup"><span data-stu-id="b7bbc-137">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="b7bbc-138">X</span><span class="sxs-lookup"><span data-stu-id="b7bbc-138">X</span></span>     | <span data-ttu-id="b7bbc-139">X</span><span class="sxs-lookup"><span data-stu-id="b7bbc-139">X</span></span>       |



 

<span data-ttu-id="b7bbc-140">Como UAVs estão disponíveis em todos os estágios do sombreador para o Direct3D 11,1, essa instrução se aplica a todos os estágios do sombreador para o tempo de execução do Direct3D 11,1, que está disponível a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b7bbc-140">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="b7bbc-141">Vértice</span><span class="sxs-lookup"><span data-stu-id="b7bbc-141">Vertex</span></span> | <span data-ttu-id="b7bbc-142">Envoltória</span><span class="sxs-lookup"><span data-stu-id="b7bbc-142">Hull</span></span> | <span data-ttu-id="b7bbc-143">Domínio</span><span class="sxs-lookup"><span data-stu-id="b7bbc-143">Domain</span></span> | <span data-ttu-id="b7bbc-144">Geometria</span><span class="sxs-lookup"><span data-stu-id="b7bbc-144">Geometry</span></span> | <span data-ttu-id="b7bbc-145">16x16</span><span class="sxs-lookup"><span data-stu-id="b7bbc-145">Pixel</span></span> | <span data-ttu-id="b7bbc-146">Computação</span><span class="sxs-lookup"><span data-stu-id="b7bbc-146">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="b7bbc-147">X</span><span class="sxs-lookup"><span data-stu-id="b7bbc-147">X</span></span>      | <span data-ttu-id="b7bbc-148">X</span><span class="sxs-lookup"><span data-stu-id="b7bbc-148">X</span></span>    | <span data-ttu-id="b7bbc-149">X</span><span class="sxs-lookup"><span data-stu-id="b7bbc-149">X</span></span>      | <span data-ttu-id="b7bbc-150">X</span><span class="sxs-lookup"><span data-stu-id="b7bbc-150">X</span></span>        | <span data-ttu-id="b7bbc-151">X</span><span class="sxs-lookup"><span data-stu-id="b7bbc-151">X</span></span>     | <span data-ttu-id="b7bbc-152">X</span><span class="sxs-lookup"><span data-stu-id="b7bbc-152">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="b7bbc-153">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="b7bbc-153">Minimum Shader Model</span></span>

<span data-ttu-id="b7bbc-154">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="b7bbc-154">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="b7bbc-155">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="b7bbc-155">Shader Model</span></span>                                              | <span data-ttu-id="b7bbc-156">Com suporte</span><span class="sxs-lookup"><span data-stu-id="b7bbc-156">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="b7bbc-157">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="b7bbc-157">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="b7bbc-158">sim</span><span class="sxs-lookup"><span data-stu-id="b7bbc-158">yes</span></span>       |
| [<span data-ttu-id="b7bbc-159">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="b7bbc-159">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="b7bbc-160">não</span><span class="sxs-lookup"><span data-stu-id="b7bbc-160">no</span></span>        |
| [<span data-ttu-id="b7bbc-161">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="b7bbc-161">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="b7bbc-162">não</span><span class="sxs-lookup"><span data-stu-id="b7bbc-162">no</span></span>        |
| [<span data-ttu-id="b7bbc-163">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b7bbc-163">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="b7bbc-164">não</span><span class="sxs-lookup"><span data-stu-id="b7bbc-164">no</span></span>        |
| [<span data-ttu-id="b7bbc-165">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b7bbc-165">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="b7bbc-166">não</span><span class="sxs-lookup"><span data-stu-id="b7bbc-166">no</span></span>        |
| [<span data-ttu-id="b7bbc-167">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b7bbc-167">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="b7bbc-168">não</span><span class="sxs-lookup"><span data-stu-id="b7bbc-168">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="b7bbc-169">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b7bbc-169">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7bbc-170">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b7bbc-170">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





