---
title: dcl_input_control_point_count (SM5-ASM)
description: Declare a contagem de pontos de controle de entrada do sombreador envoltória na seção declaração do sombreador envoltória.
ms.assetid: 2E524BF0-3DD0-446A-8437-0CF17B348D83
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f0a674a05bfd66b4c1d94da73958dc68f00fe21
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104365295"
---
# <a name="dcl_input_control_point_count-sm5---asm"></a><span data-ttu-id="c3291-103">\_ \_ \_ \_ contagem de pontos de controle de entrada de DCL (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="c3291-103">dcl\_input\_control\_point\_count (sm5 - asm)</span></span>

<span data-ttu-id="c3291-104">Declare a contagem de pontos de controle de entrada do sombreador envoltória na seção declaração do sombreador envoltória.</span><span class="sxs-lookup"><span data-stu-id="c3291-104">Declare the hull shader input control point count in the hull shader declaration section.</span></span>



| <span data-ttu-id="c3291-105">contagem de pontos de controle de entrada de DCL \_ \_ \_ \_ {1.. 32}</span><span class="sxs-lookup"><span data-stu-id="c3291-105">dcl\_input\_control\_point\_count {1..32}</span></span> |
|-------------------------------------------|



 



| <span data-ttu-id="c3291-106">Item</span><span class="sxs-lookup"><span data-stu-id="c3291-106">Item</span></span>                                                   | <span data-ttu-id="c3291-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="c3291-107">Description</span></span>                                      |
|--------------------------------------------------------|--------------------------------------------------|
| <span data-ttu-id="c3291-108"><span id="N"></span><span id="n"></span>*P*</span><span class="sxs-lookup"><span data-stu-id="c3291-108"><span id="N"></span><span id="n"></span>*N*</span></span><br/> | <span data-ttu-id="c3291-109">\[na \] contagem de pontos de controle de entrada.</span><span class="sxs-lookup"><span data-stu-id="c3291-109">\[in\] The input control point count.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c3291-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="c3291-110">Remarks</span></span>

<span data-ttu-id="c3291-111">Pelo menos 1 ponto de controle de entrada é necessário; Ele poderá ficar vazio se não for necessário.</span><span class="sxs-lookup"><span data-stu-id="c3291-111">At least 1 input control point is required; it can be empty if it is not needed.</span></span>

<span data-ttu-id="c3291-112">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="c3291-112">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="c3291-113">Vértice</span><span class="sxs-lookup"><span data-stu-id="c3291-113">Vertex</span></span> | <span data-ttu-id="c3291-114">Envoltória</span><span class="sxs-lookup"><span data-stu-id="c3291-114">Hull</span></span> | <span data-ttu-id="c3291-115">Domínio</span><span class="sxs-lookup"><span data-stu-id="c3291-115">Domain</span></span> | <span data-ttu-id="c3291-116">Geometria</span><span class="sxs-lookup"><span data-stu-id="c3291-116">Geometry</span></span> | <span data-ttu-id="c3291-117">16x16</span><span class="sxs-lookup"><span data-stu-id="c3291-117">Pixel</span></span> | <span data-ttu-id="c3291-118">Computação</span><span class="sxs-lookup"><span data-stu-id="c3291-118">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="c3291-119">X</span><span class="sxs-lookup"><span data-stu-id="c3291-119">X</span></span>    |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="c3291-120">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="c3291-120">Minimum Shader Model</span></span>

<span data-ttu-id="c3291-121">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="c3291-121">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="c3291-122">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="c3291-122">Shader Model</span></span>                                              | <span data-ttu-id="c3291-123">Com suporte</span><span class="sxs-lookup"><span data-stu-id="c3291-123">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="c3291-124">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="c3291-124">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="c3291-125">sim</span><span class="sxs-lookup"><span data-stu-id="c3291-125">yes</span></span>       |
| [<span data-ttu-id="c3291-126">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="c3291-126">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="c3291-127">não</span><span class="sxs-lookup"><span data-stu-id="c3291-127">no</span></span>        |
| [<span data-ttu-id="c3291-128">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="c3291-128">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="c3291-129">não</span><span class="sxs-lookup"><span data-stu-id="c3291-129">no</span></span>        |
| [<span data-ttu-id="c3291-130">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c3291-130">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="c3291-131">não</span><span class="sxs-lookup"><span data-stu-id="c3291-131">no</span></span>        |
| [<span data-ttu-id="c3291-132">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c3291-132">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="c3291-133">não</span><span class="sxs-lookup"><span data-stu-id="c3291-133">no</span></span>        |
| [<span data-ttu-id="c3291-134">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c3291-134">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="c3291-135">não</span><span class="sxs-lookup"><span data-stu-id="c3291-135">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="c3291-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c3291-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c3291-137">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c3291-137">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





