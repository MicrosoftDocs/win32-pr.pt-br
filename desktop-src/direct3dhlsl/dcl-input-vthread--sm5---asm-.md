---
title: dcl_input vThread (SM5-ASM)
description: Declare as IDs de entrada do sombreador de computação.
ms.assetid: C041863A-32B0-4588-A1A9-E416AF9B723C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbf6a7bb19feef95eae9cc153911407b206fde16
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103638896"
---
# <a name="dcl_input-vthread-sm5---asm"></a><span data-ttu-id="bcded-103">\_vThread de entrada DCL (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="bcded-103">dcl\_input vThread (sm5 - asm)</span></span>

<span data-ttu-id="bcded-104">Declare as IDs de entrada do sombreador de computação.</span><span class="sxs-lookup"><span data-stu-id="bcded-104">Declare compute shader input IDs.</span></span>



| <span data-ttu-id="bcded-105">\_entrada DCL {vThreadID.xyz </span><span class="sxs-lookup"><span data-stu-id="bcded-105">dcl\_input {vThreadID.xyz</span></span>\|<span data-ttu-id="bcded-106">vThreadGroupID.xyz </span><span class="sxs-lookup"><span data-stu-id="bcded-106">vThreadGroupID.xyz</span></span>\| <span data-ttu-id="bcded-107">vThreadIDInGroup.xyz </span><span class="sxs-lookup"><span data-stu-id="bcded-107">vThreadIDInGroup.xyz</span></span>\|<span data-ttu-id="bcded-108">vThreadIDInGroupFlattened}</span><span class="sxs-lookup"><span data-stu-id="bcded-108">vThreadIDInGroupFlattened}</span></span> |
|--------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="bcded-109">Item</span><span class="sxs-lookup"><span data-stu-id="bcded-109">Item</span></span>                                                                                                                                                                                                                                                                                                                                                                          | <span data-ttu-id="bcded-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="bcded-110">Description</span></span>                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="bcded-111"><span id="vThreadID___vThreadGroupID___vThreadIDInGroup___vThreadIDInGroupFlattened"></span><span id="vthreadid___vthreadgroupid___vthreadidingroup___vthreadidingroupflattened"></span><span id="VTHREADID___VTHREADGROUPID___VTHREADIDINGROUP___VTHREADIDINGROUPFLATTENED"></span>*vThreadID \| vThreadGroupID \| vThreadIDInGroup \| vThreadIDInGroupFlattened*</span><span class="sxs-lookup"><span data-stu-id="bcded-111"><span id="vThreadID___vThreadGroupID___vThreadIDInGroup___vThreadIDInGroupFlattened"></span><span id="vthreadid___vthreadgroupid___vthreadidingroup___vthreadidingroupflattened"></span><span id="VTHREADID___VTHREADGROUPID___VTHREADIDINGROUP___VTHREADIDINGROUPFLATTENED"></span>*vThreadID \| vThreadGroupID \| vThreadIDInGroup \| vThreadIDInGroupFlattened*</span></span><br/> | <span data-ttu-id="bcded-112">\[no \] valor de ID de inteiro de 32 bits sem sinal de 3 componentes.</span><span class="sxs-lookup"><span data-stu-id="bcded-112">\[in\] The 3-component unsigned 32-bit integer ID value.</span></span><br/> |



 

<span data-ttu-id="bcded-113">**a \_ entrada DCL** é uma declaração existente em outros estágios de sombreador.</span><span class="sxs-lookup"><span data-stu-id="bcded-113">**dcl\_input** is an existing declaration in other shader stages.</span></span> <span data-ttu-id="bcded-114">Ele é usado no sombreador de computação para declarar os vários valores de ID de inteiro de 32 bits não assinados de 3 componentes exclusivos do sombreador de computação.</span><span class="sxs-lookup"><span data-stu-id="bcded-114">It is used in the compute shader to declare the various 3-component unsigned 32-bit integer ID values unique to the compute shader.</span></span> <span data-ttu-id="bcded-115">Eles são:</span><span class="sxs-lookup"><span data-stu-id="bcded-115">They are:</span></span>

-   <span data-ttu-id="bcded-116">vThreadID.xyz</span><span class="sxs-lookup"><span data-stu-id="bcded-116">vThreadID.xyz</span></span>
-   <span data-ttu-id="bcded-117">vGroupID.xyz</span><span class="sxs-lookup"><span data-stu-id="bcded-117">vGroupID.xyz</span></span>
-   <span data-ttu-id="bcded-118">vThreadIDInGroup.xyz</span><span class="sxs-lookup"><span data-stu-id="bcded-118">vThreadIDInGroup.xyz</span></span>
-   <span data-ttu-id="bcded-119">vThreadIDInGroupFlattened (componente único)</span><span class="sxs-lookup"><span data-stu-id="bcded-119">vThreadIDInGroupFlattened (single component)</span></span>

<span data-ttu-id="bcded-120">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="bcded-120">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="bcded-121">Vértice</span><span class="sxs-lookup"><span data-stu-id="bcded-121">Vertex</span></span> | <span data-ttu-id="bcded-122">Envoltória</span><span class="sxs-lookup"><span data-stu-id="bcded-122">Hull</span></span> | <span data-ttu-id="bcded-123">Domínio</span><span class="sxs-lookup"><span data-stu-id="bcded-123">Domain</span></span> | <span data-ttu-id="bcded-124">Geometria</span><span class="sxs-lookup"><span data-stu-id="bcded-124">Geometry</span></span> | <span data-ttu-id="bcded-125">16x16</span><span class="sxs-lookup"><span data-stu-id="bcded-125">Pixel</span></span> | <span data-ttu-id="bcded-126">Computação</span><span class="sxs-lookup"><span data-stu-id="bcded-126">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="bcded-127">X</span><span class="sxs-lookup"><span data-stu-id="bcded-127">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="bcded-128">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="bcded-128">Minimum Shader Model</span></span>

<span data-ttu-id="bcded-129">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="bcded-129">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="bcded-130">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="bcded-130">Shader Model</span></span>                                              | <span data-ttu-id="bcded-131">Com suporte</span><span class="sxs-lookup"><span data-stu-id="bcded-131">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="bcded-132">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="bcded-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="bcded-133">sim</span><span class="sxs-lookup"><span data-stu-id="bcded-133">yes</span></span>       |
| [<span data-ttu-id="bcded-134">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="bcded-134">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="bcded-135">não</span><span class="sxs-lookup"><span data-stu-id="bcded-135">no</span></span>        |
| [<span data-ttu-id="bcded-136">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="bcded-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="bcded-137">não</span><span class="sxs-lookup"><span data-stu-id="bcded-137">no</span></span>        |
| [<span data-ttu-id="bcded-138">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bcded-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="bcded-139">não</span><span class="sxs-lookup"><span data-stu-id="bcded-139">no</span></span>        |
| [<span data-ttu-id="bcded-140">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bcded-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="bcded-141">não</span><span class="sxs-lookup"><span data-stu-id="bcded-141">no</span></span>        |
| [<span data-ttu-id="bcded-142">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bcded-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="bcded-143">não</span><span class="sxs-lookup"><span data-stu-id="bcded-143">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="bcded-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bcded-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bcded-145">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bcded-145">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





