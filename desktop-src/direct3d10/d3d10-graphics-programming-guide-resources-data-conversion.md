---
description: As seções a seguir descrevem como o Direct3D manipula as conversões entre os tipos de dados.
ms.assetid: 454d3fd0-fc0f-46a9-925e-13f8e3c39f02
title: Regras de conversão de dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52b5ba37305fb7cadc229a614b883519cf6c5f45
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122626292"
---
# <a name="data-conversion-rules"></a>Regras de conversão de dados

As seções a seguir descrevem como o Direct3D manipula as conversões entre os tipos de dados.

-   [Terminologia do tipo de dados](#data-type-terminology)
-   [Conversão de ponto flutuante](#floating-point-conversion)
    -   [Reverter de uma representação de intervalo mais alto para uma representação de intervalo inferior](#conververting-from-a-higher-range-representation-to-a-lower-range-representation)
    -   [Convertendo de uma representação de intervalo inferior em uma representação de intervalo mais alto](#converting-from-a-lower-range-representation-to-a-higher-range-representation)
-   [Conversão de inteiro](#integer-conversion)
-   [Conversão de inteiro de ponto fixo](#fixed-point-integer-conversion)
-   [Tópicos relacionados](#related-topics)

## <a name="data-type-terminology"></a>Terminologia de tipo de dados

O conjunto de termos a seguir é usado posteriormente para caracterizar várias conversões de formato.



| Termo  | Definição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SNORM | Número inteiro assinado como normalizado, o que significa que, para o número de complemento de 2 n-bits, o valor máximo significa 1,0f (por exemplo, o valor de 5 bits 01111 é mapeado para 1,0f) e o valor mínimo significa -1,0f (por exemplo, o valor de 5 bits 10000 é mapeado para -1,0f). Além disso, o segundo número mínimo é mapeado para -1,0f (por exemplo, o valor de 5 bits 10001 é mapeado para -1,0f). Assim, há duas representações de inteiro para -1,0f. Há uma representação única para 0,0f e uma representação única para 1,0f. Isso resulta em um conjunto de representações de inteiros para valores de ponto flutuante uniformemente espaçados no intervalo (-1,0f... 0,0f) e também em um conjunto complementar de representações para os números no intervalo (0,0f... 1,0f). |
| UNORM | Números inteiros não assinados como normalizados, o que significa que, para um número de n-bits, todo 0 significa 0,0f, e todo o 1 significa 1,0f. É representada uma sequência de valores de ponto flutuante uniformemente espaçados de 0,0f para 1,0f. Por exemplo, um UNORM de 2 bits representa 0,0f, 1/3, 2/3 e 1,0f.                                                                                                                                                                                                                                                                                                                                                                                                                                |
| SINT  | Inteiro assinado. inteiro complemento de 2. Por exemplo, um SINT de 3 bits representa os valores integrais -4, -3, -2, -1, 0, 1, 2, 3.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| UINT  | Inteiro não assinado. Por exemplo, um UINT de 3 bits representa os valores integrais 0, 1, 2, 3, 4, 5, 6, 7.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| FLOAT | Um valor de ponto flutuante em uma das representações definidas pelo Direct3D.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| SRGB  | Semelhante a UNORM, pois em um número n-bits todo 0 significa 0,0f e todo 1 significa 1,0f. No entanto, ao contrário de UNORM, no SRGB a sequência de codificações de inteiros não assinados entre todos os 0 e todos os 1 representa uma progressão não linear na interpretação do ponto flutuante dos números, entre 0,0f e 1,0f. De modo geral, se essa progressão não linear, SRGB, fosse exibida como uma sequência de cores, ela seria exibida como uma rampa linear de níveis de luminosidade para um observador "médio", em condições de exibição "médias", em uma exibição "média". Para obter detalhes completos, consulte o padrão de cor SRGB, IEC 61996-2-1, na IEC (International Electrotechnical Commission).                |



 

## <a name="floating-point-conversion"></a>Conversão de ponto flutuante

Sempre que ocorre uma conversão de ponto flutuante entre diferentes representações, incluindo para representações de ponto não flutuante ou de representações de ponto não flutuante, aplicam-se as regras a seguir.

### <a name="conververting-from-a-higher-range-representation-to-a-lower-range-representation"></a>Conversão de uma representação de intervalo superior para uma representação de intervalo inferior

-   Arredondar para zero é usado durante a conversão para outro formato flutuante. Se o destino for um número inteiro ou formato de ponto fixo, é usado o arredondamento para o número par mais próximo, a menos que a conversão seja explicitamente documentada com o uso de outro comportamento de arredondamento, como arredondamento para o mais próximo para FLOAT para SNORM, FLOAT para UNORM ou FLOAT para SRGB. Outras exceções são as instruções de sombreador ftoi e ftou, que usam o arredondamento em direção ao zero. Por fim, as conversões de flutuante para fixo usadas pela amostra de textura e rasterizador têm uma tolerância especificada medida em ULP (unidade no último lugar) de um ideal infinitamente preciso.
-   Para valores de fonte maiores do que o intervalo dinâmico de um formato de destino de intervalo inferior (p. ex.: um valor alto flutuante de 32 bits é gravado em um RenderTarget flutuante de 16 bits), os resultados de valor (devidamente assinado) representável máximo, NÃO incluindo o infinito assinado (devido ao arredondamento em direção ao zero descrito acima).
-   NaN em um formato de intervalo superior será convertido em representação NaN no formato de intervalo inferior se a representação NaN existir no formato de intervalo inferior. Se o formato inferior não tiver uma representação NaN, o resultado será 0.
-   INF em um formato de intervalo superior será convertido em INF no formato de intervalo inferior, se disponível. Se o formato inferior não tiver uma representação INF, ele será convertido para o valor máximo representável. A assinatura será preservada se estiver disponível no formato de destino.
-   A desnormalização em um formato de intervalo superior será convertida para a representação desnormalizada no formato de intervalo inferior, se estiver disponível no formato de intervalo inferior e a conversão for possível, caso contrário, o resultado será 0. O bit de assinatura será preservado se estiver disponível no formato de destino.

### <a name="converting-from-a-lower-range-representation-to-a-higher-range-representation"></a>Conversão de uma representação de intervalo inferior para uma representação de intervalo superior

-   NaN em um formato de intervalo inferior será convertido em representação NaN no formato de intervalo superior se a representação NaN existir no formato de intervalo superior. Se o formato de intervalo superior não tiver uma representação NaN, ela será convertida como 0.
-   INF em um formato de intervalo inferior será convertido em representação INF no formato de intervalo superior se disponível no formato de intervalo superior. Se o formato superior não tiver uma representação INF, ele será convertido no valor máximo representável (MAX \_ FLOAT nesse formato). A assinatura será preservada se estiver disponível no formato de destino.
-   A desnormalização em um formato de intervalo inferior será convertida em uma representação normalizada no formato de intervalo superior se possível, ou então para uma representação desnormalizada no formato de intervalo superior se existir a representação desnormalizada. Se isso falhar, se o formato de intervalo superior não tiver uma representação desnormalizada, ela será convertida como 0. A assinatura será preservada se estiver disponível no formato de destino. Observe que os números flutuantes de 32 bits contam como um formato sem uma representação desnormalizada (porque as desnormalizações em operações em números flutuantes de 32 bits fluem para assinar 0 preservados).

## <a name="integer-conversion"></a>Conversão de inteiro

A tabela a seguir descreve as conversões das várias representações descritas acima para outras representações. Somente as conversões que realmente ocorrem em Direct3D são mostradas.



<table>
<colgroup>
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Tipo de dados de origem</th>
<th>Tipo de dados de destino</th>
<th>Regra de conversão</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>SNORM</td>
<td>FLOAT</td>
<td>Dado um valor inteiro de n-bits que representa o intervalo assinado [-1,0f para 1,0f], a conversão para ponto flutuante é a seguinte.<br/>
<ul>
<li>O valor mais negativo é mapeado para -1,0f. por exemplo, o valor de 5 bits 10000 é mapeado para -1,0f.</li>
<li>Todos os outros valores são convertidos para flutuante (que vamos chamar de c) e, assim, o resultado = c * (1,0f / (2⁽ⁿ⁻¹⁾-1)). Por exemplo, o valor de 5 bits 10001 é convertido para -15,0f e, em seguida, dividido por 15,0f, resultando em -1,0f.</li>
</ul></td>
</tr>
<tr class="even">
<td>FLOAT</td>
<td>SNORM</td>
<td>Dado um número de ponto flutuante, a conversão para um valor inteiro de n-bits representando o intervalo assinado [-1,0f para 1,0f], é a seguinte.<br/>
<ul>
<li>Digamos que c represente o valor inicial.</li>
<li>Se c for NaN, o resultado será 0.</li>
<li>Se c > 1,0f, incluindo INF, ele será fixado em 1,0f.</li>
<li>Se c < -1.0f, incluindo -INF, ele será fixado a -1,0f.</li>
<li>Converter de escala de número flutuante em escala de números inteiros: c = c * (2ⁿ⁻¹-1).</li>
<li>Converter em um número inteiro como se segue.
<ul>
<li>Se c >= 0, c = c + 0,5f; caso contrário, c = c - 0,5f.</li>
<li>Descarte a fração decimal e o valor de ponto flutuante restante (integral) será convertido diretamente em um número inteiro.</li>
</ul></li>
</ul>
Essa conversão permite uma tolerância do D3D<em>xx</em>_FLOAT32_TO_INTEGER_TOLERANCE_IN_Unit-Last-Place Unidade-no último lugar (no lado do número inteiro). Isso significa que, após a conversão de escala de números flutuantes para escala de números inteiros, qualquer valor dentro de D3D<em>xx</em>_FLOAT32_TO_INTEGER_TOLERANCE_IN_ULP Unidade no último lugar de um valor de formato de destino representável tem permissão para ser mapeado para esse valor. O requisito adicional de Data Invertability garante que a conversão seja não decrescente no intervalo e todos os valores de saída sejam atingíveis. (Nas constantes mostradas aqui, <em>xx</em> deve ser substituído com a versão do Direct3D, por exemplo, 10, 11 ou 12.)<br/></td>
</tr>
<tr class="odd">
<td>UNORM</td>
<td>FLOAT</td>
<td>O valor de n-bits inicial é convertido em flutuante (0,0f, 1,0f, 2,0f, etc.) e, em seguida, dividido por (2ⁿ-1).<br/></td>
</tr>
<tr class="even">
<td>FLOAT</td>
<td>UNORM</td>
<td>Digamos que c represente o valor inicial.<br/>
<ul>
<li>Se c for NaN, o resultado será 0.</li>
<li>Se c > 1,0f, incluindo INF, ele será fixado em 1,0f.</li>
<li>Se c < 0,0f, incluindo -INF, ele será fixado em 0,0f.</li>
<li>Converter de escala de número flutuante em escala de números inteiros: c = c * (2ⁿ-1).</li>
<li>Converter em números inteiros.
<ul>
<li>c = c + 0,5f.</li>
<li>A fração decimal é descartada, e o valor de ponto flutuante restante (integral) será convertido diretamente em um número inteiro.</li>
</ul></li>
</ul>
Essa conversão tem uma tolerância permitida do D3D<em>xx</em>_FLOAT32_TO_INTEGER_TOLERANCE_IN_ULP Unidade no último lugar (no lado do número inteiro). Isso significa que, após a conversão de escala de números flutuantes para escala de números inteiros, qualquer valor dentro de D3D<em>xx</em>_FLOAT32_TO_INTEGER_TOLERANCE_IN_ULP Unidade no último lugar de um valor de formato de destino representável tem permissão para ser mapeado para esse valor. O requisito adicional de Data Invertability garante que a conversão seja não decrescente no intervalo e todos os valores de saída sejam atingíveis.<br/></td>
</tr>
<tr class="odd">
<td>SRGB</td>
<td>FLOAT</td>
<td>A conversão a seguir é a ideal de SRGB para FLOAT.<br/>
<ul>
<li>Tome o valor inicial de n-bits, converta-o a um número flutuante (0,0f, 1,0f, 2,0f, etc.); chame isso de c.</li>
<li>c = c * (1.0f / (2ⁿ-1))</li>
<li>Se (c < = D3D<em>xx</em>_SRGB_TO_FLOAT_THRESHOLD) então: resultado = c /D3D<em>xx</em>_SRGB_TO_FLOAT_DENOMINATOR_1, caso mais: resultado = ((c + D3D<em>xx</em>_SRGB_TO_FLOAT_OFFSET)/D3D<em>xx</em>_SRGB_TO_FLOAT_DENOMINATOR_2)D3D<em>xx</em>_SRGB_TO_FLOAT_EXPONENT</li>
</ul>
Essa conversão tem uma tolerância permitida do D3D<em>xx</em>_SRGB_TO_INTEGER_TOLERANCE_IN_ULP Unidade no último lugar (no lado SRGB). <br/></td>
</tr>
<tr class="even">
<td>FLOAT</td>
<td>SRGB</td>
<td>A seguir está a conversão FLOAT-> SRGB ideal.<br/> Supondo que o componente de cor SRGB do destino tenha n-bits:<br/>
<ul>
<li>Suponha que o valor inicial é c.</li>
<li>Se c for NaN, o resultado será 0.</li>
<li>Se c > 1,0f, incluindo INF, será fixado em 1,0f.</li>
<li>Se c < 0,0f, incluindo -INF, ele será fixado em 0,0f.</li>
<li>Se (c <= D3D<em>xx</em>_FLOAT_TO_SRGB_THRESHOLD) então: c = D3D<em>xx</em>_FLOAT_TO_SRGB_SCALE_1 * c, caso outro: c = D3D<em>xx</em>_FLOAT_TO_SRGB_SCALE_2 * c(D3D<em>xx</em>_FLOAT_TO_SRGB_EXPONENT_NUMERATOR/D3D<em>xx</em>_FLOAT_TO_SRGB_EXPONENT_DENOMINATOR) - D3D<em>xx</em>_FLOAT_TO_SRGB_OFFSET</li>
<li>Converter de escala de número flutuante em escala de números inteiros: c = c * (2ⁿ-1).</li>
<li>Converter em números inteiros:
<ul>
<li>c = c + 0,5f.</li>
<li>A fração decimal é descartada, e o valor de ponto flutuante restante (integral) será convertido diretamente em um número inteiro.</li>
</ul></li>
</ul>
Essa conversão tem uma tolerância permitida do D3D<em>xx</em>_FLOAT32_TO_INTEGER_TOLERANCE_IN_ULP Unidade no último lugar (no lado do número inteiro). Isso significa que, após a conversão de escala de números flutuantes para escala de números inteiros, qualquer valor dentro de D3D<em>xx</em>_FLOAT32_TO_INTEGER_TOLERANCE_IN_ULP Unidade no último lugar de um valor de formato de destino representável tem permissão para ser mapeado para esse valor. O requisito adicional de Data Invertability garante que a conversão seja não decrescente no intervalo e todos os valores de saída sejam atingíveis.<br/></td>
</tr>
<tr class="odd">
<td>SINT</td>
<td>SINT com mais bits</td>
<td>Para converter de SINT para um SINT com mais bits, o bit mais significativo (MSB) do número inicial é &quot;assinatura estendida&quot; para os bits adicionais disponíveis no formato de destino.<br/></td>
</tr>
<tr class="even">
<td>UINT</td>
<td>SINT com mais bits</td>
<td>Para converter de UINT em um SINT com mais bits, o número é copiado para os bits menos significativos do formato de destino (LSBs) e os MSBs adicionais são preenchidos com 0.<br/></td>
</tr>
<tr class="odd">
<td>SINT</td>
<td>UINT com mais bits</td>
<td>Para converter de SINT em UINT com mais bits: Se negativo, o valor é vinculado como 0. Caso contrário, o número é copiado para os LSBs do formato destino e os MSB adicionais são preenchidos com 0.<br/></td>
</tr>
<tr class="even">
<td>UINT</td>
<td>UINT com mais bits</td>
<td>Para converter de UINT em UINT com mais bits, o número é copiado para LSBs do formato de destino e os MSBs adicionais são preenchidos com 0.<br/></td>
</tr>
<tr class="odd">
<td>SINT ou UINT</td>
<td>SINT ou UINT com menos bits ou bits iguais</td>
<td>Para converter de um SINT ou UINT para SINT ou UINT com menos bits ou bits iguais (e/ou mudar a assinatura ou não assinatura), o valor inicial é simplesmente vinculado ao intervalo do formato de destino.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="fixed-point-integer-conversion"></a>Conversão de números inteiros de ponto fixo

Os inteiros de ponto fixo são simplesmente os inteiros de algum tamanho de bit que têm um ponto decimal implícito em um local fixo.

O tipo de dados "inteiro", presente em todos os lugares, é um caso especial de um inteiro de ponto fixo com decimal no final do número.

Representações de número de ponto fixo são caracterizadas como: i,f, onde i é o número de bits de inteiros e f é o número de bits fracionais. por exemplo, 16,8 significa 16 bits inteiros seguidos por 8 bits de fração. A parte inteira é armazenada no complemento de 2, pelo menos como definido aqui (embora ele também possa ser definido igualmente por números inteiros não assinados). A parte fracionária é armazenada em formato não assinado. A parte fracionária sempre representa a fração positiva entre os dois valores integrais mais próximos, começando pelo mais negativo.

As operações de adição e subtração em números de ponto fixo são executadas usando simplesmente a aritmética padrão de números inteiros, sem qualquer consideração em relação ao decimal implícito. A adição de 1 a um número de ponto fixo 16,8 significa apenas a adição de 256, como o decimal está a 8 lugares do extremo menos significativo do número. Outras operações, como a multiplicação, também podem ser executadas simplesmente usando aritmética de números inteiros, desde que o efeito sobre o decimal fixo seja levado em consideração. Por exemplo, multiplicar dois inteiros de 16,8 usando um multiplicador inteiro produz um resultado de 32,16.

Representações de inteiro de ponto fixo são usadas de duas maneiras no Direct3D.

-   As posições de vértice pós-vinculadas no rasterizador são ajustadas para ponto fixo, para distribuir de maneira uniforme a precisão pela área RenderTarget. Muitas operações de rasterizador, incluindo o conjunto de face frontal como um exemplo, ocorrem em posições de ponto fixo ajustadas, enquanto outras operações, como instalação de interpolador do atributo, usam posições que foram convertidas de volta para um ponto flutuante das posições de ponto fixo ajustadas.
-   As coordenadas de textura para operações de amostragem são ajustadas para ponto fixo (após serem dimensionadas por tamanho de textura), para distribuir uniformemente a precisão no espaço de textura, ao escolher locais/pesos de toque de filtros. Os valores ponderados são convertidos de volta para ponto flutuante antes de a aritmética real de filtragem ser realizada.



<table>
<colgroup>
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Tipo de dados de origem</th>
<th>Tipo de dados de destino</th>
<th>Regra de conversão</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>FLOAT</td>
<td>Inteiro de ponto fixo</td>
<td>A seguir está o procedimento geral para converter um número de ponto flutuante n para um inteiro de ponto fixo inteiro i,f, onde i é o número de bits de números inteiros (assinados) e f é o número de bits fracionários.<br/>
<ul>
<li>Calcular FixedMin = -2⁽ⁱ⁻¹⁾</li>
<li>Compute FixedMax = 2⁽⁻ Meio⁾ - 2<sup>(-f)</sup></li>
<li>Se n for um NaN, result = 0; se n for +Inf, result = FixedMax*2<sup>f</sup>; se n for -Inf, result = FixedMin*2<sup>f</sup></li>
<li>Se n >= FixedMax, result = Fixedmax*2<sup>f</sup>; se n <= FixedMin, result = FixedMin*2 <sup> f</sup></li>
<li>Ou calcule n*2<sup>f</sup> e converta em números inteiros.</li>
</ul>
As implementações são permitidas em D3D<em>xx</em>_FLOAT32_TO_INTEGER_TOLERANCE_IN_ULP Unidade no último lugar tolerância no resultado inteiro, em vez do valor infinitamente preciso n*2<sup>f</sup> depois do último passo acima.<br/></td>
</tr>
<tr class="even">
<td>Inteiro de ponto fixo</td>
<td>FLOAT</td>
<td>Suponha que a representação de ponto fixo específico sendo convertida em flutuante não contenha mais do que um total de 24 bits de informações, não mais de 23 bits dos quais está no componente fracionário. Suponha que um dado número de ponto fixo, fxp, esteja na forma de i,f (i bits de números inteiros, f bits fracionários). A conversão para flutuante é semelhante ao pseudocódigo a seguir.<br/> float result = (float)(fxp >> f) + // extract integer<br/> <dl> ((float)(fxp & (2<sup>f</sup> - 1)) / (2<sup>f</sup>)); // extrair fração<br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Recursos (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 




