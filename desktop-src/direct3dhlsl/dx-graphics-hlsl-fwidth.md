---
title: fwidth
description: Retorna o valor absoluto dos derivativos parciais do valor especificado.
ms.assetid: 7184c3b4-1720-4176-a494-7f73322a918e
keywords:
- fwidth HLSL
topic_type:
- apiref
api_name:
- fwidth
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cf2d5a34e1f387aadb3b044ddd1264616a61109b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084746"
---
# <a name="fwidth"></a><span data-ttu-id="ebbb2-104">fwidth</span><span class="sxs-lookup"><span data-stu-id="ebbb2-104">fwidth</span></span>

<span data-ttu-id="ebbb2-105">Retorna o valor absoluto dos derivativos parciais do valor especificado.</span><span class="sxs-lookup"><span data-stu-id="ebbb2-105">Returns the absolute value of the partial derivatives of the specified value.</span></span>



| <span data-ttu-id="ebbb2-106">*RET* fwidth (*x*)</span><span class="sxs-lookup"><span data-stu-id="ebbb2-106">*ret* fwidth(*x*)</span></span> |
|-------------------|



 

<span data-ttu-id="ebbb2-107">Essa função computa o seguinte: [**ABS**](dx-graphics-hlsl-abs.md)([**campo DDX**](dx-graphics-hlsl-ddx.md)(*x*)) + [**ABS**](dx-graphics-hlsl-abs.md)([**ddy**](dx-graphics-hlsl-ddy.md)(*x*)).</span><span class="sxs-lookup"><span data-stu-id="ebbb2-107">This function computes the following: [**abs**](dx-graphics-hlsl-abs.md)([**ddx**](dx-graphics-hlsl-ddx.md)(*x*)) + [**abs**](dx-graphics-hlsl-abs.md)([**ddy**](dx-graphics-hlsl-ddy.md)(*x*)).</span></span>

<span data-ttu-id="ebbb2-108">Essa função só tem suporte em sombreadores de pixel.</span><span class="sxs-lookup"><span data-stu-id="ebbb2-108">This function is only supported in pixel shaders.</span></span>

## <a name="parameters"></a><span data-ttu-id="ebbb2-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ebbb2-109">Parameters</span></span>



| <span data-ttu-id="ebbb2-110">Item</span><span class="sxs-lookup"><span data-stu-id="ebbb2-110">Item</span></span>                                                   | <span data-ttu-id="ebbb2-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="ebbb2-111">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="ebbb2-112"><span id="x"></span><span id="X"></span>*w.x.y.*</span><span class="sxs-lookup"><span data-stu-id="ebbb2-112"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="ebbb2-113">\[no \] valor especificado.</span><span class="sxs-lookup"><span data-stu-id="ebbb2-113">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="ebbb2-114">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="ebbb2-114">Return Value</span></span>

<span data-ttu-id="ebbb2-115">O valor absoluto dos derivativos parciais do parâmetro *x* .</span><span class="sxs-lookup"><span data-stu-id="ebbb2-115">The absolute value of the partial derivatives of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="ebbb2-116">Descrição do tipo</span><span class="sxs-lookup"><span data-stu-id="ebbb2-116">Type Description</span></span>



| <span data-ttu-id="ebbb2-117">Name</span><span class="sxs-lookup"><span data-stu-id="ebbb2-117">Name</span></span>  | [<span data-ttu-id="ebbb2-118">**Tipo de modelo**</span><span class="sxs-lookup"><span data-stu-id="ebbb2-118">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="ebbb2-119">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="ebbb2-119">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="ebbb2-120">Tamanho</span><span class="sxs-lookup"><span data-stu-id="ebbb2-120">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="ebbb2-121">*x*</span><span class="sxs-lookup"><span data-stu-id="ebbb2-121">*x*</span></span>   | <span data-ttu-id="ebbb2-122">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **vetor** ou **matriz**</span><span class="sxs-lookup"><span data-stu-id="ebbb2-122">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="ebbb2-123">**barra**</span><span class="sxs-lookup"><span data-stu-id="ebbb2-123">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="ebbb2-124">any</span><span class="sxs-lookup"><span data-stu-id="ebbb2-124">any</span></span>                            |
| <span data-ttu-id="ebbb2-125">*RET*</span><span class="sxs-lookup"><span data-stu-id="ebbb2-125">*ret*</span></span> | <span data-ttu-id="ebbb2-126">igual ao *x* de entrada</span><span class="sxs-lookup"><span data-stu-id="ebbb2-126">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="ebbb2-127">**barra**</span><span class="sxs-lookup"><span data-stu-id="ebbb2-127">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="ebbb2-128">mesmas dimensões como entrada *x*</span><span class="sxs-lookup"><span data-stu-id="ebbb2-128">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="ebbb2-129">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="ebbb2-129">Minimum Shader Model</span></span>

<span data-ttu-id="ebbb2-130">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="ebbb2-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="ebbb2-131">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="ebbb2-131">Shader Model</span></span>                                                                       | <span data-ttu-id="ebbb2-132">Com suporte</span><span class="sxs-lookup"><span data-stu-id="ebbb2-132">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="ebbb2-133">[Modelo do sombreador 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="ebbb2-133">[Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) and higher shader models</span></span> | <span data-ttu-id="ebbb2-134">sim</span><span class="sxs-lookup"><span data-stu-id="ebbb2-134">yes</span></span>                 |
| [<span data-ttu-id="ebbb2-135">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ebbb2-135">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md)                          | <span data-ttu-id="ebbb2-136">Sim ( \_ somente PS 2 \_ x)</span><span class="sxs-lookup"><span data-stu-id="ebbb2-136">yes (ps\_2\_x only)</span></span> |
| [<span data-ttu-id="ebbb2-137">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ebbb2-137">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="ebbb2-138">não</span><span class="sxs-lookup"><span data-stu-id="ebbb2-138">no</span></span>                  |



 

## <a name="see-also"></a><span data-ttu-id="ebbb2-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="ebbb2-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebbb2-140">**Funções intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="ebbb2-140">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

