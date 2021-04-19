---
title: Função Process2DQuadTessFactorsMax
description: Gera os fatores de mosaico corrigidos para um patch quádruplo. | Função Process2DQuadTessFactorsMax
ms.assetid: 1de95946-d82d-42ba-93d7-ab8383fd5018
keywords:
- HLSL da função Process2DQuadTessFactorsMax
topic_type:
- apiref
api_name:
- Process2DQuadTessFactorsMax
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d090c102671ec89fa347db95da2b21b5f11adcfe
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104989155"
---
# <a name="process2dquadtessfactorsmax-function"></a><span data-ttu-id="ced54-105">Função Process2DQuadTessFactorsMax</span><span class="sxs-lookup"><span data-stu-id="ced54-105">Process2DQuadTessFactorsMax function</span></span>

<span data-ttu-id="ced54-106">Gera os fatores de mosaico corrigidos para um patch quádruplo.</span><span class="sxs-lookup"><span data-stu-id="ced54-106">Generates the corrected tessellation factors for a quad patch.</span></span>

## <a name="syntax"></a><span data-ttu-id="ced54-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ced54-107">Syntax</span></span>

``` syntax
void Process2DQuadTessFactorsMax(
  in  float4 RawEdgeFactors,
  in  float2 InsideScale,
  out float4 RoundedEdgeTessFactors,
  out float2 RoundedInsideTessFactors,
  out float2 UnroundedInsideTessFactors
);
```

## <a name="parameters"></a><span data-ttu-id="ced54-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ced54-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ced54-109">*RawEdgeFactors* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ced54-109">*RawEdgeFactors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ced54-110">Tipo: **FLOAT4**</span><span class="sxs-lookup"><span data-stu-id="ced54-110">Type: **float4**</span></span>

<span data-ttu-id="ced54-111">Os fatores de mosaico de borda, passados para o estágio Tessellator.</span><span class="sxs-lookup"><span data-stu-id="ced54-111">The edge tessellation factors, passed into the tessellator stage.</span></span>

</dd> <dt>

<span data-ttu-id="ced54-112">*InsideScale* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ced54-112">*InsideScale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ced54-113">Tipo: **float2**</span><span class="sxs-lookup"><span data-stu-id="ced54-113">Type: **float2**</span></span>

<span data-ttu-id="ced54-114">O fator de escala aplicado aos fatores de mosaico UV calculados pelo estágio de mosaico.</span><span class="sxs-lookup"><span data-stu-id="ced54-114">The scale factor applied to the UV tessellation factors computed by the tessellation stage.</span></span> <span data-ttu-id="ced54-115">O intervalo permitido para InsideScale é de 0,0 a 1,0.</span><span class="sxs-lookup"><span data-stu-id="ced54-115">The allowable range for InsideScale is 0.0 to 1.0.</span></span>

</dd> <dt>

<span data-ttu-id="ced54-116">*RoundedEdgeTessFactors* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ced54-116">*RoundedEdgeTessFactors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ced54-117">Tipo: **FLOAT4**</span><span class="sxs-lookup"><span data-stu-id="ced54-117">Type: **float4**</span></span>

<span data-ttu-id="ced54-118">Os fatores de borda arredondada-mosaico calculados pelo estágio Tessellator.</span><span class="sxs-lookup"><span data-stu-id="ced54-118">The rounded edge-tessellation factors calculated by the tessellator stage.</span></span>

</dd> <dt>

<span data-ttu-id="ced54-119">*RoundedInsideTessFactors* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ced54-119">*RoundedInsideTessFactors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ced54-120">Tipo: **float2**</span><span class="sxs-lookup"><span data-stu-id="ced54-120">Type: **float2**</span></span>

<span data-ttu-id="ced54-121">Os fatores de mosaico arredondados calculados pelo estágio Tessellator para bordas internas.</span><span class="sxs-lookup"><span data-stu-id="ced54-121">The rounded tessellation factors calculated by the tessellator stage for inside edges.</span></span>

</dd> <dt>

<span data-ttu-id="ced54-122">*UnroundedInsideTessFactors* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ced54-122">*UnroundedInsideTessFactors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ced54-123">Tipo: **float2**</span><span class="sxs-lookup"><span data-stu-id="ced54-123">Type: **float2**</span></span>

<span data-ttu-id="ced54-124">Os fatores de mosaico calculados pelo estágio Tessellator para bordas internas.</span><span class="sxs-lookup"><span data-stu-id="ced54-124">The tessellation factors calculated by the tessellator stage for inside edges.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ced54-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ced54-125">Return value</span></span>

<span data-ttu-id="ced54-126">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="ced54-126">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ced54-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="ced54-127">Remarks</span></span>

<span data-ttu-id="ced54-128">Gera os fatores de mosaico corrigidos para um patch quádruplo, computando os fatores de mosaico internos como o máximo dos fatores de mosaico de borda.</span><span class="sxs-lookup"><span data-stu-id="ced54-128">Generates the corrected tessellation factors for a quad patch, computing the inside tessellation factors as the maximum of the edge tessellation factors.</span></span> <span data-ttu-id="ced54-129">Os fatores de mosaico você e V dentro são calculados de forma independente usando os máximos dos lados opostos do domínio e, em seguida, são dimensionados por InsideScale.</span><span class="sxs-lookup"><span data-stu-id="ced54-129">The U and V inside tessellation factors are computed independently using the maximums of opposing sides of the domain, then are scaled by InsideScale.</span></span> <span data-ttu-id="ced54-130">O resultado é arredondado com base no modo de particionamento, mas os resultados não arredondados estão disponíveis usando o parâmetro UnroundedInsideTessFactors.</span><span class="sxs-lookup"><span data-stu-id="ced54-130">The result is then rounded based on the partitioning mode, but the unrounded results are available using the UnroundedInsideTessFactors parameter.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="ced54-131">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="ced54-131">Minimum Shader Model</span></span>

<span data-ttu-id="ced54-132">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="ced54-132">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="ced54-133">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="ced54-133">Shader Model</span></span>                                                                | <span data-ttu-id="ced54-134">Com suporte</span><span class="sxs-lookup"><span data-stu-id="ced54-134">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="ced54-135">[Modelo](d3d11-graphics-reference-sm5.md) de sombreador 5 e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="ced54-135">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="ced54-136">sim</span><span class="sxs-lookup"><span data-stu-id="ced54-136">yes</span></span>       |



 

<span data-ttu-id="ced54-137">Essa função tem suporte nos seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="ced54-137">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="ced54-138">Vértice</span><span class="sxs-lookup"><span data-stu-id="ced54-138">Vertex</span></span> | <span data-ttu-id="ced54-139">Envoltória</span><span class="sxs-lookup"><span data-stu-id="ced54-139">Hull</span></span> | <span data-ttu-id="ced54-140">Domínio</span><span class="sxs-lookup"><span data-stu-id="ced54-140">Domain</span></span> | <span data-ttu-id="ced54-141">Geometria</span><span class="sxs-lookup"><span data-stu-id="ced54-141">Geometry</span></span> | <span data-ttu-id="ced54-142">16x16</span><span class="sxs-lookup"><span data-stu-id="ced54-142">Pixel</span></span> | <span data-ttu-id="ced54-143">Computação</span><span class="sxs-lookup"><span data-stu-id="ced54-143">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="ced54-144">x</span><span class="sxs-lookup"><span data-stu-id="ced54-144">x</span></span>    |        |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="ced54-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="ced54-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ced54-146">Funções intrínsecas</span><span class="sxs-lookup"><span data-stu-id="ced54-146">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="ced54-147">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="ced54-147">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




