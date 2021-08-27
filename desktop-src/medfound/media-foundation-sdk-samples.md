---
description: Esta seção descreve os aplicativos de exemplo que demonstram como usar Media Foundation.Exemplos de codificaçãoPlayback SamplesPlug-InsSource Reader SamplesVideo CaptureMiscellaneous SamplesDeprecated ou Obsolete SamplesRelated topics
ms.assetid: 9d460107-ec12-4df5-a7a9-d19943685599
title: Exemplos de SDK do Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5482fabe5e4bfdfe5d451fd8ccb9c0ba0504a5ff
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482712"
---
# <a name="media-foundation-sdk-samples"></a>Exemplos de SDK do Media Foundation

Esta seção descreve os aplicativos de exemplo que demonstram como usar Media Foundation.

-   [Exemplos de codificação](#encoding-samples)
-   [Exemplos de reprodução](#playback-samples)
-   [Plug-ins](#plug-ins)
-   [Exemplos de leitor de origem](#source-reader-samples)
-   [Captura de vídeo](#video-capture)
-   [Exemplos diversos](#miscellaneous-samples)
-   [Exemplos preterido ou obsoletos](#deprecated-or-obsolete-samples)
-   [Tópicos relacionados](#related-topics)

## <a name="encoding-samples"></a>Exemplos de codificação



| Amostra                            | Descrição                                                 |
|-----------------------------------|-------------------------------------------------------------|
| [Transcodificar](transcode-sample.md) | Mostra como recodificar um arquivo de mídia para Windows mídia. |



 

## <a name="playback-samples"></a>Exemplos de reprodução



| Amostra                                            | Descrição                                                                                                                                                                                                     |
|---------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [BasicPlayback](/previous-versions//bb970475(v=vs.85))          | Reproduz arquivos de áudio e vídeo usando a Sessão [de Mídia](media-session.md). Este exemplo demonstra como criar topologias de reprodução, controlar a Sessão de Mídia e receber eventos de sessão durante a reprodução. |
| [MFPlayer](/previous-versions//bb970516(v=vs.85))                    | Demonstra algumas funções de reprodução que não estão incluídas no [exemplo BasicPlayback.](/previous-versions//bb970475(v=vs.85))                                                                                              |
| [ProtectedPlayback](protectedplayback-sample.md) | Reproduz arquivos de áudio e vídeo protegidos. Este exemplo mostra como usar a sessão PMP (caminho de mídia protegida) e como usar objetos do habilitador de conteúdo.                                                              |



 

## <a name="plug-ins"></a>Plug-Ins



| Amostra                                       | Sub-Area                         | Descrição                                                                                            |
|----------------------------------------------|----------------------------------|--------------------------------------------------------------------------------------------------------|
| [Decodificador](decoder-sample.md)                | Media Foundation transformação (MFT) | Decodificador de vídeo.                                                                                         |
| [EVRPresenter](evrpresenter-sample.md)      | Diversos                    | Apresentador personalizado para o [EVR (Renderizador](enhanced-video-renderer.md) de Vídeo Aprimorado).                 |
| [MFT \_ AudioDelay](mft-audiodelay-sample.md) | MFT                              | Transformação de efeito de áudio. Mostra como escrever um MFT básico para processamento de áudio.                           |
| [MFT \_ Grayscale](mft-grayscale-sample.md)   | MFT                              | Efeito de vídeo em escala de cinza. Mostra como escrever um MFT básico para processamento de vídeo.                           |
| [MPEG1Source](mpeg1source-sample.md)        | Fonte de mídia                     | Analisar fluxos de camada de sistemas MPEG-1. Mostra como escrever uma fonte de mídia personalizada e um manipulador de fluxo de byte. |
| [WavSink](wavsink-sample.md)                | Sink de mídia                       | Um sink de arquivo morto que grava arquivos .wav. Mostra como escrever um sink de mídia personalizado.                        |
| [WavSource](wavsource-sample.md)            | Fonte de mídia                     | Analisar arquivos .wav. Mostra como escrever uma fonte de mídia personalizada e um manipulador de fluxo de byte.                   |



 

## <a name="source-reader-samples"></a>Exemplos de leitor de origem



| Amostra                                      | Descrição                                                                         |
|---------------------------------------------|-------------------------------------------------------------------------------------|
| [Clipe de áudio](audio-clip-sample.md)         | Usa o [Leitor de Origem](source-reader.md) para decodificar o áudio de um arquivo de mídia.      |
| [VideoThumbnail](videothumbnail-sample.md) | Usa o [Leitor de Origem](source-reader.md) para obter quadros individuais de um arquivo de vídeo. |



 

## <a name="video-capture"></a>Captura de vídeo



| Amostra                                        | Descrição                                                                                 |
|-----------------------------------------------|---------------------------------------------------------------------------------------------|
| [MFCaptureD3D](mfcaptured3d-sample.md)       | Mostra como visualizar o vídeo de um dispositivo de captura de vídeo usando o Direct3D para renderizar o vídeo. |
| [MFCaptureToFile](mfcapturetofile-sample.md) | Mostra como capturar vídeo de uma câmera de vídeo para um arquivo.                                   |



 

## <a name="miscellaneous-samples"></a>Exemplos diversos



| Amostra                                         | Descrição                                                                                                                                           |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ASFParser](asfparser-sample.md)              | Mostra como analisar dados de um arquivo ASF (Advanced Systems Format).                                                                                   |
| [DXVA-HD](dxva-hd-sample.md)                  | Mostra como usar a DXVA-HD (Alta Definição de Aceleração de Vídeo) do Microsoft DirectX.                                                                      |
| [DXVA2 \_ VideoProc](dxva2-videoproc-sample.md) | Usa a DXVA (Aceleração de Vídeo) 2.0 do DirectX para criar um fluxo de vídeo 4:2:2 YUV. Este exemplo mostra como usar os recursos de processamento de vídeo do DXVA. |



 

## <a name="deprecated-or-obsolete-samples"></a>Exemplos preterido ou obsoletos




| Amostra | Descrição | 
|--------|-------------|
| <a href="mfplayer2-sample.md">MFPlayer2</a> | Demonstra alguns recursos avançados de reprodução da API <a href="using-mfplay-for-audio-video-playback.md">MFPlay.</a> | 
| <a href="/previous-versions//bb970336(v=vs.85)">PlaybackFX</a> | Aplica um efeito de escala de cinza ao vídeo. Mostra como inserir MFTs em uma topologia de reprodução.<br /><blockquote>[!Note]<br />Este exemplo não está mais incluído no SDK.</blockquote><br /> | 
| <a href="playlist-sample.md">Playlist</a> | Reproduz uma sequência de arquivos de áudio usando a origem do sequenciador.<br /><blockquote>[!Note]<br />Este exemplo não está mais incluído no SDK.</blockquote><br /> | 
| <a href="simplecapture-sample.md">SimpleCapture</a> | Mostra como visualizar o vídeo de um dispositivo de captura de vídeo usando a API MFPlay. | 
| <a href="simpleplay-sample.md">SimplePlay</a> | Mostra como reproduzir um arquivo de mídia usando a API MFPlay. | 




 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Microsoft Media Foundation](microsoft-media-foundation-sdk.md)
</dt> <dt>

[Sobre o Media Foundation](about-the-media-foundation-sdk.md)
</dt> </dl>

 

 
