---
title: SampleCmp (objeto de textura DirectX HLSL)
description: Faz a amostragem de uma textura e compara um único componente com relação ao valor de comparação especificado.
ms.assetid: e21894c4-e8c5-4c3d-92c1-727964f8fd94
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6991bead4bfc42451c26fe5476b4c114626eb7e8
ms.sourcegitcommit: 0d6365d4e852b09a9100d9cfb9a5334922ebf478
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/17/2020
ms.locfileid: "104988726"
---
# <a name="samplecmp-directx-hlsl-texture-object"></a><span data-ttu-id="baff4-103">SampleCmp (objeto de textura DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="baff4-103">SampleCmp (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="baff4-104">Faz a amostragem de uma textura e compara um único componente com relação ao valor de comparação especificado.</span><span class="sxs-lookup"><span data-stu-id="baff4-104">Samples a texture and compares a single component against the specified comparison value.</span></span>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="baff4-105">float Object. SampleCmp (</span><span class="sxs-lookup"><span data-stu-id="baff4-105">float Object.SampleCmp(</span></span> <dl> <span data-ttu-id="baff4-106">SamplerComparisonState S,</span><span class="sxs-lookup"><span data-stu-id="baff4-106">SamplerComparisonState S,</span></span><br />
<span data-ttu-id="baff4-107">Local de flutuação,</span><span class="sxs-lookup"><span data-stu-id="baff4-107">float Location,</span></span><br />
<span data-ttu-id="baff4-108">comparent Comparevalue,</span><span class="sxs-lookup"><span data-stu-id="baff4-108">float CompareValue,</span></span><br />
<span data-ttu-id="baff4-109">[deslocamento int]</span><span class="sxs-lookup"><span data-stu-id="baff4-109">[int Offset]</span></span><br />
</dl><span data-ttu-id="baff4-110">);</span><span class="sxs-lookup"><span data-stu-id="baff4-110">);</span></span></td>
</tr>
</tbody>
</table>
 

<span data-ttu-id="baff4-111">A comparação é uma comparação de componente único entre o primeiro componente armazenado na textura e o valor de comparação passado para o método.</span><span class="sxs-lookup"><span data-stu-id="baff4-111">The comparison is a single-component comparison between the first component stored in the texture, and the comparison value passed into the method.</span></span>

<span data-ttu-id="baff4-112">Esse método pode ser invocado somente de um sombreador de pixel; Não há suporte para ele em um vértice ou sombreador de geometria.</span><span class="sxs-lookup"><span data-stu-id="baff4-112">This method can be invoked only from a pixel shader; it isn't supported in a vertex or geometry shader.</span></span>

## <a name="parameters"></a><span data-ttu-id="baff4-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="baff4-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="baff4-114"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Objeto*</span><span class="sxs-lookup"><span data-stu-id="baff4-114"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Object*</span></span>
</dt> <dd>

<span data-ttu-id="baff4-115">Qualquer tipo [de objeto de textura](dx-graphics-hlsl-to-type.md) (exceto Texture2DMS, Texture2DMSArray ou Texture3D).</span><span class="sxs-lookup"><span data-stu-id="baff4-115">Any [texture-object](dx-graphics-hlsl-to-type.md) type (except Texture2DMS, Texture2DMSArray, or Texture3D).</span></span>

</dd> <dt>

<span data-ttu-id="baff4-116"><span id="S"></span><span id="s"></span>*&*</span><span class="sxs-lookup"><span data-stu-id="baff4-116"><span id="S"></span><span id="s"></span>*S*</span></span>
</dt> <dd>

<span data-ttu-id="baff4-117">\[em \] um estado de comparação de amostras, que é o estado de amostra, mais um estado de comparação (uma função de comparação e um filtro de comparação).</span><span class="sxs-lookup"><span data-stu-id="baff4-117">\[in\] A sampler-comparison state, which is the sampler state plus a comparison state (a comparison function and a comparison filter).</span></span> <span data-ttu-id="baff4-118">Consulte o [tipo de amostra](dx-graphics-hlsl-sampler.md) para obter detalhes e um exemplo.</span><span class="sxs-lookup"><span data-stu-id="baff4-118">See the [sampler type](dx-graphics-hlsl-sampler.md) for details and an example.</span></span>

</dd> <dt>

<span data-ttu-id="baff4-119"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span>*Local*</span><span class="sxs-lookup"><span data-stu-id="baff4-119"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span>*Location*</span></span>
</dt> <dd>

<span data-ttu-id="baff4-120">\[nas \] coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="baff4-120">\[in\] The texture coordinates.</span></span> <span data-ttu-id="baff4-121">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="baff4-121">The argument type is dependent on the texture-object type.</span></span>

