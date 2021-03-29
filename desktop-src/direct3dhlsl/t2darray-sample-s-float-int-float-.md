---
title: 'Função Texture2DArray:: Sample (S, float, int, float)'
description: 'Amostras de uma textura com um valor opcional para fixe os valores de nível de detalhe (LOD) de exemplo para. | Função Texture2DArray:: Sample (S, float, int, float)'
ms.assetid: F6638224-0993-4F55-A8C0-7EC4140204D5
keywords:
- Exemplo de função HLSL
topic_type:
- apiref
api_name:
- Sample
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8d85e4d7e5662d76c011b1c5684f3fd36e4191ba
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104172676"
---
# <a name="texture2darraysamplesfloatintfloat-function"></a><span data-ttu-id="bdcdc-105">Função Texture2DArray:: Sample (S, float, int, float)</span><span class="sxs-lookup"><span data-stu-id="bdcdc-105">Texture2DArray::Sample(S,float,int,float) function</span></span>

<span data-ttu-id="bdcdc-106">Amostras de uma textura com um valor opcional para fixe os valores de nível de detalhe (LOD) de exemplo para.</span><span class="sxs-lookup"><span data-stu-id="bdcdc-106">Samples a texture with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="bdcdc-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bdcdc-107">Syntax</span></span>


``` syntax
DXGI_FORMAT Sample(
  in SamplerState S,
  in float        Location,
  in int          Offset,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="bdcdc-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bdcdc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bdcdc-109">*S* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="bdcdc-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bdcdc-110">Um [estado de amostra](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="bdcdc-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="bdcdc-111">Este é um objeto declarado em um arquivo de efeito que contém atribuições de estado.</span><span class="sxs-lookup"><span data-stu-id="bdcdc-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="bdcdc-112">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="bdcdc-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bdcdc-113">As coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="bdcdc-113">The texture coordinates.</span></span> <span data-ttu-id="bdcdc-114">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="bdcdc-114">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="bdcdc-115">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="bdcdc-115">Texture-Object Type</span></span>                    | <span data-ttu-id="bdcdc-116">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="bdcdc-116">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="bdcdc-117">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bdcdc-117">Texture1D</span></span>                              | <span data-ttu-id="bdcdc-118">FLOAT</span><span class="sxs-lookup"><span data-stu-id="bdcdc-118">float</span></span>          |
| <span data-ttu-id="bdcdc-119">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="bdcdc-119">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="bdcdc-120">float2</span><span class="sxs-lookup"><span data-stu-id="bdcdc-120">float2</span></span>         |
| <span data-ttu-id="bdcdc-121">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="bdcdc-121">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="bdcdc-122">float3</span><span class="sxs-lookup"><span data-stu-id="bdcdc-122">float3</span></span>         |
| <span data-ttu-id="bdcdc-123">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="bdcdc-123">TextureCubeArray</span></span>                       | <span data-ttu-id="bdcdc-124">float4</span><span class="sxs-lookup"><span data-stu-id="bdcdc-124">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="bdcdc-125">*Deslocamento* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bdcdc-125">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bdcdc-126">Um deslocamento de coordenadas de textura opcional, que pode ser usado para qualquer tipo de objeto de textura; o deslocamento é aplicado ao local antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="bdcdc-126">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="bdcdc-127">Use um deslocamento somente em um inteiro MipLevel; caso contrário, você poderá obter resultados que não se traduzem bem em hardware.</span><span class="sxs-lookup"><span data-stu-id="bdcdc-127">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="bdcdc-128">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="bdcdc-128">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="bdcdc-129">Para obter mais informações, consulte [aplicando deslocamentos de inteiro](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="bdcdc-129">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="bdcdc-130">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="bdcdc-130">Texture-Object Type</span></span>           | <span data-ttu-id="bdcdc-131">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="bdcdc-131">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="bdcdc-132">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="bdcdc-132">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="bdcdc-133">INT</span><span class="sxs-lookup"><span data-stu-id="bdcdc-133">int</span></span>            |
| <span data-ttu-id="bdcdc-134">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="bdcdc-134">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="bdcdc-135">int2</span><span class="sxs-lookup"><span data-stu-id="bdcdc-135">int2</span></span>           |
| <span data-ttu-id="bdcdc-136">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bdcdc-136">Texture3D</span></span>                     | <span data-ttu-id="bdcdc-137">Int3</span><span class="sxs-lookup"><span data-stu-id="bdcdc-137">int3</span></span>           |
| <span data-ttu-id="bdcdc-138">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="bdcdc-138">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="bdcdc-139">sem suporte</span><span class="sxs-lookup"><span data-stu-id="bdcdc-139">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="bdcdc-140">*Fixe* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bdcdc-140">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bdcdc-141">Um valor opcional para fixe os valores de LOD de exemplo para.</span><span class="sxs-lookup"><span data-stu-id="bdcdc-141">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="bdcdc-142">Por exemplo, se você passar 2.0 f para o valor fixe, certifique-se de que nenhum exemplo individual acessa um nível de MIP menor que 2,0 f.</span><span class="sxs-lookup"><span data-stu-id="bdcdc-142">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bdcdc-143">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bdcdc-143">Return value</span></span>

<span data-ttu-id="bdcdc-144">O formato de textura, que é um dos valores tipados listados [**no \_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="bdcdc-144">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="bdcdc-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="bdcdc-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdcdc-146">Métodos de exemplo</span><span class="sxs-lookup"><span data-stu-id="bdcdc-146">Sample methods</span></span>](texture2darray-sample.md)
</dt> </dl>

 

 
