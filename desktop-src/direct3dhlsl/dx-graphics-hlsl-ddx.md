---
title: campo DDX
description: Retorna a derivada parcial do valor especificado em relação à coordenada x de espaço na tela.
ms.assetid: a21c2d2a-7c62-4dc6-8521-273690be1104
keywords:
- campo DDX HLSL
topic_type:
- apiref
api_name:
- ddx
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dc82f41e8968ccfadaf5d87a8058d332f04ce3a7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366206"
---
# <a name="ddx"></a><span data-ttu-id="37af2-104">campo DDX</span><span class="sxs-lookup"><span data-stu-id="37af2-104">ddx</span></span>

<span data-ttu-id="37af2-105">Retorna a derivada parcial do valor especificado em relação à coordenada x de espaço na tela.</span><span class="sxs-lookup"><span data-stu-id="37af2-105">Returns the partial derivative of the specified value with respect to the screen-space x-coordinate.</span></span>



| <span data-ttu-id="37af2-106">*RET* campo DDX (*x*)</span><span class="sxs-lookup"><span data-stu-id="37af2-106">*ret* ddx(*x*)</span></span> |
|----------------|



 

<span data-ttu-id="37af2-107">Essa função computa a derivada parcial em relação à coordenada x de espaço na tela.</span><span class="sxs-lookup"><span data-stu-id="37af2-107">This function computes the partial derivative with respect to the screen-space x-coordinate.</span></span> <span data-ttu-id="37af2-108">Para calcular a derivada parcial em relação à coordenada y de espaço de tela, use a função [**ddy**](dx-graphics-hlsl-ddy.md) .</span><span class="sxs-lookup"><span data-stu-id="37af2-108">To compute the partial derivative with respect to the screen-space y-coordinate, use the [**ddy**](dx-graphics-hlsl-ddy.md) function.</span></span>

<span data-ttu-id="37af2-109">Essa função só tem suporte em sombreadores de pixel.</span><span class="sxs-lookup"><span data-stu-id="37af2-109">This function is only supported in pixel shaders.</span></span>

## <a name="parameters"></a><span data-ttu-id="37af2-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="37af2-110">Parameters</span></span>



| <span data-ttu-id="37af2-111">Item</span><span class="sxs-lookup"><span data-stu-id="37af2-111">Item</span></span>                                                   | <span data-ttu-id="37af2-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="37af2-112">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="37af2-113"><span id="x"></span><span id="X"></span>*w.x.y.*</span><span class="sxs-lookup"><span data-stu-id="37af2-113"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="37af2-114">\[no \] valor especificado.</span><span class="sxs-lookup"><span data-stu-id="37af2-114">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="37af2-115">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="37af2-115">Return Value</span></span>

<span data-ttu-id="37af2-116">A derivada parcial do parâmetro *x* .</span><span class="sxs-lookup"><span data-stu-id="37af2-116">The partial derivative of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="37af2-117">Descrição do tipo</span><span class="sxs-lookup"><span data-stu-id="37af2-117">Type Description</span></span>



| <span data-ttu-id="37af2-118">Name</span><span class="sxs-lookup"><span data-stu-id="37af2-118">Name</span></span>  | [<span data-ttu-id="37af2-119">**Tipo de modelo**</span><span class="sxs-lookup"><span data-stu-id="37af2-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="37af2-120">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="37af2-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="37af2-121">Tamanho</span><span class="sxs-lookup"><span data-stu-id="37af2-121">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="37af2-122">*x*</span><span class="sxs-lookup"><span data-stu-id="37af2-122">*x*</span></span>   | <span data-ttu-id="37af2-123">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **vetor** ou **matriz**</span><span class="sxs-lookup"><span data-stu-id="37af2-123">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="37af2-124">**barra**</span><span class="sxs-lookup"><span data-stu-id="37af2-124">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="37af2-125">any</span><span class="sxs-lookup"><span data-stu-id="37af2-125">any</span></span>                            |
| <span data-ttu-id="37af2-126">*RET*</span><span class="sxs-lookup"><span data-stu-id="37af2-126">*ret*</span></span> | <span data-ttu-id="37af2-127">igual ao *x* de entrada</span><span class="sxs-lookup"><span data-stu-id="37af2-127">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="37af2-128">**barra**</span><span class="sxs-lookup"><span data-stu-id="37af2-128">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="37af2-129">mesmas dimensões como entrada *x*</span><span class="sxs-lookup"><span data-stu-id="37af2-129">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="37af2-130">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="37af2-130">Minimum Shader Model</span></span>

<span data-ttu-id="37af2-131">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="37af2-131">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="37af2-132">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="37af2-132">Shader Model</span></span>                                                                | <span data-ttu-id="37af2-133">Com suporte</span><span class="sxs-lookup"><span data-stu-id="37af2-133">Supported</span></span>                                 |
|-----------------------------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="37af2-134">[Modelo](d3d11-graphics-reference-sm5.md) de sombreador 5 e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="37af2-134">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="37af2-135">sim</span><span class="sxs-lookup"><span data-stu-id="37af2-135">yes</span></span>                                       |
| [<span data-ttu-id="37af2-136">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="37af2-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                                  | <span data-ttu-id="37af2-137">sim</span><span class="sxs-lookup"><span data-stu-id="37af2-137">yes</span></span>                                       |
| [<span data-ttu-id="37af2-138">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="37af2-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md)                   | <span data-ttu-id="37af2-139">sim</span><span class="sxs-lookup"><span data-stu-id="37af2-139">yes</span></span>                                       |
| [<span data-ttu-id="37af2-140">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="37af2-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md)                   | <span data-ttu-id="37af2-141">Sim, no PS \_ 2 \_ x; sem suporte no PS \_ 2 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="37af2-141">yes in ps\_2\_x; unsupported in ps\_2\_0.</span></span> |
| [<span data-ttu-id="37af2-142">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="37af2-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                   | <span data-ttu-id="37af2-143">não</span><span class="sxs-lookup"><span data-stu-id="37af2-143">no</span></span>                                        |



 

<span data-ttu-id="37af2-144">Essa função tem suporte nos seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="37af2-144">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="37af2-145">Vértice</span><span class="sxs-lookup"><span data-stu-id="37af2-145">Vertex</span></span> | <span data-ttu-id="37af2-146">Envoltória</span><span class="sxs-lookup"><span data-stu-id="37af2-146">Hull</span></span> | <span data-ttu-id="37af2-147">Domínio</span><span class="sxs-lookup"><span data-stu-id="37af2-147">Domain</span></span> | <span data-ttu-id="37af2-148">Geometria</span><span class="sxs-lookup"><span data-stu-id="37af2-148">Geometry</span></span> | <span data-ttu-id="37af2-149">16x16</span><span class="sxs-lookup"><span data-stu-id="37af2-149">Pixel</span></span> | <span data-ttu-id="37af2-150">Computação</span><span class="sxs-lookup"><span data-stu-id="37af2-150">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="37af2-151">x</span><span class="sxs-lookup"><span data-stu-id="37af2-151">x</span></span>     |         |



 

## <a name="see-also"></a><span data-ttu-id="37af2-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="37af2-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37af2-153">**Funções intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="37af2-153">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

