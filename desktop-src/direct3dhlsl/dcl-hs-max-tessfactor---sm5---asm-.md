---
title: dcl_hs_max_tessfactor (SM5-ASM)
description: Declare o maxTessFactor para o patch.
ms.assetid: 7EF0FD81-69FE-49F6-95DF-0C452A90A713
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69bd20fc8f4a3687988e8b100975f74016a45ae6
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104988624"
---
# <a name="dcl_hs_max_tessfactor-sm5---asm"></a><span data-ttu-id="33a14-103">DCL \_ HS \_ Max \_ tessfactor (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="33a14-103">dcl\_hs\_max\_tessfactor (sm5 - asm)</span></span>

<span data-ttu-id="33a14-104">Declare o maxTessFactor para o patch.</span><span class="sxs-lookup"><span data-stu-id="33a14-104">Declare the maxTessFactor for the patch.</span></span>



| <span data-ttu-id="33a14-105">DCL \_ HS \_ Max \_ tessfactor n</span><span class="sxs-lookup"><span data-stu-id="33a14-105">dcl\_hs\_max\_tessfactor n</span></span> |
|----------------------------|



 



| <span data-ttu-id="33a14-106">Item</span><span class="sxs-lookup"><span data-stu-id="33a14-106">Item</span></span>                                                   | <span data-ttu-id="33a14-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="33a14-107">Description</span></span>                          |
|--------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="33a14-108"><span id="n"></span><span id="N"></span>*p*</span><span class="sxs-lookup"><span data-stu-id="33a14-108"><span id="n"></span><span id="N"></span>*n*</span></span><br/> | <span data-ttu-id="33a14-109">\[no \] maxTessFactor.</span><span class="sxs-lookup"><span data-stu-id="33a14-109">\[in\] The maxTessFactor.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="33a14-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="33a14-110">Remarks</span></span>

<span data-ttu-id="33a14-111">MaxTessFactor é um valor de float32 no intervalo de {1,0... 64,0}.</span><span class="sxs-lookup"><span data-stu-id="33a14-111">The maxTessFactor is a float32 value in the range {1.0 ... 64.0}.</span></span>

<span data-ttu-id="33a14-112">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="33a14-112">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="33a14-113">Vértice</span><span class="sxs-lookup"><span data-stu-id="33a14-113">Vertex</span></span> | <span data-ttu-id="33a14-114">Envoltória</span><span class="sxs-lookup"><span data-stu-id="33a14-114">Hull</span></span> | <span data-ttu-id="33a14-115">Domínio</span><span class="sxs-lookup"><span data-stu-id="33a14-115">Domain</span></span> | <span data-ttu-id="33a14-116">Geometria</span><span class="sxs-lookup"><span data-stu-id="33a14-116">Geometry</span></span> | <span data-ttu-id="33a14-117">16x16</span><span class="sxs-lookup"><span data-stu-id="33a14-117">Pixel</span></span> | <span data-ttu-id="33a14-118">Computação</span><span class="sxs-lookup"><span data-stu-id="33a14-118">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="33a14-119">X</span><span class="sxs-lookup"><span data-stu-id="33a14-119">X</span></span>    |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="33a14-120">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="33a14-120">Minimum Shader Model</span></span>

<span data-ttu-id="33a14-121">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="33a14-121">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="33a14-122">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="33a14-122">Shader Model</span></span>                                              | <span data-ttu-id="33a14-123">Com suporte</span><span class="sxs-lookup"><span data-stu-id="33a14-123">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="33a14-124">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="33a14-124">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="33a14-125">sim</span><span class="sxs-lookup"><span data-stu-id="33a14-125">yes</span></span>       |
| [<span data-ttu-id="33a14-126">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="33a14-126">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="33a14-127">não</span><span class="sxs-lookup"><span data-stu-id="33a14-127">no</span></span>        |
| [<span data-ttu-id="33a14-128">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="33a14-128">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="33a14-129">não</span><span class="sxs-lookup"><span data-stu-id="33a14-129">no</span></span>        |
| [<span data-ttu-id="33a14-130">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="33a14-130">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="33a14-131">não</span><span class="sxs-lookup"><span data-stu-id="33a14-131">no</span></span>        |
| [<span data-ttu-id="33a14-132">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="33a14-132">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="33a14-133">não</span><span class="sxs-lookup"><span data-stu-id="33a14-133">no</span></span>        |
| [<span data-ttu-id="33a14-134">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="33a14-134">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="33a14-135">não</span><span class="sxs-lookup"><span data-stu-id="33a14-135">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="33a14-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="33a14-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33a14-137">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="33a14-137">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





