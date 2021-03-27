---
title: ldexp (Corecrt \_ Math. h)
description: Retorna o resultado da multiplicação do valor especificado por dois, elevado à potência do expoente especificado.
ms.assetid: 6d6fee96-f952-4058-a1ac-3abb98dbd540
keywords:
- ldexp HLSL
topic_type:
- apiref
api_name:
- ldexp
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 731cb5cbf933ea3f8754a7d70b9ef0b7a54e783b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103837949"
---
# <a name="ldexp"></a><span data-ttu-id="9bb47-104">ldexp</span><span class="sxs-lookup"><span data-stu-id="9bb47-104">ldexp</span></span>

<span data-ttu-id="9bb47-105">Retorna o resultado da multiplicação do valor especificado por dois, elevado à potência do expoente especificado.</span><span class="sxs-lookup"><span data-stu-id="9bb47-105">Returns the result of multiplying the specified value by two, raised to the power of the specified exponent.</span></span>



| <span data-ttu-id="9bb47-106">*RET* ldexp (*x*, *exp*)</span><span class="sxs-lookup"><span data-stu-id="9bb47-106">*ret* ldexp(*x*, *exp*)</span></span> |
|-------------------------|



 

<span data-ttu-id="9bb47-107">Essa função usa a seguinte fórmula: *x* \* 2 <sup>exp</sup></span><span class="sxs-lookup"><span data-stu-id="9bb47-107">This function uses the following formula: *x* \* 2<sup>exp</sup></span></span>

## <a name="parameters"></a><span data-ttu-id="9bb47-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9bb47-108">Parameters</span></span>



| <span data-ttu-id="9bb47-109">Item</span><span class="sxs-lookup"><span data-stu-id="9bb47-109">Item</span></span>                                                         | <span data-ttu-id="9bb47-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="9bb47-110">Description</span></span>                               |
|--------------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="9bb47-111"><span id="x"></span><span id="X"></span>*w.x.y.*</span><span class="sxs-lookup"><span data-stu-id="9bb47-111"><span id="x"></span><span id="X"></span>*x*</span></span><br/>       | <span data-ttu-id="9bb47-112">\[no \] valor especificado.</span><span class="sxs-lookup"><span data-stu-id="9bb47-112">\[in\] The specified value.</span></span><br/>    |
| <span data-ttu-id="9bb47-113"><span id="exp"></span><span id="EXP"></span>*exp*</span><span class="sxs-lookup"><span data-stu-id="9bb47-113"><span id="exp"></span><span id="EXP"></span>*exp*</span></span><br/> | <span data-ttu-id="9bb47-114">\[no \] expoente especificado.</span><span class="sxs-lookup"><span data-stu-id="9bb47-114">\[in\] The specified exponent.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="9bb47-115">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="9bb47-115">Return Value</span></span>

<span data-ttu-id="9bb47-116">O resultado da multiplicação do parâmetro *x* por dois, elevado à potência do parâmetro *exp* .</span><span class="sxs-lookup"><span data-stu-id="9bb47-116">The result of multiplying the *x* parameter by two, raised to the power of the *exp* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="9bb47-117">Descrição do tipo</span><span class="sxs-lookup"><span data-stu-id="9bb47-117">Type Description</span></span>



| <span data-ttu-id="9bb47-118">Name</span><span class="sxs-lookup"><span data-stu-id="9bb47-118">Name</span></span>  | [<span data-ttu-id="9bb47-119">**Tipo de modelo**</span><span class="sxs-lookup"><span data-stu-id="9bb47-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="9bb47-120">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="9bb47-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="9bb47-121">Tamanho</span><span class="sxs-lookup"><span data-stu-id="9bb47-121">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="9bb47-122">*x*</span><span class="sxs-lookup"><span data-stu-id="9bb47-122">*x*</span></span>   | <span data-ttu-id="9bb47-123">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **vetor** ou **matriz**</span><span class="sxs-lookup"><span data-stu-id="9bb47-123">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="9bb47-124">**barra**</span><span class="sxs-lookup"><span data-stu-id="9bb47-124">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="9bb47-125">any</span><span class="sxs-lookup"><span data-stu-id="9bb47-125">any</span></span>                            |
| <span data-ttu-id="9bb47-126">*exp*</span><span class="sxs-lookup"><span data-stu-id="9bb47-126">*exp*</span></span> | <span data-ttu-id="9bb47-127">igual ao *x* de entrada</span><span class="sxs-lookup"><span data-stu-id="9bb47-127">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="9bb47-128">**barra**</span><span class="sxs-lookup"><span data-stu-id="9bb47-128">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="9bb47-129">mesmas dimensões como entrada *x*</span><span class="sxs-lookup"><span data-stu-id="9bb47-129">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="9bb47-130">*RET*</span><span class="sxs-lookup"><span data-stu-id="9bb47-130">*ret*</span></span> | <span data-ttu-id="9bb47-131">igual ao *x* de entrada</span><span class="sxs-lookup"><span data-stu-id="9bb47-131">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="9bb47-132">**barra**</span><span class="sxs-lookup"><span data-stu-id="9bb47-132">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="9bb47-133">mesmas dimensões como entrada *x*</span><span class="sxs-lookup"><span data-stu-id="9bb47-133">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="9bb47-134">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="9bb47-134">Minimum Shader Model</span></span>

<span data-ttu-id="9bb47-135">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="9bb47-135">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="9bb47-136">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="9bb47-136">Shader Model</span></span>                                                                       | <span data-ttu-id="9bb47-137">Com suporte</span><span class="sxs-lookup"><span data-stu-id="9bb47-137">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="9bb47-138">[Modelo do sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="9bb47-138">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="9bb47-139">sim</span><span class="sxs-lookup"><span data-stu-id="9bb47-139">yes</span></span>                 |
| [<span data-ttu-id="9bb47-140">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9bb47-140">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="9bb47-141">Sim ( \_ apenas vs 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="9bb47-141">yes (vs\_1\_1 only)</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="9bb47-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9bb47-142">Requirements</span></span>



| <span data-ttu-id="9bb47-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="9bb47-143">Requirement</span></span> | <span data-ttu-id="9bb47-144">Valor</span><span class="sxs-lookup"><span data-stu-id="9bb47-144">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="9bb47-145">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9bb47-145">Header</span></span><br/> | <dl> <span data-ttu-id="9bb47-146"><dt>Corecrt \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="9bb47-146"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9bb47-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="9bb47-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bb47-148">**Funções intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="9bb47-148">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

