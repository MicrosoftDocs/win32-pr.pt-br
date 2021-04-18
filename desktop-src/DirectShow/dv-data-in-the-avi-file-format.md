---
description: Dados de DV no formato de arquivo AVI
ms.assetid: ae1ec184-afc3-4ec1-9b92-f53656293446
title: Dados de DV no formato de arquivo AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65f1393bfe4bbee4d080d90755f33cfa7f4a7fa4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456792"
---
# <a name="dv-data-in-the-avi-file-format"></a>Dados de DV no formato de arquivo AVI

A Microsoft especificou o formato de armazenamento de dados de vídeo digital (DV) em arquivos AVI. Em conformidade com essa especificação, você garantirá que os arquivos AVI criados nesse formato serão compatíveis com as versões futuras da arquitetura de vídeo digital do DirectShow para o Windowsplatform.

Este artigo descreve o formato dos arquivos AVI que contêm dados DV. Os FOURCC (códigos de quatro caracteres) específicos para os fluxos de dados de DV e os manipuladores de fluxo do DV compressor/descompactador estão definidos. A estrutura de formato de fluxo para dados DV está definida. As especificações para dois métodos de armazenamento de dados DV no formato de arquivo AVI são especificadas.

Supõe-se que o leitor esteja familiarizado com o formato de dados DV. (Esse formato é definido na *especificação de uso do consumidor digital VCRs*, também chamado de livro azul.)

Há dois tipos de arquivos AVI do DV: arquivos AVI que contêm um fluxo de dados DV, chamado arquivos do *tipo 1* ; e arquivos AVI que contêm vídeo DV como um fluxo ' vids ' e áudio DV como fluxos ' auds ', chamados *de arquivos de tipo 2* .

**Arquivos AVI contendo um fluxo de dados DV (tipo 1)**

Os dados intercalados de DV podem ser armazenados em seu formato nativo como um único fluxo dentro de um arquivo RIFF AVI. Isso tem a vantagem de usar a quantidade mínima de armazenamento de dados para DV. A desvantagem principal é que esse formato de arquivo não é compatível com versões anteriores com vídeo para Windows, porque ele não contém um vídeo "vids" ou um fluxo "auds" de áudio. O suporte é fornecido para o fluxo DV intercalado por meio dos filtros [DV Muxer](dv-muxer-filter.md) e [DV Splitter](dv-splitter-filter.md) fornecidos com o DirectShow.

Os dados de DV podem ser armazenados em um único fluxo dentro de um arquivo RIFF AVI especificando o "iAVS" (fluxo de áudio e vídeo intercalado) FOURCC (código de quatro caracteres) no membro **fccType** e qualquer um dos "dvsd", "dvhd" ou "DVSL" FOURCC no membro **fccHandler** da parte de cabeçalho de fluxo "strh". Os quadros por segundo do fluxo de vídeo devem ser especificados nos membros **dwRate** e **dwScale** e o número total de blocos de vídeo na parte ' movi ' no membro **dwLength** .

O manipulador de fluxo ' dvsd ' FOURCC especifica que os dados de DV estão conforme definidos na parte 2 da *especificação de uso de consumidor digital VCRs*. O vídeo está no formato de 525 linhas às 29,97 Hz (525-60) ou 625 linhas às 25, 0 Hz (625-50).

O manipulador de fluxo ' dvhd ' FOURCC especifica que os dados de DV estão conforme definidos na parte 3 da *especificação de uso de consumidor digital VCRs*. O vídeo está no formato de 1125 linhas às 30, 0 Hz (1125-60) ou 1250 linhas às 25, 0 Hz (1250-50).

O manipulador de fluxo ' dvsl ' FOURCC especifica que os dados de DV são os mesmos definidos na parte 6 da *especificação de uso do consumidor digital VCRs*. O vídeo está no formato de alta compactação SD (SDL).

> [!Note]  
> O restante deste artigo fornece definições para fluxos ' dvsd '.

 

A parte do cabeçalho do fluxo deve ser seguida por uma parte do formato de fluxo [**DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo) .

