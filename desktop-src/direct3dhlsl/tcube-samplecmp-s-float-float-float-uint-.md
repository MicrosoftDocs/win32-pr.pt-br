---
title: 'Função SampleCmp:: SampleCmp (S, float, float, float, uint) para TextureCube'
description: 'Essa função amostra uma textura usando um valor de comparação para rejeitar amostras, com um valor opcional para fixe os valores de nível de detalhe (LOD) de exemplo para. | Função SampleCmp:: SampleCmp (S, float, float, float, uint) para TextureCube'
ms.assetid: 050E2856-1E93-4C69-8213-EEC082E82D40
keywords:
- HLSL da função SampleCmp
topic_type:
- apiref
api_name:
- SampleCmp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b73bf86b0c24feae87ea0bb4150d313fff604002
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104968718"
---
# <a name="samplecmpsamplecmpsfloatfloatfloatuint-function-for-texturecube"></a><span data-ttu-id="3f559-105">Função SampleCmp:: SampleCmp (S, float, float, float, uint) para TextureCube</span><span class="sxs-lookup"><span data-stu-id="3f559-105">SampleCmp::SampleCmp(S,float,float,float,uint) function for TextureCube</span></span>

<span data-ttu-id="3f559-106">Amostras de uma textura, usando um valor de comparação para rejeitar amostras, com um valor opcional para fixe os valores de nível de detalhe (LOD) de exemplo para.</span><span class="sxs-lookup"><span data-stu-id="3f559-106">Samples a texture, using a comparison value to reject samples, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="3f559-107">Retorna o status sobre a operação.</span><span class="sxs-lookup"><span data-stu-id="3f559-107">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f559-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3f559-108">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleCmp(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="3f559-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3f559-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f559-110">*S* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="3f559-110">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f559-111">Tipo: **samplestate**</span><span class="sxs-lookup"><span data-stu-id="3f559-111">Type: **SamplerState**</span></span>

<span data-ttu-id="3f559-112">Um [estado de amostra](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="3f559-112">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="3f559-113">Este é um objeto declarado em um arquivo de efeito que contém atribuições de estado.</span><span class="sxs-lookup"><span data-stu-id="3f559-113">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="3f559-114">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="3f559-114">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f559-115">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="3f559-115">Type: **float**</span></span>

<span data-ttu-id="3f559-116">As coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="3f559-116">The texture coordinates.</span></span> <span data-ttu-id="3f559-117">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="3f559-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="3f559-118">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="3f559-118">Texture-Object Type</span></span>                    | <span data-ttu-id="3f559-119">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="3f559-119">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="3f559-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3f559-120">Texture1D</span></span>                              | <span data-ttu-id="3f559-121">FLOAT</span><span class="sxs-lookup"><span data-stu-id="3f559-121">float</span></span>          |
| <span data-ttu-id="3f559-122">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="3f559-122">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="3f559-123">float2</span><span class="sxs-lookup"><span data-stu-id="3f559-123">float2</span></span>         |
| <span data-ttu-id="3f559-124">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="3f559-124">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="3f559-125">float3</span><span class="sxs-lookup"><span data-stu-id="3f559-125">float3</span></span>         |
| <span data-ttu-id="3f559-126">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="3f559-126">TextureCubeArray</span></span>                       | <span data-ttu-id="3f559-127">float4</span><span class="sxs-lookup"><span data-stu-id="3f559-127">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="3f559-128">*Comparevalue* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3f559-128">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f559-129">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="3f559-129">Type: **float**</span></span>

<span data-ttu-id="3f559-130">Um valor de ponto flutuante a ser usado como um valor de comparação.</span><span class="sxs-lookup"><span data-stu-id="3f559-130">A floating-point value to use as a comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="3f559-131">*Fixe* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3f559-131">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f559-132">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="3f559-132">Type: **float**</span></span>

<span data-ttu-id="3f559-133">Um valor opcional para fixe os valores de LOD de exemplo para.</span><span class="sxs-lookup"><span data-stu-id="3f559-133">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="3f559-134">Por exemplo, se você passar 2.0 f para o valor fixe, certifique-se de que nenhum exemplo individual acessa um nível de MIP menor que 2,0 f.</span><span class="sxs-lookup"><span data-stu-id="3f559-134">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="3f559-135">*Status* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="3f559-135">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3f559-136">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="3f559-136">Type: **uint**</span></span>

<span data-ttu-id="3f559-137">O status da operação.</span><span class="sxs-lookup"><span data-stu-id="3f559-137">The status of the operation.</span></span> <span data-ttu-id="3f559-138">Você não pode acessar o status diretamente; em vez disso, passe o status para a função intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="3f559-138">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="3f559-139">**CheckAccessFullyMapped** retornará **true** se todos os valores da operação de **amostra**, **coleta** ou **carregamento** correspondente acessaram os blocos mapeados em um recurso de bloco ao [lado](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="3f559-139">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="3f559-140">Se qualquer valor tiver sido tirado de um bloco não mapeado, **CheckAccessFullyMapped** retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="3f559-140">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f559-141">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3f559-141">Return value</span></span>

<span data-ttu-id="3f559-142">Tipo: **[ **\_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="3f559-142">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="3f559-143">O formato de textura, que é um dos valores tipados listados [**no \_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="3f559-143">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="3f559-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="3f559-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f559-145">Métodos SampleCmp</span><span class="sxs-lookup"><span data-stu-id="3f559-145">SampleCmp methods</span></span>](texturecube-samplecmp.md)
</dt> <dt>

[<span data-ttu-id="3f559-146">**TextureCube**</span><span class="sxs-lookup"><span data-stu-id="3f559-146">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
