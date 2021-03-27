---
title: Função de exemplo (S, float, int, float, uint) (referência de HLSL)
description: Exemplifica um Texture2D com um valor opcional para fixe de exemplo (LOD) de amostra para e retorna o status da operação.
ms.assetid: 1B9F48C4-DDB9-4547-B4AF-81A3ADA44C3F
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
ms.openlocfilehash: 9b378cb4031acecb8e0018053c7547e1948cc3e6
ms.sourcegitcommit: 0d6365d4e852b09a9100d9cfb9a5334922ebf478
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/17/2020
ms.locfileid: "103643079"
---
# <a name="samplesfloatintfloatuint-function-hlsl-reference"></a><span data-ttu-id="f18dd-104">Função de exemplo (S, float, int, float, uint) (referência de HLSL)</span><span class="sxs-lookup"><span data-stu-id="f18dd-104">Sample(S,float,int,float,uint) function (HLSL reference)</span></span>

<span data-ttu-id="f18dd-105">Exemplifica um [**Texture2D**](sm5-object-texture2d.md) com um valor opcional para fixe de exemplo (LOD) de amostra para e retorna o status da operação.</span><span class="sxs-lookup"><span data-stu-id="f18dd-105">Samples a [**Texture2D**](sm5-object-texture2d.md) with an optional value to clamp sample level-of-detail (LOD) values to, and returns status of the operation.</span></span>

> [!Note]  
> <span data-ttu-id="f18dd-106">Requer o [modelo de sombreador 5](d3d11-graphics-reference-sm5.md) ou superior.</span><span class="sxs-lookup"><span data-stu-id="f18dd-106">Requires [shader model 5](d3d11-graphics-reference-sm5.md) or higher.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="f18dd-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f18dd-107">Syntax</span></span>

``` syntax
DXGI_FORMAT Sample(
  in  SamplerState S,
  in  float Location,
  in  int Offset,
  in  float Clamp,
  out uint Status
);
```

