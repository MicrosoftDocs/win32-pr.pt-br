---
title: 'Função Texture2DArray:: Sample (S, float, int, float, uint)'
description: 'Exemplifica uma textura com um valor opcional para fixe os valores de nível de detalhe (LOD) de exemplo para e retorna o status da operação. | Função Texture2DArray:: Sample (S, float, int, float, uint)'
ms.assetid: 0F9DBC0D-F35D-4A7A-B8F5-1EFBF7E14615
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
ms.openlocfilehash: e2027377a1659aa46fcf10e39f39b21e2243c943
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968311"
---
# <a name="texture2darraysamplesfloatintfloatuint-function"></a><span data-ttu-id="5c539-105">Função Texture2DArray:: Sample (S, float, int, float, uint)</span><span class="sxs-lookup"><span data-stu-id="5c539-105">Texture2DArray::Sample(S,float,int,float,uint) function</span></span>

<span data-ttu-id="5c539-106">Exemplifica uma textura com um valor opcional para fixe os valores de nível de detalhe (LOD) de exemplo para e retorna o status da operação.</span><span class="sxs-lookup"><span data-stu-id="5c539-106">Samples a texture with an optional value to clamp sample level-of-detail (LOD) values to, and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c539-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5c539-107">Syntax</span></span>


``` syntax
DXGI_FORMAT Sample(
  in  SamplerState S,
  in  float        Location,
  in  int          Offset,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="5c539-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5c539-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c539-109">*S* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="5c539-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c539-110">Um [estado de amostra](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="5c539-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="5c539-111">Este é um objeto declarado em um arquivo de efeito que contém atribuições de estado.</span><span class="sxs-lookup"><span data-stu-id="5c539-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="5c539-112">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="5c539-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c539-113">As coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="5c539-113">The texture coordinates.</span></span> <span data-ttu-id="5c539-114">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="5c539-114">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="5c539-115">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="5c539-115">Texture-Object Type</span></span>                    | <span data-ttu-id="5c539-116">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="5c539-116">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="5c539-117">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5c539-117">Texture1D</span></span>                              | <span data-ttu-id="5c539-118">FLOAT</span><span class="sxs-lookup"><span data-stu-id="5c539-118">float</span></span>          |
| <span data-ttu-id="5c539-119">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="5c539-119">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="5c539-120">float2</span><span class="sxs-lookup"><span data-stu-id="5c539-120">float2</span></span>         |
| <span data-ttu-id="5c539-121">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="5c539-121">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="5c539-122">float3</span><span class="sxs-lookup"><span data-stu-id="5c539-122">float3</span></span>         |
| <span data-ttu-id="5c539-123">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="5c539-123">TextureCubeArray</span></span>                       | <span data-ttu-id="5c539-124">float4</span><span class="sxs-lookup"><span data-stu-id="5c539-124">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="5c539-125">*Deslocamento* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5c539-125">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c539-126">Um deslocamento de coordenadas de textura opcional, que pode ser usado para qualquer tipo de objeto de textura; o deslocamento é aplicado ao local antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="5c539-126">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="5c539-127">Use um deslocamento somente em um inteiro MipLevel; caso contrário, você poderá obter resultados que não se traduzem bem em hardware.</span><span class="sxs-lookup"><span data-stu-id="5c539-127">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="5c539-128">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="5c539-128">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="5c539-129">Para obter mais informações, consulte [aplicando deslocamentos de inteiro](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="5c539-129">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="5c539-130">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="5c539-130">Texture-Object Type</span></span>           | <span data-ttu-id="5c539-131">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="5c539-131">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="5c539-132">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="5c539-132">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="5c539-133">INT</span><span class="sxs-lookup"><span data-stu-id="5c539-133">int</span></span>            |
| <span data-ttu-id="5c539-134">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="5c539-134">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="5c539-135">int2</span><span class="sxs-lookup"><span data-stu-id="5c539-135">int2</span></span>           |
| <span data-ttu-id="5c539-136">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5c539-136">Texture3D</span></span>                     | <span data-ttu-id="5c539-137">Int3</span><span class="sxs-lookup"><span data-stu-id="5c539-137">int3</span></span>           |
| <span data-ttu-id="5c539-138">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="5c539-138">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="5c539-139">sem suporte</span><span class="sxs-lookup"><span data-stu-id="5c539-139">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="5c539-140">*Fixe* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5c539-140">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c539-141">Um valor opcional para fixe os valores de LOD de exemplo para.</span><span class="sxs-lookup"><span data-stu-id="5c539-141">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="5c539-142">Por exemplo, se você passar 2.0 f para o valor fixe, certifique-se de que nenhum exemplo individual acessa um nível de MIP menor que 2,0 f.</span><span class="sxs-lookup"><span data-stu-id="5c539-142">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="5c539-143">*Status* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="5c539-143">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5c539-144">O status da operação.</span><span class="sxs-lookup"><span data-stu-id="5c539-144">The status of the operation.</span></span> <span data-ttu-id="5c539-145">Você não pode acessar o status diretamente; em vez disso, passe o status para a função intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="5c539-145">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="5c539-146">**CheckAccessFullyMapped** retornará **true** se todos os valores da operação de **amostra**, **coleta** ou **carregamento** correspondente acessaram os blocos mapeados em um recurso de bloco ao [lado](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="5c539-146">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="5c539-147">Se qualquer valor tiver sido tirado de um bloco não mapeado, **CheckAccessFullyMapped** retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="5c539-147">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c539-148">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5c539-148">Return value</span></span>

<span data-ttu-id="5c539-149">O formato de textura, que é um dos valores tipados listados [**no \_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="5c539-149">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="5c539-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="5c539-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c539-151">Métodos de exemplo</span><span class="sxs-lookup"><span data-stu-id="5c539-151">Sample methods</span></span>](texture2darray-sample.md)
</dt> </dl>

 

 
