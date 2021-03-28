---
title: hs_control_point_phase (SM5-ASM)
description: Inicie a fase de ponto de controle em um sombreador envoltória.
ms.assetid: 9CF26691-C04F-4728-8418-40F313ABBE4A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aba3f591fcd656e64609513dca7b9126496a86d6
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104006912"
---
# <a name="hs_control_point_phase-sm5---asm"></a><span data-ttu-id="2a2f1-103">\_ \_ fase de ponto de controle HS \_ (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="2a2f1-103">hs\_control\_point\_phase (sm5 - asm)</span></span>

<span data-ttu-id="2a2f1-104">Inicie a fase de ponto de controle em um sombreador envoltória.</span><span class="sxs-lookup"><span data-stu-id="2a2f1-104">Start the control point phase in a hull shader.</span></span>



| <span data-ttu-id="2a2f1-105">\_fase de \_ ponto de controle HS \_</span><span class="sxs-lookup"><span data-stu-id="2a2f1-105">hs\_control\_point\_phase</span></span> |
|---------------------------|



 

## <a name="remarks"></a><span data-ttu-id="2a2f1-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="2a2f1-106">Remarks</span></span>

<span data-ttu-id="2a2f1-107">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="2a2f1-107">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="2a2f1-108">Vértice</span><span class="sxs-lookup"><span data-stu-id="2a2f1-108">Vertex</span></span> | <span data-ttu-id="2a2f1-109">Envoltória</span><span class="sxs-lookup"><span data-stu-id="2a2f1-109">Hull</span></span> | <span data-ttu-id="2a2f1-110">Domínio</span><span class="sxs-lookup"><span data-stu-id="2a2f1-110">Domain</span></span> | <span data-ttu-id="2a2f1-111">Geometria</span><span class="sxs-lookup"><span data-stu-id="2a2f1-111">Geometry</span></span> | <span data-ttu-id="2a2f1-112">16x16</span><span class="sxs-lookup"><span data-stu-id="2a2f1-112">Pixel</span></span> | <span data-ttu-id="2a2f1-113">Computação</span><span class="sxs-lookup"><span data-stu-id="2a2f1-113">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="2a2f1-114">X</span><span class="sxs-lookup"><span data-stu-id="2a2f1-114">X</span></span>    |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="2a2f1-115">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="2a2f1-115">Minimum Shader Model</span></span>

<span data-ttu-id="2a2f1-116">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="2a2f1-116">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="2a2f1-117">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="2a2f1-117">Shader Model</span></span>                                              | <span data-ttu-id="2a2f1-118">Com suporte</span><span class="sxs-lookup"><span data-stu-id="2a2f1-118">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="2a2f1-119">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="2a2f1-119">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="2a2f1-120">sim</span><span class="sxs-lookup"><span data-stu-id="2a2f1-120">yes</span></span>       |
| [<span data-ttu-id="2a2f1-121">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="2a2f1-121">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="2a2f1-122">não</span><span class="sxs-lookup"><span data-stu-id="2a2f1-122">no</span></span>        |
| [<span data-ttu-id="2a2f1-123">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="2a2f1-123">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="2a2f1-124">não</span><span class="sxs-lookup"><span data-stu-id="2a2f1-124">no</span></span>        |
| [<span data-ttu-id="2a2f1-125">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2a2f1-125">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="2a2f1-126">não</span><span class="sxs-lookup"><span data-stu-id="2a2f1-126">no</span></span>        |
| [<span data-ttu-id="2a2f1-127">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2a2f1-127">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="2a2f1-128">não</span><span class="sxs-lookup"><span data-stu-id="2a2f1-128">no</span></span>        |
| [<span data-ttu-id="2a2f1-129">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2a2f1-129">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="2a2f1-130">não</span><span class="sxs-lookup"><span data-stu-id="2a2f1-130">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="2a2f1-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2a2f1-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a2f1-132">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2a2f1-132">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 




