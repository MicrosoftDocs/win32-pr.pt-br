---
title: texCUBE (referência de HLSL)
description: Amostra uma textura de cubo.
ms.assetid: 77943eb9-86e8-4ae4-8975-8f925e084ce4
keywords:
- texCUBE HLSL
topic_type:
- apiref
api_name:
- texCUBE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 524ed44028372eeabf176c30da8b3a31a8ee7988
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007680"
---
# <a name="texcube-hlsl-reference"></a><span data-ttu-id="b8c84-104">texCUBE (referência de HLSL)</span><span class="sxs-lookup"><span data-stu-id="b8c84-104">texCUBE (HLSL reference)</span></span>

<span data-ttu-id="b8c84-105">Amostra uma textura de cubo.</span><span class="sxs-lookup"><span data-stu-id="b8c84-105">Samples a cube texture.</span></span>



| <span data-ttu-id="b8c84-106">RET texCUBE (s, t)</span><span class="sxs-lookup"><span data-stu-id="b8c84-106">ret texCUBE(s, t)</span></span> |
|-------------------|



 

## <a name="parameters"></a><span data-ttu-id="b8c84-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b8c84-107">Parameters</span></span>



| <span data-ttu-id="b8c84-108">Item</span><span class="sxs-lookup"><span data-stu-id="b8c84-108">Item</span></span>                                                   | <span data-ttu-id="b8c84-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="b8c84-109">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="b8c84-110"><span id="s"></span><span id="S"></span>*&*</span><span class="sxs-lookup"><span data-stu-id="b8c84-110"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="b8c84-111">\[no \] estado de amostra.</span><span class="sxs-lookup"><span data-stu-id="b8c84-111">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="b8c84-112"><span id="t"></span><span id="T"></span>*t*</span><span class="sxs-lookup"><span data-stu-id="b8c84-112"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="b8c84-113">\[na \] coordenada de textura.</span><span class="sxs-lookup"><span data-stu-id="b8c84-113">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="b8c84-114">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="b8c84-114">Return Value</span></span>

<span data-ttu-id="b8c84-115">O valor dos dados de textura.</span><span class="sxs-lookup"><span data-stu-id="b8c84-115">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="b8c84-116">Descrição do tipo</span><span class="sxs-lookup"><span data-stu-id="b8c84-116">Type Description</span></span>



| <span data-ttu-id="b8c84-117">Name</span><span class="sxs-lookup"><span data-stu-id="b8c84-117">Name</span></span> | <span data-ttu-id="b8c84-118">Entrada/saída</span><span class="sxs-lookup"><span data-stu-id="b8c84-118">In/Out</span></span> | [<span data-ttu-id="b8c84-119">**Tipo de modelo**</span><span class="sxs-lookup"><span data-stu-id="b8c84-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="b8c84-120">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="b8c84-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="b8c84-121">Tamanho</span><span class="sxs-lookup"><span data-stu-id="b8c84-121">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="b8c84-122">s</span><span class="sxs-lookup"><span data-stu-id="b8c84-122">s</span></span>    | <span data-ttu-id="b8c84-123">in</span><span class="sxs-lookup"><span data-stu-id="b8c84-123">in</span></span>     | [<span data-ttu-id="b8c84-124">**objeto**</span><span class="sxs-lookup"><span data-stu-id="b8c84-124">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="b8c84-125">samplerCUBE</span><span class="sxs-lookup"><span data-stu-id="b8c84-125">samplerCUBE</span></span>](dx-graphics-hlsl-sampler.md)                    | <span data-ttu-id="b8c84-126">1</span><span class="sxs-lookup"><span data-stu-id="b8c84-126">1</span></span>    |
| <span data-ttu-id="b8c84-127">t</span><span class="sxs-lookup"><span data-stu-id="b8c84-127">t</span></span>    | <span data-ttu-id="b8c84-128">in</span><span class="sxs-lookup"><span data-stu-id="b8c84-128">in</span></span>     | [<span data-ttu-id="b8c84-129">**vetor**</span><span class="sxs-lookup"><span data-stu-id="b8c84-129">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="b8c84-130">**barra**</span><span class="sxs-lookup"><span data-stu-id="b8c84-130">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="b8c84-131">3</span><span class="sxs-lookup"><span data-stu-id="b8c84-131">3</span></span>    |
| <span data-ttu-id="b8c84-132">RET</span><span class="sxs-lookup"><span data-stu-id="b8c84-132">ret</span></span>  | <span data-ttu-id="b8c84-133">out</span><span class="sxs-lookup"><span data-stu-id="b8c84-133">out</span></span>    | [<span data-ttu-id="b8c84-134">**vetor**</span><span class="sxs-lookup"><span data-stu-id="b8c84-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="b8c84-135">**barra**</span><span class="sxs-lookup"><span data-stu-id="b8c84-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="b8c84-136">4</span><span class="sxs-lookup"><span data-stu-id="b8c84-136">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="b8c84-137">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="b8c84-137">Minimum Shader Model</span></span>

<span data-ttu-id="b8c84-138">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="b8c84-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="b8c84-139">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="b8c84-139">Shader Model</span></span>                                              | <span data-ttu-id="b8c84-140">Com suporte</span><span class="sxs-lookup"><span data-stu-id="b8c84-140">Supported</span></span>               |
|-----------------------------------------------------------|-------------------------|
| [<span data-ttu-id="b8c84-141">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="b8c84-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="b8c84-142">Sim (somente sombreador de pixel)</span><span class="sxs-lookup"><span data-stu-id="b8c84-142">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="b8c84-143">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b8c84-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="b8c84-144">Sim (somente sombreador de pixel)</span><span class="sxs-lookup"><span data-stu-id="b8c84-144">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="b8c84-145">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b8c84-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="b8c84-146">Sim (somente sombreador de pixel)</span><span class="sxs-lookup"><span data-stu-id="b8c84-146">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="b8c84-147">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b8c84-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="b8c84-148">Sim (somente sombreador de pixel)</span><span class="sxs-lookup"><span data-stu-id="b8c84-148">yes (pixel shader only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="b8c84-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="b8c84-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8c84-150">**Funções intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="b8c84-150">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

