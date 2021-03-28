---
title: Objeto de textura
description: No Direct3D 10, você especifica os exemplos e as texturas de forma independente; a amostragem de textura é implementada usando um objeto de textura de modelo. Este objeto de textura de modelo tem um formato específico, retorna um tipo específico e implementa vários métodos.
ms.assetid: e8cb483a-d831-4942-b6fe-61dd5edb1813
keywords:
- Objeto de textura HLSL
topic_type:
- apiref
api_name:
- Texture Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b075ddc1f659923efd03d9fe9d21ee3238e656e9
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/10/2021
ms.locfileid: "104172899"
---
# <a name="texture-object"></a>Objeto de textura

No Direct3D 10, você especifica os exemplos e as texturas de forma independente; a amostragem de textura é implementada usando um objeto de textura de modelo. Este objeto de textura de modelo tem um formato específico, retorna um tipo específico e implementa vários métodos.




|                                                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Diferenças entre o Direct3D9 e o Direct3D10: no Direct3D 9, os exemplos são associados a texturas específicas; no Direct3D 10, as texturas e os exemplos são objetos independentes. Cada objeto modelo-Texture implementa métodos de amostragem de textura que usam a textura e a amostra como parâmetros de entrada.<br/> |



 

Aqui está a sintaxe para criar todos os objetos de textura (exceto objetos com uma amostra).



| Nome do \[ < *tipo* de Object1 > \] ; |
|------------------------------------|



 

Os objetos com várias amostras (Texture2DMS e Texture2DMSArray) exigem que o tamanho da textura seja explicitamente declarado e expresso como o número de amostras.



| \[ < *Tipo de Object2, nome de amostra* > \] ; |
|---------------------------------------------|



 

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
<td>Um objeto de textura. Deve ser um dos tipos a seguir. <br/> 
<table>
<thead>
<tr class="header">
<th>Tipo de Object1</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Buffer</td>
<td>Buffer </td>
</tr>
<tr class="even">
<td>Texture1D</td>
<td>textura 1D</td>
</tr>
<tr class="odd">
<td>Texture1DArray</td>
<td>Matriz de texturas 1D</td>
</tr>
<tr class="even">
<td>Texture2D</td>
<td>textura 2D</td>
</tr>
<tr class="odd">
<td>Texture2DArray</td>
<td>Matriz de texturas 2D</td>
</tr>
<tr class="even">
<td>Texture3D</td>
<td>textura 3D</td>
</tr>
<tr class="odd">
<td>TextureCube</td>
<td>Textura do cubo</td>
</tr>
<tr class="even">
<td>TextureCubeArray  </td>
<td>Matriz de texturas de cubo</td>
</tr>
<tr class="odd">
<td>Tipo de Object2</td>
<td>Description</td>
</tr>
<tr class="even">
<td>Texture2DMS</td>
<td>textura de multiamostras 2D</td>
</tr>
<tr class="odd">
<td>Texture2DMSArray</td>
<td>Matriz de texturas com multiamostragens 2D</td>
</tr>
</tbody>
</table>

<p> </p>
<ol>
<li>O tipo de buffer oferece suporte à maioria dos métodos de objeto de textura, exceto GetDimensions.</li>
<li>O TextureCubeArray está disponível no modelo de sombreador 4,1 ou superior.</li>
<li>O modelo do sombreador 4,1 está disponível no Direct3D 10,1 ou superior.</li>
</ol></td>
</tr>
<tr class="even">
<td><p><span id="Type"></span><span id="type"></span><span id="TYPE"></span><em>Escreva</em></p></td>
<td><p>Opcional. Qualquer tipo de <a href="dx-graphics-hlsl-scalar.md">HLSL escalar</a> ou <a href="dx-graphics-hlsl-vector.md"><strong>tipo de HLSL de vetor</strong></a>, entre colchetes angulares. O tipo padrão é <strong>FLOAT4</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><span id="Name"></span><span id="name"></span><span id="NAME"></span><em>Nomes</em></p></td>
<td><p>Uma cadeia de caracteres ASCII que especifica o nome do objeto de textura.</p></td>
</tr>
<tr class="even">
<td><p><span id="Samples"></span><span id="samples"></span><span id="SAMPLES"></span><em>Amostras</em></p></td>
<td><p>O número de amostras (intervalos entre 1 e 128).</p></td>
</tr>
</tbody>
</table>



 

## <a name="example-1"></a>Exemplo 1

Aqui está um exemplo de declaração de um objeto de textura.


```
Texture2D <float4> MyTex;

Texture2DMS <float4, 128> MyMSTex;
```



## <a name="texture-object-methods"></a>Métodos de objeto de textura

Cada objeto de textura implementa determinados métodos; Aqui está a tabela que lista todos os métodos. Consulte a página de referência para cada método para ver quais objetos podem usar esse método.



