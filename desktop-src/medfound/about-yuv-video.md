---
description: Sobre o vídeo yuv
ms.assetid: 089f42f2-1e5b-4d4b-98a4-9ef0ca2823c1
title: Sobre o vídeo yuv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3499a8adfe1a43a22fe9bdd9ff4e576b7a14c398a9dafc0b945647d7225ad581
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118744235"
---
# <a name="about-yuv-video"></a>Sobre o vídeo yuv

O vídeo digital geralmente é codificado em um *formato YUV.* Este artigo explica os conceitos gerais do vídeo YUV, juntamente com alguma terminologia, sem se a fundo na matemática do processamento de vídeo YUV.

Se você já trabalhou com gráficos de computador, provavelmente está familiarizado com a cor RGB. Uma cor RGB é codificada usando três valores: vermelho, verde e azul. Esses valores correspondem diretamente a partes do espectro visível. Os três valores RGB formam um sistema de coordenadas matemática, chamado de *espaço de cores.* O componente vermelho define um eixo desse sistema de coordenadas, azul define o segundo e verde define o terceiro, conforme mostrado na ilustração a seguir. Qualquer cor RGB válida se enquadra em algum lugar dentro desse espaço de cores. Por exemplo, o magenta puro é 100% azul, 100% vermelho e 0% verde.

![diagrama mostrando o espaço de cor rgb](images/8ec60365-ed5c-41f7-9da9-be46aa82896a.gif)

Embora o RGB seja uma maneira comum de representar cores, outros sistemas de coordenadas são possíveis. O termo *YUV* refere-se a uma família de espaços de cores, que codificam informações de brilho separadamente das informações de cor. Assim como o RGB, o YUV usa três valores para representar qualquer cor. Esses valores são termo Y', U e V. (na verdade, esse uso do termo "YUV" é tecnicamente impreciso. No vídeo do computador, o termo YUV quase sempre se refere a um espaço de cores específico chamado Y'CbCr, discutido posteriormente. No entanto, o YUV geralmente é usado como um termo geral para qualquer espaço de cores que funcione com os mesmos princípios que Y'CbCr.)

O componente Y', também chamado *de luma*, representa o valor de brilho da cor. O símbolo principal (') é usado para diferenciar o luma de um valor intimamente relacionado, *luminância*, que é designado como Y. A Luminance é derivada de valores RGB *lineares,* enquanto luma é derivado de valores RGB não *lineares* (corrigidos por gama). A Luminância é uma medida mais próxima do verdadeiro brilho, mas o luma é mais prático de usar por motivos técnicos. O símbolo principal é frequentemente omitido, mas os espaços de cores YUV sempre usam luma, não luminância.

O Luma é derivado de uma cor RGB por meio de uma média ponderada dos componentes vermelho, verde e azul. Para a tv de definição padrão, a fórmula a seguir é usada:

`Y' = 0.299R + 0.587G + 0.114B`

Essa fórmula reflete o fato de que o olho humano é mais sensível a determinados tipos de luz do que outros, o que afeta o brilho percebido de uma cor. A luz azul aparece mais esmaecida, verde aparece mais brilhante e vermelho está em algum lugar entre eles. Essa fórmula também reflete as características físicas das pessoas que são usadas nos primeiros rádios. Uma fórmula mais nova, levando em conta a tecnologia de tv moderna, é usada para a tv de alta definição:

`Y' = 0.2125R + 0.7154G + 0.0721B`

A equação de luma para a tv de definição padrão é definida em uma especificação chamada ITU-R BT.601. Para a tv de alta definição, a especificação relevante é ITU-R BT.709.

Os componentes você e V, também  chamados valores *de chroma* ou valores de diferença de cor, são derivados subtraindo o valor Y dos componentes vermelho e azul da cor RGB original:

`U = B - Y'`

`V = R - Y'`

Juntos, esses valores contêm informações suficientes para recuperar o valor RGB original.

## <a name="benefits-of-yuv"></a>Benefícios do YUV

