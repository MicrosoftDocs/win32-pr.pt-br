---
title: dcl_uav_structured (SM5-ASM)
description: Declare um UAV (modo de exibição de acesso não ordenado) para uso por um sombreador. | dcl_uav_structured (SM5-ASM)
ms.assetid: 40D6B8F7-8A41-4EFE-A8A3-44A646B4D43B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3dc02396f4837a095506e736d81ea8c00eb0669f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104172698"
---
# <a name="dcl_uav_structured-sm5---asm"></a><span data-ttu-id="22596-104">DCL \_ UAV \_ estruturado (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="22596-104">dcl\_uav\_structured (sm5 - asm)</span></span>

<span data-ttu-id="22596-105">Declare um UAV (modo de exibição de acesso não ordenado) para uso por um sombreador.</span><span class="sxs-lookup"><span data-stu-id="22596-105">Declare an unordered access view (UAV) for use by a shader.</span></span>



| <span data-ttu-id="22596-106">\_UAV \_ estruturada \[ \_ de DCL GLC \] dstUAV, structByteStride</span><span class="sxs-lookup"><span data-stu-id="22596-106">dcl\_uav\_structured\[\_glc\] dstUAV, structByteStride</span></span> |
|--------------------------------------------------------|



 



| <span data-ttu-id="22596-107">Item</span><span class="sxs-lookup"><span data-stu-id="22596-107">Item</span></span>                                                                                                                                   | <span data-ttu-id="22596-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="22596-108">Description</span></span>                                           |
|----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span data-ttu-id="22596-109"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*</span><span class="sxs-lookup"><span data-stu-id="22596-109"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*</span></span><br/>                                         | <span data-ttu-id="22596-110">\[no \] UAV.</span><span class="sxs-lookup"><span data-stu-id="22596-110">\[in\] The UAV.</span></span><br/>                            |
| <span data-ttu-id="22596-111"><span id="structByteStride"></span><span id="structbytestride"></span><span id="STRUCTBYTESTRIDE"></span>*structByteStride*</span><span class="sxs-lookup"><span data-stu-id="22596-111"><span id="structByteStride"></span><span id="structbytestride"></span><span id="STRUCTBYTESTRIDE"></span>*structByteStride*</span></span><br/> | <span data-ttu-id="22596-112">\[no \] tamanho da estrutura em bytes.</span><span class="sxs-lookup"><span data-stu-id="22596-112">\[in\] The size of the structure in bytes.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="22596-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="22596-113">Remarks</span></span>

<span data-ttu-id="22596-114">*dstUAV* é um \# registro u declarado como uma referência a um UnorderedAccessView de um buffer estruturado com o stride especificado que deve ser associado ao slot UAV \# na API.</span><span class="sxs-lookup"><span data-stu-id="22596-114">*dstUAV* is a u\# register declared as a reference to an UnorderedAccessView of a structured buffer with the specified stride that must be bound to UAV slot \# at the API.</span></span>

<span data-ttu-id="22596-115">O conteúdo da estrutura não tem tipo; as operações executadas na memória podem interpretar implicitamente os dados como tendo um tipo.</span><span class="sxs-lookup"><span data-stu-id="22596-115">The contents of the structure have no type; operations performed on the memory may implicitly interpret the data as having a type.</span></span>

<span data-ttu-id="22596-116">*structByteStride* é o tamanho da estrutura em bytes no buffer que está sendo declarado.</span><span class="sxs-lookup"><span data-stu-id="22596-116">*structByteStride* is the size of the structure in bytes in the buffer being declared.</span></span> <span data-ttu-id="22596-117">Esse valor deve ser maior que zero.</span><span class="sxs-lookup"><span data-stu-id="22596-117">This value must be greater than zero.</span></span> <span data-ttu-id="22596-118">*structByteStride* é do tipo uint e deve ser um múltiplo de 4.</span><span class="sxs-lookup"><span data-stu-id="22596-118">*structByteStride* is of type uint, and must be a multiple of 4.</span></span>

<span data-ttu-id="22596-119">Instruções que fazem referência a um u estruturado \# usam um endereço 2D, em que o primeiro componente escolhe \[ struct \] e o segundo componente escolhe o \[ deslocamento dentro de struct, em bytes alinhados \] .</span><span class="sxs-lookup"><span data-stu-id="22596-119">Instructions that reference a structured u\# take a 2D address, where the first component picks \[struct\], and the second component picks \[offset within struct, in aligned bytes\].</span></span>