Os dados reais de DV são armazenados como \# \# partes ' DC ' na parte ' movi ' (o \# \# no formato representa o identificador de fluxo). Cada parte contém um quadro de dados, de 10 ou 12 seqüências de DV DIF para sistemas 525-60 ou 625-50, respectivamente. O formato de sequência DIF DV SD (' dvsd ') é definido na parte 2 da *especificação de uso de consumidor VCRs digital*.

O exemplo a seguir mostra o formato de RIFF AIFF para um arquivo AVI com um fluxo de dados DV, expandido com partes de cabeçalho concluídas.


```C++
00000000 RIFF (0FAE35D4) 'AVI '
0000000C     LIST (00000106) 'hdrl'
00000018         avih (00000038)
                     dwMicroSecPerFrame    : 33367
                     dwMaxBytesPerSec      : 3728000
                     dwPaddingGranularity  : 0
                     dwFlags               : 0x810 HASINDEX | TRUSTCKTYPE
                     dwTotalFrames         : 2192
                     dwInitialFrames       : 0
                     dwStreams             : 1
                     dwSuggestedBufferSize : 120000
                     dwWidth               : 720
                     dwHeight              : 480
                     dwReserved            : 0x0
00000058         LIST (0000006C) 'strl'
00000064             strh (00000038)
                         fccType               : 'iavs'
                         fccHandler            : 'dvsd'
                         dwFlags               : 0x0
                         wPriority             : 0
                         wLanguage             : 0x0 undefined
                         dwInitialFrames       : 0
                         dwScale               : 100 (29.970 Frames/Sec)
                         dwRate                : 2997
                         dwStart               : 0
                         dwLength              : 2192
                         dwSuggestedBufferSize : 120000
                         dwQuality             : 0
                         dwSampleSize          : 0
                         rcFrame               : 0,0,720,480
000000A4             strf (00000020)
                         dwDVAAuxSrc     : 0x........
                         dwDVAAuxCtl     : 0x........
                         dwDVAAuxSrc1    : 0x........
                         dwDVAAuxCtl1    : 0x........
                         dwDVVAuxSrc     : 0x........
                         dwDVVAuxCtl     : 0x........
                         dwDVReserved[2] : 0,0
000000CC     LIST (0FADAC00) 'movi'
0FADACD4     idx1 (00008900)
```



**Arquivos AVI que contêm vídeo DV e fluxos de áudio DV (tipo 2)**

Os dados intercalados de DV podem ser divididos em um fluxo de vídeo e de um a quatro fluxos de áudio em um arquivo RIFF AVI. Isso tem a vantagem de ser compatível com versões anteriores com vídeo para Windows, pois contém um fluxo de vídeo "vids" padrão e pelo menos um fluxo de áudio "auds" padrão. a desvantagem principal é que esse formato de arquivo requer que os dados de áudio sejam armazenados de forma redundante como fluxos de áudio. O fluxo de "vídeo" é, na verdade, o fluxo de dados de DV intercalado nativo. No entanto, como um fluxo "vids" padrão com um tipo de manipulador de "dvsd", o [decodificador de vídeo DV](dv-video-decoder-filter.md) é usado. Esse formato também requer o uso do filtro de [Splitter DV](dv-splitter-filter.md) para dividir arquivos "capturados" antes de gravá-los como arquivos AVI.

Os dados DV podem ser armazenados como um fluxo de vídeo com um número separado de fluxos de áudio em um arquivo RIFF AVI. O fluxo de vídeo é especificado com um cabeçalho de fluxo de vídeo padrão (o valor do membro **fccType** é ' vids '). O membro **fccHandler** é especificado como ' dvsd ', ' dvhd ' ou ' dvsl '. Os quadros por segundo do fluxo de vídeo devem ser especificados nos membros **dwRate** e **dwScale** e o número total de blocos de vídeo na parte ' movi ' no membro **dwLength** .

Neste arquivo AVI que contém vídeo DV como um fluxo ' vids ' e áudio DV como forma de fluxos ' auds ' de DV, a parte do formato de fluxo de vídeo é uma estrutura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) padrão. A parte de formato de fluxo pode ser estendida opcionalmente para incluir a parte [**DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo) , aumentando o tamanho da parte do formato de fluxo de 40 bytes (tamanho da estrutura **BITMAPINFOHEADER** ) para 72 bytes (tamanho das estruturas **BITMAPINFOHEADER** mais **DVINFO** ) e imediatamente após a estrutura de dados **BITMAPINFOHEADER** com uma estrutura de dados **DVINFO** .

