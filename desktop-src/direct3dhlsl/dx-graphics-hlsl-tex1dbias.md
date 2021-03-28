---
title: tex1Dbias
description: Amostras de uma textura 1D após a tendência do nível de MIP por t.w.
ms.assetid: 2619ae23-e4b2-4699-b2ac-5ee711f9569a
keywords:
- tex1Dbias HLSL
topic_type:
- apiref
api_name:
- tex1Dbias
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0328b9328a1406177fa26bd566c0fbf7d384db63
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084633"
---
# <a name="tex1dbias"></a><span data-ttu-id="cf2c4-104">tex1Dbias</span><span class="sxs-lookup"><span data-stu-id="cf2c4-104">tex1Dbias</span></span>

<span data-ttu-id="cf2c4-105">Amostras de uma textura 1D após a tendência do nível de MIP por t.w.</span><span class="sxs-lookup"><span data-stu-id="cf2c4-105">Samples a 1D texture after biasing the mip level by t.w.</span></span>



| <span data-ttu-id="cf2c4-106">RET tex1Dbias (s, t)</span><span class="sxs-lookup"><span data-stu-id="cf2c4-106">ret tex1Dbias(s, t)</span></span> |
|---------------------|



 

## <a name="parameters"></a><span data-ttu-id="cf2c4-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cf2c4-107">Parameters</span></span>



| <span data-ttu-id="cf2c4-108">Item</span><span class="sxs-lookup"><span data-stu-id="cf2c4-108">Item</span></span>                                                   | <span data-ttu-id="cf2c4-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="cf2c4-109">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="cf2c4-110"><span id="s"></span><span id="S"></span>*&*</span><span class="sxs-lookup"><span data-stu-id="cf2c4-110"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="cf2c4-111">\[no \] estado de amostra.</span><span class="sxs-lookup"><span data-stu-id="cf2c4-111">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="cf2c4-112"><span id="t"></span><span id="T"></span>*t*</span><span class="sxs-lookup"><span data-stu-id="cf2c4-112"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="cf2c4-113">\[na \] coordenada de textura.</span><span class="sxs-lookup"><span data-stu-id="cf2c4-113">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="cf2c4-114">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="cf2c4-114">Return Value</span></span>

<span data-ttu-id="cf2c4-115">O valor dos dados de textura.</span><span class="sxs-lookup"><span data-stu-id="cf2c4-115">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="cf2c4-116">Descrição do tipo</span><span class="sxs-lookup"><span data-stu-id="cf2c4-116">Type Description</span></span>



| <span data-ttu-id="cf2c4-117">Name</span><span class="sxs-lookup"><span data-stu-id="cf2c4-117">Name</span></span> | <span data-ttu-id="cf2c4-118">Entrada/saída</span><span class="sxs-lookup"><span data-stu-id="cf2c4-118">In/Out</span></span> | [<span data-ttu-id="cf2c4-119">**Tipo de modelo**</span><span class="sxs-lookup"><span data-stu-id="cf2c4-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="cf2c4-120">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="cf2c4-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="cf2c4-121">Tamanho</span><span class="sxs-lookup"><span data-stu-id="cf2c4-121">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="cf2c4-122">s</span><span class="sxs-lookup"><span data-stu-id="cf2c4-122">s</span></span>    | <span data-ttu-id="cf2c4-123">in</span><span class="sxs-lookup"><span data-stu-id="cf2c4-123">in</span></span>     | [<span data-ttu-id="cf2c4-124">**objeto**</span><span class="sxs-lookup"><span data-stu-id="cf2c4-124">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="cf2c4-125">sampler1D</span><span class="sxs-lookup"><span data-stu-id="cf2c4-125">sampler1D</span></span>](dx-graphics-hlsl-sampler.md)                      | <span data-ttu-id="cf2c4-126">1</span><span class="sxs-lookup"><span data-stu-id="cf2c4-126">1</span></span>    |
| <span data-ttu-id="cf2c4-127">t</span><span class="sxs-lookup"><span data-stu-id="cf2c4-127">t</span></span>    | <span data-ttu-id="cf2c4-128">in</span><span class="sxs-lookup"><span data-stu-id="cf2c4-128">in</span></span>     | [<span data-ttu-id="cf2c4-129">**vetor**</span><span class="sxs-lookup"><span data-stu-id="cf2c4-129">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="cf2c4-130">**barra**</span><span class="sxs-lookup"><span data-stu-id="cf2c4-130">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="cf2c4-131">4</span><span class="sxs-lookup"><span data-stu-id="cf2c4-131">4</span></span>    |
| <span data-ttu-id="cf2c4-132">RET</span><span class="sxs-lookup"><span data-stu-id="cf2c4-132">ret</span></span>  | <span data-ttu-id="cf2c4-133">out</span><span class="sxs-lookup"><span data-stu-id="cf2c4-133">out</span></span>    | [<span data-ttu-id="cf2c4-134">**vetor**</span><span class="sxs-lookup"><span data-stu-id="cf2c4-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="cf2c4-135">**barra**</span><span class="sxs-lookup"><span data-stu-id="cf2c4-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="cf2c4-136">4</span><span class="sxs-lookup"><span data-stu-id="cf2c4-136">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="cf2c4-137">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="cf2c4-137">Minimum Shader Model</span></span>

<span data-ttu-id="cf2c4-138">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="cf2c4-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="cf2c4-139">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="cf2c4-139">Shader Model</span></span>                                              | <span data-ttu-id="cf2c4-140">Com suporte</span><span class="sxs-lookup"><span data-stu-id="cf2c4-140">Supported</span></span>               |
|-----------------------------------------------------------|-------------------------|
| [<span data-ttu-id="cf2c4-141">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="cf2c4-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="cf2c4-142">Sim (somente sombreador de pixel)</span><span class="sxs-lookup"><span data-stu-id="cf2c4-142">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="cf2c4-143">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cf2c4-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="cf2c4-144">Sim (somente sombreador de pixel)</span><span class="sxs-lookup"><span data-stu-id="cf2c4-144">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="cf2c4-145">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cf2c4-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="cf2c4-146">Sim (somente sombreador de pixel)</span><span class="sxs-lookup"><span data-stu-id="cf2c4-146">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="cf2c4-147">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cf2c4-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="cf2c4-148">não</span><span class="sxs-lookup"><span data-stu-id="cf2c4-148">no</span></span>                      |



 

## <a name="see-also"></a><span data-ttu-id="cf2c4-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="cf2c4-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf2c4-150">**Funções intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="cf2c4-150">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

