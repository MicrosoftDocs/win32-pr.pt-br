---
title: dot
description: Retorna o produto escalar de dois vetores.
ms.assetid: ad24c06c-0b40-4dc5-a2b9-1d5438635ed8
keywords:
- ponto HLSL
topic_type:
- apiref
api_name:
- dot
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d6d05abf0d67628d1d77b362b028107e07b83457
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917560"
---
# <a name="dot"></a><span data-ttu-id="15203-104">dot</span><span class="sxs-lookup"><span data-stu-id="15203-104">dot</span></span>

<span data-ttu-id="15203-105">Retorna o produto escalar de dois vetores.</span><span class="sxs-lookup"><span data-stu-id="15203-105">Returns the dot product of two vectors.</span></span>



| <span data-ttu-id="15203-106">ponto de *resposta* (*x*, *y*)</span><span class="sxs-lookup"><span data-stu-id="15203-106">*ret* dot(*x*, *y*)</span></span> |
|---------------------|



 

## <a name="parameters"></a><span data-ttu-id="15203-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="15203-107">Parameters</span></span>



| <span data-ttu-id="15203-108">Item</span><span class="sxs-lookup"><span data-stu-id="15203-108">Item</span></span>                                                   | <span data-ttu-id="15203-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="15203-109">Description</span></span>                          |
|--------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="15203-110"><span id="x"></span><span id="X"></span>*w.x.y.*</span><span class="sxs-lookup"><span data-stu-id="15203-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="15203-111">\[no \] primeiro vetor.</span><span class="sxs-lookup"><span data-stu-id="15203-111">\[in\] The first vector.</span></span><br/>  |
| <span data-ttu-id="15203-112"><span id="y"></span><span id="Y"></span>*Iar*</span><span class="sxs-lookup"><span data-stu-id="15203-112"><span id="y"></span><span id="Y"></span>*y*</span></span><br/> | <span data-ttu-id="15203-113">\[no \] segundo vetor.</span><span class="sxs-lookup"><span data-stu-id="15203-113">\[in\] The second vector.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="15203-114">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="15203-114">Return Value</span></span>

<span data-ttu-id="15203-115">O produto de ponto do parâmetro *x* e o parâmetro *y* .</span><span class="sxs-lookup"><span data-stu-id="15203-115">The dot product of the *x* parameter and the *y* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="15203-116">Descrição do tipo</span><span class="sxs-lookup"><span data-stu-id="15203-116">Type Description</span></span>



| <span data-ttu-id="15203-117">Name</span><span class="sxs-lookup"><span data-stu-id="15203-117">Name</span></span>  | [<span data-ttu-id="15203-118">**Tipo de modelo**</span><span class="sxs-lookup"><span data-stu-id="15203-118">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="15203-119">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="15203-119">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                 | <span data-ttu-id="15203-120">Tamanho</span><span class="sxs-lookup"><span data-stu-id="15203-120">Size</span></span>                            |
|-------|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|---------------------------------|
| <span data-ttu-id="15203-121">*x*</span><span class="sxs-lookup"><span data-stu-id="15203-121">*x*</span></span>   | [<span data-ttu-id="15203-122">**vetor**</span><span class="sxs-lookup"><span data-stu-id="15203-122">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="15203-123">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="15203-123">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="15203-124">any</span><span class="sxs-lookup"><span data-stu-id="15203-124">any</span></span>                             |
| <span data-ttu-id="15203-125">*y*</span><span class="sxs-lookup"><span data-stu-id="15203-125">*y*</span></span>   | [<span data-ttu-id="15203-126">**vetor**</span><span class="sxs-lookup"><span data-stu-id="15203-126">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="15203-127">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="15203-127">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="15203-128">mesmas dimensões como entrada *x*</span><span class="sxs-lookup"><span data-stu-id="15203-128">same dimensions(s) as input *x*</span></span> |
| <span data-ttu-id="15203-129">*RET*</span><span class="sxs-lookup"><span data-stu-id="15203-129">*ret*</span></span> | [<span data-ttu-id="15203-130">**escalar**</span><span class="sxs-lookup"><span data-stu-id="15203-130">**scalar**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="15203-131">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="15203-131">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="15203-132">1</span><span class="sxs-lookup"><span data-stu-id="15203-132">1</span></span>                               |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="15203-133">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="15203-133">Minimum Shader Model</span></span>

<span data-ttu-id="15203-134">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="15203-134">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="15203-135">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="15203-135">Shader Model</span></span>                                                                       | <span data-ttu-id="15203-136">Com suporte</span><span class="sxs-lookup"><span data-stu-id="15203-136">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="15203-137">[Modelo do sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="15203-137">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="15203-138">sim</span><span class="sxs-lookup"><span data-stu-id="15203-138">yes</span></span>       |
| [<span data-ttu-id="15203-139">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="15203-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="15203-140">sim</span><span class="sxs-lookup"><span data-stu-id="15203-140">yes</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="15203-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="15203-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15203-142">**Funções intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="15203-142">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

