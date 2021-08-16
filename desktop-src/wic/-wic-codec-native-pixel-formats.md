---
description: Este tópico apresenta os formatos de pixel fornecidos pelo WIC (Windows Imaging Component).
ms.assetid: 348b6d15-e339-4dce-99f3-4d639ee9bf7d
title: Visão geral de formatos de pixel nativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 379e67d422ccbd05ef178e67eb25c973e6b5943ef85d22873097f245f8914a23
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118206332"
---
# <a name="native-pixel-formats-overview"></a>Visão geral de formatos de pixel nativo

Este tópico apresenta os formatos de pixel fornecidos pelo WIC (Windows Imaging Component).

Um formato de pixel descreve o layout de memória de cada pixel em um bitmap. Esse layout de memória descreve como os dados de imagem de um bitmap são codificados especificando o formato numérico e a organização do canal de cores. O WIC dá suporte a vários formatos numéricos para vários esquemas de organização de canal de cores, fornecendo uma ampla variedade de formatos de pixel.

-   [Profundidade de bits](#bit-depth)
-   [Codificação numérica](#numerical-encoding)
-   [Canais de cores](#color-channels)
    -   [Modelo de cor RGB/BGR](#rgbbgr-color-model)
    -   [Modelo de cor do CMYK](#cmyk-color-model)
    -   [Modelo de cores de n canais](#n-channel-color-model)
    -   [Modelos de cores indexados e em escala de cinza](#indexed-and-grayscale-color-models)
    -   [Modelo de cores Y'CbCr](#ycbcr-color-model)
-   [Formato de pixel WIC](#wic-pixel-format)
    -   [Formatos de pixel indefinido](#undefined-pixel-formats)
    -   [Formatos de pixel indexados](#indexed-pixel-formats)
    -   [Formatos de pixel de bits empacotados](#packed-bit-pixel-formats)
    -   [Formatos de pixel em escala de cinza](#grayscale-pixel-formats)
    -   [Formatos de Pixel RGB/BGR](#rgbbgr-pixel-formats)
    -   [Formatos de pixel do CMYK](#cmyk-pixel-formats)
    -   [Formatos de pixel de n canais](#n-channel-pixel-formats)
    -   [Formatos de pixel somente alfa](#alpha-only-pixel-formats)
    -   [Formatos de pixel Y'CbCr](#ycbcr-pixel-formats)
-   [Espaço de cores](#color-space)
-   [Formatos de imagem nativa](#native-image-formats)
    -   [Codec nativo do BMP](#bmp-native-codec)
    -   [Codec nativo gif](#gif-native-codec)
    -   [Codec nativo de ICO](#ico-native-codec)
    -   [JPEG Native Codec](#jpeg-native-codec)
    -   [Codec nativo de PNG](#png-native-codec)
    -   [Codec nativo TIFF](#tiff-native-codec)
    -   [Codec nativo JPEG-XR](#jpeg-xr-native-codec)
-   [Codec nativo do DDS](#dds-native-codec)
-   [Extensibilidade de formato de pixel](#pixel-format-extensibility)
-   [Tópicos relacionados](#related-topics)

## <a name="bit-depth"></a>Profundidade de bits

A *profundidade de bits* é o número de bits usados para codificar cada canal de cor. Atualmente, a maioria das imagens digitais usa uma profundidade de bits de 8, o que significa que cada canal de cor em um pixel é representado por 8 bits, fornecendo 2 (256) valores exclusivos por canal. Uma imagem que tem uma profundidade de bits de 8 e três canais de cores (como vermelho, verde e azul) usa 24 bits por pixel (bpp), que fornece 26.777.216 cores diferentes por pixel.

Para uma melhor resolução de cores, uma profundidade de bits de 16 ou 32 pode ser usada. Isso fornece a cada canal de cores 2 vezes (65.536) ou 2000 valores exclusivos, a um custo de mais memória por pixel.

Em alguns formatos, a profundidade do bit não é um múltiplo de 8. Esses formatos são chamados *de formatos* empacotados, porque os canais de cores em um pixel não estão alinhados aos limites de byte. Por exemplo, se as profundidades de bits de 5, três canais de cores podem ser armazenados em 16 bits (incluindo 1 bit de preenchimento, para fazer com que os pixels sejam alinhados por byte). Formatos empacotados são úteis quando a memória ou a capacidade de processamento são limitadas.

## <a name="numerical-encoding"></a>Codificação numérica

Para a maioria das imagens digitais de hoje, bytes não assinados e inteiros curtos sem sinal são usados para descrever o intervalo numérico de cada canal de cores. O valor mínimo (0) representa a intensidade zero em um único canal de cor e o preto é obtido quando todos os canais de cor são zero. Da mesma forma, o valor máximo representa a intensidade total e o branco é obtido quando todos os canais de cores estão em intensidade total. Em uma profundidade de bits de 8, um UINT fornece 256 valores exclusivos por canal de cores (0 a 255). Uma UINT de 16 bits fornece 65.536 valores exclusivos por canal de cores (0 a 65.535).

Além disso, o WIC dá suporte a formatos de ponto fixo e de ponto flutuante. Esses formatos suportam intervalos dinâmicos maiores, porque todo o intervalo numérico de cada canal de cores é maior que o intervalo visível. Como resultado, as cores podem ser ajustadas acima ou abaixo do intervalo visível, durante as etapas intermediárias do processamento de imagem, sem perda de informações de imagem.

### <a name="fixed-point-numerical-encoding"></a>Fixed-Point codificação numérica

Os valores de ponto fixo de 16 bits são interpretados como s2.13: bit de sinal, dois bits inteiros e 13 bits fracionados. Usando essa interpretação, um intervalo numérico de -4,0 a +3,999... pode ser representado, com o valor de 1,0 representado pelo valor inteiro com sinal 8192 (0x2000).

Os valores de ponto fixo de 32 bits são interpretados como s7.24: bit de sinal, sete bits inteiros e vinte e quatro bits fracionados. Usando essa interpretação, um intervalo numérico de -128,0 a +127,999... pode ser representado, com o valor de 1,0 representado pelo valor inteiro com sinal 16777216 (0x01000000).

## <a name="color-channels"></a>Canais de cores

Os canais de cores de um formato de pixel definem o layout de memória de cada cor dentro dos dados de imagem de um bitmap. Há uma variedade de diferentes estruturas de canal de cores comuns nas imagens digitais de hoje, e o WIC dá suporte a muitas delas.

### <a name="rgbbgr-color-model"></a>Modelo de cor RGB/BGR

Formatos RGB e BGR descrevem cores em um modelo de cor aditiva. O método mais comum de descrever uma imagem é com três canais de cores separados que representam as cores vermelho (R), verde (G) e azul (B). O WIC dá suporte a esses três canais na ordem RGB (vermelho-verde-azul) ou BGR (azul-verde-vermelho). Essa é a ordem na qual cada canal de cor aparece dentro do fluxo de bits sequencial. Por exemplo, no formato \_ WICPixelFormat32bppRGB guid, cada pixel tem 32 bits de largura. O canal vermelho é o primeiro byte (menos significativo) na memória, seguido por verde e, em seguida, azul. Por outro lado, no formato \_ WICPixelFormat32bppBGR guid, os canais de cores estão na ordem oposta. O WIC dá suporte a vários formatos RGB/BGR, incluindo formatos de bits empacotados especiais, como GUID \_ WICPixelFormat16bppBGR555.

> [!Note]  
> Os canais de cores dos formatos de bits especiais empacotados BGR não estão em múltiplos de 8, como os canais de cores em formatos de pixel típicos. Isso significa que os valores de canal não são alinhados por byte. É necessário ter cuidado ao ler canais de cores de bits empacotados.

 

Além dos formatos RGB e BGR, o WIC também fornece formatos de pixel RGB e BGR que suportam um canal alfa (A). O canal alfa fornece dados de opacidade para o pixel. Para formatos com um canal alfa adicionado, o canal alfa geralmente é o último na ordem do canal de cores. Por exemplo, no formato de pixel GUID \_ WICPixelFormat32bppBGRA, a ordem de byte é azul, verde e vermelho, seguido pelo canal alfa.

O WIC também dá suporte a formatos de pixel RGB alfa pré-multiplicados (P). Em um formato de pixel RGBA típico, os valores de cor vermelho, verde e azul são os valores de cor reais para a imagem. Para fazer uma imagem composta no formato RGBA padrão, o valor alfa da imagem em primeiro plano deve ser multiplicado por cada um dos canais vermelho, verde e azul antes de adiá-lo à cor da imagem de plano de fundo. Em um formato de pixel RGB alfa pré-multiplicado, cada canal de cor já foi multiplicado pelo valor alfa. Isso fornece um método mais eficiente de composição de imagem com dados de canal alfa. Para recuperar os true color de cada canal em um formato de pixel PRGBA/PBGRA, a multiplicação de canal alfa deve ser invertida dividindo os valores de cor pelo valor alfa.

### <a name="cmyk-color-model"></a>Modelo de cor do CMYK

O CMYK é um modelo de cor subtrativo usado na impressão. As cores produzidas por um modelo de CMYK são geradas pela luz que não é absorada, mas refletida. O CMYK é um modelo de quatro canais de ciano (C), magenta (M), amarelo (Y) e preto (K). Quando todos os quatro canais de cor estão no valor máximo, o resultado é preto. Assim como os modelos de cores RGB/BGR, a ordem de byte dentro do fluxo de bits sequencial é dada pelo nome do formato de pixel. Por exemplo, no formato de pixel GUID \_ WICPixelFormat32bppCMYK, cada pixel é feito de 32 bits. O primeiro byte contém o valor ciano, seguido, por sua vez, por magenta, amarelo e preto. O WIC fornece formatos de pixel para CMYK em 32 e 64 bits por pixel (bpp).

Além do modelo de cor padrão do CMYK, o WIC também fornece CMYK com alfa. Isso permite que as imagens do CMYK tenham dados de mesclagem alfa semelhantes ao modelo de cor RGB/BGR. O canal alfa está localizado imediatamente após preto no fluxo de bits sequencial de um bitmap.

### <a name="n-channel-color-model"></a>Modelo de cores de n canais

Para flexibilidade, o WIC também fornece formatos de pixel que não têm uma ordem de canal predefinida. O WIC fornece formatos de pixel que suportam de três a oito canais de dados de imagem contínuos em profundidades de bits de 8 e 16. Ao contrário dos formatos de pixel RGB/BGR e CMYK, os formatos de n canais não especificam a ordem do canal, mas o número de canais de cores disponíveis. Por exemplo, no formato de pixel GUID WICPixelFormat32bpp4Channels, cada pixel é feito de 32 bits com cada um dos quatro canais ocupando um único \_ byte.

O WIC também fornece formatos de pixel para n-channel com alfa. Isso permite que imagens de n canais tenham dados de mesclagem alfa semelhantes aos modelos de cores RGB/BGR e CMYK. O canal alfa está localizado imediatamente após o último canal de cor no fluxo de bits sequencial de um bitmap.

### <a name="indexed-and-grayscale-color-models"></a>Modelos de cores indexados e em escala de cinza

*Os formatos* indexados usam uma tabela de cores, chamada *de paleta*. A paleta é armazenada externamente nos dados de pixel ou definida implicitamente. O valor de cada pixel na imagem é um índice na paleta. Com um formato indexado, o número de bits por pixel está diretamente relacionado ao número de entradas na paleta. Isso reduz significativamente a quantidade de dados necessários para representar a imagem, mas também restringe o número de cores disponíveis para a imagem. O WIC dá suporte a formatos indexados com 1, 2, 4 ou 8 bpp.

Para formatos monocromáticos (escala de cinza), o WIC dá suporte a 1, 2, 4, 8, 16 e 32 bits por pixel. Para profundidades de bits de 1, 8, 16 e 32, os dados de cor são armazenados em um único canal. Para profundidades de bits de 2 ou 4, os pixels são índices em uma paleta de escala de cinza.

### <a name="ycbcr-color-model"></a>Modelo de cores Y'CbCr

O WIC adiciona suporte para o modelo de cor jpeg JFIF Y'CbCr. Y'CbCr separa cores em um componente luma (Y') e dois componentes de chroma (Cb e Cr). Muitos arquivos JPEG armazenam na nativo dados de imagem usando o modelo de cor Y'CbCr.

O sistema visual humano é menos sensível a alterações no chroma do que ao luma, e os formatos Y'CbCr podem aproveitar essa sensibilidade reduzida reduzindo a quantidade de dados de chroma armazenados em relação ao luma. Eles fazem isso, armazenar chroma e luma em planos separados e dimensionar cada plano de componente para uma resolução diferente. Essa prática é conhecida como subampling chroma.

Como os dados chroma e luma são armazenados separadamente e podem ser resoluções diferentes, o WIC define formatos de pixel de luma e chroma separados. O WIC dá suporte a dados de 8 bits por canal.

## <a name="wic-pixel-format"></a>Formato de pixel WIC

Os formatos de pixel no WIC são definidos usando GUIDs para evitar conflitos com IHVs. O WIC fornece um nome amigável para referenciar o GUID de um formato de pixel nativo. A convenção de nomen entre os formatos de pixel WIC é a seguinte:

**\[Tipo de ordem de Armazenamento \_ GUID WICPixelFormat \] \[ Bits por \] \[ \] \[ Pixel\]**

| Componente format         | Descrição                                                                                                                                                                                                                                                                                                  |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **GUID \_ WICPixelFormat** | A identificação descritiva para todos os formatos de pixel WIC. O nome amigável para todos os pixels WIC começa com essa cadeia de caracteres.                                                                                                                                                                                       |
| **Bits por Pixel**       | O número de bits por pixel (bpp) usado para o formato de pixel.                                                                                                                                                                                                                                                |
| **Ordem do canal**        | O modelo de canal de cores e a ordem de cada canal para o formato.                                                                                                                                                                                                                                            |
| **Armazenamento Tipo**         | A codificação numérica usada para o formato de pixel. A codificação padrão é um inteiro sem sinal. Se nada seguir as informações do modelo de cor, um inteiro sem sinal (UINT) será implícito. FixedPoint e Float são usados para identificar formatos de pixel que usam codificação de ponto fixo e de ponto flutuante, respectivamente. |



 

> [!Note]  
> Para formatos de n canais, a Ordem do Canal não especifica a ordem de cores, mas o \[ \] número de canais disponíveis. Por exemplo, GUID \_ WICPixelFormat24bpp3Channels fornece três canais de cores em que "3Channels" é a entrada Ordem de Canal, mas indica apenas o número de canais e não a \[ \] ordem.

 

Por exemplo, o nome amigável GUID \_ WICPixelFormat24bppRGB significa que o formato de pixel usa 24 bits por pixel e o modelo de cor RGB. Como o nome não identifica explicitamente um tipo de armazenamento, um inteiro sem sinal é implícito.

O WIC dá suporte a vários formatos de pixel. As tabelas a seguir agrupam formatos de pixel semelhantes por estrutura de cores, fornecendo informações adicionais, como profundidade de bits, bits por pixel e codificação numérica. Cada tabela contém as seguintes informações:

-   **Nome amigável.** O nome amigável do formato de pixel.
-   **Contagem de Canais**. O número de canais de cores.
-   **Bits por canal.** O número de bits por canal (profundidade de bits).
-   **Bits por pixel.** O número de bits por pixel, incluindo quaisquer bits de preenchimento.
-   **Armazenamento Tipo**. A codificação numérica dos dados da imagem. Esse valor pode ser um UINT (inteiro sem sinal), um número de ponto fixo (FixedPoint) ou um número de ponto flutuante (Float).

> [!Note]  
> Para maior clareza, este documento refere-se a formatos de pixel apenas por seus nomes amigáveis. O valor hexadecimal real para os formatos de pixel pode ser encontrado nos arquivos wincodec.h/idl.

 

### <a name="undefined-pixel-formats"></a>Formatos de pixel indefinido

A lista a seguir mostra formatos de pixel genéricos que são usados quando o formato de pixel é indefinido ou não é importante para uma operação de imagem.

-   GUID \_ WICPixelFormatUndefined
-   GUID \_ WICPixelFormatDontCare

### <a name="indexed-pixel-formats"></a>Formatos de pixel indexados

A tabela a seguir lista os formatos de pixel indexados fornecidos pelo WIC. Nesses formatos, o valor de cada pixel é um índice em uma paleta de cores.



| Nome amigável                   | Contagem de Canais | Bits por Pixel | Tipo de armazenamento |
|---------------------------------|---------------|----------------|--------------|
| GUID \_ WICPixelFormat1bppIndexed | 1             | 1              | UINT         |
| GUID \_ WICPixelFormat2bppIndexed | 1             | 2              | UINT         |
| GUID \_ WICPixelFormat4bppIndexed | 1             | 4              | UINT         |
| GUID \_ WICPixelFormat8bppIndexed | 1             | 8              | UINT         |



 

### <a name="packed-bit-pixel-formats"></a>Formatos de pixel de bits empacotados

A tabela a seguir lista os formatos de bits empacotados fornecidos pelo WIC. Nesses formatos, os dados de canal de cores não são alinhados por byte.



| Nome amigável                          | Contagem de Canais | Bits por canal       | Bits por Pixel | Tipo de armazenamento |
|-------------------------------------------|---------------|------------------------|----------------|--------------|
| GUID \_ WICPixelFormat16bppBGR555           | 3             | 5                      | 16             | UINT         |
| GUID \_ WICPixelFormat16bppBGR565           | 3             | 5(B)/6(G)/5(R)         | 16             | UINT         |
| GUID \_ WICPixelFormat16bppBGRA555          | 4             | 5(B)/5(G)/5(R)/1(A)    | 16             | UINT         |
| GUID \_ WICPixelFormat32bppBGR101010        | 3             | 10                     | 32             | UINT         |
| GUID \_ WICPixelFormat32bppRGBA1010102      | 4             | 10(R)/10(G)/10(B)/2(A) | 32             | UINT         |
| GUID \_ WICPixelFormat32bppRGBA1010102XR    | 4             | 10(R)/10(G)/10(B)/2(A) | 32             | UINT         |
| GUID \_ WICPixelFormat32bppR10G10B10A2      | 4             | 10(R)/10(G)/10(B)/2(A) | 32             | UINT         |
| GUID \_ WICPixelFormat32bppR10G10B10A2HDR10 | 4             | 10(R)/10(G)/10(B)/2(A) | 32             | UINT         |

Para os \_ formatos WICPixelFormat32bppBGR101010 e GUID \_ WICPixelFormat32bppRGBA1010102, o canal vermelho é armazenado nos bits menos significativos. Para os \_ formatos WICPixelFormat32bppR10G10B10A2 e GUID \_ WICPixelFormat32bppR10G10B10A2HDR10, o canal vermelho é definido [](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)nos bits mais significativos, o mesmo layout que DXGI_FORMAT_R10G10B10A2_UNORM .

O formato \_ WICPixelFormat32bppR10G10B10A2HDR10 é o formato de pixel de 10 bits para HDR10 (espaço em cores BT.2020 e SMPTE ST.2084 EOTF).

### <a name="grayscale-pixel-formats"></a>Formatos de pixel em escala de cinza

A tabela a seguir lista os formatos de escala de cinza fornecidos pelo WIC. Nesses formatos, os dados de cor representam tons de cinza.



| Nome amigável                           | Contagem de Canais | Bits por canal | Bits por Pixel | Tipo de armazenamento |
|-----------------------------------------|---------------|------------------|----------------|--------------|
| GUID \_ WICPixelFormatBlackWhite          | 1             | 1                | 1              | UINT         |
| GUID \_ WICPixelFormat2bppGray            | 1             | 2                | 2              | UINT         |
| GUID \_ WICPixelFormat4bppGray            | 1             | 4                | 4              | UINT         |
| GUID \_ WICPixelFormat8bppGray            | 1             | 8                | 8              | UINT         |
| GUID \_ WICPixelFormat16bppGray           | 1             | 16               | 16             | UINT         |
| GUID \_ WICPixelFormat16bppGrayFixedPoint | 1             | 16               | 16             | FixedPoint   |
| GUID \_ WICPixelFormat16bppGrayHalf       | 1             | 16               | 16             | Float        |
| GUID \_ WICPixelFormat32bppGrayFloat      | 1             | 32               | 32             | Float        |
| GUID \_ WICPixelFormat32bppGrayFixedPoint | 1             | 32               | 32             | FixedPoint   |



 

### <a name="rgbbgr-pixel-formats"></a>Formatos de Pixel RGB/BGR

A tabela a seguir lista os formatos RGB/BGR fornecidos pelo WIC. Esses formatos separam os dados de cor primária em canais vermelho (R), verde (G) e azul (B). Um canal alfa (A) adicional é fornecido para informações de opacidade em alguns formatos.



| Nome amigável                            | Contagem de Canais | Bits por canal | Bits por Pixel | Tipo de armazenamento |
|------------------------------------------|---------------|------------------|----------------|--------------|
| GUID \_ WICPixelFormat24bppRGB             | 3             | 8                | 24             | UINT         |
| GUID \_ WICPixelFormat24bppBGR             | 3             | 8                | 24             | UINT         |
| GUID \_ WICPixelFormat32bppBGR             | 3             | 8                | 32             | UINT         |
| GUID \_ WICPixelFormat32bppRGBA            | 4             | 8                | 32             | UINT         |
| GUID \_ WICPixelFormat32bppBGRA            | 4             | 8                | 32             | UINT         |
| GUID \_ WICPixelFormat32bppRGBE\*          | 4             | 8                | 32             | Float        |
| GUID \_ WICPixelFormat32bppPRGBA           | 4             | 8                | 32             | UINT         |
| GUID \_ WICPixelFormat32bppPBGRA           | 4             | 8                | 32             | UINT         |
| GUID \_ WICPixelFormat48bppRGB             | 3             | 16               | 48             | UINT         |
| GUID \_ WICPixelFormat48bppBGR             | 3             | 16               | 48             | UINT         |
| GUID \_ WICPixelFormat48bppRGBFixedPoint   | 3             | 16               | 48             | Fixo        |
| GUID \_ WICPixelFormat48bppBGRFixedPoint   | 3             | 16               | 48             | Fixo        |
| GUID \_ WICPixelFormat48bppRGBHalf         | 3             | 16               | 48             | Float        |
| GUID \_ WICPixelFormat64bppRGBA            | 4             | 16               | 64             | UINT         |
| GUID \_ WICPixelFormat64bppBGRA            | 4             | 16               | 64             | UINT         |
| GUID \_ WICPixelFormat64bppPRGBA           | 4             | 16               | 64             | UINT         |
| GUID \_ WICPixelFormat64bppPBGRA           | 4             | 16               | 64             | UINT         |
| GUID \_ WICPixelFormat64bppRGBFixedPoint   | 3             | 16               | 64             | Fixo        |
| GUID \_ WICPixelFormat64bppRGBAFixedPoint  | 4             | 16               | 64             | Fixo        |
| GUID \_ WICPixelFormat64bppBGRAFixedPoint  | 4             | 16               | 64             | Fixo        |
| GUID \_ WICPixelFormat64bppRGBHalf         | 3             | 16               | 64             | Float        |
| GUID \_ WICPixelFormat64bppRGBAHalf        | 4             | 16               | 64             | Float        |
| GUID \_ WICPixelFormat96bppRGBFixedPoint   | 3             | 32               | 96             | Fixo        |
| GUID \_ WICPixelFormat128bppRGBFloat       | 3             | 32               | 128            | Float        |
| GUID \_ WICPixelFormat128bppRGBAFloat      | 4             | 32               | 128            | Float        |
| GUID \_ WICPixelFormat128bppPRGBAFloat     | 4             | 32               | 128            | Float        |
| GUID \_ WICPixelFormat128bppRGBFixedPoint  | 3             | 32               | 128            | Fixo        |
| GUID \_ WICPixelFormat128bppRGBAFixedPoint | 4             | 32               | 128            | Fixo        |



 

> [!Note]  
> \*O formato GUID WICPixelFormat32bppRGBE codifica três valores de ponto flutuante de 16 bits em 4 bytes, da seguinte forma: três mantissas de 8 bits sem sinal para os canais R, G e B, além de um expoente compartilhado de \_ 8 bits. Esse formato fornece precisão de ponto flutuante de 16 bits em uma representação de pixel menor.

 

Começando com Windows 8 e a Atualização de Plataforma [para Windows 7,](/windows/desktop/direct3darticles/platform-update-for-windows-7)o WIC fornece formatos adicionais, mostrados na tabela aqui.



| Nome amigável                      | Contagem de Canais | Bits por canal | Bits por Pixel | Tipo de armazenamento |
|------------------------------------|---------------|------------------|----------------|--------------|
| GUID \_ WICPixelFormat32bppRGB       | 3             | 8                | 32             | UINT         |
| GUID \_ WICPixelFormat64bppRGB       | 3             | 16               | 64             | UINT         |
| GUID \_ WICPixelFormat96bppRGBFloat  | 3             | 32               | 96             | FLOAT        |
| GUID \_ WICPixelFormat64bppPRGBAHalf | 4             | 16               | 64             | FLOAT        |



 

### <a name="cmyk-pixel-formats"></a>Formatos de pixel do CMYK

A tabela a seguir lista os formatos CMYK fornecidos pelo WIC. Esses formatos separam os dados de cor primária em canais ciano (C), magenta (M), amarelo (Y) e preto (K).



| Nome amigável                      | Contagem de Canais | Bits por canal | Bits por Pixel | Tipo de armazenamento |
|------------------------------------|---------------|------------------|----------------|--------------|
| GUID \_ WICPixelFormat32bppCMYK      | 4             | 8                | 32             | UINT         |
| GUID \_ WICPixelFormat64bppCMYK      | 4             | 16               | 64             | UINT         |
| GUID \_ WICPixelFormat40bppCMYKAlpha | 5             | 8                | 40             | UINT         |
| GUID \_ WICPixelFormat80bppCMYKAlpha | 5             | 16               | 80             | UINT         |



 

### <a name="n-channel-pixel-formats"></a>Formatos de pixel de n canais

A tabela a seguir lista os formatos de n canais fornecidos pelo WIC. Esses formatos fornecem vários canais de cores indefinido para armazenar dados de imagem.



| Nome amigável                            | Contagem de Canais | Bits por canal | Bits por Pixel | Tipo de armazenamento |
|------------------------------------------|---------------|------------------|----------------|--------------|
| GUID \_ WICPixelFormat24bpp3Channels       | 3             | 8                | 24             | UINT         |
| GUID \_ WICPixelFormat48bpp3Channels       | 3             | 16               | 48             | UINT         |
| GUID \_ WICPixelFormat32bpp3ChannelsAlpha  | 4             | 8                | 32             | UINT         |
| GUID \_ WICPixelFormat64bpp3ChannelsAlpha  | 4             | 16               | 64             | UINT         |
| GUID \_ WICPixelFormat32bpp4Channels       | 4             | 8                | 32             | UINT         |
| GUID \_ WICPixelFormat64bpp4Channels       | 4             | 16               | 64             | UINT         |
| GUID \_ WICPixelFormat40bpp4ChannelsAlpha  | 5             | 8                | 40             | UINT         |
| GUID \_ WICPixelFormat80bpp4ChannelsAlpha  | 5             | 16               | 80             | UINT         |
| GUID \_ WICPixelFormat40bpp5Channels       | 5             | 8                | 40             | UINT         |
| GUID \_ WICPixelFormat80bpp5Channels       | 5             | 16               | 80             | UINT         |
| GUID \_ WICPixelFormat48bpp5ChannelsAlpha  | 6             | 8                | 48             | UINT         |
| GUID \_ WICPixelFormat96bpp5ChannelsAlpha  | 6             | 16               | 96             | UINT         |
| GUID \_ WICPixelFormat48bpp6Channels       | 6             | 8                | 48             | UINT         |
| GUID \_ WICPixelFormat96bpp6Channels       | 6             | 16               | 96             | UINT         |
| GUID \_ WICPixelFormat56bpp6ChannelsAlpha  | 7             | 8                | 56             | UINT         |
| GUID \_ WICPixelFormat112bpp6ChannelsAlpha | 7             | 16               | 112            | UINT         |
| GUID \_ WICPixelFormat56bpp7Channels       | 7             | 8                | 56             | UINT         |
| GUID \_ WICPixelFormat112bpp7Channels      | 7             | 16               | 112            | UINT         |
| GUID \_ WICPixelFormat64bpp7ChannelsAlpha  | 8             | 8                | 64             | UINT         |
| GUID \_ WICPixelFormat128bpp7ChannelsAlpha | 8             | 16               | 128            | UINT         |
| GUID \_ WICPixelFormat64bpp8Channels       | 8             | 8                | 64             | UINT         |
| GUID \_ WICPixelFormat128bpp8Channels      | 8             | 16               | 128            | UINT         |
| GUID \_ WICPixelFormat72bpp8ChannelsAlpha  | 9             | 8                | 72             | UINT         |
| GUID \_ WICPixelFormat144bpp8ChannelsAlpha | 9             | 16               | 144            | UINT         |



 

### <a name="alpha-only-pixel-formats"></a>Formatos de pixel somente alfa

A tabela a seguir lista os formatos Somente Alfa fornecidos pelo WIC. Esse formato contém apenas informações alfa.



| Nome amigável                 | Contagem de Canais | Bits por canal | Bits por Pixel | Tipo de armazenamento |
|-------------------------------|---------------|------------------|----------------|--------------|
| GUID \_ WICPixelFormat8bppAlpha | 1             | 8                | 32             | UINT         |



 

### <a name="ycbcr-pixel-formats"></a>Formatos de pixel Y'CbCr

A tabela a seguir lista os formatos Y'CbCr fornecidos pelo WIC. Esses formatos separam os dados de cor primária em luma (Y), diferença de chroma azul (Cb) e cr (diferença de coloração vermelha). Observe que esses formatos foram projetados para armazenar dados de pixel JPEG JFIF Y'CbCr.



| Nome amigável                 | Contagem de Canais | Bits por Pixel | Tipo de armazenamento |
|-------------------------------|---------------|----------------|--------------|
| GUID \_ WICPixelFormat8bppY     | 1             | 8              | UINT         |
| GUID \_ WICPixelFormat8bppCb    | 1             | 8              | UINT         |
| GUID \_ WICPixelFormat8bppCr    | 1             | 8              | UINT         |
| GUID \_ WICPixelFormat16bppCbCr | 2             | 16             | UINT         |



 

## <a name="color-space"></a>Espaço de cores

Os formatos de pixel em si não têm um espaço de cor. Em geral, o espaço de cores é uma interpretação semântica dos valores de pixel que depende do contexto do bitmap. Algumas imagens identificam um contexto de cor que define o espaço de cor da imagem. Somente na ausência de um contexto de cor o espaço de cores deve ser inferido.

As informações de contexto de cor são definidas pela interface [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) para WIC. Para recuperar as informações de contexto de cor de um quadro de imagem, use o **método GetColorContext.**

Na ausência de informações de espaço de cores para uma imagem, a regra geral para inferência de espaço em cores é que os formatos RGB UINT e escala de cinza usam o sRGB (espaço de cor RGB padrão), enquanto os formatos RGB de ponto fixo e de ponto flutuante e escala de cinza usam o espaço de cores RGB estendido (scRGB). O modelo de cor do CMYK usa um espaço de cores RWOP.

## <a name="native-image-formats"></a>Formatos de imagem nativa

Cada um dos Windows codecs WIC fornecidos dá suporte a um subconjunto dos formatos de pixel WIC. Para cada codec, os formatos de decodificado com suporte podem ser diferentes dos formatos de codificação com suporte.

Ao decodificar uma imagem, se os dados são armazenados na verdade em um formato de pixel sem suporte pelo decodificador, ele será convertido em um formato com suporte. Para determinar o formato de pixel de saída, chame [**IWICBitmapFrameDecode::GetPixelFormat.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getpixelformat)

Ao codificar uma imagem, use [**IWICBitmapFrameEncode::SetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setpixelformat) para solicitar que o codificador use um formato de pixel específico. O codificador retornará o formato de pixel com suporte mais próximo, que pode ser diferente do que foi solicitado.

As tabelas a seguir mostram os formatos de pixel com suporte por cada um dos codecs Windows WIC fornecidos.

### <a name="bmp-native-codec"></a>Codec nativo do BMP



| Formatos de pixel do decodificador                   | Formatos de pixel do codificador                   |
|-----------------------------------------|-----------------------------------------|
| GUID \_ WICPixelFormat1bppIndexed         | GUID \_ WICPixelFormat1bppIndexed         |
| GUID \_ WICPixelFormat4bppIndexed         | GUID \_ WICPixelFormat4bppIndexed         |
| GUID \_ WICPixelFormat8bppIndexed         | GUID \_ WICPixelFormat8bppIndexed         |
| GUID \_ WICPixelFormat16bppBGR555         | GUID \_ WICPixelFormat16bppBGR555         |
| GUID \_ WICPixelFormat16bppBGR565         | GUID \_ WICPixelFormat16bppBGR565         |
| GUID \_ WICPixelFormat24bppBGR            | GUID \_ WICPixelFormat24bppBGR            |
| GUID \_ WICPixelFormat32bppBGR            | GUID \_ WICPixelFormat32bppBGR            |
| GUID \_ WICPixelFormat32bppBGRA\*         | \_WICPIXELFORMAT32BPPBGRA GUID\*         |
| \_WICPIXELFORMAT64BPPRGBAFIXEDPOINT GUID | \_WICPIXELFORMAT32BPPPBGRA GUID          |
|                                         | \_WICPIXELFORMAT64BPPRGBAFIXEDPOINT GUID |
|                                         | \_WICPIXELFORMAT64BPPBGRAFIXEDPOINT GUID |



 

> [!Note]  
> \_o GUID WICPixelFormat32bppBGRA só tem suporte no Windows 8, a [atualização de plataforma para Windows 7](/windows/desktop/direct3darticles/platform-update-for-windows-7)e superior.
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
> \_o GUID WICPixelFormat96bppRGBFloat só tem suporte no Windows 8, a [atualização de plataforma para Windows 7](/windows/desktop/direct3darticles/platform-update-for-windows-7)e superior.

 

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
> o codec dds Windows fornecido dá suporte a arquivos dds codificados usando os seguintes \_ valores de formato DXGI:

 

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

[Windows Visão geral do componente de geração de imagens](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[GUIDs e CLSIDs do WIC](-wic-guids-clsids.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[Como escrever um CODEC de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Especificação de foto de HD 1,0](https://www.microsoft.com/whdc/xps/wmphoto.mspx)
</dt> </dl>

 

 
