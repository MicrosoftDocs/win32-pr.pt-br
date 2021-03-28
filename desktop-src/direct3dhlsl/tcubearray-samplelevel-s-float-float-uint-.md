---
title: 'Função SampleLevel:: SampleLevel (S, float, float, uint)'
description: 'Obtém uma textura no nível de mipmap especificado e retorna o status sobre a operação. | Função SampleLevel:: SampleLevel (S, float, float, uint)'
ms.assetid: 3794D17F-BC70-4D3A-9F2C-ADF900983D2C
keywords:
- HLSL da função SampleLevel
topic_type:
- apiref
api_name:
- SampleLevel
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 356e2779d82e886946e93d2071ae693279c07eb8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104172754"
---
# <a name="samplelevelsamplelevelsfloatfloatuint-function"></a><span data-ttu-id="15667-105">Função SampleLevel:: SampleLevel (S, float, float, uint)</span><span class="sxs-lookup"><span data-stu-id="15667-105">SampleLevel::SampleLevel(S,float,float,uint) function</span></span>

<span data-ttu-id="15667-106">Obtém uma textura no nível de mipmap especificado e retorna o status sobre a operação.</span><span class="sxs-lookup"><span data-stu-id="15667-106">Samples a texture on the specified mipmap level and returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="15667-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="15667-107">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleLevel(
  in  SamplerState S,
  in  float        Location,
  in  float        LOD,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="15667-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="15667-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15667-109">*S* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="15667-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15667-110">Tipo: **samplestate**</span><span class="sxs-lookup"><span data-stu-id="15667-110">Type: **SamplerState**</span></span>

<span data-ttu-id="15667-111">Um [estado de amostra](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="15667-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="15667-112">Este é um objeto declarado em um arquivo de efeito que contém atribuições de estado.</span><span class="sxs-lookup"><span data-stu-id="15667-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="15667-113">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="15667-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15667-114">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="15667-114">Type: **float**</span></span>

<span data-ttu-id="15667-115">As coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="15667-115">The texture coordinates.</span></span> <span data-ttu-id="15667-116">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="15667-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="15667-117">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="15667-117">Texture-Object Type</span></span>                    | <span data-ttu-id="15667-118">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="15667-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="15667-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="15667-119">Texture1D</span></span>                              | <span data-ttu-id="15667-120">FLOAT</span><span class="sxs-lookup"><span data-stu-id="15667-120">float</span></span>          |
| <span data-ttu-id="15667-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="15667-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="15667-122">float2</span><span class="sxs-lookup"><span data-stu-id="15667-122">float2</span></span>         |
| <span data-ttu-id="15667-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="15667-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="15667-124">float3</span><span class="sxs-lookup"><span data-stu-id="15667-124">float3</span></span>         |
| <span data-ttu-id="15667-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="15667-125">TextureCubeArray</span></span>                       | <span data-ttu-id="15667-126">float4</span><span class="sxs-lookup"><span data-stu-id="15667-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="15667-127">*LOD* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="15667-127">*LOD* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15667-128">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="15667-128">Type: **float**</span></span>

<span data-ttu-id="15667-129">\[em \] um número que especifica o nível de mipmap.</span><span class="sxs-lookup"><span data-stu-id="15667-129">\[in\] A number that specifies the mipmap level.</span></span> <span data-ttu-id="15667-130">Se o valor for ≤ 0, o nível de mipmap 0 (maior mapa) será usado.</span><span class="sxs-lookup"><span data-stu-id="15667-130">If the value is ≤ 0, mipmap level 0 (biggest map) is used.</span></span> <span data-ttu-id="15667-131">O valor fracionário (se fornecido) é usado para interpolar entre dois níveis de mipmap.</span><span class="sxs-lookup"><span data-stu-id="15667-131">The fractional value (if supplied) is used to interpolate between two mipmap levels.</span></span>

</dd> <dt>

<span data-ttu-id="15667-132">*Status* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="15667-132">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="15667-133">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="15667-133">Type: **uint**</span></span>

<span data-ttu-id="15667-134">O status da operação.</span><span class="sxs-lookup"><span data-stu-id="15667-134">The status of the operation.</span></span> <span data-ttu-id="15667-135">Você não pode acessar o status diretamente; em vez disso, passe o status para a função intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="15667-135">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="15667-136">**CheckAccessFullyMapped** retornará **true** se todos os valores da operação de **amostra**, **coleta** ou **carregamento** correspondente acessaram os blocos mapeados em um recurso de bloco ao [lado](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="15667-136">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="15667-137">Se qualquer valor tiver sido tirado de um bloco não mapeado, **CheckAccessFullyMapped** retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="15667-137">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15667-138">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="15667-138">Return value</span></span>

<span data-ttu-id="15667-139">Tipo: **[ **\_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="15667-139">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="15667-140">O formato de textura, que é um dos valores tipados listados [**no \_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="15667-140">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="15667-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="15667-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15667-142">Métodos SampleLevel</span><span class="sxs-lookup"><span data-stu-id="15667-142">SampleLevel methods</span></span>](texturecubearray-samplelevel.md)
</dt> <dt>

[<span data-ttu-id="15667-143">**TextureCubeArray**</span><span class="sxs-lookup"><span data-stu-id="15667-143">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
