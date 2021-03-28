---
title: faceforward
description: Inverte a superfície – normal (se necessário) para enfrentar uma direção oposta à i; Retorna o resultado em n.
ms.assetid: 6530a928-d221-49e4-ab68-6285c3db370f
keywords:
- faceforward HLSL
topic_type:
- apiref
api_name:
- faceforward
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c6a3f035ed4f0d16b500864f941bc4fe5413ff54
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084635"
---
# <a name="faceforward"></a><span data-ttu-id="4a638-104">faceforward</span><span class="sxs-lookup"><span data-stu-id="4a638-104">faceforward</span></span>

<span data-ttu-id="4a638-105">Inverte a superfície – normal (se necessário) para enfrentar uma direção oposta à i; Retorna o resultado em n.</span><span class="sxs-lookup"><span data-stu-id="4a638-105">Flips the surface-normal (if needed) to face in a direction opposite to i; returns the result in n.</span></span>



| <span data-ttu-id="4a638-106">*RET* faceforward (*n*, *i*, *ng*)</span><span class="sxs-lookup"><span data-stu-id="4a638-106">*ret* faceforward(*n*, *i*, *ng*)</span></span> |
|-----------------------------------|



 

<span data-ttu-id="4a638-107">Essa função usa a seguinte fórmula:-*n*  sinal (ponto (*i*, *ng*)).</span><span class="sxs-lookup"><span data-stu-id="4a638-107">This function uses the following formula: -*n*  sign(dot(*i*, *ng*)).</span></span>

## <a name="parameters"></a><span data-ttu-id="4a638-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4a638-108">Parameters</span></span>



| <span data-ttu-id="4a638-109">Item</span><span class="sxs-lookup"><span data-stu-id="4a638-109">Item</span></span>                                                      | <span data-ttu-id="4a638-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="4a638-110">Description</span></span>                                                                                                     |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a638-111"><span id="n"></span><span id="N"></span>*p*</span><span class="sxs-lookup"><span data-stu-id="4a638-111"><span id="n"></span><span id="N"></span>*n*</span></span><br/>    | <span data-ttu-id="4a638-112">\[na \] superfície de ponto flutuante resultante-vetor normal.</span><span class="sxs-lookup"><span data-stu-id="4a638-112">\[in\] The resulting floating-point surface-normal vector.</span></span><br/>                                           |
| <span data-ttu-id="4a638-113"><span id="i"></span><span id="I"></span>*Encontrei*</span><span class="sxs-lookup"><span data-stu-id="4a638-113"><span id="i"></span><span id="I"></span>*i*</span></span><br/>    | <span data-ttu-id="4a638-114">\[em \] um ponto flutuante, o vetor de incidente que aponta da posição de exibição para a posição de sombreamento.</span><span class="sxs-lookup"><span data-stu-id="4a638-114">\[in\] A floating-point, incident vector that points from the view position to the shading position.</span></span><br/> |
| <span data-ttu-id="4a638-115"><span id="ng"></span><span id="NG"></span>*ção*</span><span class="sxs-lookup"><span data-stu-id="4a638-115"><span id="ng"></span><span id="NG"></span>*ng*</span></span><br/> | <span data-ttu-id="4a638-116">\[em \] uma superfície de ponto flutuante-vetor normal.</span><span class="sxs-lookup"><span data-stu-id="4a638-116">\[in\] A floating-point surface-normal vector.</span></span><br/>                                                       |



 

## <a name="return-value"></a><span data-ttu-id="4a638-117">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="4a638-117">Return Value</span></span>

<span data-ttu-id="4a638-118">Um vetor de ponto flutuante, de superfície normal, que está voltado para a direção da exibição.</span><span class="sxs-lookup"><span data-stu-id="4a638-118">A floating-point, surface normal vector that is facing the view direction.</span></span>

## <a name="type-description"></a><span data-ttu-id="4a638-119">Descrição do tipo</span><span class="sxs-lookup"><span data-stu-id="4a638-119">Type Description</span></span>



| <span data-ttu-id="4a638-120">Name</span><span class="sxs-lookup"><span data-stu-id="4a638-120">Name</span></span>  | [<span data-ttu-id="4a638-121">**Tipo de modelo**</span><span class="sxs-lookup"><span data-stu-id="4a638-121">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="4a638-122">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="4a638-122">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="4a638-123">Tamanho</span><span class="sxs-lookup"><span data-stu-id="4a638-123">Size</span></span>                           |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="4a638-124">*n*</span><span class="sxs-lookup"><span data-stu-id="4a638-124">*n*</span></span>   | [<span data-ttu-id="4a638-125">**vetor**</span><span class="sxs-lookup"><span data-stu-id="4a638-125">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="4a638-126">**barra**</span><span class="sxs-lookup"><span data-stu-id="4a638-126">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="4a638-127">any</span><span class="sxs-lookup"><span data-stu-id="4a638-127">any</span></span>                            |
| <span data-ttu-id="4a638-128">*i*</span><span class="sxs-lookup"><span data-stu-id="4a638-128">*i*</span></span>   | [<span data-ttu-id="4a638-129">**vetor**</span><span class="sxs-lookup"><span data-stu-id="4a638-129">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="4a638-130">**barra**</span><span class="sxs-lookup"><span data-stu-id="4a638-130">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="4a638-131">mesma dimensão (s) como entrada *n*</span><span class="sxs-lookup"><span data-stu-id="4a638-131">same dimension(s) as input *n*</span></span> |
| <span data-ttu-id="4a638-132">*ção*</span><span class="sxs-lookup"><span data-stu-id="4a638-132">*ng*</span></span>  | [<span data-ttu-id="4a638-133">**vetor**</span><span class="sxs-lookup"><span data-stu-id="4a638-133">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="4a638-134">**barra**</span><span class="sxs-lookup"><span data-stu-id="4a638-134">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="4a638-135">mesmas dimensões como entrada *n*</span><span class="sxs-lookup"><span data-stu-id="4a638-135">same dimensions as input *n*</span></span>   |
| <span data-ttu-id="4a638-136">*RET*</span><span class="sxs-lookup"><span data-stu-id="4a638-136">*ret*</span></span> | [<span data-ttu-id="4a638-137">**vetor**</span><span class="sxs-lookup"><span data-stu-id="4a638-137">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="4a638-138">**barra**</span><span class="sxs-lookup"><span data-stu-id="4a638-138">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="4a638-139">mesmas dimensões como entrada *n*</span><span class="sxs-lookup"><span data-stu-id="4a638-139">same dimensions as input *n*</span></span>   |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="4a638-140">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="4a638-140">Minimum Shader Model</span></span>

<span data-ttu-id="4a638-141">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="4a638-141">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="4a638-142">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="4a638-142">Shader Model</span></span>                                                                       | <span data-ttu-id="4a638-143">Com suporte</span><span class="sxs-lookup"><span data-stu-id="4a638-143">Supported</span></span>             |
|------------------------------------------------------------------------------------|-----------------------|
| <span data-ttu-id="4a638-144">[Modelo do sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="4a638-144">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="4a638-145">sim</span><span class="sxs-lookup"><span data-stu-id="4a638-145">yes</span></span>                   |
| [<span data-ttu-id="4a638-146">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4a638-146">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="4a638-147">vs \_ 1 \_ 1 e PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="4a638-147">vs\_1\_1 and ps\_1\_4</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="4a638-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="4a638-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a638-149">**Funções intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="4a638-149">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