Os fluxos de áudio são especificados com um cabeçalho de fluxo de áudio padrão (o valor do membro **fccType** é ' auds '). O membro **fccHandler** não é usado para fluxos de áudio.

Os dados de vídeo DV são armazenados como \# \# partes ' DC ', conforme definido na descrição anterior de um arquivo AVI com um dado DV, e os dados de áudio são armazenados como \# \# partes ' WB ' na parte ' movi '.

> [!Note]  
> A *especificação do VCRs digital de uso do consumidor* pode não estar disponível em alguns idiomas e países.

 

O exemplo a seguir mostra o formato de RIFF AIFF para um arquivo AVI que contém o vídeo DV como um fluxo ' vids ' e áudio DV como fluxos ' auds ' expandidos com fragmentos de cabeçalho concluídos (incluindo dados [**DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo) opcionais que seguem o [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) na subparte ' strf ' para o fluxo ' vids ').


```C++
00000000 RIFF (103E2920) 'AVI '
0000000C     LIST (00000146) 'hdrl'
00000018         avih (00000038)
                     dwMicroSecPerFrame    : 33367
                     dwMaxBytesPerSec      : 3728000
                     dwPaddingGranularity  : 0
                     dwFlags               : 0x810 HASINDEX | TRUSTCKTYPE
                     dwTotalFrames         : 2192
                     dwInitialFrames       : 0
                     dwStreams             : 2
                     dwSuggestedBufferSize : 120000
                     dwWidth               : 720
                     dwHeight              : 480
                     dwReserved            : 0x0
00000058         LIST (00000094) 'strl'
00000064             strh (00000038)
                         fccType               : 'vids'
                         fccHandler            : 'dvsd'
                         dwFlags               : 0x0
                         wPriority             : 0
                         wLanguage             : 0x0 undefined
                         dwInitialFrames       : 0
                         dwScale               : 100 (29.970 Frames/Sec)
                         dwRate                : 2997
                         dwStart               : 0
                         dwLength              : 2192
                         dwSuggestedBufferSize : 120000
                         dwQuality             : 0
                         dwSampleSize          : 0
                         rcFrame               : 0,0,720,480
000000A4             strf (00000048)
                         biSize          : 40
                         biWidth         : 720
                         biHeight        : 480
                         biPlanes        : 1
                         biBitCount      : 24
                         biCompression   : 0x64737664 'dvsd'
                         biSizeImage     : 120000
                         biXPelsPerMeter : 0
                         biYPelsPerMeter : 0
                         biClrUsed       : 0
                         biClrImportant  : 0
                         dwDVAAuxSrc     : 0x........
                         dwDVAAuxCtl     : 0x........
                         dwDVAAuxSrc1    : 0x........
                         dwDVAAuxCtl1    : 0x........
                         dwDVVAuxSrc     : 0x........
                         dwDVVAuxCtl     : 0x........
                         dwDVReserved[2] : 0,0
000000F4         LIST (0000005E) 'strl'
00000100             strh (00000038)
                         fccType               : 'auds'
                         fccHandler            : '    '
                         dwFlags               : 0x0
                         wPriority             : 0
                         wLanguage             : 0x0 undefined
                         dwInitialFrames       : 0
                         dwScale               : 1 (32000.000 Samples/Sec)
                         dwRate                : 32000
                         dwStart               : 0
                         dwLength              : 2340474
                         dwSuggestedBufferSize : 4272
                         dwQuality             : 0
                         dwSampleSize          : 4
                         rcFrame               : 0,0,0,0
00000140             strf (00000012)
                         wFormatTag      : 1 PCM
                         nChannels       : 2
                         nSamplesPerSec  : 32000
                         nAvgBytesPerSec : 128000
                         nBlockAlign     : 4
                         wBitsPerSample  : 16
                         cbSize          : 0
00000814     LIST (103D0EF4) 'movi'
103D1710     idx1 (00011210)
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Formato de arquivo AVI](avi-file-format.md)
</dt> </dl>

 

 
