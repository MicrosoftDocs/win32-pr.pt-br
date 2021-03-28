---
title: texCUBE (referência de HLSL) – Selecione o nível de MIP
description: Amostra uma textura de cubo usando um gradiente para selecionar o nível de MIP. | texCUBE (referência de HLSL)
ms.assetid: 5615f48b-eb0a-4de7-a441-51ec3cecf6fd
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
ms.openlocfilehash: 6286b4fedb94b9fd5c84c76171e9478f06e16ce4
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104968722"
---
# <a name="texcube-hlsl-reference---select-the-mip-level"></a><span data-ttu-id="0e52a-105">texCUBE (referência de HLSL) – Selecione o nível de MIP</span><span class="sxs-lookup"><span data-stu-id="0e52a-105">texCUBE (HLSL reference) - Select the mip level</span></span>

<span data-ttu-id="0e52a-106">Amostra uma textura de cubo usando um gradiente para selecionar o nível de MIP.</span><span class="sxs-lookup"><span data-stu-id="0e52a-106">Samples a cube texture using a gradient to select the mip level.</span></span>



| <span data-ttu-id="0e52a-107">RET texCUBE (s, t, campo DDX, ddy)</span><span class="sxs-lookup"><span data-stu-id="0e52a-107">ret texCUBE(s, t, ddx, ddy)</span></span> |
|-----------------------------|



 

## <a name="parameters"></a><span data-ttu-id="0e52a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0e52a-108">Parameters</span></span>



| <span data-ttu-id="0e52a-109">Item</span><span class="sxs-lookup"><span data-stu-id="0e52a-109">Item</span></span>                                                         | <span data-ttu-id="0e52a-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="0e52a-110">Description</span></span>                                                                  |
|--------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="0e52a-111"><span id="s"></span><span id="S"></span>*&*</span><span class="sxs-lookup"><span data-stu-id="0e52a-111"><span id="s"></span><span id="S"></span>*s*</span></span><br/>       | <span data-ttu-id="0e52a-112">\[no \] estado de amostra.</span><span class="sxs-lookup"><span data-stu-id="0e52a-112">\[in\] The sampler state.</span></span><br/>                                         |
| <span data-ttu-id="0e52a-113"><span id="t"></span><span id="T"></span>*t*</span><span class="sxs-lookup"><span data-stu-id="0e52a-113"><span id="t"></span><span id="T"></span>*t*</span></span><br/>       | <span data-ttu-id="0e52a-114">\[na \] coordenada de textura.</span><span class="sxs-lookup"><span data-stu-id="0e52a-114">\[in\] The texture coordinate.</span></span><br/>                                    |
| <span data-ttu-id="0e52a-115"><span id="ddx"></span><span id="DDX"></span>*campo DDX*</span><span class="sxs-lookup"><span data-stu-id="0e52a-115"><span id="ddx"></span><span id="DDX"></span>*ddx*</span></span><br/> | <span data-ttu-id="0e52a-116">\[em \] taxa de alteração da geometria da superfície na direção x.</span><span class="sxs-lookup"><span data-stu-id="0e52a-116">\[in\] Rate of change of the surface geometry in the x direction.</span></span><br/> |
| <span data-ttu-id="0e52a-117"><span id="ddy"></span><span id="DDY"></span>*ddy*</span><span class="sxs-lookup"><span data-stu-id="0e52a-117"><span id="ddy"></span><span id="DDY"></span>*ddy*</span></span><br/> | <span data-ttu-id="0e52a-118">\[em \] taxa de alteração da geometria da superfície na direção y.</span><span class="sxs-lookup"><span data-stu-id="0e52a-118">\[in\] Rate of change of the surface geometry in the y direction.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="0e52a-119">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="0e52a-119">Return Value</span></span>

<span data-ttu-id="0e52a-120">O valor dos dados de textura.</span><span class="sxs-lookup"><span data-stu-id="0e52a-120">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="0e52a-121">Descrição do tipo</span><span class="sxs-lookup"><span data-stu-id="0e52a-121">Type Description</span></span>



