---
title: imm_atomic_alloc (SM5-ASM)
description: Incrementar atomicamente o contador de 32 bits oculto armazenado com uma contagem ou acréscimo de UAV (exibição de acesso não ordenado), retornando o valor original.
ms.assetid: 534FA3C3-6FAC-41DC-AC07-0E53FEED000C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28a97709629497bae9af0298789453ef1d1172b7
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103638877"
---
# <a name="imm_atomic_alloc-sm5---asm"></a><span data-ttu-id="6c738-103">\_alocação atômica \_ do IMM (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="6c738-103">imm\_atomic\_alloc (sm5 - asm)</span></span>

<span data-ttu-id="6c738-104">Incrementar atomicamente o contador de 32 bits oculto armazenado com uma contagem ou acréscimo de UAV (exibição de acesso não ordenado), retornando o valor original.</span><span class="sxs-lookup"><span data-stu-id="6c738-104">Atomically increment the hidden 32-bit counter stored with a Count or Append unordered access view (UAV), returning the original value.</span></span>



| <span data-ttu-id="6c738-105">\_ \_ dst0 de alocação atômica do IMM \[ . \_ \_ máscara de componente único \] , dstUAV</span><span class="sxs-lookup"><span data-stu-id="6c738-105">imm\_atomic\_alloc dst0\[.single\_component\_mask\], dstUAV</span></span> |
|-------------------------------------------------------------|



 



| <span data-ttu-id="6c738-106">Item</span><span class="sxs-lookup"><span data-stu-id="6c738-106">Item</span></span>                                                                                           | <span data-ttu-id="6c738-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="6c738-107">Description</span></span>                                                               |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span data-ttu-id="6c738-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="6c738-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                | <span data-ttu-id="6c738-109">\[in \] contém o valor do contador retornado.</span><span class="sxs-lookup"><span data-stu-id="6c738-109">\[in\] Contains the returned counter value.</span></span><br/>                    |
| <span data-ttu-id="6c738-110"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*</span><span class="sxs-lookup"><span data-stu-id="6c738-110"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*</span></span><br/> | <span data-ttu-id="6c738-111">\[em \] um buffer estruturado UAV com o sinalizador Count ou Append.</span><span class="sxs-lookup"><span data-stu-id="6c738-111">\[in\] A Structured Buffer UAV with the Count or Append flag.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="6c738-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="6c738-112">Remarks</span></span>

<span data-ttu-id="6c738-113">Há um valor de contador inteiro de 32 bits sem sinal oculto associado a uma exibição de buffer de contagem ou acréscimo que é inicializada quando a exibição é associada ao pipeline, incluindo a opção de manter o valor anterior.</span><span class="sxs-lookup"><span data-stu-id="6c738-113">There is a hidden unsigned 32-bit integer counter value associated with each Count or Append Buffer view which is initialized when the view is bound to the pipeline, including the option to keep the previous value.</span></span>

<span data-ttu-id="6c738-114">Essa instrução faz um incremento atômico do valor do contador, retornando o original para *dst0*.</span><span class="sxs-lookup"><span data-stu-id="6c738-114">This instruction does an atomic increment of the counter value, returning the original to *dst0*.</span></span>

<span data-ttu-id="6c738-115">Para um UAV de acréscimo, o valor retornado é válido somente para a duração da invocação do sombreador.</span><span class="sxs-lookup"><span data-stu-id="6c738-115">For an Append UAV, the returned value is only valid for the duration of the shader invocation.</span></span> <span data-ttu-id="6c738-116">Depois disso, a implementação pode reorganizar o layout da memória.</span><span class="sxs-lookup"><span data-stu-id="6c738-116">after that the implementation may rearrange the memory layout.</span></span> <span data-ttu-id="6c738-117">Qualquer endereçamento de memória com base no valor retornado deve ser limitado à invocação do sombreador.</span><span class="sxs-lookup"><span data-stu-id="6c738-117">Any memory addressing based on the returned value must be limited to the shader invocation.</span></span>

<span data-ttu-id="6c738-118">Para um Append UAV, na invocação do sombreador, o compilador HLSL pode usar o valor retornado como o índice de struct a ser usado para acessar o buffer estruturado.</span><span class="sxs-lookup"><span data-stu-id="6c738-118">For an Append UAV, within the shader invocation the HLSL compiler can use the returned value as the struct index to use for accessing the structured buffer.</span></span> <span data-ttu-id="6c738-119">Acessar qualquer índice de struct diferente daqueles locais retornados por chamada (s) para **a \_ \_ alocação atômica do IMM** ou [ \_ consumir](imm-atomic-consume--sm5---asm-.md) produzir resultados indefinidos, pois exatamente qual local de memória dentro do UAV está sendo acessado é aleatório e é corrigido somente pelo tempo de vida da invocação do sombreador.</span><span class="sxs-lookup"><span data-stu-id="6c738-119">Accessing any struct index other than those locations returned by call(s) to **imm\_atomic\_alloc** or [\_consume](imm-atomic-consume--sm5---asm-.md) produce undefined results in that exactly which memory location within the UAV is being accessed is random and only fixed for the lifetime of the shader invocation.</span></span>

<span data-ttu-id="6c738-120">Para um UAV de contagem, o valor retornado pode ser salvo pelo aplicativo como uma referência a um local fixo dentro do UAV que é significativo após a invocação do sombreador.</span><span class="sxs-lookup"><span data-stu-id="6c738-120">For a Count UAV, the returned value can be saved by the application as a reference to a fixed location within the UAV that is meaningful after the shader invocation is over.</span></span> <span data-ttu-id="6c738-121">Qualquer local em um UAV de contagem sempre pode ser acessado independentemente do que é o valor de contagem.</span><span class="sxs-lookup"><span data-stu-id="6c738-121">Any location in a Count UAV may always be accessed independent of what the count value is.</span></span>

