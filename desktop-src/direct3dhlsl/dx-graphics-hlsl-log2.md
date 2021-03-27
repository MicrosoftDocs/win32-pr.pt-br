---
title: log2 (Corecrt \_ Math. h)
description: Retorna o logaritmo de base 2 do valor especificado.
ms.assetid: 0bc75697-92c0-4de5-89bd-2ce824baa03e
keywords:
- log2 HLSL
topic_type:
- apiref
api_name:
- log2
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81692071b7886fa3e3096d785bccf80c7eff937a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930740"
---
# <a name="log2"></a><span data-ttu-id="d2e74-104">log2</span><span class="sxs-lookup"><span data-stu-id="d2e74-104">log2</span></span>

<span data-ttu-id="d2e74-105">Retorna o logaritmo de base 2 do valor especificado.</span><span class="sxs-lookup"><span data-stu-id="d2e74-105">Returns the base-2 logarithm of the specified value.</span></span>



| <span data-ttu-id="d2e74-106">*RET* log2 (*x*)</span><span class="sxs-lookup"><span data-stu-id="d2e74-106">*ret* log2(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="d2e74-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d2e74-107">Parameters</span></span>



| <span data-ttu-id="d2e74-108">Item</span><span class="sxs-lookup"><span data-stu-id="d2e74-108">Item</span></span>                                                   | <span data-ttu-id="d2e74-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="d2e74-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="d2e74-110"><span id="x"></span><span id="X"></span>*w.x.y.*</span><span class="sxs-lookup"><span data-stu-id="d2e74-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="d2e74-111">\[no \] valor especificado.</span><span class="sxs-lookup"><span data-stu-id="d2e74-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="d2e74-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="d2e74-112">Return Value</span></span>

<span data-ttu-id="d2e74-113">O logaritmo de base 2 do parâmetro *x* .</span><span class="sxs-lookup"><span data-stu-id="d2e74-113">The base-2 logarithm of the *x* parameter.</span></span> <span data-ttu-id="d2e74-114">Se o parâmetro *x* for negativo, essa função retornará indefinida.</span><span class="sxs-lookup"><span data-stu-id="d2e74-114">If the *x* parameter is negative, this function returns indefinite.</span></span> <span data-ttu-id="d2e74-115">Se o parâmetro *x* for 0, essa função retornará + inf.</span><span class="sxs-lookup"><span data-stu-id="d2e74-115">If the *x* parameter is 0, this function returns +INF.</span></span>

## <a name="type-description"></a><span data-ttu-id="d2e74-116">Descrição do tipo</span><span class="sxs-lookup"><span data-stu-id="d2e74-116">Type Description</span></span>



| <span data-ttu-id="d2e74-117">Name</span><span class="sxs-lookup"><span data-stu-id="d2e74-117">Name</span></span>  | [<span data-ttu-id="d2e74-118">**Tipo de modelo**</span><span class="sxs-lookup"><span data-stu-id="d2e74-118">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="d2e74-119">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="d2e74-119">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="d2e74-120">Tamanho</span><span class="sxs-lookup"><span data-stu-id="d2e74-120">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="d2e74-121">*x*</span><span class="sxs-lookup"><span data-stu-id="d2e74-121">*x*</span></span>   | <span data-ttu-id="d2e74-122">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **vetor** ou **matriz**</span><span class="sxs-lookup"><span data-stu-id="d2e74-122">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="d2e74-123">**barra**</span><span class="sxs-lookup"><span data-stu-id="d2e74-123">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="d2e74-124">any</span><span class="sxs-lookup"><span data-stu-id="d2e74-124">any</span></span>                            |
| <span data-ttu-id="d2e74-125">*RET*</span><span class="sxs-lookup"><span data-stu-id="d2e74-125">*ret*</span></span> | <span data-ttu-id="d2e74-126">igual ao *x* de entrada</span><span class="sxs-lookup"><span data-stu-id="d2e74-126">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="d2e74-127">**barra**</span><span class="sxs-lookup"><span data-stu-id="d2e74-127">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="d2e74-128">mesmas dimensões como entrada *x*</span><span class="sxs-lookup"><span data-stu-id="d2e74-128">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d2e74-129">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="d2e74-129">Minimum Shader Model</span></span>

<span data-ttu-id="d2e74-130">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="d2e74-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="d2e74-131">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="d2e74-131">Shader Model</span></span>                                                                       | <span data-ttu-id="d2e74-132">Com suporte</span><span class="sxs-lookup"><span data-stu-id="d2e74-132">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="d2e74-133">[Modelo do sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="d2e74-133">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="d2e74-134">sim</span><span class="sxs-lookup"><span data-stu-id="d2e74-134">yes</span></span>                 |
| [<span data-ttu-id="d2e74-135">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d2e74-135">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="d2e74-136">Sim ( \_ apenas vs 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="d2e74-136">yes (vs\_1\_1 only)</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="d2e74-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2e74-137">Requirements</span></span>



| <span data-ttu-id="d2e74-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2e74-138">Requirement</span></span> | <span data-ttu-id="d2e74-139">Valor</span><span class="sxs-lookup"><span data-stu-id="d2e74-139">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2e74-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d2e74-140">Header</span></span><br/> | <dl> <span data-ttu-id="d2e74-141"><dt>Corecrt \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2e74-141"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2e74-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="d2e74-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2e74-143">**Funções intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="d2e74-143">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

