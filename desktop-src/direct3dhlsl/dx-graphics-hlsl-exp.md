---
title: exp
description: Retorna o exponencial de base e, ou ex, do valor especificado.
ms.assetid: 7a713251-af47-4f8d-b708-40309b80ba18
keywords:
- HLSL exp
topic_type:
- apiref
api_name:
- exp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 699eb97ae0fd6bbdeba0da47693178d1e4c48e36
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641239"
---
# <a name="exp"></a><span data-ttu-id="a811c-104">exp</span><span class="sxs-lookup"><span data-stu-id="a811c-104">exp</span></span>

<span data-ttu-id="a811c-105">Retorna o exponencial de base e, ou<sup>x</sup>, do valor especificado.</span><span class="sxs-lookup"><span data-stu-id="a811c-105">Returns the base-e exponential, or e<sup>x</sup>, of the specified value.</span></span>



| <span data-ttu-id="a811c-106">*RET* . (*x*)</span><span class="sxs-lookup"><span data-stu-id="a811c-106">*ret* exp(*x*)</span></span> |
|----------------|



 

## <a name="parameters"></a><span data-ttu-id="a811c-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a811c-107">Parameters</span></span>



| <span data-ttu-id="a811c-108">Item</span><span class="sxs-lookup"><span data-stu-id="a811c-108">Item</span></span>                                                   | <span data-ttu-id="a811c-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="a811c-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="a811c-110"><span id="x"></span><span id="X"></span>*w.x.y.*</span><span class="sxs-lookup"><span data-stu-id="a811c-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="a811c-111">\[no \] valor especificado.</span><span class="sxs-lookup"><span data-stu-id="a811c-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="a811c-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="a811c-112">Return Value</span></span>

<span data-ttu-id="a811c-113">O exponencial de base e do parâmetro *x* .</span><span class="sxs-lookup"><span data-stu-id="a811c-113">The base-e exponential of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="a811c-114">Descrição do tipo</span><span class="sxs-lookup"><span data-stu-id="a811c-114">Type Description</span></span>



| <span data-ttu-id="a811c-115">Name</span><span class="sxs-lookup"><span data-stu-id="a811c-115">Name</span></span>  | [<span data-ttu-id="a811c-116">**Tipo de modelo**</span><span class="sxs-lookup"><span data-stu-id="a811c-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="a811c-117">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="a811c-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="a811c-118">Tamanho</span><span class="sxs-lookup"><span data-stu-id="a811c-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="a811c-119">*x*</span><span class="sxs-lookup"><span data-stu-id="a811c-119">*x*</span></span>   | <span data-ttu-id="a811c-120">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **vetor** ou **matriz**</span><span class="sxs-lookup"><span data-stu-id="a811c-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="a811c-121">**barra**</span><span class="sxs-lookup"><span data-stu-id="a811c-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="a811c-122">any</span><span class="sxs-lookup"><span data-stu-id="a811c-122">any</span></span>                            |
| <span data-ttu-id="a811c-123">*RET*</span><span class="sxs-lookup"><span data-stu-id="a811c-123">*ret*</span></span> | <span data-ttu-id="a811c-124">igual ao *x* de entrada</span><span class="sxs-lookup"><span data-stu-id="a811c-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="a811c-125">**barra**</span><span class="sxs-lookup"><span data-stu-id="a811c-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="a811c-126">mesmas dimensões como entrada *x*</span><span class="sxs-lookup"><span data-stu-id="a811c-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="a811c-127">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="a811c-127">Minimum Shader Model</span></span>

<span data-ttu-id="a811c-128">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="a811c-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="a811c-129">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="a811c-129">Shader Model</span></span>                                                                       | <span data-ttu-id="a811c-130">Com suporte</span><span class="sxs-lookup"><span data-stu-id="a811c-130">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="a811c-131">[Modelo do sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="a811c-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="a811c-132">sim</span><span class="sxs-lookup"><span data-stu-id="a811c-132">yes</span></span>       |
| [<span data-ttu-id="a811c-133">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a811c-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="a811c-134">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="a811c-134">vs\_1\_1</span></span>  |



 

## <a name="see-also"></a><span data-ttu-id="a811c-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="a811c-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a811c-136">**Funções intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="a811c-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

