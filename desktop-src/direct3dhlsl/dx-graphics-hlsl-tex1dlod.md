---
title: tex1Dlod
description: Amostras de uma textura 1D com mipmaps. O LOD mipmap é especificado em t.w.
ms.assetid: f1700ee6-2f79-4b8b-ad34-30561f319356
keywords:
- tex1Dlod HLSL
topic_type:
- apiref
api_name:
- tex1Dlod
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8ca6379448290d027bba8a8b62f80cac39c84f25
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641564"
---
# <a name="tex1dlod"></a><span data-ttu-id="0a788-105">tex1Dlod</span><span class="sxs-lookup"><span data-stu-id="0a788-105">tex1Dlod</span></span>

<span data-ttu-id="0a788-106">Amostras de uma textura 1D com mipmaps.</span><span class="sxs-lookup"><span data-stu-id="0a788-106">Samples a 1D texture with mipmaps.</span></span> <span data-ttu-id="0a788-107">O LOD mipmap é especificado em t.w.</span><span class="sxs-lookup"><span data-stu-id="0a788-107">The mipmap LOD is specified in t.w.</span></span>



| <span data-ttu-id="0a788-108">RET tex1Dlod (s, t)</span><span class="sxs-lookup"><span data-stu-id="0a788-108">ret tex1Dlod(s, t)</span></span> |
|--------------------|



 

## <a name="parameters"></a><span data-ttu-id="0a788-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0a788-109">Parameters</span></span>



| <span data-ttu-id="0a788-110">Item</span><span class="sxs-lookup"><span data-stu-id="0a788-110">Item</span></span>                                                   | <span data-ttu-id="0a788-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="0a788-111">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="0a788-112"><span id="s"></span><span id="S"></span>*&*</span><span class="sxs-lookup"><span data-stu-id="0a788-112"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="0a788-113">\[no \] estado de amostra.</span><span class="sxs-lookup"><span data-stu-id="0a788-113">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="0a788-114"><span id="t"></span><span id="T"></span>*t*</span><span class="sxs-lookup"><span data-stu-id="0a788-114"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="0a788-115">\[na \] coordenada de textura.</span><span class="sxs-lookup"><span data-stu-id="0a788-115">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="0a788-116">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="0a788-116">Return Value</span></span>

<span data-ttu-id="0a788-117">O valor dos dados de textura.</span><span class="sxs-lookup"><span data-stu-id="0a788-117">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="0a788-118">Descrição do tipo</span><span class="sxs-lookup"><span data-stu-id="0a788-118">Type Description</span></span>



| <span data-ttu-id="0a788-119">Name</span><span class="sxs-lookup"><span data-stu-id="0a788-119">Name</span></span> | <span data-ttu-id="0a788-120">Entrada/saída</span><span class="sxs-lookup"><span data-stu-id="0a788-120">In/Out</span></span> | [<span data-ttu-id="0a788-121">**Tipo de modelo**</span><span class="sxs-lookup"><span data-stu-id="0a788-121">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="0a788-122">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="0a788-122">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="0a788-123">Tamanho</span><span class="sxs-lookup"><span data-stu-id="0a788-123">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="0a788-124">s</span><span class="sxs-lookup"><span data-stu-id="0a788-124">s</span></span>    | <span data-ttu-id="0a788-125">in</span><span class="sxs-lookup"><span data-stu-id="0a788-125">in</span></span>     | [<span data-ttu-id="0a788-126">**objeto**</span><span class="sxs-lookup"><span data-stu-id="0a788-126">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="0a788-127">sampler1D</span><span class="sxs-lookup"><span data-stu-id="0a788-127">sampler1D</span></span>](dx-graphics-hlsl-sampler.md)                      | <span data-ttu-id="0a788-128">1</span><span class="sxs-lookup"><span data-stu-id="0a788-128">1</span></span>    |
| <span data-ttu-id="0a788-129">t</span><span class="sxs-lookup"><span data-stu-id="0a788-129">t</span></span>    | <span data-ttu-id="0a788-130">in</span><span class="sxs-lookup"><span data-stu-id="0a788-130">in</span></span>     | [<span data-ttu-id="0a788-131">**vetor**</span><span class="sxs-lookup"><span data-stu-id="0a788-131">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="0a788-132">**barra**</span><span class="sxs-lookup"><span data-stu-id="0a788-132">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="0a788-133">4</span><span class="sxs-lookup"><span data-stu-id="0a788-133">4</span></span>    |
| <span data-ttu-id="0a788-134">RET</span><span class="sxs-lookup"><span data-stu-id="0a788-134">ret</span></span>  | <span data-ttu-id="0a788-135">out</span><span class="sxs-lookup"><span data-stu-id="0a788-135">out</span></span>    | [<span data-ttu-id="0a788-136">**vetor**</span><span class="sxs-lookup"><span data-stu-id="0a788-136">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="0a788-137">**barra**</span><span class="sxs-lookup"><span data-stu-id="0a788-137">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="0a788-138">4</span><span class="sxs-lookup"><span data-stu-id="0a788-138">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="0a788-139">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="0a788-139">Minimum Shader Model</span></span>

<span data-ttu-id="0a788-140">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="0a788-140">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="0a788-141">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="0a788-141">Shader Model</span></span>                                              | <span data-ttu-id="0a788-142">Com suporte</span><span class="sxs-lookup"><span data-stu-id="0a788-142">Supported</span></span>               |
|-----------------------------------------------------------|-------------------------|
| [<span data-ttu-id="0a788-143">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="0a788-143">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="0a788-144">Sim (somente sombreador de pixel)</span><span class="sxs-lookup"><span data-stu-id="0a788-144">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="0a788-145">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0a788-145">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="0a788-146">Sim (somente sombreador de pixel)</span><span class="sxs-lookup"><span data-stu-id="0a788-146">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="0a788-147">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0a788-147">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="0a788-148">não</span><span class="sxs-lookup"><span data-stu-id="0a788-148">no</span></span>                      |
| [<span data-ttu-id="0a788-149">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0a788-149">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="0a788-150">não</span><span class="sxs-lookup"><span data-stu-id="0a788-150">no</span></span>                      |



 

## <a name="see-also"></a><span data-ttu-id="0a788-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="0a788-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a788-152">**Funções intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="0a788-152">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

