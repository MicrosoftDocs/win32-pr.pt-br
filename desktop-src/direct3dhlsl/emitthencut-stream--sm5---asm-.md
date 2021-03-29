---
title: emitThenCut_stream (SM5-ASM)
description: Equivalente a um comando Emit seguido por um comando Cut. | emitThenCut_stream (SM5-ASM)
ms.assetid: E9D84647-E29B-4E31-9E95-9F7A173293D4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ae3129f2a3fb50664a5dbf070c7a1dae9bf5d6e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968315"
---
# <a name="emitthencut_stream-sm5---asm"></a><span data-ttu-id="a12b3-104">fluxo de emitThenCut \_ (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="a12b3-104">emitThenCut\_stream (sm5 - asm)</span></span>

<span data-ttu-id="a12b3-105">Equivalente a um comando [Emit](emit--sm4---asm-.md) seguido por um comando [Cut](cut--sm4---asm-.md) .</span><span class="sxs-lookup"><span data-stu-id="a12b3-105">Equivalent to an [emit](emit--sm4---asm-.md) command followed by a [cut](cut--sm4---asm-.md) command.</span></span>



| <span data-ttu-id="a12b3-106">emitThenCut \_ Stream streamIndex</span><span class="sxs-lookup"><span data-stu-id="a12b3-106">emitThenCut\_stream streamIndex</span></span> |
|---------------------------------|



 



| <span data-ttu-id="a12b3-107">Item</span><span class="sxs-lookup"><span data-stu-id="a12b3-107">Item</span></span>                                                                                                               | <span data-ttu-id="a12b3-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="a12b3-108">Description</span></span>                         |
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| <span data-ttu-id="a12b3-109"><span id="streamIndex"></span><span id="streamindex"></span><span id="STREAMINDEX"></span>*streamIndex*</span><span class="sxs-lookup"><span data-stu-id="a12b3-109"><span id="streamIndex"></span><span id="streamindex"></span><span id="STREAMINDEX"></span>*streamIndex*</span></span><br/> | <span data-ttu-id="a12b3-110">\[no \] índice de fluxo.</span><span class="sxs-lookup"><span data-stu-id="a12b3-110">\[in\] The stream index.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a12b3-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="a12b3-111">Remarks</span></span>

<span data-ttu-id="a12b3-112">Essa operação é útil ao produzir a saída do último vértice em uma topologia.</span><span class="sxs-lookup"><span data-stu-id="a12b3-112">This operation is useful when knowingly outputting the last vertex in a topology.</span></span>

<span data-ttu-id="a12b3-113">Se os fluxos não tiverem sido declarados, você deverá usar [emitThenCut](emitthencut--sm4---asm-.md) em vez de **emitThenCut \_ Stream**.</span><span class="sxs-lookup"><span data-stu-id="a12b3-113">If streams have not been declared, then you must use [emitThenCut](emitthencut--sm4---asm-.md) instead of **emitThenCut\_stream**.</span></span>

<span data-ttu-id="a12b3-114">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="a12b3-114">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="a12b3-115">Vértice</span><span class="sxs-lookup"><span data-stu-id="a12b3-115">Vertex</span></span> | <span data-ttu-id="a12b3-116">Envoltória</span><span class="sxs-lookup"><span data-stu-id="a12b3-116">Hull</span></span> | <span data-ttu-id="a12b3-117">Domínio</span><span class="sxs-lookup"><span data-stu-id="a12b3-117">Domain</span></span> | <span data-ttu-id="a12b3-118">Geometria</span><span class="sxs-lookup"><span data-stu-id="a12b3-118">Geometry</span></span> | <span data-ttu-id="a12b3-119">16x16</span><span class="sxs-lookup"><span data-stu-id="a12b3-119">Pixel</span></span> | <span data-ttu-id="a12b3-120">Computação</span><span class="sxs-lookup"><span data-stu-id="a12b3-120">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        | <span data-ttu-id="a12b3-121">X</span><span class="sxs-lookup"><span data-stu-id="a12b3-121">X</span></span>        |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="a12b3-122">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="a12b3-122">Minimum Shader Model</span></span>

<span data-ttu-id="a12b3-123">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="a12b3-123">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="a12b3-124">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="a12b3-124">Shader Model</span></span>                                              | <span data-ttu-id="a12b3-125">Com suporte</span><span class="sxs-lookup"><span data-stu-id="a12b3-125">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="a12b3-126">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="a12b3-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="a12b3-127">sim</span><span class="sxs-lookup"><span data-stu-id="a12b3-127">yes</span></span>       |
| [<span data-ttu-id="a12b3-128">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="a12b3-128">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="a12b3-129">não</span><span class="sxs-lookup"><span data-stu-id="a12b3-129">no</span></span>        |
| [<span data-ttu-id="a12b3-130">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="a12b3-130">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="a12b3-131">não</span><span class="sxs-lookup"><span data-stu-id="a12b3-131">no</span></span>        |
| [<span data-ttu-id="a12b3-132">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a12b3-132">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="a12b3-133">não</span><span class="sxs-lookup"><span data-stu-id="a12b3-133">no</span></span>        |
| [<span data-ttu-id="a12b3-134">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a12b3-134">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="a12b3-135">não</span><span class="sxs-lookup"><span data-stu-id="a12b3-135">no</span></span>        |
| [<span data-ttu-id="a12b3-136">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a12b3-136">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="a12b3-137">não</span><span class="sxs-lookup"><span data-stu-id="a12b3-137">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="a12b3-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a12b3-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a12b3-139">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a12b3-139">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