<span data-ttu-id="6c738-122">Não há nenhum fixação MSS da contagem, portanto, ele encapsula o estouro.</span><span class="sxs-lookup"><span data-stu-id="6c738-122">There is no clamping of the count, so it wraps on overflow.</span></span>

<span data-ttu-id="6c738-123">O mesmo sombreador não pode tentar a **\_ \_ alocação do IMM Atomic** e o **IMM \_ Atomic \_ consume** no mesmo UAV.</span><span class="sxs-lookup"><span data-stu-id="6c738-123">The same shader cannot attempt both **imm\_atomic\_alloc** and **imm\_atomic\_consume** on the same UAV.</span></span> <span data-ttu-id="6c738-124">Além disso, a GPU não pode permitir que várias invocações de sombreador misturem a **\_ \_ alocação atômica do IMM** e o **IMM \_ Atomic \_ consume** no mesmo UAV.</span><span class="sxs-lookup"><span data-stu-id="6c738-124">Further, the GPU cannot allow multiple shader invocations to mix **imm\_atomic\_alloc** and **imm\_atomic\_consume** on the same UAV.</span></span>

<span data-ttu-id="6c738-125">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="6c738-125">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="6c738-126">Vértice</span><span class="sxs-lookup"><span data-stu-id="6c738-126">Vertex</span></span> | <span data-ttu-id="6c738-127">Envoltória</span><span class="sxs-lookup"><span data-stu-id="6c738-127">Hull</span></span> | <span data-ttu-id="6c738-128">Domínio</span><span class="sxs-lookup"><span data-stu-id="6c738-128">Domain</span></span> | <span data-ttu-id="6c738-129">Geometria</span><span class="sxs-lookup"><span data-stu-id="6c738-129">Geometry</span></span> | <span data-ttu-id="6c738-130">16x16</span><span class="sxs-lookup"><span data-stu-id="6c738-130">Pixel</span></span> | <span data-ttu-id="6c738-131">Computação</span><span class="sxs-lookup"><span data-stu-id="6c738-131">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="6c738-132">X</span><span class="sxs-lookup"><span data-stu-id="6c738-132">X</span></span>     | <span data-ttu-id="6c738-133">X</span><span class="sxs-lookup"><span data-stu-id="6c738-133">X</span></span>       |



 

<span data-ttu-id="6c738-134">Como UAVs estão disponíveis em todos os estágios do sombreador para o Direct3D 11,1, essa instrução se aplica a todos os estágios do sombreador para o tempo de execução do Direct3D 11,1, que está disponível a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="6c738-134">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="6c738-135">Vértice</span><span class="sxs-lookup"><span data-stu-id="6c738-135">Vertex</span></span> | <span data-ttu-id="6c738-136">Envoltória</span><span class="sxs-lookup"><span data-stu-id="6c738-136">Hull</span></span> | <span data-ttu-id="6c738-137">Domínio</span><span class="sxs-lookup"><span data-stu-id="6c738-137">Domain</span></span> | <span data-ttu-id="6c738-138">Geometria</span><span class="sxs-lookup"><span data-stu-id="6c738-138">Geometry</span></span> | <span data-ttu-id="6c738-139">16x16</span><span class="sxs-lookup"><span data-stu-id="6c738-139">Pixel</span></span> | <span data-ttu-id="6c738-140">Computação</span><span class="sxs-lookup"><span data-stu-id="6c738-140">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="6c738-141">X</span><span class="sxs-lookup"><span data-stu-id="6c738-141">X</span></span>      | <span data-ttu-id="6c738-142">X</span><span class="sxs-lookup"><span data-stu-id="6c738-142">X</span></span>    | <span data-ttu-id="6c738-143">X</span><span class="sxs-lookup"><span data-stu-id="6c738-143">X</span></span>      | <span data-ttu-id="6c738-144">X</span><span class="sxs-lookup"><span data-stu-id="6c738-144">X</span></span>        | <span data-ttu-id="6c738-145">X</span><span class="sxs-lookup"><span data-stu-id="6c738-145">X</span></span>     | <span data-ttu-id="6c738-146">X</span><span class="sxs-lookup"><span data-stu-id="6c738-146">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="6c738-147">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="6c738-147">Minimum Shader Model</span></span>

<span data-ttu-id="6c738-148">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="6c738-148">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="6c738-149">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="6c738-149">Shader Model</span></span>                                              | <span data-ttu-id="6c738-150">Com suporte</span><span class="sxs-lookup"><span data-stu-id="6c738-150">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="6c738-151">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="6c738-151">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="6c738-152">sim</span><span class="sxs-lookup"><span data-stu-id="6c738-152">yes</span></span>       |
| [<span data-ttu-id="6c738-153">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="6c738-153">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="6c738-154">não</span><span class="sxs-lookup"><span data-stu-id="6c738-154">no</span></span>        |
| [<span data-ttu-id="6c738-155">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="6c738-155">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="6c738-156">não</span><span class="sxs-lookup"><span data-stu-id="6c738-156">no</span></span>        |
| [<span data-ttu-id="6c738-157">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6c738-157">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="6c738-158">não</span><span class="sxs-lookup"><span data-stu-id="6c738-158">no</span></span>        |
| [<span data-ttu-id="6c738-159">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6c738-159">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="6c738-160">não</span><span class="sxs-lookup"><span data-stu-id="6c738-160">no</span></span>        |
| [<span data-ttu-id="6c738-161">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6c738-161">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="6c738-162">não</span><span class="sxs-lookup"><span data-stu-id="6c738-162">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="6c738-163">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6c738-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6c738-164">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6c738-164">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





