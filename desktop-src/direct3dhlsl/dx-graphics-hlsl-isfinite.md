---
title: isfinito (Corecrt \_ Math. h)
description: Determina se o valor de ponto flutuante especificado é finito.
ms.assetid: 8be10499-2d06-4520-9697-dab2f461bd0d
keywords:
- HLSL isfinito
topic_type:
- apiref
api_name:
- isfinite
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f63c943dadccad9f485668948f366698f3bce5e6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104989296"
---
# <a name="isfinite"></a><span data-ttu-id="c02d3-104">isfinito</span><span class="sxs-lookup"><span data-stu-id="c02d3-104">isfinite</span></span>

<span data-ttu-id="c02d3-105">Determina se o valor de ponto flutuante especificado é finito.</span><span class="sxs-lookup"><span data-stu-id="c02d3-105">Determines if the specified floating-point value is finite.</span></span>



| <span data-ttu-id="c02d3-106">*RET* isfinito (*x*)</span><span class="sxs-lookup"><span data-stu-id="c02d3-106">*ret* isfinite(*x*)</span></span> |
|---------------------|



 

## <a name="parameters"></a><span data-ttu-id="c02d3-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c02d3-107">Parameters</span></span>



| <span data-ttu-id="c02d3-108">Item</span><span class="sxs-lookup"><span data-stu-id="c02d3-108">Item</span></span>                                                   | <span data-ttu-id="c02d3-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="c02d3-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="c02d3-110"><span id="x"></span><span id="X"></span>*w.x.y.*</span><span class="sxs-lookup"><span data-stu-id="c02d3-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="c02d3-111">\[no \] valor especificado.</span><span class="sxs-lookup"><span data-stu-id="c02d3-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="c02d3-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="c02d3-112">Return Value</span></span>

<span data-ttu-id="c02d3-113">Retorna um valor do mesmo tamanho que a entrada, com um valor definido como **true** se o parâmetro *x* for finito; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="c02d3-113">Returns a value of the same size as the input, with a value set to **True** if the *x* parameter is finite; otherwise **False**.</span></span>

## <a name="type-description"></a><span data-ttu-id="c02d3-114">Descrição do tipo</span><span class="sxs-lookup"><span data-stu-id="c02d3-114">Type Description</span></span>



| <span data-ttu-id="c02d3-115">Name</span><span class="sxs-lookup"><span data-stu-id="c02d3-115">Name</span></span>  | [<span data-ttu-id="c02d3-116">**Tipo de modelo**</span><span class="sxs-lookup"><span data-stu-id="c02d3-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="c02d3-117">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="c02d3-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="c02d3-118">Tamanho</span><span class="sxs-lookup"><span data-stu-id="c02d3-118">Size</span></span>     |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|----------|
| <span data-ttu-id="c02d3-119">*x*</span><span class="sxs-lookup"><span data-stu-id="c02d3-119">*x*</span></span>   | <span data-ttu-id="c02d3-120">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **vetor** ou **matriz**</span><span class="sxs-lookup"><span data-stu-id="c02d3-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="c02d3-121">**barra**</span><span class="sxs-lookup"><span data-stu-id="c02d3-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="c02d3-122">any</span><span class="sxs-lookup"><span data-stu-id="c02d3-122">any</span></span>      |
| <span data-ttu-id="c02d3-123">*RET*</span><span class="sxs-lookup"><span data-stu-id="c02d3-123">*ret*</span></span> | <span data-ttu-id="c02d3-124">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **vetor** ou **matriz**</span><span class="sxs-lookup"><span data-stu-id="c02d3-124">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="c02d3-125">**bool**</span><span class="sxs-lookup"><span data-stu-id="c02d3-125">**bool**</span></span>](/windows/desktop/WinProg/windows-data-types)                         | <span data-ttu-id="c02d3-126">como entrada</span><span class="sxs-lookup"><span data-stu-id="c02d3-126">as input</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="c02d3-127">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="c02d3-127">Minimum Shader Model</span></span>

<span data-ttu-id="c02d3-128">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="c02d3-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="c02d3-129">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="c02d3-129">Shader Model</span></span>                                                                       | <span data-ttu-id="c02d3-130">Com suporte</span><span class="sxs-lookup"><span data-stu-id="c02d3-130">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="c02d3-131">[Modelo do sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="c02d3-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="c02d3-132">sim</span><span class="sxs-lookup"><span data-stu-id="c02d3-132">yes</span></span>                 |
| [<span data-ttu-id="c02d3-133">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c02d3-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="c02d3-134">Sim ( \_ apenas vs 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="c02d3-134">yes (vs\_1\_1 only)</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="c02d3-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c02d3-135">Requirements</span></span>



| <span data-ttu-id="c02d3-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="c02d3-136">Requirement</span></span> | <span data-ttu-id="c02d3-137">Valor</span><span class="sxs-lookup"><span data-stu-id="c02d3-137">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="c02d3-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c02d3-138">Header</span></span><br/> | <dl> <span data-ttu-id="c02d3-139"><dt>Corecrt \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="c02d3-139"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c02d3-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="c02d3-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c02d3-141">**Funções intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="c02d3-141">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

