---
title: tex2Dproj
description: Amostras de uma textura 2D usando uma divisão projetada; a coordenada de textura é dividida por t. w antes que a pesquisa ocorra.
ms.assetid: c6b79360-3737-4b74-bdf3-6d46323e8e54
keywords:
- tex2Dproj HLSL
topic_type:
- apiref
api_name:
- tex2Dproj
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 365401e4e4eca8703207ffb5c7676748f4a06d30
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104499070"
---
# <a name="tex2dproj"></a><span data-ttu-id="712ae-104">tex2Dproj</span><span class="sxs-lookup"><span data-stu-id="712ae-104">tex2Dproj</span></span>

<span data-ttu-id="712ae-105">Amostras de uma textura 2D usando uma divisão projetada; a coordenada de textura é dividida por t. w antes que a pesquisa ocorra.</span><span class="sxs-lookup"><span data-stu-id="712ae-105">Samples a 2D texture using a projective divide; the texture coordinate is divided by t.w before the lookup takes place.</span></span>



| <span data-ttu-id="712ae-106">RET tex2Dproj (s, t)</span><span class="sxs-lookup"><span data-stu-id="712ae-106">ret tex2Dproj(s, t)</span></span> |
|---------------------|



 

## <a name="parameters"></a><span data-ttu-id="712ae-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="712ae-107">Parameters</span></span>



| <span data-ttu-id="712ae-108">Item</span><span class="sxs-lookup"><span data-stu-id="712ae-108">Item</span></span>                                                   | <span data-ttu-id="712ae-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="712ae-109">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="712ae-110"><span id="s"></span><span id="S"></span>*&*</span><span class="sxs-lookup"><span data-stu-id="712ae-110"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="712ae-111">\[no \] estado de amostra.</span><span class="sxs-lookup"><span data-stu-id="712ae-111">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="712ae-112"><span id="t"></span><span id="T"></span>*t*</span><span class="sxs-lookup"><span data-stu-id="712ae-112"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="712ae-113">\[na \] coordenada de textura.</span><span class="sxs-lookup"><span data-stu-id="712ae-113">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="712ae-114">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="712ae-114">Return Value</span></span>

<span data-ttu-id="712ae-115">O valor dos dados de textura.</span><span class="sxs-lookup"><span data-stu-id="712ae-115">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="712ae-116">Descrição do tipo</span><span class="sxs-lookup"><span data-stu-id="712ae-116">Type Description</span></span>



| <span data-ttu-id="712ae-117">Name</span><span class="sxs-lookup"><span data-stu-id="712ae-117">Name</span></span> | <span data-ttu-id="712ae-118">Entrada/saída</span><span class="sxs-lookup"><span data-stu-id="712ae-118">In/Out</span></span> | [<span data-ttu-id="712ae-119">**Tipo de modelo**</span><span class="sxs-lookup"><span data-stu-id="712ae-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="712ae-120">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="712ae-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="712ae-121">Tamanho</span><span class="sxs-lookup"><span data-stu-id="712ae-121">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="712ae-122">s</span><span class="sxs-lookup"><span data-stu-id="712ae-122">s</span></span>    | <span data-ttu-id="712ae-123">in</span><span class="sxs-lookup"><span data-stu-id="712ae-123">in</span></span>     | [<span data-ttu-id="712ae-124">**objeto**</span><span class="sxs-lookup"><span data-stu-id="712ae-124">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="712ae-125">sampler2D</span><span class="sxs-lookup"><span data-stu-id="712ae-125">sampler2D</span></span>](dx-graphics-hlsl-sampler.md)                      | <span data-ttu-id="712ae-126">1</span><span class="sxs-lookup"><span data-stu-id="712ae-126">1</span></span>    |
| <span data-ttu-id="712ae-127">t</span><span class="sxs-lookup"><span data-stu-id="712ae-127">t</span></span>    | <span data-ttu-id="712ae-128">in</span><span class="sxs-lookup"><span data-stu-id="712ae-128">in</span></span>     | [<span data-ttu-id="712ae-129">**vetor**</span><span class="sxs-lookup"><span data-stu-id="712ae-129">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="712ae-130">**barra**</span><span class="sxs-lookup"><span data-stu-id="712ae-130">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="712ae-131">4</span><span class="sxs-lookup"><span data-stu-id="712ae-131">4</span></span>    |
| <span data-ttu-id="712ae-132">RET</span><span class="sxs-lookup"><span data-stu-id="712ae-132">ret</span></span>  | <span data-ttu-id="712ae-133">out</span><span class="sxs-lookup"><span data-stu-id="712ae-133">out</span></span>    | [<span data-ttu-id="712ae-134">**vetor**</span><span class="sxs-lookup"><span data-stu-id="712ae-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="712ae-135">**barra**</span><span class="sxs-lookup"><span data-stu-id="712ae-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="712ae-136">4</span><span class="sxs-lookup"><span data-stu-id="712ae-136">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="712ae-137">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="712ae-137">Minimum Shader Model</span></span>

<span data-ttu-id="712ae-138">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="712ae-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="712ae-139">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="712ae-139">Shader Model</span></span>                                              | <span data-ttu-id="712ae-140">Com suporte</span><span class="sxs-lookup"><span data-stu-id="712ae-140">Supported</span></span>               |
|-----------------------------------------------------------|-------------------------|
| [<span data-ttu-id="712ae-141">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="712ae-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="712ae-142">Sim (somente sombreador de pixel)</span><span class="sxs-lookup"><span data-stu-id="712ae-142">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="712ae-143">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="712ae-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="712ae-144">Sim (somente sombreador de pixel)</span><span class="sxs-lookup"><span data-stu-id="712ae-144">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="712ae-145">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="712ae-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="712ae-146">Sim (somente sombreador de pixel)</span><span class="sxs-lookup"><span data-stu-id="712ae-146">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="712ae-147">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="712ae-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="712ae-148">não</span><span class="sxs-lookup"><span data-stu-id="712ae-148">no</span></span>                      |



 

## <a name="see-also"></a><span data-ttu-id="712ae-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="712ae-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="712ae-150">**Funções intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="712ae-150">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

