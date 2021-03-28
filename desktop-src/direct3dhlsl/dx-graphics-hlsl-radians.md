---
title: radianos
description: Converte o valor especificado de graus em radianos.
ms.assetid: 6fc6b1f8-b686-49ba-93ea-2b2470b3fc72
keywords:
- HLSL radianos
topic_type:
- apiref
api_name:
- radians
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 029c0ffe2838cdcc997e47cae4e0adafede4411d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366656"
---
# <a name="radians"></a><span data-ttu-id="3c0b4-104">radianos</span><span class="sxs-lookup"><span data-stu-id="3c0b4-104">radians</span></span>

<span data-ttu-id="3c0b4-105">Converte o valor especificado de graus em radianos.</span><span class="sxs-lookup"><span data-stu-id="3c0b4-105">Converts the specified value from degrees to radians.</span></span>



| <span data-ttu-id="3c0b4-106">radianos de *RET* (*x*)</span><span class="sxs-lookup"><span data-stu-id="3c0b4-106">*ret* radians(*x*)</span></span> |
|--------------------|



 

## <a name="parameters"></a><span data-ttu-id="3c0b4-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3c0b4-107">Parameters</span></span>



| <span data-ttu-id="3c0b4-108">Item</span><span class="sxs-lookup"><span data-stu-id="3c0b4-108">Item</span></span>                                                   | <span data-ttu-id="3c0b4-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="3c0b4-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="3c0b4-110"><span id="x"></span><span id="X"></span>*w.x.y.*</span><span class="sxs-lookup"><span data-stu-id="3c0b4-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="3c0b4-111">\[no \] valor especificado.</span><span class="sxs-lookup"><span data-stu-id="3c0b4-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="3c0b4-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="3c0b4-112">Return Value</span></span>

<span data-ttu-id="3c0b4-113">O parâmetro *x* convertido de graus em radianos.</span><span class="sxs-lookup"><span data-stu-id="3c0b4-113">The *x* parameter converted from degrees to radians.</span></span>

## <a name="type-description"></a><span data-ttu-id="3c0b4-114">Descrição do tipo</span><span class="sxs-lookup"><span data-stu-id="3c0b4-114">Type Description</span></span>



| <span data-ttu-id="3c0b4-115">Name</span><span class="sxs-lookup"><span data-stu-id="3c0b4-115">Name</span></span>  | [<span data-ttu-id="3c0b4-116">**Tipo de modelo**</span><span class="sxs-lookup"><span data-stu-id="3c0b4-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="3c0b4-117">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="3c0b4-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="3c0b4-118">Tamanho</span><span class="sxs-lookup"><span data-stu-id="3c0b4-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="3c0b4-119">*x*</span><span class="sxs-lookup"><span data-stu-id="3c0b4-119">*x*</span></span>   | <span data-ttu-id="3c0b4-120">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **vetor** ou **matriz**</span><span class="sxs-lookup"><span data-stu-id="3c0b4-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="3c0b4-121">**barra**</span><span class="sxs-lookup"><span data-stu-id="3c0b4-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="3c0b4-122">any</span><span class="sxs-lookup"><span data-stu-id="3c0b4-122">any</span></span>                            |
| <span data-ttu-id="3c0b4-123">*RET*</span><span class="sxs-lookup"><span data-stu-id="3c0b4-123">*ret*</span></span> | <span data-ttu-id="3c0b4-124">igual ao *x* de entrada</span><span class="sxs-lookup"><span data-stu-id="3c0b4-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="3c0b4-125">**barra**</span><span class="sxs-lookup"><span data-stu-id="3c0b4-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="3c0b4-126">mesmas dimensões como entrada *x*</span><span class="sxs-lookup"><span data-stu-id="3c0b4-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="3c0b4-127">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="3c0b4-127">Minimum Shader Model</span></span>

<span data-ttu-id="3c0b4-128">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="3c0b4-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="3c0b4-129">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="3c0b4-129">Shader Model</span></span>                                                                       | <span data-ttu-id="3c0b4-130">Com suporte</span><span class="sxs-lookup"><span data-stu-id="3c0b4-130">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="3c0b4-131">[Modelo do sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="3c0b4-131">[Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) and higher shader models</span></span> | <span data-ttu-id="3c0b4-132">sim</span><span class="sxs-lookup"><span data-stu-id="3c0b4-132">yes</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="3c0b4-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="3c0b4-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c0b4-134">**Funções intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="3c0b4-134">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

