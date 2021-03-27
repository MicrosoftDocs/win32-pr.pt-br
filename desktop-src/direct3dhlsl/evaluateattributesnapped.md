---
title: Função EvaluateAttributeSnapped
description: Avalia no pixel centróide com um deslocamento.
ms.assetid: f5085016-0e94-49bb-96b6-42fa15c30b9f
keywords:
- HLSL da função EvaluateAttributeSnapped
topic_type:
- apiref
api_name:
- EvaluateAttributeSnapped
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 70a9389ed9e9f4fff16f82610cb611bc4da2c7a3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104988537"
---
# <a name="evaluateattributesnapped-function"></a><span data-ttu-id="884fa-104">Função EvaluateAttributeSnapped</span><span class="sxs-lookup"><span data-stu-id="884fa-104">EvaluateAttributeSnapped function</span></span>

<span data-ttu-id="884fa-105">Avalia no pixel centróide com um deslocamento.</span><span class="sxs-lookup"><span data-stu-id="884fa-105">Evaluates at the pixel centroid with an offset.</span></span>

## <a name="syntax"></a><span data-ttu-id="884fa-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="884fa-106">Syntax</span></span>

``` syntax
numeric EvaluateAttributeSnapped(
  in attrib numeric value,
  in 
            int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="884fa-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="884fa-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="884fa-108">*valor* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="884fa-108">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="884fa-109">Tipo: **Atrib. numérico**</span><span class="sxs-lookup"><span data-stu-id="884fa-109">Type: **attrib numeric**</span></span>

<span data-ttu-id="884fa-110">O valor de entrada.</span><span class="sxs-lookup"><span data-stu-id="884fa-110">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="884fa-111">*deslocamento* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="884fa-111">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="884fa-112">Tipo: **Int2**</span><span class="sxs-lookup"><span data-stu-id="884fa-112">Type: **int2**</span></span>

<span data-ttu-id="884fa-113">Um deslocamento 2D do centro de pixels usando uma grade de 16x16.</span><span class="sxs-lookup"><span data-stu-id="884fa-113">A 2D offset from the pixel center using a 16x16 grid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="884fa-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="884fa-114">Remarks</span></span>

<span data-ttu-id="884fa-115">O intervalo para o parâmetro de *deslocamento* deve ser definido pelo seguinte código de byte.</span><span class="sxs-lookup"><span data-stu-id="884fa-115">The range for the *offset* parameter must be defined by the following byte code.</span></span>

<span data-ttu-id="884fa-116">Somente os 4 bits menos significativos dos primeiros dois componentes (U, V) do deslocamento de pixel são usados.</span><span class="sxs-lookup"><span data-stu-id="884fa-116">Only the least significant 4 bits of the first two components (U, V) of the pixel offset are used.</span></span> <span data-ttu-id="884fa-117">A conversão do ponto fixo de 4 bits para float é a seguinte (MSB... LSB), em que o MSB é uma parte da fração e determina o sinal:</span><span class="sxs-lookup"><span data-stu-id="884fa-117">The conversion from the 4-bit fixed point to float is as follows (MSB...LSB), where the MSB is both a part of the fraction and determines the sign:</span></span>

-   <span data-ttu-id="884fa-118">1000 =-0,5 f (-8/16)</span><span class="sxs-lookup"><span data-stu-id="884fa-118">1000 = -0.5f (-8 / 16)</span></span>
-   <span data-ttu-id="884fa-119">1001 =-0.4375 f (-7/16)</span><span class="sxs-lookup"><span data-stu-id="884fa-119">1001 = -0.4375f (-7 / 16)</span></span>
-   <span data-ttu-id="884fa-120">1010 =-0.375 f (-6/16)</span><span class="sxs-lookup"><span data-stu-id="884fa-120">1010 = -0.375f (-6 / 16)</span></span>
-   <span data-ttu-id="884fa-121">1011 =-0.3125 f (-5/16)</span><span class="sxs-lookup"><span data-stu-id="884fa-121">1011 = -0.3125f (-5 / 16)</span></span>
-   <span data-ttu-id="884fa-122">1100 =-0,25 f (-4/16)</span><span class="sxs-lookup"><span data-stu-id="884fa-122">1100 = -0.25f (-4 / 16)</span></span>
-   <span data-ttu-id="884fa-123">1101 =-0.1875 f (-3/16)</span><span class="sxs-lookup"><span data-stu-id="884fa-123">1101 = -0.1875f (-3 / 16)</span></span>
-   <span data-ttu-id="884fa-124">1110 =-0,125 f (-2/16)</span><span class="sxs-lookup"><span data-stu-id="884fa-124">1110 = -0.125f (-2 / 16)</span></span>
-   <span data-ttu-id="884fa-125">1111 =-0.0625 f (-1/16)</span><span class="sxs-lookup"><span data-stu-id="884fa-125">1111 = -0.0625f (-1 / 16)</span></span>
-   <span data-ttu-id="884fa-126">0000 = 0,0 f (0/16)</span><span class="sxs-lookup"><span data-stu-id="884fa-126">0000 = 0.0f ( 0 / 16)</span></span>
-   <span data-ttu-id="884fa-127">0001 = 0.0625 f (1/16)</span><span class="sxs-lookup"><span data-stu-id="884fa-127">0001 = 0.0625f ( 1 / 16)</span></span>
-   <span data-ttu-id="884fa-128">0010 = 0,125 f (2/16)</span><span class="sxs-lookup"><span data-stu-id="884fa-128">0010 = 0.125f ( 2 / 16)</span></span>
-   <span data-ttu-id="884fa-129">0011 = 0.1875 f (3/16)</span><span class="sxs-lookup"><span data-stu-id="884fa-129">0011 = 0.1875f ( 3 / 16)</span></span>
-   <span data-ttu-id="884fa-130">0100 = 0,25 f (4/16)</span><span class="sxs-lookup"><span data-stu-id="884fa-130">0100 = 0.25f ( 4 / 16)</span></span>
-   <span data-ttu-id="884fa-131">0101 = 0.3125 f (5/16)</span><span class="sxs-lookup"><span data-stu-id="884fa-131">0101 = 0.3125f ( 5 / 16)</span></span>
-   <span data-ttu-id="884fa-132">0110 = 0.375 f (6/16)</span><span class="sxs-lookup"><span data-stu-id="884fa-132">0110 = 0.375f ( 6 / 16)</span></span>
-   <span data-ttu-id="884fa-133">0111 = 0.4375 f (7/16)</span><span class="sxs-lookup"><span data-stu-id="884fa-133">0111 = 0.4375f ( 7 / 16)</span></span>

> [!Note]  
> <span data-ttu-id="884fa-134">As bordas esquerda e superior de um pixel são incluídas no deslocamento; no entanto, as bordas inferior e direita não são incluídas.</span><span class="sxs-lookup"><span data-stu-id="884fa-134">The left and top edges of a pixel are included in the offset; however, the bottom and right edges are not included.</span></span> <span data-ttu-id="884fa-135">Todos os outros bits no inteiro de 32 bits você e os valores de deslocamento V são ignorados.</span><span class="sxs-lookup"><span data-stu-id="884fa-135">All other bits in the 32-bit integer U and V offset values are ignored.</span></span>

 

<span data-ttu-id="884fa-136">Uma implementação pode assumir o deslocamento fornecido pelo sombreador e obter um valor completo de ponto fixo de 32 bits (28,4), que abrange o intervalo válido, executando o seguinte cálculo:</span><span class="sxs-lookup"><span data-stu-id="884fa-136">An implementation can take the offset provided by the shader and obtain a full 32-bit fixed point value (28.4), which spans the valid range, by performing the following calculation:</span></span>


```
iU = (iU<<28)>>28  // keep lowest 4 bits and sign extend, which yields [-8..7]
```



<span data-ttu-id="884fa-137">Se uma implementação precisar mapear o deslocamento para um deslocamento de ponto flutuante, ele executará o seguinte cálculo:</span><span class="sxs-lookup"><span data-stu-id="884fa-137">If an implementation must map the offset to a floating-point offset, it performs the following calculation:</span></span>


```
fU = ((float)iU)/16
```



### <a name="minimum-shader-model"></a><span data-ttu-id="884fa-138">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="884fa-138">Minimum Shader Model</span></span>

<span data-ttu-id="884fa-139">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="884fa-139">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="884fa-140">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="884fa-140">Shader Model</span></span>                                                                | <span data-ttu-id="884fa-141">Com suporte</span><span class="sxs-lookup"><span data-stu-id="884fa-141">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="884fa-142">[Modelo](d3d11-graphics-reference-sm5.md) de sombreador 5 e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="884fa-142">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="884fa-143">sim</span><span class="sxs-lookup"><span data-stu-id="884fa-143">yes</span></span>       |



 

<span data-ttu-id="884fa-144">Essa função tem suporte nos seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="884fa-144">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="884fa-145">Vértice</span><span class="sxs-lookup"><span data-stu-id="884fa-145">Vertex</span></span> | <span data-ttu-id="884fa-146">Envoltória</span><span class="sxs-lookup"><span data-stu-id="884fa-146">Hull</span></span> | <span data-ttu-id="884fa-147">Domínio</span><span class="sxs-lookup"><span data-stu-id="884fa-147">Domain</span></span> | <span data-ttu-id="884fa-148">Geometria</span><span class="sxs-lookup"><span data-stu-id="884fa-148">Geometry</span></span> | <span data-ttu-id="884fa-149">16x16</span><span class="sxs-lookup"><span data-stu-id="884fa-149">Pixel</span></span> | <span data-ttu-id="884fa-150">Computação</span><span class="sxs-lookup"><span data-stu-id="884fa-150">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="884fa-151">x</span><span class="sxs-lookup"><span data-stu-id="884fa-151">x</span></span>     |         |



 

## <a name="see-also"></a><span data-ttu-id="884fa-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="884fa-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="884fa-153">Funções intrínsecas</span><span class="sxs-lookup"><span data-stu-id="884fa-153">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="884fa-154">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="884fa-154">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




