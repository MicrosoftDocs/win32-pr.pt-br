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
ms.openlocfilehash: 7ddfbc679d95ca0a2c6fce0710b5de37f677fe0f
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122626722"
---
# <a name="scalar-types"></a>Tipos de escalares


O HLSL dá suporte a vários tipos de dados escalares:

-   **bool** - true ou false.
-   **int** – inteiro com sinal de 32 bits.
-   **uint** – inteiro sem sinal de 32 bits.
-   **dword** – inteiro sem sinal de 32 bits.
-   **metade** – valor de ponto flutuante de 16 bits. Esse tipo de dados é fornecido apenas para compatibilidade de idioma. Os destinos do sombreador Direct3D 10 mapeiam todos os metades dos tipos de dados para tipos de dados float. Um tipo de dados half não pode ser usado em uma variável global uniforme (use o sinalizador /Gec se essa funcionalidade for desejada).
-   **float** – valor de ponto flutuante de 32 bits.
-   **double** – valor de ponto flutuante de 64 bits. Você não pode usar valores de precisão dupla como entradas e saídas para um fluxo. Para passar valores de precisão dupla entre sombreadores, declare cada **um deles** como um par de tipos de dados **uint.** Em seguida, use a função  [**assint**](asuint.md) para empacotar cada duas vezes no par de **uint** s e a função [**asdouble**](asdouble.md) para desempacotar o par **de uint** s de volta no **duplo.**

A partir do Windows 8 HLSL também dá suporte a tipos de dados escalares de precisão mínima. Os drivers gráficos podem implementar tipos de dados escalares de precisão mínima usando qualquer precisão maior ou igual à precisão de bit especificada. É recomendável não depender do comportamento de fixação ou de quebra de quebra que depende da precisão subjacente específica. Por exemplo, o driver de gráficos pode executar aritmética em um **valor min16float** com precisão completa de 32 bits.

-   **min16float** – valor mínimo de ponto flutuante de 16 bits.
-   **min10float** – valor mínimo de ponto flutuante de 10 bits.
-   **min16int** – inteiro mínimo com sinal de 16 bits.
-   **min12int** – inteiro com sinal mínimo de 12 bits.
-   **min16uint** – inteiro sem sinal de 16 bits mínimo.

Para obter mais informações sobre literais escalares, consulte [Gramática](dx-graphics-hlsl-appendix-grammar.md).



<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Diferenças entre o Direct3D 9 e o Direct3D 10:<br/> No Direct3D 10, os seguintes tipos são modificadores para o tipo float.<br/>
<ul>
<li><strong>snorm float</strong> - Float normalizado com assinatura IEEE de 32 bits no intervalo -1 a 1, inclusive.</li>
<li><strong>unorm float</strong> - Float normalizado sem assinatura de IEEE de 32 bits no intervalo de 0 a 1, inclusive.</li>
</ul>
Por exemplo, aqui está uma declaração float-variable com sinal de 4 componentes.<br/> <span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
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

O HLSL também dá suporte a um tipo **de cadeia** de caracteres, que é uma cadeia de caracteres ASCII. Não há operações ou estados que aceitam cadeias de caracteres, mas os efeitos podem consultar parâmetros de cadeia de caracteres e anotações.

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
