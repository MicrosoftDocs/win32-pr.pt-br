---
title: ineg (sm4-ASM)
description: complemento de 2.
ms.assetid: 20C1EEC8-E349-4398-8EE3-EDD01EBCD4B1
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec4da3e0cbb08bee7bd732a4da8175705d1e1a0f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104365257"
---
# <a name="ineg-sm4---asm"></a><span data-ttu-id="39cd7-103">ineg (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="39cd7-103">ineg (sm4 - asm)</span></span>

<span data-ttu-id="39cd7-104">complemento de 2.</span><span class="sxs-lookup"><span data-stu-id="39cd7-104">2's complement.</span></span>



| <span data-ttu-id="39cd7-105">ineg dest \[ . Mask \] , src0 \[ . swizzle</span><span class="sxs-lookup"><span data-stu-id="39cd7-105">ineg dest\[.mask\], src0\[.swizzle</span></span> |
|------------------------------------|



 



| <span data-ttu-id="39cd7-106">Item</span><span class="sxs-lookup"><span data-stu-id="39cd7-106">Item</span></span>                                                            | <span data-ttu-id="39cd7-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="39cd7-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="39cd7-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="39cd7-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="39cd7-109">\[no \] endereço do resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="39cd7-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="39cd7-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="39cd7-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="39cd7-111">\[in \] contém os valores para a operação.</span><span class="sxs-lookup"><span data-stu-id="39cd7-111">\[in\] Contains the values for the operation.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="39cd7-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="39cd7-112">Remarks</span></span>

<span data-ttu-id="39cd7-113">Essa instrução executa o complemento de componente-Wise 2 de cada valor de 32 bits em *src0*.</span><span class="sxs-lookup"><span data-stu-id="39cd7-113">This instruction performs component-wise 2's complement of each 32-bit value in *src0*.</span></span> <span data-ttu-id="39cd7-114">Os resultados de 32 bits são armazenados no *dest*.</span><span class="sxs-lookup"><span data-stu-id="39cd7-114">The 32-bit results are stored in *dest*.</span></span>

<span data-ttu-id="39cd7-115">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="39cd7-115">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="39cd7-116">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="39cd7-116">Vertex Shader</span></span> | <span data-ttu-id="39cd7-117">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="39cd7-117">Geometry Shader</span></span> | <span data-ttu-id="39cd7-118">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="39cd7-118">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="39cd7-119">x</span><span class="sxs-lookup"><span data-stu-id="39cd7-119">x</span></span>             | <span data-ttu-id="39cd7-120">x</span><span class="sxs-lookup"><span data-stu-id="39cd7-120">x</span></span>               | <span data-ttu-id="39cd7-121">x</span><span class="sxs-lookup"><span data-stu-id="39cd7-121">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="39cd7-122">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="39cd7-122">Minimum Shader Model</span></span>

<span data-ttu-id="39cd7-123">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="39cd7-123">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="39cd7-124">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="39cd7-124">Shader Model</span></span>                                              | <span data-ttu-id="39cd7-125">Com suporte</span><span class="sxs-lookup"><span data-stu-id="39cd7-125">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="39cd7-126">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="39cd7-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="39cd7-127">sim</span><span class="sxs-lookup"><span data-stu-id="39cd7-127">yes</span></span>       |
| [<span data-ttu-id="39cd7-128">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="39cd7-128">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="39cd7-129">sim</span><span class="sxs-lookup"><span data-stu-id="39cd7-129">yes</span></span>       |
| [<span data-ttu-id="39cd7-130">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="39cd7-130">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="39cd7-131">sim</span><span class="sxs-lookup"><span data-stu-id="39cd7-131">yes</span></span>       |
| [<span data-ttu-id="39cd7-132">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="39cd7-132">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="39cd7-133">não</span><span class="sxs-lookup"><span data-stu-id="39cd7-133">no</span></span>        |
| [<span data-ttu-id="39cd7-134">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="39cd7-134">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="39cd7-135">não</span><span class="sxs-lookup"><span data-stu-id="39cd7-135">no</span></span>        |
| [<span data-ttu-id="39cd7-136">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="39cd7-136">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="39cd7-137">não</span><span class="sxs-lookup"><span data-stu-id="39cd7-137">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="39cd7-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="39cd7-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39cd7-139">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="39cd7-139">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