| <span data-ttu-id="baff4-122">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="baff4-122">Texture-Object Type</span></span>          | <span data-ttu-id="baff4-123">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="baff4-123">Parameter Type</span></span> |
|------------------------------|----------------|
| <span data-ttu-id="baff4-124">Texture1D</span><span class="sxs-lookup"><span data-stu-id="baff4-124">Texture1D</span></span>                    | <span data-ttu-id="baff4-125">FLOAT</span><span class="sxs-lookup"><span data-stu-id="baff4-125">float</span></span>          |
| <span data-ttu-id="baff4-126">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="baff4-126">Texture1DArray, Texture2D</span></span>    | <span data-ttu-id="baff4-127">float2</span><span class="sxs-lookup"><span data-stu-id="baff4-127">float2</span></span>         |
| <span data-ttu-id="baff4-128">Texture2DArray ¹, TextureCube</span><span class="sxs-lookup"><span data-stu-id="baff4-128">Texture2DArray¹, TextureCube</span></span> | <span data-ttu-id="baff4-129">float3</span><span class="sxs-lookup"><span data-stu-id="baff4-129">float3</span></span>         |
| <span data-ttu-id="baff4-130">TextureCubeArray ¹</span><span class="sxs-lookup"><span data-stu-id="baff4-130">TextureCubeArray¹</span></span>            | <span data-ttu-id="baff4-131">float4</span><span class="sxs-lookup"><span data-stu-id="baff4-131">float4</span></span>         |

</dd> <dt>

<span data-ttu-id="baff4-132"><span id="CompareValue"></span><span id="comparevalue"></span><span id="COMPAREVALUE"></span>*Comparevalue*</span><span class="sxs-lookup"><span data-stu-id="baff4-132"><span id="CompareValue"></span><span id="comparevalue"></span><span id="COMPAREVALUE"></span>*CompareValue*</span></span>
</dt> <dd>

<span data-ttu-id="baff4-133">Um valor de ponto flutuante a ser usado como um valor de comparação.</span><span class="sxs-lookup"><span data-stu-id="baff4-133">A floating-point value to use as a comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="baff4-134"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span>*Desvio*</span><span class="sxs-lookup"><span data-stu-id="baff4-134"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span>*Offset*</span></span>
</dt> <dd>

