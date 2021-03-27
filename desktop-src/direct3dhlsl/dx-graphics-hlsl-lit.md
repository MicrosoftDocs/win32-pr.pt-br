---
title: aceso
description: Retorna um vetor de coeficiente de iluminação.
ms.assetid: 6ae116df-41b7-42f1-96cb-da480a7c1bab
keywords:
- HLSL aceso
topic_type:
- apiref
api_name:
- lit
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6dbf6f1e53218355ba1ee9ccf58dac6176007218
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823777"
---
# <a name="lit"></a><span data-ttu-id="8d7ee-104">aceso</span><span class="sxs-lookup"><span data-stu-id="8d7ee-104">lit</span></span>

<span data-ttu-id="8d7ee-105">Retorna um vetor de coeficiente de iluminação.</span><span class="sxs-lookup"><span data-stu-id="8d7ee-105">Returns a lighting coefficient vector.</span></span>



| <span data-ttu-id="8d7ee-106">*RET* aceso (*n \_ ponto \_ l*, *n \_ ponto \_ h*, *m*)</span><span class="sxs-lookup"><span data-stu-id="8d7ee-106">*ret* lit(*n\_dot\_l*, *n\_dot\_h*, *m*)</span></span> |
|------------------------------------------|



 

<span data-ttu-id="8d7ee-107">Essa função retorna um vetor de coeficiente de iluminação (ambiente, difuso, especular, 1) em que:</span><span class="sxs-lookup"><span data-stu-id="8d7ee-107">This function returns a lighting coefficient vector (ambient, diffuse, specular, 1) where:</span></span>

-   <span data-ttu-id="8d7ee-108">ambiente = 1</span><span class="sxs-lookup"><span data-stu-id="8d7ee-108">ambient = 1</span></span>
-   <span data-ttu-id="8d7ee-109">difuso = n · l < 0?</span><span class="sxs-lookup"><span data-stu-id="8d7ee-109">diffuse = n · l < 0 ?</span></span> <span data-ttu-id="8d7ee-110">0: n · debug</span><span class="sxs-lookup"><span data-stu-id="8d7ee-110">0 : n · l</span></span>
-   <span data-ttu-id="8d7ee-111">especular = n · l < 0 \| \| n · h < 0?</span><span class="sxs-lookup"><span data-stu-id="8d7ee-111">specular = n · l < 0 \|\| n · h < 0 ?</span></span> <span data-ttu-id="8d7ee-112">0: (n · h) ^ m</span><span class="sxs-lookup"><span data-stu-id="8d7ee-112">0 : (n · h) ^ m</span></span>

<span data-ttu-id="8d7ee-113">Onde o vetor n é o vetor normal, l é a direção para acender e h é a metade do vetor.</span><span class="sxs-lookup"><span data-stu-id="8d7ee-113">Where the vector n is the normal vector, l is the direction to light and h is the half vector.</span></span>

## <a name="parameters"></a><span data-ttu-id="8d7ee-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8d7ee-114">Parameters</span></span>



| <span data-ttu-id="8d7ee-115">Item</span><span class="sxs-lookup"><span data-stu-id="8d7ee-115">Item</span></span>                                                                       | <span data-ttu-id="8d7ee-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="8d7ee-116">Description</span></span>                                                                              |
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d7ee-117"><span id="n_dot_l"></span><span id="N_DOT_L"></span>*n \_ ponto \_ l*</span><span class="sxs-lookup"><span data-stu-id="8d7ee-117"><span id="n_dot_l"></span><span id="N_DOT_L"></span>*n\_dot\_l*</span></span><br/> | <span data-ttu-id="8d7ee-118">\[no \] produto de ponto da superfície normalizada normal e do vetor claro.</span><span class="sxs-lookup"><span data-stu-id="8d7ee-118">\[in\] The dot product of the normalized surface normal and the light vector.</span></span><br/> |
| <span data-ttu-id="8d7ee-119"><span id="n_dot_h"></span><span id="N_DOT_H"></span>*n \_ ponto \_ h*</span><span class="sxs-lookup"><span data-stu-id="8d7ee-119"><span id="n_dot_h"></span><span id="N_DOT_H"></span>*n\_dot\_h*</span></span><br/> | <span data-ttu-id="8d7ee-120">\[no \] produto de ponto do vetor de metade do ângulo e na superfície normal.</span><span class="sxs-lookup"><span data-stu-id="8d7ee-120">\[in\] The dot product of the half-angle vector and the surface normal.</span></span><br/>       |
| <span data-ttu-id="8d7ee-121"><span id="m"></span><span id="M"></span>*d*</span><span class="sxs-lookup"><span data-stu-id="8d7ee-121"><span id="m"></span><span id="M"></span>*m*</span></span><br/>                     | <span data-ttu-id="8d7ee-122">\[em \] um expoente especular.</span><span class="sxs-lookup"><span data-stu-id="8d7ee-122">\[in\] A specular exponent.</span></span><br/>                                                   |



 

