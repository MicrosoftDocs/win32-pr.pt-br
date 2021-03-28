---
title: cosh
description: Retorna o cosseno hiperbólico do valor especificado.
ms.assetid: ed68c461-de91-4ce4-a424-8ab28ee43f23
keywords:
- cosh HLSL
topic_type:
- apiref
api_name:
- cosh
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3bd6cad2b79e849d8f20bbaf5baa6cfc7db0b702
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104988709"
---
# <a name="cosh"></a><span data-ttu-id="293fa-104">cosh</span><span class="sxs-lookup"><span data-stu-id="293fa-104">cosh</span></span>

<span data-ttu-id="293fa-105">Retorna o cosseno hiperbólico do valor especificado.</span><span class="sxs-lookup"><span data-stu-id="293fa-105">Returns the hyperbolic cosine of the specified value.</span></span>



| <span data-ttu-id="293fa-106">*RET* cosh (*x*)</span><span class="sxs-lookup"><span data-stu-id="293fa-106">*ret* cosh(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="293fa-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="293fa-107">Parameters</span></span>



| <span data-ttu-id="293fa-108">Item</span><span class="sxs-lookup"><span data-stu-id="293fa-108">Item</span></span>                                                   | <span data-ttu-id="293fa-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="293fa-109">Description</span></span>                                        |
|--------------------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="293fa-110"><span id="x"></span><span id="X"></span>*w.x.y.*</span><span class="sxs-lookup"><span data-stu-id="293fa-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="293fa-111">\[no \] valor especificado, em radianos.</span><span class="sxs-lookup"><span data-stu-id="293fa-111">\[in\] The specified value, in radians.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="293fa-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="293fa-112">Return Value</span></span>

<span data-ttu-id="293fa-113">O cosseno hiperbólico do parâmetro *x* .</span><span class="sxs-lookup"><span data-stu-id="293fa-113">The hyperbolic cosine of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="293fa-114">Descrição do tipo</span><span class="sxs-lookup"><span data-stu-id="293fa-114">Type Description</span></span>



| <span data-ttu-id="293fa-115">Name</span><span class="sxs-lookup"><span data-stu-id="293fa-115">Name</span></span>  | [<span data-ttu-id="293fa-116">**Tipo de modelo**</span><span class="sxs-lookup"><span data-stu-id="293fa-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="293fa-117">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="293fa-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="293fa-118">Tamanho</span><span class="sxs-lookup"><span data-stu-id="293fa-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="293fa-119">*x*</span><span class="sxs-lookup"><span data-stu-id="293fa-119">*x*</span></span>   | <span data-ttu-id="293fa-120">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **vetor** ou **matriz**</span><span class="sxs-lookup"><span data-stu-id="293fa-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="293fa-121">**barra**</span><span class="sxs-lookup"><span data-stu-id="293fa-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="293fa-122">any</span><span class="sxs-lookup"><span data-stu-id="293fa-122">any</span></span>                            |
| <span data-ttu-id="293fa-123">*RET*</span><span class="sxs-lookup"><span data-stu-id="293fa-123">*ret*</span></span> | <span data-ttu-id="293fa-124">igual ao *x* de entrada</span><span class="sxs-lookup"><span data-stu-id="293fa-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="293fa-125">**barra**</span><span class="sxs-lookup"><span data-stu-id="293fa-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="293fa-126">mesmas dimensões como entrada *x*</span><span class="sxs-lookup"><span data-stu-id="293fa-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="293fa-127">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="293fa-127">Minimum Shader Model</span></span>

<span data-ttu-id="293fa-128">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="293fa-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="293fa-129">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="293fa-129">Shader Model</span></span>                                                                       | <span data-ttu-id="293fa-130">Com suporte</span><span class="sxs-lookup"><span data-stu-id="293fa-130">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="293fa-131">[Modelo do sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="293fa-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="293fa-132">sim</span><span class="sxs-lookup"><span data-stu-id="293fa-132">yes</span></span>       |
| [<span data-ttu-id="293fa-133">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="293fa-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="293fa-134">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="293fa-134">vs\_1\_1</span></span>  |



 

## <a name="see-also"></a><span data-ttu-id="293fa-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="293fa-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="293fa-136">**Funções intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="293fa-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

