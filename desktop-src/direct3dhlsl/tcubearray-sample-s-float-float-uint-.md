---
title: 'Função TextureCubeArray:: Sample (S, float, float, uint)'
description: 'Exemplifica uma textura com um valor opcional para fixe os valores de nível de detalhe (LOD) de exemplo para e retorna o status da operação. | Função TextureCubeArray:: Sample (S, float, float, uint)'
ms.assetid: 5645841D-A32E-452E-873C-E070CF6A4C00
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
ms.openlocfilehash: 24e6d77698507f0d1673b66954db8e78466ac728
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103663890"
---
# <a name="texturecubearraysamplesfloatfloatuint-function"></a><span data-ttu-id="0fd18-105">Função TextureCubeArray:: Sample (S, float, float, uint)</span><span class="sxs-lookup"><span data-stu-id="0fd18-105">TextureCubeArray::Sample(S,float,float,uint) function</span></span>

<span data-ttu-id="0fd18-106">Exemplifica uma textura com um valor opcional para fixe os valores de nível de detalhe (LOD) de exemplo para e retorna o status da operação.</span><span class="sxs-lookup"><span data-stu-id="0fd18-106">Samples a texture with an optional value to clamp sample level-of-detail (LOD) values to, and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fd18-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0fd18-107">Syntax</span></span>


``` syntax
DXGI_FORMAT Sample(
  in  SamplerState S,
  in  float        Location,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="0fd18-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0fd18-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0fd18-109">*S* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="0fd18-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0fd18-110">Um [estado de amostra](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="0fd18-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="0fd18-111">Este é um objeto declarado em um arquivo de efeito que contém atribuições de estado.</span><span class="sxs-lookup"><span data-stu-id="0fd18-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="0fd18-112">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="0fd18-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0fd18-113">As coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="0fd18-113">The texture coordinates.</span></span> <span data-ttu-id="0fd18-114">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="0fd18-114">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="0fd18-115">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="0fd18-115">Texture-Object Type</span></span>                    | <span data-ttu-id="0fd18-116">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="0fd18-116">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="0fd18-117">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fd18-117">Texture1D</span></span>                              | <span data-ttu-id="0fd18-118">FLOAT</span><span class="sxs-lookup"><span data-stu-id="0fd18-118">float</span></span>          |
| <span data-ttu-id="0fd18-119">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fd18-119">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="0fd18-120">float2</span><span class="sxs-lookup"><span data-stu-id="0fd18-120">float2</span></span>         |
| <span data-ttu-id="0fd18-121">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fd18-121">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="0fd18-122">float3</span><span class="sxs-lookup"><span data-stu-id="0fd18-122">float3</span></span>         |
| <span data-ttu-id="0fd18-123">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="0fd18-123">TextureCubeArray</span></span>                       | <span data-ttu-id="0fd18-124">float4</span><span class="sxs-lookup"><span data-stu-id="0fd18-124">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="0fd18-125">*Fixe* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0fd18-125">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0fd18-126">Um valor opcional para fixe os valores de LOD de exemplo para.</span><span class="sxs-lookup"><span data-stu-id="0fd18-126">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="0fd18-127">Por exemplo, se você passar 2.0 f para o valor fixe, certifique-se de que nenhum exemplo individual acessa um nível de MIP menor que 2,0 f.</span><span class="sxs-lookup"><span data-stu-id="0fd18-127">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="0fd18-128">*Status* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="0fd18-128">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0fd18-129">O status da operação.</span><span class="sxs-lookup"><span data-stu-id="0fd18-129">The status of the operation.</span></span> <span data-ttu-id="0fd18-130">Você não pode acessar o status diretamente; em vez disso, passe o status para a função intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="0fd18-130">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="0fd18-131">**CheckAccessFullyMapped** retornará **true** se todos os valores da operação de **amostra**, **coleta** ou **carregamento** correspondente acessaram os blocos mapeados em um recurso de bloco ao [lado](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="0fd18-131">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="0fd18-132">Se qualquer valor tiver sido tirado de um bloco não mapeado, **CheckAccessFullyMapped** retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="0fd18-132">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0fd18-133">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0fd18-133">Return value</span></span>

<span data-ttu-id="0fd18-134">O formato de textura, que é um dos valores tipados listados [**no \_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="0fd18-134">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="0fd18-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="0fd18-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fd18-136">Métodos de exemplo</span><span class="sxs-lookup"><span data-stu-id="0fd18-136">Sample methods</span></span>](texturecubearray-sample.md)
</dt> <dt>

[<span data-ttu-id="0fd18-137">**TextureCubeArray**</span><span class="sxs-lookup"><span data-stu-id="0fd18-137">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
