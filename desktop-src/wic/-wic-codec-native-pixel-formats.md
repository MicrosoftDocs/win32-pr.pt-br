---
description: Este tópico apresenta os formatos de pixel fornecidos pelo Windows Imaging Component (WIC).
ms.assetid: 348b6d15-e339-4dce-99f3-4d639ee9bf7d
title: Visão geral dos formatos de pixel nativos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4df37481399ac8193effc5d8f93aa49050460ee6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105811945"
---
# <a name="native-pixel-formats-overview"></a>Visão geral dos formatos de pixel nativos

Este tópico apresenta os formatos de pixel fornecidos pelo Windows Imaging Component (WIC).

Um formato de pixel descreve o layout de memória de cada pixel em um bitmap. Este layout de memória descreve como os dados de imagem de um bitmap são codificados especificando o formato numérico e a organização do canal de cores. O WIC dá suporte a vários formatos numéricos para vários esquemas de organização de canal de cor, fornecendo uma ampla gama de formatos de pixel.

-   [Profundidade de bits](#bit-depth)
-   [Codificação numérica](#numerical-encoding)
-   [Canais de cores](#color-channels)
    -   [Modelo de cores RGB/BGR](#rgbbgr-color-model)
    -   [Modelo de cor CMYK](#cmyk-color-model)
    -   [Modelo de cores de n canais](#n-channel-color-model)
    -   [Modelos de cores indexadas e em escala de cinza](#indexed-and-grayscale-color-models)
    -   [Modelo de cores Y'CbCr](#ycbcr-color-model)
-   [Formato de pixel do WIC](#wic-pixel-format)
    -   [Formatos de pixel indefinidos](#undefined-pixel-formats)
    -   [Formatos de pixel indexados](#indexed-pixel-formats)
    -   [Formatos de pixel de bit empacotado](#packed-bit-pixel-formats)
    -   [Formatos de pixel em escala de cinza](#grayscale-pixel-formats)
    -   [Formatos de pixel RGB/BGR](#rgbbgr-pixel-formats)
    -   [Formatos de pixel CMYK](#cmyk-pixel-formats)
    -   [Formatos de pixel de n-Channel](#n-channel-pixel-formats)
    -   [Apenas formatos de pixel alfa](#alpha-only-pixel-formats)
    -   [Formatos de pixel Y'CbCr](#ycbcr-pixel-formats)
-   [Espaço de cores](#color-space)
-   [Formatos de imagem nativa](#native-image-formats)
    -   [Codec nativo BMP](#bmp-native-codec)
    -   [Codec nativo GIF](#gif-native-codec)
    -   [Codec nativo da ICO](#ico-native-codec)
    -   [Codec nativo JPEG](#jpeg-native-codec)
    -   [Codec nativo do PNG](#png-native-codec)
    -   [Codec nativo TIFF](#tiff-native-codec)
    -   [Codec de JPEG-XR Native](#jpeg-xr-native-codec)
-   [Codec do DDS Native](#dds-native-codec)
-   [Extensibilidade de formato de pixel](#pixel-format-extensibility)
-   [Tópicos relacionados](#related-topics)

## <a name="bit-depth"></a>Profundidade de bits

A *profundidade de bits* é o número de bits usados para codificar cada canal de cor. Hoje, a maioria das imagens digitais usa uma profundidade de 8 bits, o que significa que cada canal de cor em um pixel é representado por 8 bits, fornecendo 2 ⁸ (256) valores exclusivos por canal. Uma imagem que tem uma profundidade de 8 e três canais de cor (como vermelho, verde e azul) usa 24 bits por pixel (BPP), que fornece 2 ² ⁴ (16.777.216) cores diferentes por pixel.

Para uma resolução de cor melhor, é possível usar uma profundidade de bits 16 ou 32. Isso fornece cada canal de cor com 2 ¹ ⁶ (65.536) ou 2 ³ ² valores exclusivos, a um custo de mais memória por pixel.

Em alguns formatos, a profundidade de bits não é um múltiplo de 8. Esses formatos são chamados de formatos *empacotados* , porque os canais de cor em um pixel não estão alinhados aos limites de byte. Por exemplo, se as profundidades de bits de 5, três canais de cor puderem ser armazenados em 16 bits (incluindo 1 bit de preenchimento, para tornar os pixels alinhados por byte). Os formatos empacotados são úteis quando a memória ou a capacidade de processamento são limitadas.

## <a name="numerical-encoding"></a>Codificação numérica

Para a maioria das imagens digitais de hoje, os bytes não assinados e os inteiros curtos não assinados são usados para descrever o intervalo numérico de cada canal de cor. O valor mínimo (0) representa a intensidade zero em um canal de cor única e o preto é obtido quando todos os canais de cores são zero. Da mesma forma, o valor máximo representa a intensidade total e o branco é obtido quando todos os canais de cores estão com intensidade total. A uma profundidade de um bit de 8, um UINT fornece 256 valores exclusivos por canal de cor (0-255). Um UINT de 16 bits fornece 65.536 valores exclusivos por canal de cor (0-65.535).

Além disso, o WIC dá suporte a formatos de ponto fixo e ponto flutuante. Esses formatos dão suporte a intervalos dinâmicos maiores, pois todo o intervalo numérico de cada canal de cor é maior do que o intervalo visível. Como resultado, as cores podem ser ajustadas acima ou abaixo do intervalo visível, durante as etapas intermediárias de processamento de imagens, sem perda de informações de imagem.

### <a name="fixed-point-numerical-encoding"></a>Codificação numérica Fixed-Point

valores de ponto fixo de 16 bits são interpretados como s 2,13: sign bit, dois bits inteiros e treze bits fracionários. Usando essa interpretação, um intervalo numérico de − 4,0 a + 3,999... pode ser representado, com o valor de 1,0 representado pelo valor inteiro assinado 8192 (0x2000).

os valores de ponto fixo de 32 bits são interpretados como s 7.24: o bit de sinal, sete bits inteiros e vinte e quatro bits fracionários. Usando essa interpretação, um intervalo numérico de − 128,0 a + 127,999... pode ser representado, com o valor de 1,0 representado pelo valor inteiro assinado 16777216 (0x01000000).

## <a name="color-channels"></a>Canais de cores

Os canais de cor de um formato de pixel definem o layout de memória de cada cor dentro dos dados de imagem de um bitmap. Há uma variedade de diferentes estruturas de canal de cores comuns nas imagens digitais de hoje, e o WIC fornece suporte para muitas delas.

### <a name="rgbbgr-color-model"></a>Modelo de cores RGB/BGR

Os formatos RGB e BGR descrevem as cores em um modelo de cores aditivo. O método mais comum de descrever uma imagem é com três canais de cores separados que representam as cores vermelho (R), verde (G) e azul (B). O WIC fornece suporte para esses três canais na ordem vermelha-verde-azul (RGB) ou azul-verde-vermelho (BGR). Essa é a ordem na qual cada canal de cor aparece dentro do fluxo de bits sequencial. Por exemplo, no \_ formato WICPixelFormat32bppRGB de GUID, cada pixel tem 32 bits de largura. O canal vermelho é o primeiro byte (menos significativo) na memória, seguido de verde e, em seguida, azul. Por outro lado, no \_ formato WICPixelFormat32bppBGR de GUID, os canais de cores estão na ordem oposta. O WIC dá suporte a vários formatos RGB/BGR, incluindo formatos especiais de bits empacotados, como o GUID \_ WICPixelFormat16bppBGR555.

> [!Note]  
> Os canais de cores dos formatos de bits de pacotes especiais BGR não estão em múltiplos de 8 como os canais de cores em formatos de pixel típicos. Isso significa que os valores de canal não são alinhados em byte. Deve-se ter cuidado ao ler canais de cores de bits empacotados.

 

Além dos formatos RGB e BGR, o WIC também fornece formatos de pixel RGB e BGR que dão suporte a um canal alfa (A). O canal alfa fornece dados de opacidade para o pixel. Para formatos com um canal alfa adicionado, o canal alfa geralmente vem por último na ordem do canal de cores. Por exemplo, no formato de pixel GUID \_ WICPixelFormat32bppBGRA, a ordem de byte é azul, verde e vermelha, seguida pelo canal alfa.

O WIC também dá suporte a formatos de pixel RGB (P) Alpha bimultiplicados. Em um formato de pixel RGBA típico, os valores de cor vermelho, verde e azul são os valores de cor reais para a imagem. Para criar uma imagem composta no formato RGBA padrão, o valor alfa da imagem em primeiro plano deve ser multiplicado por cada um dos canais vermelho, verde e azul antes de adicioná-lo à cor da imagem de plano de fundo. Em um formato de pixel RGB previamente multiplicado, cada canal de cor já foi multiplicado pelo valor alfa. Isso fornece um método mais eficiente de composição de imagem com dados de canal alfa. Para recuperar os valores de cor verdadeiros de cada canal em um formato de pixel PRGBA/PBGRA, a multiplicação de canal alfa deve ser revertida pela divisão dos valores de cor pelo valor alfa.

### <a name="cmyk-color-model"></a>Modelo de cor CMYK

CMYK é um modelo de cor subtraído usado na impressão. As cores produzidas por um modelo CMYK são geradas pela luz que não é absorvido, mas refletidas. CMYK é um modelo de quatro canais de ciano (C), magenta (M), amarelo (Y) e preto (K). Quando todos os quatro canais de cores estiverem no valor máximo, o resultado será preto. Como os modelos de cores RGB/BGR, a ordem de bytes dentro do fluxo de bits sequencial é fornecida pelo nome do formato de pixel. Por exemplo, no formato de pixel GUID \_ WICPixelFormat32bppCMYK, cada pixel é composto de 32 bits. O primeiro byte contém o valor ciano, seguido por virar por magenta, amarelo e preto. O WIC fornece formatos de pixel para CMYK em 32 e 64 bits por pixel (BPP).

Além do modelo de cores CMYK padrão, o WIC também fornece CMYK com Alfa. Isso permite que as imagens CMYK tenham dados de mesclagem alfa semelhantes ao modelo de cores RGB/BGR. O canal alfa está localizado imediatamente após preto no fluxo de bits sequencial de um bitmap.

### <a name="n-channel-color-model"></a>Modelo de cores de n canais

Para flexibilidade, o WIC também fornece formatos de pixel que não têm uma ordem de canal predefinida. O WIC fornece formatos de pixel que dão suporte de três a oito canais de dados de imagem contínua em profundidades de bits de 8 e 16. Ao contrário dos formatos de pixel RGB/BGR e CMYK, os formatos de n-Channel não especificam a ordem do canal, mas sim o número de canais de cores disponíveis. Por exemplo, no formato de pixel GUID \_ WICPixelFormat32bpp4Channels, cada pixel é composto de 32 bits com cada um dos 4 canais que ocupam um único byte.

O WIC também fornece formatos de pixel para o n-Channel com Alfa. Isso permite que imagens de n-Channel tenham dados de mistura alfa semelhantes aos modelos de cores RGB/BGR e CMYK. O canal alfa está localizado imediatamente após o canal da última cor no fluxo de bits sequencial de um bitmap.

### <a name="indexed-and-grayscale-color-models"></a>Modelos de cores indexadas e em escala de cinza

Os formatos *indexados* usam uma tabela de cores, chamada de *paleta*. A paleta é armazenada externamente nos dados de pixel ou mais definida implicitamente. O valor de cada pixel na imagem é um índice na paleta. Com um formato indexado, o número de bits por pixel está diretamente relacionado ao número de entradas na paleta. Isso reduz significativamente a quantidade de dados necessários para representar a imagem, mas também restringe o número de cores disponíveis para a imagem. O WIC dá suporte a formatos indexados com 1, 2, 4 ou 8 bpp.

Para formatos monocromáticos (tons de cinza), o WIC dá suporte a 1, 2, 4, 8, 16 e 32 bits por pixel. Para as profundidades de bits de 1, 8, 16 e 32, os dados de cor são armazenados em um único canal. Para as profundidades de bits de 2 ou 4, os pixels são índices em uma paleta de tons de cinza.

### <a name="ycbcr-color-model"></a>Modelo de cores Y'CbCr

O WIC adiciona suporte para o modelo de cores JPEG JFIF Y'CbCr. Y'CbCr separar as cores em um componente Luma (Y) e dois componentes croma (CB e CR). Muitos arquivos JPEG armazenam nativamente dados de imagem usando o modelo de cores Y'CbCr.

O sistema visual humano é menos sensível a alterações em croma do que Luma, e os formatos Y'CbCr podem aproveitar essa sensibilidade reduzida reduzindo a quantidade de dados croma armazenados em relação a Luma. Eles realizam isso armazenando croma e Luma em planos separados e dimensionando cada plano de componente para uma resolução diferente. Essa prática é conhecida como subamostragem croma.

Como os dados croma e Luma são armazenados separadamente e podem ser resoluções diferentes, o WIC define formatos separados de pixel Luma e croma. O WIC dá suporte a dados que são de 8 bits por canal.

## <a name="wic-pixel-format"></a>Formato de pixel do WIC

Os formatos de pixel no WIC são definidos usando GUIDs para evitar conflitos com os IHVs. O WIC fornece um nome amigável para fazer referência ao GUID de um formato de pixel nativo. A Convenção de nomenclatura para os formatos de pixel do WIC é a seguinte:

**\[GUID \_ WICPixelFormat \] \[ bits por \] \[ \] tipo de armazenamento de ordem de canal de pixel \[\]**

| Componente de formato         | Descrição                                                                                                                                                                                                                                                                                                  |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_WICPIXELFORMAT GUID** | A identificação descritiva para todos os formatos de pixel do WIC. O nome amigável para todos os pixels de WIC começa com esta cadeia de caracteres.                                                                                                                                                                                       |
| **Bits por Pixel**       | O número de bits por pixel (BPP) usado para o formato de pixel.                                                                                                                                                                                                                                                |
| **Ordem do canal**        | O modelo de canal de cor e a ordem de cada canal para o formato.                                                                                                                                                                                                                                            |
| **Tipo de armazenamento**         | A codificação numérica usada para o formato de pixel. A codificação padrão é um inteiro sem sinal. Se nada seguir as informações do modelo de cor, um inteiro não assinado (UINT) é implícito. FixedPoint e float são usados para identificar formatos de pixel que usam codificação de ponto fixo e ponto flutuante, respectivamente. |



 

> [!Note]  
> Para formatos de n-Channel, a \[ ordem de canal não \] especifica a ordem de cor, mas sim o número de canais disponíveis. Por exemplo, o GUID \_ WICPixelFormat24bpp3Channels fornece 3 canais de cor em que "3Channels" é a \[ entrada de ordem de canal \] , mas indica apenas o número de canais e não o pedido.

 

Por exemplo, o GUID do nome amigável \_ WICPixelFormat24bppRGB significa que o formato de pixel usa 24 bits por pixel e o modelo de cor RGB. Como o nome não identifica explicitamente um tipo de armazenamento, um inteiro sem sinal é implícito.

O WIC dá suporte a vários formatos de pixel. As tabelas a seguir agrupam formatos de pixel semelhantes por estrutura de cores e fornecem informações adicionais, como profundidade de bits, bits por pixel e codificação numérica. Cada tabela contém as seguintes informações:

-   **Nome amigável**. O nome amigável do formato de pixel.
-   **Contagem de canais**. O número de canais de cores.
-   **Bits por canal**. O número de bits por canal (profundidade de bits).
-   **Bits por pixel**. O número de bits por pixel, incluindo quaisquer bits de preenchimento.
-   **Tipo de armazenamento**. A codificação numérica dos dados da imagem. Esse valor pode ser um inteiro não assinado (UINT), um número de ponto fixo (FixedPoint) ou um número de ponto flutuante (float).

> [!Note]  
> Para maior clareza, este documento se refere a formatos de pixel somente por seus nomes amigáveis. O valor hexadecimal real para os formatos de pixel pode ser encontrado nos arquivos wincodec. h/IDL.

 

### <a name="undefined-pixel-formats"></a>Formatos de pixel indefinidos

A lista a seguir mostra formatos de pixel genéricos que são usados quando o formato de pixel é indefinido ou não é importante para uma operação de imagem.

-   \_WICPIXELFORMATUNDEFINED GUID
-   \_WICPIXELFORMATDONTCARE GUID

### <a name="indexed-pixel-formats"></a>Formatos de pixel indexados

A tabela a seguir lista os formatos de pixel indexados fornecidos pelo WIC. Nesses formatos, o valor de cada pixel é um índice em uma paleta de cores.



| Nome amigável                   | Contagem de canais | Bits por Pixel | Tipo de armazenamento |
|---------------------------------|---------------|----------------|--------------|
| \_WICPIXELFORMAT1BPPINDEXED GUID | 1             | 1              | UINT         |
| \_WICPIXELFORMAT2BPPINDEXED GUID | 1             | 2              | UINT         |
| \_WICPIXELFORMAT4BPPINDEXED GUID | 1             | 4              | UINT         |
| \_WICPIXELFORMAT8BPPINDEXED GUID | 1             | 8              | UINT         |



 

### <a name="packed-bit-pixel-formats"></a>Formatos de pixel de bit empacotado

A tabela a seguir lista os formatos de bits empacotados fornecidos pelo WIC. Nesses formatos, os dados do canal de cor não são alinhados em byte.



| Nome amigável                          | Contagem de canais | Bits por canal       | Bits por Pixel | Tipo de armazenamento |
|-------------------------------------------|---------------|------------------------|----------------|--------------|
| \_WICPIXELFORMAT16BPPBGR555 GUID           | 3             | 5                      | 16             | UINT         |
| \_WICPIXELFORMAT16BPPBGR565 GUID           | 3             | 5 (B)/6 (G)/5 (R)         | 16             | UINT         |
| \_WICPIXELFORMAT16BPPBGRA555 GUID          | 4             | 5 (B)/5 (G)/5 (R)/1 (A)    | 16             | UINT         |
| \_WICPIXELFORMAT32BPPBGR101010 GUID        | 3             | 10                     | 32             | UINT         |
| \_WICPIXELFORMAT32BPPRGBA1010102 GUID      | 4             | 10 (R)/10 (G)/10 (B)/2 (A) | 32             | UINT         |
| \_WICPIXELFORMAT32BPPRGBA1010102XR GUID    | 4             | 10 (R)/10 (G)/10 (B)/2 (A) | 32             | UINT         |
| \_WICPIXELFORMAT32BPPR10G10B10A2 GUID      | 4             | 10 (R)/10 (G)/10 (B)/2 (A) | 32             | UINT         |
| \_WICPIXELFORMAT32BPPR10G10B10A2HDR10 GUID | 4             | 10 (R)/10 (G)/10 (B)/2 (A) | 32             | UINT         |

Para os \_ formatos GUID WICPixelFormat32bppBGR101010 e GUID \_ WICPixelFormat32bppRGBA1010102, o canal vermelho é armazenado nos bits menos significativos. Para os \_ formatos GUID WICPixelFormat32bppR10G10B10A2 e GUID \_ WICPixelFormat32bppR10G10B10A2HDR10, o canal vermelho é definido nos bits mais significativos, o mesmo layout que [DXGI_FORMAT_R10G10B10A2_UNORM](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).

O \_ formato GUID WICPixelFormat32bppR10G10B10A2HDR10 é o formato de pixel de 10 bits para HDR10 (BT. 2020 de espaço de cores e SMPTE St. 2084 EOTF).

### <a name="grayscale-pixel-formats"></a>Formatos de pixel em escala de cinza

A tabela a seguir lista os formatos em escala de cinza fornecidos pelo WIC. Nesses formatos, os dados de cor representam tons de cinza.



| Nome amigável                           | Contagem de canais | Bits por canal | Bits por Pixel | Tipo de armazenamento |
|-----------------------------------------|---------------|------------------|----------------|--------------|
| \_WICPIXELFORMATBLACKWHITE GUID          | 1             | 1                | 1              | UINT         |
| \_WICPIXELFORMAT2BPPGRAY GUID            | 1             | 2                | 2              | UINT         |
| \_WICPIXELFORMAT4BPPGRAY GUID            | 1             | 4                | 4              | UINT         |
| \_WICPIXELFORMAT8BPPGRAY GUID            | 1             | 8                | 8              | UINT         |
| \_WICPIXELFORMAT16BPPGRAY GUID           | 1             | 16               | 16             | UINT         |
| \_WICPIXELFORMAT16BPPGRAYFIXEDPOINT GUID | 1             | 16               | 16             | FixedPoint   |
| \_WICPIXELFORMAT16BPPGRAYHALF GUID       | 1             | 16               | 16             | Float        |
| \_WICPIXELFORMAT32BPPGRAYFLOAT GUID      | 1             | 32               | 32             | Float        |
| \_WICPIXELFORMAT32BPPGRAYFIXEDPOINT GUID | 1             | 32               | 32             | FixedPoint   |



 

### <a name="rgbbgr-pixel-formats"></a>Formatos de pixel RGB/BGR

A tabela a seguir lista os formatos RGB/BGR fornecidos pelo WIC. Esses formatos separam os dados de cores primários em canais vermelho (R), verde (G) e azul (B). Um canal alfa (A) adicional é fornecido para informações de opacidade em alguns formatos.



| Nome amigável                            | Contagem de canais | Bits por canal | Bits por Pixel | Tipo de armazenamento |
|------------------------------------------|---------------|------------------|----------------|--------------|
| \_WICPIXELFORMAT24BPPRGB GUID             | 3             | 8                | 24             | UINT         |
| \_WICPIXELFORMAT24BPPBGR GUID             | 3             | 8                | 24             | UINT         |
| \_WICPIXELFORMAT32BPPBGR GUID             | 3             | 8                | 32             | UINT         |
| \_WICPIXELFORMAT32BPPRGBA GUID            | 4             | 8                | 32             | UINT         |
| \_WICPIXELFORMAT32BPPBGRA GUID            | 4             | 8                | 32             | UINT         |
| \_WICPIXELFORMAT32BPPRGBE GUID\*          | 4             | 8                | 32             | Float        |
| \_WICPIXELFORMAT32BPPPRGBA GUID           | 4             | 8                | 32             | UINT         |
| \_WICPIXELFORMAT32BPPPBGRA GUID           | 4             | 8                | 32             | UINT         |
| \_WICPIXELFORMAT48BPPRGB GUID             | 3             | 16               | 48             | UINT         |
| \_WICPIXELFORMAT48BPPBGR GUID             | 3             | 16               | 48             | UINT         |
| \_WICPIXELFORMAT48BPPRGBFIXEDPOINT GUID   | 3             | 16               | 48             | Fixo        |
| \_WICPIXELFORMAT48BPPBGRFIXEDPOINT GUID   | 3             | 16               | 48             | Fixo        |
| \_WICPIXELFORMAT48BPPRGBHALF GUID         | 3             | 16               | 48             | Float        |
| \_WICPIXELFORMAT64BPPRGBA GUID            | 4             | 16               | 64             | UINT         |
| \_WICPIXELFORMAT64BPPBGRA GUID            | 4             | 16               | 64             | UINT         |
| \_WICPIXELFORMAT64BPPPRGBA GUID           | 4             | 16               | 64             | UINT         |
| \_WICPIXELFORMAT64BPPPBGRA GUID           | 4             | 16               | 64             | UINT         |
| \_WICPIXELFORMAT64BPPRGBFIXEDPOINT GUID   | 3             | 16               | 64             | Fixo        |
| \_WICPIXELFORMAT64BPPRGBAFIXEDPOINT GUID  | 4             | 16               | 64             | Fixo        |
| \_WICPIXELFORMAT64BPPBGRAFIXEDPOINT GUID  | 4             | 16               | 64             | Fixo        |
| \_WICPIXELFORMAT64BPPRGBHALF GUID         | 3             | 16               | 64             | Float        |
| \_WICPIXELFORMAT64BPPRGBAHALF GUID        | 4             | 16               | 64             | Float        |
| \_WICPIXELFORMAT96BPPRGBFIXEDPOINT GUID   | 3             | 32               | 96             | Fixo        |
| \_WICPIXELFORMAT128BPPRGBFLOAT GUID       | 3             | 32               | 128            | Float        |
| \_WICPIXELFORMAT128BPPRGBAFLOAT GUID      | 4             | 32               | 128            | Float        |
| \_WICPIXELFORMAT128BPPPRGBAFLOAT GUID     | 4             | 32               | 128            | Float        |
| \_WICPIXELFORMAT128BPPRGBFIXEDPOINT GUID  | 3             | 32               | 128            | Fixo        |
| \_WICPIXELFORMAT128BPPRGBAFIXEDPOINT GUID | 4             | 32               | 128            | Fixo        |



 

> [!Note]  
> \*O \_ formato GUID WICPixelFormat32bppRGBE codifica valores de ponto flutuante de 3 16 bits em 4 bytes, da seguinte maneira: três mantissas de 8 bits não assinados para os canais R, G e B, além de um expoente de 8 bits compartilhado. Esse formato fornece precisão de ponto flutuante de 16 bits em uma representação de pixel menor.

 

A partir do Windows 8 e da [atualização de plataforma para o Windows 7](/windows/desktop/direct3darticles/platform-update-for-windows-7), o WIC fornece formatos adicionais, mostrados na tabela aqui.



| Nome amigável                      | Contagem de canais | Bits por canal | Bits por Pixel | Tipo de armazenamento |
|------------------------------------|---------------|------------------|----------------|--------------|
| \_WICPIXELFORMAT32BPPRGB GUID       | 3             | 8                | 32             | UINT         |
| \_WICPIXELFORMAT64BPPRGB GUID       | 3             | 16               | 64             | UINT         |
| \_WICPIXELFORMAT96BPPRGBFLOAT GUID  | 3             | 32               | 96             | FLOAT        |
| \_WICPIXELFORMAT64BPPPRGBAHALF GUID | 4             | 16               | 64             | FLOAT        |



 

### <a name="cmyk-pixel-formats"></a>Formatos de pixel CMYK

A tabela a seguir lista os formatos CMYK fornecidos pelo WIC. Esses formatos separam os dados de cores primárias em canais ciano (C), magenta (M), amarelo (Y) e preto (K).



| Nome amigável                      | Contagem de canais | Bits por canal | Bits por Pixel | Tipo de armazenamento |
|------------------------------------|---------------|------------------|----------------|--------------|
| \_WICPIXELFORMAT32BPPCMYK GUID      | 4             | 8                | 32             | UINT         |
| \_WICPIXELFORMAT64BPPCMYK GUID      | 4             | 16               | 64             | UINT         |
| \_WICPIXELFORMAT40BPPCMYKALPHA GUID | 5             | 8                | 40             | UINT         |
| \_WICPIXELFORMAT80BPPCMYKALPHA GUID | 5             | 16               | 80             | UINT         |



 

### <a name="n-channel-pixel-formats"></a>Formatos de pixel de n-Channel

A tabela a seguir lista os formatos de n-Channel fornecidos pelo WIC. Esses formatos fornecem uma série de canais de cores indefinidos para armazenar dados de imagem.



| Nome amigável                            | Contagem de canais | Bits por canal | Bits por Pixel | Tipo de armazenamento |
|------------------------------------------|---------------|------------------|----------------|--------------|
| \_WICPIXELFORMAT24BPP3CHANNELS GUID       | 3             | 8                | 24             | UINT         |
| \_WICPIXELFORMAT48BPP3CHANNELS GUID       | 3             | 16               | 48             | UINT         |
| \_WICPIXELFORMAT32BPP3CHANNELSALPHA GUID  | 4             | 8                | 32             | UINT         |
| \_WICPIXELFORMAT64BPP3CHANNELSALPHA GUID  | 4             | 16               | 64             | UINT         |
| \_WICPIXELFORMAT32BPP4CHANNELS GUID       | 4             | 8                | 32             | UINT         |
| \_WICPIXELFORMAT64BPP4CHANNELS GUID       | 4             | 16               | 64             | UINT         |
| \_WICPIXELFORMAT40BPP4CHANNELSALPHA GUID  | 5             | 8                | 40             | UINT         |
| \_WICPIXELFORMAT80BPP4CHANNELSALPHA GUID  | 5             | 16               | 80             | UINT         |
| \_WICPIXELFORMAT40BPP5CHANNELS GUID       | 5             | 8                | 40             | UINT         |
| \_WICPIXELFORMAT80BPP5CHANNELS GUID       | 5             | 16               | 80             | UINT         |
| \_WICPIXELFORMAT48BPP5CHANNELSALPHA GUID  | 6             | 8                | 48             | UINT         |
| \_WICPIXELFORMAT96BPP5CHANNELSALPHA GUID  | 6             | 16               | 96             | UINT         |
| \_WICPIXELFORMAT48BPP6CHANNELS GUID       | 6             | 8                | 48             | UINT         |
| \_WICPIXELFORMAT96BPP6CHANNELS GUID       | 6             | 16               | 96             | UINT         |
| \_WICPIXELFORMAT56BPP6CHANNELSALPHA GUID  | 7             | 8                | 56             | UINT         |
| \_WICPIXELFORMAT112BPP6CHANNELSALPHA GUID | 7             | 16               | 112            | UINT         |
| \_WICPIXELFORMAT56BPP7CHANNELS GUID       | 7             | 8                | 56             | UINT         |
| \_WICPIXELFORMAT112BPP7CHANNELS GUID      | 7             | 16               | 112            | UINT         |
| \_WICPIXELFORMAT64BPP7CHANNELSALPHA GUID  | 8             | 8                | 64             | UINT         |
| \_WICPIXELFORMAT128BPP7CHANNELSALPHA GUID | 8             | 16               | 128            | UINT         |
| \_WICPIXELFORMAT64BPP8CHANNELS GUID       | 8             | 8                | 64             | UINT         |
| \_WICPIXELFORMAT128BPP8CHANNELS GUID      | 8             | 16               | 128            | UINT         |
| \_WICPIXELFORMAT72BPP8CHANNELSALPHA GUID  | 9             | 8                | 72             | UINT         |
| \_WICPIXELFORMAT144BPP8CHANNELSALPHA GUID | 9             | 16               | 144            | UINT         |



 

### <a name="alpha-only-pixel-formats"></a>Apenas formatos de pixel alfa

A tabela a seguir lista os formatos somente alfa fornecidos pelo WIC. Este formato contém apenas informações alfa.



| Nome amigável                 | Contagem de canais | Bits por canal | Bits por Pixel | Tipo de armazenamento |
|-------------------------------|---------------|------------------|----------------|--------------|
| \_WICPIXELFORMAT8BPPALPHA GUID | 1             | 8                | 32             | UINT         |



 

### <a name="ycbcr-pixel-formats"></a>Formatos de pixel Y'CbCr

A tabela a seguir lista os formatos Y'CbCr fornecidos pelo WIC. Esses formatos separam os dados de cor primários em Luma (Y), croma (azul-escuro) e a CR (Red Choma difference). Observe que esses formatos são projetados para armazenar dados JPEG JFIF Y'CbCr pixel.



| Nome amigável                 | Contagem de canais | Bits por Pixel | Tipo de armazenamento |
|-------------------------------|---------------|----------------|--------------|
| \_WICPIXELFORMAT8BPPY GUID     | 1             | 8              | UINT         |
| \_WICPIXELFORMAT8BPPCB GUID    | 1             | 8              | UINT         |
| \_WICPIXELFORMAT8BPPCR GUID    | 1             | 8              | UINT         |
| \_WICPIXELFORMAT16BPPCBCR GUID | 2             | 16             | UINT         |



 

## <a name="color-space"></a>Espaço de cores

Os formatos de pixel em si não têm um espaço de cores. Geralmente, o espaço de cores é uma interpretação semântica dos valores de pixel que depende do contexto do bitmap. Algumas imagens identificam um contexto de cor que define o espaço de cores da imagem. Somente na ausência de um contexto de cor, o espaço de cores deve ser inferido.

As informações de contexto de cor são definidas pela interface [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) para o WIC. Para recuperar as informações de contexto de cor de um quadro de imagem, use o método **GetColorContext** .

Na ausência de informações de espaço de cores para uma imagem, a regra geral para a inferência de espaço de cores é que os formatos de RGB e tons de cinza UINT usam o padrão de cores RGB (sRGB), enquanto os formatos RGB e tons de cinza e de ponto flutuante usam o scRGB (espaço de cores RGB estendido). O modelo de cores CMYK usa um espaço de cores RWOP.

## <a name="native-image-formats"></a>Formatos de imagem nativa

Cada um dos codecs do WIC fornecidos pelo Windows dá suporte a um subconjunto dos formatos de pixel do WIC. Para cada codec, os formatos de decodificação com suporte podem ser diferentes dos formatos de codificação com suporte.

Ao decodificar uma imagem, se os dados forem armazenados nativamente em um formato de pixel que não é suportado pelo decodificador, ele será convertido em um formato com suporte. Para determinar o formato de pixel de saída, chame [**IWICBitmapFrameDecode:: GetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getpixelformat).

Ao codificar uma imagem, use [**IWICBitmapFrameEncode:: SetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setpixelformat) para solicitar que o codificador use um formato de pixel específico. O codificador retornará o formato de pixel com suporte mais próximo, que pode ser diferente do que foi solicitado.

As tabelas a seguir mostram os formatos de pixel com suporte de cada um dos codecs do WIC fornecidos pelo Windows.

### <a name="bmp-native-codec"></a>Codec nativo BMP



| Formatos de pixel do decodificador                   | Formatos de pixel do codificador                   |
|-----------------------------------------|-----------------------------------------|
| \_WICPIXELFORMAT1BPPINDEXED GUID         | \_WICPIXELFORMAT1BPPINDEXED GUID         |
| \_WICPIXELFORMAT4BPPINDEXED GUID         | \_WICPIXELFORMAT4BPPINDEXED GUID         |
| \_WICPIXELFORMAT8BPPINDEXED GUID         | \_WICPIXELFORMAT8BPPINDEXED GUID         |
| \_WICPIXELFORMAT16BPPBGR555 GUID         | \_WICPIXELFORMAT16BPPBGR555 GUID         |
| \_WICPIXELFORMAT16BPPBGR565 GUID         | \_WICPIXELFORMAT16BPPBGR565 GUID         |
| \_WICPIXELFORMAT24BPPBGR GUID            | \_WICPIXELFORMAT24BPPBGR GUID            |
| \_WICPIXELFORMAT32BPPBGR GUID            | \_WICPIXELFORMAT32BPPBGR GUID            |
| \_WICPIXELFORMAT32BPPBGRA GUID\*         | \_WICPIXELFORMAT32BPPBGRA GUID\*         |
| \_WICPIXELFORMAT64BPPRGBAFIXEDPOINT GUID | \_WICPIXELFORMAT32BPPPBGRA GUID          |
|                                         | \_WICPIXELFORMAT64BPPRGBAFIXEDPOINT GUID |
|                                         | \_WICPIXELFORMAT64BPPBGRAFIXEDPOINT GUID |



 

> [!Note]  
> \_O GUID WICPixelFormat32bppBGRA só tem suporte no Windows 8, a [atualização de plataforma para o Windows 7](/windows/desktop/direct3darticles/platform-update-for-windows-7)e superior.
>
> -   Para codificar nesse formato, use a opção de codificador **EnableV5Header32bppBGRA** . O BMP será gravado com um cabeçalho BITMAPV5HEADER.
> -   Se um arquivo tiver um BITMAPV5HEADER, ele decodificará como GUID \_ WICPixelFormat32bppBGRA.

 

### <a name="gif-native-codec"></a>Codec nativo GIF



| Formatos de pixel do decodificador           | Formatos de pixel do codificador           |
|---------------------------------|---------------------------------|
| \_WICPIXELFORMAT8BPPINDEXED GUID | \_WICPIXELFORMAT8BPPINDEXED GUID |



 

### <a name="ico-native-codec"></a>Codec nativo da ICO



| Formatos de pixel do decodificador         | Formatos de pixel do codificador |
|-------------------------------|-----------------------|
| \_WICPIXELFORMAT32BPPBGRA GUID |                       |



 

### <a name="jpeg-native-codec"></a>Codec nativo JPEG



| Formatos de pixel do decodificador         | Formatos de pixel do codificador         |
|-------------------------------|-------------------------------|
| \_WICPIXELFORMAT8BPPGRAY GUID  | \_WICPIXELFORMAT8BPPGRAY GUID  |
| \_WICPIXELFORMAT24BPPBGR GUID  | \_WICPIXELFORMAT24BPPBGR GUID  |
| \_WICPIXELFORMAT32BPPCMYK GUID | \_WICPIXELFORMAT32BPPCMYK GUID |



 

### <a name="png-native-codec"></a>Codec nativo do PNG



| Formatos de pixel do decodificador           | Formatos de pixel do codificador           |
|---------------------------------|---------------------------------|
| \_WICPIXELFORMAT1BPPINDEXED GUID | \_WICPIXELFORMAT1BPPINDEXED GUID |
| \_WICPIXELFORMAT2BPPINDEXED GUID | \_WICPIXELFORMAT2BPPINDEXED GUID |
| \_WICPIXELFORMAT4BPPINDEXED GUID | \_WICPIXELFORMAT4BPPINDEXED GUID |
| \_WICPIXELFORMAT8BPPINDEXED GUID | \_WICPIXELFORMAT8BPPINDEXED GUID |
| \_WICPIXELFORMATBLACKWHITE GUID  | \_WICPIXELFORMATBLACKWHITE GUID  |
| \_WICPIXELFORMAT2BPPGRAY GUID    | \_WICPIXELFORMAT2BPPGRAY GUID    |
| \_WICPIXELFORMAT4BPPGRAY GUID    | \_WICPIXELFORMAT4BPPGRAY GUID    |
| \_WICPIXELFORMAT8BPPGRAY GUID    | \_WICPIXELFORMAT8BPPGRAY GUID    |
| \_WICPIXELFORMAT16BPPGRAY GUID   | \_WICPIXELFORMAT16BPPGRAY GUID   |
| \_WICPIXELFORMAT24BPPBGR GUID    | \_WICPIXELFORMAT24BPPBGR GUID    |
| \_WICPIXELFORMAT32BPPBGRA GUID   | \_WICPIXELFORMAT32BPPBGRA GUID   |
| \_WICPIXELFORMAT48BPPRGB GUID    | \_WICPIXELFORMAT48BPPRGB GUID    |
| \_WICPIXELFORMAT64BPPRGBA GUID   | \_WICPIXELFORMAT48BPPBGR GUID    |
|                                 | \_WICPIXELFORMAT64BPPRGBA GUID   |
|                                 | \_WICPIXELFORMAT64BPPBGRA GUID   |



 

### <a name="tiff-native-codec"></a>Codec nativo TIFF



| Formatos de pixel do decodificador                | Formatos de pixel do codificador           |
|--------------------------------------|---------------------------------|
| \_WICPIXELFORMAT1BPPINDEXED GUID      | \_WICPIXELFORMAT1BPPINDEXED GUID |
| \_WICPIXELFORMAT4BPPINDEXED GUID      | \_WICPIXELFORMAT4BPPINDEXED GUID |
| \_WICPIXELFORMAT8BPPINDEXED GUID      | \_WICPIXELFORMAT8BPPINDEXED GUID |
| \_WICPIXELFORMATBLACKWHITE GUID       | \_WICPIXELFORMATBLACKWHITE GUID  |
| \_WICPIXELFORMAT4BPPGRAY GUID         | \_WICPIXELFORMAT4BPPGRAY GUID    |
| \_WICPIXELFORMAT8BPPGRAY GUID         | \_WICPIXELFORMAT8BPPGRAY GUID    |
| \_WICPIXELFORMAT16BPPGRAY GUID        | \_WICPIXELFORMAT16BPPGRAY GUID   |
| \_WICPIXELFORMAT32BPPGRAYFLOAT GUID   | \_WICPIXELFORMAT24BPPBGR GUID    |
| \_WICPIXELFORMAT24BPPBGR GUID         | \_WICPIXELFORMAT32BPPBGRA GUID   |
| \_WICPIXELFORMAT32BPPBGRA GUID        | \_WICPIXELFORMAT32BPPCMYK GUID   |
| \_WICPIXELFORMAT32BPPPBGRA GUID       | \_WICPIXELFORMAT48BPPRGB GUID    |
| \_WICPIXELFORMAT48BPPRGB GUID         | \_WICPIXELFORMAT64BPPRGBA GUID   |
| \_WICPIXELFORMAT32BPPCMYK GUID        |                                 |
| \_WICPIXELFORMAT40BPPCMYKALPHA GUID   |                                 |
| \_WICPIXELFORMAT64BPPRGBA GUID        |                                 |
| \_WICPIXELFORMAT64BPPPRGBA GUID       |                                 |
| \_WICPIXELFORMAT64BPPCMYK GUID        |                                 |
| \_WICPIXELFORMAT80BPPCMYKALPHA GUID   |                                 |
| \_WICPIXELFORMAT96BPPRGBFLOAT GUID\*  |                                 |
| \_WICPIXELFORMAT128BPPRGBAFLOAT GUID  |                                 |
| \_WICPIXELFORMAT128BPPPRGBAFLOAT GUID |                                 |



 

> [!Note]  
> \_O GUID WICPixelFormat96bppRGBFloat só tem suporte no Windows 8, a [atualização de plataforma para o Windows 7](/windows/desktop/direct3darticles/platform-update-for-windows-7)e superior.

 

### <a name="jpeg-xr-native-codec"></a>Codec de JPEG-XR Native



| Formatos de pixel do decodificador                    | Formatos de pixel do codificador                    |
|------------------------------------------|------------------------------------------|
| \_WICPIXELFORMATBLACKWHITE GUID           | \_WICPIXELFORMATBLACKWHITE GUID           |
| \_WICPIXELFORMAT8BPPGRAY GUID             | \_WICPIXELFORMAT8BPPGRAY GUID             |
| \_WICPIXELFORMAT16BPPBGR555 GUID          | \_WICPIXELFORMAT16BPPBGR555 GUID          |
| \_WICPIXELFORMAT16BPPGRAY GUID            | \_WICPIXELFORMAT16BPPGRAY GUID            |
| \_WICPIXELFORMAT24BPPBGR GUID             | \_WICPIXELFORMAT24BPPBGR GUID             |
| \_WICPIXELFORMAT24BPPRGB GUID             | \_WICPIXELFORMAT24BPPRGB GUID             |
| \_WICPIXELFORMAT32BPPBGR GUID             | \_WICPIXELFORMAT32BPPBGR GUID             |
| \_WICPIXELFORMAT32BPPBGRA GUID            | \_WICPIXELFORMAT32BPPBGRA GUID            |
| \_WICPIXELFORMAT48BPPRGBFIXEDPOINT GUID   | \_WICPIXELFORMAT48BPPRGBFIXEDPOINT GUID   |
| \_WICPIXELFORMAT16BPPGRAYFIXEDPOINT GUID  | \_WICPIXELFORMAT16BPPGRAYFIXEDPOINT GUID  |
| \_WICPIXELFORMAT32BPPBGR101010 GUID       | \_WICPIXELFORMAT32BPPBGR101010 GUID       |
| \_WICPIXELFORMAT48BPPRGB GUID             | \_WICPIXELFORMAT48BPPRGB GUID             |
| \_WICPIXELFORMAT64BPPRGBA GUID            | \_WICPIXELFORMAT64BPPRGBA GUID            |
| \_WICPIXELFORMAT96BPPRGBFIXEDPOINT GUID   | \_WICPIXELFORMAT96BPPRGBFIXEDPOINT GUID   |
| \_WICPIXELFORMAT96BPPRGBFIXEDPOINT GUID   | \_WICPIXELFORMAT128BPPRGBAFLOAT GUID      |
| \_WICPIXELFORMAT128BPPRGBFLOAT GUID       | \_WICPIXELFORMAT128BPPRGBFLOAT GUID       |
| \_WICPIXELFORMAT32BPPCMYK GUID            | \_WICPIXELFORMAT32BPPCMYK GUID            |
| \_WICPIXELFORMAT64BPPRGBAFIXEDPOINT GUID  | \_WICPIXELFORMAT64BPPRGBAFIXEDPOINT GUID  |
| \_WICPIXELFORMAT128BPPRGBAFIXEDPOINT GUID | \_WICPIXELFORMAT128BPPRGBAFIXEDPOINT GUID |
| \_WICPIXELFORMAT64BPPCMYK GUID            | \_WICPIXELFORMAT64BPPCMYK GUID            |
| \_WICPIXELFORMAT24BPP3CHANNELS GUID       | \_WICPIXELFORMAT24BPP3CHANNELS GUID       |
| \_WICPIXELFORMAT32BPP4CHANNELS GUID       | \_WICPIXELFORMAT32BPP4CHANNELS GUID       |
| \_WICPIXELFORMAT40BPP5CHANNELS GUID       | \_WICPIXELFORMAT40BPP5CHANNELS GUID       |
| \_WICPIXELFORMAT48BPP6CHANNELS GUID       | \_WICPIXELFORMAT48BPP6CHANNELS GUID       |
| \_WICPIXELFORMAT56BPP7CHANNELS GUID       | \_WICPIXELFORMAT56BPP7CHANNELS GUID       |
| \_WICPIXELFORMAT64BPP8CHANNELS GUID       | \_WICPIXELFORMAT64BPP8CHANNELS GUID       |
| \_WICPIXELFORMAT48BPP3CHANNELS GUID       | \_WICPIXELFORMAT48BPP3CHANNELS GUID       |
| \_WICPIXELFORMAT64BPP4CHANNELS GUID       | \_WICPIXELFORMAT64BPP4CHANNELS GUID       |
| \_WICPIXELFORMAT80BPP5CHANNELS GUID       | \_WICPIXELFORMAT80BPP5CHANNELS GUID       |
| \_WICPIXELFORMAT96BPP6CHANNELS GUID       | \_WICPIXELFORMAT96BPP6CHANNELS GUID       |
| \_WICPIXELFORMAT112BPP7CHANNELS GUID      | \_WICPIXELFORMAT112BPP7CHANNELS GUID      |
| \_WICPIXELFORMAT128BPP8CHANNELS GUID      | \_WICPIXELFORMAT128BPP8CHANNELS GUID      |
| \_WICPIXELFORMAT40BPPCMYKALPHA GUID       | \_WICPIXELFORMAT40BPPCMYKALPHA GUID       |
| \_WICPIXELFORMAT80BPPCMYKALPHA GUID       | \_WICPIXELFORMAT80BPPCMYKALPHA GUID       |
| \_WICPIXELFORMAT32BPP3CHANNELSALPHA GUID  | \_WICPIXELFORMAT32BPP3CHANNELSALPHA GUID  |
| \_WICPIXELFORMAT64BPP7CHANNELSALPHA GUID  | \_WICPIXELFORMAT40BPP4CHANNELSALPHA GUID  |
| \_WICPIXELFORMAT72BPP8CHANNELSALPHA GUID  | \_WICPIXELFORMAT48BPP5CHANNELSALPHA GUID  |
| \_WICPIXELFORMAT64BPP3CHANNELSALPHA GUID  | \_WICPIXELFORMAT56BPP6CHANNELSALPHA GUID  |
| \_WICPIXELFORMAT80BPP4CHANNELSALPHA GUID  | \_WICPIXELFORMAT64BPP7CHANNELSALPHA GUID  |
| \_WICPIXELFORMAT96BPP5CHANNELSALPHA GUID  | \_WICPIXELFORMAT72BPP8CHANNELSALPHA GUID  |
| \_WICPIXELFORMAT112BPP6CHANNELSALPHA GUID | \_WICPIXELFORMAT64BPP3CHANNELSALPHA GUID  |
| \_WICPIXELFORMAT128BPP7CHANNELSALPHA GUID | \_WICPIXELFORMAT80BPP4CHANNELSALPHA GUID  |
| \_WICPIXELFORMAT144BPP8CHANNELSALPHA GUID | \_WICPIXELFORMAT96BPP5CHANNELSALPHA GUID  |
| \_WICPIXELFORMAT64BPPRGBAHALF GUID        | \_WICPIXELFORMAT112BPP6CHANNELSALPHA GUID |
| \_WICPIXELFORMAT48BPPRGBHALF GUID         | \_WICPIXELFORMAT128BPP7CHANNELSALPHA GUID |
| \_WICPIXELFORMAT32BPPRGBE GUID            | \_WICPIXELFORMAT144BPP8CHANNELSALPHA GUID |
| \_WICPIXELFORMAT16BPPGRAYHALF GUID        | \_WICPIXELFORMAT64BPPRGBAHALF GUID        |
| \_WICPIXELFORMAT32BPPGRAYFIXEDPOINT GUID  | \_WICPIXELFORMAT48BPPRGBHALF GUID         |
| \_WICPIXELFORMAT64BPPRGBFIXEDPOINT GUID   | \_WICPIXELFORMAT32BPPRGBE GUID            |
| \_WICPIXELFORMAT128BPPRGBFIXEDPOINT GUID  | \_WICPIXELFORMAT16BPPGRAYHALF GUID        |
| \_WICPIXELFORMAT64BPPRGBHALF GUID         | \_WICPIXELFORMATBLACKWHITE GUID           |



 

## <a name="dds-native-codec"></a>Codec do DDS Native



| Formatos de pixel do decodificador          | Formatos de pixel do codificador          |
|--------------------------------|--------------------------------|
| \_WICPIXELFORMAT32BPPBGRA GUID  | \_WICPIXELFORMAT32BPPBGRA GUID  |
| \_WICPIXELFORMAT32BPPPBGRA GUID | \_WICPIXELFORMAT32BPPPBGRA GUID |



 

> [!Note]  
> O codec de DDS do Windows fornecido dá suporte a arquivos DDS codificados usando os seguintes \_ valores de formato DXGI:

 

-   \_Formato dxgi \_ BC1 \_ UNORM
-   \_Formato dxgi \_ BC2 \_ UNORM
-   \_Formato dxgi \_ BC3 \_ UNORM

Eles são decodificados e codificados como GUID \_ WICPixelFormat32bppBGRA ou GUID \_ WICPixelFormat32bppPBGRA. Para obter mais informações, consulte a [visão geral do formato DDS](dds-format-overview.md).

## <a name="pixel-format-extensibility"></a>Extensibilidade de formato de pixel

Os formatos de imagem personalizados podem usar formatos de pixel que não são fornecidos nativamente pelo WIC, como YCbCr (YUV) e YCCK (Y/CB/CR/K). O WIC fornece um modelo de extensibilidade que permite que os formatos de pixel internos e de suplemento funcionem no mesmo pipeline de geração de imagens. Para integrar esses formatos de pixel com o pipeline de geração de imagens do WIC, você deve criar conversores de formato de pixel para converter formatos de pixel de suplemento em um ou mais dos formatos de pixel nativos. A interface principal para a criação de conversores de formato é [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Visão geral do Windows Imaging Component](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[GUIDs e CLSIDs do WIC](-wic-guids-clsids.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[Como escrever um CODEC de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Especificação de foto de HD 1,0](https://www.microsoft.com/whdc/xps/wmphoto.mspx)
</dt> </dl>

 

 
