---
title: Etapa
description: Compara dois valores, retornando 0 ou 1 com base em qual valor é maior.
ms.assetid: 1c1c4ec4-ae97-42ce-99af-71903e0b5edf
keywords:
- etapa HLSL
topic_type:
- apiref
api_name:
- step
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f9c800e8d8c6f78386139f822f118163f3b431f5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641656"
---
# <a name="step"></a><span data-ttu-id="0f17d-104">Etapa</span><span class="sxs-lookup"><span data-stu-id="0f17d-104">step</span></span>

<span data-ttu-id="0f17d-105">Compara dois valores, retornando 0 ou 1 com base em qual valor é maior.</span><span class="sxs-lookup"><span data-stu-id="0f17d-105">Compares two values, returning 0 or 1 based on which value is greater.</span></span>



| <span data-ttu-id="0f17d-106">etapa *RET* (*y*, *x*)</span><span class="sxs-lookup"><span data-stu-id="0f17d-106">*ret* step(*y*, *x*)</span></span> |
|----------------------|



 

## <a name="parameters"></a><span data-ttu-id="0f17d-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0f17d-107">Parameters</span></span>



| <span data-ttu-id="0f17d-108">Item</span><span class="sxs-lookup"><span data-stu-id="0f17d-108">Item</span></span>                                                   | <span data-ttu-id="0f17d-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="0f17d-109">Description</span></span>                                                   |
|--------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="0f17d-110"><span id="y"></span><span id="Y"></span>*Iar*</span><span class="sxs-lookup"><span data-stu-id="0f17d-110"><span id="y"></span><span id="Y"></span>*y*</span></span><br/> | <span data-ttu-id="0f17d-111">\[no \] primeiro valor de ponto flutuante a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="0f17d-111">\[in\] The first floating-point value to compare.</span></span><br/>  |
| <span data-ttu-id="0f17d-112"><span id="x"></span><span id="X"></span>*w.x.y.*</span><span class="sxs-lookup"><span data-stu-id="0f17d-112"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="0f17d-113">\[no \] segundo valor de ponto flutuante a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="0f17d-113">\[in\] The second floating-point value to compare.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="0f17d-114">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="0f17d-114">Return Value</span></span>

<span data-ttu-id="0f17d-115">1 se o parâmetro *x* for maior ou igual ao parâmetro *y* ; caso contrário, 0.</span><span class="sxs-lookup"><span data-stu-id="0f17d-115">1 if the *x* parameter is greater than or equal to the *y* parameter; otherwise, 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f17d-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="0f17d-116">Remarks</span></span>

<span data-ttu-id="0f17d-117">Essa função usa a seguinte fórmula: (*x*  >=  *y*)?</span><span class="sxs-lookup"><span data-stu-id="0f17d-117">This function uses the following formula: (*x* >= *y*) ?</span></span> <span data-ttu-id="0f17d-118">1:0.</span><span class="sxs-lookup"><span data-stu-id="0f17d-118">1 : 0.</span></span> <span data-ttu-id="0f17d-119">A função retorna 0 ou 1 dependendo se o parâmetro *x* é maior que o parâmetro *y* .</span><span class="sxs-lookup"><span data-stu-id="0f17d-119">The function returns either 0 or 1 depending on whether the *x* parameter is greater than the *y* parameter.</span></span> <span data-ttu-id="0f17d-120">Para calcular uma interpolação suave entre 0 e 1, use a função intrínseca [**smoothstep**](dx-graphics-hlsl-smoothstep.md) HLSL.</span><span class="sxs-lookup"><span data-stu-id="0f17d-120">To compute a smooth interpolation between 0 and 1, use the [**smoothstep**](dx-graphics-hlsl-smoothstep.md) HLSL intrinsic function.</span></span>

## <a name="type-description"></a><span data-ttu-id="0f17d-121">Descrição do tipo</span><span class="sxs-lookup"><span data-stu-id="0f17d-121">Type Description</span></span>



| <span data-ttu-id="0f17d-122">Name</span><span class="sxs-lookup"><span data-stu-id="0f17d-122">Name</span></span>  | [<span data-ttu-id="0f17d-123">**Tipo de modelo**</span><span class="sxs-lookup"><span data-stu-id="0f17d-123">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="0f17d-124">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="0f17d-124">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="0f17d-125">Tamanho</span><span class="sxs-lookup"><span data-stu-id="0f17d-125">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="0f17d-126">*y*</span><span class="sxs-lookup"><span data-stu-id="0f17d-126">*y*</span></span>   | <span data-ttu-id="0f17d-127">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **vetor** ou **matriz**</span><span class="sxs-lookup"><span data-stu-id="0f17d-127">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="0f17d-128">**barra**</span><span class="sxs-lookup"><span data-stu-id="0f17d-128">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="0f17d-129">any</span><span class="sxs-lookup"><span data-stu-id="0f17d-129">any</span></span>                            |
| <span data-ttu-id="0f17d-130">*x*</span><span class="sxs-lookup"><span data-stu-id="0f17d-130">*x*</span></span>   | <span data-ttu-id="0f17d-131">igual a *y* de entrada</span><span class="sxs-lookup"><span data-stu-id="0f17d-131">same as input *y*</span></span>                                                                                              | [<span data-ttu-id="0f17d-132">**barra**</span><span class="sxs-lookup"><span data-stu-id="0f17d-132">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="0f17d-133">mesmas dimensões como *y* de entrada</span><span class="sxs-lookup"><span data-stu-id="0f17d-133">same dimension(s) as input *y*</span></span> |
| <span data-ttu-id="0f17d-134">*RET*</span><span class="sxs-lookup"><span data-stu-id="0f17d-134">*ret*</span></span> | <span data-ttu-id="0f17d-135">igual a *y* de entrada</span><span class="sxs-lookup"><span data-stu-id="0f17d-135">same as input *y*</span></span>                                                                                              | [<span data-ttu-id="0f17d-136">**barra**</span><span class="sxs-lookup"><span data-stu-id="0f17d-136">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="0f17d-137">mesmas dimensões como *y* de entrada</span><span class="sxs-lookup"><span data-stu-id="0f17d-137">same dimension(s) as input *y*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="0f17d-138">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="0f17d-138">Minimum Shader Model</span></span>

<span data-ttu-id="0f17d-139">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="0f17d-139">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="0f17d-140">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="0f17d-140">Shader Model</span></span>                                                                       | <span data-ttu-id="0f17d-141">Com suporte</span><span class="sxs-lookup"><span data-stu-id="0f17d-141">Supported</span></span>                   |
|------------------------------------------------------------------------------------|-----------------------------|
| <span data-ttu-id="0f17d-142">[Modelo do sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="0f17d-142">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="0f17d-143">sim</span><span class="sxs-lookup"><span data-stu-id="0f17d-143">yes</span></span>                         |
| [<span data-ttu-id="0f17d-144">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0f17d-144">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="0f17d-145">Sim (vs \_ 1 \_ 1 e PS \_ 1 \_ 4)</span><span class="sxs-lookup"><span data-stu-id="0f17d-145">yes (vs\_1\_1 and ps\_1\_4)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="0f17d-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="0f17d-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f17d-147">**Funções intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="0f17d-147">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

