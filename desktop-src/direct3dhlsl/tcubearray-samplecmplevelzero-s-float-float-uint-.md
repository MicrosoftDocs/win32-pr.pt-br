---
title: 'Função SampleCmpLevelZero:: SampleCmpLevelZero (S, float, float, uint) para TextureCubeArray'
description: Faz a amostragem de uma textura no nível de mipmap 0 apenas e compara o resultado a um valor de comparação e, em seguida, retorna o status sobre a operação. Para TextureCubeArray.
ms.assetid: D73447C6-E77C-4027-B265-24F96C679357
keywords:
- HLSL da função SampleCmpLevelZero
topic_type:
- apiref
api_name:
- SampleCmpLevelZero
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ac042bd2856aa69bbba1293fb91ff74d95c0de53
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "103664122"
---
# <a name="samplecmplevelzerosamplecmplevelzerosfloatfloatuint-function-for-texturecubearray"></a><span data-ttu-id="a1077-105">Função SampleCmpLevelZero:: SampleCmpLevelZero (S, float, float, uint) para TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="a1077-105">SampleCmpLevelZero::SampleCmpLevelZero(S,float,float,uint) function for TextureCubeArray</span></span>

<span data-ttu-id="a1077-106">Faz a amostragem de uma textura no nível de mipmap 0 somente e compara o resultado a um valor de comparação.</span><span class="sxs-lookup"><span data-stu-id="a1077-106">Samples a texture on mipmap level 0 only and compares the result to a comparison value.</span></span> <span data-ttu-id="a1077-107">Retorna o status sobre a operação.</span><span class="sxs-lookup"><span data-stu-id="a1077-107">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1077-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a1077-108">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleCmpLevelZero(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="a1077-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a1077-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1077-110">*S* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="a1077-110">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1077-111">Tipo: **samplestate**</span><span class="sxs-lookup"><span data-stu-id="a1077-111">Type: **SamplerState**</span></span>

<span data-ttu-id="a1077-112">Um [estado de amostra](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="a1077-112">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="a1077-113">Este é um objeto declarado em um arquivo de efeito que contém atribuições de estado.</span><span class="sxs-lookup"><span data-stu-id="a1077-113">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="a1077-114">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="a1077-114">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1077-115">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="a1077-115">Type: **float**</span></span>

<span data-ttu-id="a1077-116">As coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="a1077-116">The texture coordinates.</span></span> <span data-ttu-id="a1077-117">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="a1077-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="a1077-118">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="a1077-118">Texture-Object Type</span></span>                    | <span data-ttu-id="a1077-119">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="a1077-119">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="a1077-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a1077-120">Texture1D</span></span>                              | <span data-ttu-id="a1077-121">FLOAT</span><span class="sxs-lookup"><span data-stu-id="a1077-121">float</span></span>          |
| <span data-ttu-id="a1077-122">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="a1077-122">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="a1077-123">float2</span><span class="sxs-lookup"><span data-stu-id="a1077-123">float2</span></span>         |
| <span data-ttu-id="a1077-124">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="a1077-124">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="a1077-125">float3</span><span class="sxs-lookup"><span data-stu-id="a1077-125">float3</span></span>         |
| <span data-ttu-id="a1077-126">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="a1077-126">TextureCubeArray</span></span>                       | <span data-ttu-id="a1077-127">float4</span><span class="sxs-lookup"><span data-stu-id="a1077-127">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="a1077-128">*Comparevalue* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a1077-128">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1077-129">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="a1077-129">Type: **float**</span></span>

<span data-ttu-id="a1077-130">Um valor de ponto flutuante a ser usado como um valor de comparação.</span><span class="sxs-lookup"><span data-stu-id="a1077-130">A floating-point value to use as a comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="a1077-131">*Status* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="a1077-131">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a1077-132">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="a1077-132">Type: **uint**</span></span>

<span data-ttu-id="a1077-133">O status da operação.</span><span class="sxs-lookup"><span data-stu-id="a1077-133">The status of the operation.</span></span> <span data-ttu-id="a1077-134">Você não pode acessar o status diretamente; em vez disso, passe o status para a função intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="a1077-134">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="a1077-135">**CheckAccessFullyMapped** retornará **true** se todos os valores da operação de **amostra**, **coleta** ou **carregamento** correspondente acessaram os blocos mapeados em um recurso de bloco ao [lado](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="a1077-135">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="a1077-136">Se qualquer valor tiver sido tirado de um bloco não mapeado, **CheckAccessFullyMapped** retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="a1077-136">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1077-137">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a1077-137">Return value</span></span>

<span data-ttu-id="a1077-138">Tipo: **[ **\_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="a1077-138">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="a1077-139">O formato de textura, que é um dos valores tipados listados [**no \_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="a1077-139">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="a1077-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="a1077-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1077-141">Métodos SampleCmpLevelZero</span><span class="sxs-lookup"><span data-stu-id="a1077-141">SampleCmpLevelZero methods</span></span>](texturecubearray-samplecmplevelzero.md)
</dt> <dt>

[<span data-ttu-id="a1077-142">**TextureCubeArray**</span><span class="sxs-lookup"><span data-stu-id="a1077-142">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
