---
title: função ddy_fine
description: Computa uma derivada parcial de alta precisão em relação à coordenada x de espaço de tela. | função ddy_fine
ms.assetid: 29fcdbc9-470b-4b5b-b18c-f75dd2c87920
keywords:
- função ddy_fine HLSL
topic_type:
- apiref
api_name:
- ddy_fine
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2a4cb297180a4988cb049ccebfa4f82571c4655c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104989262"
---
# <a name="ddy_fine-function"></a><span data-ttu-id="07a80-105">ddy \_ função fina</span><span class="sxs-lookup"><span data-stu-id="07a80-105">ddy\_fine function</span></span>

<span data-ttu-id="07a80-106">Computa uma derivada parcial de alta precisão em relação à coordenada x de espaço de tela.</span><span class="sxs-lookup"><span data-stu-id="07a80-106">Computes a high precision partial derivative with respect to the screen-space x-coordinate.</span></span>

## <a name="syntax"></a><span data-ttu-id="07a80-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="07a80-107">Syntax</span></span>

``` syntax
float ddy_fine(
  in float value
);
```

## <a name="parameters"></a><span data-ttu-id="07a80-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="07a80-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07a80-109">*valor* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="07a80-109">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07a80-110">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="07a80-110">Type: **float**</span></span>

<span data-ttu-id="07a80-111">O valor de entrada.</span><span class="sxs-lookup"><span data-stu-id="07a80-111">The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07a80-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="07a80-112">Return value</span></span>

<span data-ttu-id="07a80-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="07a80-113">Type: **float**</span></span>

<span data-ttu-id="07a80-114">O derivativo parcial de alta precisão do *valor*.</span><span class="sxs-lookup"><span data-stu-id="07a80-114">The high precision partial derivative of *value*.</span></span>

## <a name="remarks"></a><span data-ttu-id="07a80-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="07a80-115">Remarks</span></span>

<span data-ttu-id="07a80-116">As seguintes versões sobrecarregadas também estão disponíveis:</span><span class="sxs-lookup"><span data-stu-id="07a80-116">The following overloaded versions are also available:</span></span>

``` syntax
float2 ddy_fine(float2 value);
float3 ddy_fine(float3 value);
float4 ddy_fine(float4 value);  
```

### <a name="minimum-shader-model"></a><span data-ttu-id="07a80-117">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="07a80-117">Minimum Shader Model</span></span>

<span data-ttu-id="07a80-118">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="07a80-118">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="07a80-119">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="07a80-119">Shader Model</span></span>                                                                | <span data-ttu-id="07a80-120">Com suporte</span><span class="sxs-lookup"><span data-stu-id="07a80-120">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="07a80-121">[Modelo](d3d11-graphics-reference-sm5.md) de sombreador 5 e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="07a80-121">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="07a80-122">sim</span><span class="sxs-lookup"><span data-stu-id="07a80-122">yes</span></span>       |



 

<span data-ttu-id="07a80-123">Essa função tem suporte nos seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="07a80-123">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="07a80-124">Vértice</span><span class="sxs-lookup"><span data-stu-id="07a80-124">Vertex</span></span> | <span data-ttu-id="07a80-125">Envoltória</span><span class="sxs-lookup"><span data-stu-id="07a80-125">Hull</span></span> | <span data-ttu-id="07a80-126">Domínio</span><span class="sxs-lookup"><span data-stu-id="07a80-126">Domain</span></span> | <span data-ttu-id="07a80-127">Geometria</span><span class="sxs-lookup"><span data-stu-id="07a80-127">Geometry</span></span> | <span data-ttu-id="07a80-128">16x16</span><span class="sxs-lookup"><span data-stu-id="07a80-128">Pixel</span></span> | <span data-ttu-id="07a80-129">Computação</span><span class="sxs-lookup"><span data-stu-id="07a80-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="07a80-130">x</span><span class="sxs-lookup"><span data-stu-id="07a80-130">x</span></span>     |         |



 

## <a name="see-also"></a><span data-ttu-id="07a80-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="07a80-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07a80-132">Funções intrínsecas</span><span class="sxs-lookup"><span data-stu-id="07a80-132">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="07a80-133">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="07a80-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




