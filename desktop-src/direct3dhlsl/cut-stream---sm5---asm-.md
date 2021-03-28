---
title: cut_stream (SM5-ASM)
description: A instrução Geometry Shader que conclui a topologia primitiva atual no fluxo especificado, se quaisquer vértices tiverem sido emitidos para ele e iniciar uma nova topologia do tipo declarado pelo sombreador Geometry nesse fluxo.
ms.assetid: CEFDD13B-34FD-4E9C-94A0-CB8879A7DBDE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4650628d7f6b66130568f885e008a5163a9ee44f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104365201"
---
# <a name="cut_stream-sm5---asm"></a><span data-ttu-id="0816a-103">Recortar \_ fluxo (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="0816a-103">cut\_stream (sm5 - asm)</span></span>

<span data-ttu-id="0816a-104">A instrução Geometry Shader que conclui a topologia primitiva atual no fluxo especificado, se quaisquer vértices tiverem sido emitidos para ele e iniciar uma nova topologia do tipo declarado pelo sombreador Geometry nesse fluxo.</span><span class="sxs-lookup"><span data-stu-id="0816a-104">The geometry shader instruction that completes the current primitive topology at the specified stream, if any vertices have been emitted to it, and starts a new topology of the type declared by the geometry shader at that stream.</span></span>



| <span data-ttu-id="0816a-105">Recortar \_ fluxo streamIndex</span><span class="sxs-lookup"><span data-stu-id="0816a-105">cut\_stream streamIndex</span></span> |
|-------------------------|



 



| <span data-ttu-id="0816a-106">Item</span><span class="sxs-lookup"><span data-stu-id="0816a-106">Item</span></span>                                                                                                               | <span data-ttu-id="0816a-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="0816a-107">Description</span></span>                         |
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| <span data-ttu-id="0816a-108"><span id="streamIndex"></span><span id="streamindex"></span><span id="STREAMINDEX"></span>*streamIndex*</span><span class="sxs-lookup"><span data-stu-id="0816a-108"><span id="streamIndex"></span><span id="streamindex"></span><span id="STREAMINDEX"></span>*streamIndex*</span></span><br/> | <span data-ttu-id="0816a-109">\[no \] índice de fluxo.</span><span class="sxs-lookup"><span data-stu-id="0816a-109">\[in\] The stream index.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0816a-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="0816a-110">Remarks</span></span>

<span data-ttu-id="0816a-111">Quando essa instrução é executada, qualquer topologia emitida anteriormente pela invocação do sombreador de geometria é concluída.</span><span class="sxs-lookup"><span data-stu-id="0816a-111">When this instruction is executed, any previously emitted topology by the geometry shader invocation is completed.</span></span> <span data-ttu-id="0816a-112">Se não houver vértices suficientes emitidos para a topologia primitiva anterior, eles serão descartados.</span><span class="sxs-lookup"><span data-stu-id="0816a-112">If there are not enough vertices emitted for the previous primitive topology, then they are discarded.</span></span> <span data-ttu-id="0816a-113">Como as únicas topologias de saída disponíveis para o sombreador Geometry são PointList, linestrip e Trianglestrip, nunca há vértices sobrantes.</span><span class="sxs-lookup"><span data-stu-id="0816a-113">Because the only available output topologies for the geometry shader are pointlist, linestrip and trianglestrip, there are never any leftover vertices.</span></span>

<span data-ttu-id="0816a-114">*streamIndex* deve ser um valor imediato \[ 0.. 3 \] para um fluxo declarado.</span><span class="sxs-lookup"><span data-stu-id="0816a-114">*streamIndex* must be an immediate value \[0..3\] for a declared stream.</span></span>

<span data-ttu-id="0816a-115">Depois que a topologia anterior, se houver, for concluída, essa instrução fará com que uma nova topologia comece, usando a topologia declarada como a saída do sombreador de geometria.</span><span class="sxs-lookup"><span data-stu-id="0816a-115">After the previous topology, if any, is completed, this instruction causes a new topology to begin, using the topology declared as the output for the geometry shader.</span></span>

