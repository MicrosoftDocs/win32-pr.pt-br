---
title: reflexão
description: Retorna um vetor de reflexo usando um incidente Ray e uma superfície normal.
ms.assetid: e321b399-f382-4585-83a6-a7da1f7b2327
keywords:
- refletir HLSL
topic_type:
- apiref
api_name:
- reflect
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 46c981f636a797ecc4e0dd341ce44ed886c202cb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641756"
---
# <a name="reflect"></a><span data-ttu-id="bf968-104">reflexão</span><span class="sxs-lookup"><span data-stu-id="bf968-104">reflect</span></span>

<span data-ttu-id="bf968-105">Retorna um vetor de reflexo usando um incidente Ray e uma superfície normal.</span><span class="sxs-lookup"><span data-stu-id="bf968-105">Returns a reflection vector using an incident ray and a surface normal.</span></span>



| <span data-ttu-id="bf968-106">*RET* refletir (*i*, *n*)</span><span class="sxs-lookup"><span data-stu-id="bf968-106">*ret* reflect(*i*, *n*)</span></span> |
|-------------------------|



 

## <a name="parameters"></a><span data-ttu-id="bf968-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bf968-107">Parameters</span></span>



| <span data-ttu-id="bf968-108">Item</span><span class="sxs-lookup"><span data-stu-id="bf968-108">Item</span></span>                                                   | <span data-ttu-id="bf968-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="bf968-109">Description</span></span>                                          |
|--------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="bf968-110"><span id="i"></span><span id="I"></span>*Encontrei*</span><span class="sxs-lookup"><span data-stu-id="bf968-110"><span id="i"></span><span id="I"></span>*i*</span></span><br/> | <span data-ttu-id="bf968-111">\[em \] um ponto flutuante, vetor de incidente.</span><span class="sxs-lookup"><span data-stu-id="bf968-111">\[in\] A floating-point, incident vector.</span></span><br/> |
| <span data-ttu-id="bf968-112"><span id="n"></span><span id="N"></span>*p*</span><span class="sxs-lookup"><span data-stu-id="bf968-112"><span id="n"></span><span id="N"></span>*n*</span></span><br/> | <span data-ttu-id="bf968-113">\[em \] um ponto flutuante, vetor normal.</span><span class="sxs-lookup"><span data-stu-id="bf968-113">\[in\] A floating-point, normal vector.</span></span><br/>   |



 

## <a name="return-value"></a><span data-ttu-id="bf968-114">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="bf968-114">Return Value</span></span>

<span data-ttu-id="bf968-115">Um vetor de ponto flutuante, reflexo.</span><span class="sxs-lookup"><span data-stu-id="bf968-115">A floating-point, reflection vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf968-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="bf968-116">Remarks</span></span>

<span data-ttu-id="bf968-117">Essa função calcula o vetor de reflexo usando a seguinte fórmula: v = i-2 \* n \* ponto (i n).</span><span class="sxs-lookup"><span data-stu-id="bf968-117">This function calculates the reflection vector using the following formula: v = i - 2 \* n \* dot(i n) .</span></span>

## <a name="type-description"></a><span data-ttu-id="bf968-118">Descrição do tipo</span><span class="sxs-lookup"><span data-stu-id="bf968-118">Type Description</span></span>



| <span data-ttu-id="bf968-119">Name</span><span class="sxs-lookup"><span data-stu-id="bf968-119">Name</span></span>  | [<span data-ttu-id="bf968-120">**Tipo de modelo**</span><span class="sxs-lookup"><span data-stu-id="bf968-120">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="bf968-121">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="bf968-121">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="bf968-122">Tamanho</span><span class="sxs-lookup"><span data-stu-id="bf968-122">Size</span></span>                           |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="bf968-123">*i*</span><span class="sxs-lookup"><span data-stu-id="bf968-123">*i*</span></span>   | [<span data-ttu-id="bf968-124">**vetor**</span><span class="sxs-lookup"><span data-stu-id="bf968-124">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="bf968-125">**barra**</span><span class="sxs-lookup"><span data-stu-id="bf968-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="bf968-126">any</span><span class="sxs-lookup"><span data-stu-id="bf968-126">any</span></span>                            |
| <span data-ttu-id="bf968-127">*n*</span><span class="sxs-lookup"><span data-stu-id="bf968-127">*n*</span></span>   | [<span data-ttu-id="bf968-128">**vetor**</span><span class="sxs-lookup"><span data-stu-id="bf968-128">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="bf968-129">**barra**</span><span class="sxs-lookup"><span data-stu-id="bf968-129">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="bf968-130">mesma dimensão (s) como entrada *i*</span><span class="sxs-lookup"><span data-stu-id="bf968-130">same dimension(s) as input *i*</span></span> |
| <span data-ttu-id="bf968-131">*RET*</span><span class="sxs-lookup"><span data-stu-id="bf968-131">*ret*</span></span> | [<span data-ttu-id="bf968-132">**vetor**</span><span class="sxs-lookup"><span data-stu-id="bf968-132">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="bf968-133">**barra**</span><span class="sxs-lookup"><span data-stu-id="bf968-133">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="bf968-134">mesma dimensão (s) como entrada *i*</span><span class="sxs-lookup"><span data-stu-id="bf968-134">same dimension(s) as input *i*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="bf968-135">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="bf968-135">Minimum Shader Model</span></span>

<span data-ttu-id="bf968-136">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="bf968-136">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="bf968-137">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="bf968-137">Shader Model</span></span>                                                                       | <span data-ttu-id="bf968-138">Com suporte</span><span class="sxs-lookup"><span data-stu-id="bf968-138">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="bf968-139">[Modelo do sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="bf968-139">[Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) and higher shader models</span></span> | <span data-ttu-id="bf968-140">sim</span><span class="sxs-lookup"><span data-stu-id="bf968-140">yes</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="bf968-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="bf968-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf968-142">**Funções intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="bf968-142">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

