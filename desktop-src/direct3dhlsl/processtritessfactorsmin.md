---
title: Função ProcessTriTessFactorsMin
description: Gera os fatores de mosaico corrigidos para um patch tri. | Função ProcessTriTessFactorsMin
ms.assetid: fa1e19c2-fadf-42d4-9574-834eaf871393
keywords:
- HLSL da função ProcessTriTessFactorsMin
topic_type:
- apiref
api_name:
- ProcessTriTessFactorsMin
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 33f82c7935d47813d833ccc21a7ec0134adee1cc
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104506393"
---
# <a name="processtritessfactorsmin-function"></a><span data-ttu-id="32d0c-105">Função ProcessTriTessFactorsMin</span><span class="sxs-lookup"><span data-stu-id="32d0c-105">ProcessTriTessFactorsMin function</span></span>

<span data-ttu-id="32d0c-106">Gera os fatores de mosaico corrigidos para um patch tri.</span><span class="sxs-lookup"><span data-stu-id="32d0c-106">Generates the corrected tessellation factors for a tri patch.</span></span>

## <a name="syntax"></a><span data-ttu-id="32d0c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="32d0c-107">Syntax</span></span>

``` syntax
void ProcessTriTessFactorsMin(
  in  float3 RawEdgeFactors,
  in  float InsideScale,
  out float3 RoundedEdgeTessFactors,
  out float RoundedInsideTessFactors,
  out float UnroundedInsideTessFactors
);
```

## <a name="parameters"></a><span data-ttu-id="32d0c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="32d0c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32d0c-109">*RawEdgeFactors* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="32d0c-109">*RawEdgeFactors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32d0c-110">Tipo: **float3**</span><span class="sxs-lookup"><span data-stu-id="32d0c-110">Type: **float3**</span></span>

<span data-ttu-id="32d0c-111">Os fatores de mosaico de borda, passados para o estágio Tessellator.</span><span class="sxs-lookup"><span data-stu-id="32d0c-111">The edge tessellation factors, passed into the tessellator stage.</span></span>

</dd> <dt>

<span data-ttu-id="32d0c-112">*InsideScale* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="32d0c-112">*InsideScale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32d0c-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="32d0c-113">Type: **float**</span></span>

<span data-ttu-id="32d0c-114">O fator de escala aplicado aos fatores de mosaico UV calculados pelo estágio de mosaico.</span><span class="sxs-lookup"><span data-stu-id="32d0c-114">The scale factor applied to the UV tessellation factors computed by the tessellation stage.</span></span> <span data-ttu-id="32d0c-115">O intervalo permitido para InsideScale é de 0,0 a 1,0.</span><span class="sxs-lookup"><span data-stu-id="32d0c-115">The allowable range for InsideScale is 0.0 to 1.0.</span></span>

</dd> <dt>

<span data-ttu-id="32d0c-116">*RoundedEdgeTessFactors* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="32d0c-116">*RoundedEdgeTessFactors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="32d0c-117">Tipo: **float3**</span><span class="sxs-lookup"><span data-stu-id="32d0c-117">Type: **float3**</span></span>

<span data-ttu-id="32d0c-118">Os fatores de borda arredondada-mosaico calculados pelo estágio Tessellator.</span><span class="sxs-lookup"><span data-stu-id="32d0c-118">The rounded edge-tessellation factors calculated by the tessellator stage.</span></span>

</dd> <dt>

<span data-ttu-id="32d0c-119">*RoundedInsideTessFactors* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="32d0c-119">*RoundedInsideTessFactors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="32d0c-120">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="32d0c-120">Type: **float**</span></span>

<span data-ttu-id="32d0c-121">Os fatores de mosaico arredondados calculados pelo estágio Tessellator para bordas internas.</span><span class="sxs-lookup"><span data-stu-id="32d0c-121">The rounded tessellation factors calculated by the tessellator stage for inside edges.</span></span>

</dd> <dt>

<span data-ttu-id="32d0c-122">*UnroundedInsideTessFactors* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="32d0c-122">*UnroundedInsideTessFactors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="32d0c-123">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="32d0c-123">Type: **float**</span></span>

<span data-ttu-id="32d0c-124">Os fatores de mosaico calculados pelo estágio Tessellator para bordas internas.</span><span class="sxs-lookup"><span data-stu-id="32d0c-124">The tessellation factors calculated by the tessellator stage for inside edges.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32d0c-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="32d0c-125">Return value</span></span>

<span data-ttu-id="32d0c-126">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="32d0c-126">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="32d0c-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="32d0c-127">Remarks</span></span>

<span data-ttu-id="32d0c-128">Gera os fatores de mosaico corrigidos para o tri patch, computando o fator de mosaico interno como o mínimo dos fatores de mosaico de borda, que é então dimensionado por InsideScale.</span><span class="sxs-lookup"><span data-stu-id="32d0c-128">Generates the corrected tessellation factors for a tri patch, computing the inside tessellation factor as the minimum of the edge tessellation factors, which is then scaled by InsideScale.</span></span> <span data-ttu-id="32d0c-129">O resultado é arredondado com base no modo de particionamento, mas os resultados não arredondados estão disponíveis usando o parâmetro UnroundedInsideTessFactor.</span><span class="sxs-lookup"><span data-stu-id="32d0c-129">The result is then rounded based on the partitioning mode, but the unrounded results are available using the UnroundedInsideTessFactor parameter.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="32d0c-130">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="32d0c-130">Minimum Shader Model</span></span>

<span data-ttu-id="32d0c-131">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="32d0c-131">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="32d0c-132">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="32d0c-132">Shader Model</span></span>                                                                | <span data-ttu-id="32d0c-133">Com suporte</span><span class="sxs-lookup"><span data-stu-id="32d0c-133">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="32d0c-134">[Modelo](d3d11-graphics-reference-sm5.md) de sombreador 5 e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="32d0c-134">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="32d0c-135">sim</span><span class="sxs-lookup"><span data-stu-id="32d0c-135">yes</span></span>       |



 

<span data-ttu-id="32d0c-136">Essa função tem suporte nos seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="32d0c-136">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="32d0c-137">Vértice</span><span class="sxs-lookup"><span data-stu-id="32d0c-137">Vertex</span></span> | <span data-ttu-id="32d0c-138">Envoltória</span><span class="sxs-lookup"><span data-stu-id="32d0c-138">Hull</span></span> | <span data-ttu-id="32d0c-139">Domínio</span><span class="sxs-lookup"><span data-stu-id="32d0c-139">Domain</span></span> | <span data-ttu-id="32d0c-140">Geometria</span><span class="sxs-lookup"><span data-stu-id="32d0c-140">Geometry</span></span> | <span data-ttu-id="32d0c-141">16x16</span><span class="sxs-lookup"><span data-stu-id="32d0c-141">Pixel</span></span> | <span data-ttu-id="32d0c-142">Computação</span><span class="sxs-lookup"><span data-stu-id="32d0c-142">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="32d0c-143">x</span><span class="sxs-lookup"><span data-stu-id="32d0c-143">x</span></span>    |        |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="32d0c-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="32d0c-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32d0c-145">Funções intrínsecas</span><span class="sxs-lookup"><span data-stu-id="32d0c-145">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="32d0c-146">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="32d0c-146">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




