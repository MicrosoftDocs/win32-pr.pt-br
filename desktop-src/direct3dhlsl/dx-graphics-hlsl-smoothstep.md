---
title: smoothstep
description: Retorna uma interpolação de Hermite suave entre 0 e 1, se x estiver no intervalo de \ min, máx.
ms.assetid: 6a879d82-f5ab-4e9b-bc9c-8988cbe6aa82
keywords:
- smoothstep HLSL
topic_type:
- apiref
api_name:
- smoothstep
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 64e828b52a4d4517e53ba1f1aaf0f687255ad02b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104967180"
---
# <a name="smoothstep"></a><span data-ttu-id="edeae-104">smoothstep</span><span class="sxs-lookup"><span data-stu-id="edeae-104">smoothstep</span></span>

<span data-ttu-id="edeae-105">Retorna uma interpolação de Hermite suave entre 0 e 1, se *x* estiver no intervalo \[ *mín*., *máx* \] .</span><span class="sxs-lookup"><span data-stu-id="edeae-105">Returns a smooth Hermite interpolation between 0 and 1, if *x* is in the range \[*min*, *max*\].</span></span>



| <span data-ttu-id="edeae-106">*RET* smoothstep (*mín*., *máx*. *x*)</span><span class="sxs-lookup"><span data-stu-id="edeae-106">*ret* smoothstep(*min*, *max*, *x*)</span></span> |
|-------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="edeae-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="edeae-107">Parameters</span></span>



| <span data-ttu-id="edeae-108">Item</span><span class="sxs-lookup"><span data-stu-id="edeae-108">Item</span></span>                                                         | <span data-ttu-id="edeae-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="edeae-109">Description</span></span>                                               |
|--------------------------------------------------------------|-----------------------------------------------------------|
| <span data-ttu-id="edeae-110"><span id="min"></span><span id="MIN"></span>*min*</span><span class="sxs-lookup"><span data-stu-id="edeae-110"><span id="min"></span><span id="MIN"></span>*min*</span></span><br/> | <span data-ttu-id="edeae-111">\[no \] intervalo mínimo do parâmetro *x* .</span><span class="sxs-lookup"><span data-stu-id="edeae-111">\[in\] The minimum range of the *x* parameter.</span></span><br/> |
| <span data-ttu-id="edeae-112"><span id="max"></span><span id="MAX"></span>*maximizar*</span><span class="sxs-lookup"><span data-stu-id="edeae-112"><span id="max"></span><span id="MAX"></span>*max*</span></span><br/> | <span data-ttu-id="edeae-113">\[no \] intervalo máximo do parâmetro *x* .</span><span class="sxs-lookup"><span data-stu-id="edeae-113">\[in\] The maximum range of the *x* parameter.</span></span><br/> |
| <span data-ttu-id="edeae-114"><span id="x"></span><span id="X"></span>*w.x.y.*</span><span class="sxs-lookup"><span data-stu-id="edeae-114"><span id="x"></span><span id="X"></span>*x*</span></span><br/>       | <span data-ttu-id="edeae-115">\[no \] valor especificado a ser interpolado.</span><span class="sxs-lookup"><span data-stu-id="edeae-115">\[in\] The specified value to be interpolated.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="edeae-116">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="edeae-116">Return Value</span></span>

<span data-ttu-id="edeae-117">Retornará 0 se *x* for menor que *mín*; 1 se *x* for maior que *Max*; caso contrário, um valor entre 0 e 1 se *x* está no intervalo \[ *mín*., *máx* \] .</span><span class="sxs-lookup"><span data-stu-id="edeae-117">Returns 0 if *x* is less than *min*; 1 if *x* is greater than *max*; otherwise, a value between 0 and 1 if *x* is in the range \[*min*, *max*\].</span></span>

## <a name="remarks"></a><span data-ttu-id="edeae-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="edeae-118">Remarks</span></span>

