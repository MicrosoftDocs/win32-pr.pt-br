---
title: dcl_stream (SM5-ASM)
description: Declare um fluxo de saída do sombreador de geometria.
ms.assetid: 0A8B8AB5-B7B0-46BB-91E8-B2E8E3D64B74
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f46903c3257c280788e91c25700743a23c146fe
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104365286"
---
# <a name="dcl_stream-sm5---asm"></a><span data-ttu-id="032e5-103">\_fluxo de DCL (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="032e5-103">dcl\_stream (sm5 - asm)</span></span>

<span data-ttu-id="032e5-104">Declare um fluxo de saída do sombreador de geometria.</span><span class="sxs-lookup"><span data-stu-id="032e5-104">Declare a geometry shader output stream.</span></span>



| <span data-ttu-id="032e5-105">fluxo de DCL \_ m\#</span><span class="sxs-lookup"><span data-stu-id="032e5-105">dcl\_stream m\#</span></span> |
|-----------------|



 



| <span data-ttu-id="032e5-106">Item</span><span class="sxs-lookup"><span data-stu-id="032e5-106">Item</span></span>                                                       | <span data-ttu-id="032e5-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="032e5-107">Description</span></span>                             |
|------------------------------------------------------------|-----------------------------------------|
| <span data-ttu-id="032e5-108"><span id="m_"></span><span id="M_"></span>*d\#*</span><span class="sxs-lookup"><span data-stu-id="032e5-108"><span id="m_"></span><span id="M_"></span>*m\#*</span></span><br/> | <span data-ttu-id="032e5-109">\[no \] fluxo 0.. 3 (M0.. m3).</span><span class="sxs-lookup"><span data-stu-id="032e5-109">\[in\] Stream 0..3 (m0..m3).</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="032e5-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="032e5-110">Remarks</span></span>

<span data-ttu-id="032e5-111">Um determinado fluxo só pode ser declarado uma vez.</span><span class="sxs-lookup"><span data-stu-id="032e5-111">A given stream can only be declared once.</span></span>

<span data-ttu-id="032e5-112">Se nenhum fluxo for declarado, as declarações de topologia de saída e saída serão consideradas para o fluxo 0.</span><span class="sxs-lookup"><span data-stu-id="032e5-112">If no streams are declared, output and output topology declarations are assumed to be for stream 0.</span></span>

<span data-ttu-id="032e5-113">O primeiro **\_ fluxo DCL** não pode aparecer após nenhuma instrução de **\_ saída DCL** ou **\_ outputTopology DCL** .</span><span class="sxs-lookup"><span data-stu-id="032e5-113">The first **dcl\_stream** cannot appear after any **dcl\_output** or **dcl\_outputTopology** statements.</span></span>

<span data-ttu-id="032e5-114">Todas as instruções de **\_ saída DCL** ou **DCL \_ outputToplogy** após qualquer instrução de **\_ fluxo** m de DCL \# definem as saídas para o fluxo m \# .</span><span class="sxs-lookup"><span data-stu-id="032e5-114">Any **dcl\_output** or **dcl\_outputToplogy** statements after any **dcl\_stream** m\# statement define the outputs for stream m\#.</span></span>

<span data-ttu-id="032e5-115">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="032e5-115">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="032e5-116">Vértice</span><span class="sxs-lookup"><span data-stu-id="032e5-116">Vertex</span></span> | <span data-ttu-id="032e5-117">Envoltória</span><span class="sxs-lookup"><span data-stu-id="032e5-117">Hull</span></span> | <span data-ttu-id="032e5-118">Domínio</span><span class="sxs-lookup"><span data-stu-id="032e5-118">Domain</span></span> | <span data-ttu-id="032e5-119">Geometria</span><span class="sxs-lookup"><span data-stu-id="032e5-119">Geometry</span></span> | <span data-ttu-id="032e5-120">16x16</span><span class="sxs-lookup"><span data-stu-id="032e5-120">Pixel</span></span> | <span data-ttu-id="032e5-121">Computação</span><span class="sxs-lookup"><span data-stu-id="032e5-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        | <span data-ttu-id="032e5-122">X</span><span class="sxs-lookup"><span data-stu-id="032e5-122">X</span></span>        |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="032e5-123">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="032e5-123">Minimum Shader Model</span></span>

<span data-ttu-id="032e5-124">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="032e5-124">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="032e5-125">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="032e5-125">Shader Model</span></span>                                              | <span data-ttu-id="032e5-126">Com suporte</span><span class="sxs-lookup"><span data-stu-id="032e5-126">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="032e5-127">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="032e5-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="032e5-128">sim</span><span class="sxs-lookup"><span data-stu-id="032e5-128">yes</span></span>       |
| [<span data-ttu-id="032e5-129">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="032e5-129">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="032e5-130">não</span><span class="sxs-lookup"><span data-stu-id="032e5-130">no</span></span>        |
| [<span data-ttu-id="032e5-131">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="032e5-131">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="032e5-132">não</span><span class="sxs-lookup"><span data-stu-id="032e5-132">no</span></span>        |
| [<span data-ttu-id="032e5-133">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="032e5-133">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="032e5-134">não</span><span class="sxs-lookup"><span data-stu-id="032e5-134">no</span></span>        |
| [<span data-ttu-id="032e5-135">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="032e5-135">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="032e5-136">não</span><span class="sxs-lookup"><span data-stu-id="032e5-136">no</span></span>        |
| [<span data-ttu-id="032e5-137">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="032e5-137">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="032e5-138">não</span><span class="sxs-lookup"><span data-stu-id="032e5-138">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="032e5-139">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="032e5-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="032e5-140">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="032e5-140">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





