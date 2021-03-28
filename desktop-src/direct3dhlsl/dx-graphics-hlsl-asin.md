---
title: asin
description: Retorna o arco seno do valor especificado.
ms.assetid: 49559cb2-3305-4c97-8071-1589bcca3a75
keywords:
- Asen HLSL
topic_type:
- apiref
api_name:
- asin
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a2f64865cb3172037f6630dc422a69aa4d135b1d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104008304"
---
# <a name="asin"></a><span data-ttu-id="ee6ee-104">asin</span><span class="sxs-lookup"><span data-stu-id="ee6ee-104">asin</span></span>

<span data-ttu-id="ee6ee-105">Retorna o arco seno do valor especificado.</span><span class="sxs-lookup"><span data-stu-id="ee6ee-105">Returns the arcsine of the specified value.</span></span>



| <span data-ttu-id="ee6ee-106">*RET* Asen (*x*)</span><span class="sxs-lookup"><span data-stu-id="ee6ee-106">*ret* asin(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="ee6ee-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ee6ee-107">Parameters</span></span>



| <span data-ttu-id="ee6ee-108">Item</span><span class="sxs-lookup"><span data-stu-id="ee6ee-108">Item</span></span>                                                   | <span data-ttu-id="ee6ee-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="ee6ee-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="ee6ee-110"><span id="x"></span><span id="X"></span>*w.x.y.*</span><span class="sxs-lookup"><span data-stu-id="ee6ee-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="ee6ee-111">\[no \] valor especificado.</span><span class="sxs-lookup"><span data-stu-id="ee6ee-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="ee6ee-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="ee6ee-112">Return Value</span></span>

<span data-ttu-id="ee6ee-113">O arco seno do parâmetro *x* .</span><span class="sxs-lookup"><span data-stu-id="ee6ee-113">The arcsine of the *x* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee6ee-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="ee6ee-114">Remarks</span></span>

<span data-ttu-id="ee6ee-115">Cada componente do parâmetro *x* deve estar dentro do intervalo de-π/2 a π/2.</span><span class="sxs-lookup"><span data-stu-id="ee6ee-115">Each component of the *x* parameter should be within the range of -π/2 to π/2.</span></span>

## <a name="type-description"></a><span data-ttu-id="ee6ee-116">Descrição do tipo</span><span class="sxs-lookup"><span data-stu-id="ee6ee-116">Type Description</span></span>



| <span data-ttu-id="ee6ee-117">Name</span><span class="sxs-lookup"><span data-stu-id="ee6ee-117">Name</span></span>  | [<span data-ttu-id="ee6ee-118">**Tipo de modelo**</span><span class="sxs-lookup"><span data-stu-id="ee6ee-118">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="ee6ee-119">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="ee6ee-119">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="ee6ee-120">Tamanho</span><span class="sxs-lookup"><span data-stu-id="ee6ee-120">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="ee6ee-121">*x*</span><span class="sxs-lookup"><span data-stu-id="ee6ee-121">*x*</span></span>   | <span data-ttu-id="ee6ee-122">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **vetor** ou **matriz**</span><span class="sxs-lookup"><span data-stu-id="ee6ee-122">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="ee6ee-123">**barra**</span><span class="sxs-lookup"><span data-stu-id="ee6ee-123">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="ee6ee-124">any</span><span class="sxs-lookup"><span data-stu-id="ee6ee-124">any</span></span>                            |
| <span data-ttu-id="ee6ee-125">*RET*</span><span class="sxs-lookup"><span data-stu-id="ee6ee-125">*ret*</span></span> | <span data-ttu-id="ee6ee-126">igual ao *x* de entrada</span><span class="sxs-lookup"><span data-stu-id="ee6ee-126">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="ee6ee-127">**barra**</span><span class="sxs-lookup"><span data-stu-id="ee6ee-127">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="ee6ee-128">mesmas dimensões como entrada *x*</span><span class="sxs-lookup"><span data-stu-id="ee6ee-128">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="ee6ee-129">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="ee6ee-129">Minimum Shader Model</span></span>

<span data-ttu-id="ee6ee-130">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="ee6ee-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="ee6ee-131">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="ee6ee-131">Shader Model</span></span>                                                                       | <span data-ttu-id="ee6ee-132">Com suporte</span><span class="sxs-lookup"><span data-stu-id="ee6ee-132">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="ee6ee-133">[Modelo do sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="ee6ee-133">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="ee6ee-134">sim</span><span class="sxs-lookup"><span data-stu-id="ee6ee-134">yes</span></span>       |
| [<span data-ttu-id="ee6ee-135">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ee6ee-135">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="ee6ee-136">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="ee6ee-136">vs\_1\_1</span></span>  |



 

## <a name="see-also"></a><span data-ttu-id="ee6ee-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="ee6ee-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee6ee-138">**Funções intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="ee6ee-138">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