| Método de textura                                                                     | Description                                                                                                       | vs \_ 4 \_ 0 | vs \_ 4 \_ 1  | PS \_ 4 \_ 0 | PS \_ 4 \_ 1  | GS \_ 4 \_ 0 | GS \_ 4 \_ 1  |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|----------|-----------|----------|-----------|----------|-----------|
| [CalculateLevelOfDetail](dx-graphics-hlsl-to-calculate-lod.md)                    | Calcule o LOD, retorne um resultado de clamped.                                                                       |          |           |          | x         |          |           |
| [CalculateLevelOfDetailUnclamped](dx-graphics-hlsl-to-calculate-lod-unclamped.md) | Calcule o LOD, retorne um resultado de unclamped.                                                                    |          |           |          | x         |          |           |
| [Gather](dx-graphics-hlsl-to-gather.md)                                           | Obtém as quatro amostras (somente componente vermelho) que seriam usadas para interpolação bilinear ao fazer amostragem de uma textura. |          | x         |          | x         |          | x         |
| [GetDimensions](dx-graphics-hlsl-to-getdimensions.md)                             | Obter a dimensão de textura para um nível de mipmap especificado.                                                           | x        | x         | x        | x         | x        | x         |
| [GetDimensions (multiamostra)](dx-graphics-hlsl-to-getdimensions.md)               | Obter a dimensão de textura para um nível de mipmap especificado.                                                           |          | x         |          | x         |          | x         |
| [GetSamplePosition](dx-graphics-hlsl-to-get-sample-position.md)                   | Obtém a posição do exemplo especificado.                                                                         |          | x         |          | x         |          | x         |
| [Carregar](dx-graphics-hlsl-to-load.md)                                               | Carregar dados sem nenhuma filtragem ou amostragem.                                                                      | x        | x         | x        | x         | x        | x         |
| [Carregar (multiamostrar)](dx-graphics-hlsl-to-load.md)                                 | Carregar dados sem nenhuma filtragem ou amostragem.                                                                      |          | x         | x        | x         |          | x         |
| [Amostra](dx-graphics-hlsl-to-sample.md)                                           | Amostra de uma textura.                                                                                                 |          |           | x        | x         |          |           |
| [SampleBias](dx-graphics-hlsl-to-samplebias.md)                                   | Exemplo de textura, depois de aplicar o valor de tendência ao nível de mipmap.                                              |          |           | x        | x         |          |           |
| [SampleCmp](dx-graphics-hlsl-to-samplecmp.md)                                     | Amostra de uma textura, usando um valor de comparação para rejeitar amostras.                                                     |          |           | x        | x         |          |           |
| [SampleCmpLevelZero](dx-graphics-hlsl-to-samplecmplevelzero.md)                   | Amostra de uma textura (somente mipmap nível 0), usando um valor de comparação para rejeitar amostras.                               | x        | x         | x        | x         | x        | x         |
| [SampleGrad](dx-graphics-hlsl-to-samplegrad.md)                                   | Exemplo de uma textura usando um gradiente para influenciar a maneira como o local de exemplo é calculado.                         | x        | x         | x        | x         | x        | x         |
| [SampleLevel](dx-graphics-hlsl-to-samplelevel.md)                                 | Exemplo de uma textura no nível de mipmap especificado.                                                                   | x        | x         | x        | x         | x        | x         |



 

### <a name="return-type"></a>Tipo de retorno

O tipo de retorno de um método de objeto de textura é FLOAT4, a menos que especificado de outra forma, com exceção dos objetos de textura com alias multiamostrados que sempre precisam do tipo e da contagem de amostras especificadas. O tipo de retorno é o mesmo que o tipo de recurso de textura ([**\_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)). Em outras palavras, pode ser qualquer um dos tipos a seguir.



| Tipo                       | Description                                                                                                                                                             |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| FLOAT                      | 32-bit float (consulte [regras de ponto flutuante](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) para diferenças de IEEE float)                            |
| INT                        | Inteiro com sinal de 32 bits                                                                                                                                                   |
| unsigned int               | Inteiro sem sinal de 32 bits                                                                                                                                                 |
| snorm                      | 32-bit float no intervalo de 1 a 1 inclusivo (consulte [regras de ponto flutuante](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) para diferenças de IEEE float) |
| unorm                      | 32-bit float no intervalo de 0 a 1 inclusivo (consulte [regras de ponto flutuante](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) para diferenças de IEEE float)  |
| qualquer tipo ou struct de textura | O número de componentes retornados deve estar entre 1 e 3, inclusive.                                                                                                    |



 

Além disso, o tipo de retorno pode ser qualquer tipo de textura, incluindo uma estrutura, mas deve ser inferior a 4 componentes, como um tipo float1 que retorna um componente.

## <a name="default-values-for-missing-components-in-a-texture"></a>Valores padrão para componentes ausentes em uma textura

O valor padrão para componentes ausentes em um tipo de recurso de textura é zero para qualquer componente, exceto o componente alfa (A); o valor padrão para o que está faltando é um. A maneira que ele aparece para o sombreador depende do tipo de recurso de textura. Ele assume a forma do primeiro componente tipado que está realmente presente no tipo de recurso de textura (a partir da esquerda na ordem RGBA). Se esse formulário for UNORM ou FLOAT, o valor padrão para o que está faltando é 1,0 f. Se o formulário for Santo ou UINT, o valor padrão para a ausente é 0x1.

Por exemplo, quando um sombreador lê [**o \_ formato dxgi \_ R24 \_ UNORM \_ x8 \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) tipo de recurso de textura sem tipos, os valores padrão para G e B são zero e o valor padrão de a é 1,0 f; quando um sombreador lê o tipo de recurso de textura [**R16G16 do \_ formato \_ \_ dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) , o valor padrão de B é zero e o valor padrão de a é 0x00000001; quando um sombreador lê o tipo de recurso de textura de [**\_ formato dxgi \_ R16 \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) , os valores padrão para G e B são zero e o valor padrão de a é 0x00000001.

## <a name="example-2"></a>Exemplo 2

Aqui está um exemplo de amostragem de textura usando um método de textura.


```
sampler MySamp;
Texture2D <float4> MyTex;
 
float4 main( float2 TexCoords[2] : TEXCOORD ) : SV_Target
{
    return MyTex.Sample( MySamp, TexCoords[0] ));
}
```



## <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Esse objeto tem suporte nos seguintes modelos de sombreador.



| Modelo de Sombreador                                                        | Com suporte |
|---------------------------------------------------------------------|-----------|
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md) e modelos de sombreador mais altos | sim       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

