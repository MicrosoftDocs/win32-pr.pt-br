---
title: dcl_input vGSInstanceID (SM5-ASM)
description: Habilitar a instanciação do sombreador de geometria.
ms.assetid: 47B9BAD5-0FFF-4DB7-B34A-7811B8A4F792
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3134a9d372f1fde5457f26235fe9a6a5439c58c1
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104293600"
---
# <a name="dcl_input-vgsinstanceid-sm5---asm"></a><span data-ttu-id="57d72-103">\_vGSInstanceID de entrada DCL (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="57d72-103">dcl\_input vGSInstanceID (sm5 - asm)</span></span>

<span data-ttu-id="57d72-104">Habilitar a instanciação do sombreador de geometria.</span><span class="sxs-lookup"><span data-stu-id="57d72-104">Enable geometry shader instancing.</span></span>



| <span data-ttu-id="57d72-105">\_vGSInstanceID de entrada DCL, instanceCount</span><span class="sxs-lookup"><span data-stu-id="57d72-105">dcl\_input vGSInstanceID, instanceCount</span></span> |
|-----------------------------------------|



 



| <span data-ttu-id="57d72-106">Item</span><span class="sxs-lookup"><span data-stu-id="57d72-106">Item</span></span>                                                                                                                       | <span data-ttu-id="57d72-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="57d72-107">Description</span></span>                           |
|----------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span data-ttu-id="57d72-108"><span id="vGSInstanceID"></span><span id="vgsinstanceid"></span><span id="VGSINSTANCEID"></span>*vGSInstanceID*</span><span class="sxs-lookup"><span data-stu-id="57d72-108"><span id="vGSInstanceID"></span><span id="vgsinstanceid"></span><span id="VGSINSTANCEID"></span>*vGSInstanceID*</span></span><br/> | <span data-ttu-id="57d72-109">\[na \] ID da instância.</span><span class="sxs-lookup"><span data-stu-id="57d72-109">\[in\] The instance ID.</span></span><br/>    |
| <span data-ttu-id="57d72-110"><span id="instanceCount"></span><span id="instancecount"></span><span id="INSTANCECOUNT"></span>*instanceCount*</span><span class="sxs-lookup"><span data-stu-id="57d72-110"><span id="instanceCount"></span><span id="instancecount"></span><span id="INSTANCECOUNT"></span>*instanceCount*</span></span><br/> | <span data-ttu-id="57d72-111">\[na \] contagem de instâncias.</span><span class="sxs-lookup"><span data-stu-id="57d72-111">\[in\] The instance count.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="57d72-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="57d72-112">Remarks</span></span>

<span data-ttu-id="57d72-113">O parâmetro *instanceCount* da declaração especifica quantas instâncias o sombreador de geometria deve executar para cada primitiva de entrada.</span><span class="sxs-lookup"><span data-stu-id="57d72-113">The *instanceCount* parameter of the declaration specifies how many instances the geometry shader should execute for each input primitive.</span></span> <span data-ttu-id="57d72-114">O valor máximo para *instanceCount* é 32.</span><span class="sxs-lookup"><span data-stu-id="57d72-114">The maximum value for *instanceCount* is 32.</span></span>

<span data-ttu-id="57d72-115">O número máximo de vértices declarados para saída, via [**DCL \_ maxOutputVertexCount**](dcl-maxoutputvertexcount.md), aplica-se individualmente a cada instância.</span><span class="sxs-lookup"><span data-stu-id="57d72-115">The maximum number of vertices declared for output, via [**dcl\_maxOutputVertexCount**](dcl-maxoutputvertexcount.md), applies individually to each instance.</span></span>

<span data-ttu-id="57d72-116">A contagem de instâncias nessa declaração, multiplicada pela contagem máxima de vértices por instância via [**DCL \_ maxOutputVertexCount**](dcl-maxoutputvertexcount.md), deve ser <= 1024.</span><span class="sxs-lookup"><span data-stu-id="57d72-116">The instance count in this declaration, multiplied by the maximum vertex count per instance via [**dcl\_maxOutputVertexCount**](dcl-maxoutputvertexcount.md), must be <= 1024.</span></span>

<span data-ttu-id="57d72-117">A quantidade de dados que uma determinada instância de sombreador de geometria pode emitir é de 1024 escalares máximos, validadas contando todos os escalares declarados para entrada e multiplicando pela contagem de vértices de saída declarada.</span><span class="sxs-lookup"><span data-stu-id="57d72-117">The amount of data that a given geometry shader instance can emit is 1024 scalars maximum, validated by counting up all scalars declared for input and multiplying by the declared output vertex count.</span></span>

<span data-ttu-id="57d72-118">O uso da instanciação do sombreador de geometria aumenta efetivamente a quantidade total de dados que podem ser emitidos por primitivo de entrada.</span><span class="sxs-lookup"><span data-stu-id="57d72-118">Use of geometry shader instancing effectively increases the total amount of data that can be emitted per input primitive.</span></span> <span data-ttu-id="57d72-119">1024 escalares para uma única instância gera até 1024 \* 32 escalares de dados de saída em todas as instâncias de sombreador de geometria para um único primitivo de entrada.</span><span class="sxs-lookup"><span data-stu-id="57d72-119">1024 scalars for a single instance yields up to 1024\*32 scalars of output data across all geometry shader instances for a single input primitive.</span></span> <span data-ttu-id="57d72-120">No entanto, quanto mais instâncias, menor é o número de vértices que cada instância pode emitir.</span><span class="sxs-lookup"><span data-stu-id="57d72-120">However the more instances, the fewer vertices each instance can emit.</span></span> <span data-ttu-id="57d72-121">Uma única instância (sem instanciação) pode emitir 1024 vértices.</span><span class="sxs-lookup"><span data-stu-id="57d72-121">A single instance (no instancing) can emit 1024 vertices.</span></span> <span data-ttu-id="57d72-122">Se você declarar \* instâncias de 32, isso significa que cada instância só poderá produzir uma saída de 1024/32 = 32 vértices.</span><span class="sxs-lookup"><span data-stu-id="57d72-122">If you declare \*32 instances it means each instance can only output 1024/32 = 32 vertices.</span></span>

