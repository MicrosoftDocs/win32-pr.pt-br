---
title: texCUBElod
description: Obtém uma textura de cubo com mipmaps. O LOD mipmap é especificado em t.w.
ms.assetid: fa7b236d-2c52-42bd-9123-919541f9e675
keywords:
- texCUBElod HLSL
topic_type:
- apiref
api_name:
- texCUBElod
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 72635211263085f03b87c2e013ea57d1b6a21464
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104967222"
---
# <a name="texcubelod"></a><span data-ttu-id="30393-105">texCUBElod</span><span class="sxs-lookup"><span data-stu-id="30393-105">texCUBElod</span></span>

<span data-ttu-id="30393-106">Obtém uma textura de cubo com mipmaps.</span><span class="sxs-lookup"><span data-stu-id="30393-106">Samples a cube texture with mipmaps.</span></span> <span data-ttu-id="30393-107">O LOD mipmap é especificado em t.w.</span><span class="sxs-lookup"><span data-stu-id="30393-107">The mipmap LOD is specified in t.w.</span></span>



| <span data-ttu-id="30393-108">RET texCUBElod (s, t)</span><span class="sxs-lookup"><span data-stu-id="30393-108">ret texCUBElod(s, t)</span></span> |
|----------------------|



 

## <a name="parameters"></a><span data-ttu-id="30393-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="30393-109">Parameters</span></span>



| <span data-ttu-id="30393-110">Item</span><span class="sxs-lookup"><span data-stu-id="30393-110">Item</span></span>                                                   | <span data-ttu-id="30393-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="30393-111">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="30393-112"><span id="s"></span><span id="S"></span>*&*</span><span class="sxs-lookup"><span data-stu-id="30393-112"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="30393-113">\[no \] estado de amostra.</span><span class="sxs-lookup"><span data-stu-id="30393-113">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="30393-114"><span id="t"></span><span id="T"></span>*t*</span><span class="sxs-lookup"><span data-stu-id="30393-114"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="30393-115">\[na \] coordenada de textura.</span><span class="sxs-lookup"><span data-stu-id="30393-115">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="30393-116">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="30393-116">Return Value</span></span>

<span data-ttu-id="30393-117">O valor dos dados de textura.</span><span class="sxs-lookup"><span data-stu-id="30393-117">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="30393-118">Descrição do tipo</span><span class="sxs-lookup"><span data-stu-id="30393-118">Type Description</span></span>



| <span data-ttu-id="30393-119">Name</span><span class="sxs-lookup"><span data-stu-id="30393-119">Name</span></span> | <span data-ttu-id="30393-120">Entrada/saída</span><span class="sxs-lookup"><span data-stu-id="30393-120">In/Out</span></span> | [<span data-ttu-id="30393-121">**Tipo de modelo**</span><span class="sxs-lookup"><span data-stu-id="30393-121">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="30393-122">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="30393-122">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="30393-123">Tamanho</span><span class="sxs-lookup"><span data-stu-id="30393-123">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="30393-124">s</span><span class="sxs-lookup"><span data-stu-id="30393-124">s</span></span>    | <span data-ttu-id="30393-125">in</span><span class="sxs-lookup"><span data-stu-id="30393-125">in</span></span>     | [<span data-ttu-id="30393-126">**objeto**</span><span class="sxs-lookup"><span data-stu-id="30393-126">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="30393-127">samplerCUBE</span><span class="sxs-lookup"><span data-stu-id="30393-127">samplerCUBE</span></span>](dx-graphics-hlsl-sampler.md)                    | <span data-ttu-id="30393-128">1</span><span class="sxs-lookup"><span data-stu-id="30393-128">1</span></span>    |
| <span data-ttu-id="30393-129">t</span><span class="sxs-lookup"><span data-stu-id="30393-129">t</span></span>    | <span data-ttu-id="30393-130">in</span><span class="sxs-lookup"><span data-stu-id="30393-130">in</span></span>     | [<span data-ttu-id="30393-131">**vetor**</span><span class="sxs-lookup"><span data-stu-id="30393-131">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="30393-132">**barra**</span><span class="sxs-lookup"><span data-stu-id="30393-132">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="30393-133">4</span><span class="sxs-lookup"><span data-stu-id="30393-133">4</span></span>    |
| <span data-ttu-id="30393-134">RET</span><span class="sxs-lookup"><span data-stu-id="30393-134">ret</span></span>  | <span data-ttu-id="30393-135">out</span><span class="sxs-lookup"><span data-stu-id="30393-135">out</span></span>    | [<span data-ttu-id="30393-136">**vetor**</span><span class="sxs-lookup"><span data-stu-id="30393-136">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="30393-137">**barra**</span><span class="sxs-lookup"><span data-stu-id="30393-137">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="30393-138">4</span><span class="sxs-lookup"><span data-stu-id="30393-138">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="30393-139">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="30393-139">Minimum Shader Model</span></span>

<span data-ttu-id="30393-140">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="30393-140">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="30393-141">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="30393-141">Shader Model</span></span>                                              | <span data-ttu-id="30393-142">Com suporte</span><span class="sxs-lookup"><span data-stu-id="30393-142">Supported</span></span>               |
|-----------------------------------------------------------|-------------------------|
| [<span data-ttu-id="30393-143">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="30393-143">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="30393-144">Sim (somente sombreador de pixel)</span><span class="sxs-lookup"><span data-stu-id="30393-144">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="30393-145">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="30393-145">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="30393-146">Sim (somente sombreador de pixel)</span><span class="sxs-lookup"><span data-stu-id="30393-146">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="30393-147">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="30393-147">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="30393-148">não</span><span class="sxs-lookup"><span data-stu-id="30393-148">no</span></span>                      |
| [<span data-ttu-id="30393-149">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="30393-149">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="30393-150">não</span><span class="sxs-lookup"><span data-stu-id="30393-150">no</span></span>                      |



 

## <a name="see-also"></a><span data-ttu-id="30393-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="30393-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30393-152">**Funções intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="30393-152">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

