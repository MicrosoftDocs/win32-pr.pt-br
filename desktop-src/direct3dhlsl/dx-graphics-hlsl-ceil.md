---
title: ceil (Corecrt \_ Math. h)
description: Retorna o menor valor inteiro que é maior ou igual ao valor especificado.
ms.assetid: 9823f321-14c3-4b27-9a4b-7a885cece39b
keywords:
- ceil HLSL
topic_type:
- apiref
api_name:
- ceil
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec86db320119b7f162ed48a748c1d1ff4335b6f3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104989286"
---
# <a name="ceil"></a><span data-ttu-id="34f49-104">ceil</span><span class="sxs-lookup"><span data-stu-id="34f49-104">ceil</span></span>

<span data-ttu-id="34f49-105">Retorna o menor valor inteiro que é maior ou igual ao valor especificado.</span><span class="sxs-lookup"><span data-stu-id="34f49-105">Returns the smallest integer value that is greater than or equal to the specified value.</span></span>



| <span data-ttu-id="34f49-106">*RET* ceil (*x*)</span><span class="sxs-lookup"><span data-stu-id="34f49-106">*ret* ceil(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="34f49-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="34f49-107">Parameters</span></span>



| <span data-ttu-id="34f49-108">Item</span><span class="sxs-lookup"><span data-stu-id="34f49-108">Item</span></span>                                                   | <span data-ttu-id="34f49-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="34f49-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="34f49-110"><span id="x"></span><span id="X"></span>*w.x.y.*</span><span class="sxs-lookup"><span data-stu-id="34f49-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="34f49-111">\[no \] valor especificado.</span><span class="sxs-lookup"><span data-stu-id="34f49-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="34f49-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="34f49-112">Return Value</span></span>

<span data-ttu-id="34f49-113">O menor valor inteiro (retornado como um tipo de ponto flutuante) que é maior ou igual ao parâmetro *x* .</span><span class="sxs-lookup"><span data-stu-id="34f49-113">The smallest integer value (returned as a floating-point type) that is greater than or equal to the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="34f49-114">Descrição do tipo</span><span class="sxs-lookup"><span data-stu-id="34f49-114">Type Description</span></span>



| <span data-ttu-id="34f49-115">Name</span><span class="sxs-lookup"><span data-stu-id="34f49-115">Name</span></span>  | [<span data-ttu-id="34f49-116">**Tipo de modelo**</span><span class="sxs-lookup"><span data-stu-id="34f49-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="34f49-117">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="34f49-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="34f49-118">Tamanho</span><span class="sxs-lookup"><span data-stu-id="34f49-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="34f49-119">*x*</span><span class="sxs-lookup"><span data-stu-id="34f49-119">*x*</span></span>   | <span data-ttu-id="34f49-120">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **vetor** ou **matriz**</span><span class="sxs-lookup"><span data-stu-id="34f49-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="34f49-121">**barra**</span><span class="sxs-lookup"><span data-stu-id="34f49-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="34f49-122">any</span><span class="sxs-lookup"><span data-stu-id="34f49-122">any</span></span>                            |
| <span data-ttu-id="34f49-123">*RET*</span><span class="sxs-lookup"><span data-stu-id="34f49-123">*ret*</span></span> | <span data-ttu-id="34f49-124">igual ao *x* de entrada</span><span class="sxs-lookup"><span data-stu-id="34f49-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="34f49-125">**barra**</span><span class="sxs-lookup"><span data-stu-id="34f49-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="34f49-126">mesmas dimensões como entrada *x*</span><span class="sxs-lookup"><span data-stu-id="34f49-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="34f49-127">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="34f49-127">Minimum Shader Model</span></span>

<span data-ttu-id="34f49-128">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="34f49-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="34f49-129">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="34f49-129">Shader Model</span></span>                                                                       | <span data-ttu-id="34f49-130">Com suporte</span><span class="sxs-lookup"><span data-stu-id="34f49-130">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="34f49-131">[Modelo do sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="34f49-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="34f49-132">sim</span><span class="sxs-lookup"><span data-stu-id="34f49-132">yes</span></span>       |
| [<span data-ttu-id="34f49-133">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="34f49-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="34f49-134">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="34f49-134">vs\_1\_1</span></span>  |



 

## <a name="requirements"></a><span data-ttu-id="34f49-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="34f49-135">Requirements</span></span>



| <span data-ttu-id="34f49-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="34f49-136">Requirement</span></span> | <span data-ttu-id="34f49-137">Valor</span><span class="sxs-lookup"><span data-stu-id="34f49-137">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="34f49-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="34f49-138">Header</span></span><br/> | <dl> <span data-ttu-id="34f49-139"><dt>Corecrt \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="34f49-139"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34f49-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="34f49-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34f49-141">**Funções intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="34f49-141">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

