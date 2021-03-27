---
title: Tipos de escalares
description: Tipos de escalares
ms.assetid: bf24d27f-2720-4268-bc74-fc46afedb9aa
keywords:
- Tipos escalares HLSL
topic_type:
- apiref
api_name:
- Scalar Types
api_type:
- NA
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/29/2020
ms.openlocfilehash: 7198932c6edb91e6f797b232b6c980976f3696a7
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/10/2021
ms.locfileid: "103663954"
---
# <a name="scalar-types"></a>Tipos de escalares


O HLSL dá suporte a vários tipos de dados escalares:

-   **bool** -true ou false.
-   inteiro com sinal **int** -32-bit.
-   **uint** -32-bit inteiro sem sinal.
-   **DWORD** -32 bits inteiro sem sinal.
-   valor de ponto flutuante de **metade** de 16 bits. Esse tipo de dados é fornecido somente para compatibilidade de idioma. Os destinos do sombreador do Direct3D 10 mapeiam todos os tipos de dados em anel para tipos de dados float. Um tipo de metade de dados não pode ser usado em uma variável global uniforme (use o sinalizador/GEC se essa funcionalidade for desejada).
-   **float** -valor de ponto flutuante de 32 bits.
-   valor de ponto flutuante de 64 bits **duplo** . Você não pode usar valores de precisão dupla como entradas e saídas para um fluxo. Para passar valores de precisão dupla entre sombreadores, declare cada **duplo** como um par de tipos de dados **uint** . Em seguida, use a função [**asuint**](asuint.md) para empacotar cada **duplo** no par de s **uint** e a função [**AsDouble**](asdouble.md) para desempacotar o par de s **uint** no **Double**.

A partir do Windows 8 HLSL também dá suporte a tipos de dados escalares de precisão mínima. Os drivers gráficos podem implementar os tipos de dados escalares de precisão mínima usando qualquer precisão maior ou igual à precisão de bit especificada. Recomendamos não contar com o comportamento de fixação MSS ou encapsulamento que depende da precisão subjacente específica. Por exemplo, o driver de gráficos pode executar aritmética em um valor de **min16float** na precisão total de 32 bits.

-   **min16float** -valor de ponto flutuante de 16 bits mínimo.
-   **min10float** -valor de ponto flutuante de 10 bits mínimo.
-   **min16int** -inteiro com sinal de 16 bits mínimo.
-   **min12int** -inteiro com sinal de 12 bits mínimo.
-   **min16uint** -inteiro sem sinal de 16 bits mínimo.

Para obter mais informações sobre literais escalares, consulte [gramática](dx-graphics-hlsl-appendix-grammar.md).



<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Diferenças entre o Direct3D 9 e o Direct3D 10:<br/> No Direct3D 10, os tipos a seguir são modificadores para o tipo float.<br/>
<ul>
<li><strong>snorm float</strong> - IEEE 32-bit assinado – float normalizado no intervalo de 1 a 1, inclusive.</li>
<li><strong>unorm float</strong> - IEEE 32-bit não assinado – float normalizado no intervalo de 0 a 1, inclusive.</li>
</ul>
Por exemplo, aqui está uma declaração float-Variable assinada com 4 componentes.<br/> <span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>snorm float4 fourComponentIEEEFloat;</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>



 

## <a name="string-type"></a>Tipo de cadeia de caracteres

O HLSL também dá suporte a um tipo de **cadeia de caracteres** , que é uma cadeia de caracteres ASCII. Não há operações ou Estados que aceitem cadeias de caracteres, mas os efeitos podem consultar os parâmetros e as anotações da cadeia.

## <a name="example"></a>Exemplo

```c
// top-level variable
float globalShaderVariable; 

// top-level function
void function(
in float4 position: POSITION0 // top-level argument
              )
{
  float localShaderVariable; // local variable
  function2(...)
}

void function2()
{
  ...
}
```

## <a name="see-also"></a>Confira também



* [Declarando tipos escalares](./dx-graphics-hlsl-writing-shaders-9.md#declaring-shader-variables)
* [Tipos de dados (DirectX HLSL)](dx-graphics-hlsl-data-types.md)