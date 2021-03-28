---
title: 'Função TextureCube:: Sample (S, float, float, uint)'
description: 'Exemplifica uma textura com um valor opcional para fixe os valores de nível de detalhe (LOD) de exemplo para e retorna o status da operação. | Função TextureCube:: Sample (S, float, float, uint)'
ms.assetid: 8FA17583-9002-4DEC-A6D5-85B25DEA19B7
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
ms.openlocfilehash: 9a91e9a3dcc2df617f50175eb0872398bc564103
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968453"
---
# <a name="texturecubesamplesfloatfloatuint-function"></a><span data-ttu-id="d2241-105">Função TextureCube:: Sample (S, float, float, uint)</span><span class="sxs-lookup"><span data-stu-id="d2241-105">TextureCube::Sample(S,float,float,uint) function</span></span>

<span data-ttu-id="d2241-106">Exemplifica uma textura com um valor opcional para fixe os valores de nível de detalhe (LOD) de exemplo para e retorna o status da operação.</span><span class="sxs-lookup"><span data-stu-id="d2241-106">Samples a texture with an optional value to clamp sample level-of-detail (LOD) values to, and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2241-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d2241-107">Syntax</span></span>


``` syntax
DXGI_FORMAT Sample(
  in  SamplerState S,
  in  float        Location,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="d2241-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d2241-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2241-109">*S* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="d2241-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2241-110">Um [estado de amostra](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="d2241-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="d2241-111">Este é um objeto declarado em um arquivo de efeito que contém atribuições de estado.</span><span class="sxs-lookup"><span data-stu-id="d2241-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="d2241-112">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="d2241-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2241-113">As coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="d2241-113">The texture coordinates.</span></span> <span data-ttu-id="d2241-114">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="d2241-114">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="d2241-115">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="d2241-115">Texture-Object Type</span></span>                    | <span data-ttu-id="d2241-116">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="d2241-116">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="d2241-117">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d2241-117">Texture1D</span></span>                              | <span data-ttu-id="d2241-118">FLOAT</span><span class="sxs-lookup"><span data-stu-id="d2241-118">float</span></span>          |
| <span data-ttu-id="d2241-119">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="d2241-119">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="d2241-120">float2</span><span class="sxs-lookup"><span data-stu-id="d2241-120">float2</span></span>         |
| <span data-ttu-id="d2241-121">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="d2241-121">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="d2241-122">float3</span><span class="sxs-lookup"><span data-stu-id="d2241-122">float3</span></span>         |
| <span data-ttu-id="d2241-123">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="d2241-123">TextureCubeArray</span></span>                       | <span data-ttu-id="d2241-124">float4</span><span class="sxs-lookup"><span data-stu-id="d2241-124">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="d2241-125">*Fixe* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d2241-125">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2241-126">Um valor opcional para fixe os valores de LOD de exemplo para.</span><span class="sxs-lookup"><span data-stu-id="d2241-126">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="d2241-127">Por exemplo, se você passar 2.0 f para o valor fixe, certifique-se de que nenhum exemplo individual acessa um nível de MIP menor que 2,0 f.</span><span class="sxs-lookup"><span data-stu-id="d2241-127">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="d2241-128">*Status* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="d2241-128">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d2241-129">O status da operação.</span><span class="sxs-lookup"><span data-stu-id="d2241-129">The status of the operation.</span></span> <span data-ttu-id="d2241-130">Você não pode acessar o status diretamente; em vez disso, passe o status para a função intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="d2241-130">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="d2241-131">**CheckAccessFullyMapped** retornará **true** se todos os valores da operação de **amostra**, **coleta** ou **carregamento** correspondente acessaram os blocos mapeados em um recurso de bloco ao [lado](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="d2241-131">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="d2241-132">Se qualquer valor tiver sido tirado de um bloco não mapeado, **CheckAccessFullyMapped** retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="d2241-132">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2241-133">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d2241-133">Return value</span></span>

<span data-ttu-id="d2241-134">O formato de textura, que é um dos valores tipados listados [**no \_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="d2241-134">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="d2241-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="d2241-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2241-136">Métodos de exemplo</span><span class="sxs-lookup"><span data-stu-id="d2241-136">Sample methods</span></span>](texturecube-sample.md)
</dt> <dt>

[<span data-ttu-id="d2241-137">**TextureCube**</span><span class="sxs-lookup"><span data-stu-id="d2241-137">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
