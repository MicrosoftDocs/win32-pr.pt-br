---
title: SampleLevel (objeto de textura HLSL do DirectX)
description: Amostra uma textura usando um deslocamento no nível de mipmap.
ms.assetid: d61426c8-e09f-4e88-99f6-fa96c4a2b58d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bc3a074641ce5b15a3d837e8bd91dfdae09fe627
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826680"
---
# <a name="samplelevel-directx-hlsl-texture-object"></a>SampleLevel (objeto de textura HLSL do DirectX)

Amostra uma textura usando um deslocamento no nível de mipmap.

&lt;Template Type &gt; Object.SampleLevel( sampler \_ state S, float Location, float LOD \[ , int Offset \] );



 

Essa função é semelhante a [Sample,](dx-graphics-hlsl-to-sample.md) exceto que ela usa o nível LOD (no último componente do parâmetro location) para escolher o nível mipmap. Por exemplo, uma textura 2D usa os dois primeiros componentes para coordenadas uv e o terceiro componente para o nível mipmap.

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
<td>Qualquer <a href="dx-graphics-hlsl-to-type.md">tipo de objeto de</a> textura (exceto Texture2DMS e Texture2DMSArray).<br/></td>
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
<td>Texture1D</td>
<td>FLOAT</td>
</tr>
<tr class="even">
<td>Texture1DArray, Texture2D</td>
<td>float2</td>
</tr>
<tr class="odd">
<td>Texture2DArray, Texture3D, TextureCube</td>
<td>float3</td>
</tr>
<tr class="even">
<td>TextureCubeArray </td>
<td>float4</td>
</tr>
</tbody>
</table>

<p> </p>
<p>Se o objeto de textura for uma matriz, o último componente será o índice da matriz.</p></td>
</tr>
<tr class="even">
<td><p><span id="LOD"></span><span id="lod"></span><em>Lod</em></p></td>
<td><p>[in] Um número que especifica o nível de mipmap. Se o valor for = 0, o zero (maior mapa) será usado. O valor fracionado (se fornecido) é usado para interpolar entre dois níveis de mipmap.</p></td>
</tr>
<tr class="odd">
<td><p><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Deslocamento</em></p></td>
<td><p>[in] Um deslocamento de coordenada de textura opcional, que pode ser usado para qualquer tipo de objeto de textura; o deslocamento é aplicado ao local antes da amostragem. Os deslocamentos de textura precisam ser estáticos. O tipo de argumento depende do tipo de objeto de textura. Para obter mais informações, consulte <a href="/windows/win32/direct3dhlsl/dx-graphics-hlsl-to-sample#applying-texture-coordinate-offsets">Aplicando deslocamentos de coordenadas de textura.</a></p>

<table>
<thead>
<tr class="header">
<th>Texture-Object tipo</th>
<th>Tipo de parâmetro</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Texture1D, Texture1DArray</td>
<td>INT</td>
</tr>
<tr class="even">
<td>Texture2D, Texture2DArray</td>
<td>int2</td>
</tr>
<tr class="odd">
<td>Texture3D</td>
<td>int3</td>
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

O tipo de modelo da textura, que pode ser um vetor de um ou vários componentes. O formato é baseado no formato [**DXGI \_ da textura.**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Essa função tem suporte nos modelos de sombreador a seguir.



| vs \_ 4 \_ 0 | vs \_ 4 \_ 1  | ps \_ 4 \_ 0 | ps \_ 4 \_ 1  | gs \_ 4 \_ 0 | gs \_ 4 \_ 1  |
|----------|-----------|----------|-----------|----------|-----------|
| x        | x         | x        | x         | x        | x         |



 

1.  TextureCubeArray está disponível no Modelo de Sombreador 4.1 ou superior.
2.  O Modelo de Sombreador 4.1 está disponível no Direct3D 10.1 ou superior.

## <a name="example"></a>Exemplo

Este exemplo de código parcial é do arquivo Instancing.fx no [Exemplo instancing10](https://msdn.microsoft.com/library/Ee416415(v=VS.85).aspx).


```
// Object Declarations
Texture1D g_txRandom;

SamplerState g_samPoint
{
    Filter = MIN_MAG_MIP_POINT;
    AddressU = Wrap;
    AddressV = Wrap;
};

    
// Shader body calling the intrinsic function
float3 RandomDir(float fOffset)
{   
    float tCoord = (fOffset) / 300.0;
    return g_txRandom.SampleLevel( g_samPoint, tCoord, 0 );
   ...

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Objeto de textura](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

