---
title: sin
description: Retorna o seno do valor especificado.
ms.assetid: e1c3ead8-73dd-4798-8553-1a42dbaefe8e
keywords:
- HLSL Sin
topic_type:
- apiref
api_name:
- sin
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d48332d35052a893dcb348a70e4d464a6bbfe0c9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366558"
---
# <a name="sin"></a><span data-ttu-id="4ca35-104">sin</span><span class="sxs-lookup"><span data-stu-id="4ca35-104">sin</span></span>

<span data-ttu-id="4ca35-105">Retorna o seno do valor especificado.</span><span class="sxs-lookup"><span data-stu-id="4ca35-105">Returns the sine of the specified value.</span></span>



| <span data-ttu-id="4ca35-106">Sen *RET* (*x*)</span><span class="sxs-lookup"><span data-stu-id="4ca35-106">*ret* sin(*x*)</span></span> |
|----------------|



 

## <a name="parameters"></a><span data-ttu-id="4ca35-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4ca35-107">Parameters</span></span>



| <span data-ttu-id="4ca35-108">Item</span><span class="sxs-lookup"><span data-stu-id="4ca35-108">Item</span></span>                                                   | <span data-ttu-id="4ca35-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="4ca35-109">Description</span></span>                                        |
|--------------------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="4ca35-110"><span id="x"></span><span id="X"></span>*w.x.y.*</span><span class="sxs-lookup"><span data-stu-id="4ca35-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="4ca35-111">\[no \] valor especificado, em radianos.</span><span class="sxs-lookup"><span data-stu-id="4ca35-111">\[in\] The specified value, in radians.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="4ca35-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="4ca35-112">Return Value</span></span>

<span data-ttu-id="4ca35-113">O seno do parâmetro *x* .</span><span class="sxs-lookup"><span data-stu-id="4ca35-113">The sine of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="4ca35-114">Descrição do tipo</span><span class="sxs-lookup"><span data-stu-id="4ca35-114">Type Description</span></span>



| <span data-ttu-id="4ca35-115">Name</span><span class="sxs-lookup"><span data-stu-id="4ca35-115">Name</span></span>  | [<span data-ttu-id="4ca35-116">**Tipo de modelo**</span><span class="sxs-lookup"><span data-stu-id="4ca35-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="4ca35-117">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="4ca35-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="4ca35-118">Tamanho</span><span class="sxs-lookup"><span data-stu-id="4ca35-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="4ca35-119">*x*</span><span class="sxs-lookup"><span data-stu-id="4ca35-119">*x*</span></span>   | <span data-ttu-id="4ca35-120">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **vetor** ou **matriz**</span><span class="sxs-lookup"><span data-stu-id="4ca35-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="4ca35-121">**barra**</span><span class="sxs-lookup"><span data-stu-id="4ca35-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="4ca35-122">any</span><span class="sxs-lookup"><span data-stu-id="4ca35-122">any</span></span>                            |
| <span data-ttu-id="4ca35-123">*RET*</span><span class="sxs-lookup"><span data-stu-id="4ca35-123">*ret*</span></span> | <span data-ttu-id="4ca35-124">igual ao *x* de entrada</span><span class="sxs-lookup"><span data-stu-id="4ca35-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="4ca35-125">**barra**</span><span class="sxs-lookup"><span data-stu-id="4ca35-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="4ca35-126">mesmas dimensões como entrada *x*</span><span class="sxs-lookup"><span data-stu-id="4ca35-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="4ca35-127">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="4ca35-127">Minimum Shader Model</span></span>

<span data-ttu-id="4ca35-128">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="4ca35-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="4ca35-129">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="4ca35-129">Shader Model</span></span>                                                                       | <span data-ttu-id="4ca35-130">Com suporte</span><span class="sxs-lookup"><span data-stu-id="4ca35-130">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="4ca35-131">[Modelo do sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="4ca35-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="4ca35-132">sim</span><span class="sxs-lookup"><span data-stu-id="4ca35-132">yes</span></span>                 |
| [<span data-ttu-id="4ca35-133">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4ca35-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="4ca35-134">Sim ( \_ apenas vs 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="4ca35-134">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="4ca35-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="4ca35-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ca35-136">**Funções intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="4ca35-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

