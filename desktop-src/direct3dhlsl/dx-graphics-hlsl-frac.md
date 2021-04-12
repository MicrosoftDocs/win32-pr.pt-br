---
title: frac
description: Retorna a parte fracionária (ou Decimal) de x; que é maior ou igual a 0 e menor que 1.
ms.assetid: 4e85390f-2b1a-402b-b932-09b80097f7e6
keywords:
- frac HLSL
topic_type:
- apiref
api_name:
- frac
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 468bddc34f22f9bb5f34871102678e1765148b11
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454313"
---
# <a name="frac"></a><span data-ttu-id="b927d-104">frac</span><span class="sxs-lookup"><span data-stu-id="b927d-104">frac</span></span>

<span data-ttu-id="b927d-105">Retorna a parte fracionária (ou Decimal) de x; que é maior ou igual a 0 e menor que 1.</span><span class="sxs-lookup"><span data-stu-id="b927d-105">Returns the fractional (or decimal) part of x; which is greater than or equal to 0 and less than 1.</span></span>

<span data-ttu-id="b927d-106">Consulte também [truncar](./dx-graphics-hlsl-trunc.md).</span><span class="sxs-lookup"><span data-stu-id="b927d-106">Also see [trunc](./dx-graphics-hlsl-trunc.md).</span></span>

| <span data-ttu-id="b927d-107">*RET* frac (*x*)</span><span class="sxs-lookup"><span data-stu-id="b927d-107">*ret* frac(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="b927d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b927d-108">Parameters</span></span>



| <span data-ttu-id="b927d-109">Item</span><span class="sxs-lookup"><span data-stu-id="b927d-109">Item</span></span>                                                   | <span data-ttu-id="b927d-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="b927d-110">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="b927d-111"><span id="x"></span><span id="X"></span>*w.x.y.*</span><span class="sxs-lookup"><span data-stu-id="b927d-111"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="b927d-112">\[no \] valor especificado.</span><span class="sxs-lookup"><span data-stu-id="b927d-112">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="b927d-113">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="b927d-113">Return Value</span></span>

<span data-ttu-id="b927d-114">A parte fracionária do parâmetro *x* .</span><span class="sxs-lookup"><span data-stu-id="b927d-114">The fractional part of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="b927d-115">Descrição do tipo</span><span class="sxs-lookup"><span data-stu-id="b927d-115">Type Description</span></span>



| <span data-ttu-id="b927d-116">Name</span><span class="sxs-lookup"><span data-stu-id="b927d-116">Name</span></span>  | [<span data-ttu-id="b927d-117">**Tipo de modelo**</span><span class="sxs-lookup"><span data-stu-id="b927d-117">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="b927d-118">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="b927d-118">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="b927d-119">Tamanho</span><span class="sxs-lookup"><span data-stu-id="b927d-119">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="b927d-120">*x*</span><span class="sxs-lookup"><span data-stu-id="b927d-120">*x*</span></span>   | <span data-ttu-id="b927d-121">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **vetor** ou **matriz**</span><span class="sxs-lookup"><span data-stu-id="b927d-121">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="b927d-122">**barra**</span><span class="sxs-lookup"><span data-stu-id="b927d-122">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="b927d-123">any</span><span class="sxs-lookup"><span data-stu-id="b927d-123">any</span></span>                            |
| <span data-ttu-id="b927d-124">*RET*</span><span class="sxs-lookup"><span data-stu-id="b927d-124">*ret*</span></span> | <span data-ttu-id="b927d-125">igual ao *x* de entrada</span><span class="sxs-lookup"><span data-stu-id="b927d-125">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="b927d-126">**barra**</span><span class="sxs-lookup"><span data-stu-id="b927d-126">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="b927d-127">mesmas dimensões como entrada *x*</span><span class="sxs-lookup"><span data-stu-id="b927d-127">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="b927d-128">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="b927d-128">Minimum Shader Model</span></span>

<span data-ttu-id="b927d-129">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="b927d-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="b927d-130">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="b927d-130">Shader Model</span></span>                                                                       | <span data-ttu-id="b927d-131">Com suporte</span><span class="sxs-lookup"><span data-stu-id="b927d-131">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="b927d-132">[Modelo do sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="b927d-132">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="b927d-133">sim</span><span class="sxs-lookup"><span data-stu-id="b927d-133">yes</span></span>       |
| [<span data-ttu-id="b927d-134">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b927d-134">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="b927d-135">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="b927d-135">vs\_1\_1</span></span>  |



 

## <a name="see-also"></a><span data-ttu-id="b927d-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="b927d-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b927d-137">**Funções intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="b927d-137">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

