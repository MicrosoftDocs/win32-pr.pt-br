---
description: Esta seção lista os tipos de mídia usados para dados MPEG-1.
ms.assetid: 4ea1cb84-0558-4c4a-9483-1b0f2a8f76f8
title: Tipos de Mídia MPEG-1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64f6486b455fc2045ceb0256f6b6344f06a8923ef767c397068022acec052627
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684926"
---
# <a name="mpeg-1-media-types"></a>Tipos de Mídia MPEG-1

Esta seção lista os tipos de mídia usados para dados MPEG-1.

## <a name="mpeg-1-system-stream"></a>MPEG-1 System Stream



| Rótulo | Valor |
|-----------------------|-------------------------------------------------|
| Tipo principal            | Fluxo \_ MEDIATYPE                               |
| Subtype               | MEDIASUBTYPE \_ MPEG1System                       |
| Tipo de formato           | FORMAT \_ MPEGStreams                             |
| Estrutura de formato      | [**AM \_ MPEGSYSTEMTYPE**](/previous-versions/windows/desktop/api/mpegtype/ns-mpegtype-am_mpegsystemtype) |
| Conteúdo de exemplo de mídia | Fluxo de byte; sem alinhamento                       |



 

## <a name="mpeg-1-system-stream-from-video-cd"></a>Fluxo do sistema MPEG-1 do CD de vídeo



| Rótulo | Valor |
|-----------------------|----------------------------|
| Tipo principal            | Fluxo \_ MEDIATYPE          |
| Subtype               | MEDIASUBTYPE \_ MPEG1VideoCD |
| Tipo de formato           | GUID \_ NULL                 |
| Estrutura de formato      | Nenhum                       |
| Conteúdo de exemplo de mídia | Fluxo de byte; sem alinhamento. |



 

## <a name="mpeg-1-audio-packet"></a>Pacote de Áudio MPEG-1



| Rótulo | Valor |
|-----------------------|------------------------------------------------|
| Tipo principal            | ÁUDIO \_ MEDIATYPE                               |
| Subtype               | MEDIASUBTYPE \_ MPEG1Packet                      |
| Tipo de formato           | FORMAT \_ WaveFormatEx                           |
| Estrutura de formato      | [**MPEG1WAVEFORMAT**](/windows/desktop/api/mmreg/ns-mmreg-mpeg1waveformat)     |
| Conteúdo de exemplo de mídia | Pacote MPEG-1 único, incluindo o header de pacote. |



 

## <a name="mpeg-1-audio-payload"></a>Conteúdo de áudio MPEG-1



| Rótulo | Valor |
|-----------------------|--------------------------------------------|
| Tipo principal            | ÁUDIO \_ MEDIATYPE                           |
| Subtype               | MEDIASUBTYPE \_ MPEG1Payload                 |
| Tipo de formato           | FORMAT \_ WaveFormatEx                       |
| Estrutura de formato      | [**MPEG1WAVEFORMAT**](/windows/desktop/api/mmreg/ns-mmreg-mpeg1waveformat) |
| Conteúdo de exemplo de mídia | Dados de áudio MPEG-1 alinhados por byte.            |



 

## <a name="mpeg-1-video-packet"></a>Pacote de vídeo MPEG-1



| Rótulo | Valor |
|-----------------------|------------------------------------------------|
| Tipo principal            | Vídeo \_ MEDIATYPE                               |
| Subtype               | MEDIASUBTYPE \_ MPEG1Packet                      |
| Tipo de formato           | FORMAT \_ MPEGVideo                              |
| Estrutura de formato      | [**MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo)       |
| Conteúdo de exemplo de mídia | Pacote MPEG-1 único, incluindo o header de pacote. |



 

## <a name="mpeg-1-video-payload"></a>Payload de vídeo MPEG-1



| Rótulo | Valor |
|-----------------------|------------------------------------------|
| Tipo principal            | Vídeo \_ MEDIATYPE                         |
| Subtype               | MEDIASUBTYPE \_ MPEG1Payload               |
| Tipo de formato           | FORMAT \_ MPEGVideo                        |
| Estrutura de formato      | [**MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo) |
| Conteúdo de exemplo de mídia | Dados de vídeo MPEG-1 alinhados a byte.          |



 

## <a name="mpeg-1-native-video-stream"></a>Fluxo de vídeo nativo do MPEG-1



| Rótulo | Valor |
|-----------------------|------------------------------------------------|
| Tipo principal            | Fluxo \_ MEDIATYPE                              |
| Subtype               | MEDIASUBTYPE \_ MPEG1Video                      |
| Tipo de formato           | GUID \_ NULL                                     |
| Estrutura de formato      | Nenhum                                           |
| Conteúdo de exemplo de mídia | Matriz de bytes de fluxo de vídeo (sem camada do sistema). |



 

## <a name="mpeg-1-native-audio-stream"></a>Fluxo de áudio nativo do MPEG-1



| Rótulo | Valor |
|-----------------------|------------------------------------------------|
| Tipo principal            | Fluxo \_ MEDIATYPE                              |
| Subtype               | MEDIASUBTYPE \_ MPEG1Audio                      |
| Tipo de formato           | GUID \_ NULL                                     |
| Estrutura de formato      | Nenhum                                           |
| Conteúdo de exemplo de mídia | Matriz de bytes de fluxo de áudio (sem camada do sistema). |



 

## <a name="remarks"></a>Comentários

Os DirectShow MPEG-1 são suportados por esses tipos da seguinte forma.



| Filtrar               | Direção | Tipos de mídia com suporte                                                                                             |
|----------------------|-----------|-------------------------------------------------------------------------------------------------------------------|
| Divisor MPEG-1      | Entrada     | Fluxo do sistema MPEG-1 streamMPEG-1 do CD de vídeo<br/>                                                 |
| Divisor MPEG-1      | Saída    | Conteúdo de áudio MPEG-1 PacketMPEG-1<br/> Pacote de vídeo MPEG-1<br/> Payload de vídeo MPEG-1<br/> |
| Software Audio Codec | Entrada     | Conteúdo de áudio MPEG-1 PacketMPEG-1<br/>                                                                |
| Codec de vídeo de software | Entrada     | Payload de vídeo MPEG-1 Video packetMPEG-1<br/>                                                                |
| Software Audio Codec | Saída    | Áudio pcm                                                                                                         |
| Codec de vídeo de software | Saída    | Vídeo descompactado (Y41P, YUY2, UYVY, RGB-24, RGB-32, RGB-565, RGB-555, RGB-8)                                    |



 

Os tipos de mídia de conteúdo e pacote de vídeo MPEG-1 contêm um header de sequência completo para que os dados possam ser reproduzir no meio de um arquivo sem a necessidade de um header de sequência para inicializar a reprodução de vídeo.

O header de sequência de vídeo é anexado ao tipo de dados de vídeo para vídeo MPEG para que a reprodução possa começar no meio de um fluxo. O comprimento desse campo é de até 140 bytes; ele inclui o código inicial do 0x000001B3 de sequência no início, juntamente com as matrizes de quantização encontradas no primeiro header de sequência encontrado.

 

 




