---
title: sqrt
description: Retorna a raiz quadrada do valor de ponto flutuante especificado, por componente.
ms.assetid: e8debc60-1441-4974-9ab3-6d1c2217caaf
keywords:
- sqrt HLSL
topic_type:
- apiref
api_name:
- sqrt
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ff3c872dac6da28a1ec92993e387bd23daec7f86
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366045"
---
# <a name="sqrt"></a><span data-ttu-id="9655f-104">sqrt</span><span class="sxs-lookup"><span data-stu-id="9655f-104">sqrt</span></span>

<span data-ttu-id="9655f-105">Retorna a raiz quadrada do valor de ponto flutuante especificado, por componente.</span><span class="sxs-lookup"><span data-stu-id="9655f-105">Returns the square root of the specified floating-point value, per component.</span></span>



| <span data-ttu-id="9655f-106">*RET* sqrt (*x*)</span><span class="sxs-lookup"><span data-stu-id="9655f-106">*ret* sqrt(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="9655f-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9655f-107">Parameters</span></span>



| <span data-ttu-id="9655f-108">Item</span><span class="sxs-lookup"><span data-stu-id="9655f-108">Item</span></span>                                                   | <span data-ttu-id="9655f-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="9655f-109">Description</span></span>                                           |
|--------------------------------------------------------|-------------------------------------------------------|
| <span data-ttu-id="9655f-110"><span id="x"></span><span id="X"></span>*w.x.y.*</span><span class="sxs-lookup"><span data-stu-id="9655f-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="9655f-111">\[no \] valor de ponto flutuante especificado.</span><span class="sxs-lookup"><span data-stu-id="9655f-111">\[in\] The specified floating-point value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="9655f-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="9655f-112">Return Value</span></span>

<span data-ttu-id="9655f-113">A raiz quadrada do parâmetro *x* , por componente.</span><span class="sxs-lookup"><span data-stu-id="9655f-113">The square root of the *x* parameter, per component.</span></span>

## <a name="type-description"></a><span data-ttu-id="9655f-114">Descrição do tipo</span><span class="sxs-lookup"><span data-stu-id="9655f-114">Type Description</span></span>



| <span data-ttu-id="9655f-115">Name</span><span class="sxs-lookup"><span data-stu-id="9655f-115">Name</span></span>  | [<span data-ttu-id="9655f-116">**Tipo de modelo**</span><span class="sxs-lookup"><span data-stu-id="9655f-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="9655f-117">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="9655f-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="9655f-118">Tamanho</span><span class="sxs-lookup"><span data-stu-id="9655f-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="9655f-119">*x*</span><span class="sxs-lookup"><span data-stu-id="9655f-119">*x*</span></span>   | <span data-ttu-id="9655f-120">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **vetor** ou **matriz**</span><span class="sxs-lookup"><span data-stu-id="9655f-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="9655f-121">**barra**</span><span class="sxs-lookup"><span data-stu-id="9655f-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="9655f-122">any</span><span class="sxs-lookup"><span data-stu-id="9655f-122">any</span></span>                            |
| <span data-ttu-id="9655f-123">*RET*</span><span class="sxs-lookup"><span data-stu-id="9655f-123">*ret*</span></span> | <span data-ttu-id="9655f-124">igual ao *x* de entrada</span><span class="sxs-lookup"><span data-stu-id="9655f-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="9655f-125">**barra**</span><span class="sxs-lookup"><span data-stu-id="9655f-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="9655f-126">mesmas dimensões como entrada *x*</span><span class="sxs-lookup"><span data-stu-id="9655f-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="9655f-127">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="9655f-127">Minimum Shader Model</span></span>

<span data-ttu-id="9655f-128">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="9655f-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="9655f-129">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="9655f-129">Shader Model</span></span>                                                                       | <span data-ttu-id="9655f-130">Com suporte</span><span class="sxs-lookup"><span data-stu-id="9655f-130">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="9655f-131">[Modelo do sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="9655f-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="9655f-132">sim</span><span class="sxs-lookup"><span data-stu-id="9655f-132">yes</span></span>                 |
| [<span data-ttu-id="9655f-133">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9655f-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="9655f-134">Sim ( \_ apenas vs 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="9655f-134">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="9655f-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="9655f-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9655f-136">**Funções intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="9655f-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

