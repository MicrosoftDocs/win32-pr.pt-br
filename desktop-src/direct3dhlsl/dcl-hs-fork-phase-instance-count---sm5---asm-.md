---
title: dcl_hs_fork_phase_instance_count (SM5-ASM)
description: Declare a contagem de instâncias da fase de bifurcação em uma fase de bifurcação do envoltória Shader.
ms.assetid: E38C48BB-3439-4F63-8DF8-21CF562CF5E6
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3459b43c22f60699445f3ef05e5323e268eeb71
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104365298"
---
# <a name="dcl_hs_fork_phase_instance_count-sm5---asm"></a><span data-ttu-id="6549e-103">\_contagem de \_ instâncias da fase de bifurcação do DCL HS \_ \_ \_ (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="6549e-103">dcl\_hs\_fork\_phase\_instance\_count (sm5 - asm)</span></span>

<span data-ttu-id="6549e-104">Declare a contagem de instâncias da fase de bifurcação em uma fase de bifurcação do envoltória Shader.</span><span class="sxs-lookup"><span data-stu-id="6549e-104">Declare the fork phase instance count in a hull shader fork phase.</span></span>



| <span data-ttu-id="6549e-105">\_ \_ contagem de instâncias da fase de bifurcação do DCL HS \_ \_ \_ {1... Max 32-bit uint}</span><span class="sxs-lookup"><span data-stu-id="6549e-105">dcl\_hs\_fork\_phase\_instance\_count {1...max 32-bit UINT}</span></span> |
|-------------------------------------------------------------|



 



| <span data-ttu-id="6549e-106">Item</span><span class="sxs-lookup"><span data-stu-id="6549e-106">Item</span></span>                                                   | <span data-ttu-id="6549e-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="6549e-107">Description</span></span>                           |
|--------------------------------------------------------|---------------------------------------|
| <span data-ttu-id="6549e-108"><span id="N"></span><span id="n"></span>*P*</span><span class="sxs-lookup"><span data-stu-id="6549e-108"><span id="N"></span><span id="n"></span>*N*</span></span><br/> | <span data-ttu-id="6549e-109">\[na \] contagem de instâncias.</span><span class="sxs-lookup"><span data-stu-id="6549e-109">\[in\] The instance count.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6549e-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="6549e-110">Remarks</span></span>

<span data-ttu-id="6549e-111">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="6549e-111">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="6549e-112">Vértice</span><span class="sxs-lookup"><span data-stu-id="6549e-112">Vertex</span></span> | <span data-ttu-id="6549e-113">Envoltória</span><span class="sxs-lookup"><span data-stu-id="6549e-113">Hull</span></span> | <span data-ttu-id="6549e-114">Domínio</span><span class="sxs-lookup"><span data-stu-id="6549e-114">Domain</span></span> | <span data-ttu-id="6549e-115">Geometria</span><span class="sxs-lookup"><span data-stu-id="6549e-115">Geometry</span></span> | <span data-ttu-id="6549e-116">16x16</span><span class="sxs-lookup"><span data-stu-id="6549e-116">Pixel</span></span> | <span data-ttu-id="6549e-117">Computação</span><span class="sxs-lookup"><span data-stu-id="6549e-117">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="6549e-118">X</span><span class="sxs-lookup"><span data-stu-id="6549e-118">X</span></span>    |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="6549e-119">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="6549e-119">Minimum Shader Model</span></span>

<span data-ttu-id="6549e-120">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="6549e-120">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="6549e-121">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="6549e-121">Shader Model</span></span>                                              | <span data-ttu-id="6549e-122">Com suporte</span><span class="sxs-lookup"><span data-stu-id="6549e-122">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="6549e-123">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="6549e-123">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="6549e-124">sim</span><span class="sxs-lookup"><span data-stu-id="6549e-124">yes</span></span>       |
| [<span data-ttu-id="6549e-125">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="6549e-125">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="6549e-126">não</span><span class="sxs-lookup"><span data-stu-id="6549e-126">no</span></span>        |
| [<span data-ttu-id="6549e-127">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="6549e-127">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="6549e-128">não</span><span class="sxs-lookup"><span data-stu-id="6549e-128">no</span></span>        |
| [<span data-ttu-id="6549e-129">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6549e-129">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="6549e-130">não</span><span class="sxs-lookup"><span data-stu-id="6549e-130">no</span></span>        |
| [<span data-ttu-id="6549e-131">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6549e-131">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="6549e-132">não</span><span class="sxs-lookup"><span data-stu-id="6549e-132">no</span></span>        |
| [<span data-ttu-id="6549e-133">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6549e-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="6549e-134">não</span><span class="sxs-lookup"><span data-stu-id="6549e-134">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="6549e-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6549e-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6549e-136">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6549e-136">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





