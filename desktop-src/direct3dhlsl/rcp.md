---
title: rcp
description: Calcula um recíproco rápido, aproximado e por componente.
ms.assetid: c8d451e4-717e-45b3-a0fe-da55feb8f443
keywords:
- HLSL de RCP
topic_type:
- apiref
api_name:
- rcp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2a857c897def08f31e18ef19466daa2b4584740a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641323"
---
# <a name="rcp"></a><span data-ttu-id="f0282-104">rcp</span><span class="sxs-lookup"><span data-stu-id="f0282-104">rcp</span></span>

<span data-ttu-id="f0282-105">Calcula um recíproco rápido, aproximado e por componente.</span><span class="sxs-lookup"><span data-stu-id="f0282-105">Calculates a fast, approximate, per-component reciprocal.</span></span>



| <span data-ttu-id="f0282-106">*RET* RCP (*x*)</span><span class="sxs-lookup"><span data-stu-id="f0282-106">*ret* rcp(*x*)</span></span> |
|----------------|



 

## <a name="parameters"></a><span data-ttu-id="f0282-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f0282-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0282-108"><span id="x"></span><span id="X"></span>*w.x.y.*</span><span class="sxs-lookup"><span data-stu-id="f0282-108"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="f0282-109">\[no \] valor de entrada.</span><span class="sxs-lookup"><span data-stu-id="f0282-109">\[in\] The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0282-110">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="f0282-110">Return Value</span></span>

<span data-ttu-id="f0282-111">O recíproco do parâmetro *x* .</span><span class="sxs-lookup"><span data-stu-id="f0282-111">The reciprocal of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="f0282-112">Descrição do tipo</span><span class="sxs-lookup"><span data-stu-id="f0282-112">Type Description</span></span>



| <span data-ttu-id="f0282-113">Name</span><span class="sxs-lookup"><span data-stu-id="f0282-113">Name</span></span>  | [<span data-ttu-id="f0282-114">**Tipo de modelo**</span><span class="sxs-lookup"><span data-stu-id="f0282-114">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="f0282-115">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="f0282-115">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                      | <span data-ttu-id="f0282-116">Tamanho</span><span class="sxs-lookup"><span data-stu-id="f0282-116">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="f0282-117">*x*</span><span class="sxs-lookup"><span data-stu-id="f0282-117">*x*</span></span>   | <span data-ttu-id="f0282-118">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **vetor** ou **matriz**</span><span class="sxs-lookup"><span data-stu-id="f0282-118">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | <span data-ttu-id="f0282-119">[**float**](/windows/desktop/WinProg/windows-data-types) ou [ **Double**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="f0282-119">[**float**](/windows/desktop/WinProg/windows-data-types) or [**double**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="f0282-120">any</span><span class="sxs-lookup"><span data-stu-id="f0282-120">any</span></span>                            |
| <span data-ttu-id="f0282-121">*RET*</span><span class="sxs-lookup"><span data-stu-id="f0282-121">*ret*</span></span> | <span data-ttu-id="f0282-122">igual ao *x* de entrada</span><span class="sxs-lookup"><span data-stu-id="f0282-122">same as input *x*</span></span>                                                                                              | <span data-ttu-id="f0282-123">[**float**](/windows/desktop/WinProg/windows-data-types) ou [ **Double**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="f0282-123">[**float**](/windows/desktop/WinProg/windows-data-types) or [**double**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="f0282-124">mesmas dimensões como entrada *x*</span><span class="sxs-lookup"><span data-stu-id="f0282-124">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="f0282-125">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="f0282-125">Minimum Shader Model</span></span>

<span data-ttu-id="f0282-126">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="f0282-126">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="f0282-127">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="f0282-127">Shader Model</span></span>                                                                | <span data-ttu-id="f0282-128">Com suporte</span><span class="sxs-lookup"><span data-stu-id="f0282-128">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="f0282-129">[Modelo](d3d11-graphics-reference-sm5.md) de sombreador 5 e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="f0282-129">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="f0282-130">sim</span><span class="sxs-lookup"><span data-stu-id="f0282-130">yes</span></span>       |



 

<span data-ttu-id="f0282-131">Essa função tem suporte nos seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="f0282-131">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="f0282-132">Vértice</span><span class="sxs-lookup"><span data-stu-id="f0282-132">Vertex</span></span> | <span data-ttu-id="f0282-133">Envoltória</span><span class="sxs-lookup"><span data-stu-id="f0282-133">Hull</span></span> | <span data-ttu-id="f0282-134">Domínio</span><span class="sxs-lookup"><span data-stu-id="f0282-134">Domain</span></span> | <span data-ttu-id="f0282-135">Geometria</span><span class="sxs-lookup"><span data-stu-id="f0282-135">Geometry</span></span> | <span data-ttu-id="f0282-136">16x16</span><span class="sxs-lookup"><span data-stu-id="f0282-136">Pixel</span></span> | <span data-ttu-id="f0282-137">Computação</span><span class="sxs-lookup"><span data-stu-id="f0282-137">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="f0282-138">x</span><span class="sxs-lookup"><span data-stu-id="f0282-138">x</span></span>      | <span data-ttu-id="f0282-139">x</span><span class="sxs-lookup"><span data-stu-id="f0282-139">x</span></span>    | <span data-ttu-id="f0282-140">x</span><span class="sxs-lookup"><span data-stu-id="f0282-140">x</span></span>      | <span data-ttu-id="f0282-141">x</span><span class="sxs-lookup"><span data-stu-id="f0282-141">x</span></span>        | <span data-ttu-id="f0282-142">x</span><span class="sxs-lookup"><span data-stu-id="f0282-142">x</span></span>     | <span data-ttu-id="f0282-143">x</span><span class="sxs-lookup"><span data-stu-id="f0282-143">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="f0282-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="f0282-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0282-145">Funções intrínsecas</span><span class="sxs-lookup"><span data-stu-id="f0282-145">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="f0282-146">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="f0282-146">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 