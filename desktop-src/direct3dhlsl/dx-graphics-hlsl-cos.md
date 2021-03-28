---
title: cos
description: Retorna o cosseno do valor especificado.
ms.assetid: 96c15702-98be-45bc-9abc-60ccc3c217b6
keywords:
- HLSL de cos
topic_type:
- apiref
api_name:
- cos
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4f5c0f4f071d47102c673301a397bfe3ecf178e4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366659"
---
# <a name="cos"></a><span data-ttu-id="74514-104">cos</span><span class="sxs-lookup"><span data-stu-id="74514-104">cos</span></span>

<span data-ttu-id="74514-105">Retorna o cosseno do valor especificado.</span><span class="sxs-lookup"><span data-stu-id="74514-105">Returns the cosine of the specified value.</span></span>



| <span data-ttu-id="74514-106">*RET* cos (*x*)</span><span class="sxs-lookup"><span data-stu-id="74514-106">*ret* cos(*x*)</span></span> |
|----------------|



 

## <a name="parameters"></a><span data-ttu-id="74514-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="74514-107">Parameters</span></span>



| <span data-ttu-id="74514-108">Item</span><span class="sxs-lookup"><span data-stu-id="74514-108">Item</span></span>                                                   | <span data-ttu-id="74514-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="74514-109">Description</span></span>                                        |
|--------------------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="74514-110"><span id="x"></span><span id="X"></span>*w.x.y.*</span><span class="sxs-lookup"><span data-stu-id="74514-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="74514-111">\[no \] valor especificado, em radianos.</span><span class="sxs-lookup"><span data-stu-id="74514-111">\[in\] The specified value, in radians.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="74514-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="74514-112">Return Value</span></span>

<span data-ttu-id="74514-113">O cosseno do parâmetro *x* .</span><span class="sxs-lookup"><span data-stu-id="74514-113">The cosine of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="74514-114">Descrição do tipo</span><span class="sxs-lookup"><span data-stu-id="74514-114">Type Description</span></span>



| <span data-ttu-id="74514-115">Name</span><span class="sxs-lookup"><span data-stu-id="74514-115">Name</span></span>  | [<span data-ttu-id="74514-116">**Tipo de modelo**</span><span class="sxs-lookup"><span data-stu-id="74514-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="74514-117">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="74514-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="74514-118">Tamanho</span><span class="sxs-lookup"><span data-stu-id="74514-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="74514-119">*x*</span><span class="sxs-lookup"><span data-stu-id="74514-119">*x*</span></span>   | <span data-ttu-id="74514-120">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **vetor** ou **matriz**</span><span class="sxs-lookup"><span data-stu-id="74514-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="74514-121">**barra**</span><span class="sxs-lookup"><span data-stu-id="74514-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="74514-122">any</span><span class="sxs-lookup"><span data-stu-id="74514-122">any</span></span>                            |
| <span data-ttu-id="74514-123">*RET*</span><span class="sxs-lookup"><span data-stu-id="74514-123">*ret*</span></span> | <span data-ttu-id="74514-124">igual ao *x* de entrada</span><span class="sxs-lookup"><span data-stu-id="74514-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="74514-125">**barra**</span><span class="sxs-lookup"><span data-stu-id="74514-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="74514-126">mesmas dimensões como entrada *x*</span><span class="sxs-lookup"><span data-stu-id="74514-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="74514-127">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="74514-127">Minimum Shader Model</span></span>

<span data-ttu-id="74514-128">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="74514-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="74514-129">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="74514-129">Shader Model</span></span>                                                                       | <span data-ttu-id="74514-130">Com suporte</span><span class="sxs-lookup"><span data-stu-id="74514-130">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="74514-131">[Modelo do sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="74514-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="74514-132">sim</span><span class="sxs-lookup"><span data-stu-id="74514-132">yes</span></span>       |
| [<span data-ttu-id="74514-133">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="74514-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="74514-134">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="74514-134">vs\_1\_1</span></span>  |



 

## <a name="see-also"></a><span data-ttu-id="74514-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="74514-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74514-136">**Funções intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="74514-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

