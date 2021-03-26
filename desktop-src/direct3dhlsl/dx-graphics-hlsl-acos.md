---
title: acos
description: Retorna o arco cosseno do valor especificado.
ms.assetid: c9bc33b8-d586-4c64-9453-5ab97396f2cf
keywords:
- HLSL de acos
topic_type:
- apiref
api_name:
- acos
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2cd909c4a4c1300374bba723f1edabb48d51b2e0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084848"
---
# <a name="acos"></a><span data-ttu-id="78260-104">acos</span><span class="sxs-lookup"><span data-stu-id="78260-104">acos</span></span>

<span data-ttu-id="78260-105">Retorna o arco cosseno do valor especificado.</span><span class="sxs-lookup"><span data-stu-id="78260-105">Returns the arccosine of the specified value.</span></span>



| <span data-ttu-id="78260-106">acos de *RET* (*x*)</span><span class="sxs-lookup"><span data-stu-id="78260-106">*ret* acos(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="78260-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="78260-107">Parameters</span></span>



| <span data-ttu-id="78260-108">Item</span><span class="sxs-lookup"><span data-stu-id="78260-108">Item</span></span>                                                   | <span data-ttu-id="78260-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="78260-109">Description</span></span>                                                                                                         |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78260-110"><span id="x"></span><span id="X"></span>*w.x.y.*</span><span class="sxs-lookup"><span data-stu-id="78260-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="78260-111">\[no \] valor especificado.</span><span class="sxs-lookup"><span data-stu-id="78260-111">\[in\] The specified value.</span></span> <span data-ttu-id="78260-112">Cada componente deve ser um valor de ponto flutuante dentro do intervalo de-1 a 1.</span><span class="sxs-lookup"><span data-stu-id="78260-112">Each component should be a floating-point value within the range of -1 to 1.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="78260-113">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="78260-113">Return Value</span></span>

<span data-ttu-id="78260-114">O arco cosseno do parâmetro *x* .</span><span class="sxs-lookup"><span data-stu-id="78260-114">The arccosine of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="78260-115">Descrição do tipo</span><span class="sxs-lookup"><span data-stu-id="78260-115">Type Description</span></span>



| <span data-ttu-id="78260-116">Name</span><span class="sxs-lookup"><span data-stu-id="78260-116">Name</span></span>  | [<span data-ttu-id="78260-117">**Tipo de modelo**</span><span class="sxs-lookup"><span data-stu-id="78260-117">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="78260-118">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="78260-118">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="78260-119">Tamanho</span><span class="sxs-lookup"><span data-stu-id="78260-119">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="78260-120">*x*</span><span class="sxs-lookup"><span data-stu-id="78260-120">*x*</span></span>   | <span data-ttu-id="78260-121">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **vetor** ou **matriz**</span><span class="sxs-lookup"><span data-stu-id="78260-121">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="78260-122">**barra**</span><span class="sxs-lookup"><span data-stu-id="78260-122">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="78260-123">any</span><span class="sxs-lookup"><span data-stu-id="78260-123">any</span></span>                            |
| <span data-ttu-id="78260-124">*RET*</span><span class="sxs-lookup"><span data-stu-id="78260-124">*ret*</span></span> | <span data-ttu-id="78260-125">igual ao *x* de entrada</span><span class="sxs-lookup"><span data-stu-id="78260-125">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="78260-126">**barra**</span><span class="sxs-lookup"><span data-stu-id="78260-126">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="78260-127">mesmas dimensões como entrada *x*</span><span class="sxs-lookup"><span data-stu-id="78260-127">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="78260-128">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="78260-128">Minimum Shader Model</span></span>

<span data-ttu-id="78260-129">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="78260-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="78260-130">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="78260-130">Shader Model</span></span>                                                                       | <span data-ttu-id="78260-131">Com suporte</span><span class="sxs-lookup"><span data-stu-id="78260-131">Supported</span></span>     |
|------------------------------------------------------------------------------------|---------------|
| <span data-ttu-id="78260-132">[Modelo do sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="78260-132">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="78260-133">sim</span><span class="sxs-lookup"><span data-stu-id="78260-133">yes</span></span>           |
| [<span data-ttu-id="78260-134">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="78260-134">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="78260-135">\_apenas vs 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="78260-135">vs\_1\_1 only</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="78260-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="78260-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78260-137">**Funções intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="78260-137">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

