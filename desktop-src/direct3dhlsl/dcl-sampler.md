---
title: dcl_sampler (sm4-ASM)
description: '\_amostra de DCL (sm4-ASM)'
ms.assetid: 285a47fa-2d47-4ba9-90b9-3f4c61d5dce1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: cb3835e1c0e2cfb5ffbb49523617b9d233810494
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122627092"
---
# <a name="dcl_sampler-sm4---asm"></a>\_amostra de DCL (sm4-ASM)

Declara um registro de amostra.



| a \_ amostra de DCL SN, modo |
|-----------------------|



 



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Item</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="sN"></span><span id="sn"></span><span id="SN"></span>s<em>N</em><br/></td>
<td>no Um registro de amostra, em que <em>N</em> é um inteiro que denota o número do registro.<br/></td>
</tr>
<tr class="even">
<td><span id="mode"></span><span id="MODE"></span><em>moda</em><br/></td>
<td>no Um modo de amostra, que restringe quais Estados de amostra (listados nos membros de <a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_sampler_desc"><strong>D3D10_SAMPLER_DESC</strong></a>) são respeitados. Os modos e os Estados são listados na tabela a seguir.<br/> 
<table>
<thead>
<tr class="header">
<th>Mode</th>
<th>Estados de amostra respeitados</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>padrão</td>
<td><em>Filter</em> (não pode usar os valores _COMPARISON ou _TEXT), <em>addressfield/V/W</em>, <em>MinLOD/MaxLOD</em>, <em>MipLODBias</em>, <em>MaxAnisotropy</em>, <em>BorderColor [4]</em></td>
</tr>
<tr class="even">
<td>comparação</td>
<td><em>Filter</em>, <em>ComparisonFunction</em>, <em>endereçou/V/W</em>, <em>MinLOD, MaxLOD</em>, <em>MipLODBias</em>, <em>MaxAnisotropy</em>, <em>BorderColor [4]</em></td>
</tr>
<tr class="odd">
<td>mixagem</td>
<td><em>Filter</em> (deve ser um dos _TEXT valores), <em>MonoFilterWidth</em>, <em>MonoFilterHeight</em> (esses dois Estados são estado global do dispositivo), <em>MinLOD</em>, <em>MipLODBias</em>, <em>MaxAnisotropy</em></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

O modo restringe as instruções de exemplo que podem ser usadas; Esta tabela lista os métodos de objeto de textura que têm suporte para cada modo.



| Um sistema operacional operando neste modo | Pode usar estes Texture-Object métodos                                                                                                           |
|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| padrão                          | [Exemplo](dx-graphics-hlsl-to-sample.md), [SampleLevel](dx-graphics-hlsl-to-samplelevel.md), [SampleGrad](dx-graphics-hlsl-to-samplegrad.md) |
| comparação                       | [SampleCmp](dx-graphics-hlsl-to-samplecmp.md), [SampleCmpLevelZero](dx-graphics-hlsl-to-samplecmplevelzero.md)                               |
| mixagem                             | [SampleLevel](dx-graphics-hlsl-to-samplelevel.md)                                                                                             |



 

Essa instrução se aplica aos seguintes estágios de sombreador:



| Sombreador de vértice | Sombreador de geometria | Sombreador de pixel |
|---------------|-----------------|--------------|
| x             | x               | w.x.y.\*          |



 

\* -O uso de uma amostra no modo mono tem suporte apenas em um sombreador de pixel.

Essa instrução está incluída para auxiliar na depuração de um sombreador no assembly; Você não pode criar um sombreador na linguagem de assembly usando o modelo de sombreador 4.

## <a name="example"></a>Exemplo

Veja um exemplo.


```
dcl_sampler s3, default
```



## <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Essa função tem suporte nos seguintes modelos de sombreador.



| Modelo de Sombreador                                              | Com suporte |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sim       |
| [Modelo do sombreador 4,1](dx-graphics-hlsl-sm4.md)              | sim       |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | sim       |
| [Modelo de sombreador 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | não        |
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | não        |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | não        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Assembly do Shader Model 4 (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

