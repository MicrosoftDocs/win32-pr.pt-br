---
title: sincos
description: Retorna o seno e o cosseno de x.
ms.assetid: 2ef9e84e-4539-47f5-9966-d8e02ca15d36
keywords:
- Sincos HLSL
topic_type:
- apiref
api_name:
- sincos
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8391c2fcecc939db1d7044fe56fbd281fe3e79fc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104988698"
---
# <a name="sincos"></a><span data-ttu-id="16959-104">sincos</span><span class="sxs-lookup"><span data-stu-id="16959-104">sincos</span></span>

<span data-ttu-id="16959-105">Retorna o seno e o cosseno de x.</span><span class="sxs-lookup"><span data-stu-id="16959-105">Returns the sine and cosine of x.</span></span>



| <span data-ttu-id="16959-106">Sincos (*x*, out *s*, *c*)</span><span class="sxs-lookup"><span data-stu-id="16959-106">sincos(*x*, out *s*, out *c*)</span></span> |
|-------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="16959-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="16959-107">Parameters</span></span>



| <span data-ttu-id="16959-108">Item</span><span class="sxs-lookup"><span data-stu-id="16959-108">Item</span></span>                                                   | <span data-ttu-id="16959-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="16959-109">Description</span></span>                                        |
|--------------------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="16959-110"><span id="x"></span><span id="X"></span>*w.x.y.*</span><span class="sxs-lookup"><span data-stu-id="16959-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="16959-111">\[no \] valor especificado, em radianos.</span><span class="sxs-lookup"><span data-stu-id="16959-111">\[in\] The specified value, in radians.</span></span><br/> |
| <span data-ttu-id="16959-112"><span id="s"></span><span id="S"></span>*&*</span><span class="sxs-lookup"><span data-stu-id="16959-112"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="16959-113">\[out \] retorna o seno de x.</span><span class="sxs-lookup"><span data-stu-id="16959-113">\[out\] Returns the sine of x.</span></span><br/>          |
| <span data-ttu-id="16959-114"><span id="c"></span><span id="C"></span>*&*</span><span class="sxs-lookup"><span data-stu-id="16959-114"><span id="c"></span><span id="C"></span>*c*</span></span><br/> | <span data-ttu-id="16959-115">\[out \] retorna o cosseno de x.</span><span class="sxs-lookup"><span data-stu-id="16959-115">\[out\] Returns the cosine of x.</span></span><br/>        |



 

## <a name="return-value"></a><span data-ttu-id="16959-116">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="16959-116">Return Value</span></span>

<span data-ttu-id="16959-117">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="16959-117">None.</span></span>

## <a name="type-description"></a><span data-ttu-id="16959-118">Descrição do tipo</span><span class="sxs-lookup"><span data-stu-id="16959-118">Type Description</span></span>



| <span data-ttu-id="16959-119">Name</span><span class="sxs-lookup"><span data-stu-id="16959-119">Name</span></span> | [<span data-ttu-id="16959-120">**Tipo de modelo**</span><span class="sxs-lookup"><span data-stu-id="16959-120">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="16959-121">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="16959-121">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="16959-122">Tamanho</span><span class="sxs-lookup"><span data-stu-id="16959-122">Size</span></span>                           |
|------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="16959-123">*x*</span><span class="sxs-lookup"><span data-stu-id="16959-123">*x*</span></span>  | <span data-ttu-id="16959-124">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **vetor** ou **matriz**</span><span class="sxs-lookup"><span data-stu-id="16959-124">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="16959-125">**barra**</span><span class="sxs-lookup"><span data-stu-id="16959-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="16959-126">any</span><span class="sxs-lookup"><span data-stu-id="16959-126">any</span></span>                            |
| <span data-ttu-id="16959-127">*s*</span><span class="sxs-lookup"><span data-stu-id="16959-127">*s*</span></span>  | <span data-ttu-id="16959-128">igual ao *x* de entrada</span><span class="sxs-lookup"><span data-stu-id="16959-128">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="16959-129">**barra**</span><span class="sxs-lookup"><span data-stu-id="16959-129">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="16959-130">mesmas dimensões como entrada *x*</span><span class="sxs-lookup"><span data-stu-id="16959-130">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="16959-131">c</span><span class="sxs-lookup"><span data-stu-id="16959-131">c</span></span>    | <span data-ttu-id="16959-132">igual ao *x* de entrada</span><span class="sxs-lookup"><span data-stu-id="16959-132">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="16959-133">**barra**</span><span class="sxs-lookup"><span data-stu-id="16959-133">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="16959-134">mesmas dimensões como entrada *x*</span><span class="sxs-lookup"><span data-stu-id="16959-134">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="16959-135">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="16959-135">Minimum Shader Model</span></span>

<span data-ttu-id="16959-136">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="16959-136">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="16959-137">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="16959-137">Shader Model</span></span>                                                                       | <span data-ttu-id="16959-138">Com suporte</span><span class="sxs-lookup"><span data-stu-id="16959-138">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="16959-139">[Modelo do sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="16959-139">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="16959-140">sim</span><span class="sxs-lookup"><span data-stu-id="16959-140">yes</span></span>                 |
| [<span data-ttu-id="16959-141">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="16959-141">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="16959-142">Sim ( \_ apenas vs 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="16959-142">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="16959-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="16959-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16959-144">**Funções intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="16959-144">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