<span data-ttu-id="baff4-135">\[em \] um deslocamento de coordenadas de textura opcional, que pode ser usado para qualquer tipo de objeto de textura; o deslocamento é aplicado ao local antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="baff4-135">\[in\] An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="baff4-136">Os deslocamentos de textura precisam ser estáticos.</span><span class="sxs-lookup"><span data-stu-id="baff4-136">The texture offsets need to be static.</span></span> <span data-ttu-id="baff4-137">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="baff4-137">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="baff4-138">Para obter mais informações, consulte [aplicando deslocamentos de coordenadas de textura](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="baff4-138">For more info, see [Applying texture coordinate offsets](dx-graphics-hlsl-to-sample.md).</span></span>

| <span data-ttu-id="baff4-139">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="baff4-139">Texture-Object Type</span></span>            | <span data-ttu-id="baff4-140">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="baff4-140">Parameter Type</span></span> |
|--------------------------------|----------------|
| <span data-ttu-id="baff4-141">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="baff4-141">Texture1D, Texture1DArray</span></span>      | <span data-ttu-id="baff4-142">INT</span><span class="sxs-lookup"><span data-stu-id="baff4-142">int</span></span>            |
| <span data-ttu-id="baff4-143">Texture2D, Texture2DArray ¹</span><span class="sxs-lookup"><span data-stu-id="baff4-143">Texture2D, Texture2DArray¹</span></span>     | <span data-ttu-id="baff4-144">int2</span><span class="sxs-lookup"><span data-stu-id="baff4-144">int2</span></span>           |
| <span data-ttu-id="baff4-145">TextureCube, TextureCubeArray ¹</span><span class="sxs-lookup"><span data-stu-id="baff4-145">TextureCube, TextureCubeArray¹</span></span> | <span data-ttu-id="baff4-146">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="baff4-146">Not supported</span></span>  |

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="baff4-147">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="baff4-147">Return Value</span></span>

<span data-ttu-id="baff4-148">Retorna um valor de ponto flutuante no intervalo \[ 0.. 1 \] .</span><span class="sxs-lookup"><span data-stu-id="baff4-148">Returns a floating-point value in the range \[0..1\].</span></span>

<span data-ttu-id="baff4-149">Para cada Texel buscada (com base na configuração de amostra do modo de filtro), **SampleCmp** executa uma comparação do valor z (terceiro componente de entrada) do sombreador com o valor Texel (1 se a comparação for aprovada; caso contrário, 0).</span><span class="sxs-lookup"><span data-stu-id="baff4-149">For each texel fetched (based on the sampler configuration of the filter mode), **SampleCmp** performs a comparison of the z value (3rd component of input) from the shader against the texel value (1 if the comparison passes; otherwise 0).</span></span> <span data-ttu-id="baff4-150">Em seguida, **SampleCmp** mistura esses 0 e 1 resultados para cada Texel em conjunto, como na filtragem de textura normal (não uma média) e retorna o \[ valor 0.. 1 resultante \] para o sombreador.</span><span class="sxs-lookup"><span data-stu-id="baff4-150">**SampleCmp** then blends these 0 and 1 results for each texel together as in normal texture filtering (not an average) and returns the resulting \[0..1\] value to the shader.</span></span>

## <a name="remarks"></a><span data-ttu-id="baff4-151">Comentários</span><span class="sxs-lookup"><span data-stu-id="baff4-151">Remarks</span></span>

<span data-ttu-id="baff4-152">A filtragem de comparação fornece uma operação básica de filtragem que é útil para a filtragem de profundidade mais próxima do percentual.</span><span class="sxs-lookup"><span data-stu-id="baff4-152">Comparison filtering provides a basic filtering operation that is useful for percentage-closer-depth filtering.</span></span>

<span data-ttu-id="baff4-153">Ao usar esse método em um recurso de ponto flutuante (em vez de um formato assinado de forma normalizada ou não-normalizado), o valor de comparação não é automaticamente clamped entre 0,0 e 1,0.</span><span class="sxs-lookup"><span data-stu-id="baff4-153">When using this method on a floating-point resource (Instead of a signed-normalized or unsigned-normalized format), the comparison value is not automatically clamped between 0.0 and 1.0.</span></span> <span data-ttu-id="baff4-154">Portanto, um fixe manual do valor de comparação pode ser necessário para técnicas de sombreamento comuns.</span><span class="sxs-lookup"><span data-stu-id="baff4-154">Therefore, a manual clamp of the comparison value may be necessary for common shadowing techniques.</span></span>

<span data-ttu-id="baff4-155">Use um deslocamento somente em um inteiro MipLevel; caso contrário, você poderá obter resultados diferentes dependendo da implementação do hardware ou das configurações do driver.</span><span class="sxs-lookup"><span data-stu-id="baff4-155">Use an offset only at an integer miplevel; otherwise, you may get different results depending on hardware implementation or driver settings.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="baff4-156">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="baff4-156">Minimum Shader Model</span></span>

<span data-ttu-id="baff4-157">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="baff4-157">This function is supported in the following shader models.</span></span>

| <span data-ttu-id="baff4-158">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="baff4-158">vs\_4\_0</span></span> | <span data-ttu-id="baff4-159">vs \_ 4 \_ 1 ²</span><span class="sxs-lookup"><span data-stu-id="baff4-159">vs\_4\_1²</span></span> | <span data-ttu-id="baff4-160">PS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="baff4-160">ps\_4\_0</span></span> | <span data-ttu-id="baff4-161">PS \_ 4 \_ 1 ²</span><span class="sxs-lookup"><span data-stu-id="baff4-161">ps\_4\_1²</span></span> | <span data-ttu-id="baff4-162">GS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="baff4-162">gs\_4\_0</span></span> | <span data-ttu-id="baff4-163">GS \_ 4 \_ 1 ²</span><span class="sxs-lookup"><span data-stu-id="baff4-163">gs\_4\_1²</span></span> |
|----------|-----------|----------|-----------|----------|-----------|
|          |           | <span data-ttu-id="baff4-164">x ¹</span><span class="sxs-lookup"><span data-stu-id="baff4-164">x¹</span></span>       | <span data-ttu-id="baff4-165">x</span><span class="sxs-lookup"><span data-stu-id="baff4-165">x</span></span>         |          |           |

1.  <span data-ttu-id="baff4-166">Texture2DArray e TextureCubeArray estão disponíveis no modelo de sombreador 4,1 ou superior.</span><span class="sxs-lookup"><span data-stu-id="baff4-166">Texture2DArray and TextureCubeArray are available in Shader Model 4.1 or higher.</span></span>
2.  <span data-ttu-id="baff4-167">O modelo do sombreador 4,1 está disponível no Direct3D 10,1 ou superior.</span><span class="sxs-lookup"><span data-stu-id="baff4-167">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

> [!NOTE]  
> <span data-ttu-id="baff4-168">O **SampleCmp** também está disponível em PS 4 \_ 0 \_ nível \_ 9 \_ 1 e 4 \_ 0 \_ nível \_ 9 \_ 3 quando você usa as técnicas descritas em [implementando buffers de sombra para o nível de recurso do Direct3D 9](/previous-versions/windows/apps/jj262110(v=win.10)).</span><span class="sxs-lookup"><span data-stu-id="baff4-168">**SampleCmp** is also available in ps 4\_0\_level\_9\_1 and 4\_0\_level\_9\_3 when you use the techniques that are described in [Implementing shadow buffers for Direct3D feature level 9](/previous-versions/windows/apps/jj262110(v=win.10)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="baff4-169">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="baff4-169">Related topics</span></span>

[<span data-ttu-id="baff4-170">Textura-objeto</span><span class="sxs-lookup"><span data-stu-id="baff4-170">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
