---
title: fmod (Corecrt \_ Math. h)
description: Retorna o restante do ponto flutuante de x/y.
ms.assetid: bb940548-c4c5-4109-a488-4ea7295c7213
keywords:
- fmod HLSL
topic_type:
- apiref
api_name:
- fmod
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9dc4367e3aa80484098e88926567953fc8e9a90
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298597"
---
# <a name="fmod"></a><span data-ttu-id="bdf75-104">fmod</span><span class="sxs-lookup"><span data-stu-id="bdf75-104">fmod</span></span>

<span data-ttu-id="bdf75-105">Retorna o restante do ponto flutuante de x/y.</span><span class="sxs-lookup"><span data-stu-id="bdf75-105">Returns the floating-point remainder of x/y.</span></span>



| <span data-ttu-id="bdf75-106">*RET* fmod (*x*, *y*)</span><span class="sxs-lookup"><span data-stu-id="bdf75-106">*ret* fmod(*x*, *y*)</span></span> |
|----------------------|



 

## <a name="parameters"></a><span data-ttu-id="bdf75-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bdf75-107">Parameters</span></span>



| <span data-ttu-id="bdf75-108">Item</span><span class="sxs-lookup"><span data-stu-id="bdf75-108">Item</span></span>                                                   | <span data-ttu-id="bdf75-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="bdf75-109">Description</span></span>                                    |
|--------------------------------------------------------|------------------------------------------------|
| <span data-ttu-id="bdf75-110"><span id="x"></span><span id="X"></span>*w.x.y.*</span><span class="sxs-lookup"><span data-stu-id="bdf75-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="bdf75-111">\[no \] dividendo de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="bdf75-111">\[in\] The floating-point dividend.</span></span><br/> |
| <span data-ttu-id="bdf75-112"><span id="y"></span><span id="Y"></span>*Iar*</span><span class="sxs-lookup"><span data-stu-id="bdf75-112"><span id="y"></span><span id="Y"></span>*y*</span></span><br/> | <span data-ttu-id="bdf75-113">\[no \] divisor de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="bdf75-113">\[in\] The floating-point divisor.</span></span><br/>  |



 

## <a name="return-value"></a><span data-ttu-id="bdf75-114">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="bdf75-114">Return Value</span></span>

<span data-ttu-id="bdf75-115">O restante de ponto flutuante do parâmetro *x* dividido pelo parâmetro *y* .</span><span class="sxs-lookup"><span data-stu-id="bdf75-115">The floating-point remainder of the *x* parameter divided by the *y* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="bdf75-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="bdf75-116">Remarks</span></span>

<span data-ttu-id="bdf75-117">O restante do ponto flutuante é calculado de modo que x = i \* + y + f, onde eu seja um inteiro, f tenha o mesmo sinal que x e o valor absoluto de f seja menor que o valor absoluto de y.</span><span class="sxs-lookup"><span data-stu-id="bdf75-117">The floating-point remainder is calculated such that x = i \* y + f, where i is an integer, f has the same sign as x, and the absolute value of f is less than the absolute value of y.</span></span>

## <a name="type-description"></a><span data-ttu-id="bdf75-118">Descrição do tipo</span><span class="sxs-lookup"><span data-stu-id="bdf75-118">Type Description</span></span>



| <span data-ttu-id="bdf75-119">Name</span><span class="sxs-lookup"><span data-stu-id="bdf75-119">Name</span></span>  | [<span data-ttu-id="bdf75-120">**Tipo de modelo**</span><span class="sxs-lookup"><span data-stu-id="bdf75-120">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="bdf75-121">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="bdf75-121">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="bdf75-122">Tamanho</span><span class="sxs-lookup"><span data-stu-id="bdf75-122">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="bdf75-123">*x*</span><span class="sxs-lookup"><span data-stu-id="bdf75-123">*x*</span></span>   | <span data-ttu-id="bdf75-124">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **vetor** ou **matriz**</span><span class="sxs-lookup"><span data-stu-id="bdf75-124">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="bdf75-125">**barra**</span><span class="sxs-lookup"><span data-stu-id="bdf75-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="bdf75-126">any</span><span class="sxs-lookup"><span data-stu-id="bdf75-126">any</span></span>                            |
| <span data-ttu-id="bdf75-127">*y*</span><span class="sxs-lookup"><span data-stu-id="bdf75-127">*y*</span></span>   | <span data-ttu-id="bdf75-128">igual ao *x* de entrada</span><span class="sxs-lookup"><span data-stu-id="bdf75-128">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="bdf75-129">**barra**</span><span class="sxs-lookup"><span data-stu-id="bdf75-129">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="bdf75-130">mesmas dimensões como entrada *x*</span><span class="sxs-lookup"><span data-stu-id="bdf75-130">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="bdf75-131">*RET*</span><span class="sxs-lookup"><span data-stu-id="bdf75-131">*ret*</span></span> | <span data-ttu-id="bdf75-132">igual ao *x* de entrada</span><span class="sxs-lookup"><span data-stu-id="bdf75-132">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="bdf75-133">**barra**</span><span class="sxs-lookup"><span data-stu-id="bdf75-133">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="bdf75-134">mesmas dimensões como entrada *x*</span><span class="sxs-lookup"><span data-stu-id="bdf75-134">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="bdf75-135">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="bdf75-135">Minimum Shader Model</span></span>

<span data-ttu-id="bdf75-136">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="bdf75-136">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="bdf75-137">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="bdf75-137">Shader Model</span></span>                                                                       | <span data-ttu-id="bdf75-138">Com suporte</span><span class="sxs-lookup"><span data-stu-id="bdf75-138">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="bdf75-139">[Modelo do sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="bdf75-139">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="bdf75-140">sim</span><span class="sxs-lookup"><span data-stu-id="bdf75-140">yes</span></span>       |
| [<span data-ttu-id="bdf75-141">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bdf75-141">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="bdf75-142">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="bdf75-142">vs\_1\_1</span></span>  |



 

## <a name="requirements"></a><span data-ttu-id="bdf75-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bdf75-143">Requirements</span></span>



| <span data-ttu-id="bdf75-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="bdf75-144">Requirement</span></span> | <span data-ttu-id="bdf75-145">Valor</span><span class="sxs-lookup"><span data-stu-id="bdf75-145">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="bdf75-146">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bdf75-146">Header</span></span><br/> | <dl> <span data-ttu-id="bdf75-147"><dt>Corecrt \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="bdf75-147"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bdf75-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="bdf75-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdf75-149">**Funções intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="bdf75-149">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

