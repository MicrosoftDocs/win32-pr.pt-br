---
description: Esta seção descreve o suporte Media Foundation para arquivos MKV (Contêiner de Mídia Matroska).
title: Suporte ao MKV (Contêiner de Mídia matroska)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aceb7a836b4a0409af3c359c8d81a0f232e6eb61082960cfb2b0705531de199c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119102136"
---
# <a name="matroska-media-container-mkv-support"></a>Suporte ao MKV (Contêiner de Mídia matroska)

Esta seção descreve o suporte Media Foundation para arquivos MKV (Contêiner de Mídia Matroska).

O formato MKV pode dar suporte a vários codecs de áudio e vídeo, como H.264 e áudio AAC. Em geral, os contêineres descrevem como os dados de áudio e vídeo são colocados e quais informações complementares são usadas para descrever esses fluxos A/V. Os contêineres também podem incluir dados que complementam fluxos A/V, como o título, idiomas dos fluxos de áudio, faixas de legenda ou legenda, fontes para esses subtítulos, imagens, informações de capítulo e menus. O MKV é um formato altamente flexível que dá suporte a muitos desses recursos de contêiner. Para obter mais informações sobre o formato MKV, consulte [https://matroska.org](https://matroska.org/)


## <a name="mkv-container-feature-support"></a>Suporte ao recurso de contêiner MKV
Os recursos de contêiner MKV têm suporte no Media Foundation das seguintes maneiras:
- Se uma ou mais faixas de vídeo estão presentes, a primeira faixa será tocada.
- Se uma ou mais faixas de áudio estão presentes, a primeira faixa será tocada.
- Há suporte para faixas de legenda, mas não são selecionadas (tocadas) por padrão.
- Se uma ou mais fontes ou imagens estão presentes, legendas e imagens não serão renderizar, embora o arquivo seja carregado e reproduzindo.
- Não há suporte para informações de menu e não serão exibidas, mas o arquivo será carregado e reproduzirá.
- Se os arquivos com capítulos se referirem a arquivos complementares, os arquivos complementares não reproduzirão.
- As imagens em miniatura estão disponíveis ao navegar por arquivos em unidades USB usando o navegador de arquivos.

Esse conjunto de recursos deve permitir a reprodução da maioria dos arquivos MKV se eles contêm codecs com suporte.
Há suporte para arquivos MKV que contêm faixas de áudio e vídeo codificadas com os codecs listados na seção a seguir.

## <a name="supported-mkv-codecs"></a>Codecs MKV com suporte

### <a name="video-codec-support-for-mkv"></a>Suporte a codec de vídeo para MKV

ID do Matroska: V_MPEG4/ISO/AVC

- MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_H264
- Descrição: vídeo H.264
- Identificadores FourCC ou WAV: H264

ID do Matroska: V_MPEG2

- MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MPEG2
- Descrição: vídeo do MPEG-2

ID do Matroska: V_MPEG1

- MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MPG1
- Descrição: vídeo do MPEG-1
- Identificadores FourCC ou WAV: MPG1

ID do Matroska: V_MPEG4/MS/V3

- MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MP43
- Descrição: Codec do Microsoft MPEG 4 versão 3
- Identificadores FourCC ou WAV: MP43

ID do Matroska: V_MPEG4/ISO/ASP

- MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MP4V
- Descrição: vídeo do MPEG-4 parte 2
- Identificadores FourCC ou WAV: MP4V

ID do Matroska: V_MS/VFW/FOURCC

- Descrição: Mapas para vários codecs geralmente com suporte no formato AVI que estão disponíveis no console.

ID do Matroska: V_THEORA

- MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_Theora
- Descrição: Theora
- Identificadores FourCC ou WAV: theo

ID do Matroska: V_MPEG4/ISO/SP

- MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MP4V
- Descrição: Perfil simples ISO MPEG4 (DivX4)
- Identificadores FourCC ou WAV: MP4V

ID do Matroska: V_MPEG4/ISO/AP

- MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MP4V
- Descrição: perfil simples avançado DO ISO MPEG4 (DivX5,Fild, FFMPEG)
- Identificadores FourCC ou WAV: MP4V


ID do Matroska: V_MPEGH/ISO/HEVC 

- MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_HEVC
- Descrição: HEVC/H.265
- Identificadores FourCC ou WAV: 

ID do Matroska: V_VP8

- MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_VP80
- Descrição: formato codec vp8
- Identificadores FourCC ou WAV: VP80

ID do Matroska: V_VP9

- MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_VP90
- Descrição: formato codec VP9
- Identificadores FourCC ou WAV: VP90

ID do Matroska: V_MJPEG

- MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MJPG
- Descrição: JPEG de movimento
- Identificadores FourCC ou WAV: MJPG

ID do Matroska: V_AV1

- MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_AV1
- Descrição: AOMedia Video 1
- Identificadores FourCC ou WAV: AV01

### <a name="audio-codec-support-for-mkv"></a>Suporte a codec de áudio para MKV

ID do Matroska: A_AAC

- MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_AAC
- Descrição: Codificação de Áudio Avançada (AAC)
- Identificadores FourCC ou WAV: WAVE_FORMAT_MPEG_HEAAC

ID do Matroska: A_AC3

- MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_Dolby_AC3
- Descrição: Dolby AC3
- Identificadores FourCC ou WAV: WAVE_FORMAT_DOLBY_AC3_SPDIF

ID do Matroska: A_MPEG/L3

- MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_MP3
- Descrição: MPEG Audio Layer-3 (MP3)
- Identificadores FourCC ou WAV: WAVE_FORMAT_MPEGLAYER3

ID do Matroska: A_MPEG/L1

- MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_MPEG
- Descrição: conteúdo de áudio MPEG-1
- Identificadores FourCC ou WAV: WAVE_FORMAT_MPEG

ID do Matroska: A_PCM/INT/BIG

- MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_PCM
- Descrição: áudio PCM descompactado
- Identificadores FourCC ou WAV: WAVE_FORMAT_PCM

ID do Matroska: A_PCM/INT/LIT

- MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_PCM
- Descrição: áudio PCM descompactado
- Identificadores FourCC ou WAV: WAVE_FORMAT_PCM

ID do Matroska: A_PCM/FLOAT/IEEE

- MF_MT_SUBTYPE de Media Foundation MSFT: MFAudioFormat_Float
- Descrição: áudio de ponto flutuante de IEEE não compactado
- Identificadores FourCC ou WAV: WAVE_FORMAT_IEEE_FLOAT

ID do Matroska: A_ALAC

- MF_MT_SUBTYPE de Media Foundation MSFT: MFAudioFormat_ALAC
- Descrição: codec de áudio do Apple Lossless
- Identificadores FourCC ou WAV: 

ID do Matroska: A_MPEG/L2

- MF_MT_SUBTYPE de Media Foundation MSFT: MFAudioFormat_MPEG
- Descrição: áudio MPEG 1, 2 camada II
- Identificadores FourCC ou WAV: WAVE_FORMAT_MPEG

ID do Matroska: A_DTS

- MF_MT_SUBTYPE de Media Foundation MSFT: MEDIASUBTYPE_DTS_HD
- Descrição: sistema de teatro digital
- Identificadores FourCC ou WAV: WAVE_FORMAT_DTS

ID do Matroska: A_OPUS

- MF_MT_SUBTYPE de Media Foundation MSFT: MFAudioFormat_Opus
- Descrição: Opus
- Identificadores FourCC ou WAV: WAVE_FORMAT_OPUS

ID do Matroska: A_VORBIS

- MF_MT_SUBTYPE de Media Foundation MSFT: MFAudioFormat_Vorbis
- Descrição: Vorbis
- Identificadores FourCC ou WAV: 

ID do Matroska: A_FLAC

- MF_MT_SUBTYPE de Media Foundation MSFT: MFAudioFormat_FLAC
- Descrição: codec de áudio sem perdas gratuita
- Identificadores FourCC ou WAV: WAVE_FORMAT_FLAC

ID de Matroska: A_AAC/MAIN

- MF_MT_SUBTYPE de Media Foundation MSFT: MFAudioFormat_AAC
- Descrição: AAC (codificação de áudio avançada)
- Identificadores FourCC ou WAV: WAVE_FORMAT_MPEG_HEAAC

ID do Matroska: A_EAC3

- MF_MT_SUBTYPE de Media Foundation MSFT: MFAudioFormat_Dolby_DDPlus
- Descrição: AC avançada-3
- Identificadores FourCC ou WAV: 

ID do Matroska: A_TRUEHD

- MF_MT_SUBTYPE de Media Foundation MSFT: MEDIASUBTYPE_DOLBY_TRUEHD
- Descrição: Dolby TrueHD
- Identificadores FourCC ou WAV: 

ID do Matroska: A_MS/ACM

- MF_MT_SUBTYPE de Media Foundation MSFT: Mapas a vários tipos de áudio WAVE_FORMAT definidos em mmreg. h


### <a name="subtitles-codec-support-for-mkv"></a>Suporte ao codec de legendas para MKV

ID do Matroska: S_TEXT/ASCII

- MF_MT_SUBTYPE de Media Foundation MSFT: MFSubtitleFormat_SRT
- Descrição: texto ASCII

ID do Matroska: S_TEXT/UTF8

- MF_MT_SUBTYPE de Media Foundation MSFT: MFSubtitleFormat_SRT
- Descrição: texto sem formatação UTF-8

ID do Matroska: S_TEXT/SSA

- MF_MT_SUBTYPE de Media Foundation MSFT: MFSubtitleFormat_SSA
- Descrição: formato de legenda

ID do Matroska: S_TEXT/ASS

- MF_MT_SUBTYPE de Media Foundation MSFT: MFSubtitleFormat_SSA
- Descrição: formato de legendas avançadas

ID do Matroska: S_VOBSUB

- MF_MT_SUBTYPE de Media Foundation MSFT: MFSubtitleFormat_VobSub
- Descrição: VobSub legendas

ID do Matroska: S_HDMV/PGS

- MF_MT_SUBTYPE de Media Foundation MSFT: MFSubtitleFormat_PGS
- Descrição: HDMV de apresentação de imagens (PGS)


## <a name="technical-details-regarding-codecs"></a>Detalhes técnicos sobre codecs

Consulte os detalhes técnicos a seguir sobre os codecs.

- [Especificações do codec Matroska](http://www.matroska.org/technical/specs/codecid/index.html)
- [GUIDs de subtipo de áudio](audio-subtype-guids.md)
- [GUIDs de subtipo de vídeo](video-subtype-guids.md)


## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Formatos de mídia compatíveis com o Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> <dt>

[Guia de programação Media Foundation](media-foundation-programming-guide.md)
</dt> </dl>

 

 



