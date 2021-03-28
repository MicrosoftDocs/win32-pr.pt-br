---
title: graus
description: Converte o valor especificado de radianos em graus.
ms.assetid: e60a3ec4-9177-457a-8314-a5788f353633
keywords:
- graus HLSL
topic_type:
- apiref
api_name:
- degrees
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 47d8bba0ee43da81a18baaeaffca0e3c917e460d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366204"
---
# <a name="degrees"></a><span data-ttu-id="b7e34-104">graus</span><span class="sxs-lookup"><span data-stu-id="b7e34-104">degrees</span></span>

<span data-ttu-id="b7e34-105">Converte o valor especificado de radianos em graus.</span><span class="sxs-lookup"><span data-stu-id="b7e34-105">Converts the specified value from radians to degrees.</span></span>



| <span data-ttu-id="b7e34-106">*RET* graus (*x*)</span><span class="sxs-lookup"><span data-stu-id="b7e34-106">*ret* degrees(*x*)</span></span> |
|--------------------|



 

## <a name="parameters"></a><span data-ttu-id="b7e34-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b7e34-107">Parameters</span></span>



| <span data-ttu-id="b7e34-108">Item</span><span class="sxs-lookup"><span data-stu-id="b7e34-108">Item</span></span>                                                   | <span data-ttu-id="b7e34-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="b7e34-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="b7e34-110"><span id="x"></span><span id="X"></span>*w.x.y.*</span><span class="sxs-lookup"><span data-stu-id="b7e34-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="b7e34-111">\[no \] valor especificado.</span><span class="sxs-lookup"><span data-stu-id="b7e34-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="b7e34-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="b7e34-112">Return Value</span></span>

<span data-ttu-id="b7e34-113">O resultado da conversão do parâmetro *x* de radianos em graus.</span><span class="sxs-lookup"><span data-stu-id="b7e34-113">The result of converting the *x* parameter from radians to degrees.</span></span>

## <a name="type-description"></a><span data-ttu-id="b7e34-114">Descrição do tipo</span><span class="sxs-lookup"><span data-stu-id="b7e34-114">Type Description</span></span>



| <span data-ttu-id="b7e34-115">Name</span><span class="sxs-lookup"><span data-stu-id="b7e34-115">Name</span></span>  | [<span data-ttu-id="b7e34-116">**Tipo de modelo**</span><span class="sxs-lookup"><span data-stu-id="b7e34-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="b7e34-117">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="b7e34-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="b7e34-118">Tamanho</span><span class="sxs-lookup"><span data-stu-id="b7e34-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="b7e34-119">*x*</span><span class="sxs-lookup"><span data-stu-id="b7e34-119">*x*</span></span>   | <span data-ttu-id="b7e34-120">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **vetor** ou **matriz**</span><span class="sxs-lookup"><span data-stu-id="b7e34-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="b7e34-121">**barra**</span><span class="sxs-lookup"><span data-stu-id="b7e34-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="b7e34-122">any</span><span class="sxs-lookup"><span data-stu-id="b7e34-122">any</span></span>                            |
| <span data-ttu-id="b7e34-123">*RET*</span><span class="sxs-lookup"><span data-stu-id="b7e34-123">*ret*</span></span> | <span data-ttu-id="b7e34-124">igual ao *x* de entrada</span><span class="sxs-lookup"><span data-stu-id="b7e34-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="b7e34-125">**barra**</span><span class="sxs-lookup"><span data-stu-id="b7e34-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="b7e34-126">mesmas dimensões como entrada *x*</span><span class="sxs-lookup"><span data-stu-id="b7e34-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="b7e34-127">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="b7e34-127">Minimum Shader Model</span></span>

<span data-ttu-id="b7e34-128">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="b7e34-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="b7e34-129">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="b7e34-129">Shader Model</span></span>                                                                       | <span data-ttu-id="b7e34-130">Com suporte</span><span class="sxs-lookup"><span data-stu-id="b7e34-130">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="b7e34-131">[Modelo do sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="b7e34-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="b7e34-132">sim</span><span class="sxs-lookup"><span data-stu-id="b7e34-132">yes</span></span>       |
| [<span data-ttu-id="b7e34-133">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b7e34-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="b7e34-134">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="b7e34-134">vs\_1\_1</span></span>  |



 

## <a name="see-also"></a><span data-ttu-id="b7e34-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="b7e34-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7e34-136">**Funções intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="b7e34-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

