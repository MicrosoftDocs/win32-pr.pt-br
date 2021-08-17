---
description: Funções de vídeo e imagem
ms.assetid: 02401edc-362b-4f6c-b10b-c46b30b3ebe7
title: Funções de vídeo e imagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ab4b57f804c1da1e4a6da0ca4625e3503ed9987077a80f1f98dde91cf2e27f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119432116"
---
# <a name="video-and-image-functions"></a>Funções de vídeo e imagem

Essas funções e macros manipulam as estruturas DirectShow formato de vídeo.



| Função                                                             | Descrição                                                                                                                                                       |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BIT \_ MASKS \_ MATCH**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-bit_masks_match)                         | Compara as máscaras de cores para duas estruturas [**VIDEOINFO.**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo)                                                                                       |
| [**Bitmasks**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-bitmasks)                                         | Recupera as máscaras de cor de uma [**estrutura VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo)                                                                                         |
| [**CheckVideoInfoType**](checkvideoinfotype.md)                     | Verifica um tipo de mídia que contém uma estrutura de formato [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) para erros que podem causar estouros de buffer ou estouros inteiros.   |
| [**CheckVideoInfo2Type**](checkvideoinfo2type.md)                   | Verifica um tipo de mídia que contém uma estrutura de formato [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) em busca de erros que possam causar estouros de buffer ou estouros inteiros. |
| [**Cores**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-colors)                                             | Recupera as entradas da paleta de uma [**estrutura VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo)                                                                                     |
| [**ContainsPalette**](containspalette.md)                           | Determina se uma estrutura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) especificada contém uma paleta.                                                           |
| [**ConvertVideoInfoToVideoInfo2**](convertvideoinfotovideoinfo2.md) | Converte um tipo de mídia que usa [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) em um que usa [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2)                          |
| [**DIBSIZE**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-dibsize)                                           | Calcula o número de bytes exigidos por um DIB (bitmap independente de dispositivo).                                                                                     |
| [**GetBitCount**](getbitcount.md)                                   | Retorna o número de bits por pixel usado por um subtipo de vídeo especificado.                                                                                           |
| [**GetBitmapFormatSize**](getbitmapformatsize.md)                   | Calcula o tamanho necessário para uma estrutura [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) que pode conter uma estrutura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) especificada.       |
| [**GetBitmapPalette**](getbitmappalette.md)                         | Retorna a primeira entrada de paleta em uma [**estrutura VIDEOINFOHEADER.**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)                                                                        |
| [**GetBitmapSize**](getbitmapsize.md)                               | Calcula o número de bytes exigidos por um DIB (bitmap independente de dispositivo).                                                                                     |
| [**GetBitmapSubtype**](getbitmapsubtype.md)                         | Retorna o GUID do **subtipo de** mídia para o bitmap especificado.                                                                                                      |
| [**GetSubtypeName**](getsubtypename.md)                             | Recupera o nome acessível por humanos de um subtipo de vídeo.                                                                                                             |
| [**GetTrueColorType**](gettruecolortype.md)                         | Retorna o GUID de **subtipo de mídia** para um bitmap RGB de 16 bits descompactado.                                                                                          |
| [**Cabeçalho**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-header)                                             | Retorna o endereço do [**BITMAPINFOHEADER em**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) um [**VIDEOINFOHEADER.**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)                                      |
| [**INFORMAÇÕES DE SEQUÊNCIA MPEG1 \_ \_**](/previous-versions/windows/desktop/api/amvideo/nf-amvideo-mpeg1_sequence_info)                 | Retorna o endereço do header de sequência dentro de uma [**estrutura MPEG1VIDEOINFO.**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo)                                                          |
| [**PALESSED**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-palettised)                                     | Verifica se um bitmap tem uma profundidade de cor de 8 bits ou menos.                                                                                                      |
| [**ENTRADAS DE \_ PALETA**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-palette_entries)                          | Recupera o número máximo de cores na paleta de um bitmap especificado.                                                                                      |
| [**REDEFINIR \_ MÁSCARAS**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-reset_masks)                                  | Preenche os campos de máscara de cores em uma [**estrutura VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) com zeros.                                                                            |
| [**REDEFINIR \_ O HEADER**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-reset_header)                                | Preenche um [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) com zeros.                                                                                                   |
| [**REDEFINIR \_ PALETA**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-reset_palette)                              | Preenche as entradas da paleta em uma estrutura [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) com zeros.                                                                              |
| [**PALETA \_ DE TAMANHO \_ EGA**](/previous-versions/windows/desktop/legacy/dd377602(v=vs.85))                       | Calcula o tamanho necessário para as entradas da paleta em um bitmap RGB de 4 bits.                                                                                         |
| [**MÁSCARAS \_ DE TAMANHO**](/previous-versions/windows/desktop/legacy/dd377603(v=vs.85))                                    | Calcula o tamanho das máscaras de cor em uma [**estrutura VIDEOINFO.**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo)                                                                             |
| [**SIZE \_ MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-size_mpeg1videoinfo)                  | Calcula o tamanho de uma estrutura [**MPEG1VIDEOINFO,**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo) incluindo o header de sequência.                                                      |
| [**PALETA \_ DE TAMANHOS**](/previous-versions/windows/desktop/legacy/dd377605(v=vs.85))                                | calcula o tamanho das entradas da paleta em uma [**estrutura VIDEOINFO.**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo)                                                                         |
| [**SIZE \_ PREHEADER**](/previous-versions/windows/desktop/legacy/dd377606(v=vs.85))                            | Calcula o deslocamento de byte do **campo bmiHeader** dentro de uma [**estrutura VIDEOINFOHEADER.**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)                                              |
| [**TAMANHO \_ VIDEOHEADER**](/previous-versions/windows/desktop/legacy/dd377607(v=vs.85))                        | Calcula o tamanho da estrutura [**VIDEOINFOHEADER.**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)                                                                                  |
| [**Truecolor**](/previous-versions/windows/desktop/legacy/dd407230(v=vs.85))                                   | Retorna a [**estrutura TRUECOLORINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-truecolorinfo) de uma [**estrutura VIDEOINFO.**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo)                                            |
| [**ValidateBitmapInfoHeader**](validatebitmapinfoheader.md)         | Verifica se há erros em uma [**estrutura BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) que podem causar estouros de buffer ou estouros inteiros.                                   |



 

## <a name="remarks"></a>Comentários

A maioria das macros e funções descritas na seção foi projetada para manipular estruturas **VIDEOINFOHEADER** e **VIDEOINFO** para bitmaps RGB. Use essas macros com cuidado: a maioria delas pressupo que a estrutura especificada foi inicializada corretamente. Muitos deles também assumem que a **estrutura BITMAPINFOHEADER** é o tamanho padrão; ou seja, `biSize == sizeof(BITMAPINFOHEADER)` .

A DirectShow de classes base também fornece as constantes globais a seguir, que definem as máscaras de cores padrão para bitmaps de cor verdadeira.



| Dados globais | Descrição                                                   |
|-------------|---------------------------------------------------------------|
| **bits555** | Matriz de máscaras de cores para um bitmap RGB de 16 bits no formato 5-5-5. |
| **bits565** | Matriz de máscaras de cores para um bitmap RGB de 16 bits no formato 5-6-5. |
| **bits888** | Matriz de máscaras de cores para um bitmap RGB de 24 bits.                 |



 

Cada uma dessas constantes em uma matriz de três **DWORD** s, contendo as máscaras vermelho, verde e azul, nessa ordem.

 

 
