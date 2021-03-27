---
title: rsqrt
description: Retorna o recíproco da raiz quadrada do valor especificado.
ms.assetid: 4e266e41-cde9-4a59-8937-98bfc63f3b5d
keywords:
- rsqrt HLSL
topic_type:
- apiref
api_name:
- rsqrt
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 56eb5f1cba8510e57a2c4b5622e10dc91666b6a6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104988670"
---
# <a name="rsqrt"></a><span data-ttu-id="c5b0f-104">rsqrt</span><span class="sxs-lookup"><span data-stu-id="c5b0f-104">rsqrt</span></span>

<span data-ttu-id="c5b0f-105">Retorna o recíproco da raiz quadrada do valor especificado.</span><span class="sxs-lookup"><span data-stu-id="c5b0f-105">Returns the reciprocal of the square root of the specified value.</span></span>



| <span data-ttu-id="c5b0f-106">*RET* rsqrt (*x*)</span><span class="sxs-lookup"><span data-stu-id="c5b0f-106">*ret* rsqrt(*x*)</span></span> |
|------------------|



 

## <a name="parameters"></a><span data-ttu-id="c5b0f-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c5b0f-107">Parameters</span></span>



| <span data-ttu-id="c5b0f-108">Item</span><span class="sxs-lookup"><span data-stu-id="c5b0f-108">Item</span></span>                                                   | <span data-ttu-id="c5b0f-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="c5b0f-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="c5b0f-110"><span id="x"></span><span id="X"></span>*w.x.y.*</span><span class="sxs-lookup"><span data-stu-id="c5b0f-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="c5b0f-111">\[no \] valor especificado.</span><span class="sxs-lookup"><span data-stu-id="c5b0f-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="c5b0f-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="c5b0f-112">Return Value</span></span>

<span data-ttu-id="c5b0f-113">O recíproco da raiz quadrada do parâmetro *x* .</span><span class="sxs-lookup"><span data-stu-id="c5b0f-113">The reciprocal of the square root of the *x* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5b0f-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="c5b0f-114">Remarks</span></span>

<span data-ttu-id="c5b0f-115">Essa função usa a seguinte fórmula: 1/ **sqrt**(*x*).</span><span class="sxs-lookup"><span data-stu-id="c5b0f-115">This function uses the following formula: 1 / **sqrt**(*x*).</span></span>

## <a name="type-description"></a><span data-ttu-id="c5b0f-116">Descrição do tipo</span><span class="sxs-lookup"><span data-stu-id="c5b0f-116">Type Description</span></span>



| <span data-ttu-id="c5b0f-117">Name</span><span class="sxs-lookup"><span data-stu-id="c5b0f-117">Name</span></span>  | [<span data-ttu-id="c5b0f-118">**Tipo de modelo**</span><span class="sxs-lookup"><span data-stu-id="c5b0f-118">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="c5b0f-119">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="c5b0f-119">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="c5b0f-120">Tamanho</span><span class="sxs-lookup"><span data-stu-id="c5b0f-120">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="c5b0f-121">*x*</span><span class="sxs-lookup"><span data-stu-id="c5b0f-121">*x*</span></span>   | <span data-ttu-id="c5b0f-122">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **vetor** ou **matriz**</span><span class="sxs-lookup"><span data-stu-id="c5b0f-122">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="c5b0f-123">**barra**</span><span class="sxs-lookup"><span data-stu-id="c5b0f-123">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="c5b0f-124">any</span><span class="sxs-lookup"><span data-stu-id="c5b0f-124">any</span></span>                            |
| <span data-ttu-id="c5b0f-125">*RET*</span><span class="sxs-lookup"><span data-stu-id="c5b0f-125">*ret*</span></span> | <span data-ttu-id="c5b0f-126">igual ao *x* de entrada</span><span class="sxs-lookup"><span data-stu-id="c5b0f-126">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="c5b0f-127">**barra**</span><span class="sxs-lookup"><span data-stu-id="c5b0f-127">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="c5b0f-128">mesmas dimensões como entrada *x*</span><span class="sxs-lookup"><span data-stu-id="c5b0f-128">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="c5b0f-129">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="c5b0f-129">Minimum Shader Model</span></span>

<span data-ttu-id="c5b0f-130">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="c5b0f-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="c5b0f-131">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="c5b0f-131">Shader Model</span></span>                                                                       | <span data-ttu-id="c5b0f-132">Com suporte</span><span class="sxs-lookup"><span data-stu-id="c5b0f-132">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="c5b0f-133">[Modelo do sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="c5b0f-133">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="c5b0f-134">sim</span><span class="sxs-lookup"><span data-stu-id="c5b0f-134">yes</span></span>                 |
| [<span data-ttu-id="c5b0f-135">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c5b0f-135">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="c5b0f-136">Sim ( \_ apenas vs 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="c5b0f-136">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="c5b0f-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="c5b0f-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5b0f-138">**Funções intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="c5b0f-138">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