<span data-ttu-id="22596-120">O \_ sinalizador GLC significa "globalmente coerente".</span><span class="sxs-lookup"><span data-stu-id="22596-120">The \_glc flag means for"globally coherent".</span></span> <span data-ttu-id="22596-121">A ausência de \_ GLC significa que o UAV está sendo declarado somente como "grupo coerente" no sombreador de computação ou "coerente localmente" em uma invocação de sombreador de pixel único.</span><span class="sxs-lookup"><span data-stu-id="22596-121">The absence of \_glc means the UAV is being declared only as "group coherent" in the compute shader, or "locally coherent" in a single pixel shader invocation.</span></span>

<span data-ttu-id="22596-122">O \_ sinalizador OPC é o contador de preservação de ordem.</span><span class="sxs-lookup"><span data-stu-id="22596-122">The \_opc flag is the order preserving counter.</span></span> <span data-ttu-id="22596-123">Isso indica que, se um UAV estiver associado ao slot \# (u \# ), ele deverá ter sido criado com o sinalizador Counter.</span><span class="sxs-lookup"><span data-stu-id="22596-123">It indicates that if a UAV is bound to slot \# (u\#), it must have been created with the COUNTER flag.</span></span> <span data-ttu-id="22596-124">Isso significa que as operações do [IMM \_ Atomic \_ Alloc](imm-atomic-alloc--sm5---asm-.md) ou do [IMM \_ Atomic \_ consume](imm-atomic-consume--sm5---asm-.md) no sombreador manipulam um contador cujos valores podem ser usados no sombreador como uma referência permanente a um local no UAV.</span><span class="sxs-lookup"><span data-stu-id="22596-124">This means that [imm\_atomic\_alloc](imm-atomic-alloc--sm5---asm-.md) or [imm\_atomic\_consume](imm-atomic-consume--sm5---asm-.md) operations in the shader manipulate a counter whose values can be used in the shader as a permanent reference to a location in the UAV.</span></span> <span data-ttu-id="22596-125">Os dados não podem ser reordenados depois que o sombreador terminar.</span><span class="sxs-lookup"><span data-stu-id="22596-125">Data cannot be reordered after the shader is over.</span></span>

<span data-ttu-id="22596-126">A ausência do \_ sinalizador OPC significa que se o sombreador usar as instruções de[ \_ \_ alocação atômica do IMM](imm-atomic-alloc--sm5---asm-.md) ou de [ \_ \_ consumo do IMM Atomic](imm-atomic-consume--sm5---asm-.md) e um UAV estiver associado ao slot \# (u), ele deverá ter sido criado com o sinalizador Append, que fornece um contador que não garante que a ordem seja preservada após a invocação do sombreador.</span><span class="sxs-lookup"><span data-stu-id="22596-126">The absence of the \_opc flag means that if the shader uses[imm\_atomic\_alloc](imm-atomic-alloc--sm5---asm-.md) or [imm\_atomic\_consume](imm-atomic-consume--sm5---asm-.md) instructions and a UAV is bound to slot \# (u), it must have been created with the APPEND flag, which provides a counter that does not guarantee order is preserved after the shader invocation.</span></span>

<span data-ttu-id="22596-127">Se o \_ sinalizador OPC estiver ausente e o sombreador não contiver as instruções de contêiner [IMM \_ Atomic \_ Alloc](imm-atomic-alloc--sm5---asm-.md) ou [IMM \_ Atomic \_ consume](imm-atomic-consume--sm5---asm-.md) , um UAV associado ao slot \# (u) poderá ter sido criado com o sinalizador Counter (o contador não será usado por este sombreador), sem sinalizador (nenhum contador), mas não com o sinalizador Append.</span><span class="sxs-lookup"><span data-stu-id="22596-127">If the \_opc flag is absent and the shader does not contain [imm\_atomic\_alloc](imm-atomic-alloc--sm5---asm-.md) or [imm\_atomic\_consume](imm-atomic-consume--sm5---asm-.md) instructions, a UAV bound to slot \# (u) is permitted to have been created with the COUNTER flag (the counter will go unused by this shader), no flag (no counter), but not with the APPEND flag.</span></span>

> [!Note]  
> <span data-ttu-id="22596-128">o cs \_ 4 \_ 0 e o cs \_ 4 \_ 1 dão suporte ao **\_ tgsm DCL \_ estruturado**, mas não ao [DCL \_ tgsm \_ RAW](dcl-tgsm-raw--sm5---asm-.md).</span><span class="sxs-lookup"><span data-stu-id="22596-128">cs\_4\_0 and cs\_4\_1 supports **dcl\_tgsm\_structured**, but not [dcl\_tgsm\_raw](dcl-tgsm-raw--sm5---asm-.md).</span></span>

 

