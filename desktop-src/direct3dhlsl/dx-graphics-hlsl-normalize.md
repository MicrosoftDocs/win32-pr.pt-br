---
title: normaliza
description: Normaliza o vetor de ponto flutuante especificado de acordo com x/Length (x).
ms.assetid: 7fd6f8ff-f3ff-4d14-b3fc-b44fdddf6c75
keywords:
- normalizar HLSL
topic_type:
- apiref
api_name:
- normalize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f48c78f80f5f92f950795018f05a46c7883d9736
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917646"
---
# <a name="normalize"></a><span data-ttu-id="3c347-104">normaliza</span><span class="sxs-lookup"><span data-stu-id="3c347-104">normalize</span></span>

<span data-ttu-id="3c347-105">Normaliza o vetor de ponto flutuante especificado de acordo com x/Length (x).</span><span class="sxs-lookup"><span data-stu-id="3c347-105">Normalizes the specified floating-point vector according to x / length(x).</span></span>



| <span data-ttu-id="3c347-106">Normalize. de *RET* (*x*)</span><span class="sxs-lookup"><span data-stu-id="3c347-106">*ret* normalize(*x*)</span></span> |
|----------------------|



 

## <a name="parameters"></a><span data-ttu-id="3c347-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3c347-107">Parameters</span></span>



| <span data-ttu-id="3c347-108">Item</span><span class="sxs-lookup"><span data-stu-id="3c347-108">Item</span></span>                                                   | <span data-ttu-id="3c347-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="3c347-109">Description</span></span>                                            |
|--------------------------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="3c347-110"><span id="x"></span><span id="X"></span>*w.x.y.*</span><span class="sxs-lookup"><span data-stu-id="3c347-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="3c347-111">\[no \] vetor de ponto flutuante especificado.</span><span class="sxs-lookup"><span data-stu-id="3c347-111">\[in\] The specified floating-point vector.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="3c347-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="3c347-112">Return Value</span></span>

<span data-ttu-id="3c347-113">O parâmetro *x* normalizado.</span><span class="sxs-lookup"><span data-stu-id="3c347-113">The normalized *x* parameter.</span></span> <span data-ttu-id="3c347-114">Se o comprimento do parâmetro *x* for 0, o resultado será indefinido.</span><span class="sxs-lookup"><span data-stu-id="3c347-114">If the length of the *x* parameter is 0, the result is indefinite.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c347-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="3c347-115">Remarks</span></span>

<span data-ttu-id="3c347-116">A função intrínseca **Normalize** HLSL usa a seguinte fórmula: *x*  /  [**comprimento**](dx-graphics-hlsl-length.md)(*x*).</span><span class="sxs-lookup"><span data-stu-id="3c347-116">The **normalize** HLSL intrinsic function uses the following formula: *x* / [**length**](dx-graphics-hlsl-length.md)(*x*).</span></span>

## <a name="type-description"></a><span data-ttu-id="3c347-117">Descrição do tipo</span><span class="sxs-lookup"><span data-stu-id="3c347-117">Type Description</span></span>



| <span data-ttu-id="3c347-118">Name</span><span class="sxs-lookup"><span data-stu-id="3c347-118">Name</span></span>  | [<span data-ttu-id="3c347-119">**Tipo de modelo**</span><span class="sxs-lookup"><span data-stu-id="3c347-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="3c347-120">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="3c347-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="3c347-121">Tamanho</span><span class="sxs-lookup"><span data-stu-id="3c347-121">Size</span></span>                           |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="3c347-122">*x*</span><span class="sxs-lookup"><span data-stu-id="3c347-122">*x*</span></span>   | [<span data-ttu-id="3c347-123">**vetor**</span><span class="sxs-lookup"><span data-stu-id="3c347-123">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="3c347-124">**barra**</span><span class="sxs-lookup"><span data-stu-id="3c347-124">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="3c347-125">any</span><span class="sxs-lookup"><span data-stu-id="3c347-125">any</span></span>                            |
| <span data-ttu-id="3c347-126">*RET*</span><span class="sxs-lookup"><span data-stu-id="3c347-126">*ret*</span></span> | <span data-ttu-id="3c347-127">igual ao *x* de entrada</span><span class="sxs-lookup"><span data-stu-id="3c347-127">same as input *x*</span></span>                                                                   | [<span data-ttu-id="3c347-128">**barra**</span><span class="sxs-lookup"><span data-stu-id="3c347-128">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="3c347-129">mesmas dimensões como entrada *x*</span><span class="sxs-lookup"><span data-stu-id="3c347-129">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="3c347-130">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="3c347-130">Minimum Shader Model</span></span>

<span data-ttu-id="3c347-131">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="3c347-131">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="3c347-132">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="3c347-132">Shader Model</span></span>                                                                       | <span data-ttu-id="3c347-133">Com suporte</span><span class="sxs-lookup"><span data-stu-id="3c347-133">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="3c347-134">[Modelo do sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="3c347-134">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="3c347-135">sim</span><span class="sxs-lookup"><span data-stu-id="3c347-135">yes</span></span>                 |
| [<span data-ttu-id="3c347-136">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3c347-136">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="3c347-137">Sim ( \_ apenas vs 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="3c347-137">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="3c347-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="3c347-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c347-139">**Funções intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="3c347-139">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

