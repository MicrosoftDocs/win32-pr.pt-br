---
title: dcl_input vOutputControlPointID (SM5-ASM)
description: Declare a ID do ponto de controle de saída em uma fase do ponto de controle do sombreador envoltória.
ms.assetid: 376ECA4F-DD71-4466-8A9D-E92A536832BC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9cee49a8a825f25b0fbbccff027d5ad1b9ade514
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104006930"
---
# <a name="dcl_input-voutputcontrolpointid-sm5---asm"></a><span data-ttu-id="5abdd-103">\_vOutputControlPointID de entrada DCL (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="5abdd-103">dcl\_input vOutputControlPointID (sm5 - asm)</span></span>

<span data-ttu-id="5abdd-104">Declare a ID do ponto de controle de saída em uma fase do ponto de controle do sombreador envoltória.</span><span class="sxs-lookup"><span data-stu-id="5abdd-104">Declare the output control point ID in a hull shader control point phase.</span></span>



| <span data-ttu-id="5abdd-105">\_vOutputControlPointID de entrada DCL</span><span class="sxs-lookup"><span data-stu-id="5abdd-105">dcl\_input vOutputControlPointID</span></span> |
|----------------------------------|



 



| <span data-ttu-id="5abdd-106">Item</span><span class="sxs-lookup"><span data-stu-id="5abdd-106">Item</span></span>                                                                                                                                                       | <span data-ttu-id="5abdd-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="5abdd-107">Description</span></span>                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span data-ttu-id="5abdd-108"><span id="vOutputControlPointID"></span><span id="voutputcontrolpointid"></span><span id="VOUTPUTCONTROLPOINTID"></span>*vOutputControlPointID*</span><span class="sxs-lookup"><span data-stu-id="5abdd-108"><span id="vOutputControlPointID"></span><span id="voutputcontrolpointid"></span><span id="VOUTPUTCONTROLPOINTID"></span>*vOutputControlPointID*</span></span><br/> | <span data-ttu-id="5abdd-109">\[na \] ID do ponto de controle de saída.</span><span class="sxs-lookup"><span data-stu-id="5abdd-109">\[in\] The output control point ID.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5abdd-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="5abdd-110">Remarks</span></span>

<span data-ttu-id="5abdd-111">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="5abdd-111">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="5abdd-112">Vértice</span><span class="sxs-lookup"><span data-stu-id="5abdd-112">Vertex</span></span> | <span data-ttu-id="5abdd-113">Envoltória</span><span class="sxs-lookup"><span data-stu-id="5abdd-113">Hull</span></span> | <span data-ttu-id="5abdd-114">Domínio</span><span class="sxs-lookup"><span data-stu-id="5abdd-114">Domain</span></span> | <span data-ttu-id="5abdd-115">Geometria</span><span class="sxs-lookup"><span data-stu-id="5abdd-115">Geometry</span></span> | <span data-ttu-id="5abdd-116">16x16</span><span class="sxs-lookup"><span data-stu-id="5abdd-116">Pixel</span></span> | <span data-ttu-id="5abdd-117">Computação</span><span class="sxs-lookup"><span data-stu-id="5abdd-117">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="5abdd-118">X</span><span class="sxs-lookup"><span data-stu-id="5abdd-118">X</span></span>    |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="5abdd-119">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="5abdd-119">Minimum Shader Model</span></span>

<span data-ttu-id="5abdd-120">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="5abdd-120">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="5abdd-121">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="5abdd-121">Shader Model</span></span>                                              | <span data-ttu-id="5abdd-122">Com suporte</span><span class="sxs-lookup"><span data-stu-id="5abdd-122">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="5abdd-123">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="5abdd-123">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="5abdd-124">sim</span><span class="sxs-lookup"><span data-stu-id="5abdd-124">yes</span></span>       |
| [<span data-ttu-id="5abdd-125">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="5abdd-125">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="5abdd-126">não</span><span class="sxs-lookup"><span data-stu-id="5abdd-126">no</span></span>        |
| [<span data-ttu-id="5abdd-127">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="5abdd-127">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="5abdd-128">não</span><span class="sxs-lookup"><span data-stu-id="5abdd-128">no</span></span>        |
| [<span data-ttu-id="5abdd-129">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5abdd-129">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="5abdd-130">não</span><span class="sxs-lookup"><span data-stu-id="5abdd-130">no</span></span>        |
| [<span data-ttu-id="5abdd-131">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5abdd-131">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="5abdd-132">não</span><span class="sxs-lookup"><span data-stu-id="5abdd-132">no</span></span>        |
| [<span data-ttu-id="5abdd-133">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5abdd-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="5abdd-134">não</span><span class="sxs-lookup"><span data-stu-id="5abdd-134">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="5abdd-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5abdd-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5abdd-136">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5abdd-136">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





