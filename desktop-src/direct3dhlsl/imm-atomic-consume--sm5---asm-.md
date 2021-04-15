---
title: imm_atomic_consume (SM5-ASM)
description: Decrementar atomicamente o contador de 32 bits oculto armazenado com uma contagem ou acréscimo de UAV (exibição de acesso não ordenado), retornando o novo valor.
ms.assetid: 1115C318-2F86-4161-AC5C-2A61A262DC28
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a1c6fe01ddb92b2ce870b16254f75c52cadd341
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104988595"
---
# <a name="imm_atomic_consume-sm5---asm"></a><span data-ttu-id="6e96f-103">\_consume atômico \_ do IMM (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="6e96f-103">imm\_atomic\_consume (sm5 - asm)</span></span>

<span data-ttu-id="6e96f-104">Decrementar atomicamente o contador de 32 bits oculto armazenado com uma contagem ou acréscimo de UAV (exibição de acesso não ordenado), retornando o novo valor.</span><span class="sxs-lookup"><span data-stu-id="6e96f-104">Atomically decrement the hidden 32-bit counter stored with a Count or Append unordered access view (UAV), returning the new value.</span></span>



| <span data-ttu-id="6e96f-105">o IMM \_ Atomic \_ consume dst0 \[ . \_ máscara de componente único \_ \] , dstUAV</span><span class="sxs-lookup"><span data-stu-id="6e96f-105">imm\_atomic\_consume dst0\[.single\_component\_mask\], dstUAV</span></span> |
|---------------------------------------------------------------|



 



| <span data-ttu-id="6e96f-106">Item</span><span class="sxs-lookup"><span data-stu-id="6e96f-106">Item</span></span>                                                                                           | <span data-ttu-id="6e96f-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="6e96f-107">Description</span></span>                                                               |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span data-ttu-id="6e96f-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="6e96f-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                | <span data-ttu-id="6e96f-109">\[in \] contém o valor do contador original retornado.</span><span class="sxs-lookup"><span data-stu-id="6e96f-109">\[in\] Contains the returned original counter value.</span></span><br/>           |
| <span data-ttu-id="6e96f-110"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*</span><span class="sxs-lookup"><span data-stu-id="6e96f-110"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*</span></span><br/> | <span data-ttu-id="6e96f-111">\[em \] um buffer estruturado UAV com o sinalizador Count ou Append.</span><span class="sxs-lookup"><span data-stu-id="6e96f-111">\[in\] A structured buffer UAV with the Count or Append flag.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="6e96f-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="6e96f-112">Remarks</span></span>

<span data-ttu-id="6e96f-113">Consulte [a \_ \_ alocação atômica do IMM](imm-atomic-alloc--sm5---asm-.md) para obter uma discussão sobre a validade do valor da contagem retornada, dependendo se o UAV é Count ou Append.</span><span class="sxs-lookup"><span data-stu-id="6e96f-113">See [imm\_atomic\_alloc](imm-atomic-alloc--sm5---asm-.md) for a discussion about the validity of the returned count value depending on whether the UAV is Count or Append.</span></span> <span data-ttu-id="6e96f-114">O mesmo se aplica **ao \_ \_ consumo atômico do IMM**.</span><span class="sxs-lookup"><span data-stu-id="6e96f-114">The same applies for **imm\_atomic\_consume**.</span></span>

<span data-ttu-id="6e96f-115">o **IMM \_ Atomic \_ consume** faz um decréscimo atômico do valor do contador, retornando o novo valor para *dst0*.</span><span class="sxs-lookup"><span data-stu-id="6e96f-115">**imm\_atomic\_consume** does an atomic decrement of the counter value, returning the new value to *dst0*.</span></span>

<span data-ttu-id="6e96f-116">Não há nenhum fixação MSS da contagem, portanto, ele encapsula em estouro negativo.</span><span class="sxs-lookup"><span data-stu-id="6e96f-116">There is no clamping of the count, so it wraps on underflow.</span></span>

<span data-ttu-id="6e96f-117">O mesmo sombreador não pode tentar a **\_ \_ alocação do IMM Atomic** e o **IMM \_ Atomic \_ consume** no mesmo UAV.</span><span class="sxs-lookup"><span data-stu-id="6e96f-117">The same shader cannot attempt both **imm\_atomic\_alloc** and **imm\_atomic\_consume** on the same UAV.</span></span> <span data-ttu-id="6e96f-118">Além disso, a GPU não pode permitir que várias invocações de sombreador misturem a **\_ \_ alocação atômica do IMM** e o **IMM \_ Atomic \_ consume** no mesmo UAV.</span><span class="sxs-lookup"><span data-stu-id="6e96f-118">Further, the GPU cannot allow multiple shader invocations to mix **imm\_atomic\_alloc** and **imm\_atomic\_consume** on the same UAV.</span></span>

