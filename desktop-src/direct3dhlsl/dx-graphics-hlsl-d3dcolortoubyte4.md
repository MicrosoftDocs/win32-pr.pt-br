---
title: D3DCOLORtoUBYTE4
description: Converte um ponto flutuante, um vetor de 4D definido por um D3DCOLOR para um UBYTE4.
ms.assetid: 20a7be00-1e36-41c3-bc98-933b3faa8f35
keywords:
- D3DCOLORtoUBYTE4 HLSL
topic_type:
- apiref
api_name:
- D3DCOLORtoUBYTE4
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c60f0934d6700ec7fbd9e6d9e6443cb6409ab15f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104499139"
---
# <a name="d3dcolortoubyte4"></a><span data-ttu-id="98f52-104">D3DCOLORtoUBYTE4</span><span class="sxs-lookup"><span data-stu-id="98f52-104">D3DCOLORtoUBYTE4</span></span>

<span data-ttu-id="98f52-105">Converte um ponto flutuante, um vetor de 4D definido por um D3DCOLOR para um UBYTE4.</span><span class="sxs-lookup"><span data-stu-id="98f52-105">Converts a floating-point, 4D vector set by a D3DCOLOR to a UBYTE4.</span></span>



| <span data-ttu-id="98f52-106">*RET* D3DCOLORtoUBYTE4 (*x*)</span><span class="sxs-lookup"><span data-stu-id="98f52-106">*ret* D3DCOLORtoUBYTE4(*x*)</span></span> |
|-----------------------------|



 

<span data-ttu-id="98f52-107">Essa função swizzles e dimensiona os componentes do parâmetro *x* .</span><span class="sxs-lookup"><span data-stu-id="98f52-107">This function swizzles and scales components of the *x* parameter.</span></span> <span data-ttu-id="98f52-108">Use essa função para compensar a falta de suporte a UBYTE4 em alguns hardwares.</span><span class="sxs-lookup"><span data-stu-id="98f52-108">Use this function to compensate for the lack of UBYTE4 support in some hardware.</span></span>

## <a name="parameters"></a><span data-ttu-id="98f52-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="98f52-109">Parameters</span></span>



| <span data-ttu-id="98f52-110">Item</span><span class="sxs-lookup"><span data-stu-id="98f52-110">Item</span></span>                                                   | <span data-ttu-id="98f52-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="98f52-111">Description</span></span>                                              |
|--------------------------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="98f52-112"><span id="x"></span><span id="X"></span>*w.x.y.*</span><span class="sxs-lookup"><span data-stu-id="98f52-112"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="98f52-113">\[no \] Vector4 de ponto flutuante a ser convertido.</span><span class="sxs-lookup"><span data-stu-id="98f52-113">\[in\] The floating-point vector4 to convert.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="98f52-114">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="98f52-114">Return Value</span></span>

<span data-ttu-id="98f52-115">A representação UBYTE4 do parâmetro *x* .</span><span class="sxs-lookup"><span data-stu-id="98f52-115">The UBYTE4 representation of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="98f52-116">Descrição do tipo</span><span class="sxs-lookup"><span data-stu-id="98f52-116">Type Description</span></span>



| <span data-ttu-id="98f52-117">Name</span><span class="sxs-lookup"><span data-stu-id="98f52-117">Name</span></span>  | [<span data-ttu-id="98f52-118">**Tipo de modelo**</span><span class="sxs-lookup"><span data-stu-id="98f52-118">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="98f52-119">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="98f52-119">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="98f52-120">Tamanho</span><span class="sxs-lookup"><span data-stu-id="98f52-120">Size</span></span> |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="98f52-121">*x*</span><span class="sxs-lookup"><span data-stu-id="98f52-121">*x*</span></span>   | [<span data-ttu-id="98f52-122">**vetor**</span><span class="sxs-lookup"><span data-stu-id="98f52-122">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="98f52-123">**barra**</span><span class="sxs-lookup"><span data-stu-id="98f52-123">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="98f52-124">4</span><span class="sxs-lookup"><span data-stu-id="98f52-124">4</span></span>    |
| <span data-ttu-id="98f52-125">*RET*</span><span class="sxs-lookup"><span data-stu-id="98f52-125">*ret*</span></span> | [<span data-ttu-id="98f52-126">**vetor**</span><span class="sxs-lookup"><span data-stu-id="98f52-126">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="98f52-127">**valores**</span><span class="sxs-lookup"><span data-stu-id="98f52-127">**integer**</span></span>](/windows/desktop/WinProg/windows-data-types)                      | <span data-ttu-id="98f52-128">4</span><span class="sxs-lookup"><span data-stu-id="98f52-128">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="98f52-129">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="98f52-129">Minimum Shader Model</span></span>

<span data-ttu-id="98f52-130">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="98f52-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="98f52-131">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="98f52-131">Shader Model</span></span>                                                                       | <span data-ttu-id="98f52-132">Com suporte</span><span class="sxs-lookup"><span data-stu-id="98f52-132">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="98f52-133">[Modelo do sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="98f52-133">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="98f52-134">sim</span><span class="sxs-lookup"><span data-stu-id="98f52-134">yes</span></span>       |
| [<span data-ttu-id="98f52-135">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="98f52-135">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="98f52-136">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="98f52-136">vs\_1\_1</span></span>  |



 

## <a name="see-also"></a><span data-ttu-id="98f52-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="98f52-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98f52-138">**Funções intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="98f52-138">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

