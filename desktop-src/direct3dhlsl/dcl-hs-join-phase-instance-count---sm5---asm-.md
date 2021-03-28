---
title: dcl_hs_join_phase_instance_count (SM5-ASM)
description: Declare a contagem de instâncias da fase de junção em uma fase de junção do sombreador envoltória.
ms.assetid: 9951B849-0537-4D08-9ADE-8CF6FF51A193
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34c3acc7074170ab4561a54e67668698d58b7ac1
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104365299"
---
# <a name="dcl_hs_join_phase_instance_count-sm5---asm"></a><span data-ttu-id="d4b50-103">\_contagem de \_ instâncias da \_ fase de junção do DCL HS \_ \_ (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="d4b50-103">dcl\_hs\_join\_phase\_instance\_count (sm5 - asm)</span></span>

<span data-ttu-id="d4b50-104">Declare a contagem de instâncias da fase de junção em uma fase de junção do sombreador envoltória.</span><span class="sxs-lookup"><span data-stu-id="d4b50-104">Declare the join phase instance count in a hull shader join phase.</span></span>



| <span data-ttu-id="d4b50-105">\_ \_ contagem de instâncias da fase de junção do DCL HS \_ \_ \_ {1... Max 32-bit uint}</span><span class="sxs-lookup"><span data-stu-id="d4b50-105">dcl\_hs\_join\_phase\_instance\_count {1... max 32-bit UINT}</span></span> |
|--------------------------------------------------------------|



 



| <span data-ttu-id="d4b50-106">Item</span><span class="sxs-lookup"><span data-stu-id="d4b50-106">Item</span></span>                                                   | <span data-ttu-id="d4b50-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="d4b50-107">Description</span></span>                           |
|--------------------------------------------------------|---------------------------------------|
| <span data-ttu-id="d4b50-108"><span id="N"></span><span id="n"></span>*P*</span><span class="sxs-lookup"><span data-stu-id="d4b50-108"><span id="N"></span><span id="n"></span>*N*</span></span><br/> | <span data-ttu-id="d4b50-109">\[na \] contagem de instâncias.</span><span class="sxs-lookup"><span data-stu-id="d4b50-109">\[in\] The instance count.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d4b50-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="d4b50-110">Remarks</span></span>

<span data-ttu-id="d4b50-111">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="d4b50-111">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="d4b50-112">Vértice</span><span class="sxs-lookup"><span data-stu-id="d4b50-112">Vertex</span></span> | <span data-ttu-id="d4b50-113">Envoltória</span><span class="sxs-lookup"><span data-stu-id="d4b50-113">Hull</span></span> | <span data-ttu-id="d4b50-114">Domínio</span><span class="sxs-lookup"><span data-stu-id="d4b50-114">Domain</span></span> | <span data-ttu-id="d4b50-115">Geometria</span><span class="sxs-lookup"><span data-stu-id="d4b50-115">Geometry</span></span> | <span data-ttu-id="d4b50-116">16x16</span><span class="sxs-lookup"><span data-stu-id="d4b50-116">Pixel</span></span> | <span data-ttu-id="d4b50-117">Computação</span><span class="sxs-lookup"><span data-stu-id="d4b50-117">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="d4b50-118">X</span><span class="sxs-lookup"><span data-stu-id="d4b50-118">X</span></span>    |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d4b50-119">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="d4b50-119">Minimum Shader Model</span></span>

<span data-ttu-id="d4b50-120">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="d4b50-120">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="d4b50-121">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="d4b50-121">Shader Model</span></span>                                              | <span data-ttu-id="d4b50-122">Com suporte</span><span class="sxs-lookup"><span data-stu-id="d4b50-122">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="d4b50-123">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="d4b50-123">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="d4b50-124">sim</span><span class="sxs-lookup"><span data-stu-id="d4b50-124">yes</span></span>       |
| [<span data-ttu-id="d4b50-125">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="d4b50-125">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="d4b50-126">não</span><span class="sxs-lookup"><span data-stu-id="d4b50-126">no</span></span>        |
| [<span data-ttu-id="d4b50-127">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="d4b50-127">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="d4b50-128">não</span><span class="sxs-lookup"><span data-stu-id="d4b50-128">no</span></span>        |
| [<span data-ttu-id="d4b50-129">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d4b50-129">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="d4b50-130">não</span><span class="sxs-lookup"><span data-stu-id="d4b50-130">no</span></span>        |
| [<span data-ttu-id="d4b50-131">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d4b50-131">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="d4b50-132">não</span><span class="sxs-lookup"><span data-stu-id="d4b50-132">no</span></span>        |
| [<span data-ttu-id="d4b50-133">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d4b50-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="d4b50-134">não</span><span class="sxs-lookup"><span data-stu-id="d4b50-134">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="d4b50-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d4b50-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d4b50-136">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d4b50-136">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





