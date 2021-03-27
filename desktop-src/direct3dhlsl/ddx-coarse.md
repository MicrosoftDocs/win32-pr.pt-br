---
title: função ddx_coarse
description: Computa uma derivada parcial de baixa precisão em relação à coordenada x de espaço de tela.
ms.assetid: 5719f45d-b2ae-4916-8f31-c2797b661814
keywords:
- função ddx_coarse HLSL
topic_type:
- apiref
api_name:
- ddx_coarse
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4f9d4805a1d516a5d8980fcd8209fd6733fe86c4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104006679"
---
# <a name="ddx_coarse-function"></a><span data-ttu-id="6e7b9-104">\_função campo DDX grande</span><span class="sxs-lookup"><span data-stu-id="6e7b9-104">ddx\_coarse function</span></span>

<span data-ttu-id="6e7b9-105">Computa uma derivada parcial de baixa precisão em relação à coordenada x de espaço de tela.</span><span class="sxs-lookup"><span data-stu-id="6e7b9-105">Computes a low precision partial derivative with respect to the screen-space x-coordinate.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e7b9-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6e7b9-106">Syntax</span></span>

``` syntax
float ddx_coarse(
  in float value
);
```

## <a name="parameters"></a><span data-ttu-id="6e7b9-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6e7b9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e7b9-108">*valor* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="6e7b9-108">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e7b9-109">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="6e7b9-109">Type: **float**</span></span>

<span data-ttu-id="6e7b9-110">O valor de entrada.</span><span class="sxs-lookup"><span data-stu-id="6e7b9-110">The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e7b9-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6e7b9-111">Return value</span></span>

<span data-ttu-id="6e7b9-112">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="6e7b9-112">Type: **float**</span></span>

<span data-ttu-id="6e7b9-113">O derivativo parcial de baixa precisão do *valor*.</span><span class="sxs-lookup"><span data-stu-id="6e7b9-113">The low precision partial derivative of *value*.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e7b9-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="6e7b9-114">Remarks</span></span>

<span data-ttu-id="6e7b9-115">As seguintes versões sobrecarregadas também estão disponíveis:</span><span class="sxs-lookup"><span data-stu-id="6e7b9-115">The following overloaded versions are also available:</span></span>

``` syntax
float2 ddx_coarse(float2 value);
float3 ddx_coarse(float3 value);
float4 ddx_coarse(float4 value);
```

### <a name="minimum-shader-model"></a><span data-ttu-id="6e7b9-116">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="6e7b9-116">Minimum Shader Model</span></span>

<span data-ttu-id="6e7b9-117">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="6e7b9-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="6e7b9-118">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="6e7b9-118">Shader Model</span></span>                                                                | <span data-ttu-id="6e7b9-119">Com suporte</span><span class="sxs-lookup"><span data-stu-id="6e7b9-119">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="6e7b9-120">[Modelo](d3d11-graphics-reference-sm5.md) de sombreador 5 e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="6e7b9-120">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="6e7b9-121">sim</span><span class="sxs-lookup"><span data-stu-id="6e7b9-121">yes</span></span>       |



 

<span data-ttu-id="6e7b9-122">Essa função tem suporte nos seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="6e7b9-122">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="6e7b9-123">Vértice</span><span class="sxs-lookup"><span data-stu-id="6e7b9-123">Vertex</span></span> | <span data-ttu-id="6e7b9-124">Envoltória</span><span class="sxs-lookup"><span data-stu-id="6e7b9-124">Hull</span></span> | <span data-ttu-id="6e7b9-125">Domínio</span><span class="sxs-lookup"><span data-stu-id="6e7b9-125">Domain</span></span> | <span data-ttu-id="6e7b9-126">Geometria</span><span class="sxs-lookup"><span data-stu-id="6e7b9-126">Geometry</span></span> | <span data-ttu-id="6e7b9-127">16x16</span><span class="sxs-lookup"><span data-stu-id="6e7b9-127">Pixel</span></span> | <span data-ttu-id="6e7b9-128">Computação</span><span class="sxs-lookup"><span data-stu-id="6e7b9-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="6e7b9-129">x</span><span class="sxs-lookup"><span data-stu-id="6e7b9-129">x</span></span>     |         |



 

## <a name="see-also"></a><span data-ttu-id="6e7b9-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="6e7b9-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e7b9-131">Funções intrínsecas</span><span class="sxs-lookup"><span data-stu-id="6e7b9-131">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="6e7b9-132">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="6e7b9-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




