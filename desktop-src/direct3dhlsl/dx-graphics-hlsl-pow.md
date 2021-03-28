---
title: pow
description: Retorna o valor especificado elevado à potência especificada.
ms.assetid: 1d64452c-81c7-4ef5-a332-13e0263c2cd1
keywords:
- pow HLSL
topic_type:
- apiref
api_name:
- pow
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f190c374b6c0ac42d41862eb918f0c0482b6d785
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454309"
---
# <a name="pow"></a><span data-ttu-id="7b049-104">pow</span><span class="sxs-lookup"><span data-stu-id="7b049-104">pow</span></span>

<span data-ttu-id="7b049-105">Retorna o valor especificado elevado à potência especificada.</span><span class="sxs-lookup"><span data-stu-id="7b049-105">Returns the specified value raised to the specified power.</span></span>



| <span data-ttu-id="7b049-106">*RET* pow (*x*, *y*)</span><span class="sxs-lookup"><span data-stu-id="7b049-106">*ret* pow(*x*, *y*)</span></span> |
|---------------------|



 

## <a name="parameters"></a><span data-ttu-id="7b049-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7b049-107">Parameters</span></span>



| <span data-ttu-id="7b049-108">Item</span><span class="sxs-lookup"><span data-stu-id="7b049-108">Item</span></span>                                                   | <span data-ttu-id="7b049-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="7b049-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="7b049-110"><span id="x"></span><span id="X"></span>*w.x.y.*</span><span class="sxs-lookup"><span data-stu-id="7b049-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="7b049-111">\[no \] valor especificado.</span><span class="sxs-lookup"><span data-stu-id="7b049-111">\[in\] The specified value.</span></span><br/> |
| <span data-ttu-id="7b049-112"><span id="y"></span><span id="Y"></span>*Iar*</span><span class="sxs-lookup"><span data-stu-id="7b049-112"><span id="y"></span><span id="Y"></span>*y*</span></span><br/> | <span data-ttu-id="7b049-113">\[na \] potência especificada.</span><span class="sxs-lookup"><span data-stu-id="7b049-113">\[in\] The specified power.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="7b049-114">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="7b049-114">Return Value</span></span>

<span data-ttu-id="7b049-115">O parâmetro *x* é elevado à potência do parâmetro *y* .</span><span class="sxs-lookup"><span data-stu-id="7b049-115">The *x* parameter raised to the power of the *y* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b049-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="7b049-116">Remarks</span></span>

<span data-ttu-id="7b049-117">A função intrínseca **pow** HLSL calcula *x*<sup>y</sup>.</span><span class="sxs-lookup"><span data-stu-id="7b049-117">The **pow** HLSL intrinsic function calculates *x*<sup>y</sup>.</span></span>



| <span data-ttu-id="7b049-118">X</span><span class="sxs-lookup"><span data-stu-id="7b049-118">X</span></span>      | <span data-ttu-id="7b049-119">Y</span><span class="sxs-lookup"><span data-stu-id="7b049-119">Y</span></span>      | <span data-ttu-id="7b049-120">Resultado</span><span class="sxs-lookup"><span data-stu-id="7b049-120">Result</span></span>                                                                      |
|--------|--------|-----------------------------------------------------------------------------|
| <span data-ttu-id="7b049-121">< 0</span><span class="sxs-lookup"><span data-stu-id="7b049-121">< 0</span></span> | <span data-ttu-id="7b049-122">any</span><span class="sxs-lookup"><span data-stu-id="7b049-122">any</span></span>    | <span data-ttu-id="7b049-123">NAN</span><span class="sxs-lookup"><span data-stu-id="7b049-123">NAN</span></span>                                                                         |
| <span data-ttu-id="7b049-124">> 0</span><span class="sxs-lookup"><span data-stu-id="7b049-124">> 0</span></span> | <span data-ttu-id="7b049-125">= = 0</span><span class="sxs-lookup"><span data-stu-id="7b049-125">== 0</span></span>   | <span data-ttu-id="7b049-126">1</span><span class="sxs-lookup"><span data-stu-id="7b049-126">1</span></span>                                                                           |
| <span data-ttu-id="7b049-127">= = 0</span><span class="sxs-lookup"><span data-stu-id="7b049-127">== 0</span></span>   | <span data-ttu-id="7b049-128">> 0</span><span class="sxs-lookup"><span data-stu-id="7b049-128">> 0</span></span> | <span data-ttu-id="7b049-129">0</span><span class="sxs-lookup"><span data-stu-id="7b049-129">0</span></span>                                                                           |
| <span data-ttu-id="7b049-130">= = 0</span><span class="sxs-lookup"><span data-stu-id="7b049-130">== 0</span></span>   | <span data-ttu-id="7b049-131">< 0</span><span class="sxs-lookup"><span data-stu-id="7b049-131">< 0</span></span> | <span data-ttu-id="7b049-132">ini</span><span class="sxs-lookup"><span data-stu-id="7b049-132">inf</span></span>                                                                         |
| <span data-ttu-id="7b049-133">> 0</span><span class="sxs-lookup"><span data-stu-id="7b049-133">> 0</span></span> | <span data-ttu-id="7b049-134">< 0</span><span class="sxs-lookup"><span data-stu-id="7b049-134">< 0</span></span> | <span data-ttu-id="7b049-135">1/X<sup>-Y</sup></span><span class="sxs-lookup"><span data-stu-id="7b049-135">1/X<sup>-Y</sup></span></span>                                                            |
| <span data-ttu-id="7b049-136">= = 0</span><span class="sxs-lookup"><span data-stu-id="7b049-136">== 0</span></span>   | <span data-ttu-id="7b049-137">= = 0</span><span class="sxs-lookup"><span data-stu-id="7b049-137">== 0</span></span>   | <span data-ttu-id="7b049-138">Depende do processador gráfico específico</span><span class="sxs-lookup"><span data-stu-id="7b049-138">Depends on the particular graphics processor</span></span><br/> <span data-ttu-id="7b049-139">0, ou 1, ou NAN</span><span class="sxs-lookup"><span data-stu-id="7b049-139">0, or 1, or NAN</span></span><br/> |



 

