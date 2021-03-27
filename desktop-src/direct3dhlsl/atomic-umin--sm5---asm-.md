---
title: atomic_umin (SM5-ASM)
description: Inteiro não assinado atômico mínimo para memória.
ms.assetid: 08822267-1A7F-4976-9402-601DD4B86E59
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8089dbed0e23443291176c47cda1a691202b164f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104967115"
---
# <a name="atomic_umin-sm5---asm"></a><span data-ttu-id="088cd-103">\_umin atômico (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="088cd-103">atomic\_umin (sm5 - asm)</span></span>

<span data-ttu-id="088cd-104">Inteiro não assinado atômico mínimo para memória.</span><span class="sxs-lookup"><span data-stu-id="088cd-104">Atomic unsigned integer minimum to memory.</span></span>



| <span data-ttu-id="088cd-105">\_componente Atomic umin DST, dstAddress \[ . swizzle \] , src0 \[ . Select \_\]</span><span class="sxs-lookup"><span data-stu-id="088cd-105">atomic\_umin dst, dstAddress\[.swizzle\], src0\[.select\_component\]</span></span> |
|----------------------------------------------------------------------|



 



| <span data-ttu-id="088cd-106">Item</span><span class="sxs-lookup"><span data-stu-id="088cd-106">Item</span></span>                                                                                                           | <span data-ttu-id="088cd-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="088cd-107">Description</span></span>                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="088cd-108"><span id="dst"></span><span id="DST"></span>*DST*</span><span class="sxs-lookup"><span data-stu-id="088cd-108"><span id="dst"></span><span id="DST"></span>*dst*</span></span><br/>                                                   | <span data-ttu-id="088cd-109">\[nos \] componentes para comparar com o *src0*.</span><span class="sxs-lookup"><span data-stu-id="088cd-109">\[in\] The components to compare to *src0*.</span></span> <span data-ttu-id="088cd-110">Esse valor deve ser uma exibição de acesso não ordenada (UAV) (u \# ).</span><span class="sxs-lookup"><span data-stu-id="088cd-110">This value must be an unordered access view (UAV) (u\#).</span></span> <span data-ttu-id="088cd-111">No sombreador de computação, ele também pode ser a memória compartilhada do grupo de threads (g \# ).</span><span class="sxs-lookup"><span data-stu-id="088cd-111">In the compute shader it can also be thread group shared memory (g\#).</span></span> <br/> |
| <span data-ttu-id="088cd-112"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span><span class="sxs-lookup"><span data-stu-id="088cd-112"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span></span><br/> | <span data-ttu-id="088cd-113">\[no \] endereço de memória.</span><span class="sxs-lookup"><span data-stu-id="088cd-113">\[in\] The memory address.</span></span><br/>                                                                                                                                                   |
| <span data-ttu-id="088cd-114"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="088cd-114"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                | <span data-ttu-id="088cd-115">\[nos \] componentes para comparar com o *horário de verão*.</span><span class="sxs-lookup"><span data-stu-id="088cd-115">\[in\] The components to compare to *dst*.</span></span><br/>                                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="088cd-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="088cd-116">Remarks</span></span>

<span data-ttu-id="088cd-117">Essa instrução executa um componente único sem sinal de 32 bits de operando *src0* no *DST* em 32 bits por endereço de componente *dstAddress*, executado atomicamente.</span><span class="sxs-lookup"><span data-stu-id="088cd-117">This instruction performs a single component 32-bit unsigned minimum of operand *src0* into *dst* at 32-bit per component address *dstAddress*, performed atomically.</span></span>

<span data-ttu-id="088cd-118">O número de componentes extraídos do endereço é determinado pela dimensionalidade do *DST* u \# ou g \# .</span><span class="sxs-lookup"><span data-stu-id="088cd-118">The number of components taken from the address is determined by the dimensionality of *dst* u\# or g\#.</span></span>

<span data-ttu-id="088cd-119">Se o *DST* for um u \# , ele poderá ser declarado como RAW, tipado ou estruturado.</span><span class="sxs-lookup"><span data-stu-id="088cd-119">If *dst* is a u\#, it can be declared as raw, typed or structured.</span></span> <span data-ttu-id="088cd-120">Se digitado, ele deve ser declarado como UINT/Santo com o formato de recurso ligado sendo R32 \_ uint/ \_ Santo.</span><span class="sxs-lookup"><span data-stu-id="088cd-120">If typed, it must be declared as UINT/SINT with the bound resource format being R32\_UINT/\_SINT.</span></span>

<span data-ttu-id="088cd-121">Se o *DST* for g \# , ele deverá ser declarado como bruto ou estruturado.</span><span class="sxs-lookup"><span data-stu-id="088cd-121">If *dst* is g\#, it must be declared as raw or structured.</span></span>

<span data-ttu-id="088cd-122">Nada é retornado para o sombreador.</span><span class="sxs-lookup"><span data-stu-id="088cd-122">Nothing is returned to the shader.</span></span>

<span data-ttu-id="088cd-123">Se a invocação do sombreador estiver inativa, por exemplo, se o pixel tiver sido descartado anteriormente em sua execução ou se uma invocação de pixel/amostra existir apenas para servir como um auxiliar para um pixel/amostra real para derivações, essa instrução não alterará a memória de *DST* (silenciosamente).</span><span class="sxs-lookup"><span data-stu-id="088cd-123">If the shader invocation is inactive, for example if the pixel has been discarded earlier in its execution, or if a pixel/sample invocation only exists to serve as a helper to a real pixel/sample for derivatives, this instruction does not alter the *dst* memory at all (silently).</span></span>

