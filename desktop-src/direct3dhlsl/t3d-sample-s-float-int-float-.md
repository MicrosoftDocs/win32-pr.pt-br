---
title: 'Função Texture3D:: Sample (S, float, int, float)'
description: 'Amostras de uma textura com um valor opcional para fixe os valores de nível de detalhe (LOD) de exemplo para. | Função Texture3D:: Sample (S, float, int, float)'
ms.assetid: A1114A4A-16B9-4A5D-9A9D-262D6BAA9F2E
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
ms.openlocfilehash: 11577e6151d2353477a70e6ef2873d287eb71a87
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104989149"
---
# <a name="texture3dsamplesfloatintfloat-function"></a><span data-ttu-id="19ad7-105">Função Texture3D:: Sample (S, float, int, float)</span><span class="sxs-lookup"><span data-stu-id="19ad7-105">Texture3D::Sample(S,float,int,float) function</span></span>

<span data-ttu-id="19ad7-106">Amostras de uma textura com um valor opcional para fixe os valores de nível de detalhe (LOD) de exemplo para.</span><span class="sxs-lookup"><span data-stu-id="19ad7-106">Samples a texture with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="19ad7-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="19ad7-107">Syntax</span></span>


``` syntax
DXGI_FORMAT Sample(
  in SamplerState S,
  in float        Location,
  in int          Offset,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="19ad7-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="19ad7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19ad7-109">*S* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="19ad7-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19ad7-110">Um [estado de amostra](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="19ad7-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="19ad7-111">Este é um objeto declarado em um arquivo de efeito que contém atribuições de estado.</span><span class="sxs-lookup"><span data-stu-id="19ad7-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="19ad7-112">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="19ad7-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19ad7-113">As coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="19ad7-113">The texture coordinates.</span></span> <span data-ttu-id="19ad7-114">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="19ad7-114">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="19ad7-115">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="19ad7-115">Texture-Object Type</span></span>                    | <span data-ttu-id="19ad7-116">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="19ad7-116">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="19ad7-117">Texture1D</span><span class="sxs-lookup"><span data-stu-id="19ad7-117">Texture1D</span></span>                              | <span data-ttu-id="19ad7-118">FLOAT</span><span class="sxs-lookup"><span data-stu-id="19ad7-118">float</span></span>          |
| <span data-ttu-id="19ad7-119">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="19ad7-119">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="19ad7-120">float2</span><span class="sxs-lookup"><span data-stu-id="19ad7-120">float2</span></span>         |
| <span data-ttu-id="19ad7-121">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="19ad7-121">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="19ad7-122">float3</span><span class="sxs-lookup"><span data-stu-id="19ad7-122">float3</span></span>         |
| <span data-ttu-id="19ad7-123">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="19ad7-123">TextureCubeArray</span></span>                       | <span data-ttu-id="19ad7-124">float4</span><span class="sxs-lookup"><span data-stu-id="19ad7-124">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="19ad7-125">*Deslocamento* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="19ad7-125">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19ad7-126">Um deslocamento de coordenadas de textura opcional, que pode ser usado para qualquer tipo de objeto de textura; o deslocamento é aplicado ao local antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="19ad7-126">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="19ad7-127">Use um deslocamento somente em um inteiro MipLevel; caso contrário, você poderá obter resultados que não se traduzem bem em hardware.</span><span class="sxs-lookup"><span data-stu-id="19ad7-127">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="19ad7-128">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="19ad7-128">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="19ad7-129">Para obter mais informações, consulte [aplicando deslocamentos de inteiro](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="19ad7-129">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="19ad7-130">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="19ad7-130">Texture-Object Type</span></span>           | <span data-ttu-id="19ad7-131">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="19ad7-131">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="19ad7-132">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="19ad7-132">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="19ad7-133">INT</span><span class="sxs-lookup"><span data-stu-id="19ad7-133">int</span></span>            |
| <span data-ttu-id="19ad7-134">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="19ad7-134">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="19ad7-135">int2</span><span class="sxs-lookup"><span data-stu-id="19ad7-135">int2</span></span>           |
| <span data-ttu-id="19ad7-136">Texture3D</span><span class="sxs-lookup"><span data-stu-id="19ad7-136">Texture3D</span></span>                     | <span data-ttu-id="19ad7-137">Int3</span><span class="sxs-lookup"><span data-stu-id="19ad7-137">int3</span></span>           |
| <span data-ttu-id="19ad7-138">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="19ad7-138">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="19ad7-139">sem suporte</span><span class="sxs-lookup"><span data-stu-id="19ad7-139">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="19ad7-140">*Fixe* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="19ad7-140">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19ad7-141">Um valor opcional para fixe os valores de LOD de exemplo para.</span><span class="sxs-lookup"><span data-stu-id="19ad7-141">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="19ad7-142">Por exemplo, se você passar 2.0 f para o valor fixe, certifique-se de que nenhum exemplo individual acessa um nível de MIP menor que 2,0 f.</span><span class="sxs-lookup"><span data-stu-id="19ad7-142">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19ad7-143">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="19ad7-143">Return value</span></span>

<span data-ttu-id="19ad7-144">O formato de textura, que é um dos valores tipados listados [**no \_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="19ad7-144">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="19ad7-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="19ad7-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19ad7-146">Métodos de exemplo</span><span class="sxs-lookup"><span data-stu-id="19ad7-146">Sample methods</span></span>](texture3d-sample.md)
</dt> <dt>

[<span data-ttu-id="19ad7-147">**Texture3D**</span><span class="sxs-lookup"><span data-stu-id="19ad7-147">**Texture3D**</span></span>](sm5-object-texture3d.md)
</dt> </dl>

 

 
