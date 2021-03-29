---
title: 'Texture2DMSArray:: sample. Função Operator'
description: 'Retorna uma variável de recurso somente leitura. | Texture2DMSArray:: sample. Função Operator'
ms.assetid: 5334c1d5-dfbd-4987-875c-0b92967b0f13
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
ms.openlocfilehash: e78746e0afe03e65a313982ca35c27a75ea14f1b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968516"
---
# <a name="texture2dmsarraysampleoperator----function"></a><span data-ttu-id="04e5d-105">Texture2DMSArray:: sample. Função Operator</span><span class="sxs-lookup"><span data-stu-id="04e5d-105">Texture2DMSArray::sample.Operator    function</span></span>

<span data-ttu-id="04e5d-106">Retorna uma variável de recurso somente leitura.</span><span class="sxs-lookup"><span data-stu-id="04e5d-106">Returns a read-only resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="04e5d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="04e5d-107">Syntax</span></span>

``` syntax
R sample.Operator[][](
  in uint sampleSlice,
  in uint3 pos
);
```

## <a name="parameters"></a><span data-ttu-id="04e5d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="04e5d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04e5d-109">*sampleSlice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="04e5d-109">*sampleSlice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04e5d-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="04e5d-110">Type: **uint**</span></span>

<span data-ttu-id="04e5d-111">O índice de fatia de exemplo.</span><span class="sxs-lookup"><span data-stu-id="04e5d-111">The sample slice index.</span></span>

</dd> <dt>

<span data-ttu-id="04e5d-112">*pos* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="04e5d-112">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04e5d-113">Tipo: **uint3**</span><span class="sxs-lookup"><span data-stu-id="04e5d-113">Type: **uint3**</span></span>

<span data-ttu-id="04e5d-114">A posição do índice.</span><span class="sxs-lookup"><span data-stu-id="04e5d-114">The index position.</span></span> <span data-ttu-id="04e5d-115">O primeiro e o segundo componentes contêm as coordenadas (x, y).</span><span class="sxs-lookup"><span data-stu-id="04e5d-115">The first and second components contain the (x, y) coordinates.</span></span> <span data-ttu-id="04e5d-116">O terceiro componente indica a fatia de matriz desejada.</span><span class="sxs-lookup"><span data-stu-id="04e5d-116">The third component indicates the desired array slice.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04e5d-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="04e5d-117">Return value</span></span>

<span data-ttu-id="04e5d-118">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="04e5d-118">Type: **R**</span></span>

<span data-ttu-id="04e5d-119">Uma variável de recurso somente leitura.</span><span class="sxs-lookup"><span data-stu-id="04e5d-119">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="04e5d-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="04e5d-120">Remarks</span></span>

### <a name="usage-example"></a><span data-ttu-id="04e5d-121">Exemplo de uso</span><span class="sxs-lookup"><span data-stu-id="04e5d-121">Usage Example</span></span>


```
Texture2DMSArray<float4, 4> alpha;

float4 main( float3 tcoord : texturecoord0 ) : SV_Target
{
     return s_msTexture.sample[2][tcoord];
}
```



<span data-ttu-id="04e5d-122">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="04e5d-122">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="04e5d-123">Vértice</span><span class="sxs-lookup"><span data-stu-id="04e5d-123">Vertex</span></span> | <span data-ttu-id="04e5d-124">Envoltória</span><span class="sxs-lookup"><span data-stu-id="04e5d-124">Hull</span></span> | <span data-ttu-id="04e5d-125">Domínio</span><span class="sxs-lookup"><span data-stu-id="04e5d-125">Domain</span></span> | <span data-ttu-id="04e5d-126">Geometria</span><span class="sxs-lookup"><span data-stu-id="04e5d-126">Geometry</span></span> | <span data-ttu-id="04e5d-127">16x16</span><span class="sxs-lookup"><span data-stu-id="04e5d-127">Pixel</span></span> | <span data-ttu-id="04e5d-128">Computação</span><span class="sxs-lookup"><span data-stu-id="04e5d-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="04e5d-129">x</span><span class="sxs-lookup"><span data-stu-id="04e5d-129">x</span></span>      | <span data-ttu-id="04e5d-130">x</span><span class="sxs-lookup"><span data-stu-id="04e5d-130">x</span></span>    | <span data-ttu-id="04e5d-131">x</span><span class="sxs-lookup"><span data-stu-id="04e5d-131">x</span></span>      | <span data-ttu-id="04e5d-132">x</span><span class="sxs-lookup"><span data-stu-id="04e5d-132">x</span></span>        | <span data-ttu-id="04e5d-133">x</span><span class="sxs-lookup"><span data-stu-id="04e5d-133">x</span></span>     | <span data-ttu-id="04e5d-134">x</span><span class="sxs-lookup"><span data-stu-id="04e5d-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="04e5d-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="04e5d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04e5d-136">Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="04e5d-136">Texture2DMSArray</span></span>](sm5-object-texture2dmsarray.md)
</dt> <dt>

[<span data-ttu-id="04e5d-137">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="04e5d-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




