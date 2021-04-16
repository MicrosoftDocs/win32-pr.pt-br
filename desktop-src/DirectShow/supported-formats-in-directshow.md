---
description: Formatos com suporte no DirectShow
ms.assetid: cd8af779-2fb5-4724-a838-5d0c8244f0d3
title: Formatos com suporte no DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5a6c9a0c85a3ccdfd3db092ba2efce00a191493
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758047"
---
# <a name="supported-formats-in-directshow"></a>Formatos com suporte no DirectShow

O DirectShow é uma arquitetura aberta, o que significa que ele pode dar suporte a qualquer formato, desde que haja filtros para analisá-los e decodificá-los. Os filtros fornecidos pela Microsoft, seja como redistribuíveis por meio do DirectShow ou componentes do sistema operacional Windows, fornecem suporte padrão para os seguintes formatos de arquivo e compactação.

Tipos de arquivo:



| Tipo de arquivo                                                                                        | Mais informações                                                                                                                  |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| ASF (Advanced Systems Format), incluindo o Windows Media Audio (WMA) e o Windows Media Video (WMV) | [Filtro de leitor ASF do WM](about-the-wm-asf-reader-filter.md)<br/> [Filtro de gravador ASF do WM](wm-asf-writer-filter.md)<br/> |
| AIFF                                                                                             | [Filtro do analisador de som WAVE](wave-parser-filter.md)                                                                                      |
| AU                                                                                               | [Filtro do analisador de som WAVE](wave-parser-filter.md)                                                                                      |
| Audio-Video Interleaved (AVI)                                                                    | [Filtro AVI Mux](avi-mux-filter.md)<br/> [Filtro de Splitter AVI](avi-splitter-filter.md)<br/>                         |
| MIDI                                                                                             | [Filtro de analisador de MIDI](midi-parser-filter.md)<br/> [**Filtro de renderizador MIDI**](midi-renderer-filter.md)<br/>           |
| SND                                                                                              |                                                                                                                                   |
| WAV                                                                                              | [Filtro do analisador de som WAVE](wave-parser-filter.md)                                                                                      |



 

Formatos de compactação:



| Formatar                                        | Mais informações                                                                                                                                                                                                                                |
|-----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AAC                                           | [**Decodificador de áudio do Microsoft MPEG-1/DD/AAC**](microsoft-mpeg-1-dd-audio-decoder.md)                                                                                                                                                              |
| Cinepak                                       |                                                                                                                                                                                                                                                 |
| Vídeo digital (DV)                            | [Filtro de decodificador de vídeo DV](dv-video-decoder-filter.md)<br/> [Filtro de codificador de vídeo DV](dv-video-encoder-filter.md)<br/>                                                                                                             |
| H.264                                         | [**Decodificador de vídeo do Microsoft MPEG-2**](microsoft-mpeg-2-video-decoder.md)                                                                                                                                                                        |
| Vídeo ISO MPEG-4 versão 1,0                  |                                                                                                                                                                                                                                                 |
| Microsoft MPEG-4 versão 3                    |                                                                                                                                                                                                                                                 |
| MJPEG                                         | [Filtro de compressor de MJPEG](mjpeg-compressor-filter.md)<br/> [Filtro de descompactação de MJPEG](mjpeg-decompressor-filter.md)<br/>                                                                                                         |
| Camada de áudio MPEG-3 (MP3) (somente descompactação) |                                                                                                                                                                                                                                                 |
| Áudio MPEG-1 camada I e camada II             | [**Decodificador de áudio do Microsoft MPEG-1/DD/AAC**](microsoft-mpeg-1-dd-audio-decoder.md)<br/> [Filtro de decodificador de áudio MPEG-1](mpeg-1-audio-decoder-filter.md)<br/>                                                                         |
| Vídeo MPEG-1                                  | [Filtro de decodificador de vídeo MPEG-1](mpeg-1-video-decoder-filter.md)<br/> [**Decodificador de vídeo do Microsoft MPEG-2**](microsoft-mpeg-2-video-decoder.md)<br/>                                                                                   |
| Áudio MPEG-2                                  | [**Codificador de áudio Microsoft MPEG-2**](microsoft-mpeg-2-audio-encoder.md)<br/> [**Codificador MPEG-2 da Microsoft**](microsoft-mpeg-2-encoder.md)<br/>                                                                                     |
| Vídeo MPEG-2                                  | [**Codificador MPEG-2 da Microsoft**](microsoft-mpeg-2-encoder.md)<br/> [**Decodificador de vídeo do Microsoft MPEG-2**](microsoft-mpeg-2-video-decoder.md)<br/> [**Codificador de vídeo MPEG-2 da Microsoft**](microsoft-mpeg-2-video-encoder.md)<br/> |



 

Para obter informações sobre a disponibilidade de codecs de terceiros específicos para redistribuição com aplicativos do DirectShow, entre em contato com o fabricante do codec.

 

 




