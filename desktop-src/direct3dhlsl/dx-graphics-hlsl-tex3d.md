---
title: tex3D (referência de HLSL)
description: Amostras de uma textura 3D.
ms.assetid: 713eec24-bdf5-456e-98da-30e2c9d7e808
keywords:
- tex3D HLSL
topic_type:
- apiref
api_name:
- tex3D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e3a071d00dedabdff02bae302c71aa8ecece4ba2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641654"
---
# <a name="tex3d-hlsl-reference"></a><span data-ttu-id="39c1a-104">tex3D (referência de HLSL)</span><span class="sxs-lookup"><span data-stu-id="39c1a-104">tex3D (HLSL reference)</span></span>

<span data-ttu-id="39c1a-105">Amostras de uma textura 3D.</span><span class="sxs-lookup"><span data-stu-id="39c1a-105">Samples a 3D texture.</span></span>



| <span data-ttu-id="39c1a-106">RET tex3D (s, t)</span><span class="sxs-lookup"><span data-stu-id="39c1a-106">ret tex3D(s, t)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="39c1a-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="39c1a-107">Parameters</span></span>



| <span data-ttu-id="39c1a-108">Item</span><span class="sxs-lookup"><span data-stu-id="39c1a-108">Item</span></span>                                                   | <span data-ttu-id="39c1a-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="39c1a-109">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="39c1a-110"><span id="s"></span><span id="S"></span>*&*</span><span class="sxs-lookup"><span data-stu-id="39c1a-110"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="39c1a-111">\[no \] estado de amostra.</span><span class="sxs-lookup"><span data-stu-id="39c1a-111">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="39c1a-112"><span id="t"></span><span id="T"></span>*t*</span><span class="sxs-lookup"><span data-stu-id="39c1a-112"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="39c1a-113">\[na \] coordenada de textura.</span><span class="sxs-lookup"><span data-stu-id="39c1a-113">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="39c1a-114">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="39c1a-114">Return Value</span></span>

<span data-ttu-id="39c1a-115">O valor dos dados de textura.</span><span class="sxs-lookup"><span data-stu-id="39c1a-115">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="39c1a-116">Descrição do tipo</span><span class="sxs-lookup"><span data-stu-id="39c1a-116">Type Description</span></span>



| <span data-ttu-id="39c1a-117">Name</span><span class="sxs-lookup"><span data-stu-id="39c1a-117">Name</span></span> | <span data-ttu-id="39c1a-118">Entrada/saída</span><span class="sxs-lookup"><span data-stu-id="39c1a-118">In/Out</span></span> | [<span data-ttu-id="39c1a-119">**Tipo de modelo**</span><span class="sxs-lookup"><span data-stu-id="39c1a-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="39c1a-120">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="39c1a-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="39c1a-121">Tamanho</span><span class="sxs-lookup"><span data-stu-id="39c1a-121">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="39c1a-122">s</span><span class="sxs-lookup"><span data-stu-id="39c1a-122">s</span></span>    | <span data-ttu-id="39c1a-123">in</span><span class="sxs-lookup"><span data-stu-id="39c1a-123">in</span></span>     | [<span data-ttu-id="39c1a-124">**objeto**</span><span class="sxs-lookup"><span data-stu-id="39c1a-124">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="39c1a-125">sampler3D</span><span class="sxs-lookup"><span data-stu-id="39c1a-125">sampler3D</span></span>](dx-graphics-hlsl-sampler.md)                      | <span data-ttu-id="39c1a-126">1</span><span class="sxs-lookup"><span data-stu-id="39c1a-126">1</span></span>    |
| <span data-ttu-id="39c1a-127">t</span><span class="sxs-lookup"><span data-stu-id="39c1a-127">t</span></span>    | <span data-ttu-id="39c1a-128">in</span><span class="sxs-lookup"><span data-stu-id="39c1a-128">in</span></span>     | [<span data-ttu-id="39c1a-129">**vetor**</span><span class="sxs-lookup"><span data-stu-id="39c1a-129">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="39c1a-130">**barra**</span><span class="sxs-lookup"><span data-stu-id="39c1a-130">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="39c1a-131">3</span><span class="sxs-lookup"><span data-stu-id="39c1a-131">3</span></span>    |
| <span data-ttu-id="39c1a-132">RET</span><span class="sxs-lookup"><span data-stu-id="39c1a-132">ret</span></span>  | <span data-ttu-id="39c1a-133">out</span><span class="sxs-lookup"><span data-stu-id="39c1a-133">out</span></span>    | [<span data-ttu-id="39c1a-134">**vetor**</span><span class="sxs-lookup"><span data-stu-id="39c1a-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="39c1a-135">**barra**</span><span class="sxs-lookup"><span data-stu-id="39c1a-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="39c1a-136">4</span><span class="sxs-lookup"><span data-stu-id="39c1a-136">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="39c1a-137">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="39c1a-137">Minimum Shader Model</span></span>

<span data-ttu-id="39c1a-138">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="39c1a-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="39c1a-139">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="39c1a-139">Shader Model</span></span>                                              | <span data-ttu-id="39c1a-140">Com suporte</span><span class="sxs-lookup"><span data-stu-id="39c1a-140">Supported</span></span>                                                                                                                         |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="39c1a-141">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="39c1a-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="39c1a-142">Sim (somente sombreador de pixel), mas você deve usar a [opção de compilação herdada](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax) ao compilar.</span><span class="sxs-lookup"><span data-stu-id="39c1a-142">yes (pixel shader only), but you must use the [legacy compile option](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax) when compiling.</span></span> |
| [<span data-ttu-id="39c1a-143">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="39c1a-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="39c1a-144">Sim (somente sombreador de pixel)</span><span class="sxs-lookup"><span data-stu-id="39c1a-144">yes (pixel shader only)</span></span>                                                                                                           |
| [<span data-ttu-id="39c1a-145">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="39c1a-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="39c1a-146">Sim (somente sombreador de pixel)</span><span class="sxs-lookup"><span data-stu-id="39c1a-146">yes (pixel shader only)</span></span>                                                                                                           |
| [<span data-ttu-id="39c1a-147">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="39c1a-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="39c1a-148">Sim (somente sombreador de pixel)</span><span class="sxs-lookup"><span data-stu-id="39c1a-148">yes (pixel shader only)</span></span>                                                                                                           |



 

## <a name="see-also"></a><span data-ttu-id="39c1a-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="39c1a-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39c1a-150">**Funções intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="39c1a-150">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

