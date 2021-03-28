---
title: texCUBEgrad
description: Amostra uma textura de cubo usando um gradiente para selecionar o nível de MIP. | texCUBEgrad
ms.assetid: ebc5e38a-e314-43b0-9a00-7e4147e24bf0
keywords:
- texCUBEgrad HLSL
topic_type:
- apiref
api_name:
- texCUBEgrad
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 694382488754c221c59df72112678a5971e62c0b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104011994"
---
# <a name="texcubegrad"></a><span data-ttu-id="ca7e7-105">texCUBEgrad</span><span class="sxs-lookup"><span data-stu-id="ca7e7-105">texCUBEgrad</span></span>

<span data-ttu-id="ca7e7-106">Amostra uma textura de cubo usando um gradiente para selecionar o nível de MIP.</span><span class="sxs-lookup"><span data-stu-id="ca7e7-106">Samples a cube texture using a gradient to select the mip level.</span></span>



| <span data-ttu-id="ca7e7-107">RET texCUBEgrad (s, t, campo DDX, ddy)</span><span class="sxs-lookup"><span data-stu-id="ca7e7-107">ret texCUBEgrad(s, t, ddx, ddy)</span></span> |
|---------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="ca7e7-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ca7e7-108">Parameters</span></span>



| <span data-ttu-id="ca7e7-109">Item</span><span class="sxs-lookup"><span data-stu-id="ca7e7-109">Item</span></span>                                                         | <span data-ttu-id="ca7e7-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="ca7e7-110">Description</span></span>                                                                  |
|--------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="ca7e7-111"><span id="s"></span><span id="S"></span>*&*</span><span class="sxs-lookup"><span data-stu-id="ca7e7-111"><span id="s"></span><span id="S"></span>*s*</span></span><br/>       | <span data-ttu-id="ca7e7-112">\[no \] estado de amostra.</span><span class="sxs-lookup"><span data-stu-id="ca7e7-112">\[in\] The sampler state.</span></span><br/>                                         |
| <span data-ttu-id="ca7e7-113"><span id="t"></span><span id="T"></span>*t*</span><span class="sxs-lookup"><span data-stu-id="ca7e7-113"><span id="t"></span><span id="T"></span>*t*</span></span><br/>       | <span data-ttu-id="ca7e7-114">\[na \] coordenada de textura.</span><span class="sxs-lookup"><span data-stu-id="ca7e7-114">\[in\] The texture coordinate.</span></span><br/>                                    |
| <span data-ttu-id="ca7e7-115"><span id="ddx"></span><span id="DDX"></span>*campo DDX*</span><span class="sxs-lookup"><span data-stu-id="ca7e7-115"><span id="ddx"></span><span id="DDX"></span>*ddx*</span></span><br/> | <span data-ttu-id="ca7e7-116">\[em \] taxa de alteração da geometria da superfície na direção x.</span><span class="sxs-lookup"><span data-stu-id="ca7e7-116">\[in\] Rate of change of the surface geometry in the x direction.</span></span><br/> |
| <span data-ttu-id="ca7e7-117"><span id="ddy"></span><span id="DDY"></span>*ddy*</span><span class="sxs-lookup"><span data-stu-id="ca7e7-117"><span id="ddy"></span><span id="DDY"></span>*ddy*</span></span><br/> | <span data-ttu-id="ca7e7-118">\[em \] taxa de alteração da geometria da superfície na direção y.</span><span class="sxs-lookup"><span data-stu-id="ca7e7-118">\[in\] Rate of change of the surface geometry in the y direction.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="ca7e7-119">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="ca7e7-119">Return Value</span></span>

<span data-ttu-id="ca7e7-120">O valor dos dados de textura.</span><span class="sxs-lookup"><span data-stu-id="ca7e7-120">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="ca7e7-121">Descrição do tipo</span><span class="sxs-lookup"><span data-stu-id="ca7e7-121">Type Description</span></span>



