---
description: Funções de vídeo e imagem
ms.assetid: 02401edc-362b-4f6c-b10b-c46b30b3ebe7
title: Funções de vídeo e imagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c55e439a17dd570b6e939d1cb84d836f9100eaf7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759107"
---
# <a name="video-and-image-functions"></a>Funções de vídeo e imagem

Essas funções e macros manipulam as estruturas de formato de vídeo do DirectShow.



| Função                                                             | Descrição                                                                                                                                                       |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_correspondência de máscaras de bits \_**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-bit_masks_match)                         | Compara as máscaras de cores para duas estruturas [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) .                                                                                       |
| [**BITMASKS**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-bitmasks)                                         | Recupera as máscaras de cor de uma estrutura [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo)                                                                                         |
| [**CheckVideoInfoType**](checkvideoinfotype.md)                     | Verifica um tipo de mídia que contém uma estrutura de formato [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) para erros que podem causar saturações de buffer ou estouros de inteiros.   |
| [**CheckVideoInfo2Type**](checkvideoinfo2type.md)                   | Verifica um tipo de mídia que contém uma estrutura de formato [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) para erros que podem causar saturações de buffer ou estouros de inteiros. |
| [**CORES**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-colors)                                             | Recupera as entradas da paleta de uma estrutura [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo)                                                                                     |
| [**ContainsPalette**](containspalette.md)                           | Determina se uma estrutura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) especificada contém uma paleta.                                                           |
| [**ConvertVideoInfoToVideoInfo2**](convertvideoinfotovideoinfo2.md) | Converte um tipo de mídia que usa [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) para um que usa [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2)                          |
| [**DIBS**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-dibsize)                                           | Calcula o número de bytes exigidos por um bitmap independente de dispositivo (DIB).                                                                                     |
| [**GetBitCount**](getbitcount.md)                                   | Retorna o número de bits por pixel usado por um subtipo de vídeo especificado.                                                                                           |
| [**GetBitmapFormatSize**](getbitmapformatsize.md)                   | Calcula o tamanho necessário para uma estrutura [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) que pode conter uma estrutura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) especificada.       |
| [**GetBitmapPalette**](getbitmappalette.md)                         | Retorna a primeira entrada da paleta em uma estrutura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) .                                                                        |
| [**GetBitmapSize**](getbitmapsize.md)                               | Calcula o número de bytes exigidos por um bitmap independente de dispositivo (DIB).                                                                                     |
| [**GetBitmapSubtype**](getbitmapsubtype.md)                         | Retorna o **GUID** do subtipo de mídia para o bitmap especificado.                                                                                                      |
| [**GetSubtypeName**](getsubtypename.md)                             | Recupera o nome legível por humanos de um subtipo de vídeo.                                                                                                             |
| [**GetTrueColorType**](gettruecolortype.md)                         | Retorna o **GUID** do subtipo de mídia para um bitmap RGB não compactado de 16 bits.                                                                                          |
| [**VERGA**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-header)                                             | Retorna o endereço do [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) em um [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader).                                      |
| [**\_Informações de sequência de MPEG1 \_**](/previous-versions/windows/desktop/api/amvideo/nf-amvideo-mpeg1_sequence_info)                 | Retorna o endereço do cabeçalho de sequência dentro de uma estrutura [**MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo) .                                                          |
| [**PALETTISED**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-palettised)                                     | Verifica se um bitmap tem uma intensidade de cor de 8 bits ou menos.                                                                                                      |
| [**entradas da paleta \_**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-palette_entries)                          | Recupera o número máximo de cores na paleta de um bitmap especificado.                                                                                      |
| [**REDEFINIR \_ máscaras**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-reset_masks)                                  | Preenche os campos de máscara de cor em uma estrutura [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) com zeros.                                                                            |
| [**REDEFINIR \_ cabeçalho**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-reset_header)                                | Preenche um [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) com zeros.                                                                                                   |
| [**REDEFINIR \_ paleta**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-reset_palette)                              | Preenche as entradas da paleta em uma estrutura [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) com zeros.                                                                              |
| [**paleta de tamanho \_ EGA \_**](/previous-versions/windows/desktop/legacy/dd377602(v=vs.85))                       | Calcula o tamanho necessário para as entradas da paleta em um bitmap RGB de 4 bits.                                                                                         |
| [**máscaras de tamanho \_**](/previous-versions/windows/desktop/legacy/dd377603(v=vs.85))                                    | Calcula o tamanho das máscaras de cor em uma estrutura [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) .                                                                             |
| [**MPEG1VIDEOINFO de tamanho \_**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-size_mpeg1videoinfo)                  | Calcula o tamanho de uma estrutura [**MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo) , incluindo o cabeçalho Sequence.                                                      |
| [**paleta de tamanho \_**](/previous-versions/windows/desktop/legacy/dd377605(v=vs.85))                                | Calcula o tamanho das entradas da paleta em uma estrutura [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) .                                                                         |
| [**precabeçalho de tamanho \_**](/previous-versions/windows/desktop/legacy/dd377606(v=vs.85))                            | Calcula o deslocamento de byte do campo **bmiHeader** em uma estrutura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) .                                              |
| [**VIDEOHEADER de tamanho \_**](/previous-versions/windows/desktop/legacy/dd377607(v=vs.85))                        | Calcula o tamanho da estrutura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) .                                                                                  |
| [**TRUECOLOR**](/previous-versions/windows/desktop/legacy/dd407230(v=vs.85))                                   | Retorna a estrutura [**TRUECOLORINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-truecolorinfo) de uma estrutura [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) .                                            |
| [**ValidateBitmapInfoHeader**](validatebitmapinfoheader.md)         | Verifica se há erros em uma estrutura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) que podem causar estouros de buffer ou estouro de inteiro.                                   |



 

## <a name="remarks"></a>Comentários

A maioria das macros e funções descritas na seção são projetadas para manipular estruturas **VIDEOINFOHEADER** e **VIDEOINFO** para bitmaps RGB. Use essas macros com cuidado: a maioria deles pressupõe que a estrutura especificada foi inicializada corretamente. Muitos deles também pressupõem que a estrutura **BITMAPINFOHEADER** seja o tamanho padrão; ou seja, `biSize == sizeof(BITMAPINFOHEADER)` .

A biblioteca de classes base do DirectShow também fornece as seguintes constantes globais, que definem as máscaras de cores padrão para bitmaps de cor real.



| Dados globais | Descrição                                                   |
|-------------|---------------------------------------------------------------|
| **bits555** | Matriz de máscaras de cores para um bitmap RGB de 16 bits no formato 5-5-5. |
| **bits565** | Matriz de máscaras de cores para um bitmap RGB de 16 bits no formato 5-6-5. |
| **bits888** | Matriz de máscaras de cores para um bitmap RGB de 24 bits.                 |



 

Cada uma dessas constantes em uma matriz de três **DWORD** s, contendo as máscaras vermelha, verde e azul, nessa ordem.

 

 
