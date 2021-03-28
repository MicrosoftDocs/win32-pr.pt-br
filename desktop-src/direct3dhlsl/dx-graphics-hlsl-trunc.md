---
title: trunc (Corecrt \_ Math. h)
description: Trunca um valor de ponto flutuante para o componente de número inteiro.
ms.assetid: a0978fa2-71f8-4257-8c90-96224c2ec953
keywords:
- truncar HLSL
topic_type:
- apiref
api_name:
- trunc
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34493f60e60bc0dce35f5f9db50360265191c742
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104989319"
---
# <a name="trunc"></a><span data-ttu-id="65704-104">trunc</span><span class="sxs-lookup"><span data-stu-id="65704-104">trunc</span></span>

<span data-ttu-id="65704-105">Trunca um valor de ponto flutuante para o componente de número inteiro.</span><span class="sxs-lookup"><span data-stu-id="65704-105">Truncates a floating-point value to the integer component.</span></span>



| <span data-ttu-id="65704-106">RET TRUNC (*x*)</span><span class="sxs-lookup"><span data-stu-id="65704-106">ret trunc(*x*)</span></span> |
|----------------|



 

## <a name="parameters"></a><span data-ttu-id="65704-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="65704-107">Parameters</span></span>



| <span data-ttu-id="65704-108">Item</span><span class="sxs-lookup"><span data-stu-id="65704-108">Item</span></span>                                                   | <span data-ttu-id="65704-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="65704-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="65704-110"><span id="x"></span><span id="X"></span>*w.x.y.*</span><span class="sxs-lookup"><span data-stu-id="65704-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="65704-111">\[na \] entrada especificada.</span><span class="sxs-lookup"><span data-stu-id="65704-111">\[in\] The specified input.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="65704-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="65704-112">Return Value</span></span>

<span data-ttu-id="65704-113">O valor de entrada truncado para um componente de número inteiro.</span><span class="sxs-lookup"><span data-stu-id="65704-113">The input value truncated to an integer component.</span></span>

## <a name="remarks"></a><span data-ttu-id="65704-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="65704-114">Remarks</span></span>

<span data-ttu-id="65704-115">Essa função Trunca um valor de ponto flutuante para o componente de número inteiro.</span><span class="sxs-lookup"><span data-stu-id="65704-115">This function truncates a floating-point value to the integer component.</span></span> <span data-ttu-id="65704-116">Dado um valor de ponto flutuante de 1,6, a função TRUNC retornaria 1,0, onde como a função [**Round (DirectX HLSL)**](dx-graphics-hlsl-round.md) retornaria 2,0.</span><span class="sxs-lookup"><span data-stu-id="65704-116">Given a floating-point value of 1.6, the trunc function would return 1.0, where as the [**round (DirectX HLSL)**](dx-graphics-hlsl-round.md) function would return 2.0.</span></span>

## <a name="type-description"></a><span data-ttu-id="65704-117">Descrição do tipo</span><span class="sxs-lookup"><span data-stu-id="65704-117">Type Description</span></span>



| <span data-ttu-id="65704-118">Name</span><span class="sxs-lookup"><span data-stu-id="65704-118">Name</span></span> | [<span data-ttu-id="65704-119">**Tipo de modelo**</span><span class="sxs-lookup"><span data-stu-id="65704-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="65704-120">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="65704-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="65704-121">Tamanho</span><span class="sxs-lookup"><span data-stu-id="65704-121">Size</span></span>                         |
|------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|------------------------------|
| <span data-ttu-id="65704-122">*x*</span><span class="sxs-lookup"><span data-stu-id="65704-122">*x*</span></span>  | <span data-ttu-id="65704-123">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **vetor** ou **matriz**</span><span class="sxs-lookup"><span data-stu-id="65704-123">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="65704-124">**barra**</span><span class="sxs-lookup"><span data-stu-id="65704-124">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="65704-125">any</span><span class="sxs-lookup"><span data-stu-id="65704-125">any</span></span>                          |
| <span data-ttu-id="65704-126">RET</span><span class="sxs-lookup"><span data-stu-id="65704-126">ret</span></span>  | <span data-ttu-id="65704-127">Mesmo tipo que o x de entrada</span><span class="sxs-lookup"><span data-stu-id="65704-127">Same type as input x</span></span>                                                                                           | [<span data-ttu-id="65704-128">**barra**</span><span class="sxs-lookup"><span data-stu-id="65704-128">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="65704-129">Mesmas dimensões como entrada x</span><span class="sxs-lookup"><span data-stu-id="65704-129">Same dimension(s) as input x</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="65704-130">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="65704-130">Minimum Shader Model</span></span>

<span data-ttu-id="65704-131">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="65704-131">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="65704-132">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="65704-132">Shader Model</span></span>                                                                       | <span data-ttu-id="65704-133">Com suporte</span><span class="sxs-lookup"><span data-stu-id="65704-133">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="65704-134">[Modelo do sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="65704-134">[Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) and higher shader models</span></span> | <span data-ttu-id="65704-135">sim</span><span class="sxs-lookup"><span data-stu-id="65704-135">yes</span></span>       |



 

## <a name="requirements"></a><span data-ttu-id="65704-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65704-136">Requirements</span></span>



| <span data-ttu-id="65704-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="65704-137">Requirement</span></span> | <span data-ttu-id="65704-138">Valor</span><span class="sxs-lookup"><span data-stu-id="65704-138">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="65704-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="65704-139">Header</span></span><br/> | <dl> <span data-ttu-id="65704-140"><dt>Corecrt \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="65704-140"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65704-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="65704-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65704-142">**Funções intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="65704-142">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

