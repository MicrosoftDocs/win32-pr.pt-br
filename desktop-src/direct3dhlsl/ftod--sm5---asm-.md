---
title: ftod (SM5-ASM)
description: Conversão por componente de dados de ponto flutuante de precisão simples para dados de ponto flutuante de precisão dupla.
ms.assetid: 95297556-41ED-4ED0-8F9A-16B7A440AF25
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6790735745805426d32aefcc5d5d771ade644e43
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104293581"
---
# <a name="ftod-sm5---asm"></a><span data-ttu-id="00d14-103">ftod (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="00d14-103">ftod (sm5 - asm)</span></span>

<span data-ttu-id="00d14-104">Conversão por componente de dados de ponto flutuante de precisão simples para dados de ponto flutuante de precisão dupla.</span><span class="sxs-lookup"><span data-stu-id="00d14-104">Component-wise conversion from single-precision floating-point data to double-precision floating-point data.</span></span>



| <span data-ttu-id="00d14-105">ftod dest \[ . Mask \] , \[ - \] src \[ . swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="00d14-105">ftod dest\[.mask\], \[-\]src\[.swizzle\],</span></span> |
|-------------------------------------------|



 



| <span data-ttu-id="00d14-106">Item</span><span class="sxs-lookup"><span data-stu-id="00d14-106">Item</span></span>                                                            | <span data-ttu-id="00d14-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="00d14-107">Description</span></span>                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="00d14-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="00d14-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="00d14-109">\[no \] endereço dos dados convertidos.</span><span class="sxs-lookup"><span data-stu-id="00d14-109">\[in\] The address of the converted data.</span></span><br/> |
| <span data-ttu-id="00d14-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="00d14-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="00d14-111">\[nos \] dados a serem convertidos.</span><span class="sxs-lookup"><span data-stu-id="00d14-111">\[in\] The data to be converted.</span></span><br/>          |



 

## <a name="remarks"></a><span data-ttu-id="00d14-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="00d14-112">Remarks</span></span>

<span data-ttu-id="00d14-113">Cada componente da origem é convertido da representação de precisão única para a representação de precisão dupla.</span><span class="sxs-lookup"><span data-stu-id="00d14-113">Each component of the source is converted from the single-precision representation to the double-precision representation.</span></span>

<span data-ttu-id="00d14-114">As máscaras de *destino* válidas são. XY,. zw e. xyzw.</span><span class="sxs-lookup"><span data-stu-id="00d14-114">The valid *dest* masks are .xy, .zw, and .xyzw.</span></span> <span data-ttu-id="00d14-115">. o XY recebe o resultado da primeira conversão e. zw recebe o resultado da segunda conversão.</span><span class="sxs-lookup"><span data-stu-id="00d14-115">.xy receives the result of the first conversion, and .zw receives the result of the second conversion.</span></span>

<span data-ttu-id="00d14-116">*dest* é um vec2 duplo entre (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="00d14-116">*dest* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>

<span data-ttu-id="00d14-117">*src* é um vec2 flutuante entre x e y (ZW ignorado) (post swizzle).</span><span class="sxs-lookup"><span data-stu-id="00d14-117">*src* is a float vec2 across x and y (zw ignored) (post swizzle).</span></span>

<span data-ttu-id="00d14-118">Para o float32<->conversões duplas, as implementações podem honrar as innormas float32 ou pode liberá-las.</span><span class="sxs-lookup"><span data-stu-id="00d14-118">For float32<->double conversions, implementations may either honor float32 denorms or may flush them.</span></span>

<span data-ttu-id="00d14-119">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="00d14-119">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="00d14-120">Vértice</span><span class="sxs-lookup"><span data-stu-id="00d14-120">Vertex</span></span> | <span data-ttu-id="00d14-121">Envoltória</span><span class="sxs-lookup"><span data-stu-id="00d14-121">Hull</span></span> | <span data-ttu-id="00d14-122">Domínio</span><span class="sxs-lookup"><span data-stu-id="00d14-122">Domain</span></span> | <span data-ttu-id="00d14-123">Geometria</span><span class="sxs-lookup"><span data-stu-id="00d14-123">Geometry</span></span> | <span data-ttu-id="00d14-124">16x16</span><span class="sxs-lookup"><span data-stu-id="00d14-124">Pixel</span></span> | <span data-ttu-id="00d14-125">Computação</span><span class="sxs-lookup"><span data-stu-id="00d14-125">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="00d14-126">X</span><span class="sxs-lookup"><span data-stu-id="00d14-126">X</span></span>      | <span data-ttu-id="00d14-127">X</span><span class="sxs-lookup"><span data-stu-id="00d14-127">X</span></span>    | <span data-ttu-id="00d14-128">X</span><span class="sxs-lookup"><span data-stu-id="00d14-128">X</span></span>      | <span data-ttu-id="00d14-129">X</span><span class="sxs-lookup"><span data-stu-id="00d14-129">X</span></span>        | <span data-ttu-id="00d14-130">X</span><span class="sxs-lookup"><span data-stu-id="00d14-130">X</span></span>     | <span data-ttu-id="00d14-131">X</span><span class="sxs-lookup"><span data-stu-id="00d14-131">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="00d14-132">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="00d14-132">Minimum Shader Model</span></span>

<span data-ttu-id="00d14-133">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="00d14-133">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="00d14-134">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="00d14-134">Shader Model</span></span>                                              | <span data-ttu-id="00d14-135">Com suporte</span><span class="sxs-lookup"><span data-stu-id="00d14-135">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="00d14-136">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="00d14-136">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="00d14-137">sim</span><span class="sxs-lookup"><span data-stu-id="00d14-137">yes</span></span>       |
| [<span data-ttu-id="00d14-138">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="00d14-138">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="00d14-139">não</span><span class="sxs-lookup"><span data-stu-id="00d14-139">no</span></span>        |
| [<span data-ttu-id="00d14-140">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="00d14-140">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="00d14-141">não</span><span class="sxs-lookup"><span data-stu-id="00d14-141">no</span></span>        |
| [<span data-ttu-id="00d14-142">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="00d14-142">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="00d14-143">não</span><span class="sxs-lookup"><span data-stu-id="00d14-143">no</span></span>        |
| [<span data-ttu-id="00d14-144">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="00d14-144">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="00d14-145">não</span><span class="sxs-lookup"><span data-stu-id="00d14-145">no</span></span>        |
| [<span data-ttu-id="00d14-146">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="00d14-146">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="00d14-147">não</span><span class="sxs-lookup"><span data-stu-id="00d14-147">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="00d14-148">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="00d14-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00d14-149">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="00d14-149">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





