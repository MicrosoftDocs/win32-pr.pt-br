---
title: dcl_output_control_point_count (SM5-ASM)
description: Declara a contagem de pontos de controle de saída do sombreador envoltória.
ms.assetid: 51E8117F-1802-413B-9820-04D5CEBE2DB6
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 147f8f7021252f07cdb6dd0f225555ff0f23d54b
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104006928"
---
# <a name="dcl_output_control_point_count-sm5---asm"></a><span data-ttu-id="9cb2e-103">\_ \_ \_ contagem de pontos de controle de saída de DCL \_ (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="9cb2e-103">dcl\_output\_control\_point\_count (sm5 - asm)</span></span>

<span data-ttu-id="9cb2e-104">Declara a contagem de pontos de controle de saída do sombreador envoltória.</span><span class="sxs-lookup"><span data-stu-id="9cb2e-104">Declares the hull shader output control point count.</span></span>



| <span data-ttu-id="9cb2e-105">contagem de pontos de controle de saída de DCL \_ \_ \_ \_ N</span><span class="sxs-lookup"><span data-stu-id="9cb2e-105">dcl\_output\_control\_point\_count N</span></span> |
|--------------------------------------|



 



| <span data-ttu-id="9cb2e-106">Item</span><span class="sxs-lookup"><span data-stu-id="9cb2e-106">Item</span></span>                                                   | <span data-ttu-id="9cb2e-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="9cb2e-107">Description</span></span>                                                                                    |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9cb2e-108"><span id="N"></span><span id="n"></span>*P*</span><span class="sxs-lookup"><span data-stu-id="9cb2e-108"><span id="N"></span><span id="n"></span>*N*</span></span><br/> | <span data-ttu-id="9cb2e-109">\[em \] um valor inteiro de 0 a 32 que especifica a contagem de pontos de controle de saída.</span><span class="sxs-lookup"><span data-stu-id="9cb2e-109">\[in\] An integer value from 0 to 32 that specifies the output control point count.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9cb2e-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="9cb2e-110">Remarks</span></span>

<span data-ttu-id="9cb2e-111">O sombreador envoltória poderá produzir 0 pontos de controle se eles não forem necessários.</span><span class="sxs-lookup"><span data-stu-id="9cb2e-111">The hull shader can output 0 control points if they are not needed.</span></span>

<span data-ttu-id="9cb2e-112">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="9cb2e-112">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="9cb2e-113">Vértice</span><span class="sxs-lookup"><span data-stu-id="9cb2e-113">Vertex</span></span> | <span data-ttu-id="9cb2e-114">Envoltória</span><span class="sxs-lookup"><span data-stu-id="9cb2e-114">Hull</span></span>                 | <span data-ttu-id="9cb2e-115">Domínio</span><span class="sxs-lookup"><span data-stu-id="9cb2e-115">Domain</span></span> | <span data-ttu-id="9cb2e-116">Geometria</span><span class="sxs-lookup"><span data-stu-id="9cb2e-116">Geometry</span></span> | <span data-ttu-id="9cb2e-117">16x16</span><span class="sxs-lookup"><span data-stu-id="9cb2e-117">Pixel</span></span> | <span data-ttu-id="9cb2e-118">Computação</span><span class="sxs-lookup"><span data-stu-id="9cb2e-118">Compute</span></span> |
|--------|----------------------|--------|----------|-------|---------|
|        | <span data-ttu-id="9cb2e-119">Seção de declarações</span><span class="sxs-lookup"><span data-stu-id="9cb2e-119">Declarations Section</span></span> |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="9cb2e-120">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="9cb2e-120">Minimum Shader Model</span></span>

<span data-ttu-id="9cb2e-121">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="9cb2e-121">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="9cb2e-122">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="9cb2e-122">Shader Model</span></span>                                              | <span data-ttu-id="9cb2e-123">Com suporte</span><span class="sxs-lookup"><span data-stu-id="9cb2e-123">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="9cb2e-124">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="9cb2e-124">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="9cb2e-125">sim</span><span class="sxs-lookup"><span data-stu-id="9cb2e-125">yes</span></span>       |
| [<span data-ttu-id="9cb2e-126">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="9cb2e-126">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="9cb2e-127">não</span><span class="sxs-lookup"><span data-stu-id="9cb2e-127">no</span></span>        |
| [<span data-ttu-id="9cb2e-128">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="9cb2e-128">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="9cb2e-129">não</span><span class="sxs-lookup"><span data-stu-id="9cb2e-129">no</span></span>        |
| [<span data-ttu-id="9cb2e-130">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9cb2e-130">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="9cb2e-131">não</span><span class="sxs-lookup"><span data-stu-id="9cb2e-131">no</span></span>        |
| [<span data-ttu-id="9cb2e-132">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9cb2e-132">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="9cb2e-133">não</span><span class="sxs-lookup"><span data-stu-id="9cb2e-133">no</span></span>        |
| [<span data-ttu-id="9cb2e-134">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9cb2e-134">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="9cb2e-135">não</span><span class="sxs-lookup"><span data-stu-id="9cb2e-135">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="9cb2e-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9cb2e-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9cb2e-137">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9cb2e-137">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





