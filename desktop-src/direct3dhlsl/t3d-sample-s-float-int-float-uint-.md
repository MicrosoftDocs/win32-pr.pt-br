---
title: 'Função Texture3D:: Sample (S, float, int, float, uint)'
description: 'Exemplifica uma textura com um valor opcional para fixe os valores de nível de detalhe (LOD) de exemplo para e retorna o status da operação. | Função Texture3D:: Sample (S, float, int, float, uint)'
ms.assetid: DB8401A1-1065-4616-BDDE-9ADB59B09C8B
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
ms.openlocfilehash: 1f1704a30ba689d50bc9c551ac6a43a4a38f90a9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104989148"
---
# <a name="texture3dsamplesfloatintfloatuint-function"></a><span data-ttu-id="aa3bc-105">Função Texture3D:: Sample (S, float, int, float, uint)</span><span class="sxs-lookup"><span data-stu-id="aa3bc-105">Texture3D::Sample(S,float,int,float,uint) function</span></span>

<span data-ttu-id="aa3bc-106">Exemplifica uma textura com um valor opcional para fixe os valores de nível de detalhe (LOD) de exemplo para e retorna o status da operação.</span><span class="sxs-lookup"><span data-stu-id="aa3bc-106">Samples a texture with an optional value to clamp sample level-of-detail (LOD) values to, and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa3bc-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="aa3bc-107">Syntax</span></span>


``` syntax
DXGI_FORMAT Sample(
  in  SamplerState S,
  in  float        Location,
  in  int          Offset,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="aa3bc-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aa3bc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa3bc-109">*S* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="aa3bc-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa3bc-110">Um [estado de amostra](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="aa3bc-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="aa3bc-111">Este é um objeto declarado em um arquivo de efeito que contém atribuições de estado.</span><span class="sxs-lookup"><span data-stu-id="aa3bc-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="aa3bc-112">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="aa3bc-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa3bc-113">As coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="aa3bc-113">The texture coordinates.</span></span> <span data-ttu-id="aa3bc-114">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="aa3bc-114">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="aa3bc-115">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="aa3bc-115">Texture-Object Type</span></span>                    | <span data-ttu-id="aa3bc-116">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="aa3bc-116">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="aa3bc-117">Texture1D</span><span class="sxs-lookup"><span data-stu-id="aa3bc-117">Texture1D</span></span>                              | <span data-ttu-id="aa3bc-118">FLOAT</span><span class="sxs-lookup"><span data-stu-id="aa3bc-118">float</span></span>          |
| <span data-ttu-id="aa3bc-119">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="aa3bc-119">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="aa3bc-120">float2</span><span class="sxs-lookup"><span data-stu-id="aa3bc-120">float2</span></span>         |
| <span data-ttu-id="aa3bc-121">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="aa3bc-121">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="aa3bc-122">float3</span><span class="sxs-lookup"><span data-stu-id="aa3bc-122">float3</span></span>         |
| <span data-ttu-id="aa3bc-123">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="aa3bc-123">TextureCubeArray</span></span>                       | <span data-ttu-id="aa3bc-124">float4</span><span class="sxs-lookup"><span data-stu-id="aa3bc-124">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="aa3bc-125">*Deslocamento* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="aa3bc-125">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa3bc-126">Um deslocamento de coordenadas de textura opcional, que pode ser usado para qualquer tipo de objeto de textura; o deslocamento é aplicado ao local antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="aa3bc-126">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="aa3bc-127">Use um deslocamento somente em um inteiro MipLevel; caso contrário, você poderá obter resultados que não se traduzem bem em hardware.</span><span class="sxs-lookup"><span data-stu-id="aa3bc-127">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="aa3bc-128">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="aa3bc-128">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="aa3bc-129">Para obter mais informações, consulte [aplicando deslocamentos de inteiro](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="aa3bc-129">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="aa3bc-130">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="aa3bc-130">Texture-Object Type</span></span>           | <span data-ttu-id="aa3bc-131">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="aa3bc-131">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="aa3bc-132">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="aa3bc-132">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="aa3bc-133">INT</span><span class="sxs-lookup"><span data-stu-id="aa3bc-133">int</span></span>            |
| <span data-ttu-id="aa3bc-134">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="aa3bc-134">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="aa3bc-135">int2</span><span class="sxs-lookup"><span data-stu-id="aa3bc-135">int2</span></span>           |
| <span data-ttu-id="aa3bc-136">Texture3D</span><span class="sxs-lookup"><span data-stu-id="aa3bc-136">Texture3D</span></span>                     | <span data-ttu-id="aa3bc-137">Int3</span><span class="sxs-lookup"><span data-stu-id="aa3bc-137">int3</span></span>           |
| <span data-ttu-id="aa3bc-138">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="aa3bc-138">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="aa3bc-139">sem suporte</span><span class="sxs-lookup"><span data-stu-id="aa3bc-139">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="aa3bc-140">*Fixe* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="aa3bc-140">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa3bc-141">Um valor opcional para fixe os valores de LOD de exemplo para.</span><span class="sxs-lookup"><span data-stu-id="aa3bc-141">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="aa3bc-142">Por exemplo, se você passar 2.0 f para o valor fixe, certifique-se de que nenhum exemplo individual acessa um nível de MIP menor que 2,0 f.</span><span class="sxs-lookup"><span data-stu-id="aa3bc-142">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="aa3bc-143">*Status* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="aa3bc-143">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aa3bc-144">O status da operação.</span><span class="sxs-lookup"><span data-stu-id="aa3bc-144">The status of the operation.</span></span> <span data-ttu-id="aa3bc-145">Você não pode acessar o status diretamente; em vez disso, passe o status para a função intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="aa3bc-145">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="aa3bc-146">**CheckAccessFullyMapped** retornará **true** se todos os valores da operação de **amostra**, **coleta** ou **carregamento** correspondente acessaram os blocos mapeados em um recurso de bloco ao [lado](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="aa3bc-146">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="aa3bc-147">Se qualquer valor tiver sido tirado de um bloco não mapeado, **CheckAccessFullyMapped** retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="aa3bc-147">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa3bc-148">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="aa3bc-148">Return value</span></span>

<span data-ttu-id="aa3bc-149">O formato de textura, que é um dos valores tipados listados [**no \_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="aa3bc-149">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="aa3bc-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="aa3bc-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa3bc-151">Métodos de exemplo</span><span class="sxs-lookup"><span data-stu-id="aa3bc-151">Sample methods</span></span>](texture3d-sample.md)
</dt> <dt>

[<span data-ttu-id="aa3bc-152">**Texture3D**</span><span class="sxs-lookup"><span data-stu-id="aa3bc-152">**Texture3D**</span></span>](sm5-object-texture3d.md)
</dt> </dl>

 

 
