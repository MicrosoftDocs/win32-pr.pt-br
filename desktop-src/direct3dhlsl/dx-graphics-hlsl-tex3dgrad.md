---
title: tex3Dgrad
description: Amostra uma textura 3D usando um gradiente para selecionar o nível de MIP. | tex3Dgrad
ms.assetid: 230c42cc-31b7-4f57-ade4-14f069094d46
keywords:
- tex3Dgrad HLSL
topic_type:
- apiref
api_name:
- tex3Dgrad
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4cd8188b7f39cc2b79eb2e961857732cd8dae9f4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968405"
---
# <a name="tex3dgrad"></a><span data-ttu-id="09c79-105">tex3Dgrad</span><span class="sxs-lookup"><span data-stu-id="09c79-105">tex3Dgrad</span></span>

<span data-ttu-id="09c79-106">Amostra uma textura 3D usando um gradiente para selecionar o nível de MIP.</span><span class="sxs-lookup"><span data-stu-id="09c79-106">Samples a 3D texture using a gradient to select the mip level.</span></span>



| <span data-ttu-id="09c79-107">RET tex3Dgrad (s, t, campo DDX, ddy)</span><span class="sxs-lookup"><span data-stu-id="09c79-107">ret tex3Dgrad(s, t, ddx, ddy)</span></span> |
|-------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="09c79-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="09c79-108">Parameters</span></span>



| <span data-ttu-id="09c79-109">Item</span><span class="sxs-lookup"><span data-stu-id="09c79-109">Item</span></span>                                                         | <span data-ttu-id="09c79-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="09c79-110">Description</span></span>                                                                  |
|--------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="09c79-111"><span id="s"></span><span id="S"></span>*&*</span><span class="sxs-lookup"><span data-stu-id="09c79-111"><span id="s"></span><span id="S"></span>*s*</span></span><br/>       | <span data-ttu-id="09c79-112">\[no \] estado de amostra.</span><span class="sxs-lookup"><span data-stu-id="09c79-112">\[in\] The sampler state.</span></span><br/>                                         |
| <span data-ttu-id="09c79-113"><span id="t"></span><span id="T"></span>*t*</span><span class="sxs-lookup"><span data-stu-id="09c79-113"><span id="t"></span><span id="T"></span>*t*</span></span><br/>       | <span data-ttu-id="09c79-114">\[na \] coordenada de textura.</span><span class="sxs-lookup"><span data-stu-id="09c79-114">\[in\] The texture coordinate.</span></span><br/>                                    |
| <span data-ttu-id="09c79-115"><span id="ddx"></span><span id="DDX"></span>*campo DDX*</span><span class="sxs-lookup"><span data-stu-id="09c79-115"><span id="ddx"></span><span id="DDX"></span>*ddx*</span></span><br/> | <span data-ttu-id="09c79-116">\[em \] taxa de alteração da geometria da superfície na direção x.</span><span class="sxs-lookup"><span data-stu-id="09c79-116">\[in\] Rate of change of the surface geometry in the x direction.</span></span><br/> |
| <span data-ttu-id="09c79-117"><span id="ddy"></span><span id="DDY"></span>*ddy*</span><span class="sxs-lookup"><span data-stu-id="09c79-117"><span id="ddy"></span><span id="DDY"></span>*ddy*</span></span><br/> | <span data-ttu-id="09c79-118">\[em \] taxa de alteração da geometria da superfície na direção y.</span><span class="sxs-lookup"><span data-stu-id="09c79-118">\[in\] Rate of change of the surface geometry in the y direction.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="09c79-119">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="09c79-119">Return Value</span></span>

<span data-ttu-id="09c79-120">O valor dos dados de textura.</span><span class="sxs-lookup"><span data-stu-id="09c79-120">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="09c79-121">Descrição do tipo</span><span class="sxs-lookup"><span data-stu-id="09c79-121">Type Description</span></span>



