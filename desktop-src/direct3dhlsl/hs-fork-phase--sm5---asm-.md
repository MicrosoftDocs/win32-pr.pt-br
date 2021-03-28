---
title: hs_fork_phase (SM5-ASM)
description: Inicie a fase de bifurcação em um sombreador envoltória.
ms.assetid: 13D6A06C-F001-45BE-8AB4-D7ACA73BF535
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9316cc92c1bf5683afa620927b3c6f38432c3c4e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104365269"
---
# <a name="hs_fork_phase-sm5---asm"></a><span data-ttu-id="fdbdd-103">\_fase de bifurcação HS \_ (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="fdbdd-103">hs\_fork\_phase (sm5 - asm)</span></span>

<span data-ttu-id="fdbdd-104">Inicie a fase de bifurcação em um sombreador envoltória.</span><span class="sxs-lookup"><span data-stu-id="fdbdd-104">Start the fork phase in a hull shader.</span></span>



| <span data-ttu-id="fdbdd-105">\_fase de bifurcação HS \_</span><span class="sxs-lookup"><span data-stu-id="fdbdd-105">hs\_fork\_phase</span></span> |
|-----------------|



 

## <a name="remarks"></a><span data-ttu-id="fdbdd-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="fdbdd-106">Remarks</span></span>

<span data-ttu-id="fdbdd-107">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="fdbdd-107">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="fdbdd-108">Vértice</span><span class="sxs-lookup"><span data-stu-id="fdbdd-108">Vertex</span></span> | <span data-ttu-id="fdbdd-109">Envoltória</span><span class="sxs-lookup"><span data-stu-id="fdbdd-109">Hull</span></span> | <span data-ttu-id="fdbdd-110">Domínio</span><span class="sxs-lookup"><span data-stu-id="fdbdd-110">Domain</span></span> | <span data-ttu-id="fdbdd-111">Geometria</span><span class="sxs-lookup"><span data-stu-id="fdbdd-111">Geometry</span></span> | <span data-ttu-id="fdbdd-112">16x16</span><span class="sxs-lookup"><span data-stu-id="fdbdd-112">Pixel</span></span> | <span data-ttu-id="fdbdd-113">Computação</span><span class="sxs-lookup"><span data-stu-id="fdbdd-113">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="fdbdd-114">X</span><span class="sxs-lookup"><span data-stu-id="fdbdd-114">X</span></span>    |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="fdbdd-115">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="fdbdd-115">Minimum Shader Model</span></span>

<span data-ttu-id="fdbdd-116">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="fdbdd-116">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="fdbdd-117">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="fdbdd-117">Shader Model</span></span>                                              | <span data-ttu-id="fdbdd-118">Com suporte</span><span class="sxs-lookup"><span data-stu-id="fdbdd-118">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="fdbdd-119">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="fdbdd-119">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="fdbdd-120">sim</span><span class="sxs-lookup"><span data-stu-id="fdbdd-120">yes</span></span>       |
| [<span data-ttu-id="fdbdd-121">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="fdbdd-121">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="fdbdd-122">não</span><span class="sxs-lookup"><span data-stu-id="fdbdd-122">no</span></span>        |
| [<span data-ttu-id="fdbdd-123">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="fdbdd-123">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="fdbdd-124">não</span><span class="sxs-lookup"><span data-stu-id="fdbdd-124">no</span></span>        |
| [<span data-ttu-id="fdbdd-125">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fdbdd-125">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="fdbdd-126">não</span><span class="sxs-lookup"><span data-stu-id="fdbdd-126">no</span></span>        |
| [<span data-ttu-id="fdbdd-127">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fdbdd-127">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="fdbdd-128">não</span><span class="sxs-lookup"><span data-stu-id="fdbdd-128">no</span></span>        |
| [<span data-ttu-id="fdbdd-129">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fdbdd-129">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="fdbdd-130">não</span><span class="sxs-lookup"><span data-stu-id="fdbdd-130">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="fdbdd-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fdbdd-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fdbdd-132">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fdbdd-132">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 




