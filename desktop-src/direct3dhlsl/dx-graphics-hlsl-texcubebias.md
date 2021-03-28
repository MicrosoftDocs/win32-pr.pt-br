---
title: texCUBEbias
description: Amostrar uma textura de cubo após a tendência do nível de MIP por t.w.
ms.assetid: dad27cff-6b10-45db-b70f-c4ad78c64e76
keywords:
- texCUBEbias HLSL
topic_type:
- apiref
api_name:
- texCUBEbias
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0129c20db1da320e9cb85aacfc4490124be28f8a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084585"
---
# <a name="texcubebias"></a><span data-ttu-id="faa46-104">texCUBEbias</span><span class="sxs-lookup"><span data-stu-id="faa46-104">texCUBEbias</span></span>

<span data-ttu-id="faa46-105">Amostrar uma textura de cubo após a tendência do nível de MIP por t.w.</span><span class="sxs-lookup"><span data-stu-id="faa46-105">Samples a cube texture after biasing the mip level by t.w.</span></span>



| <span data-ttu-id="faa46-106">RET texCUBEbias (s, t)</span><span class="sxs-lookup"><span data-stu-id="faa46-106">ret texCUBEbias(s, t)</span></span> |
|-----------------------|



 

## <a name="parameters"></a><span data-ttu-id="faa46-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="faa46-107">Parameters</span></span>



| <span data-ttu-id="faa46-108">Item</span><span class="sxs-lookup"><span data-stu-id="faa46-108">Item</span></span>                                                   | <span data-ttu-id="faa46-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="faa46-109">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="faa46-110"><span id="s"></span><span id="S"></span>*&*</span><span class="sxs-lookup"><span data-stu-id="faa46-110"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="faa46-111">\[no \] estado de amostra.</span><span class="sxs-lookup"><span data-stu-id="faa46-111">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="faa46-112"><span id="t"></span><span id="T"></span>*t*</span><span class="sxs-lookup"><span data-stu-id="faa46-112"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="faa46-113">\[na \] coordenada de textura.</span><span class="sxs-lookup"><span data-stu-id="faa46-113">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="faa46-114">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="faa46-114">Return Value</span></span>

<span data-ttu-id="faa46-115">O valor dos dados de textura.</span><span class="sxs-lookup"><span data-stu-id="faa46-115">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="faa46-116">Descrição do tipo</span><span class="sxs-lookup"><span data-stu-id="faa46-116">Type Description</span></span>



| <span data-ttu-id="faa46-117">Name</span><span class="sxs-lookup"><span data-stu-id="faa46-117">Name</span></span> | <span data-ttu-id="faa46-118">Entrada/saída</span><span class="sxs-lookup"><span data-stu-id="faa46-118">In/Out</span></span> | [<span data-ttu-id="faa46-119">**Tipo de modelo**</span><span class="sxs-lookup"><span data-stu-id="faa46-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="faa46-120">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="faa46-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="faa46-121">Tamanho</span><span class="sxs-lookup"><span data-stu-id="faa46-121">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="faa46-122">s</span><span class="sxs-lookup"><span data-stu-id="faa46-122">s</span></span>    | <span data-ttu-id="faa46-123">in</span><span class="sxs-lookup"><span data-stu-id="faa46-123">in</span></span>     | [<span data-ttu-id="faa46-124">**objeto**</span><span class="sxs-lookup"><span data-stu-id="faa46-124">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="faa46-125">samplerCUBE</span><span class="sxs-lookup"><span data-stu-id="faa46-125">samplerCUBE</span></span>](dx-graphics-hlsl-sampler.md)                    | <span data-ttu-id="faa46-126">1</span><span class="sxs-lookup"><span data-stu-id="faa46-126">1</span></span>    |
| <span data-ttu-id="faa46-127">t</span><span class="sxs-lookup"><span data-stu-id="faa46-127">t</span></span>    | <span data-ttu-id="faa46-128">in</span><span class="sxs-lookup"><span data-stu-id="faa46-128">in</span></span>     | [<span data-ttu-id="faa46-129">**vetor**</span><span class="sxs-lookup"><span data-stu-id="faa46-129">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="faa46-130">**barra**</span><span class="sxs-lookup"><span data-stu-id="faa46-130">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="faa46-131">4</span><span class="sxs-lookup"><span data-stu-id="faa46-131">4</span></span>    |
| <span data-ttu-id="faa46-132">RET</span><span class="sxs-lookup"><span data-stu-id="faa46-132">ret</span></span>  | <span data-ttu-id="faa46-133">out</span><span class="sxs-lookup"><span data-stu-id="faa46-133">out</span></span>    | [<span data-ttu-id="faa46-134">**vetor**</span><span class="sxs-lookup"><span data-stu-id="faa46-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="faa46-135">**barra**</span><span class="sxs-lookup"><span data-stu-id="faa46-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="faa46-136">4</span><span class="sxs-lookup"><span data-stu-id="faa46-136">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="faa46-137">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="faa46-137">Minimum Shader Model</span></span>

<span data-ttu-id="faa46-138">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="faa46-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="faa46-139">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="faa46-139">Shader Model</span></span>                                              | <span data-ttu-id="faa46-140">Com suporte</span><span class="sxs-lookup"><span data-stu-id="faa46-140">Supported</span></span>               |
|-----------------------------------------------------------|-------------------------|
| [<span data-ttu-id="faa46-141">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="faa46-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="faa46-142">Sim (somente sombreador de pixel)</span><span class="sxs-lookup"><span data-stu-id="faa46-142">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="faa46-143">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="faa46-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="faa46-144">Sim (somente sombreador de pixel)</span><span class="sxs-lookup"><span data-stu-id="faa46-144">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="faa46-145">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="faa46-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="faa46-146">Sim (somente sombreador de pixel)</span><span class="sxs-lookup"><span data-stu-id="faa46-146">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="faa46-147">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="faa46-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="faa46-148">não</span><span class="sxs-lookup"><span data-stu-id="faa46-148">no</span></span>                      |



 

## <a name="see-also"></a><span data-ttu-id="faa46-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="faa46-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="faa46-150">**Funções intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="faa46-150">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

