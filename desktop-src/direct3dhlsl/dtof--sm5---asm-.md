---
title: dtof (SM5-ASM)
description: Conversão por componente de dados de ponto flutuante de precisão dupla para dados de ponto flutuante de precisão simples.
ms.assetid: 1D2EF05C-06EF-44F0-AA0F-22D3057FF43E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a66e72cf4c2cb1ac49adc492a586b4cbb9eef3b4
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104293555"
---
# <a name="dtof-sm5---asm"></a><span data-ttu-id="ecd17-103">dtof (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="ecd17-103">dtof (sm5 - asm)</span></span>

<span data-ttu-id="ecd17-104">Conversão por componente de dados de ponto flutuante de precisão dupla para dados de ponto flutuante de precisão simples.</span><span class="sxs-lookup"><span data-stu-id="ecd17-104">Component-wise conversion from double-precision floating-point data to single-precision floating-point data.</span></span>



| <span data-ttu-id="ecd17-105">dtof dest \[ . Mask \] , \[ - \] src \[ . swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="ecd17-105">dtof dest\[.mask\], \[-\]src\[.swizzle\],</span></span> |
|-------------------------------------------|



 



| <span data-ttu-id="ecd17-106">Item</span><span class="sxs-lookup"><span data-stu-id="ecd17-106">Item</span></span>                                                            | <span data-ttu-id="ecd17-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="ecd17-107">Description</span></span>                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ecd17-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="ecd17-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="ecd17-109">\[no \] endereço dos dados convertidos.</span><span class="sxs-lookup"><span data-stu-id="ecd17-109">\[in\] The address of the converted data.</span></span><br/> |
| <span data-ttu-id="ecd17-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="ecd17-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="ecd17-111">\[nos \] dados a serem convertidos.</span><span class="sxs-lookup"><span data-stu-id="ecd17-111">\[in\] The data to be converted.</span></span><br/>          |



 

## <a name="remarks"></a><span data-ttu-id="ecd17-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="ecd17-112">Remarks</span></span>

<span data-ttu-id="ecd17-113">Cada componente da origem é convertido da representação de precisão dupla para a representação de precisão única usando o arredondamento de arredondamento mais próximo.</span><span class="sxs-lookup"><span data-stu-id="ecd17-113">Each component of the source is converted from the double-precision representation to the single-precision representation using round-to-nearest-even rounding.</span></span>

<span data-ttu-id="ecd17-114">O swizzles válido para o parâmetro de origem é. xyzw,. xyxy,. zwxy,. zwzw.</span><span class="sxs-lookup"><span data-stu-id="ecd17-114">The valid swizzles for the source parameter are .xyzw, .xyxy, .zwxy, .zwzw.</span></span>

<span data-ttu-id="ecd17-115">As máscaras de *destino* válidas são um ou dois componentes.</span><span class="sxs-lookup"><span data-stu-id="ecd17-115">The valid *dest* masks are any one or two components.</span></span> <span data-ttu-id="ecd17-116">Isto é:. x,. y,. z,. w,. XY,. XZ,. XW,. yz,. YW,. zw o resultado da primeira conversão vai para o primeiro componente na máscara e o resultado do segundo componente vai para o segundo componente na máscara, se presente.</span><span class="sxs-lookup"><span data-stu-id="ecd17-116">That is: .x, .y, .z, .w, .xy, .xz, .xw, .yz, .yw, .zw The result of the first conversion goes to the first component in the mask, and the result of the second component goes in the second component in the mask, if present.</span></span>

<span data-ttu-id="ecd17-117">os componentes de *destino* são float32.</span><span class="sxs-lookup"><span data-stu-id="ecd17-117">*dest* components are float32.</span></span>

<span data-ttu-id="ecd17-118">*src* é um vec2 duplo entre (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB) post swizzle.</span><span class="sxs-lookup"><span data-stu-id="ecd17-118">*src* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB) post swizzle.</span></span>

<span data-ttu-id="ecd17-119">Para o float32<->conversões duplas, as implementações podem honrar as innormas float32 ou pode liberá-las.</span><span class="sxs-lookup"><span data-stu-id="ecd17-119">For float32<->double conversions, implementations may either honor float32 denorms or may flush them.</span></span>

<span data-ttu-id="ecd17-120">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="ecd17-120">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="ecd17-121">Vértice</span><span class="sxs-lookup"><span data-stu-id="ecd17-121">Vertex</span></span> | <span data-ttu-id="ecd17-122">Envoltória</span><span class="sxs-lookup"><span data-stu-id="ecd17-122">Hull</span></span> | <span data-ttu-id="ecd17-123">Domínio</span><span class="sxs-lookup"><span data-stu-id="ecd17-123">Domain</span></span> | <span data-ttu-id="ecd17-124">Geometria</span><span class="sxs-lookup"><span data-stu-id="ecd17-124">Geometry</span></span> | <span data-ttu-id="ecd17-125">16x16</span><span class="sxs-lookup"><span data-stu-id="ecd17-125">Pixel</span></span> | <span data-ttu-id="ecd17-126">Computação</span><span class="sxs-lookup"><span data-stu-id="ecd17-126">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="ecd17-127">X</span><span class="sxs-lookup"><span data-stu-id="ecd17-127">X</span></span>      | <span data-ttu-id="ecd17-128">X</span><span class="sxs-lookup"><span data-stu-id="ecd17-128">X</span></span>    | <span data-ttu-id="ecd17-129">X</span><span class="sxs-lookup"><span data-stu-id="ecd17-129">X</span></span>      | <span data-ttu-id="ecd17-130">X</span><span class="sxs-lookup"><span data-stu-id="ecd17-130">X</span></span>        | <span data-ttu-id="ecd17-131">X</span><span class="sxs-lookup"><span data-stu-id="ecd17-131">X</span></span>     | <span data-ttu-id="ecd17-132">X</span><span class="sxs-lookup"><span data-stu-id="ecd17-132">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="ecd17-133">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="ecd17-133">Minimum Shader Model</span></span>

<span data-ttu-id="ecd17-134">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="ecd17-134">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="ecd17-135">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="ecd17-135">Shader Model</span></span>                                              | <span data-ttu-id="ecd17-136">Com suporte</span><span class="sxs-lookup"><span data-stu-id="ecd17-136">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="ecd17-137">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="ecd17-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="ecd17-138">sim</span><span class="sxs-lookup"><span data-stu-id="ecd17-138">yes</span></span>       |
| [<span data-ttu-id="ecd17-139">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="ecd17-139">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="ecd17-140">não</span><span class="sxs-lookup"><span data-stu-id="ecd17-140">no</span></span>        |
| [<span data-ttu-id="ecd17-141">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="ecd17-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="ecd17-142">não</span><span class="sxs-lookup"><span data-stu-id="ecd17-142">no</span></span>        |
| [<span data-ttu-id="ecd17-143">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ecd17-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="ecd17-144">não</span><span class="sxs-lookup"><span data-stu-id="ecd17-144">no</span></span>        |
| [<span data-ttu-id="ecd17-145">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ecd17-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="ecd17-146">não</span><span class="sxs-lookup"><span data-stu-id="ecd17-146">no</span></span>        |
| [<span data-ttu-id="ecd17-147">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ecd17-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="ecd17-148">não</span><span class="sxs-lookup"><span data-stu-id="ecd17-148">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="ecd17-149">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ecd17-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ecd17-150">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ecd17-150">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





