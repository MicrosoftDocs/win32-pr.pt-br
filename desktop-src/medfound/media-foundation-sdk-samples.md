---
description: Esta seção descreve os aplicativos de exemplo que demonstram como usar os tópicos Media Foundation. Encoding SamplesPlayback SamplesPlug-InsSource Reader SamplesVideo CaptureMiscellaneous SamplesDeprecated ou obsoletos SamplesRelated
ms.assetid: 9d460107-ec12-4df5-a7a9-d19943685599
title: Exemplos de SDK do Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa7d07d4136e613b4c6b553aa089834f58ccf65b6b87043ec5148d8db4ee6547
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119465137"
---
# <a name="media-foundation-sdk-samples"></a>Exemplos de SDK do Media Foundation

Esta seção descreve os aplicativos de exemplo que demonstram como usar Media Foundation.

-   [Exemplos de codificação](#encoding-samples)
-   [Exemplos de reprodução](#playback-samples)
-   [Plug-ins](#plug-ins)
-   [Amostras do leitor de origem](#source-reader-samples)
-   [Captura de vídeo](#video-capture)
-   [Exemplos diversos](#miscellaneous-samples)
-   [Amostras preteridas ou obsoletas](#deprecated-or-obsolete-samples)
-   [Tópicos relacionados](#related-topics)

## <a name="encoding-samples"></a>Exemplos de codificação



| Amostra                            | Descrição                                                 |
|-----------------------------------|-------------------------------------------------------------|
| [Codificação](transcode-sample.md) | mostra como recodificar um arquivo de mídia para Windows formato de mídia. |



 

## <a name="playback-samples"></a>Exemplos de reprodução



| Amostra                                            | Descrição                                                                                                                                                                                                     |
|---------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [BasicPlayback](/previous-versions//bb970475(v=vs.85))          | Reproduz arquivos de áudio e vídeo usando a [sessão de mídia](media-session.md). Este exemplo demonstra como criar topologias de reprodução, controlar a sessão de mídia e receber eventos de sessão durante a reprodução. |
| [MFPlayer](/previous-versions//bb970516(v=vs.85))                    | Demonstra algumas funções de reprodução que não estão incluídas no exemplo [BasicPlayback](/previous-versions//bb970475(v=vs.85)) .                                                                                              |
| [ProtectedPlayback](protectedplayback-sample.md) | Reproduz arquivos de áudio e vídeo protegidos. Este exemplo mostra como usar a sessão do caminho de mídia protegida (PMP) e como usar objetos de habilitação de conteúdo.                                                              |



 

## <a name="plug-ins"></a>Plug-Ins



| Amostra                                       | Sub-Area                         | Descrição                                                                                            |
|----------------------------------------------|----------------------------------|--------------------------------------------------------------------------------------------------------|
| [Decodificador](decoder-sample.md)                | Media Foundation transformação (MFT) | Decodificador de vídeo.                                                                                         |
| [EVRPresenter](evrpresenter-sample.md)      | Diversos                    | Apresentador personalizado para o [processador de vídeo avançado](enhanced-video-renderer.md) (EVR).                 |
| [\_AUDIODELAY MFT](mft-audiodelay-sample.md) | MFT                              | Transformação de efeito de áudio. Mostra como gravar um MFT básico para processamento de áudio.                           |
| [Escala de cinza da MFT \_](mft-grayscale-sample.md)   | MFT                              | Efeito de vídeo em escala de cinza. Mostra como gravar um MFT básico para processamento de vídeo.                           |
| [MPEG1Source](mpeg1source-sample.md)        | Origem da mídia                     | Analisa os fluxos de camada de sistemas MPEG-1. Mostra como gravar uma fonte de mídia personalizada e um manipulador de fluxo de bytes. |
| [WavSink](wavsink-sample.md)                | Coletor de mídia                       | Um coletor de arquivo que grava arquivos. wav. Mostra como gravar um coletor de mídia personalizado.                        |
| [WavSource](wavsource-sample.md)            | Origem da mídia                     | Analisa arquivos. wav. Mostra como gravar uma fonte de mídia personalizada e um manipulador de fluxo de bytes.                   |



 

## <a name="source-reader-samples"></a>Amostras do leitor de origem



| Amostra                                      | Descrição                                                                         |
|---------------------------------------------|-------------------------------------------------------------------------------------|
| [Clipe de áudio](audio-clip-sample.md)         | Usa o [leitor de origem](source-reader.md) para decodificar áudio de um arquivo de mídia.      |
| [VideoThumbnail](videothumbnail-sample.md) | Usa o [leitor de origem](source-reader.md) para obter quadros únicos de um arquivo de vídeo. |



 

## <a name="video-capture"></a>Captura de vídeo



| Amostra                                        | Descrição                                                                                 |
|-----------------------------------------------|---------------------------------------------------------------------------------------------|
| [MFCaptureD3D](mfcaptured3d-sample.md)       | Mostra como visualizar o vídeo de um dispositivo de captura de vídeo, usando o Direct3D para renderizar o vídeo. |
| [MFCaptureToFile](mfcapturetofile-sample.md) | Mostra como capturar vídeo de uma câmera de vídeo para um arquivo.                                   |



 

## <a name="miscellaneous-samples"></a>Exemplos diversos



| Amostra                                         | Descrição                                                                                                                                           |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ASFParser](asfparser-sample.md)              | Mostra como analisar dados de um arquivo ASF (Advanced Systems Format).                                                                                   |
| [DXVA-HD](dxva-hd-sample.md)                  | Mostra como usar o Microsoft DirectX vídeo Acceleration High Definition (DXVA-HD).                                                                      |
| [DXVA2 \_ VideoProc](dxva2-videoproc-sample.md) | Usa a DXVA (DirectX Video Acceleration) 2,0 para criar um fluxo de vídeo YUV de 4:2:2. Este exemplo mostra como usar os recursos de processamento de vídeo do DXVA. |



 

## <a name="deprecated-or-obsolete-samples"></a>Amostras preteridas ou obsoletas



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Amostra</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mfplayer2-sample.md">MFPlayer2</a></td>
<td>Demonstra alguns recursos avançados de reprodução da API do <a href="using-mfplay-for-audio-video-playback.md">MFPlay</a> .</td>
</tr>
<tr class="even">
<td><a href="/previous-versions//bb970336(v=vs.85)">PlaybackFX</a></td>
<td>Aplica um efeito de escala de cinza ao vídeo. Mostra como inserir MFTs em uma topologia de reprodução.<br/>
<blockquote>
[!Note]<br />
Este exemplo não está mais incluído no SDK.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="playlist-sample.md">Playlist</a></td>
<td>Reproduz uma sequência de arquivos de áudio usando a origem do sequenciador.<br/>
<blockquote>
[!Note]<br />
Este exemplo não está mais incluído no SDK.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="simplecapture-sample.md">SimpleCapture</a></td>
<td>Mostra como visualizar o vídeo de um dispositivo de captura de vídeo usando a API MFPlay.</td>
</tr>
<tr class="odd">
<td><a href="simpleplay-sample.md">SimplePlay</a></td>
<td>Mostra como reproduzir um arquivo de mídia usando a API MFPlay.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Microsoft Media Foundation](microsoft-media-foundation-sdk.md)
</dt> <dt>

[Sobre o Media Foundation](about-the-media-foundation-sdk.md)
</dt> </dl>

 

 
