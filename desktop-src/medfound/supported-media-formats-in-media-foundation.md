---
description: Esse tópico lista os formatos de mídia para os quais o Microsoft Media Foundation dá suporte nativo.
ms.assetid: 69c12a28-4b58-4979-b4d8-ae37efa847fe
title: Formatos de mídia compatíveis com o Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ecbc5024ab70e9e0bdd07d6213ad9779c21e2b7f34f10f3e2d3fe538a784734
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118238185"
---
# <a name="supported-media-formats-in-media-foundation"></a>Formatos de mídia compatíveis com o Media Foundation

Esse tópico lista os formatos de mídia para os quais o Microsoft Media Foundation dá suporte nativo. Terceiros podem dar suporte a formatos adicionais escrevendo plug-ins personalizados.

## <a name="file-containers"></a>Contêineres de arquivo



| Formatar                                           | Extensões de arquivo          | Fonte de mídia                                 | Sink de mídia                                   | Exige                                                              |
|--------------------------------------------------|--------------------------|----------------------------------------------|----------------------------------------------|-----------------------------------------------------------------------|
| 3GP                                              | .3g2, .3gp, .3gp2, .3gpp | [Origem do arquivo MPEG-4](mpeg-4-file-source.md) | 3GP File Sink                                | Windows 7                                                             |
| FORMATO DE STREAMING Avançado (ASF)                  | .asf, .wma, .wmv         | [Fonte de mídia do ASF](asf-media-source.md)     | [ASF Media Sink](asf-media-sinks.md)        | Windows Vista                                                         |
| Fluxo de Transporte de Dados de Áudio (ADTS).              | .aac, .adts              | Origem do arquivo ADTS                             | Nenhum                                         | Windows 7                                                             |
| AVI                                              | .avi                     | Origem do arquivo AVI                              | Nenhum                                         | Windows 7                                                             |
| MP3                                              | .mp3                     | [**Origem do arquivo MP3**](mp3-file-source.md)   | MP3 File Sink                                | Fonte de arquivo: Windows Vista<br/> Sink de arquivo: Windows 7<br/> |
| MPEG-4                                           | .m4a, .m4v, .mov, .mp4   | [Origem do arquivo MPEG-4](mpeg-4-file-source.md) | [**MPEG-4 File Sink**](mpeg-4-file-sink.md) | Windows 7                                                             |
| SAMI (Intercâmbio de Mídia Acessível Sincronizado) | .sami, .smi              | [Fonte de mídia SAMI](sami-media-source.md)   | Nenhum                                         | Windows Vista                                                         |
| Onda                                             | .wav                     | Origem do arquivo AVI                              | Nenhum                                         | Windows 7                                                             |



 

## <a name="audio-codecs"></a>Codecs de áudio



| Formatar                                              | Decodificador                                                                                                                                                          | Codificador                                                                                                                                                          | Exige      |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------|
| codificação μ lei                                        | Codec μ ACM (Gerenciador de Compactação de Áudio)                                                                                                                      | Nenhum                                                                                                                                                             | Windows Vista |
| Modularidade de código de pulso diferencial adaptável (ADPCM) | ACM ADPCM Codec                                                                                                                                                  | Nenhum                                                                                                                                                             | Windows Vista |
| Codificação de áudio avançada (AAC)                         | [**Decodificador AAC**](aac-decoder.md)                                                                                                                               | [**Codificador AAC**](aac-encoder.md)                                                                                                                               | Windows 7     |
| MP3                                                 | [**Windows Decodificador mp3 de mídia**](windows-media-mp3-decoder.md)                                                                                                   | Nenhum                                                                                                                                                             | Windows Vista |
| GSM 6.10                                            | ACM GSM 6.10 Codec                                                                                                                                               | Nenhum                                                                                                                                                             | Windows Vista |
| Áudio do Windows Media (WMA)                           | [**Windows Decodificador de áudio de mídia**](windowsmediaaudiodecoder.md)<br/> [**Windows Decodificador de voz de áudio de mídia**](windowsmediaaudiovoicedecoder.md)<br/> | [**Windows Codificador de áudio de mídia**](windowsmediaaudioencoder.md)<br/> [**Windows Codificador de voz de áudio de mídia**](windowsmediaaudiovoiceencoder.md)<br/> | Windows Vista |



 

> [!Note]  
> Media Foundation fornece wrappers para vários codecs do ACM, listados na tabela anterior. No entanto, Media Foundation dá suporte a codecs arbitrários do ACM.

 

## <a name="video-codecs"></a>Codecs de vídeo



| Formatar                                                                                                         | Decodificador                                                                                                                                                                  | Codificador                                                                                                                             | Exige      |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|---------------|
| Vídeo dv                                                                                                       | [**Decodificador de vídeo DV**](dv-video-decoder.md)                                                                                                                             | Nenhum                                                                                                                                | Windows 7     |
| H.264                                                                                                          | [**Decodificador de vídeo H.264**](h-264-video-decoder.md)                                                                                                                       | [**Codificador de vídeo H.264**](h-264-video-encoder.md)                                                                                  | Windows 7     |
| H.263<br/> (Perfil de linha de base H.264 compatível com o modo de header de vídeo curto MPEG-4 Pt2)<br/> | [**Decodificador de vídeo MPEG-4 parte 2**](mpeg4part2videodecoder.md)                                                                                                            | Nenhum                                                                                                                                | Windows 8     |
| MJPEG                                                                                                          | Decodificador de MJPEG                                                                                                                                                            | Nenhum                                                                                                                                | Windows 7     |
| MPEG-4, parte 2                                                                                                  | [**Decodificador de vídeo MPEG-4 parte 2**](mpeg4part2videodecoder.md)                                                                                                            | Nenhum                                                                                                                                | Windows 7     |
| MPEG-4 V1/V2/V3                                                                                                | [**Windows Decodificador de mídia MPEG-4 v3**](./windowsmediampeg4v3decoder.md)<br/> [**Windows Decodificador de mídia MPEG4 V1/V2**](windowsmediampeg4decoder.md)<br/>         | Nenhum                                                                                                                                | Windows Vista |
| Vídeo do Windows Media (WMV)                                                                                      | [**Windows Decodificador de vídeo de mídia 9**](windowsmediavideo9decoder.md)<br/> [**Windows Decodificador de tela vídeo de mídia 9**](windowsmediavideo9screendecoder.md)<br/> | Windows Codificador de vídeo de mídia 9<br/> Windows Codificador de tela de vídeo de mídia 9<br/> Windows Codificador de vídeo de mídia 7/8<br/> | Windows Vista |



 

> [!Note]  
> A coluna "Requires" lista o sistema operacional mínimo necessário para usar esses codecs em um aplicativo Media Foundation. alguns desses codecs foram introduzidos antes do Windows Vista como DMOs ( [DirectX Media objects](../directshow/directx-media-objects.md) ). se um codec der suporte à funcionalidade DMO, ele poderá ser usado com [DirectShow](../directshow/directshow.md) ou o [SDK do formato de mídia Windows](../wmformat/windows-media-format-11-sdk.md).

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Objetos de codec](codecobjects.md)
</dt> <dt>

[Guia de programação Media Foundation](media-foundation-programming-guide.md)
</dt> <dt>

[Fontes de mídia e coletores](media-sources-and-sinks.md)
</dt> </dl>

 

 
