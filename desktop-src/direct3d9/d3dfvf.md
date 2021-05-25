---
description: Constantes de formato de vértice flexíveis, ou códigos FVF, são usadas para descrever o conteúdo de vértices intercalados em um único fluxo de dados que será processado pelo pipeline de função fixa.
ms.assetid: 85d9f5b2-8e4a-4f92-a587-eae5b293778c
title: D3DFVF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a088dda530904c320720371c76601fd4fb254481
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343254"
---
# <a name="d3dfvf"></a>D3DFVF

Constantes de formato de vértice flexíveis, ou códigos FVF, são usadas para descrever o conteúdo de vértices intercalados em um único fluxo de dados que será processado pelo pipeline de função fixa.

## <a name="vertex-data-flags"></a>Sinalizadores de dados de vértice

Os sinalizadores a seguir descrevem um formato de vértice. Para obter informações sobre formatos de vértice, consulte Códigos FVF de função [fixa (Direct3D 9)](fixed-function-fvf-codes.md).



| \#Definir                            | Descrição                                                                                                                                                                                                                                                                                                                                                             | Ordem e tipo de dados                                                                                       |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| D3DFVF \_ DIFUSO                     | O formato de vértice inclui um componente de cor difusa.                                                                                                                                                                                                                                                                                                                       | DWORD na ordem ARGB. Consulte [**D3DCOLOR \_ ARGB**](d3dcolor-argb.md).                                         |
| D3DFVF \_ NORMAL                      | O formato de vértice inclui um vetor normal de vértice. Esse sinalizador não pode ser usado com o sinalizador \_ XYZRHW D3DFVF.                                                                                                                                                                                                                                                                   | float, float, float                                                                                       |
| D3DFVF \_ PSIZE                       | Formato de vértice especificado no tamanho do ponto. Esse tamanho é expresso em unidades de espaço da câmera para vértices que não são transformados e acesos e em unidades de espaço do dispositivo para vértices transformados e acesos.                                                                                                                                                                          | FLOAT                                                                                                     |
| \_Especular D3DFVF                    | O formato de vértice inclui um componente de cor especular.                                                                                                                                                                                                                                                                                                                      | DWORD na ordem ARGB. Consulte [**D3DCOLOR \_ ARGB**](d3dcolor-argb.md).                                         |
| D3DFVF \_ XYZ                         | O formato de vértice inclui a posição de um vértice não transformado. Esse sinalizador não pode ser usado com o \_ sinalizador D3DFVF XYZRHW.                                                                                                                                                                                                                                                  | float, float, float.                                                                                      |
| D3DFVF \_ XYZRHW                      | O formato de vértice inclui a posição de um vértice transformado. Esse sinalizador não pode ser usado com os \_ sinalizadores normais D3DFVF XYZ ou D3DFVF \_ .                                                                                                                                                                                                                                     | float, float, float, float.                                                                               |
| D3DFVF \_ XYZB1 D3DFVF \_ XYZB5 | O formato de vértice contém dados de posição e um número correspondente de valores de peso (beta) a serem usados para operações de mesclagem de vértice de várias matrizes. Atualmente, o Direct3D pode misturar com até três valores de peso e quatro matrizes de mesclagem. Para obter mais informações sobre o uso de matrizes de mesclagem, consulte [Direct3D 9 (índice de vértices indexados)](indexed-vertex-blending.md). | 1, 2 ou 3 floats. Quando D3DFVF \_ LASTBETA \_ UBYTE4 é usado, o último peso de mesclagem é tratado como um DWORD. |
| D3DFVF \_ XYZW                        | O formato de vértice contém dados transformados e recortados (x, y, z, w). ProcessVertices não invoca o clipper, em vez disso, a saída de dados em coordenadas de clipe. Essa constante foi projetada para e só pode ser usada com o pipeline de vértice programável.                                                                                                                 | float, float, float, float                                                                                |



 

## <a name="texture-flags"></a>Sinalizadores de textura

Os sinalizadores a seguir descrevem sinalizadores de textura usados pelo pipeline de função fixa.



| \#Definir                          | Descrição                                                                                                                                                                                                                                                                        |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DFVF \_ TEX0 – D3DFVF \_ TEXAS8       | Número de conjuntos de coordenadas de textura para esse vértice. Os valores reais para esses sinalizadores não são sequenciais.                                                                                                                                                                           |
| D3DFVF \_ TEXCOORDSIZEN(coordIndex) | Defina um conjunto de dados de coordenadas de textura. n indica a dimensão das coordenadas de textura. coordIndex indica o número do índice da coordenada de textura. Consulte [**D3DFVF \_ TEXCOORDSIZEN**](d3dfvf-texcoordsizen.md) e Coordenadas de textura [e Estágios de textura](texture-coordinates.md). |



 

