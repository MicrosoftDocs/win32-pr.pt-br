---
title: cruzadas
description: Retorna o produto cruzado de dois vetores 3D de ponto flutuante.
ms.assetid: 5f1832af-6bc5-49a7-956a-fd762f674f5f
keywords:
- HLSL cruzado
topic_type:
- apiref
api_name:
- cross
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 91959bf415c3e56edf370942de268523bf998743
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104988708"
---
# <a name="cross"></a><span data-ttu-id="4e24f-104">cruzadas</span><span class="sxs-lookup"><span data-stu-id="4e24f-104">cross</span></span>

<span data-ttu-id="4e24f-105">Retorna o produto cruzado de dois vetores 3D de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="4e24f-105">Returns the cross product of two floating-point, 3D vectors.</span></span>



| <span data-ttu-id="4e24f-106">cruzada de *RET* (*x*, *y*)</span><span class="sxs-lookup"><span data-stu-id="4e24f-106">*ret* cross(*x*, *y*)</span></span> |
|-----------------------|



 

## <a name="parameters"></a><span data-ttu-id="4e24f-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4e24f-107">Parameters</span></span>



| <span data-ttu-id="4e24f-108">Item</span><span class="sxs-lookup"><span data-stu-id="4e24f-108">Item</span></span>                                                   | <span data-ttu-id="4e24f-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="4e24f-109">Description</span></span>                                             |
|--------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="4e24f-110"><span id="x"></span><span id="X"></span>*w.x.y.*</span><span class="sxs-lookup"><span data-stu-id="4e24f-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="4e24f-111">\[no \] primeiro ponto flutuante, vetor 3D.</span><span class="sxs-lookup"><span data-stu-id="4e24f-111">\[in\] The first floating-point, 3D vector.</span></span><br/>  |
| <span data-ttu-id="4e24f-112"><span id="y"></span><span id="Y"></span>*Iar*</span><span class="sxs-lookup"><span data-stu-id="4e24f-112"><span id="y"></span><span id="Y"></span>*y*</span></span><br/> | <span data-ttu-id="4e24f-113">\[no \] segundo ponto flutuante, vetor 3D.</span><span class="sxs-lookup"><span data-stu-id="4e24f-113">\[in\] The second floating-point, 3D vector.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="4e24f-114">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="4e24f-114">Return Value</span></span>

<span data-ttu-id="4e24f-115">O produto cruzado do parâmetro *x* e o parâmetro *y* .</span><span class="sxs-lookup"><span data-stu-id="4e24f-115">The cross product of the *x* parameter and the *y* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="4e24f-116">Descrição do tipo</span><span class="sxs-lookup"><span data-stu-id="4e24f-116">Type Description</span></span>



| <span data-ttu-id="4e24f-117">Name</span><span class="sxs-lookup"><span data-stu-id="4e24f-117">Name</span></span>  | [<span data-ttu-id="4e24f-118">**Tipo de modelo**</span><span class="sxs-lookup"><span data-stu-id="4e24f-118">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="4e24f-119">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="4e24f-119">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="4e24f-120">Tamanho</span><span class="sxs-lookup"><span data-stu-id="4e24f-120">Size</span></span> |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="4e24f-121">*x*</span><span class="sxs-lookup"><span data-stu-id="4e24f-121">*x*</span></span>   | [<span data-ttu-id="4e24f-122">**vetor**</span><span class="sxs-lookup"><span data-stu-id="4e24f-122">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="4e24f-123">**barra**</span><span class="sxs-lookup"><span data-stu-id="4e24f-123">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="4e24f-124">3</span><span class="sxs-lookup"><span data-stu-id="4e24f-124">3</span></span>    |
| <span data-ttu-id="4e24f-125">*y*</span><span class="sxs-lookup"><span data-stu-id="4e24f-125">*y*</span></span>   | [<span data-ttu-id="4e24f-126">**vetor**</span><span class="sxs-lookup"><span data-stu-id="4e24f-126">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="4e24f-127">**barra**</span><span class="sxs-lookup"><span data-stu-id="4e24f-127">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="4e24f-128">3</span><span class="sxs-lookup"><span data-stu-id="4e24f-128">3</span></span>    |
| <span data-ttu-id="4e24f-129">*RET*</span><span class="sxs-lookup"><span data-stu-id="4e24f-129">*ret*</span></span> | [<span data-ttu-id="4e24f-130">**vetor**</span><span class="sxs-lookup"><span data-stu-id="4e24f-130">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="4e24f-131">**barra**</span><span class="sxs-lookup"><span data-stu-id="4e24f-131">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="4e24f-132">3</span><span class="sxs-lookup"><span data-stu-id="4e24f-132">3</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="4e24f-133">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="4e24f-133">Minimum Shader Model</span></span>

<span data-ttu-id="4e24f-134">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="4e24f-134">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="4e24f-135">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="4e24f-135">Shader Model</span></span>                                                                       | <span data-ttu-id="4e24f-136">Com suporte</span><span class="sxs-lookup"><span data-stu-id="4e24f-136">Supported</span></span>             |
|------------------------------------------------------------------------------------|-----------------------|
| <span data-ttu-id="4e24f-137">[Modelo do sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="4e24f-137">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="4e24f-138">sim</span><span class="sxs-lookup"><span data-stu-id="4e24f-138">yes</span></span>                   |
| [<span data-ttu-id="4e24f-139">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4e24f-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="4e24f-140">vs \_ 1 \_ 1 e PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="4e24f-140">vs\_1\_1 and ps\_1\_4</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="4e24f-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="4e24f-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e24f-142">**Funções intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="4e24f-142">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

