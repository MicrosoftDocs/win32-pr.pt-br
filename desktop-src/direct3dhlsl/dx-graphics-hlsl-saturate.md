---
title: Saturação (referência de HLSL)
description: Coloca o valor especificado dentro do intervalo de 0 a 1.
ms.assetid: efe4dedd-732a-4643-8a57-61814434f6ff
keywords:
- saturar HLSL
topic_type:
- apiref
api_name:
- saturate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 609443bdc1d0cff6a4c81c8eb26d86a30ea1e721
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294077"
---
# <a name="saturate-hlsl-reference"></a><span data-ttu-id="7825b-104">Saturação (referência de HLSL)</span><span class="sxs-lookup"><span data-stu-id="7825b-104">saturate (HLSL reference)</span></span>

<span data-ttu-id="7825b-105">Coloca o valor especificado dentro do intervalo de 0 a 1.</span><span class="sxs-lookup"><span data-stu-id="7825b-105">Clamps the specified value within the range of 0 to 1.</span></span>



| <span data-ttu-id="7825b-106">saturação de *RET* (*x*)</span><span class="sxs-lookup"><span data-stu-id="7825b-106">*ret* saturate(*x*)</span></span> |
|---------------------|



 

## <a name="parameters"></a><span data-ttu-id="7825b-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7825b-107">Parameters</span></span>



| <span data-ttu-id="7825b-108">Item</span><span class="sxs-lookup"><span data-stu-id="7825b-108">Item</span></span>                                                   | <span data-ttu-id="7825b-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="7825b-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="7825b-110"><span id="x"></span><span id="X"></span>*w.x.y.*</span><span class="sxs-lookup"><span data-stu-id="7825b-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="7825b-111">\[no \] valor especificado.</span><span class="sxs-lookup"><span data-stu-id="7825b-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="7825b-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="7825b-112">Return Value</span></span>

<span data-ttu-id="7825b-113">O parâmetro *x* , clamped dentro do intervalo de 0 a 1.</span><span class="sxs-lookup"><span data-stu-id="7825b-113">The *x* parameter, clamped within the range of 0 to 1.</span></span>

## <a name="type-description"></a><span data-ttu-id="7825b-114">Descrição do tipo</span><span class="sxs-lookup"><span data-stu-id="7825b-114">Type Description</span></span>



| <span data-ttu-id="7825b-115">Name</span><span class="sxs-lookup"><span data-stu-id="7825b-115">Name</span></span>  | [<span data-ttu-id="7825b-116">**Tipo de modelo**</span><span class="sxs-lookup"><span data-stu-id="7825b-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="7825b-117">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="7825b-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="7825b-118">Tamanho</span><span class="sxs-lookup"><span data-stu-id="7825b-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="7825b-119">*x*</span><span class="sxs-lookup"><span data-stu-id="7825b-119">*x*</span></span>   | <span data-ttu-id="7825b-120">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **vetor** ou **matriz**</span><span class="sxs-lookup"><span data-stu-id="7825b-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="7825b-121">**barra**</span><span class="sxs-lookup"><span data-stu-id="7825b-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="7825b-122">any</span><span class="sxs-lookup"><span data-stu-id="7825b-122">any</span></span>                            |
| <span data-ttu-id="7825b-123">*RET*</span><span class="sxs-lookup"><span data-stu-id="7825b-123">*ret*</span></span> | <span data-ttu-id="7825b-124">igual ao *x* de entrada</span><span class="sxs-lookup"><span data-stu-id="7825b-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="7825b-125">**barra**</span><span class="sxs-lookup"><span data-stu-id="7825b-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="7825b-126">mesmas dimensões como entrada *x*</span><span class="sxs-lookup"><span data-stu-id="7825b-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="7825b-127">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="7825b-127">Minimum Shader Model</span></span>

<span data-ttu-id="7825b-128">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="7825b-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="7825b-129">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="7825b-129">Shader Model</span></span>                                                                       | <span data-ttu-id="7825b-130">Com suporte</span><span class="sxs-lookup"><span data-stu-id="7825b-130">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="7825b-131">[Modelo do sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="7825b-131">[Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) and higher shader models</span></span> | <span data-ttu-id="7825b-132">sim</span><span class="sxs-lookup"><span data-stu-id="7825b-132">yes</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="7825b-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="7825b-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7825b-134">**Funções intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="7825b-134">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

