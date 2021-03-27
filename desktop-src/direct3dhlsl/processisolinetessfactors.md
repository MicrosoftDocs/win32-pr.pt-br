---
title: Função ProcessIsolineTessFactors
description: Gera os fatores de mosaico arredondados para um Isoline.
ms.assetid: 0816b3e0-cb03-4a7a-9732-e84c637b3d48
keywords:
- HLSL da função ProcessIsolineTessFactors
topic_type:
- apiref
api_name:
- ProcessIsolineTessFactors
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 10da0e5bf0f2138c57da3fcfe962bc6a88800068
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103638675"
---
# <a name="processisolinetessfactors-function"></a><span data-ttu-id="4ada8-104">Função ProcessIsolineTessFactors</span><span class="sxs-lookup"><span data-stu-id="4ada8-104">ProcessIsolineTessFactors function</span></span>

<span data-ttu-id="4ada8-105">Gera os fatores de mosaico arredondados para um Isoline.</span><span class="sxs-lookup"><span data-stu-id="4ada8-105">Generates the rounded tessellation factors for an isoline.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ada8-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4ada8-106">Syntax</span></span>

``` syntax
void ProcessIsolineTessFactors(
  in  float RawDetailFactor,
  in  float RawDensityFactor,
  out float RoundedDetailFactor,
  out float RoundedDensityFactor
);
```

## <a name="parameters"></a><span data-ttu-id="4ada8-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4ada8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ada8-108">*RawDetailFactor* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4ada8-108">*RawDetailFactor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ada8-109">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="4ada8-109">Type: **float**</span></span>

<span data-ttu-id="4ada8-110">O fator de detalhe desejado.</span><span class="sxs-lookup"><span data-stu-id="4ada8-110">The desired detail factor.</span></span>

</dd> <dt>

<span data-ttu-id="4ada8-111">*RawDensityFactor* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4ada8-111">*RawDensityFactor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ada8-112">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="4ada8-112">Type: **float**</span></span>

<span data-ttu-id="4ada8-113">O fator de densidade desejado.</span><span class="sxs-lookup"><span data-stu-id="4ada8-113">The desired density factor.</span></span>

</dd> <dt>

<span data-ttu-id="4ada8-114">*RoundedDetailFactor* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="4ada8-114">*RoundedDetailFactor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4ada8-115">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="4ada8-115">Type: **float**</span></span>

<span data-ttu-id="4ada8-116">O fator de detalhe arredondado clamped a um intervalo que pode ser usado pelo Tessellator.</span><span class="sxs-lookup"><span data-stu-id="4ada8-116">The rounded detail factor clamped to a range that can be used by the tessellator.</span></span>

</dd> <dt>

<span data-ttu-id="4ada8-117">*RoundedDensityFactor* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="4ada8-117">*RoundedDensityFactor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4ada8-118">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="4ada8-118">Type: **float**</span></span>

<span data-ttu-id="4ada8-119">O fator de densidade arredondado clamped a um rangethat pode ser usado pelo Tessellator.</span><span class="sxs-lookup"><span data-stu-id="4ada8-119">The rounded density factor clamped to a rangethat can be used by the tessellator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ada8-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4ada8-120">Return value</span></span>

<span data-ttu-id="4ada8-121">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="4ada8-121">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ada8-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="4ada8-122">Remarks</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="4ada8-123">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="4ada8-123">Minimum Shader Model</span></span>

<span data-ttu-id="4ada8-124">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="4ada8-124">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="4ada8-125">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="4ada8-125">Shader Model</span></span>                                                                | <span data-ttu-id="4ada8-126">Com suporte</span><span class="sxs-lookup"><span data-stu-id="4ada8-126">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="4ada8-127">[Modelo](d3d11-graphics-reference-sm5.md) de sombreador 5 e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="4ada8-127">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="4ada8-128">sim</span><span class="sxs-lookup"><span data-stu-id="4ada8-128">yes</span></span>       |



 

<span data-ttu-id="4ada8-129">Essa função tem suporte nos seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="4ada8-129">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="4ada8-130">Vértice</span><span class="sxs-lookup"><span data-stu-id="4ada8-130">Vertex</span></span> | <span data-ttu-id="4ada8-131">Envoltória</span><span class="sxs-lookup"><span data-stu-id="4ada8-131">Hull</span></span> | <span data-ttu-id="4ada8-132">Domínio</span><span class="sxs-lookup"><span data-stu-id="4ada8-132">Domain</span></span> | <span data-ttu-id="4ada8-133">Geometria</span><span class="sxs-lookup"><span data-stu-id="4ada8-133">Geometry</span></span> | <span data-ttu-id="4ada8-134">16x16</span><span class="sxs-lookup"><span data-stu-id="4ada8-134">Pixel</span></span> | <span data-ttu-id="4ada8-135">Computação</span><span class="sxs-lookup"><span data-stu-id="4ada8-135">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="4ada8-136">x</span><span class="sxs-lookup"><span data-stu-id="4ada8-136">x</span></span>    |        |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="4ada8-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="4ada8-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ada8-138">Funções intrínsecas</span><span class="sxs-lookup"><span data-stu-id="4ada8-138">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="4ada8-139">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="4ada8-139">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




