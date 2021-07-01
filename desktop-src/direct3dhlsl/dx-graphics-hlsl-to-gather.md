---
title: Coletar (objeto de textura DirectX HLSL)
description: Obtém as quatro amostras (somente componente vermelho) que seriam usadas para interpolação bilinear ao fazer amostragem de uma textura.
ms.assetid: a394d8c2-99cc-4a38-9ac9-34afc666ebe0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4659ba19e9fa950a659969f2491533858f4658fb
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120541"
---
# <a name="gather-directx-hlsl-texture-object"></a><span data-ttu-id="bf7b2-103">Coletar (objeto de textura DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bf7b2-103">Gather (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="bf7b2-104">Obtém as quatro amostras (somente componente vermelho) que seriam usadas para interpolação bilinear ao fazer amostragem de uma textura.</span><span class="sxs-lookup"><span data-stu-id="bf7b2-104">Gets the four samples (red component only) that would be used for bilinear interpolation when sampling a texture.</span></span>

<span data-ttu-id="bf7b2-105">&lt;Modelo &gt; do tipo 4 objeto. coletar ( \_ estado de amostra S, float2 \| 3 \| 4 local \[ , deslocamento de Int2 \] );</span><span class="sxs-lookup"><span data-stu-id="bf7b2-105">&lt;Template Type&gt;4 Object.Gather( sampler\_state S, float2\|3\|4 Location \[, int2 Offset\] );</span></span>



 

## <a name="parameters"></a><span data-ttu-id="bf7b2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bf7b2-106">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bf7b2-107">Item</span><span class="sxs-lookup"><span data-stu-id="bf7b2-107">Item</span></span></th>
<th><span data-ttu-id="bf7b2-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="bf7b2-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bf7b2-109"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Objeto</em></span><span class="sxs-lookup"><span data-stu-id="bf7b2-109"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Object</em></span></span><br/></td>
<td><span data-ttu-id="bf7b2-110">Há suporte para os seguintes tipos de <a href="dx-graphics-hlsl-to-type.md">objeto de textura</a> : Texture2D, Texture2DArray, TextureCube, TextureCubeArray.</span><span class="sxs-lookup"><span data-stu-id="bf7b2-110">The following <a href="dx-graphics-hlsl-to-type.md">texture-object</a> types are supported: Texture2D, Texture2DArray, TextureCube, TextureCubeArray.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bf7b2-111"><span id="S"></span><span id="s"></span><em>&</em></span><span class="sxs-lookup"><span data-stu-id="bf7b2-111"><span id="S"></span><span id="s"></span><em>S</em></span></span><br/></td>
<td><span data-ttu-id="bf7b2-112">no Um <a href="dx-graphics-hlsl-sampler.md">estado de amostra</a>.</span><span class="sxs-lookup"><span data-stu-id="bf7b2-112">[in] A <a href="dx-graphics-hlsl-sampler.md">Sampler state</a>.</span></span> <span data-ttu-id="bf7b2-113">Este é um objeto declarado em um arquivo de efeito que contém atribuições de estado.</span><span class="sxs-lookup"><span data-stu-id="bf7b2-113">This is an object declared in an effect file that contains state assignments.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bf7b2-114"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Local</em></span><span class="sxs-lookup"><span data-stu-id="bf7b2-114"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Location</em></span></span><br/></td>
<td><span data-ttu-id="bf7b2-115">no As coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="bf7b2-115">[in] The texture coordinates.</span></span> <span data-ttu-id="bf7b2-116">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="bf7b2-116">The argument type is dependent on the texture-object type.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="bf7b2-117">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="bf7b2-117">Texture-Object Type</span></span></th>
<th><span data-ttu-id="bf7b2-118">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="bf7b2-118">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bf7b2-119">Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf7b2-119">Texture2D</span></span></td>
<td><span data-ttu-id="bf7b2-120">float2</span><span class="sxs-lookup"><span data-stu-id="bf7b2-120">float2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bf7b2-121">Texture2DArray, TextureCube</span><span class="sxs-lookup"><span data-stu-id="bf7b2-121">Texture2DArray, TextureCube</span></span></td>
<td><span data-ttu-id="bf7b2-122">float3</span><span class="sxs-lookup"><span data-stu-id="bf7b2-122">float3</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bf7b2-123">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="bf7b2-123">TextureCubeArray</span></span> </td>
<td><span data-ttu-id="bf7b2-124">float4</span><span class="sxs-lookup"><span data-stu-id="bf7b2-124">float4</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf7b2-125"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Desvio</em></span><span class="sxs-lookup"><span data-stu-id="bf7b2-125"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Offset</em></span></span></p></td>
<td><p><span data-ttu-id="bf7b2-126">no Um deslocamento de coordenadas de textura opcional, que pode ser usado para qualquer tipo de objeto de textura; o deslocamento é aplicado ao local antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="bf7b2-126">[in] An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="bf7b2-127">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="bf7b2-127">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="bf7b2-128">Para sombreadores que visam o modelo de sombreador 5,0 e acima, os 6 bits menos significativos de cada valor de deslocamento são respeitados como um valor assinado, produzindo [-32.. 31] intervalo.</span><span class="sxs-lookup"><span data-stu-id="bf7b2-128">For shaders targeting Shader Model 5.0 and above, the 6 least significant bits of each offset value is honored as a signed value, yielding [-32..31] range.</span></span> <span data-ttu-id="bf7b2-129">Para os sombreadores do modelo do sombreador anterior, os deslocamentos precisam ser inteiros imediatos entre-8 e 7.</span><span class="sxs-lookup"><span data-stu-id="bf7b2-129">For previous shader model shaders, offsets need to be immediate integers between -8 and 7.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="bf7b2-130">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="bf7b2-130">Texture-Object Type</span></span></th>
<th><span data-ttu-id="bf7b2-131">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="bf7b2-131">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bf7b2-132">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="bf7b2-132">Texture2D, Texture2DArray</span></span></td>
<td><span data-ttu-id="bf7b2-133">int2</span><span class="sxs-lookup"><span data-stu-id="bf7b2-133">int2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bf7b2-134">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="bf7b2-134">TextureCube, TextureCubeArray</span></span> </td>
<td><span data-ttu-id="bf7b2-135">sem suporte</span><span class="sxs-lookup"><span data-stu-id="bf7b2-135">not supported</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="return-value"></a><span data-ttu-id="bf7b2-136">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="bf7b2-136">Return Value</span></span>

