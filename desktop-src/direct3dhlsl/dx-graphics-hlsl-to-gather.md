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
ms.openlocfilehash: f333c204b77d6e0c64119e16f31e170fec1d0f6c
ms.sourcegitcommit: 07ba02719c9779e082b108ae74f9699fb0236c34
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/06/2021
ms.locfileid: "108644098"
---
# <a name="gather-directx-hlsl-texture-object"></a>Coletar (objeto de textura DirectX HLSL)

Obtém as quatro amostras (somente componente vermelho) que seriam usadas para interpolação bilinear ao fazer amostragem de uma textura.



|                                                                                                    |
|----------------------------------------------------------------------------------------------------|
| &lt;Modelo &gt; do tipo 4 objeto. coletar ( \_ estado de amostra S, float2 \| 3 \| 4 local \[ , deslocamento de Int2 \] ); |



 

## <a name="parameters"></a>Parâmetros



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Item</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Objeto</em><br/></td>
<td>Há suporte para os seguintes tipos de <a href="dx-graphics-hlsl-to-type.md">objeto de textura</a> : Texture2D, Texture2DArray, TextureCube, TextureCubeArray.<br/></td>
</tr>
<tr class="even">
<td><span id="S"></span><span id="s"></span><em>&</em><br/></td>
<td>no Um <a href="dx-graphics-hlsl-sampler.md">estado de amostra</a>. Este é um objeto declarado em um arquivo de efeito que contém atribuições de estado.<br/></td>
</tr>
<tr class="odd">
<td><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Local</em><br/></td>
<td>no As coordenadas de textura. O tipo de argumento é dependente do tipo de objeto Texture. <br/> 
<table>
<thead>
<tr class="header">
<th>Tipo de Texture-Object</th>
<th>Tipo de parâmetro</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Texture2D</td>
<td>float2</td>
</tr>
<tr class="even">
<td>Texture2DArray, TextureCube</td>
<td>float3</td>
</tr>
<tr class="odd">
<td>TextureCubeArray </td>
<td>float4</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Desvio</em></p></td>
<td><p>no Um deslocamento de coordenadas de textura opcional, que pode ser usado para qualquer tipo de objeto de textura; o deslocamento é aplicado ao local antes da amostragem. O tipo de argumento é dependente do tipo de objeto Texture. Para sombreadores que visam o modelo de sombreador 5,0 e acima, os 6 bits menos significativos de cada valor de deslocamento são respeitados como um valor assinado, produzindo [-32.. 31] intervalo. Para os sombreadores do modelo do sombreador anterior, os deslocamentos precisam ser inteiros imediatos entre-8 e 7.</p>

<table>
<thead>
<tr class="header">
<th>Tipo de Texture-Object</th>
<th>Tipo de parâmetro</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Texture2D, Texture2DArray</td>
<td>int2</td>
</tr>
<tr class="even">
<td>TextureCube, TextureCubeArray </td>
<td>sem suporte</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="return-value"></a>Valor retornado

Um vetor de quatro componentes, com quatro componentes de dados vermelhos, cujo tipo é o mesmo que o tipo de modelo da textura.

## <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Essa função tem suporte nos seguintes modelos de sombreador.



| vs \_ 4 \_ 0 | vs \_ 4 \_ 1  | PS \_ 4 \_ 0 | PS \_ 4 \_ 1  | GS \_ 4 \_ 0 | GS \_ 4 \_ 1  |
|----------|-----------|----------|-----------|----------|-----------|
|          | x         |          | x         |          | x         |



 

1.  O TextureCubeArray está disponível no modelo de sombreador 4,1 ou superior.
2.  O modelo do sombreador 4,1 está disponível no Direct3D 10,1 ou superior.

## <a name="example"></a>Exemplo


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Textura-objeto](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 