## <a name="parameters"></a><span data-ttu-id="f18dd-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f18dd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f18dd-109">*S* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="f18dd-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f18dd-110">Um [estado de amostra](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="f18dd-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="f18dd-111">Este é um objeto declarado em um arquivo de efeito que contém atribuições de estado.</span><span class="sxs-lookup"><span data-stu-id="f18dd-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="f18dd-112">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="f18dd-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f18dd-113">As coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="f18dd-113">The texture coordinates.</span></span> <span data-ttu-id="f18dd-114">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="f18dd-114">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="f18dd-115">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="f18dd-115">Texture-Object Type</span></span>                    | <span data-ttu-id="f18dd-116">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="f18dd-116">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="f18dd-117">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f18dd-117">Texture1D</span></span>                              | <span data-ttu-id="f18dd-118">FLOAT</span><span class="sxs-lookup"><span data-stu-id="f18dd-118">float</span></span>          |
| <span data-ttu-id="f18dd-119">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="f18dd-119">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="f18dd-120">float2</span><span class="sxs-lookup"><span data-stu-id="f18dd-120">float2</span></span>         |
| <span data-ttu-id="f18dd-121">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="f18dd-121">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="f18dd-122">float3</span><span class="sxs-lookup"><span data-stu-id="f18dd-122">float3</span></span>         |
| <span data-ttu-id="f18dd-123">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="f18dd-123">TextureCubeArray</span></span>                       | <span data-ttu-id="f18dd-124">float4</span><span class="sxs-lookup"><span data-stu-id="f18dd-124">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="f18dd-125">*Deslocamento* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f18dd-125">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f18dd-126">Um deslocamento de coordenadas de textura opcional, que pode ser usado para qualquer tipo de objeto de textura; o deslocamento é aplicado ao local antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="f18dd-126">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="f18dd-127">Os deslocamentos de textura precisam ser estáticos.</span><span class="sxs-lookup"><span data-stu-id="f18dd-127">The texture offsets need to be static.</span></span> <span data-ttu-id="f18dd-128">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="f18dd-128">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="f18dd-129">Para obter mais informações, consulte [aplicando deslocamentos de coordenadas de textura](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="f18dd-129">For more info, see [Applying texture coordinate offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="f18dd-130">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="f18dd-130">Texture-Object Type</span></span>           | <span data-ttu-id="f18dd-131">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="f18dd-131">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="f18dd-132">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="f18dd-132">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="f18dd-133">INT</span><span class="sxs-lookup"><span data-stu-id="f18dd-133">int</span></span>            |
| <span data-ttu-id="f18dd-134">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="f18dd-134">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="f18dd-135">int2</span><span class="sxs-lookup"><span data-stu-id="f18dd-135">int2</span></span>           |
| <span data-ttu-id="f18dd-136">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f18dd-136">Texture3D</span></span>                     | <span data-ttu-id="f18dd-137">Int3</span><span class="sxs-lookup"><span data-stu-id="f18dd-137">int3</span></span>           |
| <span data-ttu-id="f18dd-138">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="f18dd-138">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="f18dd-139">sem suporte</span><span class="sxs-lookup"><span data-stu-id="f18dd-139">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="f18dd-140">*Fixe* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f18dd-140">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f18dd-141">Um valor opcional para fixe os valores de LOD de exemplo para.</span><span class="sxs-lookup"><span data-stu-id="f18dd-141">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="f18dd-142">Por exemplo, se você passar 2.0 f para o valor fixe, certifique-se de que nenhum exemplo individual acessa um nível de MIP menor que 2,0 f.</span><span class="sxs-lookup"><span data-stu-id="f18dd-142">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="f18dd-143">*Status* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="f18dd-143">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f18dd-144">O status da operação.</span><span class="sxs-lookup"><span data-stu-id="f18dd-144">The status of the operation.</span></span> <span data-ttu-id="f18dd-145">Você não pode acessar o status diretamente; em vez disso, passe o status para a função intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="f18dd-145">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="f18dd-146">**CheckAccessFullyMapped** retornará **true** se todos os valores da operação de **amostra**, **coleta** ou **carregamento** correspondente acessaram os blocos mapeados em um recurso de bloco ao [lado](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="f18dd-146">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="f18dd-147">Se qualquer valor tiver sido tirado de um bloco não mapeado, **CheckAccessFullyMapped** retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="f18dd-147">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f18dd-148">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f18dd-148">Return value</span></span>

<span data-ttu-id="f18dd-149">O formato de textura, que é um dos valores tipados listados [**no \_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="f18dd-149">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="remarks"></a><span data-ttu-id="f18dd-150">Comentários</span><span class="sxs-lookup"><span data-stu-id="f18dd-150">Remarks</span></span>

<span data-ttu-id="f18dd-151">A amostragem de textura usa a posição Texel para pesquisar um valor de Texel.</span><span class="sxs-lookup"><span data-stu-id="f18dd-151">Texture sampling uses the texel position to look up a texel value.</span></span> <span data-ttu-id="f18dd-152">Um deslocamento pode ser aplicado à posição antes da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="f18dd-152">An offset can be applied to the position before lookup.</span></span> <span data-ttu-id="f18dd-153">O estado de amostra contém as opções de amostragem e filtragem.</span><span class="sxs-lookup"><span data-stu-id="f18dd-153">The sampler state contains the sampling and filtering options.</span></span> <span data-ttu-id="f18dd-154">Esse método pode ser invocado dentro de um sombreador de pixel, mas não tem suporte em um sombreador de vértice ou em um sombreador de geometria.</span><span class="sxs-lookup"><span data-stu-id="f18dd-154">This method can be invoked within a pixel shader, but it is not supported in a vertex shader or a geometry shader.</span></span>

<span data-ttu-id="f18dd-155">Use um deslocamento somente em um inteiro MipLevel; caso contrário, você poderá obter resultados diferentes dependendo da implementação do hardware ou das configurações do driver.</span><span class="sxs-lookup"><span data-stu-id="f18dd-155">Use an offset only at an integer miplevel; otherwise, you may get different results depending on hardware implementation or driver settings.</span></span>

### <a name="calculating-texel-positions"></a><span data-ttu-id="f18dd-156">Calculando posições texels</span><span class="sxs-lookup"><span data-stu-id="f18dd-156">Calculating Texel Positions</span></span>

<span data-ttu-id="f18dd-157">As coordenadas de textura são valores de ponto flutuante que referenciam dados de textura, que também são conhecidos como espaço de textura normalizado.</span><span class="sxs-lookup"><span data-stu-id="f18dd-157">Texture coordinates are floating-point values that reference texture data, which is also known as normalized texture space.</span></span> <span data-ttu-id="f18dd-158">Os modos de disposição de endereço são aplicados nesta ordem (coordenadas de textura + deslocamentos + modo de encapsulamento) para modificar as coordenadas de textura fora do \[ intervalo 0... 1 \] .</span><span class="sxs-lookup"><span data-stu-id="f18dd-158">Address wrapping modes are applied in this order (texture coordinates + offsets + wrap mode) to modify texture coordinates outside the \[0...1\] range.</span></span>

<span data-ttu-id="f18dd-159">Para matrizes de textura, um valor adicional no parâmetro Location especifica um índice em uma matriz de textura.</span><span class="sxs-lookup"><span data-stu-id="f18dd-159">For texture arrays, an additional value in the location parameter specifies an index into a texture array.</span></span> <span data-ttu-id="f18dd-160">Esse índice é tratado como um valor flutuante de escala (em vez do espaço normalizado para coordenadas de textura padrão).</span><span class="sxs-lookup"><span data-stu-id="f18dd-160">This index is treated as a scaled float value (instead of the normalized space for standard texture coordinates).</span></span> <span data-ttu-id="f18dd-161">A conversão para um índice de inteiro é feita na seguinte ordem (float + Round-to-the mais próximo inteiro + fixe para o intervalo de matriz).</span><span class="sxs-lookup"><span data-stu-id="f18dd-161">The conversion to an integer index is done in the following order (float + round-to-nearest-even integer + clamp to the array range).</span></span>

### <a name="applying-texture-coordinate-offsets"></a><span data-ttu-id="f18dd-162">Aplicando deslocamentos de coordenadas de textura</span><span class="sxs-lookup"><span data-stu-id="f18dd-162">Applying Texture Coordinate Offsets</span></span>

<span data-ttu-id="f18dd-163">O parâmetro offset modifica as coordenadas de textura, no espaço Texel.</span><span class="sxs-lookup"><span data-stu-id="f18dd-163">The offset parameter modifies the texture coordinates, in texel space.</span></span> <span data-ttu-id="f18dd-164">Embora as coordenadas de textura sejam números de ponto flutuante normalizados, o deslocamento aplica um deslocamento de inteiro.</span><span class="sxs-lookup"><span data-stu-id="f18dd-164">Even though texture coordinates are normalized floating-point numbers, the offset applies an integer offset.</span></span> <span data-ttu-id="f18dd-165">Observe também que os deslocamentos de textura precisam ser estáticos.</span><span class="sxs-lookup"><span data-stu-id="f18dd-165">Also note that the texture offsets need to be static.</span></span>

<span data-ttu-id="f18dd-166">O formato de dados retornado é determinado pelo formato de textura.</span><span class="sxs-lookup"><span data-stu-id="f18dd-166">The data format returned is determined by the texture format.</span></span> <span data-ttu-id="f18dd-167">Por exemplo, se o recurso de textura tiver sido definido com o formato DXGI \_ \_ A8B8G8R8 \_ UNORM \_ sRGB, a operação de amostragem converterá texels de amostra de gama 2,0 para 1,0, filtrará e gravará o resultado como um valor de ponto flutuante no intervalo \[ 0.. 1 \] .</span><span class="sxs-lookup"><span data-stu-id="f18dd-167">For example, if the texture resource was defined with the DXGI\_FORMAT\_A8B8G8R8\_UNORM\_SRGB format, the sampling operation converts sampled texels from gamma 2.0 to 1.0, filter, and writes the result as a floating-point value in the range \[0..1\].</span></span>

## <a name="see-also"></a><span data-ttu-id="f18dd-168">Confira também</span><span class="sxs-lookup"><span data-stu-id="f18dd-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f18dd-169">Métodos de exemplo</span><span class="sxs-lookup"><span data-stu-id="f18dd-169">Sample methods</span></span>](texture-sample-overload.md)
</dt> <dt>

[<span data-ttu-id="f18dd-170">Textura-objeto</span><span class="sxs-lookup"><span data-stu-id="f18dd-170">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 