### <a name="restrictions"></a><span data-ttu-id="0816a-116">Restrições</span><span class="sxs-lookup"><span data-stu-id="0816a-116">Restrictions</span></span>

-   <span data-ttu-id="0816a-117">Essa instrução aplica-se somente ao sombreador Geometry.</span><span class="sxs-lookup"><span data-stu-id="0816a-117">This instruction applies to the geometry shader only.</span></span>
-   <span data-ttu-id="0816a-118">**recortar \_ fluxo** pode aparecer qualquer número de vezes no sombreador Geometry, incluindo dentro do controle de fluxo.</span><span class="sxs-lookup"><span data-stu-id="0816a-118">**cut\_stream** can appear any number of times in the geometry shader, including within flow control.</span></span>
-   <span data-ttu-id="0816a-119">Se o sombreador de geometria terminar e os vértices tiverem sido emitidos, a topologia que ele está compilando será concluída, como se uma instrução **Cut \_ Stream** fosse executada como a última instrução.</span><span class="sxs-lookup"><span data-stu-id="0816a-119">If the geometry shader ends and vertices have been emitted, the topology they are building is completed, as if a **cut\_stream** instruction was executed as the last instruction.</span></span>
-   <span data-ttu-id="0816a-120">Se os fluxos não tiverem sido declarados, você deverá usar [recortar](cut--sm4---asm-.md) em vez de **recortar \_ fluxo**.</span><span class="sxs-lookup"><span data-stu-id="0816a-120">If streams have not been declared, you must use [cut](cut--sm4---asm-.md) instead of **cut\_stream**.</span></span>

<span data-ttu-id="0816a-121">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="0816a-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="0816a-122">Vértice</span><span class="sxs-lookup"><span data-stu-id="0816a-122">Vertex</span></span> | <span data-ttu-id="0816a-123">Envoltória</span><span class="sxs-lookup"><span data-stu-id="0816a-123">Hull</span></span> | <span data-ttu-id="0816a-124">Domínio</span><span class="sxs-lookup"><span data-stu-id="0816a-124">Domain</span></span> | <span data-ttu-id="0816a-125">Geometria</span><span class="sxs-lookup"><span data-stu-id="0816a-125">Geometry</span></span> | <span data-ttu-id="0816a-126">16x16</span><span class="sxs-lookup"><span data-stu-id="0816a-126">Pixel</span></span> | <span data-ttu-id="0816a-127">Computação</span><span class="sxs-lookup"><span data-stu-id="0816a-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        | <span data-ttu-id="0816a-128">X</span><span class="sxs-lookup"><span data-stu-id="0816a-128">X</span></span>        |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="0816a-129">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="0816a-129">Minimum Shader Model</span></span>

<span data-ttu-id="0816a-130">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="0816a-130">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="0816a-131">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="0816a-131">Shader Model</span></span>                                              | <span data-ttu-id="0816a-132">Com suporte</span><span class="sxs-lookup"><span data-stu-id="0816a-132">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="0816a-133">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="0816a-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="0816a-134">sim</span><span class="sxs-lookup"><span data-stu-id="0816a-134">yes</span></span>       |
| [<span data-ttu-id="0816a-135">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="0816a-135">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="0816a-136">não</span><span class="sxs-lookup"><span data-stu-id="0816a-136">no</span></span>        |
| [<span data-ttu-id="0816a-137">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="0816a-137">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="0816a-138">não</span><span class="sxs-lookup"><span data-stu-id="0816a-138">no</span></span>        |
| [<span data-ttu-id="0816a-139">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0816a-139">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="0816a-140">não</span><span class="sxs-lookup"><span data-stu-id="0816a-140">no</span></span>        |
| [<span data-ttu-id="0816a-141">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0816a-141">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="0816a-142">não</span><span class="sxs-lookup"><span data-stu-id="0816a-142">no</span></span>        |
| [<span data-ttu-id="0816a-143">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0816a-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="0816a-144">não</span><span class="sxs-lookup"><span data-stu-id="0816a-144">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="0816a-145">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0816a-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0816a-146">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0816a-146">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





