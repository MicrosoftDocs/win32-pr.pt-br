---
title: atomic_iadd (SM5-ASM)
description: Inteiro atômico adicione à memória.
ms.assetid: 093C7FA5-41BF-4BDD-A35D-1AACE8CB9B5C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6a8652d4e29aae9f32a84f7a4e4d477abd54b7c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104293590"
---
# <a name="atomic_iadd-sm5---asm"></a><span data-ttu-id="157d4-103">\_IAdd atômico (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="157d4-103">atomic\_iadd (sm5 - asm)</span></span>

<span data-ttu-id="157d4-104">Inteiro atômico adicione à memória.</span><span class="sxs-lookup"><span data-stu-id="157d4-104">Atomic integer add to memory.</span></span>



| <span data-ttu-id="157d4-105">\_componente Atomic IAdd DST, dstAddress \[ . swizzle \] , src0 \[ . Select \_\]</span><span class="sxs-lookup"><span data-stu-id="157d4-105">atomic\_iadd dst, dstAddress\[.swizzle\], src0\[.select\_component\]</span></span> |
|----------------------------------------------------------------------|



 



| <span data-ttu-id="157d4-106">Item</span><span class="sxs-lookup"><span data-stu-id="157d4-106">Item</span></span>                                                                                                           | <span data-ttu-id="157d4-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="157d4-107">Description</span></span>                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="157d4-108"><span id="dst"></span><span id="DST"></span>*DST*</span><span class="sxs-lookup"><span data-stu-id="157d4-108"><span id="dst"></span><span id="DST"></span>*dst*</span></span><br/>                                                   | <span data-ttu-id="157d4-109">\[nos \] componentes a serem adicionados com *src0*.</span><span class="sxs-lookup"><span data-stu-id="157d4-109">\[in\] The components to add with *src0*.</span></span> <span data-ttu-id="157d4-110">Esse valor deve ser uma exibição de acesso não ordenada (UAV) (u \# ).</span><span class="sxs-lookup"><span data-stu-id="157d4-110">This value must be an unordered access view (UAV) (u\#).</span></span> <span data-ttu-id="157d4-111">No sombreador de computação, ele também pode ser a memória compartilhada do grupo de threads (g \# ).</span><span class="sxs-lookup"><span data-stu-id="157d4-111">In the compute shader it can also be thread group shared memory (g\#).</span></span> <br/> |
| <span data-ttu-id="157d4-112"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span><span class="sxs-lookup"><span data-stu-id="157d4-112"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span></span><br/> | <span data-ttu-id="157d4-113">\[no \] endereço de memória.</span><span class="sxs-lookup"><span data-stu-id="157d4-113">\[in\] The memory address.</span></span><br/>                                                                                                                                                 |
| <span data-ttu-id="157d4-114"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="157d4-114"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                | <span data-ttu-id="157d4-115">\[nos \] componentes a serem adicionados ao *DST*.</span><span class="sxs-lookup"><span data-stu-id="157d4-115">\[in\] The components to add to *dst*.</span></span><br/>                                                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="157d4-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="157d4-116">Remarks</span></span>

<span data-ttu-id="157d4-117">Essa instrução executa um único componente de *src0* de operando de inteiro de 32 bits no *DST* em 32 bits por endereço de componente *dstAddress*, executado atomicamente.</span><span class="sxs-lookup"><span data-stu-id="157d4-117">This instruction performs a single component 32-bit integer add of operand *src0* into *dst* at 32-bit per component address *dstAddress*, performed atomically.</span></span> <span data-ttu-id="157d4-118">Esta instrução não diferencia a assinatura.</span><span class="sxs-lookup"><span data-stu-id="157d4-118">This instruction is insensitive to sign.</span></span>

<span data-ttu-id="157d4-119">O número de componentes extraídos do endereço é determinado pela dimensionalidade do *DST* u \# ou g \# .</span><span class="sxs-lookup"><span data-stu-id="157d4-119">The number of components taken from the address is determined by the dimensionality of *dst* u\# or g\#.</span></span>

<span data-ttu-id="157d4-120">Se o *DST* for um u \# , ele poderá ser declarado como RAW, tipado ou estruturado.</span><span class="sxs-lookup"><span data-stu-id="157d4-120">If *dst* is a u\#, it can be declared as raw, typed or structured.</span></span> <span data-ttu-id="157d4-121">Se digitado, ele deve ser declarado como UINT/Santo com o formato de recurso ligado sendo R32 \_ uint/ \_ Santo.</span><span class="sxs-lookup"><span data-stu-id="157d4-121">If typed, it must be declared as UINT/SINT with the bound resource format being R32\_UINT/\_SINT.</span></span>

<span data-ttu-id="157d4-122">Se o *DST* for g \# , ele deverá ser declarado como bruto ou estruturado.</span><span class="sxs-lookup"><span data-stu-id="157d4-122">If *dst* is g\#, it must be declared as raw or structured.</span></span>

<span data-ttu-id="157d4-123">Nada é retornado para o sombreador.</span><span class="sxs-lookup"><span data-stu-id="157d4-123">Nothing is returned to the shader.</span></span>

<span data-ttu-id="157d4-124">Se a invocação do sombreador estiver inativa, por exemplo, se o pixel tiver sido descartado anteriormente em sua execução ou se uma invocação de pixel/amostra existir apenas para servir como um auxiliar para um pixel/amostra real para derivações, essa instrução não alterará a memória de *DST* (silenciosamente).</span><span class="sxs-lookup"><span data-stu-id="157d4-124">If the shader invocation is inactive, for example if the pixel has been discarded earlier in its execution, or if a pixel/sample invocation only exists to serve as a helper to a real pixel/sample for derivatives, this instruction does not alter the *dst* memory at all (silently).</span></span>

