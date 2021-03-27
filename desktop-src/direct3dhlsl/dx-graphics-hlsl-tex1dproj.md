---
title: tex1Dproj
description: Amostras de uma textura 1D usando uma divisão projetada; a coordenada de textura é dividida por t. w antes que a pesquisa ocorra.
ms.assetid: 7cfe996d-3967-40da-b0e7-e03938478594
keywords:
- tex1Dproj HLSL
topic_type:
- apiref
api_name:
- tex1Dproj
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 34fc1c019ab5479fe8a23446c94073e19ca68de7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104967208"
---
# <a name="tex1dproj"></a><span data-ttu-id="a0c25-104">tex1Dproj</span><span class="sxs-lookup"><span data-stu-id="a0c25-104">tex1Dproj</span></span>

<span data-ttu-id="a0c25-105">Amostras de uma textura 1D usando uma divisão projetada; a coordenada de textura é dividida por t. w antes que a pesquisa ocorra.</span><span class="sxs-lookup"><span data-stu-id="a0c25-105">Samples a 1D texture using a projective divide; the texture coordinate is divided by t.w before the lookup takes place.</span></span>



| <span data-ttu-id="a0c25-106">RET tex1Dproj (s, t)</span><span class="sxs-lookup"><span data-stu-id="a0c25-106">ret tex1Dproj(s, t)</span></span> |
|---------------------|



 

## <a name="parameters"></a><span data-ttu-id="a0c25-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a0c25-107">Parameters</span></span>



| <span data-ttu-id="a0c25-108">Item</span><span class="sxs-lookup"><span data-stu-id="a0c25-108">Item</span></span>                                                   | <span data-ttu-id="a0c25-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="a0c25-109">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="a0c25-110"><span id="s"></span><span id="S"></span>*&*</span><span class="sxs-lookup"><span data-stu-id="a0c25-110"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="a0c25-111">\[no \] estado de amostra.</span><span class="sxs-lookup"><span data-stu-id="a0c25-111">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="a0c25-112"><span id="t"></span><span id="T"></span>*t*</span><span class="sxs-lookup"><span data-stu-id="a0c25-112"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="a0c25-113">\[na \] coordenada de textura.</span><span class="sxs-lookup"><span data-stu-id="a0c25-113">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="a0c25-114">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="a0c25-114">Return Value</span></span>

<span data-ttu-id="a0c25-115">O valor dos dados de textura.</span><span class="sxs-lookup"><span data-stu-id="a0c25-115">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="a0c25-116">Descrição do tipo</span><span class="sxs-lookup"><span data-stu-id="a0c25-116">Type Description</span></span>



| <span data-ttu-id="a0c25-117">Name</span><span class="sxs-lookup"><span data-stu-id="a0c25-117">Name</span></span> | <span data-ttu-id="a0c25-118">Entrada/saída</span><span class="sxs-lookup"><span data-stu-id="a0c25-118">In/Out</span></span> | [<span data-ttu-id="a0c25-119">**Tipo de modelo**</span><span class="sxs-lookup"><span data-stu-id="a0c25-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="a0c25-120">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="a0c25-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="a0c25-121">Tamanho</span><span class="sxs-lookup"><span data-stu-id="a0c25-121">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="a0c25-122">s</span><span class="sxs-lookup"><span data-stu-id="a0c25-122">s</span></span>    | <span data-ttu-id="a0c25-123">in</span><span class="sxs-lookup"><span data-stu-id="a0c25-123">in</span></span>     | [<span data-ttu-id="a0c25-124">**objeto**</span><span class="sxs-lookup"><span data-stu-id="a0c25-124">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="a0c25-125">sampler1D</span><span class="sxs-lookup"><span data-stu-id="a0c25-125">sampler1D</span></span>](dx-graphics-hlsl-sampler.md)                      | <span data-ttu-id="a0c25-126">1</span><span class="sxs-lookup"><span data-stu-id="a0c25-126">1</span></span>    |
| <span data-ttu-id="a0c25-127">t</span><span class="sxs-lookup"><span data-stu-id="a0c25-127">t</span></span>    | <span data-ttu-id="a0c25-128">in</span><span class="sxs-lookup"><span data-stu-id="a0c25-128">in</span></span>     | [<span data-ttu-id="a0c25-129">**vetor**</span><span class="sxs-lookup"><span data-stu-id="a0c25-129">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="a0c25-130">**barra**</span><span class="sxs-lookup"><span data-stu-id="a0c25-130">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="a0c25-131">4</span><span class="sxs-lookup"><span data-stu-id="a0c25-131">4</span></span>    |
| <span data-ttu-id="a0c25-132">RET</span><span class="sxs-lookup"><span data-stu-id="a0c25-132">ret</span></span>  | <span data-ttu-id="a0c25-133">out</span><span class="sxs-lookup"><span data-stu-id="a0c25-133">out</span></span>    | [<span data-ttu-id="a0c25-134">**vetor**</span><span class="sxs-lookup"><span data-stu-id="a0c25-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="a0c25-135">**barra**</span><span class="sxs-lookup"><span data-stu-id="a0c25-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="a0c25-136">4</span><span class="sxs-lookup"><span data-stu-id="a0c25-136">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="a0c25-137">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="a0c25-137">Minimum Shader Model</span></span>

<span data-ttu-id="a0c25-138">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="a0c25-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="a0c25-139">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="a0c25-139">Shader Model</span></span>                                              | <span data-ttu-id="a0c25-140">Com suporte</span><span class="sxs-lookup"><span data-stu-id="a0c25-140">Supported</span></span>               |
|-----------------------------------------------------------|-------------------------|
| [<span data-ttu-id="a0c25-141">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="a0c25-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="a0c25-142">Sim (somente sombreador de pixel)</span><span class="sxs-lookup"><span data-stu-id="a0c25-142">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="a0c25-143">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a0c25-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="a0c25-144">Sim (somente sombreador de pixel)</span><span class="sxs-lookup"><span data-stu-id="a0c25-144">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="a0c25-145">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a0c25-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="a0c25-146">Sim (somente sombreador de pixel)</span><span class="sxs-lookup"><span data-stu-id="a0c25-146">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="a0c25-147">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a0c25-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="a0c25-148">não</span><span class="sxs-lookup"><span data-stu-id="a0c25-148">no</span></span>                      |



 

## <a name="see-also"></a><span data-ttu-id="a0c25-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="a0c25-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0c25-150">**Funções intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="a0c25-150">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

