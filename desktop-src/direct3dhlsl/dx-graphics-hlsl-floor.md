---
title: Floor (Corecrt \_ Math. h)
description: Retorna o maior inteiro que é menor ou igual ao valor especificado.
ms.assetid: f7193425-2448-4ae6-99d5-bb5e1aa74111
keywords:
- HLSL de piso
topic_type:
- apiref
api_name:
- floor
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ecb46719d5361ec9f7c36b21d94793bc9a67ffe
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968576"
---
# <a name="floor"></a><span data-ttu-id="44b7e-104">floor</span><span class="sxs-lookup"><span data-stu-id="44b7e-104">floor</span></span>

<span data-ttu-id="44b7e-105">Retorna o maior inteiro que é menor ou igual ao valor especificado.</span><span class="sxs-lookup"><span data-stu-id="44b7e-105">Returns the largest integer that is less than or equal to the specified value.</span></span>



| <span data-ttu-id="44b7e-106">baixa de *RET* (*x*)</span><span class="sxs-lookup"><span data-stu-id="44b7e-106">*ret* floor(*x*)</span></span> |
|------------------|



 

## <a name="parameters"></a><span data-ttu-id="44b7e-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="44b7e-107">Parameters</span></span>



| <span data-ttu-id="44b7e-108">Item</span><span class="sxs-lookup"><span data-stu-id="44b7e-108">Item</span></span>                                                   | <span data-ttu-id="44b7e-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="44b7e-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="44b7e-110"><span id="x"></span><span id="X"></span>*w.x.y.*</span><span class="sxs-lookup"><span data-stu-id="44b7e-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="44b7e-111">\[no \] valor especificado.</span><span class="sxs-lookup"><span data-stu-id="44b7e-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="44b7e-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="44b7e-112">Return Value</span></span>

<span data-ttu-id="44b7e-113">O maior valor inteiro (retornado como um tipo de ponto flutuante) que é menor ou igual ao parâmetro *x* .</span><span class="sxs-lookup"><span data-stu-id="44b7e-113">The largest integer value (returned as a floating-point type) that is less than or equal to the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="44b7e-114">Descrição do tipo</span><span class="sxs-lookup"><span data-stu-id="44b7e-114">Type Description</span></span>



| <span data-ttu-id="44b7e-115">Name</span><span class="sxs-lookup"><span data-stu-id="44b7e-115">Name</span></span>  | [<span data-ttu-id="44b7e-116">**Tipo de modelo**</span><span class="sxs-lookup"><span data-stu-id="44b7e-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="44b7e-117">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="44b7e-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="44b7e-118">Tamanho</span><span class="sxs-lookup"><span data-stu-id="44b7e-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="44b7e-119">*x*</span><span class="sxs-lookup"><span data-stu-id="44b7e-119">*x*</span></span>   | <span data-ttu-id="44b7e-120">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **vetor** ou **matriz**</span><span class="sxs-lookup"><span data-stu-id="44b7e-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="44b7e-121">**barra**</span><span class="sxs-lookup"><span data-stu-id="44b7e-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="44b7e-122">any</span><span class="sxs-lookup"><span data-stu-id="44b7e-122">any</span></span>                            |
| <span data-ttu-id="44b7e-123">*RET*</span><span class="sxs-lookup"><span data-stu-id="44b7e-123">*ret*</span></span> | <span data-ttu-id="44b7e-124">igual ao *x* de entrada</span><span class="sxs-lookup"><span data-stu-id="44b7e-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="44b7e-125">**barra**</span><span class="sxs-lookup"><span data-stu-id="44b7e-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="44b7e-126">mesmas dimensões como entrada *x*</span><span class="sxs-lookup"><span data-stu-id="44b7e-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="44b7e-127">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="44b7e-127">Minimum Shader Model</span></span>

<span data-ttu-id="44b7e-128">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="44b7e-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="44b7e-129">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="44b7e-129">Shader Model</span></span>                                                                       | <span data-ttu-id="44b7e-130">Com suporte</span><span class="sxs-lookup"><span data-stu-id="44b7e-130">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="44b7e-131">[Modelo do sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="44b7e-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="44b7e-132">sim</span><span class="sxs-lookup"><span data-stu-id="44b7e-132">yes</span></span>       |
| [<span data-ttu-id="44b7e-133">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="44b7e-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="44b7e-134">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="44b7e-134">vs\_1\_1</span></span>  |



 

## <a name="requirements"></a><span data-ttu-id="44b7e-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44b7e-135">Requirements</span></span>



| <span data-ttu-id="44b7e-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="44b7e-136">Requirement</span></span> | <span data-ttu-id="44b7e-137">Valor</span><span class="sxs-lookup"><span data-stu-id="44b7e-137">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="44b7e-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="44b7e-138">Header</span></span><br/> | <dl> <span data-ttu-id="44b7e-139"><dt>Corecrt \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="44b7e-139"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44b7e-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="44b7e-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44b7e-141">**Funções intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="44b7e-141">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

