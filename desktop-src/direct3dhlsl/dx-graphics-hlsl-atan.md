---
title: atan
description: Retorna o arco tangente do valor especificado.
ms.assetid: e3ce3ac3-1012-414f-a193-102208083e39
keywords:
- ATAN HLSL
topic_type:
- apiref
api_name:
- atan
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 290ced1e5100e3bbc780fab6ab984deaca38528f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641241"
---
# <a name="atan"></a><span data-ttu-id="371c7-104">atan</span><span class="sxs-lookup"><span data-stu-id="371c7-104">atan</span></span>

<span data-ttu-id="371c7-105">Retorna o arco tangente do valor especificado.</span><span class="sxs-lookup"><span data-stu-id="371c7-105">Returns the arctangent of the specified value.</span></span>



| <span data-ttu-id="371c7-106">*RET* ATAN (*x*)</span><span class="sxs-lookup"><span data-stu-id="371c7-106">*ret* atan(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="371c7-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="371c7-107">Parameters</span></span>



| <span data-ttu-id="371c7-108">Item</span><span class="sxs-lookup"><span data-stu-id="371c7-108">Item</span></span>                                                   | <span data-ttu-id="371c7-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="371c7-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="371c7-110"><span id="x"></span><span id="X"></span>*w.x.y.*</span><span class="sxs-lookup"><span data-stu-id="371c7-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="371c7-111">\[no \] valor especificado.</span><span class="sxs-lookup"><span data-stu-id="371c7-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="371c7-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="371c7-112">Return Value</span></span>

<span data-ttu-id="371c7-113">O arco tangente do parâmetro *x* .</span><span class="sxs-lookup"><span data-stu-id="371c7-113">The arctangent of the *x* parameter.</span></span> <span data-ttu-id="371c7-114">Esse valor está dentro do intervalo de-π/2 a π/2.</span><span class="sxs-lookup"><span data-stu-id="371c7-114">This value is within the range of -π/2 to π/2.</span></span>

## <a name="type-description"></a><span data-ttu-id="371c7-115">Descrição do tipo</span><span class="sxs-lookup"><span data-stu-id="371c7-115">Type Description</span></span>



| <span data-ttu-id="371c7-116">Name</span><span class="sxs-lookup"><span data-stu-id="371c7-116">Name</span></span>  | [<span data-ttu-id="371c7-117">**Tipo de modelo**</span><span class="sxs-lookup"><span data-stu-id="371c7-117">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="371c7-118">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="371c7-118">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="371c7-119">Tamanho</span><span class="sxs-lookup"><span data-stu-id="371c7-119">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="371c7-120">*x*</span><span class="sxs-lookup"><span data-stu-id="371c7-120">*x*</span></span>   | <span data-ttu-id="371c7-121">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **vetor** ou **matriz**</span><span class="sxs-lookup"><span data-stu-id="371c7-121">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="371c7-122">**barra**</span><span class="sxs-lookup"><span data-stu-id="371c7-122">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="371c7-123">any</span><span class="sxs-lookup"><span data-stu-id="371c7-123">any</span></span>                            |
| <span data-ttu-id="371c7-124">*RET*</span><span class="sxs-lookup"><span data-stu-id="371c7-124">*ret*</span></span> | <span data-ttu-id="371c7-125">igual ao *x* de entrada</span><span class="sxs-lookup"><span data-stu-id="371c7-125">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="371c7-126">**barra**</span><span class="sxs-lookup"><span data-stu-id="371c7-126">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="371c7-127">mesmas dimensões como entrada *x*</span><span class="sxs-lookup"><span data-stu-id="371c7-127">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="371c7-128">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="371c7-128">Minimum Shader Model</span></span>

<span data-ttu-id="371c7-129">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="371c7-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="371c7-130">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="371c7-130">Shader Model</span></span>                                                                       | <span data-ttu-id="371c7-131">Com suporte</span><span class="sxs-lookup"><span data-stu-id="371c7-131">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="371c7-132">[Modelo do sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="371c7-132">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="371c7-133">sim</span><span class="sxs-lookup"><span data-stu-id="371c7-133">yes</span></span>       |
| [<span data-ttu-id="371c7-134">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="371c7-134">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="371c7-135">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="371c7-135">vs\_1\_1</span></span>  |



 

## <a name="see-also"></a><span data-ttu-id="371c7-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="371c7-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="371c7-137">**Funções intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="371c7-137">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

