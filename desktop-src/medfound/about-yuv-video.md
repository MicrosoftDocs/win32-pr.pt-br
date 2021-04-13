---
description: Sobre o vídeo YUV
ms.assetid: 089f42f2-1e5b-4d4b-98a4-9ef0ca2823c1
title: Sobre o vídeo YUV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b57b4a453870af34c221683bdaf613b5038081d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501642"
---
# <a name="about-yuv-video"></a>Sobre o vídeo YUV

Geralmente, o vídeo digital é codificado em um formato *YUV* . Este artigo explica os conceitos gerais do vídeo YUV, juntamente com alguma terminologia, sem se aprofundar na matemática do processamento de vídeo YUV.

Se você já trabalhou com gráficos de computador, provavelmente está familiarizado com a cor RGB. Uma cor RGB é codificada usando três valores: vermelho, verde e azul. Esses valores correspondem diretamente a partes do espectro visível. Os três valores RGB formam um sistema de coordenadas matemática, chamado de *espaço de cores*. O componente vermelho define um eixo desse sistema de coordenadas, azul define o segundo e verde define o terceiro, conforme mostrado na ilustração a seguir. Qualquer cor RGB válida cai em algum lugar nesse espaço de cores. Por exemplo, o magenta puro é 100% azul, 100% vermelho e 0% verde.

![diagrama mostrando o espaço de cores RGB](images/8ec60365-ed5c-41f7-9da9-be46aa82896a.gif)

Embora o RGB seja uma maneira comum de representar cores, outros sistemas de coordenadas são possíveis. O termo *YUV* refere-se a uma família de espaços de cores, todos os quais codificam informações de brilho separadamente das informações de cores. Assim como o RGB, o YUV usa três valores para representar qualquer cor. Esses valores são chamados Y ', U e V. (na verdade, esse uso do termo "YUV" é tecnicamente impreciso. No vídeo do computador, o termo YUV quase sempre se refere a um espaço de cor específico chamado Y'CbCr, discutido posteriormente. No entanto, o YUV é geralmente usado como um termo geral para qualquer espaço de cores que funcione nos mesmos princípios que Y'CbCr.)

O componente Y ', também chamado de *Luma*, representa o valor de brilho da cor. O símbolo primo (') é usado para diferenciar o Luma de um valor bem relacionado, *luminância*, que é designado como Y. a luminância é derivada de valores RGB *lineares* , enquanto Luma é derivado de valores RGB *não lineares* (gama-corrigidos). A luminância é uma medida mais próxima do verdadeiro brilho, mas o Luma é mais prático de usar por motivos técnicos. O símbolo primo é frequentemente omitido, mas os espaços de cores YUV sempre usam Luma, e não luminescência.

Luma é derivado de uma cor RGB, tomando uma média ponderada dos componentes vermelho, verde e azul. Para televisão de definição padrão, a fórmula a seguir é usada:

`Y' = 0.299R + 0.587G + 0.114B`

Essa fórmula reflete o fato de que o olho humano é mais sensível a determinados ondas de luz do que outros, o que afeta o brilho percebido de uma cor. A luz azul parece mais clara, verde parece mais brilhante e vermelho está em algum lugar entre elas. Essa fórmula também reflete as características físicas do phosphors usado em televisões iniciais. Uma fórmula mais recente, levando em conta a tecnologia de televisão moderna, é usada para televisão de alta definição:

`Y' = 0.2125R + 0.7154G + 0.0721B`

A equação Luma para a televisão de definição padrão é definida em uma especificação chamada ITU-R BT. 601. Para televisão de alta definição, a especificação relevante é ITU-R BT. 709.

Os componentes você e V, também chamados de valores *croma* ou valores de *diferença de cor* , são derivados ao subtrair o valor Y dos componentes vermelho e azul da cor RGB original:

`U = B - Y'`

`V = R - Y'`

Juntos, esses valores contêm informações suficientes para recuperar o valor RGB original.

## <a name="benefits-of-yuv"></a>Benefícios do YUV

A televisão analógica usa o YUV parcialmente por motivos históricos. Os sinais de televisão de cores analógicas foram projetados para serem compatíveis com as televisão em preto e branco. O sinal de televisão colorida transporta as informações de croma (você e V) sobrepostas ao sinal Luma. As televisões em preto e branco ignoram o croma e exibem o sinal combinado como uma imagem em tons de cinza. (O sinal é projetado de forma que o croma não interfira significativamente no sinal Luma.) As televisões de cores podem extrair o croma e converter o sinal de volta em RGB.