<span data-ttu-id="57d72-123">A declaração de instanciação do sombreador de geometria torna disponível para o programa um registro de entrada de inteiro de 32 bits autônomo, *vGSInstanceID*.</span><span class="sxs-lookup"><span data-stu-id="57d72-123">The geometry shader instancing declaration makes available to the program a standalone 32-bit integer input register, *vGSInstanceID*.</span></span> <span data-ttu-id="57d72-124">Cada instância de sombreador de geometria é identificada pelo valor contido em *vGSInstanceID* \[ 0, 1, 2... \] .</span><span class="sxs-lookup"><span data-stu-id="57d72-124">Each geometry shader instance is identified by the value contained in *vGSInstanceID* \[0,1,2...\].</span></span>

<span data-ttu-id="57d72-125">*vGSInstanceID* não faz parte da matriz de vértice de entrada do sombreador de geometria (por exemplo, 3 vértices ao inserir um triângulo).</span><span class="sxs-lookup"><span data-stu-id="57d72-125">*vGSInstanceID* is not part of the geometry shader input vertex array (e.g. 3 vertices when inputting a triangle).</span></span> <span data-ttu-id="57d72-126">O registro de *vGSInstanceID* permanece por conta própria, como vPrimitiveID.</span><span class="sxs-lookup"><span data-stu-id="57d72-126">The *vGSInstanceID* register stands on its own, like vPrimitiveID.</span></span>

<span data-ttu-id="57d72-127">Quando cada instância de sombreador de geometria termina, há um corte implícito na topologia de saída, portanto, as instâncias consecutivas não dependem umas das outras.</span><span class="sxs-lookup"><span data-stu-id="57d72-127">When each geometry shader instance ends, there is an implicit cut in the output topology, so consecutive instances do not depend on each other.</span></span>

<span data-ttu-id="57d72-128">Embora o hardware possa executar cada instância de sombreador de geometria em paralelo, a saída de todas as instâncias no final é serializada como se todas as invocações de sombreador de geometria em instância executassem sequencialmente em um loop Iterando *vGSInstanceID* de 0 a *instanceCount*-1, com a topologia de saída implícita recorta no final de cada instância.</span><span class="sxs-lookup"><span data-stu-id="57d72-128">Although hardware may execute each geometry shader instance in parallel, the output of all instances at the end is serialized as if all the instanced geometry shader invocations ran sequentially in a loop iterating *vGSInstanceID* from 0 to *instanceCount*-1, with implicit output topology cuts at the end of each instance.</span></span>

<span data-ttu-id="57d72-129">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="57d72-129">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="57d72-130">Vértice</span><span class="sxs-lookup"><span data-stu-id="57d72-130">Vertex</span></span> | <span data-ttu-id="57d72-131">Envoltória</span><span class="sxs-lookup"><span data-stu-id="57d72-131">Hull</span></span> | <span data-ttu-id="57d72-132">Domínio</span><span class="sxs-lookup"><span data-stu-id="57d72-132">Domain</span></span> | <span data-ttu-id="57d72-133">Geometria</span><span class="sxs-lookup"><span data-stu-id="57d72-133">Geometry</span></span> | <span data-ttu-id="57d72-134">16x16</span><span class="sxs-lookup"><span data-stu-id="57d72-134">Pixel</span></span> | <span data-ttu-id="57d72-135">Computação</span><span class="sxs-lookup"><span data-stu-id="57d72-135">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        | <span data-ttu-id="57d72-136">X</span><span class="sxs-lookup"><span data-stu-id="57d72-136">X</span></span>        |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="57d72-137">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="57d72-137">Minimum Shader Model</span></span>

<span data-ttu-id="57d72-138">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="57d72-138">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="57d72-139">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="57d72-139">Shader Model</span></span>                                              | <span data-ttu-id="57d72-140">Com suporte</span><span class="sxs-lookup"><span data-stu-id="57d72-140">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="57d72-141">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="57d72-141">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="57d72-142">sim</span><span class="sxs-lookup"><span data-stu-id="57d72-142">yes</span></span>       |
| [<span data-ttu-id="57d72-143">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="57d72-143">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="57d72-144">não</span><span class="sxs-lookup"><span data-stu-id="57d72-144">no</span></span>        |
| [<span data-ttu-id="57d72-145">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="57d72-145">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="57d72-146">não</span><span class="sxs-lookup"><span data-stu-id="57d72-146">no</span></span>        |
| [<span data-ttu-id="57d72-147">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="57d72-147">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="57d72-148">não</span><span class="sxs-lookup"><span data-stu-id="57d72-148">no</span></span>        |
| [<span data-ttu-id="57d72-149">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="57d72-149">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="57d72-150">não</span><span class="sxs-lookup"><span data-stu-id="57d72-150">no</span></span>        |
| [<span data-ttu-id="57d72-151">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="57d72-151">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="57d72-152">não</span><span class="sxs-lookup"><span data-stu-id="57d72-152">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="57d72-153">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="57d72-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="57d72-154">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="57d72-154">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





