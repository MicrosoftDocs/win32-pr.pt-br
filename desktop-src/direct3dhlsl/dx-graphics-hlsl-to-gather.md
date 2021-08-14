---
title: Gather (objeto de textura HLSL do DirectX)
description: Obtém os quatro exemplos (somente componente vermelho) que seriam usados para interpolação bilinear ao amostragem de uma textura.
ms.assetid: a394d8c2-99cc-4a38-9ac9-34afc666ebe0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5edf92b127210a5eb05e5339a1dff4cc08ce9443e638461b71d7bf7d27c7b78a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118513085"
---
# <a name="gather-directx-hlsl-texture-object"></a>Gather (objeto de textura HLSL do DirectX)

Obtém os quatro exemplos (somente componente vermelho) que seriam usados para interpolação bilinear ao amostragem de uma textura.

&lt;Template Type &gt; 4 Object.Gather( sampler \_ state S, float2 \| 3 \| 4 Location \[ , int2 Offset \] );



 

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
<td>Há suporte <a href="dx-graphics-hlsl-to-type.md">para os seguintes tipos de</a> objeto de textura: Texture2D, Texture2DArray, TextureCube, TextureCubeArray.<br/></td>
</tr>
<tr class="even">
<td><span id="S"></span><span id="s"></span><em>S</em><br/></td>
<td>[in] Um <a href="dx-graphics-hlsl-sampler.md">estado sampler</a>. Esse é um objeto declarado em um arquivo de efeito que contém atribuições de estado.<br/></td>
</tr>
<tr class="odd">
<td><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Localização</em><br/></td>
<td>[in] As coordenadas de textura. O tipo de argumento depende do tipo de objeto de textura. <br/> 
<table>
<thead>
<tr class="header">
<th>Texture-Object tipo</th>
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
<td><p><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Deslocamento</em></p></td>
<td><p>[in] Um deslocamento de coordenada de textura opcional, que pode ser usado para qualquer tipo de objeto de textura; o deslocamento é aplicado ao local antes da amostragem. O tipo de argumento depende do tipo de objeto de textura. Para sombreadores destinados ao Modelo de Sombreador 5.0 e superior, os 6 bits menos significativos de cada valor de deslocamento são honorados como um valor assinado, visando o intervalo [-32,.31]. Para sombreadores de modelo de sombreador anteriores, deslocamentos precisam ser inteiros imediatos entre -8 e 7.</p>

<table>
<thead>
<tr class="header">
<th>Texture-Object tipo</th>
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



 

## <a name="return-value"></a>Valor Retornado

Um vetor de quatro componentes, com quatro componentes de dados vermelhos, cujo tipo é o mesmo que o tipo de modelo da textura.

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Essa função tem suporte nos modelos de sombreador a seguir.



| vs \_ 4 \_ 0 | vs \_ 4 \_ 1  | ps \_ 4 \_ 0 | ps \_ 4 \_ 1  | gs \_ 4 \_ 0 | gs \_ 4 \_ 1  |
|----------|-----------|----------|-----------|----------|-----------|
|          | x         |          | x         |          | x         |



 

1.  TextureCubeArray está disponível no Modelo de Sombreador 4.1 ou superior.
2.  O Modelo de Sombreador 4.1 está disponível no Direct3D 10.1 ou superior.

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

[Objeto de textura](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 





