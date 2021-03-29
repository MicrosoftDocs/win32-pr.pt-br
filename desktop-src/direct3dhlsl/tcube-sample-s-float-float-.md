---
title: 'Função TextureCube:: Sample (S, float, float)'
description: 'Amostras de uma textura com um valor opcional para fixe os valores de nível de detalhe (LOD) de exemplo para. | Função TextureCube:: Sample (S, float, float)'
ms.assetid: 7DB25135-46B5-48E2-91D0-A45D355179D6
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
ms.openlocfilehash: 2ce841eb68e426fc76032d45353f2b439f0f3e4b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104172621"
---
# <a name="texturecubesamplesfloatfloat-function"></a><span data-ttu-id="40473-105">Função TextureCube:: Sample (S, float, float)</span><span class="sxs-lookup"><span data-stu-id="40473-105">TextureCube::Sample(S,float,float) function</span></span>

<span data-ttu-id="40473-106">Amostras de uma textura com um valor opcional para fixe os valores de nível de detalhe (LOD) de exemplo para.</span><span class="sxs-lookup"><span data-stu-id="40473-106">Samples a texture with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="40473-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="40473-107">Syntax</span></span>


``` syntax
DXGI_FORMAT Sample(
  in SamplerState S,
  in float        Location,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="40473-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="40473-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40473-109">*S* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="40473-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40473-110">Tipo: **samplestate**</span><span class="sxs-lookup"><span data-stu-id="40473-110">Type: **SamplerState**</span></span>

<span data-ttu-id="40473-111">Um [estado de amostra](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="40473-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="40473-112">Este é um objeto declarado em um arquivo de efeito que contém atribuições de estado.</span><span class="sxs-lookup"><span data-stu-id="40473-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="40473-113">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="40473-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40473-114">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="40473-114">Type: **float**</span></span>

<span data-ttu-id="40473-115">As coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="40473-115">The texture coordinates.</span></span> <span data-ttu-id="40473-116">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="40473-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="40473-117">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="40473-117">Texture-Object Type</span></span>                    | <span data-ttu-id="40473-118">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="40473-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="40473-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="40473-119">Texture1D</span></span>                              | <span data-ttu-id="40473-120">FLOAT</span><span class="sxs-lookup"><span data-stu-id="40473-120">float</span></span>          |
| <span data-ttu-id="40473-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="40473-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="40473-122">float2</span><span class="sxs-lookup"><span data-stu-id="40473-122">float2</span></span>         |
| <span data-ttu-id="40473-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="40473-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="40473-124">float3</span><span class="sxs-lookup"><span data-stu-id="40473-124">float3</span></span>         |
| <span data-ttu-id="40473-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="40473-125">TextureCubeArray</span></span>                       | <span data-ttu-id="40473-126">float4</span><span class="sxs-lookup"><span data-stu-id="40473-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="40473-127">*Fixe* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="40473-127">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40473-128">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="40473-128">Type: **float**</span></span>

<span data-ttu-id="40473-129">Um valor opcional para fixe os valores de LOD de exemplo para.</span><span class="sxs-lookup"><span data-stu-id="40473-129">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="40473-130">Por exemplo, se você passar 2.0 f para o valor fixe, certifique-se de que nenhum exemplo individual acessa um nível de MIP menor que 2,0 f.</span><span class="sxs-lookup"><span data-stu-id="40473-130">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40473-131">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="40473-131">Return value</span></span>

<span data-ttu-id="40473-132">Tipo: **[ **\_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="40473-132">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="40473-133">O formato de textura, que é um dos valores tipados listados [**no \_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="40473-133">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="40473-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="40473-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40473-135">Métodos de exemplo</span><span class="sxs-lookup"><span data-stu-id="40473-135">Sample methods</span></span>](texturecube-sample.md)
</dt> <dt>

[<span data-ttu-id="40473-136">**TextureCube**</span><span class="sxs-lookup"><span data-stu-id="40473-136">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
