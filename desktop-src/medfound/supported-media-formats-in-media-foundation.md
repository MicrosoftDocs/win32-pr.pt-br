---
description: Esse tópico lista os formatos de mídia para os quais o Microsoft Media Foundation dá suporte nativo.
ms.assetid: 69c12a28-4b58-4979-b4d8-ae37efa847fe
title: Formatos de mídia compatíveis com o Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00e8f698179d37fc6bde8d5d1dab25214727cd38
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105756522"
---
# <a name="supported-media-formats-in-media-foundation"></a>Formatos de mídia compatíveis com o Media Foundation

Esse tópico lista os formatos de mídia para os quais o Microsoft Media Foundation dá suporte nativo. Terceiros podem dar suporte a formatos adicionais escrevendo plug-ins personalizados.

## <a name="file-containers"></a>Contêineres de arquivo



| Formatar                                           | Extensões de arquivo          | Origem da mídia                                 | Coletor de mídia                                   | Exige                                                              |
|--------------------------------------------------|--------------------------|----------------------------------------------|----------------------------------------------|-----------------------------------------------------------------------|
| 3GP                                              | .3G2,. 3GP,. 3GP2,. 3GPP | [Fonte de arquivo MPEG-4](mpeg-4-file-source.md) | Coletor de arquivos 3GP                                | Windows 7                                                             |
| ASF (Advanced Streaming Format)                  | . ASF,. WMA,. wmv         | [Fonte de mídia ASF](asf-media-source.md)     | [Coletor de mídia ASF](asf-media-sinks.md)        | Windows Vista                                                         |
| Fluxo de transporte de dados de áudio (ADTS).              | . AAC,. ADTS              | Origem do arquivo ADTS                             | Nenhum                                         | Windows 7                                                             |
| AVI                                              | .avi                     | Fonte de arquivo AVI                              | Nenhum                                         | Windows 7                                                             |
| MP3                                              | .mp3                     | [**Origem de arquivo MP3**](mp3-file-source.md)   | Coletor de arquivos MP3                                | Origem do arquivo: Windows Vista<br/> Coletor de arquivos: Windows 7<br/> |
| MPEG-4                                           | . M4A,. m4v,. mov,. MP4   | [Fonte de arquivo MPEG-4](mpeg-4-file-source.md) | [**Coletor de arquivos MPEG-4**](mpeg-4-file-sink.md) | Windows 7                                                             |
| SAMI (intercâmbio de mídia acessível) sincronizado | . Sami,. SMI              | [Fonte de mídia SAMI](sami-media-source.md)   | Nenhum                                         | Windows Vista                                                         |
| ONDA                                             | .wav                     | Fonte de arquivo AVI                              | Nenhum                                         | Windows 7                                                             |



 

## <a name="audio-codecs"></a>Codecs de áudio



| Formatar                                              | Decodificador                                                                                                                                                          | Codificador                                                                                                                                                          | Exige      |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------|
| Codificação de μ-Law                                        | Codec do Gerenciador de compactação de áudio (ACM) μ-Law                                                                                                                      | Nenhum                                                                                                                                                             | Windows Vista |
| Modulação de código de pulso diferencial adaptável (ADPCM) | Codec ACM ADPCM                                                                                                                                                  | Nenhum                                                                                                                                                             | Windows Vista |
| AAC (codificação de áudio avançada)                         | [**Decodificador AAC**](aac-decoder.md)                                                                                                                               | [**Codificador AAC**](aac-encoder.md)                                                                                                                               | Windows 7     |
| MP3                                                 | [**Decodificador MP3 do Windows Media**](windows-media-mp3-decoder.md)                                                                                                   | Nenhum                                                                                                                                                             | Windows Vista |
| GSM 6.10                                            | Codec ACM GSM 6,10                                                                                                                                               | Nenhum                                                                                                                                                             | Windows Vista |
| Áudio do Windows Media (WMA)                           | [**Decodificador de áudio do Windows Media**](windowsmediaaudiodecoder.md)<br/> [**Decodificador de voz do Windows Media Audio**](windowsmediaaudiovoicedecoder.md)<br/> | [**Codificador de áudio do Windows Media**](windowsmediaaudioencoder.md)<br/> [**Codificador de voz do Windows Media Audio**](windowsmediaaudiovoiceencoder.md)<br/> | Windows Vista |



 

> [!Note]  
> Media Foundation fornece wrappers para vários codecs do ACM, listados na tabela anterior. No entanto, Media Foundation não dá suporte a codecs ACM arbitrários.

 

## <a name="video-codecs"></a>Codecs de vídeo



| Formatar                                                                                                         | Decodificador                                                                                                                                                                  | Codificador                                                                                                                             | Exige      |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|---------------|
| Vídeo DV                                                                                                       | [**Decodificador de vídeo DV**](dv-video-decoder.md)                                                                                                                             | Nenhum                                                                                                                                | Windows 7     |
| H.264                                                                                                          | [**Decodificador de vídeo H. 264**](h-264-video-decoder.md)                                                                                                                       | [**Codificador de vídeo H. 264**](h-264-video-encoder.md)                                                                                  | Windows 7     |
| H.263<br/> (Perfil de linha de base H. 264 que é compatível com o modo de cabeçalho de vídeo curto PT2 MPEG-4)<br/> | [**Decodificador de vídeo MPEG-4 parte 2**](mpeg4part2videodecoder.md)                                                                                                            | Nenhum                                                                                                                                | Windows 8     |
| MJPEG                                                                                                          | Decodificador de MJPEG                                                                                                                                                            | Nenhum                                                                                                                                | Windows 7     |
| MPEG-4, parte 2                                                                                                  | [**Decodificador de vídeo MPEG-4 parte 2**](mpeg4part2videodecoder.md)                                                                                                            | Nenhum                                                                                                                                | Windows 7     |
| MPEG-4 V1/V2/V3                                                                                                | [**Decodificador do Windows Media MPEG-4 v3**](./windowsmediampeg4v3decoder.md)<br/> [**Decodificador do Windows Media MPEG4 V1/V2**](windowsmediampeg4decoder.md)<br/>         | Nenhum                                                                                                                                | Windows Vista |
| Vídeo do Windows Media (WMV)                                                                                      | [**Decodificador do Windows Media Video 9**](windowsmediavideo9decoder.md)<br/> [**Decodificador de tela do Windows Media Video 9**](windowsmediavideo9screendecoder.md)<br/> | Codificador do Windows Media Video 9<br/> Codificador de tela do Windows Media Video 9<br/> Codificador de vídeo 7/8 do Windows Media<br/> | Windows Vista |



 

> [!Note]  
> A coluna "Requires" lista o sistema operacional mínimo necessário para usar esses codecs em um aplicativo Media Foundation. Alguns desses codecs foram introduzidos antes do Windows Vista como DMOS ( [DirectX Media Objects](../directshow/directx-media-objects.md) ). Se um codec der suporte à funcionalidade DMO, ele poderá ser usado com o [DirectShow](../directshow/directshow.md) ou com o [Windows Media Format SDK](../wmformat/windows-media-format-11-sdk.md).

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Objetos de codec](codecobjects.md)
</dt> <dt>

[Guia de programação Media Foundation](media-foundation-programming-guide.md)
</dt> <dt>

[Fontes de mídia e coletores](media-sources-and-sinks.md)
</dt> </dl>

 

 