<span data-ttu-id="edeae-119">Use a função intrínseca **smoothstep** HLSL para criar uma transição suave entre dois valores.</span><span class="sxs-lookup"><span data-stu-id="edeae-119">Use the **smoothstep** HLSL intrinsic function to create a smooth transition between two values.</span></span> <span data-ttu-id="edeae-120">Por exemplo, você pode usar essa função para misturar duas cores suavemente.</span><span class="sxs-lookup"><span data-stu-id="edeae-120">For example, you can use this function to blend two colors smoothly.</span></span>

## <a name="type-description"></a><span data-ttu-id="edeae-121">Descrição do tipo</span><span class="sxs-lookup"><span data-stu-id="edeae-121">Type Description</span></span>



| <span data-ttu-id="edeae-122">Name</span><span class="sxs-lookup"><span data-stu-id="edeae-122">Name</span></span>  | [<span data-ttu-id="edeae-123">**Tipo de modelo**</span><span class="sxs-lookup"><span data-stu-id="edeae-123">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="edeae-124">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="edeae-124">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="edeae-125">Tamanho</span><span class="sxs-lookup"><span data-stu-id="edeae-125">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="edeae-126">*x*</span><span class="sxs-lookup"><span data-stu-id="edeae-126">*x*</span></span>   | <span data-ttu-id="edeae-127">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **vetor** ou **matriz**</span><span class="sxs-lookup"><span data-stu-id="edeae-127">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="edeae-128">**barra**</span><span class="sxs-lookup"><span data-stu-id="edeae-128">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="edeae-129">any</span><span class="sxs-lookup"><span data-stu-id="edeae-129">any</span></span>                            |
| <span data-ttu-id="edeae-130">*min*</span><span class="sxs-lookup"><span data-stu-id="edeae-130">*min*</span></span> | <span data-ttu-id="edeae-131">igual ao *x* de entrada</span><span class="sxs-lookup"><span data-stu-id="edeae-131">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="edeae-132">**barra**</span><span class="sxs-lookup"><span data-stu-id="edeae-132">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="edeae-133">mesmas dimensões como entrada *x*</span><span class="sxs-lookup"><span data-stu-id="edeae-133">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="edeae-134">*max*</span><span class="sxs-lookup"><span data-stu-id="edeae-134">*max*</span></span> | <span data-ttu-id="edeae-135">igual ao *x* de entrada</span><span class="sxs-lookup"><span data-stu-id="edeae-135">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="edeae-136">**barra**</span><span class="sxs-lookup"><span data-stu-id="edeae-136">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="edeae-137">mesmas dimensões como entrada *x*</span><span class="sxs-lookup"><span data-stu-id="edeae-137">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="edeae-138">*RET*</span><span class="sxs-lookup"><span data-stu-id="edeae-138">*ret*</span></span> | <span data-ttu-id="edeae-139">igual ao *x* de entrada</span><span class="sxs-lookup"><span data-stu-id="edeae-139">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="edeae-140">**barra**</span><span class="sxs-lookup"><span data-stu-id="edeae-140">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="edeae-141">mesmas dimensões como entrada *x*</span><span class="sxs-lookup"><span data-stu-id="edeae-141">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="edeae-142">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="edeae-142">Minimum Shader Model</span></span>

<span data-ttu-id="edeae-143">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="edeae-143">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="edeae-144">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="edeae-144">Shader Model</span></span>                                                                       | <span data-ttu-id="edeae-145">Com suporte</span><span class="sxs-lookup"><span data-stu-id="edeae-145">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="edeae-146">[Modelo do sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="edeae-146">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="edeae-147">sim</span><span class="sxs-lookup"><span data-stu-id="edeae-147">yes</span></span>                 |
| [<span data-ttu-id="edeae-148">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="edeae-148">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="edeae-149">Sim ( \_ apenas vs 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="edeae-149">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="edeae-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="edeae-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edeae-151">**Funções intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="edeae-151">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

