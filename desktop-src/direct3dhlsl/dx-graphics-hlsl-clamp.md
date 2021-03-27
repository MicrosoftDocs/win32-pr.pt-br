---
title: fixe
description: Coloca o valor especificado para o intervalo mínimo e máximo especificado.
ms.assetid: bcfafcec-3f9c-4b65-950c-da34184d5cdb
keywords:
- Fixe HLSL
topic_type:
- apiref
api_name:
- clamp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f5d6b0a3e83c0b1a5e511aba96df03b828b90c11
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641660"
---
# <a name="clamp"></a><span data-ttu-id="7989d-104">fixe</span><span class="sxs-lookup"><span data-stu-id="7989d-104">clamp</span></span>

<span data-ttu-id="7989d-105">Coloca o valor especificado para o intervalo mínimo e máximo especificado.</span><span class="sxs-lookup"><span data-stu-id="7989d-105">Clamps the specified value to the specified minimum and maximum range.</span></span>



| <span data-ttu-id="7989d-106">*RET* fixe (*x*, *mín*., *máx*.)</span><span class="sxs-lookup"><span data-stu-id="7989d-106">*ret* clamp(*x*, *min*, *max*)</span></span> |
|--------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="7989d-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7989d-107">Parameters</span></span>



| <span data-ttu-id="7989d-108">Item</span><span class="sxs-lookup"><span data-stu-id="7989d-108">Item</span></span>                                                         | <span data-ttu-id="7989d-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="7989d-109">Description</span></span>                                    |
|--------------------------------------------------------------|------------------------------------------------|
| <span data-ttu-id="7989d-110"><span id="x"></span><span id="X"></span>*w.x.y.*</span><span class="sxs-lookup"><span data-stu-id="7989d-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/>       | <span data-ttu-id="7989d-111">\[em \] um valor para fixe.</span><span class="sxs-lookup"><span data-stu-id="7989d-111">\[in\] A value to clamp.</span></span><br/>            |
| <span data-ttu-id="7989d-112"><span id="min"></span><span id="MIN"></span>*min*</span><span class="sxs-lookup"><span data-stu-id="7989d-112"><span id="min"></span><span id="MIN"></span>*min*</span></span><br/> | <span data-ttu-id="7989d-113">\[no \] intervalo mínimo especificado.</span><span class="sxs-lookup"><span data-stu-id="7989d-113">\[in\] The specified minimum range.</span></span><br/> |
| <span data-ttu-id="7989d-114"><span id="max"></span><span id="MAX"></span>*maximizar*</span><span class="sxs-lookup"><span data-stu-id="7989d-114"><span id="max"></span><span id="MAX"></span>*max*</span></span><br/> | <span data-ttu-id="7989d-115">\[no \] intervalo máximo especificado.</span><span class="sxs-lookup"><span data-stu-id="7989d-115">\[in\] The specified maximum range.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="7989d-116">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="7989d-116">Return Value</span></span>

<span data-ttu-id="7989d-117">O valor de clamped para o parâmetro *x* .</span><span class="sxs-lookup"><span data-stu-id="7989d-117">The clamped value for the *x* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="7989d-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="7989d-118">Remarks</span></span>

<span data-ttu-id="7989d-119">Para os valores de-INF ou INF, fixe se comportará conforme o esperado.</span><span class="sxs-lookup"><span data-stu-id="7989d-119">For values of -INF or INF, clamp will behave as expected.</span></span> <span data-ttu-id="7989d-120">No entanto, para valores de NaN, os resultados são indefinidos.</span><span class="sxs-lookup"><span data-stu-id="7989d-120">However for values of NaN, the results are undefined.</span></span>

## <a name="type-description"></a><span data-ttu-id="7989d-121">Descrição do tipo</span><span class="sxs-lookup"><span data-stu-id="7989d-121">Type Description</span></span>



| <span data-ttu-id="7989d-122">Name</span><span class="sxs-lookup"><span data-stu-id="7989d-122">Name</span></span>  | [<span data-ttu-id="7989d-123">**Tipo de modelo**</span><span class="sxs-lookup"><span data-stu-id="7989d-123">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="7989d-124">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="7989d-124">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                 | <span data-ttu-id="7989d-125">Tamanho</span><span class="sxs-lookup"><span data-stu-id="7989d-125">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="7989d-126">*x*</span><span class="sxs-lookup"><span data-stu-id="7989d-126">*x*</span></span>   | <span data-ttu-id="7989d-127">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **vetor** ou **matriz**</span><span class="sxs-lookup"><span data-stu-id="7989d-127">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | <span data-ttu-id="7989d-128">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="7989d-128">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="7989d-129">any</span><span class="sxs-lookup"><span data-stu-id="7989d-129">any</span></span>                            |
| <span data-ttu-id="7989d-130">*min*</span><span class="sxs-lookup"><span data-stu-id="7989d-130">*min*</span></span> | <span data-ttu-id="7989d-131">igual ao *x* de entrada</span><span class="sxs-lookup"><span data-stu-id="7989d-131">same as input *x*</span></span>                                                                                              | <span data-ttu-id="7989d-132">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="7989d-132">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="7989d-133">mesmas dimensões como entrada *x*</span><span class="sxs-lookup"><span data-stu-id="7989d-133">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="7989d-134">*max*</span><span class="sxs-lookup"><span data-stu-id="7989d-134">*max*</span></span> | <span data-ttu-id="7989d-135">igual ao *x* de entrada</span><span class="sxs-lookup"><span data-stu-id="7989d-135">same as input *x*</span></span>                                                                                              | <span data-ttu-id="7989d-136">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="7989d-136">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="7989d-137">mesmas dimensões como entrada *x*</span><span class="sxs-lookup"><span data-stu-id="7989d-137">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="7989d-138">*RET*</span><span class="sxs-lookup"><span data-stu-id="7989d-138">*ret*</span></span> | <span data-ttu-id="7989d-139">igual ao *x* de entrada</span><span class="sxs-lookup"><span data-stu-id="7989d-139">same as input *x*</span></span>                                                                                              | <span data-ttu-id="7989d-140">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="7989d-140">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="7989d-141">mesmas dimensões como entrada *x*</span><span class="sxs-lookup"><span data-stu-id="7989d-141">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="7989d-142">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="7989d-142">Minimum Shader Model</span></span>

<span data-ttu-id="7989d-143">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="7989d-143">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="7989d-144">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="7989d-144">Shader Model</span></span>                                                                       | <span data-ttu-id="7989d-145">Com suporte</span><span class="sxs-lookup"><span data-stu-id="7989d-145">Supported</span></span>             |
|------------------------------------------------------------------------------------|-----------------------|
| <span data-ttu-id="7989d-146">[Modelo do sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="7989d-146">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="7989d-147">sim</span><span class="sxs-lookup"><span data-stu-id="7989d-147">yes</span></span>                   |
| [<span data-ttu-id="7989d-148">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7989d-148">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="7989d-149">vs \_ 1 \_ 1 e PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="7989d-149">vs\_1\_1 and ps\_1\_4</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="7989d-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="7989d-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7989d-151">**Funções intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="7989d-151">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

