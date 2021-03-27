---
title: tex2D (referência de HLSL)
description: Amostras de uma textura 2D.
ms.assetid: 9f4cbca8-c3de-42ed-89d9-5e86e47d12e5
keywords:
- tex2D HLSL
topic_type:
- apiref
api_name:
- tex2D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0ac8edb3bc4bb84c2259e193abda90dc32ef385d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641655"
---
# <a name="tex2d-hlsl-reference"></a><span data-ttu-id="2772b-104">tex2D (referência de HLSL)</span><span class="sxs-lookup"><span data-stu-id="2772b-104">tex2D (HLSL reference)</span></span>

<span data-ttu-id="2772b-105">Amostras de uma textura 2D.</span><span class="sxs-lookup"><span data-stu-id="2772b-105">Samples a 2D texture.</span></span>



| <span data-ttu-id="2772b-106">RET tex2D (s, t)</span><span class="sxs-lookup"><span data-stu-id="2772b-106">ret tex2D(s, t)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="2772b-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2772b-107">Parameters</span></span>



| <span data-ttu-id="2772b-108">Item</span><span class="sxs-lookup"><span data-stu-id="2772b-108">Item</span></span>                                                   | <span data-ttu-id="2772b-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="2772b-109">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="2772b-110"><span id="s"></span><span id="S"></span>*&*</span><span class="sxs-lookup"><span data-stu-id="2772b-110"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="2772b-111">\[no \] estado de amostra.</span><span class="sxs-lookup"><span data-stu-id="2772b-111">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="2772b-112"><span id="t"></span><span id="T"></span>*t*</span><span class="sxs-lookup"><span data-stu-id="2772b-112"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="2772b-113">\[na \] coordenada de textura.</span><span class="sxs-lookup"><span data-stu-id="2772b-113">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="2772b-114">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="2772b-114">Return Value</span></span>

<span data-ttu-id="2772b-115">O valor dos dados de textura.</span><span class="sxs-lookup"><span data-stu-id="2772b-115">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="2772b-116">Descrição do tipo</span><span class="sxs-lookup"><span data-stu-id="2772b-116">Type Description</span></span>



| <span data-ttu-id="2772b-117">Name</span><span class="sxs-lookup"><span data-stu-id="2772b-117">Name</span></span> | <span data-ttu-id="2772b-118">Entrada/saída</span><span class="sxs-lookup"><span data-stu-id="2772b-118">In/Out</span></span> | [<span data-ttu-id="2772b-119">**Tipo de modelo**</span><span class="sxs-lookup"><span data-stu-id="2772b-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="2772b-120">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="2772b-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="2772b-121">Tamanho</span><span class="sxs-lookup"><span data-stu-id="2772b-121">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="2772b-122">s</span><span class="sxs-lookup"><span data-stu-id="2772b-122">s</span></span>    | <span data-ttu-id="2772b-123">in</span><span class="sxs-lookup"><span data-stu-id="2772b-123">in</span></span>     | [<span data-ttu-id="2772b-124">**objeto**</span><span class="sxs-lookup"><span data-stu-id="2772b-124">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="2772b-125">sampler2D</span><span class="sxs-lookup"><span data-stu-id="2772b-125">sampler2D</span></span>](dx-graphics-hlsl-sampler.md)                      | <span data-ttu-id="2772b-126">1</span><span class="sxs-lookup"><span data-stu-id="2772b-126">1</span></span>    |
| <span data-ttu-id="2772b-127">t</span><span class="sxs-lookup"><span data-stu-id="2772b-127">t</span></span>    | <span data-ttu-id="2772b-128">in</span><span class="sxs-lookup"><span data-stu-id="2772b-128">in</span></span>     | [<span data-ttu-id="2772b-129">**vetor**</span><span class="sxs-lookup"><span data-stu-id="2772b-129">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="2772b-130">**barra**</span><span class="sxs-lookup"><span data-stu-id="2772b-130">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="2772b-131">2</span><span class="sxs-lookup"><span data-stu-id="2772b-131">2</span></span>    |
| <span data-ttu-id="2772b-132">RET</span><span class="sxs-lookup"><span data-stu-id="2772b-132">ret</span></span>  | <span data-ttu-id="2772b-133">out</span><span class="sxs-lookup"><span data-stu-id="2772b-133">out</span></span>    | [<span data-ttu-id="2772b-134">**vetor**</span><span class="sxs-lookup"><span data-stu-id="2772b-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="2772b-135">**barra**</span><span class="sxs-lookup"><span data-stu-id="2772b-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="2772b-136">4</span><span class="sxs-lookup"><span data-stu-id="2772b-136">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="2772b-137">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="2772b-137">Minimum Shader Model</span></span>

<span data-ttu-id="2772b-138">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="2772b-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="2772b-139">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="2772b-139">Shader Model</span></span>                                              | <span data-ttu-id="2772b-140">Com suporte</span><span class="sxs-lookup"><span data-stu-id="2772b-140">Supported</span></span>                                                                                                                         |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2772b-141">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="2772b-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="2772b-142">Sim (somente sombreador de pixel), mas você deve usar a [opção de compilação herdada](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax) ao compilar.</span><span class="sxs-lookup"><span data-stu-id="2772b-142">yes (pixel shader only), but you must use the [legacy compile option](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax) when compiling.</span></span> |
| [<span data-ttu-id="2772b-143">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2772b-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="2772b-144">Sim (somente sombreador de pixel)</span><span class="sxs-lookup"><span data-stu-id="2772b-144">yes (pixel shader only)</span></span>                                                                                                           |
| [<span data-ttu-id="2772b-145">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2772b-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="2772b-146">Sim (somente sombreador de pixel)</span><span class="sxs-lookup"><span data-stu-id="2772b-146">yes (pixel shader only)</span></span>                                                                                                           |
| [<span data-ttu-id="2772b-147">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2772b-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="2772b-148">Sim (somente sombreador de pixel)</span><span class="sxs-lookup"><span data-stu-id="2772b-148">yes (pixel shader only)</span></span>                                                                                                           |



 

## <a name="see-also"></a><span data-ttu-id="2772b-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="2772b-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2772b-150">**Funções intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="2772b-150">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