| <span data-ttu-id="ca7e7-122">Name</span><span class="sxs-lookup"><span data-stu-id="ca7e7-122">Name</span></span> | <span data-ttu-id="ca7e7-123">Entrada/saída</span><span class="sxs-lookup"><span data-stu-id="ca7e7-123">In/Out</span></span> | [<span data-ttu-id="ca7e7-124">**Tipo de modelo**</span><span class="sxs-lookup"><span data-stu-id="ca7e7-124">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="ca7e7-125">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="ca7e7-125">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="ca7e7-126">Tamanho</span><span class="sxs-lookup"><span data-stu-id="ca7e7-126">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="ca7e7-127">s</span><span class="sxs-lookup"><span data-stu-id="ca7e7-127">s</span></span>    | <span data-ttu-id="ca7e7-128">in</span><span class="sxs-lookup"><span data-stu-id="ca7e7-128">in</span></span>     | [<span data-ttu-id="ca7e7-129">**objeto**</span><span class="sxs-lookup"><span data-stu-id="ca7e7-129">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="ca7e7-130">samplerCUBE</span><span class="sxs-lookup"><span data-stu-id="ca7e7-130">samplerCUBE</span></span>](dx-graphics-hlsl-sampler.md)                    | <span data-ttu-id="ca7e7-131">1</span><span class="sxs-lookup"><span data-stu-id="ca7e7-131">1</span></span>    |
| <span data-ttu-id="ca7e7-132">t</span><span class="sxs-lookup"><span data-stu-id="ca7e7-132">t</span></span>    | <span data-ttu-id="ca7e7-133">in</span><span class="sxs-lookup"><span data-stu-id="ca7e7-133">in</span></span>     | [<span data-ttu-id="ca7e7-134">**vetor**</span><span class="sxs-lookup"><span data-stu-id="ca7e7-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="ca7e7-135">**barra**</span><span class="sxs-lookup"><span data-stu-id="ca7e7-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="ca7e7-136">3</span><span class="sxs-lookup"><span data-stu-id="ca7e7-136">3</span></span>    |
| <span data-ttu-id="ca7e7-137">campo DDX</span><span class="sxs-lookup"><span data-stu-id="ca7e7-137">ddx</span></span>  | <span data-ttu-id="ca7e7-138">in</span><span class="sxs-lookup"><span data-stu-id="ca7e7-138">in</span></span>     | [<span data-ttu-id="ca7e7-139">**vetor**</span><span class="sxs-lookup"><span data-stu-id="ca7e7-139">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="ca7e7-140">**barra**</span><span class="sxs-lookup"><span data-stu-id="ca7e7-140">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="ca7e7-141">3</span><span class="sxs-lookup"><span data-stu-id="ca7e7-141">3</span></span>    |
| <span data-ttu-id="ca7e7-142">ddy</span><span class="sxs-lookup"><span data-stu-id="ca7e7-142">ddy</span></span>  | <span data-ttu-id="ca7e7-143">in</span><span class="sxs-lookup"><span data-stu-id="ca7e7-143">in</span></span>     | [<span data-ttu-id="ca7e7-144">**vetor**</span><span class="sxs-lookup"><span data-stu-id="ca7e7-144">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="ca7e7-145">**barra**</span><span class="sxs-lookup"><span data-stu-id="ca7e7-145">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="ca7e7-146">3</span><span class="sxs-lookup"><span data-stu-id="ca7e7-146">3</span></span>    |
| <span data-ttu-id="ca7e7-147">RET</span><span class="sxs-lookup"><span data-stu-id="ca7e7-147">ret</span></span>  | <span data-ttu-id="ca7e7-148">out</span><span class="sxs-lookup"><span data-stu-id="ca7e7-148">out</span></span>    | [<span data-ttu-id="ca7e7-149">**vetor**</span><span class="sxs-lookup"><span data-stu-id="ca7e7-149">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="ca7e7-150">**barra**</span><span class="sxs-lookup"><span data-stu-id="ca7e7-150">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="ca7e7-151">4</span><span class="sxs-lookup"><span data-stu-id="ca7e7-151">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="ca7e7-152">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="ca7e7-152">Minimum Shader Model</span></span>

<span data-ttu-id="ca7e7-153">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="ca7e7-153">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="ca7e7-154">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="ca7e7-154">Shader Model</span></span>                                              | <span data-ttu-id="ca7e7-155">Com suporte</span><span class="sxs-lookup"><span data-stu-id="ca7e7-155">Supported</span></span>                |
|-----------------------------------------------------------|--------------------------|
| [<span data-ttu-id="ca7e7-156">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="ca7e7-156">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="ca7e7-157">Sim (somente sombreador de pixel)</span><span class="sxs-lookup"><span data-stu-id="ca7e7-157">yes (pixel shader only)</span></span>  |
| [<span data-ttu-id="ca7e7-158">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ca7e7-158">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="ca7e7-159">Sim (somente sombreador de pixel)</span><span class="sxs-lookup"><span data-stu-id="ca7e7-159">yes  (pixel shader only)</span></span> |
| [<span data-ttu-id="ca7e7-160">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ca7e7-160">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="ca7e7-161">Sim (somente sombreador de pixel)</span><span class="sxs-lookup"><span data-stu-id="ca7e7-161">yes  (pixel shader only)</span></span> |
| [<span data-ttu-id="ca7e7-162">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ca7e7-162">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="ca7e7-163">não</span><span class="sxs-lookup"><span data-stu-id="ca7e7-163">no</span></span>                       |



 

1.  <span data-ttu-id="ca7e7-164">A reordenação de código significativa é feita para mover computações de gradiente fora do controle de fluxo.</span><span class="sxs-lookup"><span data-stu-id="ca7e7-164">Significant code reordering is done to move gradient computations outside of flow control.</span></span>
2.  <span data-ttu-id="ca7e7-165">Se o limite de D3DPSHADERCAPS2 \_ 0 for definido com D3DD3DPSHADERCAPS2 \_ 0 \_ GRADIENTINSTRUCTIONS, o compilador mapeará essa função para texldd.</span><span class="sxs-lookup"><span data-stu-id="ca7e7-165">If the D3DPSHADERCAPS2\_0 cap is set with D3DD3DPSHADERCAPS2\_0\_GRADIENTINSTRUCTIONS, the compiler maps this function to texldd.</span></span>

## <a name="see-also"></a><span data-ttu-id="ca7e7-166">Confira também</span><span class="sxs-lookup"><span data-stu-id="ca7e7-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca7e7-167">**Funções intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="ca7e7-167">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

