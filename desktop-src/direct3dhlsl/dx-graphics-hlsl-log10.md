---
title: log10
description: Retorna o logaritmo de base 10 do valor especificado.
ms.assetid: a94f8438-8153-4a31-bde3-98831edf99e5
keywords:
- log10 HLSL
topic_type:
- apiref
api_name:
- log10
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2d226dcc33da1aee6d55e21c6d97febc23577503
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294341"
---
# <a name="log10"></a><span data-ttu-id="c95b1-104">log10</span><span class="sxs-lookup"><span data-stu-id="c95b1-104">log10</span></span>

<span data-ttu-id="c95b1-105">Retorna o logaritmo de base 10 do valor especificado.</span><span class="sxs-lookup"><span data-stu-id="c95b1-105">Returns the base-10 logarithm of the specified value.</span></span>



| <span data-ttu-id="c95b1-106">*RET* log10 (*x*)</span><span class="sxs-lookup"><span data-stu-id="c95b1-106">*ret* log10(*x*)</span></span> |
|------------------|



 

## <a name="parameters"></a><span data-ttu-id="c95b1-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c95b1-107">Parameters</span></span>



| <span data-ttu-id="c95b1-108">Item</span><span class="sxs-lookup"><span data-stu-id="c95b1-108">Item</span></span>                                                   | <span data-ttu-id="c95b1-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="c95b1-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="c95b1-110"><span id="x"></span><span id="X"></span>*w.x.y.*</span><span class="sxs-lookup"><span data-stu-id="c95b1-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="c95b1-111">\[no \] valor especificado.</span><span class="sxs-lookup"><span data-stu-id="c95b1-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="c95b1-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="c95b1-112">Return Value</span></span>

<span data-ttu-id="c95b1-113">O logaritmo de base 10 do parâmetro *x* .</span><span class="sxs-lookup"><span data-stu-id="c95b1-113">The base-10 logarithm of the *x* parameter.</span></span> <span data-ttu-id="c95b1-114">Se o parâmetro *x* for negativo, essa função retornará indefinida.</span><span class="sxs-lookup"><span data-stu-id="c95b1-114">If the *x* parameter is negative, this function returns indefinite.</span></span> <span data-ttu-id="c95b1-115">Se o *x* for 0, essa função retornará-inf.</span><span class="sxs-lookup"><span data-stu-id="c95b1-115">If the *x* is 0, this function returns -INF.</span></span>

## <a name="type-description"></a><span data-ttu-id="c95b1-116">Descrição do tipo</span><span class="sxs-lookup"><span data-stu-id="c95b1-116">Type Description</span></span>



| <span data-ttu-id="c95b1-117">Name</span><span class="sxs-lookup"><span data-stu-id="c95b1-117">Name</span></span>  | [<span data-ttu-id="c95b1-118">**Tipo de modelo**</span><span class="sxs-lookup"><span data-stu-id="c95b1-118">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="c95b1-119">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="c95b1-119">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="c95b1-120">Tamanho</span><span class="sxs-lookup"><span data-stu-id="c95b1-120">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="c95b1-121">*x*</span><span class="sxs-lookup"><span data-stu-id="c95b1-121">*x*</span></span>   | <span data-ttu-id="c95b1-122">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **vetor** ou **matriz**</span><span class="sxs-lookup"><span data-stu-id="c95b1-122">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="c95b1-123">**barra**</span><span class="sxs-lookup"><span data-stu-id="c95b1-123">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="c95b1-124">any</span><span class="sxs-lookup"><span data-stu-id="c95b1-124">any</span></span>                            |
| <span data-ttu-id="c95b1-125">*RET*</span><span class="sxs-lookup"><span data-stu-id="c95b1-125">*ret*</span></span> | <span data-ttu-id="c95b1-126">igual ao *x* de entrada</span><span class="sxs-lookup"><span data-stu-id="c95b1-126">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="c95b1-127">**barra**</span><span class="sxs-lookup"><span data-stu-id="c95b1-127">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="c95b1-128">mesmas dimensões como entrada *x*</span><span class="sxs-lookup"><span data-stu-id="c95b1-128">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="c95b1-129">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="c95b1-129">Minimum Shader Model</span></span>

<span data-ttu-id="c95b1-130">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="c95b1-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="c95b1-131">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="c95b1-131">Shader Model</span></span>                                                                       | <span data-ttu-id="c95b1-132">Com suporte</span><span class="sxs-lookup"><span data-stu-id="c95b1-132">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="c95b1-133">[Modelo do sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="c95b1-133">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="c95b1-134">sim</span><span class="sxs-lookup"><span data-stu-id="c95b1-134">yes</span></span>                 |
| [<span data-ttu-id="c95b1-135">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c95b1-135">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="c95b1-136">Sim ( \_ apenas vs 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="c95b1-136">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="c95b1-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="c95b1-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c95b1-138">**Funções intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="c95b1-138">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

