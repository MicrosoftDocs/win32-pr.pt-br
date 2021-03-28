---
title: dcl_input vForkInstanceID (SM5-ASM)
description: Declare a ID da instância em uma fase de bifurcação do sombreador envoltória.
ms.assetid: AA73E8B6-C6D7-4483-B46E-C733341F552C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20ce5fcf111a59abb0c9a6ccb36de63d94dcb11e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104006931"
---
# <a name="dcl_input-vforkinstanceid-sm5---asm"></a><span data-ttu-id="6f52f-103">\_vForkInstanceID de entrada DCL (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="6f52f-103">dcl\_input vForkInstanceID (sm5 - asm)</span></span>

<span data-ttu-id="6f52f-104">Declare a ID da instância em uma fase de bifurcação do sombreador envoltória.</span><span class="sxs-lookup"><span data-stu-id="6f52f-104">Declare the instance ID in a hull shader fork phase.</span></span>



| <span data-ttu-id="6f52f-105">\_vForkInstanceID de entrada DCL</span><span class="sxs-lookup"><span data-stu-id="6f52f-105">dcl\_input vForkInstanceID</span></span> |
|----------------------------|



 



| <span data-ttu-id="6f52f-106">Item</span><span class="sxs-lookup"><span data-stu-id="6f52f-106">Item</span></span>                                                                                                                               | <span data-ttu-id="6f52f-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="6f52f-107">Description</span></span>                        |
|------------------------------------------------------------------------------------------------------------------------------------|------------------------------------|
| <span data-ttu-id="6f52f-108"><span id="vForkInstanceID"></span><span id="vforkinstanceid"></span><span id="VFORKINSTANCEID"></span>*vForkInstanceID*</span><span class="sxs-lookup"><span data-stu-id="6f52f-108"><span id="vForkInstanceID"></span><span id="vforkinstanceid"></span><span id="VFORKINSTANCEID"></span>*vForkInstanceID*</span></span><br/> | <span data-ttu-id="6f52f-109">\[na \] ID da instância.</span><span class="sxs-lookup"><span data-stu-id="6f52f-109">\[in\] The instance ID.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6f52f-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="6f52f-110">Remarks</span></span>

<span data-ttu-id="6f52f-111">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="6f52f-111">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="6f52f-112">Vértice</span><span class="sxs-lookup"><span data-stu-id="6f52f-112">Vertex</span></span> | <span data-ttu-id="6f52f-113">Envoltória</span><span class="sxs-lookup"><span data-stu-id="6f52f-113">Hull</span></span> | <span data-ttu-id="6f52f-114">Domínio</span><span class="sxs-lookup"><span data-stu-id="6f52f-114">Domain</span></span> | <span data-ttu-id="6f52f-115">Geometria</span><span class="sxs-lookup"><span data-stu-id="6f52f-115">Geometry</span></span> | <span data-ttu-id="6f52f-116">16x16</span><span class="sxs-lookup"><span data-stu-id="6f52f-116">Pixel</span></span> | <span data-ttu-id="6f52f-117">Computação</span><span class="sxs-lookup"><span data-stu-id="6f52f-117">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="6f52f-118">X</span><span class="sxs-lookup"><span data-stu-id="6f52f-118">X</span></span>    |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="6f52f-119">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="6f52f-119">Minimum Shader Model</span></span>

<span data-ttu-id="6f52f-120">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="6f52f-120">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="6f52f-121">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="6f52f-121">Shader Model</span></span>                                              | <span data-ttu-id="6f52f-122">Com suporte</span><span class="sxs-lookup"><span data-stu-id="6f52f-122">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="6f52f-123">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="6f52f-123">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="6f52f-124">sim</span><span class="sxs-lookup"><span data-stu-id="6f52f-124">yes</span></span>       |
| [<span data-ttu-id="6f52f-125">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="6f52f-125">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="6f52f-126">não</span><span class="sxs-lookup"><span data-stu-id="6f52f-126">no</span></span>        |
| [<span data-ttu-id="6f52f-127">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="6f52f-127">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="6f52f-128">não</span><span class="sxs-lookup"><span data-stu-id="6f52f-128">no</span></span>        |
| [<span data-ttu-id="6f52f-129">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6f52f-129">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="6f52f-130">não</span><span class="sxs-lookup"><span data-stu-id="6f52f-130">no</span></span>        |
| [<span data-ttu-id="6f52f-131">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6f52f-131">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="6f52f-132">não</span><span class="sxs-lookup"><span data-stu-id="6f52f-132">no</span></span>        |
| [<span data-ttu-id="6f52f-133">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6f52f-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="6f52f-134">não</span><span class="sxs-lookup"><span data-stu-id="6f52f-134">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="6f52f-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6f52f-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6f52f-136">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6f52f-136">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





