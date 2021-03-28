---
title: função ddx_fine
description: Computa uma derivada parcial de alta precisão em relação à coordenada x de espaço de tela. | função ddx_fine
ms.assetid: 41062d6f-2b7f-4594-a6de-da37ded5d444
keywords:
- função ddx_fine HLSL
topic_type:
- apiref
api_name:
- ddx_fine
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c1a579ba5899cf4d3ac3f25ef5a40337f6291977
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968542"
---
# <a name="ddx_fine-function"></a><span data-ttu-id="a95d9-105">campo DDX \_ função fina</span><span class="sxs-lookup"><span data-stu-id="a95d9-105">ddx\_fine function</span></span>

<span data-ttu-id="a95d9-106">Computa uma derivada parcial de alta precisão em relação à coordenada x de espaço de tela.</span><span class="sxs-lookup"><span data-stu-id="a95d9-106">Computes a high precision partial derivative with respect to the screen-space x-coordinate.</span></span>

## <a name="syntax"></a><span data-ttu-id="a95d9-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a95d9-107">Syntax</span></span>

``` syntax
float ddx_fine(
  in float value
);
```

## <a name="parameters"></a><span data-ttu-id="a95d9-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a95d9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a95d9-109">*valor* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="a95d9-109">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a95d9-110">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="a95d9-110">Type: **float**</span></span>

<span data-ttu-id="a95d9-111">O valor de entrada.</span><span class="sxs-lookup"><span data-stu-id="a95d9-111">The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a95d9-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a95d9-112">Return value</span></span>

<span data-ttu-id="a95d9-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="a95d9-113">Type: **float**</span></span>

<span data-ttu-id="a95d9-114">O derivativo parcial de alta precisão do *valor*.</span><span class="sxs-lookup"><span data-stu-id="a95d9-114">The high precision partial derivative of *value*.</span></span>

## <a name="remarks"></a><span data-ttu-id="a95d9-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="a95d9-115">Remarks</span></span>

<span data-ttu-id="a95d9-116">As seguintes versões sobrecarregadas também estão disponíveis:</span><span class="sxs-lookup"><span data-stu-id="a95d9-116">The following overloaded versions are also available:</span></span>

``` syntax
float2 ddx_fine(float2 value);
float3 ddx_fine(float3 value);
float4 ddx_fine(float4 value);
```

### <a name="minimum-shader-model"></a><span data-ttu-id="a95d9-117">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="a95d9-117">Minimum Shader Model</span></span>

<span data-ttu-id="a95d9-118">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="a95d9-118">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="a95d9-119">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="a95d9-119">Shader Model</span></span>                                                                | <span data-ttu-id="a95d9-120">Com suporte</span><span class="sxs-lookup"><span data-stu-id="a95d9-120">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="a95d9-121">[Modelo](d3d11-graphics-reference-sm5.md) de sombreador 5 e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="a95d9-121">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="a95d9-122">sim</span><span class="sxs-lookup"><span data-stu-id="a95d9-122">yes</span></span>       |



 

<span data-ttu-id="a95d9-123">Essa função tem suporte nos seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="a95d9-123">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="a95d9-124">Vértice</span><span class="sxs-lookup"><span data-stu-id="a95d9-124">Vertex</span></span> | <span data-ttu-id="a95d9-125">Envoltória</span><span class="sxs-lookup"><span data-stu-id="a95d9-125">Hull</span></span> | <span data-ttu-id="a95d9-126">Domínio</span><span class="sxs-lookup"><span data-stu-id="a95d9-126">Domain</span></span> | <span data-ttu-id="a95d9-127">Geometria</span><span class="sxs-lookup"><span data-stu-id="a95d9-127">Geometry</span></span> | <span data-ttu-id="a95d9-128">16x16</span><span class="sxs-lookup"><span data-stu-id="a95d9-128">Pixel</span></span> | <span data-ttu-id="a95d9-129">Computação</span><span class="sxs-lookup"><span data-stu-id="a95d9-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="a95d9-130">x</span><span class="sxs-lookup"><span data-stu-id="a95d9-130">x</span></span>     |         |



 

## <a name="see-also"></a><span data-ttu-id="a95d9-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="a95d9-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a95d9-132">Funções intrínsecas</span><span class="sxs-lookup"><span data-stu-id="a95d9-132">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="a95d9-133">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="a95d9-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




