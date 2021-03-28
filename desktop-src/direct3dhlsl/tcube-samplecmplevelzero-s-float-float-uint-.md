---
title: 'Função SampleCmpLevelZero:: SampleCmpLevelZero (S, float, float, uint) para TextureCube'
description: Faz a amostragem de uma textura no nível de mipmap 0 somente e compara o resultado a um valor de comparação. Retorna o status sobre a operação. Para TextureCube.
ms.assetid: FE40307D-B9BE-434F-A6EF-7CA3C5BC7D70
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
ms.openlocfilehash: ff58c51919e575260c71f7b58d8f3d0fda6c1dd1
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104968729"
---
# <a name="samplecmplevelzerosamplecmplevelzerosfloatfloatuint-function-for-texturecube"></a><span data-ttu-id="75edc-106">Função SampleCmpLevelZero:: SampleCmpLevelZero (S, float, float, uint) para TextureCube</span><span class="sxs-lookup"><span data-stu-id="75edc-106">SampleCmpLevelZero::SampleCmpLevelZero(S,float,float,uint) function for TextureCube</span></span>

<span data-ttu-id="75edc-107">Faz a amostragem de uma textura no nível de mipmap 0 somente e compara o resultado a um valor de comparação.</span><span class="sxs-lookup"><span data-stu-id="75edc-107">Samples a texture on mipmap level 0 only and compares the result to a comparison value.</span></span> <span data-ttu-id="75edc-108">Retorna o status sobre a operação.</span><span class="sxs-lookup"><span data-stu-id="75edc-108">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="75edc-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="75edc-109">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleCmpLevelZero(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="75edc-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="75edc-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75edc-111">*S* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="75edc-111">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75edc-112">Tipo: **samplestate**</span><span class="sxs-lookup"><span data-stu-id="75edc-112">Type: **SamplerState**</span></span>

<span data-ttu-id="75edc-113">Um [estado de amostra](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="75edc-113">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="75edc-114">Este é um objeto declarado em um arquivo de efeito que contém atribuições de estado.</span><span class="sxs-lookup"><span data-stu-id="75edc-114">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="75edc-115">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="75edc-115">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75edc-116">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="75edc-116">Type: **float**</span></span>

<span data-ttu-id="75edc-117">As coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="75edc-117">The texture coordinates.</span></span> <span data-ttu-id="75edc-118">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="75edc-118">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="75edc-119">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="75edc-119">Texture-Object Type</span></span>                    | <span data-ttu-id="75edc-120">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="75edc-120">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="75edc-121">Texture1D</span><span class="sxs-lookup"><span data-stu-id="75edc-121">Texture1D</span></span>                              | <span data-ttu-id="75edc-122">FLOAT</span><span class="sxs-lookup"><span data-stu-id="75edc-122">float</span></span>          |
| <span data-ttu-id="75edc-123">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="75edc-123">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="75edc-124">float2</span><span class="sxs-lookup"><span data-stu-id="75edc-124">float2</span></span>         |
| <span data-ttu-id="75edc-125">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="75edc-125">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="75edc-126">float3</span><span class="sxs-lookup"><span data-stu-id="75edc-126">float3</span></span>         |
| <span data-ttu-id="75edc-127">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="75edc-127">TextureCubeArray</span></span>                       | <span data-ttu-id="75edc-128">float4</span><span class="sxs-lookup"><span data-stu-id="75edc-128">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="75edc-129">*Comparevalue* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="75edc-129">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75edc-130">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="75edc-130">Type: **float**</span></span>

<span data-ttu-id="75edc-131">Um valor de ponto flutuante a ser usado como um valor de comparação.</span><span class="sxs-lookup"><span data-stu-id="75edc-131">A floating-point value to use as a comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="75edc-132">*Status* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="75edc-132">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="75edc-133">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="75edc-133">Type: **uint**</span></span>

<span data-ttu-id="75edc-134">O status da operação.</span><span class="sxs-lookup"><span data-stu-id="75edc-134">The status of the operation.</span></span> <span data-ttu-id="75edc-135">Você não pode acessar o status diretamente; em vez disso, passe o status para a função intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="75edc-135">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="75edc-136">**CheckAccessFullyMapped** retornará **true** se todos os valores da operação de **amostra**, **coleta** ou **carregamento** correspondente acessaram os blocos mapeados em um recurso de bloco ao [lado](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="75edc-136">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="75edc-137">Se qualquer valor tiver sido tirado de um bloco não mapeado, **CheckAccessFullyMapped** retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="75edc-137">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75edc-138">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="75edc-138">Return value</span></span>

<span data-ttu-id="75edc-139">Tipo: **[ **\_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="75edc-139">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="75edc-140">O formato de textura, que é um dos valores tipados listados [**no \_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="75edc-140">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="75edc-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="75edc-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75edc-142">Métodos SampleCmpLevelZero</span><span class="sxs-lookup"><span data-stu-id="75edc-142">SampleCmpLevelZero methods</span></span>](texturecube-samplecmplevelzero.md)
</dt> <dt>

[<span data-ttu-id="75edc-143">**TextureCube**</span><span class="sxs-lookup"><span data-stu-id="75edc-143">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
