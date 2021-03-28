---
title: exp2 (Corecrt \_ Math. h)
description: Retorna a base 2 exponencial ou 2x do valor especificado.
ms.assetid: 68b0057c-864d-440b-84f6-781d5fa3b019
keywords:
- exp2 HLSL
topic_type:
- apiref
api_name:
- exp2
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63aaf5ee7c29da49ca2e7b21d80af6967721058d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968577"
---
# <a name="exp2"></a><span data-ttu-id="8ca4c-104">exp2</span><span class="sxs-lookup"><span data-stu-id="8ca4c-104">exp2</span></span>

<span data-ttu-id="8ca4c-105">Retorna o exponencial de base 2, ou 2<sup>x</sup>, do valor especificado.</span><span class="sxs-lookup"><span data-stu-id="8ca4c-105">Returns the base 2 exponential, or 2<sup>x</sup>, of the specified value.</span></span>



| <span data-ttu-id="8ca4c-106">*RET* exp2 (*x*)</span><span class="sxs-lookup"><span data-stu-id="8ca4c-106">*ret* exp2(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="8ca4c-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8ca4c-107">Parameters</span></span>



| <span data-ttu-id="8ca4c-108">Item</span><span class="sxs-lookup"><span data-stu-id="8ca4c-108">Item</span></span>                                                   | <span data-ttu-id="8ca4c-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="8ca4c-109">Description</span></span>                                           |
|--------------------------------------------------------|-------------------------------------------------------|
| <span data-ttu-id="8ca4c-110"><span id="x"></span><span id="X"></span>*w.x.y.*</span><span class="sxs-lookup"><span data-stu-id="8ca4c-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="8ca4c-111">\[no \] valor de ponto flutuante especificado.</span><span class="sxs-lookup"><span data-stu-id="8ca4c-111">\[in\] The specified floating-point value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="8ca4c-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="8ca4c-112">Return Value</span></span>

<span data-ttu-id="8ca4c-113">O exponencial de base 2 do parâmetro *x* .</span><span class="sxs-lookup"><span data-stu-id="8ca4c-113">The base 2 exponential of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="8ca4c-114">Descrição do tipo</span><span class="sxs-lookup"><span data-stu-id="8ca4c-114">Type Description</span></span>



| <span data-ttu-id="8ca4c-115">Name</span><span class="sxs-lookup"><span data-stu-id="8ca4c-115">Name</span></span>  | [<span data-ttu-id="8ca4c-116">**Tipo de modelo**</span><span class="sxs-lookup"><span data-stu-id="8ca4c-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="8ca4c-117">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="8ca4c-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="8ca4c-118">Tamanho</span><span class="sxs-lookup"><span data-stu-id="8ca4c-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="8ca4c-119">*x*</span><span class="sxs-lookup"><span data-stu-id="8ca4c-119">*x*</span></span>   | <span data-ttu-id="8ca4c-120">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **vetor** ou **matriz**</span><span class="sxs-lookup"><span data-stu-id="8ca4c-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="8ca4c-121">**barra**</span><span class="sxs-lookup"><span data-stu-id="8ca4c-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="8ca4c-122">any</span><span class="sxs-lookup"><span data-stu-id="8ca4c-122">any</span></span>                            |
| <span data-ttu-id="8ca4c-123">*RET*</span><span class="sxs-lookup"><span data-stu-id="8ca4c-123">*ret*</span></span> | <span data-ttu-id="8ca4c-124">igual ao *x* de entrada</span><span class="sxs-lookup"><span data-stu-id="8ca4c-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="8ca4c-125">**barra**</span><span class="sxs-lookup"><span data-stu-id="8ca4c-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="8ca4c-126">mesmas dimensões como entrada *x*</span><span class="sxs-lookup"><span data-stu-id="8ca4c-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="8ca4c-127">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="8ca4c-127">Minimum Shader Model</span></span>

<span data-ttu-id="8ca4c-128">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="8ca4c-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="8ca4c-129">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="8ca4c-129">Shader Model</span></span>                                                                       | <span data-ttu-id="8ca4c-130">Com suporte</span><span class="sxs-lookup"><span data-stu-id="8ca4c-130">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="8ca4c-131">[Modelo do sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="8ca4c-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="8ca4c-132">sim</span><span class="sxs-lookup"><span data-stu-id="8ca4c-132">yes</span></span>       |
| [<span data-ttu-id="8ca4c-133">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8ca4c-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="8ca4c-134">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="8ca4c-134">vs\_1\_1</span></span>  |



 

## <a name="requirements"></a><span data-ttu-id="8ca4c-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ca4c-135">Requirements</span></span>



| <span data-ttu-id="8ca4c-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ca4c-136">Requirement</span></span> | <span data-ttu-id="8ca4c-137">Valor</span><span class="sxs-lookup"><span data-stu-id="8ca4c-137">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ca4c-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8ca4c-138">Header</span></span><br/> | <dl> <span data-ttu-id="8ca4c-139"><dt>Corecrt \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ca4c-139"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ca4c-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="8ca4c-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ca4c-141">**Funções intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="8ca4c-141">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

