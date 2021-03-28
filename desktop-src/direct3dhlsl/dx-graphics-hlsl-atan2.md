---
title: atan2 (Corecrt \_ Math. h)
description: Retorna o arco tangente de dois valores (x, y).
ms.assetid: e7b53751-f321-4390-8f8f-ec1fa3aaa798
keywords:
- atan2 HLSL
topic_type:
- apiref
api_name:
- atan2
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52fbc6574d0fc0d53a165ae7da87c2627a295be4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104172992"
---
# <a name="atan2"></a><span data-ttu-id="64d8f-104">atan2</span><span class="sxs-lookup"><span data-stu-id="64d8f-104">atan2</span></span>

<span data-ttu-id="64d8f-105">Retorna o arco tangente de dois valores (x, y).</span><span class="sxs-lookup"><span data-stu-id="64d8f-105">Returns the arctangent of two values (x,y).</span></span>



| <span data-ttu-id="64d8f-106">*RET* ATAN2 (*y*, *x*)</span><span class="sxs-lookup"><span data-stu-id="64d8f-106">*ret* atan2(*y*, *x*)</span></span> |
|-----------------------|



 

## <a name="parameters"></a><span data-ttu-id="64d8f-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="64d8f-107">Parameters</span></span>



| <span data-ttu-id="64d8f-108">Item</span><span class="sxs-lookup"><span data-stu-id="64d8f-108">Item</span></span>                                                   | <span data-ttu-id="64d8f-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="64d8f-109">Description</span></span>                    |
|--------------------------------------------------------|--------------------------------|
| <span data-ttu-id="64d8f-110"><span id="y"></span><span id="Y"></span>*Iar*</span><span class="sxs-lookup"><span data-stu-id="64d8f-110"><span id="y"></span><span id="Y"></span>*y*</span></span><br/> | <span data-ttu-id="64d8f-111">\[no \] valor y.</span><span class="sxs-lookup"><span data-stu-id="64d8f-111">\[in\] The y value.</span></span><br/> |
| <span data-ttu-id="64d8f-112"><span id="x"></span><span id="X"></span>*w.x.y.*</span><span class="sxs-lookup"><span data-stu-id="64d8f-112"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="64d8f-113">\[no \] valor x.</span><span class="sxs-lookup"><span data-stu-id="64d8f-113">\[in\] The x value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="64d8f-114">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="64d8f-114">Return Value</span></span>

<span data-ttu-id="64d8f-115">O arco tangente de (y, x).</span><span class="sxs-lookup"><span data-stu-id="64d8f-115">The arctangent of (y,x).</span></span>

## <a name="remarks"></a><span data-ttu-id="64d8f-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="64d8f-116">Remarks</span></span>

<span data-ttu-id="64d8f-117">Os sinais dos parâmetros *x* e *y* são usados para determinar o quadrante dos valores de retorno dentro do intervalo de-π a π.</span><span class="sxs-lookup"><span data-stu-id="64d8f-117">The signs of the *x* and *y* parameters are used to determine the quadrant of the return values within the range of -π to π.</span></span> <span data-ttu-id="64d8f-118">A função intrínseca **ATAN2** HLSL é bem definida para cada ponto que não seja a origem, mesmo se *y* for igual a 0 e *x* for igual a 0.</span><span class="sxs-lookup"><span data-stu-id="64d8f-118">The **atan2** HLSL intrinsic function is well-defined for every point other than the origin, even if *y* equals 0 and *x* does not equal 0.</span></span>

## <a name="type-description"></a><span data-ttu-id="64d8f-119">Descrição do tipo</span><span class="sxs-lookup"><span data-stu-id="64d8f-119">Type Description</span></span>



| <span data-ttu-id="64d8f-120">Name</span><span class="sxs-lookup"><span data-stu-id="64d8f-120">Name</span></span>  | [<span data-ttu-id="64d8f-121">**Tipo de modelo**</span><span class="sxs-lookup"><span data-stu-id="64d8f-121">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="64d8f-122">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="64d8f-122">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="64d8f-123">Tamanho</span><span class="sxs-lookup"><span data-stu-id="64d8f-123">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="64d8f-124">*y*</span><span class="sxs-lookup"><span data-stu-id="64d8f-124">*y*</span></span>   | <span data-ttu-id="64d8f-125">igual ao *x* de entrada</span><span class="sxs-lookup"><span data-stu-id="64d8f-125">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="64d8f-126">**barra**</span><span class="sxs-lookup"><span data-stu-id="64d8f-126">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="64d8f-127">mesmas dimensões como entrada *x*</span><span class="sxs-lookup"><span data-stu-id="64d8f-127">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="64d8f-128">*x*</span><span class="sxs-lookup"><span data-stu-id="64d8f-128">*x*</span></span>   | <span data-ttu-id="64d8f-129">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **vetor** ou **matriz**</span><span class="sxs-lookup"><span data-stu-id="64d8f-129">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="64d8f-130">**barra**</span><span class="sxs-lookup"><span data-stu-id="64d8f-130">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="64d8f-131">any</span><span class="sxs-lookup"><span data-stu-id="64d8f-131">any</span></span>                            |
| <span data-ttu-id="64d8f-132">*RET*</span><span class="sxs-lookup"><span data-stu-id="64d8f-132">*ret*</span></span> | <span data-ttu-id="64d8f-133">igual ao *x* de entrada</span><span class="sxs-lookup"><span data-stu-id="64d8f-133">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="64d8f-134">**barra**</span><span class="sxs-lookup"><span data-stu-id="64d8f-134">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="64d8f-135">mesmas dimensões como entrada *x*</span><span class="sxs-lookup"><span data-stu-id="64d8f-135">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="64d8f-136">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="64d8f-136">Minimum Shader Model</span></span>

<span data-ttu-id="64d8f-137">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="64d8f-137">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="64d8f-138">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="64d8f-138">Shader Model</span></span>                                                                       | <span data-ttu-id="64d8f-139">Com suporte</span><span class="sxs-lookup"><span data-stu-id="64d8f-139">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="64d8f-140">[Modelo do sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="64d8f-140">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="64d8f-141">sim</span><span class="sxs-lookup"><span data-stu-id="64d8f-141">yes</span></span>       |
| [<span data-ttu-id="64d8f-142">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="64d8f-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="64d8f-143">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="64d8f-143">vs\_1\_1</span></span>  |



 

## <a name="requirements"></a><span data-ttu-id="64d8f-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="64d8f-144">Requirements</span></span>



| <span data-ttu-id="64d8f-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="64d8f-145">Requirement</span></span> | <span data-ttu-id="64d8f-146">Valor</span><span class="sxs-lookup"><span data-stu-id="64d8f-146">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="64d8f-147">parâmetro</span><span class="sxs-lookup"><span data-stu-id="64d8f-147">Header</span></span><br/> | <dl> <span data-ttu-id="64d8f-148"><dt>Corecrt \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="64d8f-148"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64d8f-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="64d8f-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64d8f-150">**Funções intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="64d8f-150">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

