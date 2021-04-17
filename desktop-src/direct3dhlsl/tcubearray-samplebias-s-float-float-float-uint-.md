---
title: 'Função SampleBias:: SampleBias (S, float, float, float, uint) para TextureCubeArray'
description: 'A função SampleBias:: SampleBias (S, float, float, float, uint) para o TextureCubeArray amostras de uma textura depois de aplicar o valor de tendência ao nível de mipmap.'
ms.assetid: 376F11E6-4FFF-4685-9285-9D6143C77F2D
keywords:
- HLSL da função SampleBias
topic_type:
- apiref
api_name:
- SampleBias
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4bcd5b2239a8b2d219fde28b1c9a00a693906b5c
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/02/2021
ms.locfileid: "106187891"
---
# <a name="samplebiassamplebiassfloatfloatfloatuint-function-for-texturecubearray"></a><span data-ttu-id="e797b-104">Função SampleBias:: SampleBias (S, float, float, float, uint) para TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="e797b-104">SampleBias::SampleBias(S,float,float,float,uint) function for TextureCubeArray</span></span>

<span data-ttu-id="e797b-105">Amostra uma textura, depois de aplicar o valor de tendência ao nível de mipmap, com um valor opcional para fixe de exemplo de valores de LOD (nível de detalhe) para.</span><span class="sxs-lookup"><span data-stu-id="e797b-105">Samples a texture, after applying the bias value to the mipmap level, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="e797b-106">Retorna o status sobre a operação.</span><span class="sxs-lookup"><span data-stu-id="e797b-106">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="e797b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e797b-107">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleBias(
  in  SamplerState S,
  in  float        Location,
  in  float        Bias,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="e797b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e797b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e797b-109">*S* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="e797b-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e797b-110">Tipo: **samplestate**</span><span class="sxs-lookup"><span data-stu-id="e797b-110">Type: **SamplerState**</span></span>

<span data-ttu-id="e797b-111">Um [estado de amostra](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="e797b-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="e797b-112">Este é um objeto declarado em um arquivo de efeito que contém atribuições de estado.</span><span class="sxs-lookup"><span data-stu-id="e797b-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="e797b-113">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="e797b-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e797b-114">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="e797b-114">Type: **float**</span></span>

<span data-ttu-id="e797b-115">As coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="e797b-115">The texture coordinates.</span></span> <span data-ttu-id="e797b-116">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="e797b-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="e797b-117">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="e797b-117">Texture-Object Type</span></span>                    | <span data-ttu-id="e797b-118">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="e797b-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="e797b-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e797b-119">Texture1D</span></span>                              | <span data-ttu-id="e797b-120">FLOAT</span><span class="sxs-lookup"><span data-stu-id="e797b-120">float</span></span>          |
| <span data-ttu-id="e797b-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="e797b-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="e797b-122">float2</span><span class="sxs-lookup"><span data-stu-id="e797b-122">float2</span></span>         |
| <span data-ttu-id="e797b-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="e797b-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="e797b-124">float3</span><span class="sxs-lookup"><span data-stu-id="e797b-124">float3</span></span>         |
| <span data-ttu-id="e797b-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="e797b-125">TextureCubeArray</span></span>                       | <span data-ttu-id="e797b-126">float4</span><span class="sxs-lookup"><span data-stu-id="e797b-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="e797b-127">*Tendência* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e797b-127">*Bias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e797b-128">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="e797b-128">Type: **float**</span></span>

<span data-ttu-id="e797b-129">O valor de tendência, que é um número de ponto flutuante entre 0,0 e 1,0, inclusive, é aplicado a um nível de MIP antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="e797b-129">The bias value, which is a floating-point number between 0.0 and 1.0 inclusive, is applied to a mip level before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="e797b-130">*Fixe* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e797b-130">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e797b-131">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="e797b-131">Type: **float**</span></span>

<span data-ttu-id="e797b-132">Um valor opcional para fixe os valores de LOD de exemplo para.</span><span class="sxs-lookup"><span data-stu-id="e797b-132">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="e797b-133">Por exemplo, se você passar 2.0 f para o valor fixe, certifique-se de que nenhum exemplo individual acessa um nível de MIP menor que 2,0 f.</span><span class="sxs-lookup"><span data-stu-id="e797b-133">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="e797b-134">*Status* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="e797b-134">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e797b-135">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="e797b-135">Type: **uint**</span></span>

<span data-ttu-id="e797b-136">O status da operação.</span><span class="sxs-lookup"><span data-stu-id="e797b-136">The status of the operation.</span></span> <span data-ttu-id="e797b-137">Você não pode acessar o status diretamente; em vez disso, passe o status para a função intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="e797b-137">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="e797b-138">**CheckAccessFullyMapped** retornará **true** se todos os valores da operação de **amostra**, **coleta** ou **carregamento** correspondente acessaram os blocos mapeados em um recurso de bloco ao [lado](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="e797b-138">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="e797b-139">Se qualquer valor tiver sido tirado de um bloco não mapeado, **CheckAccessFullyMapped** retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="e797b-139">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e797b-140">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e797b-140">Return value</span></span>

<span data-ttu-id="e797b-141">Tipo: **[ **\_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="e797b-141">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="e797b-142">O formato de textura, que é um dos valores tipados listados [**no \_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="e797b-142">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="e797b-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="e797b-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e797b-144">Métodos SampleBias</span><span class="sxs-lookup"><span data-stu-id="e797b-144">SampleBias methods</span></span>](texturecubearray-samplebias.md)
</dt> <dt>

[<span data-ttu-id="e797b-145">**TextureCubeArray**</span><span class="sxs-lookup"><span data-stu-id="e797b-145">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