A tv anapáloga usa YUV parcialmente por motivos históricos. Os sinais de tv de cores análogas foram projetados para serem compatíveis com versões anteriores com tvs em preto e branco. O sinal de tv de cores carrega as informações de chroma (você e V) sobrepostas ao sinal de luma. As tvs em preto e branco ignoram a chroma e exibem o sinal combinado como uma imagem em escala de cinza. (O sinal foi projetado para que o chroma não interfira significativamente no sinal de luma.) Os tvs de cores podem extrair a chroma e converter o sinal de volta em RGB.

O YUV tem outra vantagem que é mais relevante atualmente. O olhar humano é menos sensível às alterações de matiz do que às alterações no brilho. Como resultado, uma imagem pode ter menos informações de chroma do que informações de luma sem sacrificar a qualidade percebida da imagem. Por exemplo, é comum amostrar os valores de chroma na metade da resolução horizontal das amostras de luma. Em outras palavras, para cada dois exemplos de luma em uma linha de pixels, há um exemplo de U e um exemplo de V. Supondo que 8 bits sejam usados para codificar cada valor, um total de 4 bytes é necessário para cada dois pixels (dois Y', um U e um V), para uma média de 16 bits por pixel ou 30% menor do que a codificação RGB de 24 bits equivalente.

YUV não é inerentemente mais compacto do que o RGB. A menos que o chroma seja reduzido, um pixel YUV tem o mesmo tamanho de um pixel RGB. Além disso, a conversão de RGB para YUV não é perdida. Se não houver nenhum downsampling, um pixel YUV poderá ser convertido novamente em RGB sem perda de informações. O downsampling torna uma imagem YUV menor e também perde algumas das informações de cor. No entanto, se executada corretamente, a perda não é perceptívelmente significativa.

## <a name="yuv-in-computer-video"></a>Vídeo de YUV no computador

As fórmulas listadas anteriormente para YUV não são as conversões exatas usadas em vídeo digital. O vídeo digital geralmente usa uma forma de YUV chamada Y'CbCr. Essencialmente, o Y'CbCr funciona dimensionando os componentes YUV para os seguintes intervalos:



| Componente | Intervalo                              |
|-----------|------------------------------------|
| Y'        | 16–235                             |
| Cb/Cr     | 16–240, com 128 representando zero |



 

Esses intervalos assumem 8 bits de precisão para os componentes do Y'CbCr. Aqui está a derivação exata de Y'CbCr, usando a definição BT.601 de luma:

1.  Comece com valores RGB no intervalo \[ 0...1 \] . Em outras palavras, preto puro é 0 e branco puro é 1. É importante que eles sejam valores RGB não lineares (corrigidos por gama).
2.  Calcule o luma. Para BT.601, Y' = 0,299R + 0,587G + 0,114B, conforme descrito anteriormente.
3.  Calcule os valores intermediários de diferença de chroma (B - Y') e (R - Y'). Esses valores têm um intervalo de +/- 0,886 para (B - Y') e +/- 0,701 para (R - Y').
4.  Dimensione os valores de diferença de chroma da seguinte forma:

    Pb = (0,5 / (1 a 0,114)) × (B - Y')

    Pr = (0,5 / (1 a 0,299)) × (R - Y')

    Esses fatores de dimensionamento foram projetados para dar aos dois valores o mesmo intervalo numérico, +/- 0,5. Juntos, eles definem um espaço de cores YUV chamado Y'PbPr. Esse espaço de cor é usado em vídeo de componentes análogo.

5.  Dimensione os valores de Y'PbPr para obter os valores de Y'CbCr finais:

    Y' = 16 + 219 × Y'

    Cb = 128 + 224 × Pb

    Cr = 128 + 224 × Pr

Esses últimos fatores de dimensionamento produzem o intervalo de valores listados na tabela anterior. É claro que você pode converter RGB diretamente em Y'CbCr sem armazenar os resultados intermediários. As etapas são listadas separadamente aqui para mostrar como Y'CbCr deriva das equações YUV originais fornecidas no início deste artigo.

A tabela a seguir mostra os valores de RGB e YCbCr para várias cores, novamente usando a definição BT.601 de luma.



| Color   | R   | G   | B   | Y'  | Cb  | Cr  |
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

 

 