| <span data-ttu-id="09c79-122">Name</span><span class="sxs-lookup"><span data-stu-id="09c79-122">Name</span></span> | <span data-ttu-id="09c79-123">Entrada/saída</span><span class="sxs-lookup"><span data-stu-id="09c79-123">In/Out</span></span> | [<span data-ttu-id="09c79-124">**Tipo de modelo**</span><span class="sxs-lookup"><span data-stu-id="09c79-124">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="09c79-125">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="09c79-125">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="09c79-126">Tamanho</span><span class="sxs-lookup"><span data-stu-id="09c79-126">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="09c79-127">s</span><span class="sxs-lookup"><span data-stu-id="09c79-127">s</span></span>    | <span data-ttu-id="09c79-128">in</span><span class="sxs-lookup"><span data-stu-id="09c79-128">in</span></span>     | [<span data-ttu-id="09c79-129">**objeto**</span><span class="sxs-lookup"><span data-stu-id="09c79-129">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="09c79-130">sampler3D</span><span class="sxs-lookup"><span data-stu-id="09c79-130">sampler3D</span></span>](dx-graphics-hlsl-sampler.md)                      | <span data-ttu-id="09c79-131">1</span><span class="sxs-lookup"><span data-stu-id="09c79-131">1</span></span>    |
| <span data-ttu-id="09c79-132">t</span><span class="sxs-lookup"><span data-stu-id="09c79-132">t</span></span>    | <span data-ttu-id="09c79-133">in</span><span class="sxs-lookup"><span data-stu-id="09c79-133">in</span></span>     | [<span data-ttu-id="09c79-134">**vetor**</span><span class="sxs-lookup"><span data-stu-id="09c79-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="09c79-135">**barra**</span><span class="sxs-lookup"><span data-stu-id="09c79-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="09c79-136">3</span><span class="sxs-lookup"><span data-stu-id="09c79-136">3</span></span>    |
| <span data-ttu-id="09c79-137">campo DDX</span><span class="sxs-lookup"><span data-stu-id="09c79-137">ddx</span></span>  | <span data-ttu-id="09c79-138">in</span><span class="sxs-lookup"><span data-stu-id="09c79-138">in</span></span>     | [<span data-ttu-id="09c79-139">**vetor**</span><span class="sxs-lookup"><span data-stu-id="09c79-139">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="09c79-140">**barra**</span><span class="sxs-lookup"><span data-stu-id="09c79-140">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="09c79-141">3</span><span class="sxs-lookup"><span data-stu-id="09c79-141">3</span></span>    |
| <span data-ttu-id="09c79-142">ddy</span><span class="sxs-lookup"><span data-stu-id="09c79-142">ddy</span></span>  | <span data-ttu-id="09c79-143">in</span><span class="sxs-lookup"><span data-stu-id="09c79-143">in</span></span>     | [<span data-ttu-id="09c79-144">**vetor**</span><span class="sxs-lookup"><span data-stu-id="09c79-144">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="09c79-145">**barra**</span><span class="sxs-lookup"><span data-stu-id="09c79-145">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="09c79-146">3</span><span class="sxs-lookup"><span data-stu-id="09c79-146">3</span></span>    |
| <span data-ttu-id="09c79-147">RET</span><span class="sxs-lookup"><span data-stu-id="09c79-147">ret</span></span>  | <span data-ttu-id="09c79-148">out</span><span class="sxs-lookup"><span data-stu-id="09c79-148">out</span></span>    | [<span data-ttu-id="09c79-149">**vetor**</span><span class="sxs-lookup"><span data-stu-id="09c79-149">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="09c79-150">**barra**</span><span class="sxs-lookup"><span data-stu-id="09c79-150">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="09c79-151">4</span><span class="sxs-lookup"><span data-stu-id="09c79-151">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="09c79-152">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="09c79-152">Minimum Shader Model</span></span>

<span data-ttu-id="09c79-153">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="09c79-153">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="09c79-154">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="09c79-154">Shader Model</span></span>                                              | <span data-ttu-id="09c79-155">Com suporte</span><span class="sxs-lookup"><span data-stu-id="09c79-155">Supported</span></span>                |
|-----------------------------------------------------------|--------------------------|
| [<span data-ttu-id="09c79-156">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="09c79-156">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="09c79-157">Sim (somente sombreador de pixel)</span><span class="sxs-lookup"><span data-stu-id="09c79-157">yes (pixel shader only)</span></span>  |
| [<span data-ttu-id="09c79-158">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="09c79-158">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="09c79-159">Sim (somente sombreador de pixel)</span><span class="sxs-lookup"><span data-stu-id="09c79-159">yes  (pixel shader only)</span></span> |
| [<span data-ttu-id="09c79-160">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="09c79-160">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="09c79-161">Sim (somente sombreador de pixel)</span><span class="sxs-lookup"><span data-stu-id="09c79-161">yes  (pixel shader only)</span></span> |
| [<span data-ttu-id="09c79-162">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="09c79-162">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="09c79-163">não</span><span class="sxs-lookup"><span data-stu-id="09c79-163">no</span></span>                       |



 

1.  <span data-ttu-id="09c79-164">A reordenação de código significativa é feita para mover computações de gradiente fora do controle de fluxo.</span><span class="sxs-lookup"><span data-stu-id="09c79-164">Significant code reordering is done to move gradient computations outside of flow control.</span></span>
2.  <span data-ttu-id="09c79-165">Se o limite de D3DPSHADERCAPS2 \_ 0 for definido com D3DD3DPSHADERCAPS2 \_ 0 \_ GRADIENTINSTRUCTIONS, o compilador mapeará essa função para texldd.</span><span class="sxs-lookup"><span data-stu-id="09c79-165">If the D3DPSHADERCAPS2\_0 cap is set with D3DD3DPSHADERCAPS2\_0\_GRADIENTINSTRUCTIONS, the compiler maps this function to texldd.</span></span>

## <a name="remarks"></a><span data-ttu-id="09c79-166">Comentários</span><span class="sxs-lookup"><span data-stu-id="09c79-166">Remarks</span></span>

<span data-ttu-id="09c79-167">Quando o controle de fluxo está presente em um sombreador, o resultado de um cálculo de gradiente solicitado dentro de um determinado caminho de ramificação é ambíguo quando os pixels adjacentes podem descer os caminhos de controle de fluxo separados.</span><span class="sxs-lookup"><span data-stu-id="09c79-167">When flow control is present in a shader, the result of a gradient calculation requested inside a given branch path is ambiguous when adjacent pixels may go down separate flow control paths.</span></span> <span data-ttu-id="09c79-168">Portanto, é considerado ilegal usar qualquer operação de sombreador de pixel que solicite a ocorrência de um cálculo de gradiente em um local que esteja dentro de uma construção de controle de fluxo que pode variar em pixels para um determinado primitivo ser rasterizado.</span><span class="sxs-lookup"><span data-stu-id="09c79-168">Therefore, it is deemed illegal to use any pixel shader operation that requests a gradient calculation to occur at a location that is inside a flow control construct which could vary across pixels for a given primitive being rasterized.</span></span> <span data-ttu-id="09c79-169">Se um dos lados de uma instrução **If** com o atributo Branch usar uma função de gradiente, um erro de compilador poderá ser gerado.</span><span class="sxs-lookup"><span data-stu-id="09c79-169">If either side of an **if** statement with the branch attribute uses a gradient function a compiler error may be generated.</span></span> <span data-ttu-id="09c79-170">Consulte a [instrução if (DirectX HLSL)](dx-graphics-hlsl-if.md).</span><span class="sxs-lookup"><span data-stu-id="09c79-170">See [if Statement (DirectX HLSL)](dx-graphics-hlsl-if.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="09c79-171">Confira também</span><span class="sxs-lookup"><span data-stu-id="09c79-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09c79-172">**Funções intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="09c79-172">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

