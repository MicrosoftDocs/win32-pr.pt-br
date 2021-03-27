---
title: hs_join_phase (SM5-ASM)
description: Inicie a fase de junção em um sombreador envoltória.
ms.assetid: C53889BE-B65F-4F5F-8B87-7C5263FAC800
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54c45011209124d73fe866872772a3a787c538d2
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104293583"
---
# <a name="hs_join_phase-sm5---asm"></a><span data-ttu-id="ec5eb-103">\_ \_ fase de junção HS (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="ec5eb-103">hs\_join\_phase (sm5 - asm)</span></span>

<span data-ttu-id="ec5eb-104">Inicie a fase de junção em um sombreador envoltória.</span><span class="sxs-lookup"><span data-stu-id="ec5eb-104">Start the join phase in a hull shader.</span></span>



| <span data-ttu-id="ec5eb-105">\_fase de junção HS \_</span><span class="sxs-lookup"><span data-stu-id="ec5eb-105">hs\_join\_phase</span></span> |
|-----------------|



 

## <a name="remarks"></a><span data-ttu-id="ec5eb-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="ec5eb-106">Remarks</span></span>

<span data-ttu-id="ec5eb-107">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="ec5eb-107">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="ec5eb-108">Vértice</span><span class="sxs-lookup"><span data-stu-id="ec5eb-108">Vertex</span></span> | <span data-ttu-id="ec5eb-109">Envoltória</span><span class="sxs-lookup"><span data-stu-id="ec5eb-109">Hull</span></span> | <span data-ttu-id="ec5eb-110">Domínio</span><span class="sxs-lookup"><span data-stu-id="ec5eb-110">Domain</span></span> | <span data-ttu-id="ec5eb-111">Geometria</span><span class="sxs-lookup"><span data-stu-id="ec5eb-111">Geometry</span></span> | <span data-ttu-id="ec5eb-112">16x16</span><span class="sxs-lookup"><span data-stu-id="ec5eb-112">Pixel</span></span> | <span data-ttu-id="ec5eb-113">Computação</span><span class="sxs-lookup"><span data-stu-id="ec5eb-113">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="ec5eb-114">X</span><span class="sxs-lookup"><span data-stu-id="ec5eb-114">X</span></span>    |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="ec5eb-115">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="ec5eb-115">Minimum Shader Model</span></span>

<span data-ttu-id="ec5eb-116">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="ec5eb-116">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="ec5eb-117">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="ec5eb-117">Shader Model</span></span>                                              | <span data-ttu-id="ec5eb-118">Com suporte</span><span class="sxs-lookup"><span data-stu-id="ec5eb-118">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="ec5eb-119">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="ec5eb-119">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="ec5eb-120">sim</span><span class="sxs-lookup"><span data-stu-id="ec5eb-120">yes</span></span>       |
| [<span data-ttu-id="ec5eb-121">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="ec5eb-121">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="ec5eb-122">não</span><span class="sxs-lookup"><span data-stu-id="ec5eb-122">no</span></span>        |
| [<span data-ttu-id="ec5eb-123">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="ec5eb-123">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="ec5eb-124">não</span><span class="sxs-lookup"><span data-stu-id="ec5eb-124">no</span></span>        |
| [<span data-ttu-id="ec5eb-125">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ec5eb-125">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="ec5eb-126">não</span><span class="sxs-lookup"><span data-stu-id="ec5eb-126">no</span></span>        |
| [<span data-ttu-id="ec5eb-127">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ec5eb-127">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="ec5eb-128">não</span><span class="sxs-lookup"><span data-stu-id="ec5eb-128">no</span></span>        |
| [<span data-ttu-id="ec5eb-129">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ec5eb-129">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="ec5eb-130">não</span><span class="sxs-lookup"><span data-stu-id="ec5eb-130">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="ec5eb-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ec5eb-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ec5eb-132">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ec5eb-132">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 




