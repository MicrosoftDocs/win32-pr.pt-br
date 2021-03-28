---
title: dcl_tessellator_partitioning (SM5-ASM)
description: Declare o particionamento Tessellator em uma seção de declaração do sombreador envoltória.
ms.assetid: 6EA00C6B-A0DE-4CE4-8B52-1337CA92CA5E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c6f6091301f95dd2364debec2bf54c0966c0e64
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104365283"
---
# <a name="dcl_tessellator_partitioning-sm5---asm"></a><span data-ttu-id="6f442-103">particionamento de Tessellator de DCL \_ \_ (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="6f442-103">dcl\_tessellator\_partitioning (sm5 - asm)</span></span>

<span data-ttu-id="6f442-104">Declare o particionamento Tessellator em uma seção de declaração do sombreador envoltória.</span><span class="sxs-lookup"><span data-stu-id="6f442-104">Declare the tessellator partitioning in a hull shader declaration section.</span></span>



| <span data-ttu-id="6f442-105">particionamento de Tessellator de DCL \_ \_ {particionamento \_ inteiro </span><span class="sxs-lookup"><span data-stu-id="6f442-105">dcl\_tessellator\_partitioning {partitioning\_integer</span></span>\| <span data-ttu-id="6f442-106">particionamento de \_ pow2 </span><span class="sxs-lookup"><span data-stu-id="6f442-106">partitioning\_pow2</span></span>\|<span data-ttu-id="6f442-107">\_fração fracionária \_ ímpar </span><span class="sxs-lookup"><span data-stu-id="6f442-107">partitioning\_fractional\_odd</span></span>\| <span data-ttu-id="6f442-108">particionamento de \_ frações \_ até mesmo}</span><span class="sxs-lookup"><span data-stu-id="6f442-108">partitioning\_fractional\_even}</span></span> |
|---------------------------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="6f442-109">Item</span><span class="sxs-lookup"><span data-stu-id="6f442-109">Item</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | <span data-ttu-id="6f442-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="6f442-110">Description</span></span>                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="6f442-111"><span id="partitioning_integer__________________________________partitioning_pow2_partitioning_fractional_odd__________________________________partitioning_fractional_even"></span><span id="PARTITIONING_INTEGER__________________________________PARTITIONING_POW2_PARTITIONING_FRACTIONAL_ODD__________________________________PARTITIONING_FRACTIONAL_EVEN"></span>*Particionando o pow2 de particionamento de inteiros Particionando o particionamento \_ \| \_ \| \_ \_ estranho fracionário \| \_ \_ uniforme*</span><span class="sxs-lookup"><span data-stu-id="6f442-111"><span id="partitioning_integer__________________________________partitioning_pow2_partitioning_fractional_odd__________________________________partitioning_fractional_even"></span><span id="PARTITIONING_INTEGER__________________________________PARTITIONING_POW2_PARTITIONING_FRACTIONAL_ODD__________________________________PARTITIONING_FRACTIONAL_EVEN"></span>*partitioning\_integer\| partitioning\_pow2\|partitioning\_fractional\_odd\| partitioning\_fractional\_even*</span></span><br/> | <span data-ttu-id="6f442-112">\[no \] particionamento Tessellator.</span><span class="sxs-lookup"><span data-stu-id="6f442-112">\[in\] The tessellator partitioning.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6f442-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="6f442-113">Remarks</span></span>

<span data-ttu-id="6f442-114">Do ponto de vista do hardware, o \_ pow2 se comporta exatamente como o \_ inteiro.</span><span class="sxs-lookup"><span data-stu-id="6f442-114">From the hardware point of view, \_pow2 behaves just like \_integer.</span></span> <span data-ttu-id="6f442-115">Cabe ao autor do sombreador HLSL e/ou compilercode arredondar TessFactors para potências de 2.</span><span class="sxs-lookup"><span data-stu-id="6f442-115">It is up to the HLSL shader author and/or compilercode to round TessFactors to powers of 2.</span></span>

<span data-ttu-id="6f442-116">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="6f442-116">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="6f442-117">Vértice</span><span class="sxs-lookup"><span data-stu-id="6f442-117">Vertex</span></span> | <span data-ttu-id="6f442-118">Envoltória</span><span class="sxs-lookup"><span data-stu-id="6f442-118">Hull</span></span>                 | <span data-ttu-id="6f442-119">Domínio</span><span class="sxs-lookup"><span data-stu-id="6f442-119">Domain</span></span> | <span data-ttu-id="6f442-120">Geometria</span><span class="sxs-lookup"><span data-stu-id="6f442-120">Geometry</span></span> | <span data-ttu-id="6f442-121">16x16</span><span class="sxs-lookup"><span data-stu-id="6f442-121">Pixel</span></span> | <span data-ttu-id="6f442-122">Computação</span><span class="sxs-lookup"><span data-stu-id="6f442-122">Compute</span></span> |
|--------|----------------------|--------|----------|-------|---------|
|        | <span data-ttu-id="6f442-123">Seção de declarações</span><span class="sxs-lookup"><span data-stu-id="6f442-123">Declarations Section</span></span> |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="6f442-124">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="6f442-124">Minimum Shader Model</span></span>

<span data-ttu-id="6f442-125">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="6f442-125">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="6f442-126">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="6f442-126">Shader Model</span></span>                                              | <span data-ttu-id="6f442-127">Com suporte</span><span class="sxs-lookup"><span data-stu-id="6f442-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="6f442-128">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="6f442-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="6f442-129">sim</span><span class="sxs-lookup"><span data-stu-id="6f442-129">yes</span></span>       |
| [<span data-ttu-id="6f442-130">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="6f442-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="6f442-131">não</span><span class="sxs-lookup"><span data-stu-id="6f442-131">no</span></span>        |
| [<span data-ttu-id="6f442-132">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="6f442-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="6f442-133">não</span><span class="sxs-lookup"><span data-stu-id="6f442-133">no</span></span>        |
| [<span data-ttu-id="6f442-134">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6f442-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="6f442-135">não</span><span class="sxs-lookup"><span data-stu-id="6f442-135">no</span></span>        |
| [<span data-ttu-id="6f442-136">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6f442-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="6f442-137">não</span><span class="sxs-lookup"><span data-stu-id="6f442-137">no</span></span>        |
| [<span data-ttu-id="6f442-138">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6f442-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="6f442-139">não</span><span class="sxs-lookup"><span data-stu-id="6f442-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="6f442-140">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6f442-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6f442-141">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6f442-141">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