| <span data-ttu-id="0e52a-122">Name</span><span class="sxs-lookup"><span data-stu-id="0e52a-122">Name</span></span> | <span data-ttu-id="0e52a-123">Entrada/saída</span><span class="sxs-lookup"><span data-stu-id="0e52a-123">In/Out</span></span> | [<span data-ttu-id="0e52a-124">**Tipo de modelo**</span><span class="sxs-lookup"><span data-stu-id="0e52a-124">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="0e52a-125">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="0e52a-125">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="0e52a-126">Tamanho</span><span class="sxs-lookup"><span data-stu-id="0e52a-126">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="0e52a-127">s</span><span class="sxs-lookup"><span data-stu-id="0e52a-127">s</span></span>    | <span data-ttu-id="0e52a-128">in</span><span class="sxs-lookup"><span data-stu-id="0e52a-128">in</span></span>     | [<span data-ttu-id="0e52a-129">**objeto**</span><span class="sxs-lookup"><span data-stu-id="0e52a-129">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="0e52a-130">samplerCUBE</span><span class="sxs-lookup"><span data-stu-id="0e52a-130">samplerCUBE</span></span>](dx-graphics-hlsl-sampler.md)                    | <span data-ttu-id="0e52a-131">1</span><span class="sxs-lookup"><span data-stu-id="0e52a-131">1</span></span>    |
| <span data-ttu-id="0e52a-132">t</span><span class="sxs-lookup"><span data-stu-id="0e52a-132">t</span></span>    | <span data-ttu-id="0e52a-133">in</span><span class="sxs-lookup"><span data-stu-id="0e52a-133">in</span></span>     | [<span data-ttu-id="0e52a-134">**vetor**</span><span class="sxs-lookup"><span data-stu-id="0e52a-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="0e52a-135">**barra**</span><span class="sxs-lookup"><span data-stu-id="0e52a-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="0e52a-136">3</span><span class="sxs-lookup"><span data-stu-id="0e52a-136">3</span></span>    |
| <span data-ttu-id="0e52a-137">campo DDX</span><span class="sxs-lookup"><span data-stu-id="0e52a-137">ddx</span></span>  | <span data-ttu-id="0e52a-138">in</span><span class="sxs-lookup"><span data-stu-id="0e52a-138">in</span></span>     | [<span data-ttu-id="0e52a-139">**vetor**</span><span class="sxs-lookup"><span data-stu-id="0e52a-139">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="0e52a-140">**barra**</span><span class="sxs-lookup"><span data-stu-id="0e52a-140">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="0e52a-141">3</span><span class="sxs-lookup"><span data-stu-id="0e52a-141">3</span></span>    |
| <span data-ttu-id="0e52a-142">ddy</span><span class="sxs-lookup"><span data-stu-id="0e52a-142">ddy</span></span>  | <span data-ttu-id="0e52a-143">in</span><span class="sxs-lookup"><span data-stu-id="0e52a-143">in</span></span>     | [<span data-ttu-id="0e52a-144">**vetor**</span><span class="sxs-lookup"><span data-stu-id="0e52a-144">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="0e52a-145">**barra**</span><span class="sxs-lookup"><span data-stu-id="0e52a-145">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="0e52a-146">3</span><span class="sxs-lookup"><span data-stu-id="0e52a-146">3</span></span>    |
| <span data-ttu-id="0e52a-147">RET</span><span class="sxs-lookup"><span data-stu-id="0e52a-147">ret</span></span>  | <span data-ttu-id="0e52a-148">out</span><span class="sxs-lookup"><span data-stu-id="0e52a-148">out</span></span>    | [<span data-ttu-id="0e52a-149">**vetor**</span><span class="sxs-lookup"><span data-stu-id="0e52a-149">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="0e52a-150">**barra**</span><span class="sxs-lookup"><span data-stu-id="0e52a-150">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="0e52a-151">4</span><span class="sxs-lookup"><span data-stu-id="0e52a-151">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="0e52a-152">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="0e52a-152">Minimum Shader Model</span></span>

<span data-ttu-id="0e52a-153">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="0e52a-153">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="0e52a-154">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="0e52a-154">Shader Model</span></span>                                              | <span data-ttu-id="0e52a-155">Com suporte</span><span class="sxs-lookup"><span data-stu-id="0e52a-155">Supported</span></span>                |
|-----------------------------------------------------------|--------------------------|
| [<span data-ttu-id="0e52a-156">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="0e52a-156">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="0e52a-157">Sim (somente sombreador de pixel)</span><span class="sxs-lookup"><span data-stu-id="0e52a-157">yes (pixel shader only)</span></span>  |
| [<span data-ttu-id="0e52a-158">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0e52a-158">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="0e52a-159">Sim (somente sombreador de pixel)</span><span class="sxs-lookup"><span data-stu-id="0e52a-159">yes  (pixel shader only)</span></span> |
| [<span data-ttu-id="0e52a-160">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0e52a-160">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="0e52a-161">Sim (somente sombreador de pixel)</span><span class="sxs-lookup"><span data-stu-id="0e52a-161">yes  (pixel shader only)</span></span> |
| [<span data-ttu-id="0e52a-162">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0e52a-162">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="0e52a-163">não</span><span class="sxs-lookup"><span data-stu-id="0e52a-163">no</span></span>                       |



 

1.  <span data-ttu-id="0e52a-164">A reordenação de código significativa é feita para mover computações de gradiente fora do controle de fluxo.</span><span class="sxs-lookup"><span data-stu-id="0e52a-164">Significant code reordering is done to move gradient computations outside of flow control.</span></span>
2.  <span data-ttu-id="0e52a-165">Se o limite de D3DPSHADERCAPS2 \_ 0 for definido com D3DD3DPSHADERCAPS2 \_ 0 \_ GRADIENTINSTRUCTIONS, o compilador mapeará essa função para texldd.</span><span class="sxs-lookup"><span data-stu-id="0e52a-165">If the D3DPSHADERCAPS2\_0 cap is set with D3DD3DPSHADERCAPS2\_0\_GRADIENTINSTRUCTIONS, the compiler maps this function to texldd.</span></span>

## <a name="see-also"></a><span data-ttu-id="0e52a-166">Confira também</span><span class="sxs-lookup"><span data-stu-id="0e52a-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e52a-167">**Funções intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="0e52a-167">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

