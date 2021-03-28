---
title: ddy
description: Retorna a derivada parcial do valor especificado em relação à coordenada y de espaço na tela.
ms.assetid: 1c88804f-a13f-4714-a3ef-466307afbc1b
keywords:
- ddy HLSL
topic_type:
- apiref
api_name:
- ddy
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d27e48a6d9ae237e4e58d1fd30afbac3b2b40d3d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366205"
---
# <a name="ddy"></a><span data-ttu-id="6910d-104">ddy</span><span class="sxs-lookup"><span data-stu-id="6910d-104">ddy</span></span>

<span data-ttu-id="6910d-105">Retorna a derivada parcial do valor especificado em relação à coordenada y de espaço na tela.</span><span class="sxs-lookup"><span data-stu-id="6910d-105">Returns the partial derivative of the specified value with respect to the screen-space y-coordinate.</span></span>



| <span data-ttu-id="6910d-106">*RET* ddy (*x*)</span><span class="sxs-lookup"><span data-stu-id="6910d-106">*ret* ddy(*x*)</span></span> |
|----------------|



 

<span data-ttu-id="6910d-107">Essa função computa a derivada parcial em relação à coordenada y de espaço de tela.</span><span class="sxs-lookup"><span data-stu-id="6910d-107">This function computes the partial derivative with respect to the screen-space y-coordinate.</span></span> <span data-ttu-id="6910d-108">Para calcular a derivada parcial em relação à coordenada x de espaço de tela, use a função [**campo DDX**](dx-graphics-hlsl-ddx.md) .</span><span class="sxs-lookup"><span data-stu-id="6910d-108">To compute the partial derivative with respect to the screen-space x-coordinate, use the [**ddx**](dx-graphics-hlsl-ddx.md) function.</span></span>

<span data-ttu-id="6910d-109">Essa função só tem suporte em sombreadores de pixel.</span><span class="sxs-lookup"><span data-stu-id="6910d-109">This function is only supported in pixel shaders.</span></span>

## <a name="parameters"></a><span data-ttu-id="6910d-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6910d-110">Parameters</span></span>



| <span data-ttu-id="6910d-111">Item</span><span class="sxs-lookup"><span data-stu-id="6910d-111">Item</span></span>                                                   | <span data-ttu-id="6910d-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="6910d-112">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="6910d-113"><span id="x"></span><span id="X"></span>*w.x.y.*</span><span class="sxs-lookup"><span data-stu-id="6910d-113"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="6910d-114">\[no \] valor especificado.</span><span class="sxs-lookup"><span data-stu-id="6910d-114">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="6910d-115">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="6910d-115">Return Value</span></span>

<span data-ttu-id="6910d-116">A derivada parcial do parâmetro *x* .</span><span class="sxs-lookup"><span data-stu-id="6910d-116">The partial derivative of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="6910d-117">Descrição do tipo</span><span class="sxs-lookup"><span data-stu-id="6910d-117">Type Description</span></span>



| <span data-ttu-id="6910d-118">Name</span><span class="sxs-lookup"><span data-stu-id="6910d-118">Name</span></span>  | [<span data-ttu-id="6910d-119">**Tipo de modelo**</span><span class="sxs-lookup"><span data-stu-id="6910d-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="6910d-120">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="6910d-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="6910d-121">Tamanho</span><span class="sxs-lookup"><span data-stu-id="6910d-121">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="6910d-122">*x*</span><span class="sxs-lookup"><span data-stu-id="6910d-122">*x*</span></span>   | <span data-ttu-id="6910d-123">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **vetor** ou **matriz**</span><span class="sxs-lookup"><span data-stu-id="6910d-123">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="6910d-124">**barra**</span><span class="sxs-lookup"><span data-stu-id="6910d-124">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="6910d-125">any</span><span class="sxs-lookup"><span data-stu-id="6910d-125">any</span></span>                            |
| <span data-ttu-id="6910d-126">*RET*</span><span class="sxs-lookup"><span data-stu-id="6910d-126">*ret*</span></span> | <span data-ttu-id="6910d-127">igual ao *x* de entrada</span><span class="sxs-lookup"><span data-stu-id="6910d-127">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="6910d-128">**barra**</span><span class="sxs-lookup"><span data-stu-id="6910d-128">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="6910d-129">mesmas dimensões como entrada *x*</span><span class="sxs-lookup"><span data-stu-id="6910d-129">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="6910d-130">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="6910d-130">Minimum Shader Model</span></span>

<span data-ttu-id="6910d-131">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="6910d-131">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="6910d-132">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="6910d-132">Shader Model</span></span>                                                                | <span data-ttu-id="6910d-133">Com suporte</span><span class="sxs-lookup"><span data-stu-id="6910d-133">Supported</span></span>                                 |
|-----------------------------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="6910d-134">[Modelo](d3d11-graphics-reference-sm5.md) de sombreador 5 e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="6910d-134">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="6910d-135">sim</span><span class="sxs-lookup"><span data-stu-id="6910d-135">yes</span></span>                                       |
| [<span data-ttu-id="6910d-136">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="6910d-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                                  | <span data-ttu-id="6910d-137">sim</span><span class="sxs-lookup"><span data-stu-id="6910d-137">yes</span></span>                                       |
| [<span data-ttu-id="6910d-138">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6910d-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md)                   | <span data-ttu-id="6910d-139">sim</span><span class="sxs-lookup"><span data-stu-id="6910d-139">yes</span></span>                                       |
| [<span data-ttu-id="6910d-140">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6910d-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md)                   | <span data-ttu-id="6910d-141">Sim, no PS \_ 2 \_ x; sem suporte no PS \_ 2 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="6910d-141">yes in ps\_2\_x; unsupported in ps\_2\_0.</span></span> |
| [<span data-ttu-id="6910d-142">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6910d-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                   | <span data-ttu-id="6910d-143">não</span><span class="sxs-lookup"><span data-stu-id="6910d-143">no</span></span>                                        |



 

<span data-ttu-id="6910d-144">Essa função tem suporte nos seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="6910d-144">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="6910d-145">Vértice</span><span class="sxs-lookup"><span data-stu-id="6910d-145">Vertex</span></span> | <span data-ttu-id="6910d-146">Envoltória</span><span class="sxs-lookup"><span data-stu-id="6910d-146">Hull</span></span> | <span data-ttu-id="6910d-147">Domínio</span><span class="sxs-lookup"><span data-stu-id="6910d-147">Domain</span></span> | <span data-ttu-id="6910d-148">Geometria</span><span class="sxs-lookup"><span data-stu-id="6910d-148">Geometry</span></span> | <span data-ttu-id="6910d-149">16x16</span><span class="sxs-lookup"><span data-stu-id="6910d-149">Pixel</span></span> | <span data-ttu-id="6910d-150">Computação</span><span class="sxs-lookup"><span data-stu-id="6910d-150">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="6910d-151">x</span><span class="sxs-lookup"><span data-stu-id="6910d-151">x</span></span>     |         |



 

## <a name="see-also"></a><span data-ttu-id="6910d-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="6910d-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6910d-153">**Funções intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="6910d-153">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