<span data-ttu-id="157d4-125">O endereçamento fora dos limites em u não \# faz nada a ser gravado na memória, exceto se o u \# for estruturado e o deslocamento de byte na estrutura (segundo componente do endereço) estiver causando o acesso fora dos limites, todo o conteúdo do UAV se tornará indefinido.</span><span class="sxs-lookup"><span data-stu-id="157d4-125">Out of bounds addressing on u\# causes nothing to be written to memory, except if the u\# is structured, and byte offset into the struct (second component of the address) is causing the out of bounds access, then the entire contents of the UAV become undefined.</span></span>

<span data-ttu-id="157d4-126">O endereçamento fora dos limites em g \# (os limites desse g específico \# , em oposição a toda a memória compartilhada) faz com que todo o conteúdo de toda a memória compartilhada se torne indefinido.</span><span class="sxs-lookup"><span data-stu-id="157d4-126">Out of bounds addressing on g\# (the bounds of that particular g\#, as opposed to all shared memory) causes the entire contents of all shared memory to become undefined.</span></span>

<span data-ttu-id="157d4-127">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="157d4-127">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="157d4-128">Vértice</span><span class="sxs-lookup"><span data-stu-id="157d4-128">Vertex</span></span> | <span data-ttu-id="157d4-129">Envoltória</span><span class="sxs-lookup"><span data-stu-id="157d4-129">Hull</span></span> | <span data-ttu-id="157d4-130">Domínio</span><span class="sxs-lookup"><span data-stu-id="157d4-130">Domain</span></span> | <span data-ttu-id="157d4-131">Geometria</span><span class="sxs-lookup"><span data-stu-id="157d4-131">Geometry</span></span> | <span data-ttu-id="157d4-132">16x16</span><span class="sxs-lookup"><span data-stu-id="157d4-132">Pixel</span></span> | <span data-ttu-id="157d4-133">Computação</span><span class="sxs-lookup"><span data-stu-id="157d4-133">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="157d4-134">X</span><span class="sxs-lookup"><span data-stu-id="157d4-134">X</span></span>     | <span data-ttu-id="157d4-135">X</span><span class="sxs-lookup"><span data-stu-id="157d4-135">X</span></span>       |



 

<span data-ttu-id="157d4-136">Como UAVs estão disponíveis em todos os estágios do sombreador para o Direct3D 11,1, essa instrução se aplica a todos os estágios do sombreador para o tempo de execução do Direct3D 11,1, que está disponível a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="157d4-136">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="157d4-137">Vértice</span><span class="sxs-lookup"><span data-stu-id="157d4-137">Vertex</span></span> | <span data-ttu-id="157d4-138">Envoltória</span><span class="sxs-lookup"><span data-stu-id="157d4-138">Hull</span></span> | <span data-ttu-id="157d4-139">Domínio</span><span class="sxs-lookup"><span data-stu-id="157d4-139">Domain</span></span> | <span data-ttu-id="157d4-140">Geometria</span><span class="sxs-lookup"><span data-stu-id="157d4-140">Geometry</span></span> | <span data-ttu-id="157d4-141">16x16</span><span class="sxs-lookup"><span data-stu-id="157d4-141">Pixel</span></span> | <span data-ttu-id="157d4-142">Computação</span><span class="sxs-lookup"><span data-stu-id="157d4-142">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="157d4-143">X</span><span class="sxs-lookup"><span data-stu-id="157d4-143">X</span></span>      | <span data-ttu-id="157d4-144">X</span><span class="sxs-lookup"><span data-stu-id="157d4-144">X</span></span>    | <span data-ttu-id="157d4-145">X</span><span class="sxs-lookup"><span data-stu-id="157d4-145">X</span></span>      | <span data-ttu-id="157d4-146">X</span><span class="sxs-lookup"><span data-stu-id="157d4-146">X</span></span>        | <span data-ttu-id="157d4-147">X</span><span class="sxs-lookup"><span data-stu-id="157d4-147">X</span></span>     | <span data-ttu-id="157d4-148">X</span><span class="sxs-lookup"><span data-stu-id="157d4-148">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="157d4-149">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="157d4-149">Minimum Shader Model</span></span>

<span data-ttu-id="157d4-150">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="157d4-150">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="157d4-151">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="157d4-151">Shader Model</span></span>                                              | <span data-ttu-id="157d4-152">Com suporte</span><span class="sxs-lookup"><span data-stu-id="157d4-152">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="157d4-153">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="157d4-153">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="157d4-154">sim</span><span class="sxs-lookup"><span data-stu-id="157d4-154">yes</span></span>       |
| [<span data-ttu-id="157d4-155">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="157d4-155">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="157d4-156">não</span><span class="sxs-lookup"><span data-stu-id="157d4-156">no</span></span>        |
| [<span data-ttu-id="157d4-157">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="157d4-157">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="157d4-158">não</span><span class="sxs-lookup"><span data-stu-id="157d4-158">no</span></span>        |
| [<span data-ttu-id="157d4-159">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="157d4-159">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="157d4-160">não</span><span class="sxs-lookup"><span data-stu-id="157d4-160">no</span></span>        |
| [<span data-ttu-id="157d4-161">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="157d4-161">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="157d4-162">não</span><span class="sxs-lookup"><span data-stu-id="157d4-162">no</span></span>        |
| [<span data-ttu-id="157d4-163">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="157d4-163">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="157d4-164">não</span><span class="sxs-lookup"><span data-stu-id="157d4-164">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="157d4-165">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="157d4-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="157d4-166">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="157d4-166">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





