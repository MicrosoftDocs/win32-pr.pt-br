---
title: tex3Dlod
description: Amostras de uma textura 3D com mipmaps. O LOD mipmap é especificado em t.w.
ms.assetid: 9bdd8fa1-8c02-4765-8f4d-61ceb532354e
keywords:
- tex3Dlod HLSL
topic_type:
- apiref
api_name:
- tex3Dlod
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bc25af449f7f32e94d4ca344bf5ef3a4d09b376c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104967179"
---
# <a name="tex3dlod"></a><span data-ttu-id="706ab-105">tex3Dlod</span><span class="sxs-lookup"><span data-stu-id="706ab-105">tex3Dlod</span></span>

<span data-ttu-id="706ab-106">Amostras de uma textura 3D com mipmaps.</span><span class="sxs-lookup"><span data-stu-id="706ab-106">Samples a 3D texture with mipmaps.</span></span> <span data-ttu-id="706ab-107">O LOD mipmap é especificado em t.w.</span><span class="sxs-lookup"><span data-stu-id="706ab-107">The mipmap LOD is specified in t.w.</span></span>



| <span data-ttu-id="706ab-108">RET tex3Dlod (s, t)</span><span class="sxs-lookup"><span data-stu-id="706ab-108">ret tex3Dlod(s, t)</span></span> |
|--------------------|



 

## <a name="parameters"></a><span data-ttu-id="706ab-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="706ab-109">Parameters</span></span>



| <span data-ttu-id="706ab-110">Item</span><span class="sxs-lookup"><span data-stu-id="706ab-110">Item</span></span>                                                   | <span data-ttu-id="706ab-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="706ab-111">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="706ab-112"><span id="s"></span><span id="S"></span>*&*</span><span class="sxs-lookup"><span data-stu-id="706ab-112"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="706ab-113">\[no \] estado de amostra.</span><span class="sxs-lookup"><span data-stu-id="706ab-113">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="706ab-114"><span id="t"></span><span id="T"></span>*t*</span><span class="sxs-lookup"><span data-stu-id="706ab-114"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="706ab-115">\[na \] coordenada de textura.</span><span class="sxs-lookup"><span data-stu-id="706ab-115">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="706ab-116">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="706ab-116">Return Value</span></span>

<span data-ttu-id="706ab-117">O valor dos dados de textura.</span><span class="sxs-lookup"><span data-stu-id="706ab-117">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="706ab-118">Descrição do tipo</span><span class="sxs-lookup"><span data-stu-id="706ab-118">Type Description</span></span>



| <span data-ttu-id="706ab-119">Name</span><span class="sxs-lookup"><span data-stu-id="706ab-119">Name</span></span> | <span data-ttu-id="706ab-120">Entrada/saída</span><span class="sxs-lookup"><span data-stu-id="706ab-120">In/Out</span></span> | [<span data-ttu-id="706ab-121">**Tipo de modelo**</span><span class="sxs-lookup"><span data-stu-id="706ab-121">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="706ab-122">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="706ab-122">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="706ab-123">Tamanho</span><span class="sxs-lookup"><span data-stu-id="706ab-123">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="706ab-124">s</span><span class="sxs-lookup"><span data-stu-id="706ab-124">s</span></span>    | <span data-ttu-id="706ab-125">in</span><span class="sxs-lookup"><span data-stu-id="706ab-125">in</span></span>     | [<span data-ttu-id="706ab-126">**objeto**</span><span class="sxs-lookup"><span data-stu-id="706ab-126">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="706ab-127">sampler3D</span><span class="sxs-lookup"><span data-stu-id="706ab-127">sampler3D</span></span>](dx-graphics-hlsl-sampler.md)                      | <span data-ttu-id="706ab-128">1</span><span class="sxs-lookup"><span data-stu-id="706ab-128">1</span></span>    |
| <span data-ttu-id="706ab-129">t</span><span class="sxs-lookup"><span data-stu-id="706ab-129">t</span></span>    | <span data-ttu-id="706ab-130">in</span><span class="sxs-lookup"><span data-stu-id="706ab-130">in</span></span>     | [<span data-ttu-id="706ab-131">**vetor**</span><span class="sxs-lookup"><span data-stu-id="706ab-131">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="706ab-132">**barra**</span><span class="sxs-lookup"><span data-stu-id="706ab-132">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="706ab-133">4</span><span class="sxs-lookup"><span data-stu-id="706ab-133">4</span></span>    |
| <span data-ttu-id="706ab-134">RET</span><span class="sxs-lookup"><span data-stu-id="706ab-134">ret</span></span>  | <span data-ttu-id="706ab-135">out</span><span class="sxs-lookup"><span data-stu-id="706ab-135">out</span></span>    | [<span data-ttu-id="706ab-136">**vetor**</span><span class="sxs-lookup"><span data-stu-id="706ab-136">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="706ab-137">**barra**</span><span class="sxs-lookup"><span data-stu-id="706ab-137">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="706ab-138">4</span><span class="sxs-lookup"><span data-stu-id="706ab-138">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="706ab-139">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="706ab-139">Minimum Shader Model</span></span>

<span data-ttu-id="706ab-140">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="706ab-140">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="706ab-141">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="706ab-141">Shader Model</span></span>                                              | <span data-ttu-id="706ab-142">Com suporte</span><span class="sxs-lookup"><span data-stu-id="706ab-142">Supported</span></span>               |
|-----------------------------------------------------------|-------------------------|
| [<span data-ttu-id="706ab-143">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="706ab-143">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="706ab-144">Sim (somente sombreador de pixel)</span><span class="sxs-lookup"><span data-stu-id="706ab-144">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="706ab-145">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="706ab-145">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="706ab-146">Sim (somente sombreador de pixel)</span><span class="sxs-lookup"><span data-stu-id="706ab-146">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="706ab-147">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="706ab-147">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="706ab-148">não</span><span class="sxs-lookup"><span data-stu-id="706ab-148">no</span></span>                      |
| [<span data-ttu-id="706ab-149">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="706ab-149">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="706ab-150">não</span><span class="sxs-lookup"><span data-stu-id="706ab-150">no</span></span>                      |



 

## <a name="see-also"></a><span data-ttu-id="706ab-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="706ab-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="706ab-152">**Funções intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="706ab-152">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

