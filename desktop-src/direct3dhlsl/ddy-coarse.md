---
title: função ddy_coarse
description: Computa uma derivada parcial de baixa precisão em relação à coordenada y de espaço de tela.
ms.assetid: f6103cd3-f7ee-41c2-b3cf-9e72ca84b25e
keywords:
- função ddy_coarse HLSL
topic_type:
- apiref
api_name:
- ddy_coarse
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b6fef330e919a31e39306742bb03280454d47626
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104006678"
---
# <a name="ddy_coarse-function"></a><span data-ttu-id="186bb-104">\_função ddy grande</span><span class="sxs-lookup"><span data-stu-id="186bb-104">ddy\_coarse function</span></span>

<span data-ttu-id="186bb-105">Computa uma derivada parcial de baixa precisão em relação à coordenada y de espaço de tela.</span><span class="sxs-lookup"><span data-stu-id="186bb-105">Computes a low precision partial derivative with respect to the screen-space y-coordinate.</span></span>

## <a name="syntax"></a><span data-ttu-id="186bb-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="186bb-106">Syntax</span></span>

``` syntax
float ddy_coarse(
  in float value
);
```

## <a name="parameters"></a><span data-ttu-id="186bb-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="186bb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="186bb-108">*valor* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="186bb-108">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="186bb-109">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="186bb-109">Type: **float**</span></span>

<span data-ttu-id="186bb-110">O valor de entrada.</span><span class="sxs-lookup"><span data-stu-id="186bb-110">The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="186bb-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="186bb-111">Return value</span></span>

<span data-ttu-id="186bb-112">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="186bb-112">Type: **float**</span></span>

<span data-ttu-id="186bb-113">O derivativo parcial de baixa precisão do *valor*.</span><span class="sxs-lookup"><span data-stu-id="186bb-113">The low precision partial derivative of *value*.</span></span>

## <a name="remarks"></a><span data-ttu-id="186bb-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="186bb-114">Remarks</span></span>

<span data-ttu-id="186bb-115">As seguintes versões sobrecarregadas também estão disponíveis:</span><span class="sxs-lookup"><span data-stu-id="186bb-115">The following overloaded versions are also available:</span></span>

``` syntax
float2 ddy_coarse(float2 value);
float3 ddy_coarse(float3 value);
float4 ddy_coarse(float4 value);
```

### <a name="minimum-shader-model"></a><span data-ttu-id="186bb-116">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="186bb-116">Minimum Shader Model</span></span>

<span data-ttu-id="186bb-117">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="186bb-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="186bb-118">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="186bb-118">Shader Model</span></span>                                                                | <span data-ttu-id="186bb-119">Com suporte</span><span class="sxs-lookup"><span data-stu-id="186bb-119">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="186bb-120">[Modelo](d3d11-graphics-reference-sm5.md) de sombreador 5 e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="186bb-120">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="186bb-121">sim</span><span class="sxs-lookup"><span data-stu-id="186bb-121">yes</span></span>       |



 

<span data-ttu-id="186bb-122">Essa função tem suporte nos seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="186bb-122">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="186bb-123">Vértice</span><span class="sxs-lookup"><span data-stu-id="186bb-123">Vertex</span></span> | <span data-ttu-id="186bb-124">Envoltória</span><span class="sxs-lookup"><span data-stu-id="186bb-124">Hull</span></span> | <span data-ttu-id="186bb-125">Domínio</span><span class="sxs-lookup"><span data-stu-id="186bb-125">Domain</span></span> | <span data-ttu-id="186bb-126">Geometria</span><span class="sxs-lookup"><span data-stu-id="186bb-126">Geometry</span></span> | <span data-ttu-id="186bb-127">16x16</span><span class="sxs-lookup"><span data-stu-id="186bb-127">Pixel</span></span> | <span data-ttu-id="186bb-128">Computação</span><span class="sxs-lookup"><span data-stu-id="186bb-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="186bb-129">x</span><span class="sxs-lookup"><span data-stu-id="186bb-129">x</span></span>     |         |



 

## <a name="see-also"></a><span data-ttu-id="186bb-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="186bb-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="186bb-131">Funções intrínsecas</span><span class="sxs-lookup"><span data-stu-id="186bb-131">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="186bb-132">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="186bb-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




