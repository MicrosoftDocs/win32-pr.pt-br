---
title: dcl_sampler (sm4 – asm)
description: dcl \_ sampler (sm4 - asm)
ms.assetid: 285a47fa-2d47-4ba9-90b9-3f4c61d5dce1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 86e0e04558c9ca1c10f89e924605c8999a7f7346d2278850d7cd6449968fd13c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118515535"
---
# <a name="dcl_sampler-sm4---asm"></a>dcl \_ sampler (sm4 - asm)

Declara um registro de amostra.



| dcl \_ sampler sN, mode |
|-----------------------|



 



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
<td><span id="sN"></span><span id="sn"></span><span id="SN"></span>s<em>N</em><br/></td>
<td>[in] Um registro de amostra, em <em>que N</em> é um inteiro que indica o número do registro.<br/></td>
</tr>
<tr class="even">
<td><span id="mode"></span><span id="MODE"></span><em>Modo</em><br/></td>
<td>[in] Um modo de amostra, que restringe quais estados de amostra (listados nos membros <a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_sampler_desc"><strong>do D3D10_SAMPLER_DESC</strong></a>) são honorados. Os modos e os estados são listados na tabela a seguir.<br/> 
<table>
<thead>
<tr class="header">
<th>Mode</th>
<th>Estados de amostras honorados</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>padrão</td>
<td><em>Filtro</em> (não pode usar os valores _COMPARISON ou _TEXT), <em>AddressU/V/W,</em> <em>MinLOD/MaxLOD,</em> <em>MipLODBias,</em> <em>Max Ltda,</em> <em>BorderColor[4]</em></td>
</tr>
<tr class="even">
<td>comparação</td>
<td><em>Filter</em>, <em>ComparisonFunction</em>, <em>AddressU/V/W</em>, <em>MinLOD,MaxLOD,</em> <em>MipLODBias</em>, <em>MaxAnisoosay</em>, <em>BorderColor[4]</em></td>
</tr>
<tr class="odd">
<td>Mono</td>
<td><em>Filtro</em> (deve ser um dos valores _TEXT), <em>MonoFilterWidth,</em> <em>MonoFilterHeight</em> (esses dois estados são o estado do dispositivo global), <em>MinLOD</em>, <em>MipLODBias,</em> <em>Max Ltda</em></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

O modo restringe as instruções de exemplo que podem ser usadas; esta tabela lista os métodos de objeto de textura com suporte para cada modo.



| Um sampler operando nesse modo | Pode usar esses métodos Texture-Object dados                                                                                                           |
|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| padrão                          | [Sample](dx-graphics-hlsl-to-sample.md), [SampleLevel](dx-graphics-hlsl-to-samplelevel.md), [SampleGrad](dx-graphics-hlsl-to-samplegrad.md) |
| comparação                       | [SampleCmp](dx-graphics-hlsl-to-samplecmp.md), [SampleCmpLevelZero](dx-graphics-hlsl-to-samplecmplevelzero.md)                               |
| Mono                             | [SampleLevel](dx-graphics-hlsl-to-samplelevel.md)                                                                                             |



 

Essa instrução se aplica aos seguintes estágios do sombreador:



| Sombreador de vértice | Sombreador de geometria | Sombreador de pixel |
|---------------|-----------------|--------------|
| x             | x               | X\*          |



 

\* - O uso de um sampler no modo mono só tem suporte em um sombreador de pixel.

Essa instrução é incluída para auxiliar na depuração de um sombreador no assembly; não é possível autor de um sombreador na linguagem de assembly usando o Modelo de Sombreador 4.

## <a name="example"></a>Exemplo

Veja um exemplo.


```
dcl_sampler s3, default
```



## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Essa função tem suporte nos modelos de sombreador a seguir.



| Modelo de Sombreador                                              | Com suporte |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sim       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | sim       |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | sim       |
| [Modelo de sombreador 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | não        |
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | não        |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | não        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Assembly do modelo de sombreador 4 (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