O YUV tem outra vantagem que é mais relevante atualmente. O olho humano é menos sensível a alterações em matiz do que alterações no brilho. Como resultado, uma imagem pode ter menos informações de croma do que as informações de Luma sem sacrificar a qualidade percebida da imagem. Por exemplo, é comum obter amostras dos valores de croma na metade da resolução horizontal dos exemplos de Luma. Em outras palavras, para cada duas amostras de Luma em uma linha de pixels, há um exemplo de U e uma amostra de V. Supondo que 8 bits sejam usados para codificar cada valor, um total de 4 bytes é necessário para cada dois pixels (dois Y ', um U e um V), para uma média de 16 bits por pixel ou 30% menor que a codificação RGB equivalente de 24 bits.

O YUV não é, de forma inerente, mais compacto que RGB. A menos que croma seja downsampled, um pixel YUV tem o mesmo tamanho de um pixel RGB. Além disso, a conversão de RGB em YUV não é uma perda. Se não houver redução de resolução, um pixel YUV poderá ser convertido de volta para RGB sem perda de informações. A redução de resolução torna a imagem YUV menor e também perde algumas das informações de cor. No entanto, se for executado corretamente, a perda não será perceptually significativa.

## <a name="yuv-in-computer-video"></a>Vídeo YUV no computador

As fórmulas listadas anteriormente para YUV não são as conversões exatas usadas em vídeo digital. O vídeo digital geralmente usa uma forma de YUV chamada Y'CbCr. Essencialmente, o Y'CbCr funciona dimensionando os componentes YUV para os seguintes intervalos:



| Componente | Intervalo                              |
|-----------|------------------------------------|
| Iar        | 16 a 235                             |
| CB/CR     | 16 a 240, com 128 representando zero |



 

Esses intervalos pressupõem 8 bits de precisão para os componentes Y'CbCr. Aqui está a derivação exata de Y'CbCr, usando a definição de BT. 601 de Luma:

1.  Comece com valores RGB no intervalo \[ 0... 1 \] . Em outras palavras, o preto puro é 0 e o branco puro é 1. É importante que eles sejam valores RGB não lineares (gama corrigidos).
2.  Calcule o Luma. Para BT. 601, Y ' = 0.299 R + 0.587 G + 0.114 B, conforme descrito anteriormente.
3.  Calcule os valores intermediários de diferença de croma (B-Y ') e (R-Y '). Esses valores têm um intervalo de +/-0,886 para (B-Y ') e +/-0,701 para (R-Y ').
4.  Dimensione os valores de diferença de croma da seguinte maneira:

    PB = (0,5/(1-0,114)) × (B-Y ')

    PR = (0,5/(1-0,299)) × (R-Y ')

    Esses fatores de dimensionamento são projetados para fornecer os dois valores do mesmo intervalo numérico, +/-0,5. Juntos, eles definem um espaço de cores YUV chamado Y'PbPr. Esse espaço de cores é usado no vídeo de componente analógico.

5.  Dimensione os valores de Y'PbPr para obter os valores finais de Y'CbCr:

    Y ' = 16 + 219 × Y '

    CB = 128 + 224 × PB

    CR = 128 + 224 × PR

Esses últimos fatores de dimensionamento produzem o intervalo de valores listados na tabela anterior. É claro que você pode converter RGB diretamente em Y'CbCr sem armazenar os resultados intermediários. As etapas são listadas separadamente aqui para mostrar como o Y'CbCr deriva das equações YUV originais fornecidas no início deste artigo.

A tabela a seguir mostra os valores RGB e YCbCr para várias cores, usando novamente a definição BT. 601 de Luma.



| Cor   | R   | G   | B   | Iar  | CB  | Cr  |
|---------|-----|-----|-----|-----|-----|-----|
| Preto   | 0   | 0   | 0   | 16  | 128 | 128 |
| Vermelho     | 255 | 0   | 0   | 81  | 90  | 240 |
| Verde   | 0   | 255 | 0   | 145 | 54  | 34  |
| Azul    | 0   | 0   | 255 | 41  | 240 | 110 |
| Cores    | 0   | 255 | 255 | 170 | 166 | 16  |
| Magenta | 255 | 0   | 255 | 106 | 202 | 222 |
| Amarelo  | 255 | 255 | 0   | 210 | 16  | 146 |
| Branca   | 255 | 255 | 255 | 235 | 128 | 128 |



 

Como mostra esta tabela, CB e CR não correspondem a ideias intuitivas sobre cor. Por exemplo, branco puro e preto puro contêm níveis neutros de CB e CR (128). Os valores mais altos e mais baixos para CB são Blue e Yellow, respectivamente. Para CR, os valores mais altos e mais baixos são vermelho e ciano.

## <a name="for-more-information"></a>Para obter mais informações

-   [Formatos de YUV de 8 bits recomendados para renderização de vídeo](recommended-8-bit-yuv-formats-for-video-rendering.md)
-   Conector de Keith. Vídeo desmistificado, quinta edição. Newnes, 2007.
-   Charles A. Poynton. Uma introdução técnica ao vídeo digital. Wiley, 1996.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tipos de mídia de vídeo](video-media-types.md)
</dt> <dt>

[Tipos de mídia](media-types.md)
</dt> </dl>

 

 



