---
title: frexp (Corecrt \_ Math. h)
description: Retorna o mantissa e o expoente do valor de ponto flutuante especificado.
ms.assetid: 9252feff-da85-4b3e-97db-1fcddd786695
keywords:
- frexp HLSL
topic_type:
- apiref
api_name:
- frexp
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bddbcbbf9e97aff739bb06a0f0d0ddac12134463
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930588"
---
# <a name="frexp"></a><span data-ttu-id="7f7f4-104">frexp</span><span class="sxs-lookup"><span data-stu-id="7f7f4-104">frexp</span></span>

<span data-ttu-id="7f7f4-105">Retorna o mantissa e o expoente do valor de ponto flutuante especificado.</span><span class="sxs-lookup"><span data-stu-id="7f7f4-105">Returns the mantissa and exponent of the specified floating-point value.</span></span>



| <span data-ttu-id="7f7f4-106">*RET* frexp (*x*, *exp*)</span><span class="sxs-lookup"><span data-stu-id="7f7f4-106">*ret* frexp(*x*, *exp*)</span></span> |
|-------------------------|



 

<span data-ttu-id="7f7f4-107">O valor de retorno é o mantissa, e o valor retornado pelo parâmetro *exp* é o expoente.</span><span class="sxs-lookup"><span data-stu-id="7f7f4-107">The return value is the mantissa, and the value returned by *exp* parameter is the exponent.</span></span>

## <a name="parameters"></a><span data-ttu-id="7f7f4-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7f7f4-108">Parameters</span></span>



| <span data-ttu-id="7f7f4-109">Item</span><span class="sxs-lookup"><span data-stu-id="7f7f4-109">Item</span></span>                                                         | <span data-ttu-id="7f7f4-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="7f7f4-110">Description</span></span>                                                                                                                                      |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f7f4-111"><span id="x"></span><span id="X"></span>*w.x.y.*</span><span class="sxs-lookup"><span data-stu-id="7f7f4-111"><span id="x"></span><span id="X"></span>*x*</span></span><br/>       | <span data-ttu-id="7f7f4-112">\[no \] valor de ponto flutuante especificado.</span><span class="sxs-lookup"><span data-stu-id="7f7f4-112">\[in\] The specified floating-point value.</span></span> <span data-ttu-id="7f7f4-113">Se o parâmetro *x* for 0, essa função retornará 0 para o mantissa e o expoente.</span><span class="sxs-lookup"><span data-stu-id="7f7f4-113">If the *x* parameter is 0, this function returns 0 for both the mantissa and the exponent.</span></span><br/> |
| <span data-ttu-id="7f7f4-114"><span id="exp"></span><span id="EXP"></span>*exp*</span><span class="sxs-lookup"><span data-stu-id="7f7f4-114"><span id="exp"></span><span id="EXP"></span>*exp*</span></span><br/> | <span data-ttu-id="7f7f4-115">\[\]o expoente retornado do parâmetro *x* .</span><span class="sxs-lookup"><span data-stu-id="7f7f4-115">\[out\] The returned exponent of the *x* parameter.</span></span><br/>                                                                                   |



 

## <a name="return-value"></a><span data-ttu-id="7f7f4-116">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="7f7f4-116">Return Value</span></span>

<span data-ttu-id="7f7f4-117">O mantissa do parâmetro *x* .</span><span class="sxs-lookup"><span data-stu-id="7f7f4-117">The mantissa of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="7f7f4-118">Descrição do tipo</span><span class="sxs-lookup"><span data-stu-id="7f7f4-118">Type Description</span></span>



| <span data-ttu-id="7f7f4-119">Name</span><span class="sxs-lookup"><span data-stu-id="7f7f4-119">Name</span></span>  | [<span data-ttu-id="7f7f4-120">**Tipo de modelo**</span><span class="sxs-lookup"><span data-stu-id="7f7f4-120">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="7f7f4-121">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="7f7f4-121">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="7f7f4-122">Tamanho</span><span class="sxs-lookup"><span data-stu-id="7f7f4-122">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="7f7f4-123">*x*</span><span class="sxs-lookup"><span data-stu-id="7f7f4-123">*x*</span></span>   | <span data-ttu-id="7f7f4-124">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **vetor** ou **matriz**</span><span class="sxs-lookup"><span data-stu-id="7f7f4-124">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="7f7f4-125">**barra**</span><span class="sxs-lookup"><span data-stu-id="7f7f4-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="7f7f4-126">any</span><span class="sxs-lookup"><span data-stu-id="7f7f4-126">any</span></span>                            |
| <span data-ttu-id="7f7f4-127">*exp*</span><span class="sxs-lookup"><span data-stu-id="7f7f4-127">*exp*</span></span> | <span data-ttu-id="7f7f4-128">igual ao *x* de entrada</span><span class="sxs-lookup"><span data-stu-id="7f7f4-128">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="7f7f4-129">**barra**</span><span class="sxs-lookup"><span data-stu-id="7f7f4-129">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="7f7f4-130">mesmas dimensões como entrada *x*</span><span class="sxs-lookup"><span data-stu-id="7f7f4-130">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="7f7f4-131">*RET*</span><span class="sxs-lookup"><span data-stu-id="7f7f4-131">*ret*</span></span> | <span data-ttu-id="7f7f4-132">igual ao *x* de entrada</span><span class="sxs-lookup"><span data-stu-id="7f7f4-132">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="7f7f4-133">**barra**</span><span class="sxs-lookup"><span data-stu-id="7f7f4-133">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="7f7f4-134">mesmas dimensões como entrada *x*</span><span class="sxs-lookup"><span data-stu-id="7f7f4-134">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="7f7f4-135">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="7f7f4-135">Minimum Shader Model</span></span>

<span data-ttu-id="7f7f4-136">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="7f7f4-136">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="7f7f4-137">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="7f7f4-137">Shader Model</span></span>                                                                       | <span data-ttu-id="7f7f4-138">Com suporte</span><span class="sxs-lookup"><span data-stu-id="7f7f4-138">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="7f7f4-139">[Modelo do sombreador 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="7f7f4-139">[Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) and higher shader models</span></span> | <span data-ttu-id="7f7f4-140">sim</span><span class="sxs-lookup"><span data-stu-id="7f7f4-140">yes</span></span>                 |
| [<span data-ttu-id="7f7f4-141">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7f7f4-141">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md)                          | <span data-ttu-id="7f7f4-142">Sim ( \_ somente PS 2 \_ x)</span><span class="sxs-lookup"><span data-stu-id="7f7f4-142">yes (ps\_2\_x only)</span></span> |
| [<span data-ttu-id="7f7f4-143">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7f7f4-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="7f7f4-144">não</span><span class="sxs-lookup"><span data-stu-id="7f7f4-144">no</span></span>                  |



 

## <a name="remarks"></a><span data-ttu-id="7f7f4-145">Comentários</span><span class="sxs-lookup"><span data-stu-id="7f7f4-145">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="7f7f4-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7f7f4-146">Requirements</span></span>



| <span data-ttu-id="7f7f4-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f7f4-147">Requirement</span></span> | <span data-ttu-id="7f7f4-148">Valor</span><span class="sxs-lookup"><span data-stu-id="7f7f4-148">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f7f4-149">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7f7f4-149">Header</span></span><br/> | <dl> <span data-ttu-id="7f7f4-150"><dt>Corecrt \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f7f4-150"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f7f4-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="7f7f4-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f7f4-152">**Funções intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="7f7f4-152">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