<span data-ttu-id="22596-129">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="22596-129">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="22596-130">Vértice</span><span class="sxs-lookup"><span data-stu-id="22596-130">Vertex</span></span> | <span data-ttu-id="22596-131">Envoltória</span><span class="sxs-lookup"><span data-stu-id="22596-131">Hull</span></span> | <span data-ttu-id="22596-132">Domínio</span><span class="sxs-lookup"><span data-stu-id="22596-132">Domain</span></span> | <span data-ttu-id="22596-133">Geometria</span><span class="sxs-lookup"><span data-stu-id="22596-133">Geometry</span></span> | <span data-ttu-id="22596-134">16x16</span><span class="sxs-lookup"><span data-stu-id="22596-134">Pixel</span></span> | <span data-ttu-id="22596-135">Computação</span><span class="sxs-lookup"><span data-stu-id="22596-135">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="22596-136">X</span><span class="sxs-lookup"><span data-stu-id="22596-136">X</span></span>     | <span data-ttu-id="22596-137">X</span><span class="sxs-lookup"><span data-stu-id="22596-137">X</span></span>       |



 

<span data-ttu-id="22596-138">Como UAVs estão disponíveis em todos os estágios do sombreador para o Direct3D 11,1, essa instrução se aplica a todos os estágios do sombreador para o tempo de execução do Direct3D 11,1, que está disponível a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="22596-138">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="22596-139">Vértice</span><span class="sxs-lookup"><span data-stu-id="22596-139">Vertex</span></span> | <span data-ttu-id="22596-140">Envoltória</span><span class="sxs-lookup"><span data-stu-id="22596-140">Hull</span></span> | <span data-ttu-id="22596-141">Domínio</span><span class="sxs-lookup"><span data-stu-id="22596-141">Domain</span></span> | <span data-ttu-id="22596-142">Geometria</span><span class="sxs-lookup"><span data-stu-id="22596-142">Geometry</span></span> | <span data-ttu-id="22596-143">16x16</span><span class="sxs-lookup"><span data-stu-id="22596-143">Pixel</span></span> | <span data-ttu-id="22596-144">Computação</span><span class="sxs-lookup"><span data-stu-id="22596-144">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="22596-145">X</span><span class="sxs-lookup"><span data-stu-id="22596-145">X</span></span>      | <span data-ttu-id="22596-146">X</span><span class="sxs-lookup"><span data-stu-id="22596-146">X</span></span>    | <span data-ttu-id="22596-147">X</span><span class="sxs-lookup"><span data-stu-id="22596-147">X</span></span>      | <span data-ttu-id="22596-148">X</span><span class="sxs-lookup"><span data-stu-id="22596-148">X</span></span>        | <span data-ttu-id="22596-149">X</span><span class="sxs-lookup"><span data-stu-id="22596-149">X</span></span>     | <span data-ttu-id="22596-150">X</span><span class="sxs-lookup"><span data-stu-id="22596-150">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="22596-151">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="22596-151">Minimum Shader Model</span></span>

<span data-ttu-id="22596-152">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="22596-152">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="22596-153">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="22596-153">Shader Model</span></span>                                              | <span data-ttu-id="22596-154">Com suporte</span><span class="sxs-lookup"><span data-stu-id="22596-154">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="22596-155">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="22596-155">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="22596-156">sim</span><span class="sxs-lookup"><span data-stu-id="22596-156">yes</span></span>       |
| [<span data-ttu-id="22596-157">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="22596-157">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="22596-158">não</span><span class="sxs-lookup"><span data-stu-id="22596-158">no</span></span>        |
| [<span data-ttu-id="22596-159">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="22596-159">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="22596-160">não</span><span class="sxs-lookup"><span data-stu-id="22596-160">no</span></span>        |
| [<span data-ttu-id="22596-161">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="22596-161">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="22596-162">não</span><span class="sxs-lookup"><span data-stu-id="22596-162">no</span></span>        |
| [<span data-ttu-id="22596-163">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="22596-163">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="22596-164">não</span><span class="sxs-lookup"><span data-stu-id="22596-164">no</span></span>        |
| [<span data-ttu-id="22596-165">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="22596-165">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="22596-166">não</span><span class="sxs-lookup"><span data-stu-id="22596-166">no</span></span>        |



 

> [!Note]  
> <span data-ttu-id="22596-167">Essa instrução tem suporte em cs \_ 4 \_ 0 e cs \_ 4 \_ 1.</span><span class="sxs-lookup"><span data-stu-id="22596-167">This instruction is supported in cs\_4\_0 and cs\_4\_1.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="22596-168">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="22596-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22596-169">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="22596-169">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





