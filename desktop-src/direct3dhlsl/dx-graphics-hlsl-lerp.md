---
title: lerp
description: Executa uma interpolação linear.
ms.assetid: e369f182-b5bd-4b7f-aa77-9cfe11033bc4
keywords:
- Lerp HLSL
topic_type:
- apiref
api_name:
- lerp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7c7a5251aaf410d7224b87b9ee9a8f0e8a0c947e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104988671"
---
# <a name="lerp"></a><span data-ttu-id="6c6e1-104">lerp</span><span class="sxs-lookup"><span data-stu-id="6c6e1-104">lerp</span></span>

<span data-ttu-id="6c6e1-105">Executa uma interpolação linear.</span><span class="sxs-lookup"><span data-stu-id="6c6e1-105">Performs a linear interpolation.</span></span>



| <span data-ttu-id="6c6e1-106">*RET* Lerp (*x*, *y*, *s*)</span><span class="sxs-lookup"><span data-stu-id="6c6e1-106">*ret* lerp(*x*, *y*, *s*)</span></span> |
|---------------------------|



 

## <a name="parameters"></a><span data-ttu-id="6c6e1-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6c6e1-107">Parameters</span></span>



| <span data-ttu-id="6c6e1-108">Item</span><span class="sxs-lookup"><span data-stu-id="6c6e1-108">Item</span></span>                                                   | <span data-ttu-id="6c6e1-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="6c6e1-109">Description</span></span>                                                                                           |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c6e1-110"><span id="x"></span><span id="X"></span>*w.x.y.*</span><span class="sxs-lookup"><span data-stu-id="6c6e1-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="6c6e1-111">\[no \] primeiro valor de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="6c6e1-111">\[in\] The first-floating point value.</span></span><br/>                                                     |
| <span data-ttu-id="6c6e1-112"><span id="y"></span><span id="Y"></span>*Iar*</span><span class="sxs-lookup"><span data-stu-id="6c6e1-112"><span id="y"></span><span id="Y"></span>*y*</span></span><br/> | <span data-ttu-id="6c6e1-113">\[no \] segundo valor de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="6c6e1-113">\[in\] The second-floating point value.</span></span><br/>                                                    |
| <span data-ttu-id="6c6e1-114"><span id="s"></span><span id="S"></span>*&*</span><span class="sxs-lookup"><span data-stu-id="6c6e1-114"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="6c6e1-115">\[em \] um valor que interpola linearmente entre o parâmetro *x* e o parâmetro *y* .</span><span class="sxs-lookup"><span data-stu-id="6c6e1-115">\[in\] A value that linearly interpolates between the *x* parameter and the *y* parameter.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="6c6e1-116">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="6c6e1-116">Return Value</span></span>

<span data-ttu-id="6c6e1-117">O resultado da interpolação linear.</span><span class="sxs-lookup"><span data-stu-id="6c6e1-117">The result of the linear interpolation.</span></span>

## <a name="type-description"></a><span data-ttu-id="6c6e1-118">Descrição do tipo</span><span class="sxs-lookup"><span data-stu-id="6c6e1-118">Type Description</span></span>



| <span data-ttu-id="6c6e1-119">Name</span><span class="sxs-lookup"><span data-stu-id="6c6e1-119">Name</span></span>  | [<span data-ttu-id="6c6e1-120">**Tipo de modelo**</span><span class="sxs-lookup"><span data-stu-id="6c6e1-120">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="6c6e1-121">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="6c6e1-121">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="6c6e1-122">Tamanho</span><span class="sxs-lookup"><span data-stu-id="6c6e1-122">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="6c6e1-123">*x*</span><span class="sxs-lookup"><span data-stu-id="6c6e1-123">*x*</span></span>   | <span data-ttu-id="6c6e1-124">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **vetor** ou **matriz**</span><span class="sxs-lookup"><span data-stu-id="6c6e1-124">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="6c6e1-125">**barra**</span><span class="sxs-lookup"><span data-stu-id="6c6e1-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="6c6e1-126">any</span><span class="sxs-lookup"><span data-stu-id="6c6e1-126">any</span></span>                            |
| <span data-ttu-id="6c6e1-127">*y*</span><span class="sxs-lookup"><span data-stu-id="6c6e1-127">*y*</span></span>   | <span data-ttu-id="6c6e1-128">igual ao *x* de entrada</span><span class="sxs-lookup"><span data-stu-id="6c6e1-128">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="6c6e1-129">**barra**</span><span class="sxs-lookup"><span data-stu-id="6c6e1-129">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="6c6e1-130">mesmas dimensões como entrada *x*</span><span class="sxs-lookup"><span data-stu-id="6c6e1-130">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="6c6e1-131">*s*</span><span class="sxs-lookup"><span data-stu-id="6c6e1-131">*s*</span></span>   | <span data-ttu-id="6c6e1-132">igual ao *x* de entrada</span><span class="sxs-lookup"><span data-stu-id="6c6e1-132">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="6c6e1-133">**barra**</span><span class="sxs-lookup"><span data-stu-id="6c6e1-133">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="6c6e1-134">mesmas dimensões como entrada *x*</span><span class="sxs-lookup"><span data-stu-id="6c6e1-134">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="6c6e1-135">*RET*</span><span class="sxs-lookup"><span data-stu-id="6c6e1-135">*ret*</span></span> | <span data-ttu-id="6c6e1-136">igual ao *x* de entrada</span><span class="sxs-lookup"><span data-stu-id="6c6e1-136">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="6c6e1-137">**barra**</span><span class="sxs-lookup"><span data-stu-id="6c6e1-137">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="6c6e1-138">mesmas dimensões como entrada *x*</span><span class="sxs-lookup"><span data-stu-id="6c6e1-138">same dimension(s) as input *x*</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="6c6e1-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="6c6e1-139">Remarks</span></span>

<span data-ttu-id="6c6e1-140">A interpolação linear baseia-se na fórmula a seguir: x \* (1-s) + y \* s que pode ser escrito de forma equivalente como x + s (y-x).</span><span class="sxs-lookup"><span data-stu-id="6c6e1-140">Linear interpolation is based on the following formula: x\*(1-s) + y\*s which can equivalently be written as x + s(y-x).</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="6c6e1-141">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="6c6e1-141">Minimum Shader Model</span></span>

<span data-ttu-id="6c6e1-142">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="6c6e1-142">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="6c6e1-143">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="6c6e1-143">Shader Model</span></span>                                                                       | <span data-ttu-id="6c6e1-144">Com suporte</span><span class="sxs-lookup"><span data-stu-id="6c6e1-144">Supported</span></span>                   |
|------------------------------------------------------------------------------------|-----------------------------|
| <span data-ttu-id="6c6e1-145">[Modelo do sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="6c6e1-145">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="6c6e1-146">sim</span><span class="sxs-lookup"><span data-stu-id="6c6e1-146">yes</span></span>                         |
| [<span data-ttu-id="6c6e1-147">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6c6e1-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="6c6e1-148">Sim (vs \_ 1 \_ 1 e PS \_ 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="6c6e1-148">yes (vs\_1\_1 and ps\_1\_1)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="6c6e1-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="6c6e1-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c6e1-150">**Funções intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="6c6e1-150">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