<span data-ttu-id="088cd-124">O endereçamento fora dos limites em u não \# faz nada a ser gravado na memória, exceto se o u \# for estruturado e o deslocamento de byte na estrutura (segundo componente do endereço) estiver causando o acesso fora dos limites, todo o conteúdo do UAV se tornará indefinido.</span><span class="sxs-lookup"><span data-stu-id="088cd-124">Out of bounds addressing on u\# causes nothing to be written to memory, except if the u\# is structured, and byte offset into the struct (second component of the address) is causing the out of bounds access, then the entire contents of the UAV become undefined.</span></span>

<span data-ttu-id="088cd-125">O endereçamento fora dos limites em g \# (os limites desse g específico \# , em oposição a toda a memória compartilhada) faz com que todo o conteúdo de toda a memória compartilhada se torne indefinido.</span><span class="sxs-lookup"><span data-stu-id="088cd-125">Out of bounds addressing on g\# (the bounds of that particular g\#, as opposed to all shared memory) causes the entire contents of all shared memory to become undefined.</span></span>

<span data-ttu-id="088cd-126">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="088cd-126">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="088cd-127">Vértice</span><span class="sxs-lookup"><span data-stu-id="088cd-127">Vertex</span></span> | <span data-ttu-id="088cd-128">Envoltória</span><span class="sxs-lookup"><span data-stu-id="088cd-128">Hull</span></span> | <span data-ttu-id="088cd-129">Domínio</span><span class="sxs-lookup"><span data-stu-id="088cd-129">Domain</span></span> | <span data-ttu-id="088cd-130">Geometria</span><span class="sxs-lookup"><span data-stu-id="088cd-130">Geometry</span></span> | <span data-ttu-id="088cd-131">16x16</span><span class="sxs-lookup"><span data-stu-id="088cd-131">Pixel</span></span> | <span data-ttu-id="088cd-132">Computação</span><span class="sxs-lookup"><span data-stu-id="088cd-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="088cd-133">X</span><span class="sxs-lookup"><span data-stu-id="088cd-133">X</span></span>     | <span data-ttu-id="088cd-134">X</span><span class="sxs-lookup"><span data-stu-id="088cd-134">X</span></span>       |



 

<span data-ttu-id="088cd-135">Como UAVs estão disponíveis em todos os estágios do sombreador para o Direct3D 11,1, essa instrução se aplica a todos os estágios do sombreador para o tempo de execução do Direct3D 11,1, que está disponível a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="088cd-135">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="088cd-136">Vértice</span><span class="sxs-lookup"><span data-stu-id="088cd-136">Vertex</span></span> | <span data-ttu-id="088cd-137">Envoltória</span><span class="sxs-lookup"><span data-stu-id="088cd-137">Hull</span></span> | <span data-ttu-id="088cd-138">Domínio</span><span class="sxs-lookup"><span data-stu-id="088cd-138">Domain</span></span> | <span data-ttu-id="088cd-139">Geometria</span><span class="sxs-lookup"><span data-stu-id="088cd-139">Geometry</span></span> | <span data-ttu-id="088cd-140">16x16</span><span class="sxs-lookup"><span data-stu-id="088cd-140">Pixel</span></span> | <span data-ttu-id="088cd-141">Computação</span><span class="sxs-lookup"><span data-stu-id="088cd-141">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="088cd-142">X</span><span class="sxs-lookup"><span data-stu-id="088cd-142">X</span></span>      | <span data-ttu-id="088cd-143">X</span><span class="sxs-lookup"><span data-stu-id="088cd-143">X</span></span>    | <span data-ttu-id="088cd-144">X</span><span class="sxs-lookup"><span data-stu-id="088cd-144">X</span></span>      | <span data-ttu-id="088cd-145">X</span><span class="sxs-lookup"><span data-stu-id="088cd-145">X</span></span>        | <span data-ttu-id="088cd-146">X</span><span class="sxs-lookup"><span data-stu-id="088cd-146">X</span></span>     | <span data-ttu-id="088cd-147">X</span><span class="sxs-lookup"><span data-stu-id="088cd-147">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="088cd-148">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="088cd-148">Minimum Shader Model</span></span>

<span data-ttu-id="088cd-149">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="088cd-149">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="088cd-150">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="088cd-150">Shader Model</span></span>                                              | <span data-ttu-id="088cd-151">Com suporte</span><span class="sxs-lookup"><span data-stu-id="088cd-151">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="088cd-152">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="088cd-152">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="088cd-153">sim</span><span class="sxs-lookup"><span data-stu-id="088cd-153">yes</span></span>       |
| [<span data-ttu-id="088cd-154">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="088cd-154">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="088cd-155">não</span><span class="sxs-lookup"><span data-stu-id="088cd-155">no</span></span>        |
| [<span data-ttu-id="088cd-156">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="088cd-156">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="088cd-157">não</span><span class="sxs-lookup"><span data-stu-id="088cd-157">no</span></span>        |
| [<span data-ttu-id="088cd-158">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="088cd-158">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="088cd-159">não</span><span class="sxs-lookup"><span data-stu-id="088cd-159">no</span></span>        |
| [<span data-ttu-id="088cd-160">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="088cd-160">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="088cd-161">não</span><span class="sxs-lookup"><span data-stu-id="088cd-161">no</span></span>        |
| [<span data-ttu-id="088cd-162">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="088cd-162">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="088cd-163">não</span><span class="sxs-lookup"><span data-stu-id="088cd-163">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="088cd-164">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="088cd-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="088cd-165">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="088cd-165">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





