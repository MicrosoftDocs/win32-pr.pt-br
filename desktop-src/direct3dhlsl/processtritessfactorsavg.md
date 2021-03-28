---
title: Função ProcessTriTessFactorsAvg
description: Gera os fatores de mosaico corrigidos para um patch tri. | Função ProcessTriTessFactorsAvg
ms.assetid: 005a63b6-f35d-42d6-bb29-f4ebb374080e
keywords:
- HLSL da função ProcessTriTessFactorsAvg
topic_type:
- apiref
api_name:
- ProcessTriTessFactorsAvg
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 90cfa86a09e0e76c90f0013cfa6121917ca25378
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104989170"
---
# <a name="processtritessfactorsavg-function"></a><span data-ttu-id="6546d-105">Função ProcessTriTessFactorsAvg</span><span class="sxs-lookup"><span data-stu-id="6546d-105">ProcessTriTessFactorsAvg function</span></span>

<span data-ttu-id="6546d-106">Gera os fatores de mosaico corrigidos para um patch tri.</span><span class="sxs-lookup"><span data-stu-id="6546d-106">Generates the corrected tessellation factors for a tri patch.</span></span>

## <a name="syntax"></a><span data-ttu-id="6546d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6546d-107">Syntax</span></span>

``` syntax
void ProcessTriTessFactorsAvg(
  in  float3 RawEdgeFactors,
  in  float InsideScale,
  out float3 RoundedEdgeTessFactors,
  out float RoundedInsideTessFactor,
  out float UnroundedInsideTessFactor
);
```

## <a name="parameters"></a><span data-ttu-id="6546d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6546d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6546d-109">*RawEdgeFactors* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6546d-109">*RawEdgeFactors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6546d-110">Tipo: **float3**</span><span class="sxs-lookup"><span data-stu-id="6546d-110">Type: **float3**</span></span>

<span data-ttu-id="6546d-111">Os fatores de mosaico de borda, passados para o estágio Tessellator.</span><span class="sxs-lookup"><span data-stu-id="6546d-111">The edge tessellation factors, passed into the tessellator stage.</span></span>

</dd> <dt>

<span data-ttu-id="6546d-112">*InsideScale* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6546d-112">*InsideScale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6546d-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="6546d-113">Type: **float**</span></span>

<span data-ttu-id="6546d-114">O fator de escala aplicado aos fatores de mosaico UV calculados pelo estágio de mosaico.</span><span class="sxs-lookup"><span data-stu-id="6546d-114">The scale factor applied to the UV tessellation factors computed by the tessellation stage.</span></span> <span data-ttu-id="6546d-115">O intervalo permitido para InsideScale é de 0,0 a 1,0.</span><span class="sxs-lookup"><span data-stu-id="6546d-115">The allowable range for InsideScale is 0.0 to 1.0.</span></span>

</dd> <dt>

<span data-ttu-id="6546d-116">*RoundedEdgeTessFactors* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6546d-116">*RoundedEdgeTessFactors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6546d-117">Tipo: **float3**</span><span class="sxs-lookup"><span data-stu-id="6546d-117">Type: **float3**</span></span>

<span data-ttu-id="6546d-118">Os fatores de borda arredondada-mosaico calculados pelo estágio Tessellator.</span><span class="sxs-lookup"><span data-stu-id="6546d-118">The rounded edge-tessellation factors calculated by the tessellator stage.</span></span>

</dd> <dt>

<span data-ttu-id="6546d-119">*RoundedInsideTessFactor* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6546d-119">*RoundedInsideTessFactor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6546d-120">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="6546d-120">Type: **float**</span></span>

<span data-ttu-id="6546d-121">Os fatores de mosaico calculados pelo estágio Tessellator e arredondados.</span><span class="sxs-lookup"><span data-stu-id="6546d-121">The tessellation factors calculated by the tessellator stage, and rounded.</span></span>

</dd> <dt>

<span data-ttu-id="6546d-122">*UnroundedInsideTessFactor* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6546d-122">*UnroundedInsideTessFactor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6546d-123">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="6546d-123">Type: **float**</span></span>

<span data-ttu-id="6546d-124">Os fatores de mosaico original, não arredondados e UV calculados pelo estágio de mosaico.</span><span class="sxs-lookup"><span data-stu-id="6546d-124">The original, unrounded, UV tessellation factors computed by the tessellation stage.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6546d-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6546d-125">Return value</span></span>

<span data-ttu-id="6546d-126">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="6546d-126">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6546d-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="6546d-127">Remarks</span></span>

<span data-ttu-id="6546d-128">Gera os fatores de mosaico corrigidos para o tri patch, computando o fator de mosaico interno como a média dos fatores de mosaico de borda, que é então dimensionada por InsideScale.</span><span class="sxs-lookup"><span data-stu-id="6546d-128">Generates the corrected tessellation factors for a tri patch, computing the inside tessellation factor as the average of the edge tessellation factors, which is then scaled by InsideScale.</span></span> <span data-ttu-id="6546d-129">O resultado é arredondado com base no modo de particionamento, mas os resultados não arredondados estão disponíveis usando o parâmetro UnroundedInsideTessFactor.</span><span class="sxs-lookup"><span data-stu-id="6546d-129">The result is then rounded based on the partitioning mode, but the unrounded results are available using the UnroundedInsideTessFactor parameter.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="6546d-130">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="6546d-130">Minimum Shader Model</span></span>

<span data-ttu-id="6546d-131">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="6546d-131">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="6546d-132">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="6546d-132">Shader Model</span></span>                                                                | <span data-ttu-id="6546d-133">Com suporte</span><span class="sxs-lookup"><span data-stu-id="6546d-133">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="6546d-134">[Modelo](d3d11-graphics-reference-sm5.md) de sombreador 5 e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="6546d-134">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="6546d-135">sim</span><span class="sxs-lookup"><span data-stu-id="6546d-135">yes</span></span>       |



 

<span data-ttu-id="6546d-136">Essa função tem suporte nos seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="6546d-136">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="6546d-137">Vértice</span><span class="sxs-lookup"><span data-stu-id="6546d-137">Vertex</span></span> | <span data-ttu-id="6546d-138">Envoltória</span><span class="sxs-lookup"><span data-stu-id="6546d-138">Hull</span></span> | <span data-ttu-id="6546d-139">Domínio</span><span class="sxs-lookup"><span data-stu-id="6546d-139">Domain</span></span> | <span data-ttu-id="6546d-140">Geometria</span><span class="sxs-lookup"><span data-stu-id="6546d-140">Geometry</span></span> | <span data-ttu-id="6546d-141">16x16</span><span class="sxs-lookup"><span data-stu-id="6546d-141">Pixel</span></span> | <span data-ttu-id="6546d-142">Computação</span><span class="sxs-lookup"><span data-stu-id="6546d-142">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="6546d-143">x</span><span class="sxs-lookup"><span data-stu-id="6546d-143">x</span></span>    |        |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="6546d-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="6546d-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6546d-145">Funções intrínsecas</span><span class="sxs-lookup"><span data-stu-id="6546d-145">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="6546d-146">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="6546d-146">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




