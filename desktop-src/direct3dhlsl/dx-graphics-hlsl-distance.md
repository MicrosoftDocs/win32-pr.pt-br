---
title: distância
description: Retorna uma distância escalar entre dois vetores.
ms.assetid: dda8dc39-fd72-4e92-bf9d-e700db0ede9e
keywords:
- HLSL de distância
topic_type:
- apiref
api_name:
- distance
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c0f3a64778666ac8f7de16b91eed202e36e90ed1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294210"
---
# <a name="distance"></a><span data-ttu-id="8fa72-104">distância</span><span class="sxs-lookup"><span data-stu-id="8fa72-104">distance</span></span>

<span data-ttu-id="8fa72-105">Retorna uma distância escalar entre dois vetores.</span><span class="sxs-lookup"><span data-stu-id="8fa72-105">Returns a distance scalar between two vectors.</span></span>



| <span data-ttu-id="8fa72-106">distância de *RET* (*x*, *y*)</span><span class="sxs-lookup"><span data-stu-id="8fa72-106">*ret* distance(*x*, *y*)</span></span> |
|--------------------------|



 

## <a name="parameters"></a><span data-ttu-id="8fa72-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8fa72-107">Parameters</span></span>



| <span data-ttu-id="8fa72-108">Item</span><span class="sxs-lookup"><span data-stu-id="8fa72-108">Item</span></span>                                                   | <span data-ttu-id="8fa72-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="8fa72-109">Description</span></span>                                                    |
|--------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="8fa72-110"><span id="x"></span><span id="X"></span>*w.x.y.*</span><span class="sxs-lookup"><span data-stu-id="8fa72-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="8fa72-111">\[no \] primeiro vetor de ponto flutuante a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="8fa72-111">\[in\] The first floating-point vector to compare.</span></span><br/>  |
| <span data-ttu-id="8fa72-112"><span id="y"></span><span id="Y"></span>*Iar*</span><span class="sxs-lookup"><span data-stu-id="8fa72-112"><span id="y"></span><span id="Y"></span>*y*</span></span><br/> | <span data-ttu-id="8fa72-113">\[no \] segundo vetor de ponto flutuante a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="8fa72-113">\[in\] The second floating-point vector to compare.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="8fa72-114">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="8fa72-114">Return Value</span></span>

<span data-ttu-id="8fa72-115">Um valor escalar de ponto flutuante que representa a distância entre o parâmetro *x* e o parâmetro *y* .</span><span class="sxs-lookup"><span data-stu-id="8fa72-115">A floating-point, scalar value that represents the distance between the *x* parameter and the *y* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="8fa72-116">Descrição do tipo</span><span class="sxs-lookup"><span data-stu-id="8fa72-116">Type Description</span></span>



| <span data-ttu-id="8fa72-117">Name</span><span class="sxs-lookup"><span data-stu-id="8fa72-117">Name</span></span>  | [<span data-ttu-id="8fa72-118">**Tipo de modelo**</span><span class="sxs-lookup"><span data-stu-id="8fa72-118">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="8fa72-119">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="8fa72-119">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="8fa72-120">Tamanho</span><span class="sxs-lookup"><span data-stu-id="8fa72-120">Size</span></span>                           |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="8fa72-121">*x*</span><span class="sxs-lookup"><span data-stu-id="8fa72-121">*x*</span></span>   | [<span data-ttu-id="8fa72-122">**vetor**</span><span class="sxs-lookup"><span data-stu-id="8fa72-122">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="8fa72-123">**barra**</span><span class="sxs-lookup"><span data-stu-id="8fa72-123">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="8fa72-124">any</span><span class="sxs-lookup"><span data-stu-id="8fa72-124">any</span></span>                            |
| <span data-ttu-id="8fa72-125">*y*</span><span class="sxs-lookup"><span data-stu-id="8fa72-125">*y*</span></span>   | [<span data-ttu-id="8fa72-126">**vetor**</span><span class="sxs-lookup"><span data-stu-id="8fa72-126">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="8fa72-127">**barra**</span><span class="sxs-lookup"><span data-stu-id="8fa72-127">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="8fa72-128">mesmas dimensões como entrada *x*</span><span class="sxs-lookup"><span data-stu-id="8fa72-128">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="8fa72-129">*RET*</span><span class="sxs-lookup"><span data-stu-id="8fa72-129">*ret*</span></span> | [<span data-ttu-id="8fa72-130">**escalar**</span><span class="sxs-lookup"><span data-stu-id="8fa72-130">**scalar**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="8fa72-131">**FLOAT**</span><span class="sxs-lookup"><span data-stu-id="8fa72-131">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="8fa72-132">1</span><span class="sxs-lookup"><span data-stu-id="8fa72-132">1</span></span>                              |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="8fa72-133">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="8fa72-133">Minimum Shader Model</span></span>

<span data-ttu-id="8fa72-134">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="8fa72-134">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="8fa72-135">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="8fa72-135">Shader Model</span></span>                                                                       | <span data-ttu-id="8fa72-136">Com suporte</span><span class="sxs-lookup"><span data-stu-id="8fa72-136">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="8fa72-137">[Modelo do sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="8fa72-137">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="8fa72-138">sim</span><span class="sxs-lookup"><span data-stu-id="8fa72-138">yes</span></span>       |
| [<span data-ttu-id="8fa72-139">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8fa72-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="8fa72-140">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="8fa72-140">vs\_1\_1</span></span>  |



 

## <a name="see-also"></a><span data-ttu-id="8fa72-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="8fa72-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fa72-142">**Funções intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="8fa72-142">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