<span data-ttu-id="6e96f-119">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="6e96f-119">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="6e96f-120">Vértice</span><span class="sxs-lookup"><span data-stu-id="6e96f-120">Vertex</span></span> | <span data-ttu-id="6e96f-121">Envoltória</span><span class="sxs-lookup"><span data-stu-id="6e96f-121">Hull</span></span> | <span data-ttu-id="6e96f-122">Domínio</span><span class="sxs-lookup"><span data-stu-id="6e96f-122">Domain</span></span> | <span data-ttu-id="6e96f-123">Geometria</span><span class="sxs-lookup"><span data-stu-id="6e96f-123">Geometry</span></span> | <span data-ttu-id="6e96f-124">16x16</span><span class="sxs-lookup"><span data-stu-id="6e96f-124">Pixel</span></span> | <span data-ttu-id="6e96f-125">Computação</span><span class="sxs-lookup"><span data-stu-id="6e96f-125">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="6e96f-126">X</span><span class="sxs-lookup"><span data-stu-id="6e96f-126">X</span></span>     | <span data-ttu-id="6e96f-127">X</span><span class="sxs-lookup"><span data-stu-id="6e96f-127">X</span></span>       |



 

<span data-ttu-id="6e96f-128">Como UAVs estão disponíveis em todos os estágios do sombreador para o Direct3D 11,1, essa instrução se aplica a todos os estágios do sombreador para o tempo de execução do Direct3D 11,1, que está disponível a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="6e96f-128">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="6e96f-129">Vértice</span><span class="sxs-lookup"><span data-stu-id="6e96f-129">Vertex</span></span> | <span data-ttu-id="6e96f-130">Envoltória</span><span class="sxs-lookup"><span data-stu-id="6e96f-130">Hull</span></span> | <span data-ttu-id="6e96f-131">Domínio</span><span class="sxs-lookup"><span data-stu-id="6e96f-131">Domain</span></span> | <span data-ttu-id="6e96f-132">Geometria</span><span class="sxs-lookup"><span data-stu-id="6e96f-132">Geometry</span></span> | <span data-ttu-id="6e96f-133">16x16</span><span class="sxs-lookup"><span data-stu-id="6e96f-133">Pixel</span></span> | <span data-ttu-id="6e96f-134">Computação</span><span class="sxs-lookup"><span data-stu-id="6e96f-134">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="6e96f-135">X</span><span class="sxs-lookup"><span data-stu-id="6e96f-135">X</span></span>      | <span data-ttu-id="6e96f-136">X</span><span class="sxs-lookup"><span data-stu-id="6e96f-136">X</span></span>    | <span data-ttu-id="6e96f-137">X</span><span class="sxs-lookup"><span data-stu-id="6e96f-137">X</span></span>      | <span data-ttu-id="6e96f-138">X</span><span class="sxs-lookup"><span data-stu-id="6e96f-138">X</span></span>        | <span data-ttu-id="6e96f-139">X</span><span class="sxs-lookup"><span data-stu-id="6e96f-139">X</span></span>     | <span data-ttu-id="6e96f-140">X</span><span class="sxs-lookup"><span data-stu-id="6e96f-140">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="6e96f-141">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="6e96f-141">Minimum Shader Model</span></span>

<span data-ttu-id="6e96f-142">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="6e96f-142">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="6e96f-143">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="6e96f-143">Shader Model</span></span>                                              | <span data-ttu-id="6e96f-144">Com suporte</span><span class="sxs-lookup"><span data-stu-id="6e96f-144">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="6e96f-145">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="6e96f-145">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="6e96f-146">sim</span><span class="sxs-lookup"><span data-stu-id="6e96f-146">yes</span></span>       |
| [<span data-ttu-id="6e96f-147">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="6e96f-147">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="6e96f-148">não</span><span class="sxs-lookup"><span data-stu-id="6e96f-148">no</span></span>        |
| [<span data-ttu-id="6e96f-149">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="6e96f-149">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="6e96f-150">não</span><span class="sxs-lookup"><span data-stu-id="6e96f-150">no</span></span>        |
| [<span data-ttu-id="6e96f-151">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6e96f-151">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="6e96f-152">não</span><span class="sxs-lookup"><span data-stu-id="6e96f-152">no</span></span>        |
| [<span data-ttu-id="6e96f-153">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6e96f-153">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="6e96f-154">não</span><span class="sxs-lookup"><span data-stu-id="6e96f-154">no</span></span>        |
| [<span data-ttu-id="6e96f-155">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6e96f-155">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="6e96f-156">não</span><span class="sxs-lookup"><span data-stu-id="6e96f-156">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="6e96f-157">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6e96f-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e96f-158">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6e96f-158">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





