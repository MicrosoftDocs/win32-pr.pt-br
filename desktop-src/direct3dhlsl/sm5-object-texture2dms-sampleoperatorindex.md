---
title: 'Texture2DMS:: sample. Função Operator'
description: 'Recupera um valor do recurso no local e no índice de exemplo fornecidos. | Texture2DMS:: sample. Função Operator'
ms.assetid: 5bc24129-b690-44dd-ae85-8533b10befaa
keywords:
- Nova. Função Operator HLSL
topic_type:
- apiref
api_name:
- sample.Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1a73577fa67992b212b4769059f1523e584acbaf
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104172869"
---
# <a name="texture2dmssampleoperator----function"></a><span data-ttu-id="73b19-105">Texture2DMS:: sample. Função Operator</span><span class="sxs-lookup"><span data-stu-id="73b19-105">Texture2DMS::sample.Operator    function</span></span>

<span data-ttu-id="73b19-106">Recupera um valor do recurso no local e no índice de exemplo fornecidos.</span><span class="sxs-lookup"><span data-stu-id="73b19-106">Retrieves a value from the resource at the location and sample index provided.</span></span>

## <a name="syntax"></a><span data-ttu-id="73b19-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="73b19-107">Syntax</span></span>

``` syntax
R sample.Operator[][](
  in uint sampleSlice,
  in uint2 pos
);
```

## <a name="parameters"></a><span data-ttu-id="73b19-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="73b19-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73b19-109">*sampleSlice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="73b19-109">*sampleSlice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73b19-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="73b19-110">Type: **uint**</span></span>

<span data-ttu-id="73b19-111">O índice de fatia de exemplo.</span><span class="sxs-lookup"><span data-stu-id="73b19-111">The sample slice index.</span></span>

</dd> <dt>

<span data-ttu-id="73b19-112">*pos* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="73b19-112">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73b19-113">Tipo: **uint2**</span><span class="sxs-lookup"><span data-stu-id="73b19-113">Type: **uint2**</span></span>

<span data-ttu-id="73b19-114">A posição do índice.</span><span class="sxs-lookup"><span data-stu-id="73b19-114">The index position.</span></span> <span data-ttu-id="73b19-115">Os componentes contêm as coordenadas (x, y).</span><span class="sxs-lookup"><span data-stu-id="73b19-115">The components contain the (x, y) coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73b19-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="73b19-116">Return value</span></span>

<span data-ttu-id="73b19-117">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="73b19-117">Type: **R**</span></span>

<span data-ttu-id="73b19-118">Uma variável de recurso somente leitura.</span><span class="sxs-lookup"><span data-stu-id="73b19-118">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="73b19-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="73b19-119">Remarks</span></span>

### <a name="usage-example"></a><span data-ttu-id="73b19-120">Exemplo de uso</span><span class="sxs-lookup"><span data-stu-id="73b19-120">Usage Example</span></span>


```
Texture2DMS<float4, 8> tex;

float4 main( float3 tcoord : texturecoord0 ) : SV_Target
{
     return s_msTexture.sample[2][tcoord];
}
```



<span data-ttu-id="73b19-121">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="73b19-121">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="73b19-122">Vértice</span><span class="sxs-lookup"><span data-stu-id="73b19-122">Vertex</span></span> | <span data-ttu-id="73b19-123">Envoltória</span><span class="sxs-lookup"><span data-stu-id="73b19-123">Hull</span></span> | <span data-ttu-id="73b19-124">Domínio</span><span class="sxs-lookup"><span data-stu-id="73b19-124">Domain</span></span> | <span data-ttu-id="73b19-125">Geometria</span><span class="sxs-lookup"><span data-stu-id="73b19-125">Geometry</span></span> | <span data-ttu-id="73b19-126">16x16</span><span class="sxs-lookup"><span data-stu-id="73b19-126">Pixel</span></span> | <span data-ttu-id="73b19-127">Computação</span><span class="sxs-lookup"><span data-stu-id="73b19-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="73b19-128">x</span><span class="sxs-lookup"><span data-stu-id="73b19-128">x</span></span>      | <span data-ttu-id="73b19-129">x</span><span class="sxs-lookup"><span data-stu-id="73b19-129">x</span></span>    | <span data-ttu-id="73b19-130">x</span><span class="sxs-lookup"><span data-stu-id="73b19-130">x</span></span>      | <span data-ttu-id="73b19-131">x</span><span class="sxs-lookup"><span data-stu-id="73b19-131">x</span></span>        | <span data-ttu-id="73b19-132">x</span><span class="sxs-lookup"><span data-stu-id="73b19-132">x</span></span>     | <span data-ttu-id="73b19-133">x</span><span class="sxs-lookup"><span data-stu-id="73b19-133">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="73b19-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="73b19-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73b19-135">Texture2DMS</span><span class="sxs-lookup"><span data-stu-id="73b19-135">Texture2DMS</span></span>](sm5-object-texture2dms.md)
</dt> <dt>

[<span data-ttu-id="73b19-136">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="73b19-136">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