## <a name="return-value"></a><span data-ttu-id="8d7ee-123">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="8d7ee-123">Return Value</span></span>

<span data-ttu-id="8d7ee-124">O vetor de coeficiente de iluminação.</span><span class="sxs-lookup"><span data-stu-id="8d7ee-124">The lighting coefficient vector.</span></span>

## <a name="type-description"></a><span data-ttu-id="8d7ee-125">Descrição do tipo</span><span class="sxs-lookup"><span data-stu-id="8d7ee-125">Type Description</span></span>



| <span data-ttu-id="8d7ee-126">Name</span><span class="sxs-lookup"><span data-stu-id="8d7ee-126">Name</span></span>        | [<span data-ttu-id="8d7ee-127">**Tipo de modelo**</span><span class="sxs-lookup"><span data-stu-id="8d7ee-127">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="8d7ee-128">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="8d7ee-128">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="8d7ee-129">Tamanho</span><span class="sxs-lookup"><span data-stu-id="8d7ee-129">Size</span></span> |
|-------------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="8d7ee-130">*n \_ ponto \_ l*</span><span class="sxs-lookup"><span data-stu-id="8d7ee-130">*n\_dot\_l*</span></span> | [<span data-ttu-id="8d7ee-131">**escalar**</span><span class="sxs-lookup"><span data-stu-id="8d7ee-131">**scalar**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="8d7ee-132">**FLOAT**</span><span class="sxs-lookup"><span data-stu-id="8d7ee-132">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="8d7ee-133">1</span><span class="sxs-lookup"><span data-stu-id="8d7ee-133">1</span></span>    |
| <span data-ttu-id="8d7ee-134">*n \_ ponto \_ h*</span><span class="sxs-lookup"><span data-stu-id="8d7ee-134">*n\_dot\_h*</span></span> | [<span data-ttu-id="8d7ee-135">**escalar**</span><span class="sxs-lookup"><span data-stu-id="8d7ee-135">**scalar**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="8d7ee-136">**FLOAT**</span><span class="sxs-lookup"><span data-stu-id="8d7ee-136">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="8d7ee-137">1</span><span class="sxs-lookup"><span data-stu-id="8d7ee-137">1</span></span>    |
| <span data-ttu-id="8d7ee-138">*m*</span><span class="sxs-lookup"><span data-stu-id="8d7ee-138">*m*</span></span>         | [<span data-ttu-id="8d7ee-139">**escalar**</span><span class="sxs-lookup"><span data-stu-id="8d7ee-139">**scalar**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="8d7ee-140">**FLOAT**</span><span class="sxs-lookup"><span data-stu-id="8d7ee-140">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="8d7ee-141">1</span><span class="sxs-lookup"><span data-stu-id="8d7ee-141">1</span></span>    |
| <span data-ttu-id="8d7ee-142">*RET*</span><span class="sxs-lookup"><span data-stu-id="8d7ee-142">*ret*</span></span>       | [<span data-ttu-id="8d7ee-143">**vetor**</span><span class="sxs-lookup"><span data-stu-id="8d7ee-143">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="8d7ee-144">**barra**</span><span class="sxs-lookup"><span data-stu-id="8d7ee-144">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="8d7ee-145">4</span><span class="sxs-lookup"><span data-stu-id="8d7ee-145">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="8d7ee-146">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="8d7ee-146">Minimum Shader Model</span></span>

<span data-ttu-id="8d7ee-147">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="8d7ee-147">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="8d7ee-148">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="8d7ee-148">Shader Model</span></span>                                                                       | <span data-ttu-id="8d7ee-149">Com suporte</span><span class="sxs-lookup"><span data-stu-id="8d7ee-149">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="8d7ee-150">[Modelo do sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="8d7ee-150">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="8d7ee-151">sim</span><span class="sxs-lookup"><span data-stu-id="8d7ee-151">yes</span></span>                 |
| [<span data-ttu-id="8d7ee-152">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8d7ee-152">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="8d7ee-153">Sim ( \_ apenas vs 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="8d7ee-153">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="8d7ee-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="8d7ee-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d7ee-155">**Funções intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="8d7ee-155">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