<span data-ttu-id="bf7b2-137">Um vetor de quatro componentes, com quatro componentes de dados vermelhos, cujo tipo é o mesmo que o tipo de modelo da textura.</span><span class="sxs-lookup"><span data-stu-id="bf7b2-137">A four-component vector, with four components of red data, whose type is the same as the texture's template type.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="bf7b2-138">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="bf7b2-138">Minimum Shader Model</span></span>

<span data-ttu-id="bf7b2-139">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="bf7b2-139">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="bf7b2-140">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="bf7b2-140">vs\_4\_0</span></span> | <span data-ttu-id="bf7b2-141">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="bf7b2-141">vs\_4\_1</span></span>  | <span data-ttu-id="bf7b2-142">PS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="bf7b2-142">ps\_4\_0</span></span> | <span data-ttu-id="bf7b2-143">PS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="bf7b2-143">ps\_4\_1</span></span>  | <span data-ttu-id="bf7b2-144">GS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="bf7b2-144">gs\_4\_0</span></span> | <span data-ttu-id="bf7b2-145">GS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="bf7b2-145">gs\_4\_1</span></span>  |
|----------|-----------|----------|-----------|----------|-----------|
|          | <span data-ttu-id="bf7b2-146">x</span><span class="sxs-lookup"><span data-stu-id="bf7b2-146">x</span></span>         |          | <span data-ttu-id="bf7b2-147">x</span><span class="sxs-lookup"><span data-stu-id="bf7b2-147">x</span></span>         |          | <span data-ttu-id="bf7b2-148">x</span><span class="sxs-lookup"><span data-stu-id="bf7b2-148">x</span></span>         |



 

1.  <span data-ttu-id="bf7b2-149">O TextureCubeArray está disponível no modelo de sombreador 4,1 ou superior.</span><span class="sxs-lookup"><span data-stu-id="bf7b2-149">TextureCubeArray is available in Shader Model 4.1 or higher.</span></span>
2.  <span data-ttu-id="bf7b2-150">O modelo do sombreador 4,1 está disponível no Direct3D 10,1 ou superior.</span><span class="sxs-lookup"><span data-stu-id="bf7b2-150">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="example"></a><span data-ttu-id="bf7b2-151">Exemplo</span><span class="sxs-lookup"><span data-stu-id="bf7b2-151">Example</span></span>


```
Texture2D<int1> Tex2d;
Texture2DArray<int2> Tex2dArray;
TextureCube<int3> TexCube;
TextureCubeArray<float2> TexCubeArray;

SamplerState s;

int4 main (float4 f : SV_Position) : SV_Target
{
    int2 iOffset = int2(2,3);

    int4 i1 = Tex2d.Gather(s, f.xy);
    int4 i2 = Tex2d.Gather(s, f.xy, iOffset);

    int4 i3 = Tex2dArray.Gather(s, f.xyz);
    int4 i4 = Tex2dArray.Gather(s, f.xyz, iOffset);

    int4 i5 = TexCube.Gather(s, f.xyzw);

    float4 f6 = TexCubeArray.Gather(s, f.xyzw);

    return i1+i2+i3+i4+i5+int4(i6);
}
  
```



## <a name="related-topics"></a><span data-ttu-id="bf7b2-152">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bf7b2-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf7b2-153">Textura-objeto</span><span class="sxs-lookup"><span data-stu-id="bf7b2-153">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 





