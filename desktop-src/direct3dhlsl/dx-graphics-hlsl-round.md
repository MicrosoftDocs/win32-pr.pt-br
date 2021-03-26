---
title: Round (Corecrt \_ Math. h)
description: Arredonda o valor especificado para o número inteiro mais próximo.
ms.assetid: 258ce717-dca1-4ed2-ad98-1ecfdb58f939
keywords:
- arredondar HLSL
topic_type:
- apiref
api_name:
- round
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f00bf845dfe16a92729b523fba62f6fd6dcde2b5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930636"
---
# <a name="round"></a><span data-ttu-id="136d8-104">round</span><span class="sxs-lookup"><span data-stu-id="136d8-104">round</span></span>

<span data-ttu-id="136d8-105">Arredonda o valor especificado para o número inteiro mais próximo.</span><span class="sxs-lookup"><span data-stu-id="136d8-105">Rounds the specified value to the nearest integer.</span></span> <span data-ttu-id="136d8-106">Os casos intermediários são arredondados para o mais próximo mesmo.</span><span class="sxs-lookup"><span data-stu-id="136d8-106">Halfway cases are rounded to the nearest even.</span></span>



| <span data-ttu-id="136d8-107">*ida e* volta (*x*)</span><span class="sxs-lookup"><span data-stu-id="136d8-107">*ret* round(*x*)</span></span> |
|------------------|



 

## <a name="parameters"></a><span data-ttu-id="136d8-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="136d8-108">Parameters</span></span>



| <span data-ttu-id="136d8-109">Item</span><span class="sxs-lookup"><span data-stu-id="136d8-109">Item</span></span>                                                   | <span data-ttu-id="136d8-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="136d8-110">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="136d8-111"><span id="x"></span><span id="X"></span>*w.x.y.*</span><span class="sxs-lookup"><span data-stu-id="136d8-111"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="136d8-112">\[no \] valor especificado.</span><span class="sxs-lookup"><span data-stu-id="136d8-112">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="136d8-113">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="136d8-113">Return Value</span></span>

<span data-ttu-id="136d8-114">O parâmetro *x* , arredondado para o número inteiro mais próximo dentro de um tipo de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="136d8-114">The *x* parameter, rounded to the nearest integer within a floating-point type.</span></span>

## <a name="type-description"></a><span data-ttu-id="136d8-115">Descrição do tipo</span><span class="sxs-lookup"><span data-stu-id="136d8-115">Type Description</span></span>



| <span data-ttu-id="136d8-116">Name</span><span class="sxs-lookup"><span data-stu-id="136d8-116">Name</span></span>  | [<span data-ttu-id="136d8-117">**Tipo de modelo**</span><span class="sxs-lookup"><span data-stu-id="136d8-117">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="136d8-118">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="136d8-118">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="136d8-119">Tamanho</span><span class="sxs-lookup"><span data-stu-id="136d8-119">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="136d8-120">*x*</span><span class="sxs-lookup"><span data-stu-id="136d8-120">*x*</span></span>   | <span data-ttu-id="136d8-121">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **vetor** ou **matriz**</span><span class="sxs-lookup"><span data-stu-id="136d8-121">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="136d8-122">**barra**</span><span class="sxs-lookup"><span data-stu-id="136d8-122">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="136d8-123">any</span><span class="sxs-lookup"><span data-stu-id="136d8-123">any</span></span>                            |
| <span data-ttu-id="136d8-124">*RET*</span><span class="sxs-lookup"><span data-stu-id="136d8-124">*ret*</span></span> | <span data-ttu-id="136d8-125">igual ao *x* de entrada</span><span class="sxs-lookup"><span data-stu-id="136d8-125">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="136d8-126">**barra**</span><span class="sxs-lookup"><span data-stu-id="136d8-126">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="136d8-127">mesmas dimensões como entrada *x*</span><span class="sxs-lookup"><span data-stu-id="136d8-127">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="136d8-128">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="136d8-128">Minimum Shader Model</span></span>

<span data-ttu-id="136d8-129">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="136d8-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="136d8-130">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="136d8-130">Shader Model</span></span>                                                                       | <span data-ttu-id="136d8-131">Com suporte</span><span class="sxs-lookup"><span data-stu-id="136d8-131">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="136d8-132">[Modelo do sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="136d8-132">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="136d8-133">sim</span><span class="sxs-lookup"><span data-stu-id="136d8-133">yes</span></span>                 |
| [<span data-ttu-id="136d8-134">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="136d8-134">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="136d8-135">Sim ( \_ apenas vs 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="136d8-135">yes (vs\_1\_1 only)</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="136d8-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="136d8-136">Requirements</span></span>



| <span data-ttu-id="136d8-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="136d8-137">Requirement</span></span> | <span data-ttu-id="136d8-138">Valor</span><span class="sxs-lookup"><span data-stu-id="136d8-138">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="136d8-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="136d8-139">Header</span></span><br/> | <dl> <span data-ttu-id="136d8-140"><dt>Corecrt \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="136d8-140"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="136d8-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="136d8-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="136d8-142">**Funções intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="136d8-142">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

