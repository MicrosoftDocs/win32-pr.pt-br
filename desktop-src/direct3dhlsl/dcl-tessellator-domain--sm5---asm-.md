---
title: dcl_tessellator_domain (SM5-ASM)
description: Declare o domínio Tessellator em uma seção de declaração do sombreador envoltória e o sombreador de domínio.
ms.assetid: 11A1D9D0-D848-4750-875B-7060CE1CF42A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8724ee9564239ffaca6f5c34a39fb1b4ef967e51
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104365284"
---
# <a name="dcl_tessellator_domain-sm5---asm"></a><span data-ttu-id="e3756-103">\_domínio DCL Tessellator \_ (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="e3756-103">dcl\_tessellator\_domain (sm5 - asm)</span></span>

<span data-ttu-id="e3756-104">Declare o domínio Tessellator em uma seção de declaração do sombreador envoltória e o sombreador de domínio.</span><span class="sxs-lookup"><span data-stu-id="e3756-104">Declare the tessellator domain in a hull shader declaration section, and the domain shader.</span></span>



| <span data-ttu-id="e3756-105">\_domínio DCL Tessellator \_ {Domain \_ Isoline </span><span class="sxs-lookup"><span data-stu-id="e3756-105">dcl\_tessellator\_domain {domain\_isoline </span></span>\| <span data-ttu-id="e3756-106">domínio \_ Tri </span><span class="sxs-lookup"><span data-stu-id="e3756-106">domain\_tri </span></span>\| <span data-ttu-id="e3756-107">domínio \_ quádruplo}</span><span class="sxs-lookup"><span data-stu-id="e3756-107">domain\_quad}</span></span> |
|---------------------------------------------------------------------------|



 



| <span data-ttu-id="e3756-108">Item</span><span class="sxs-lookup"><span data-stu-id="e3756-108">Item</span></span>                                                                                                                                                                                | <span data-ttu-id="e3756-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="e3756-109">Description</span></span>                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span data-ttu-id="e3756-110"><span id="domain_isoline___domain_tri___domain_quad"></span><span id="DOMAIN_ISOLINE___DOMAIN_TRI___DOMAIN_QUAD"></span>*domínio \_ Isoline \| domínio \_ Tri \| domínio \_ quádruplo*</span><span class="sxs-lookup"><span data-stu-id="e3756-110"><span id="domain_isoline___domain_tri___domain_quad"></span><span id="DOMAIN_ISOLINE___DOMAIN_TRI___DOMAIN_QUAD"></span>*domain\_isoline \| domain\_tri \| domain\_quad*</span></span><br/> | <span data-ttu-id="e3756-111">\[no \] domínio.</span><span class="sxs-lookup"><span data-stu-id="e3756-111">\[in\] The domain.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e3756-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="e3756-112">Remarks</span></span>

<span data-ttu-id="e3756-113">O comportamento será indefinido se o sombreador envoltória e o sombreador de domínio fornecerem incompatibilidade de domínios ou qualquer outro decalarations conflitante.</span><span class="sxs-lookup"><span data-stu-id="e3756-113">Behavior is undefined if the hull shader and domain shader provide mismatching domains or any other conflicting decalarations.</span></span>

<span data-ttu-id="e3756-114">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="e3756-114">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="e3756-115">Vértice</span><span class="sxs-lookup"><span data-stu-id="e3756-115">Vertex</span></span> | <span data-ttu-id="e3756-116">Envoltória</span><span class="sxs-lookup"><span data-stu-id="e3756-116">Hull</span></span>                 | <span data-ttu-id="e3756-117">Domínio</span><span class="sxs-lookup"><span data-stu-id="e3756-117">Domain</span></span> | <span data-ttu-id="e3756-118">Geometria</span><span class="sxs-lookup"><span data-stu-id="e3756-118">Geometry</span></span> | <span data-ttu-id="e3756-119">16x16</span><span class="sxs-lookup"><span data-stu-id="e3756-119">Pixel</span></span> | <span data-ttu-id="e3756-120">Computação</span><span class="sxs-lookup"><span data-stu-id="e3756-120">Compute</span></span> |
|--------|----------------------|--------|----------|-------|---------|
|        | <span data-ttu-id="e3756-121">Seção de declarações</span><span class="sxs-lookup"><span data-stu-id="e3756-121">Declarations Section</span></span> | <span data-ttu-id="e3756-122">X</span><span class="sxs-lookup"><span data-stu-id="e3756-122">X</span></span>      |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="e3756-123">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="e3756-123">Minimum Shader Model</span></span>

<span data-ttu-id="e3756-124">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="e3756-124">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="e3756-125">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="e3756-125">Shader Model</span></span>                                              | <span data-ttu-id="e3756-126">Com suporte</span><span class="sxs-lookup"><span data-stu-id="e3756-126">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="e3756-127">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="e3756-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="e3756-128">sim</span><span class="sxs-lookup"><span data-stu-id="e3756-128">yes</span></span>       |
| [<span data-ttu-id="e3756-129">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="e3756-129">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="e3756-130">não</span><span class="sxs-lookup"><span data-stu-id="e3756-130">no</span></span>        |
| [<span data-ttu-id="e3756-131">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="e3756-131">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="e3756-132">não</span><span class="sxs-lookup"><span data-stu-id="e3756-132">no</span></span>        |
| [<span data-ttu-id="e3756-133">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e3756-133">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="e3756-134">não</span><span class="sxs-lookup"><span data-stu-id="e3756-134">no</span></span>        |
| [<span data-ttu-id="e3756-135">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e3756-135">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="e3756-136">não</span><span class="sxs-lookup"><span data-stu-id="e3756-136">no</span></span>        |
| [<span data-ttu-id="e3756-137">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e3756-137">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="e3756-138">não</span><span class="sxs-lookup"><span data-stu-id="e3756-138">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="e3756-139">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e3756-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3756-140">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e3756-140">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





