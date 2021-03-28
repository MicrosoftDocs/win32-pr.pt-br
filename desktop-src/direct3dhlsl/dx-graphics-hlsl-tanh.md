---
title: tanh
description: Retorna a tangente hiperbólica do valor especificado.
ms.assetid: e2d27aa0-5e03-4f2f-a29c-884711710c8d
keywords:
- Tanh HLSL
topic_type:
- apiref
api_name:
- tanh
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7c5312aaac6d6f164e940f99183e61688b393fbd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007744"
---
# <a name="tanh"></a><span data-ttu-id="3860d-104">tanh</span><span class="sxs-lookup"><span data-stu-id="3860d-104">tanh</span></span>

<span data-ttu-id="3860d-105">Retorna a tangente hiperbólica do valor especificado.</span><span class="sxs-lookup"><span data-stu-id="3860d-105">Returns the hyperbolic tangent of the specified value.</span></span>



| <span data-ttu-id="3860d-106">Tanh de *RET* (*x*)</span><span class="sxs-lookup"><span data-stu-id="3860d-106">*ret* tanh(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="3860d-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3860d-107">Parameters</span></span>



| <span data-ttu-id="3860d-108">Item</span><span class="sxs-lookup"><span data-stu-id="3860d-108">Item</span></span>                                                   | <span data-ttu-id="3860d-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="3860d-109">Description</span></span>                                        |
|--------------------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="3860d-110"><span id="x"></span><span id="X"></span>*w.x.y.*</span><span class="sxs-lookup"><span data-stu-id="3860d-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="3860d-111">\[no \] valor especificado, em radianos.</span><span class="sxs-lookup"><span data-stu-id="3860d-111">\[in\] The specified value, in radians.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="3860d-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="3860d-112">Return Value</span></span>

<span data-ttu-id="3860d-113">A tangente hiperbólica do parâmetro *x* .</span><span class="sxs-lookup"><span data-stu-id="3860d-113">The hyperbolic tangent of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="3860d-114">Descrição do tipo</span><span class="sxs-lookup"><span data-stu-id="3860d-114">Type Description</span></span>



| <span data-ttu-id="3860d-115">Name</span><span class="sxs-lookup"><span data-stu-id="3860d-115">Name</span></span>  | [<span data-ttu-id="3860d-116">**Tipo de modelo**</span><span class="sxs-lookup"><span data-stu-id="3860d-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="3860d-117">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="3860d-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="3860d-118">Tamanho</span><span class="sxs-lookup"><span data-stu-id="3860d-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="3860d-119">*x*</span><span class="sxs-lookup"><span data-stu-id="3860d-119">*x*</span></span>   | <span data-ttu-id="3860d-120">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **vetor** ou **matriz**</span><span class="sxs-lookup"><span data-stu-id="3860d-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="3860d-121">**barra**</span><span class="sxs-lookup"><span data-stu-id="3860d-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="3860d-122">any</span><span class="sxs-lookup"><span data-stu-id="3860d-122">any</span></span>                            |
| <span data-ttu-id="3860d-123">*RET*</span><span class="sxs-lookup"><span data-stu-id="3860d-123">*ret*</span></span> | <span data-ttu-id="3860d-124">igual ao *x* de entrada</span><span class="sxs-lookup"><span data-stu-id="3860d-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="3860d-125">**barra**</span><span class="sxs-lookup"><span data-stu-id="3860d-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="3860d-126">mesmas dimensões como entrada *x*</span><span class="sxs-lookup"><span data-stu-id="3860d-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="3860d-127">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="3860d-127">Minimum Shader Model</span></span>

<span data-ttu-id="3860d-128">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="3860d-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="3860d-129">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="3860d-129">Shader Model</span></span>                                                                       | <span data-ttu-id="3860d-130">Com suporte</span><span class="sxs-lookup"><span data-stu-id="3860d-130">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="3860d-131">[Modelo do sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="3860d-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="3860d-132">sim</span><span class="sxs-lookup"><span data-stu-id="3860d-132">yes</span></span>                 |
| [<span data-ttu-id="3860d-133">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3860d-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="3860d-134">Sim ( \_ apenas vs 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="3860d-134">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="3860d-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="3860d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3860d-136">**Funções intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="3860d-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

