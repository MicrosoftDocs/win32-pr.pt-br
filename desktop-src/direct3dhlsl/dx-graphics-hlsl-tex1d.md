---
title: tex1D (referência de HLSL)
description: Amostras de uma textura 1D.
ms.assetid: 587be0fd-af12-4bf0-862b-84988435e90e
keywords:
- tex1D HLSL
topic_type:
- apiref
api_name:
- tex1D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6dec5cc8a35b18c35076f99443ad3c1166fcf410
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641325"
---
# <a name="tex1d-hlsl-reference"></a><span data-ttu-id="e7a32-104">tex1D (referência de HLSL)</span><span class="sxs-lookup"><span data-stu-id="e7a32-104">tex1D (HLSL reference)</span></span>

<span data-ttu-id="e7a32-105">Amostras de uma textura 1D.</span><span class="sxs-lookup"><span data-stu-id="e7a32-105">Samples a 1D texture.</span></span>



| <span data-ttu-id="e7a32-106">RET tex1D (s, t)</span><span class="sxs-lookup"><span data-stu-id="e7a32-106">ret tex1D(s, t)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="e7a32-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e7a32-107">Parameters</span></span>



| <span data-ttu-id="e7a32-108">Item</span><span class="sxs-lookup"><span data-stu-id="e7a32-108">Item</span></span>                                                   | <span data-ttu-id="e7a32-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="e7a32-109">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="e7a32-110"><span id="s"></span><span id="S"></span>*&*</span><span class="sxs-lookup"><span data-stu-id="e7a32-110"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="e7a32-111">\[no \] estado de amostra.</span><span class="sxs-lookup"><span data-stu-id="e7a32-111">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="e7a32-112"><span id="t"></span><span id="T"></span>*t*</span><span class="sxs-lookup"><span data-stu-id="e7a32-112"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="e7a32-113">\[na \] coordenada de textura.</span><span class="sxs-lookup"><span data-stu-id="e7a32-113">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="e7a32-114">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="e7a32-114">Return Value</span></span>

<span data-ttu-id="e7a32-115">O valor dos dados de textura.</span><span class="sxs-lookup"><span data-stu-id="e7a32-115">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="e7a32-116">Descrição do tipo</span><span class="sxs-lookup"><span data-stu-id="e7a32-116">Type Description</span></span>



| <span data-ttu-id="e7a32-117">Name</span><span class="sxs-lookup"><span data-stu-id="e7a32-117">Name</span></span> | <span data-ttu-id="e7a32-118">Entrada/saída</span><span class="sxs-lookup"><span data-stu-id="e7a32-118">In/Out</span></span> | [<span data-ttu-id="e7a32-119">**Tipo de modelo**</span><span class="sxs-lookup"><span data-stu-id="e7a32-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="e7a32-120">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="e7a32-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="e7a32-121">Tamanho</span><span class="sxs-lookup"><span data-stu-id="e7a32-121">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="e7a32-122">s</span><span class="sxs-lookup"><span data-stu-id="e7a32-122">s</span></span>    | <span data-ttu-id="e7a32-123">in</span><span class="sxs-lookup"><span data-stu-id="e7a32-123">in</span></span>     | [<span data-ttu-id="e7a32-124">**objeto**</span><span class="sxs-lookup"><span data-stu-id="e7a32-124">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="e7a32-125">sampler1D</span><span class="sxs-lookup"><span data-stu-id="e7a32-125">sampler1D</span></span>](dx-graphics-hlsl-sampler.md)                      | <span data-ttu-id="e7a32-126">1</span><span class="sxs-lookup"><span data-stu-id="e7a32-126">1</span></span>    |
| <span data-ttu-id="e7a32-127">t</span><span class="sxs-lookup"><span data-stu-id="e7a32-127">t</span></span>    | <span data-ttu-id="e7a32-128">in</span><span class="sxs-lookup"><span data-stu-id="e7a32-128">in</span></span>     | [<span data-ttu-id="e7a32-129">**escalar**</span><span class="sxs-lookup"><span data-stu-id="e7a32-129">**scalar**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="e7a32-130">**FLOAT**</span><span class="sxs-lookup"><span data-stu-id="e7a32-130">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="e7a32-131">1</span><span class="sxs-lookup"><span data-stu-id="e7a32-131">1</span></span>    |
| <span data-ttu-id="e7a32-132">RET</span><span class="sxs-lookup"><span data-stu-id="e7a32-132">ret</span></span>  | <span data-ttu-id="e7a32-133">out</span><span class="sxs-lookup"><span data-stu-id="e7a32-133">out</span></span>    | [<span data-ttu-id="e7a32-134">**vetor**</span><span class="sxs-lookup"><span data-stu-id="e7a32-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="e7a32-135">**barra**</span><span class="sxs-lookup"><span data-stu-id="e7a32-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="e7a32-136">4</span><span class="sxs-lookup"><span data-stu-id="e7a32-136">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="e7a32-137">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="e7a32-137">Minimum Shader Model</span></span>

<span data-ttu-id="e7a32-138">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="e7a32-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="e7a32-139">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="e7a32-139">Shader Model</span></span>                                              | <span data-ttu-id="e7a32-140">Com suporte</span><span class="sxs-lookup"><span data-stu-id="e7a32-140">Supported</span></span>                                                                                                                         |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e7a32-141">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="e7a32-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="e7a32-142">Sim (somente sombreador de pixel), mas você deve usar a [opção de compilação herdada](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax) ao compilar.</span><span class="sxs-lookup"><span data-stu-id="e7a32-142">yes (pixel shader only), but you must use the [legacy compile option](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax) when compiling.</span></span> |
| [<span data-ttu-id="e7a32-143">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e7a32-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="e7a32-144">Sim (somente sombreador de pixel)</span><span class="sxs-lookup"><span data-stu-id="e7a32-144">yes (pixel shader only)</span></span>                                                                                                           |
| [<span data-ttu-id="e7a32-145">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e7a32-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="e7a32-146">Sim (somente sombreador de pixel)</span><span class="sxs-lookup"><span data-stu-id="e7a32-146">yes (pixel shader only)</span></span>                                                                                                           |
| [<span data-ttu-id="e7a32-147">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e7a32-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="e7a32-148">Sim (somente sombreador de pixel)</span><span class="sxs-lookup"><span data-stu-id="e7a32-148">yes (pixel shader only)</span></span>                                                                                                           |



 

## <a name="see-also"></a><span data-ttu-id="e7a32-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="e7a32-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7a32-150">**Funções intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="e7a32-150">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