## <a name="type-description"></a><span data-ttu-id="7b049-140">Descrição do tipo</span><span class="sxs-lookup"><span data-stu-id="7b049-140">Type Description</span></span>



| <span data-ttu-id="7b049-141">Name</span><span class="sxs-lookup"><span data-stu-id="7b049-141">Name</span></span>  | [<span data-ttu-id="7b049-142">**Tipo de modelo**</span><span class="sxs-lookup"><span data-stu-id="7b049-142">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="7b049-143">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="7b049-143">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="7b049-144">Tamanho</span><span class="sxs-lookup"><span data-stu-id="7b049-144">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="7b049-145">*x*</span><span class="sxs-lookup"><span data-stu-id="7b049-145">*x*</span></span>   | <span data-ttu-id="7b049-146">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **vetor** ou **matriz**</span><span class="sxs-lookup"><span data-stu-id="7b049-146">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="7b049-147">**barra**</span><span class="sxs-lookup"><span data-stu-id="7b049-147">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="7b049-148">any</span><span class="sxs-lookup"><span data-stu-id="7b049-148">any</span></span>                            |
| <span data-ttu-id="7b049-149">*y*</span><span class="sxs-lookup"><span data-stu-id="7b049-149">*y*</span></span>   | <span data-ttu-id="7b049-150">igual ao *x* de entrada</span><span class="sxs-lookup"><span data-stu-id="7b049-150">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="7b049-151">**barra**</span><span class="sxs-lookup"><span data-stu-id="7b049-151">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="7b049-152">mesmas dimensões como entrada *x*</span><span class="sxs-lookup"><span data-stu-id="7b049-152">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="7b049-153">*RET*</span><span class="sxs-lookup"><span data-stu-id="7b049-153">*ret*</span></span> | <span data-ttu-id="7b049-154">igual ao *x* de entrada</span><span class="sxs-lookup"><span data-stu-id="7b049-154">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="7b049-155">**barra**</span><span class="sxs-lookup"><span data-stu-id="7b049-155">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="7b049-156">mesmas dimensões como entrada *x*</span><span class="sxs-lookup"><span data-stu-id="7b049-156">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="7b049-157">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="7b049-157">Minimum Shader Model</span></span>

<span data-ttu-id="7b049-158">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="7b049-158">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="7b049-159">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="7b049-159">Shader Model</span></span>                                                                       | <span data-ttu-id="7b049-160">Com suporte</span><span class="sxs-lookup"><span data-stu-id="7b049-160">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="7b049-161">[Modelo do sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="7b049-161">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="7b049-162">sim</span><span class="sxs-lookup"><span data-stu-id="7b049-162">yes</span></span>                 |
| [<span data-ttu-id="7b049-163">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7b049-163">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="7b049-164">Sim ( \_ apenas vs 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="7b049-164">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="7b049-165">Confira também</span><span class="sxs-lookup"><span data-stu-id="7b049-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b049-166">**Funções intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="7b049-166">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

