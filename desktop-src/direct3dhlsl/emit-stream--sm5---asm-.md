---
title: emit_stream (SM5-ASM)
description: Emitir um vértice para um determinado fluxo.
ms.assetid: 5DBB0BEC-6EA4-4C04-A3D2-853E48260226
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f56c2582453d18120e3e95b27af9c7613728fa62
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104365218"
---
# <a name="emit_stream-sm5---asm"></a><span data-ttu-id="a9dbd-103">fluxo de emissão \_ (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="a9dbd-103">emit\_stream (sm5 - asm)</span></span>

<span data-ttu-id="a9dbd-104">Emitir um vértice para um determinado fluxo.</span><span class="sxs-lookup"><span data-stu-id="a9dbd-104">Emit a vertex to a given stream.</span></span>



| <span data-ttu-id="a9dbd-105">emitir \_ fluxo streamIndex</span><span class="sxs-lookup"><span data-stu-id="a9dbd-105">emit\_stream streamIndex</span></span> |
|--------------------------|



 



| <span data-ttu-id="a9dbd-106">Item</span><span class="sxs-lookup"><span data-stu-id="a9dbd-106">Item</span></span>                                                                                                               | <span data-ttu-id="a9dbd-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="a9dbd-107">Description</span></span>                         |
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| <span data-ttu-id="a9dbd-108"><span id="streamIndex"></span><span id="streamindex"></span><span id="STREAMINDEX"></span>*streamIndex*</span><span class="sxs-lookup"><span data-stu-id="a9dbd-108"><span id="streamIndex"></span><span id="streamindex"></span><span id="STREAMINDEX"></span>*streamIndex*</span></span><br/> | <span data-ttu-id="a9dbd-109">\[no \] índice de fluxo.</span><span class="sxs-lookup"><span data-stu-id="a9dbd-109">\[in\] The stream index.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a9dbd-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="a9dbd-110">Remarks</span></span>

<span data-ttu-id="a9dbd-111">Essa instrução faz com que todos os registros de o declarados do \# fluxo de dados sejam lidos do sombreador de geometria para gerar um vértice.</span><span class="sxs-lookup"><span data-stu-id="a9dbd-111">This instruction causes all declared o\# registers for the given stream to be read out of the geometry shader to generate a vertex.</span></span> <span data-ttu-id="a9dbd-112">Após a emissão, todos os dados em todos os registros de saída de todos os fluxos se tornam não inicializados, não apenas o fluxo emitido para.</span><span class="sxs-lookup"><span data-stu-id="a9dbd-112">Afer the emit, all data in all output registers for all streams become uninitialized, not just the stream emitted to.</span></span>

<span data-ttu-id="a9dbd-113">*streamIndex* deve ser um valor imediato \[ 0.. 3 \] para um fluxo declarado.</span><span class="sxs-lookup"><span data-stu-id="a9dbd-113">*streamIndex* must be an immediate value \[0..3\] for a declared stream.</span></span>

<span data-ttu-id="a9dbd-114">Como várias chamadas de **\_ fluxo de emissão** são emitidas, os primitivos são gerados.</span><span class="sxs-lookup"><span data-stu-id="a9dbd-114">As multiple **emit\_stream** calls are issued, primitives are generated.</span></span>

### <a name="restrictions"></a><span data-ttu-id="a9dbd-115">Restrições</span><span class="sxs-lookup"><span data-stu-id="a9dbd-115">Restrictions</span></span>

-   <span data-ttu-id="a9dbd-116">**o \_ fluxo de emissão** pode aparecer qualquer número de vezes em um sombreador de geometria, incluindo dentro do controle de fluxo.</span><span class="sxs-lookup"><span data-stu-id="a9dbd-116">**emit\_stream** can appear any number of times in a geometry shader, including within flow control.</span></span>
-   <span data-ttu-id="a9dbd-117">Se os fluxos não tiverem sido declarados, você deverá usar [Emit](emit--sm4---asm-.md) em vez de **\_ Stream de emissão**.</span><span class="sxs-lookup"><span data-stu-id="a9dbd-117">If streams have not been declared, then you must use [emit](emit--sm4---asm-.md) instead of **emit\_stream**.</span></span>

<span data-ttu-id="a9dbd-118">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="a9dbd-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="a9dbd-119">Vértice</span><span class="sxs-lookup"><span data-stu-id="a9dbd-119">Vertex</span></span> | <span data-ttu-id="a9dbd-120">Envoltória</span><span class="sxs-lookup"><span data-stu-id="a9dbd-120">Hull</span></span> | <span data-ttu-id="a9dbd-121">Domínio</span><span class="sxs-lookup"><span data-stu-id="a9dbd-121">Domain</span></span> | <span data-ttu-id="a9dbd-122">Geometria</span><span class="sxs-lookup"><span data-stu-id="a9dbd-122">Geometry</span></span> | <span data-ttu-id="a9dbd-123">16x16</span><span class="sxs-lookup"><span data-stu-id="a9dbd-123">Pixel</span></span> | <span data-ttu-id="a9dbd-124">Computação</span><span class="sxs-lookup"><span data-stu-id="a9dbd-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        | <span data-ttu-id="a9dbd-125">X</span><span class="sxs-lookup"><span data-stu-id="a9dbd-125">X</span></span>        |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="a9dbd-126">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="a9dbd-126">Minimum Shader Model</span></span>

<span data-ttu-id="a9dbd-127">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="a9dbd-127">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="a9dbd-128">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="a9dbd-128">Shader Model</span></span>                                              | <span data-ttu-id="a9dbd-129">Com suporte</span><span class="sxs-lookup"><span data-stu-id="a9dbd-129">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="a9dbd-130">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="a9dbd-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="a9dbd-131">sim</span><span class="sxs-lookup"><span data-stu-id="a9dbd-131">yes</span></span>       |
| [<span data-ttu-id="a9dbd-132">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="a9dbd-132">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="a9dbd-133">não</span><span class="sxs-lookup"><span data-stu-id="a9dbd-133">no</span></span>        |
| [<span data-ttu-id="a9dbd-134">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="a9dbd-134">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="a9dbd-135">não</span><span class="sxs-lookup"><span data-stu-id="a9dbd-135">no</span></span>        |
| [<span data-ttu-id="a9dbd-136">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a9dbd-136">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="a9dbd-137">não</span><span class="sxs-lookup"><span data-stu-id="a9dbd-137">no</span></span>        |
| [<span data-ttu-id="a9dbd-138">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a9dbd-138">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="a9dbd-139">não</span><span class="sxs-lookup"><span data-stu-id="a9dbd-139">no</span></span>        |
| [<span data-ttu-id="a9dbd-140">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a9dbd-140">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="a9dbd-141">não</span><span class="sxs-lookup"><span data-stu-id="a9dbd-141">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="a9dbd-142">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a9dbd-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9dbd-143">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a9dbd-143">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