## <a name="mask-flags"></a>Sinalizadores de máscara

Os sinalizadores a seguir descrevem sinalizadores de máscara usados pelo pipeline de função fixa.



| \#Definir                             | Descrição                                           |
|--------------------------------------|-------------------------------------------------------|
| MÁSCARA DE POSIÇÃO D3DFVF \_ \_               | Máscara para bits de posição.                               |
| D3DFVF \_ RESERVED0, D3DFVF \_ RESERVED2 | Mascarar valores para bits reservados no FVF. Não use. |
| \_Máscara de TEXCOUNT D3DFVF \_               | Valor de máscara para bits de sinalizador de textura.                     |



 

## <a name="miscellaneous-flags"></a>Sinalizadores diversos

Os sinalizadores a seguir descrevem uma variedade de sinalizadores usados pelo pipeline de função fixa.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>#definir</td>
<td>Descrição</td>
</tr>
<tr class="even">
<td>D3DFVF_LASTBETA_D3DCOLOR</td>
<td>O último campo beta nos dados da posição do vértice será do tipo D3DCOLOR. Os dados nos campos beta são usados com a aparência da paleta de matriz para especificar índices de matriz.</td>
</tr>
<tr class="odd">
<td>D3DFVF_LASTBETA_UBYTE4</td>
<td>O último campo beta nos dados da posição do vértice será do tipo UBYTE4. Os dados nos campos beta são usados com a aparência da paleta de matriz para especificar índices de matriz. <span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>// Given the following vertex data definition: 
struct VERTEXPOSITION
{
   float pos[3];
   union 
   {
      float beta[5];
      struct
      {
         float weights[4];
         DWORD MatrixIndices;  // Used as UBYTEs
      }
   }
};</code></pre></td>
</tr>
</tbody>
</table>

<p>Dado que o FVF é declarado como: D3DFVF_XYZB5 | D3DFVF_LASTBETA_UBYTE4. Peso e MatrixIndices são incluídos na versão beta [5], em que D3DFVF_LASTBETA_UBYTE4 diz para interpretar a última DWORD em beta [5] como tipo UBYTE4.</p></td>
</tr>
<tr class="even">
<td>D3DFVF_TEXCOUNT_SHIFT</td>
<td>O número de bits pelo qual mover um valor inteiro que identifica o número de coordenadas de textura de um vértice. Esse valor pode ser usado conforme mostrado abaixo.
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>DWORD dwNumTextures = 1;  // Vertex has only one set of coordinates.

// Shift the value for use when creating a 
//   flexible vertex format (FVF) combination.
dwFVF = dwNumTextures << D3DFVF_TEXCOUNT_SHIFT;

// Now, create an FVF combination using the shifted value.</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

### <a name="examples"></a>Exemplos

Os exemplos a seguir mostram outras combinações de sinalizador comuns.


```
// Untransformed vertex for lit, untextured, Gouraud-shaded content.
dwFVF = ( D3DFVF_XYZ | D3DFVF_DIFFUSE );
```




```
// Untransformed vertex for unlit, untextured, Gouraud-shaded 
//   content with diffuse material color specified per vertex.
dwFVF = ( D3DFVF_XYZ | D3DFVF_NORMAL | D3DFVF_DIFFUSE );
```




```
// Untransformed vertex for light-map-based lighting.
dwFVF = ( D3DFVF_XYZ | D3DFVF_TEX2 );
```




```
// Transformed vertex for light-map-based lighting with shared rhw.
dwFVF = ( D3DFVF_XYZRHW | D3DFVF_TEX2 );
```




```
// Heavyweight vertex for unlit, colored content with two 
//   sets of texture coordinates.
dwFVF = ( D3DFVF_XYZ | D3DFVF_NORMAL | D3DFVF_DIFFUSE | 
          D3DFVF_SPECULAR | D3DFVF_TEX2 );
```



## <a name="constant-information"></a>Informações constantes



| Requisito                         | Valor            |
|--------------------------|-------------|
| parâmetro                   | d3d9types. h |
| Sistema operacional mínimo | Windows 98  |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Constantes Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[Códigos FVF de função fixa (Direct3D 9)](fixed-function-fvf-codes.md)
</dt> <dt>

[Geometry Blending (Direct3D 9)](geometry-blending.md)
</dt> </dl>

 

 



