---
title: refract
description: Retorna um vetor de refração usando uma entrada Ray, uma superfície normal e um índice refracionário.
ms.assetid: 9f9467d7-dd9b-472a-bbdc-752394d382c6
keywords:
- refract HLSL
topic_type:
- apiref
api_name:
- refract
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9e499d078a020ade1ff9ff2566c3fd15b2a820d2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104988705"
---
# <a name="refract"></a><span data-ttu-id="d5a54-104">refract</span><span class="sxs-lookup"><span data-stu-id="d5a54-104">refract</span></span>

<span data-ttu-id="d5a54-105">Retorna um vetor de refração usando uma entrada Ray, uma superfície normal e um índice refracionário.</span><span class="sxs-lookup"><span data-stu-id="d5a54-105">Returns a refraction vector using an entering ray, a surface normal, and a refraction index.</span></span>



| <span data-ttu-id="d5a54-106">*RET* refract (*i*, *n*,?)</span><span class="sxs-lookup"><span data-stu-id="d5a54-106">*ret* refract(*i*, *n*, ?)</span></span> |
|----------------------------|



 

## <a name="parameters"></a><span data-ttu-id="d5a54-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d5a54-107">Parameters</span></span>



| <span data-ttu-id="d5a54-108">Item</span><span class="sxs-lookup"><span data-stu-id="d5a54-108">Item</span></span>                                                   | <span data-ttu-id="d5a54-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="d5a54-109">Description</span></span>                                                  |
|--------------------------------------------------------|--------------------------------------------------------------|
| <span data-ttu-id="d5a54-110"><span id="i"></span><span id="I"></span>*Encontrei*</span><span class="sxs-lookup"><span data-stu-id="d5a54-110"><span id="i"></span><span id="I"></span>*i*</span></span><br/> | <span data-ttu-id="d5a54-111">\[em \] um ponto flutuante, vetor de direção de raio.</span><span class="sxs-lookup"><span data-stu-id="d5a54-111">\[in\] A floating-point, ray direction vector.</span></span><br/>    |
| <span data-ttu-id="d5a54-112"><span id="n"></span><span id="N"></span>*p*</span><span class="sxs-lookup"><span data-stu-id="d5a54-112"><span id="n"></span><span id="N"></span>*n*</span></span><br/> | <span data-ttu-id="d5a54-113">\[em \] um ponto flutuante, vetor normal de superfície.</span><span class="sxs-lookup"><span data-stu-id="d5a54-113">\[in\] A floating-point, surface normal vector.</span></span><br/>   |
| <span data-ttu-id="d5a54-114">*?*</span><span class="sxs-lookup"><span data-stu-id="d5a54-114">*?*</span></span><br/>                                         | <span data-ttu-id="d5a54-115">\[em \] um ponto flutuante, refração do índice escalar.</span><span class="sxs-lookup"><span data-stu-id="d5a54-115">\[in\] A floating-point, refraction index scalar.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="d5a54-116">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="d5a54-116">Return Value</span></span>

<span data-ttu-id="d5a54-117">Um vetor de ponto flutuante, refração.</span><span class="sxs-lookup"><span data-stu-id="d5a54-117">A floating-point, refraction vector.</span></span> <span data-ttu-id="d5a54-118">Se o ângulo entre a inserção de Ray i e a superfície normal n for muito grande para um determinado índice de refração?, o valor de retorno será (0, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="d5a54-118">If the angle between the entering ray i and the surface normal n is too great for a given refraction index ?, the return value is (0,0,0).</span></span>

## <a name="type-description"></a><span data-ttu-id="d5a54-119">Descrição do tipo</span><span class="sxs-lookup"><span data-stu-id="d5a54-119">Type Description</span></span>



| <span data-ttu-id="d5a54-120">Name</span><span class="sxs-lookup"><span data-stu-id="d5a54-120">Name</span></span>              | [<span data-ttu-id="d5a54-121">**Tipo de modelo**</span><span class="sxs-lookup"><span data-stu-id="d5a54-121">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="d5a54-122">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="d5a54-122">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="d5a54-123">Tamanho</span><span class="sxs-lookup"><span data-stu-id="d5a54-123">Size</span></span>                           |
|-------------------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="d5a54-124">*i*</span><span class="sxs-lookup"><span data-stu-id="d5a54-124">*i*</span></span>               | [<span data-ttu-id="d5a54-125">**vetor**</span><span class="sxs-lookup"><span data-stu-id="d5a54-125">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="d5a54-126">**barra**</span><span class="sxs-lookup"><span data-stu-id="d5a54-126">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="d5a54-127">any</span><span class="sxs-lookup"><span data-stu-id="d5a54-127">any</span></span>                            |
| <span data-ttu-id="d5a54-128">*n*</span><span class="sxs-lookup"><span data-stu-id="d5a54-128">*n*</span></span>               | [<span data-ttu-id="d5a54-129">**vetor**</span><span class="sxs-lookup"><span data-stu-id="d5a54-129">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="d5a54-130">**barra**</span><span class="sxs-lookup"><span data-stu-id="d5a54-130">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="d5a54-131">mesma dimensão (s) como entrada *i*</span><span class="sxs-lookup"><span data-stu-id="d5a54-131">same dimension(s) as input *i*</span></span> |
| <span data-ttu-id="d5a54-132">?</span><span class="sxs-lookup"><span data-stu-id="d5a54-132">?</span></span>                 | [<span data-ttu-id="d5a54-133">**escalar**</span><span class="sxs-lookup"><span data-stu-id="d5a54-133">**scalar**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="d5a54-134">**FLOAT**</span><span class="sxs-lookup"><span data-stu-id="d5a54-134">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="d5a54-135">1</span><span class="sxs-lookup"><span data-stu-id="d5a54-135">1</span></span>                              |
| <span data-ttu-id="d5a54-136">vetor de refração</span><span class="sxs-lookup"><span data-stu-id="d5a54-136">refraction vector</span></span> | [<span data-ttu-id="d5a54-137">**vetor**</span><span class="sxs-lookup"><span data-stu-id="d5a54-137">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="d5a54-138">**barra**</span><span class="sxs-lookup"><span data-stu-id="d5a54-138">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="d5a54-139">mesma dimensão (s) como entrada *i*</span><span class="sxs-lookup"><span data-stu-id="d5a54-139">same dimension(s) as input *i*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d5a54-140">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="d5a54-140">Minimum Shader Model</span></span>

<span data-ttu-id="d5a54-141">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="d5a54-141">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="d5a54-142">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="d5a54-142">Shader Model</span></span>                                                                       | <span data-ttu-id="d5a54-143">Com suporte</span><span class="sxs-lookup"><span data-stu-id="d5a54-143">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="d5a54-144">[Modelo do sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="d5a54-144">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="d5a54-145">sim</span><span class="sxs-lookup"><span data-stu-id="d5a54-145">yes</span></span>                 |
| [<span data-ttu-id="d5a54-146">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d5a54-146">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="d5a54-147">Sim ( \_ apenas vs 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="d5a54-147">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="d5a54-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="d5a54-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5a54-149">**Funções intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="d5a54-149">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

