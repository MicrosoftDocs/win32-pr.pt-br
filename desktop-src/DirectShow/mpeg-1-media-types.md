---
description: Esta seção lista os tipos de mídia usados para dados MPEG-1.
ms.assetid: 4ea1cb84-0558-4c4a-9483-1b0f2a8f76f8
title: Tipos de mídia MPEG-1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e44db1f4423365efb7814d61b35c1985142aa14
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910024"
---
# <a name="mpeg-1-media-types"></a>Tipos de mídia MPEG-1

Esta seção lista os tipos de mídia usados para dados MPEG-1.

## <a name="mpeg-1-system-stream"></a>MPEG-1 System Stream



| Label | Valor |
|-----------------------|-------------------------------------------------|
| Tipo principal            | Fluxo de MEDIATYPE \_                               |
| Subtype               | MEDIASUBTYPE \_ MPEG1System                       |
| Tipo de formato           | MPEGStreams de formato \_                             |
| Estrutura de formato      | [**AM \_ MPEGSYSTEMTYPE**](/previous-versions/windows/desktop/api/mpegtype/ns-mpegtype-am_mpegsystemtype) |
| Conteúdo de exemplo de mídia | Fluxo de bytes; sem alinhamento                       |



 

## <a name="mpeg-1-system-stream-from-video-cd"></a>Fluxo do sistema MPEG-1 do CD de vídeo



| Label | Valor |
|-----------------------|----------------------------|
| Tipo principal            | Fluxo de MEDIATYPE \_          |
| Subtype               | MEDIASUBTYPE \_ MPEG1VideoCD |
| Tipo de formato           | GUID \_ nulo                 |
| Estrutura de formato      | Nenhum                       |
| Conteúdo de exemplo de mídia | Fluxo de bytes; sem alinhamento. |



 

## <a name="mpeg-1-audio-packet"></a>Pacote de áudio MPEG-1



| Label | Valor |
|-----------------------|------------------------------------------------|
| Tipo principal            | Áudio de MEDIATYPE \_                               |
| Subtype               | MEDIASUBTYPE \_ MPEG1Packet                      |
| Tipo de formato           | WaveFormatEx de formato \_                           |
| Estrutura de formato      | [**MPEG1WAVEFORMAT**](/windows/desktop/api/mmreg/ns-mmreg-mpeg1waveformat)     |
| Conteúdo de exemplo de mídia | Pacote único MPEG-1, incluindo o cabeçalho do pacote. |



 

## <a name="mpeg-1-audio-payload"></a>Carga de áudio MPEG-1



| Label | Valor |
|-----------------------|--------------------------------------------|
| Tipo principal            | Áudio de MEDIATYPE \_                           |
| Subtype               | MEDIASUBTYPE \_ MPEG1Payload                 |
| Tipo de formato           | WaveFormatEx de formato \_                       |
| Estrutura de formato      | [**MPEG1WAVEFORMAT**](/windows/desktop/api/mmreg/ns-mmreg-mpeg1waveformat) |
| Conteúdo de exemplo de mídia | Dados de áudio MPEG-1 alinhados em byte.            |



 

## <a name="mpeg-1-video-packet"></a>Pacote de vídeo MPEG-1



| Label | Valor |
|-----------------------|------------------------------------------------|
| Tipo principal            | Vídeo de MEDIATYPE \_                               |
| Subtype               | MEDIASUBTYPE \_ MPEG1Packet                      |
| Tipo de formato           | MPEGVideo de formato \_                              |
| Estrutura de formato      | [**MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo)       |
| Conteúdo de exemplo de mídia | Pacote único MPEG-1, incluindo o cabeçalho do pacote. |



 

## <a name="mpeg-1-video-payload"></a>Carga de vídeo MPEG-1



| Label | Valor |
|-----------------------|------------------------------------------|
| Tipo principal            | Vídeo de MEDIATYPE \_                         |
| Subtype               | MEDIASUBTYPE \_ MPEG1Payload               |
| Tipo de formato           | MPEGVideo de formato \_                        |
| Estrutura de formato      | [**MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo) |
| Conteúdo de exemplo de mídia | Dados de vídeo MPEG-1 alinhados em byte.          |



 

## <a name="mpeg-1-native-video-stream"></a>Fluxo de vídeo nativo MPEG-1



| Label | Valor |
|-----------------------|------------------------------------------------|
| Tipo principal            | Fluxo de MEDIATYPE \_                              |
| Subtype               | MEDIASUBTYPE \_ MPEG1Video                      |
| Tipo de formato           | GUID \_ nulo                                     |
| Estrutura de formato      | Nenhum                                           |
| Conteúdo de exemplo de mídia | Matriz de bytes de fluxo de vídeo (sem camada do sistema). |



 

## <a name="mpeg-1-native-audio-stream"></a>Fluxo de áudio nativo MPEG-1



| Label | Valor |
|-----------------------|------------------------------------------------|
| Tipo principal            | Fluxo de MEDIATYPE \_                              |
| Subtype               | MEDIASUBTYPE \_ MPEG1Audio                      |
| Tipo de formato           | GUID \_ nulo                                     |
| Estrutura de formato      | Nenhum                                           |
| Conteúdo de exemplo de mídia | Matriz de bytes de fluxo de áudio (sem camada do sistema). |



 

## <a name="remarks"></a>Comentários

Os filtros MPEG-1 do DirectShow dão suporte a esses tipos da seguinte maneira.



| Filtrar               | Direção | Tipos de mídia com suporte                                                                                             |
|----------------------|-----------|-------------------------------------------------------------------------------------------------------------------|
| Divisor MPEG-1      | Entrada     | Fluxo do sistema streamMPEG-1 do sistema MPEG-1 do CD de vídeo<br/>                                                 |
| Divisor MPEG-1      | Saída    | Carga de áudio MPEG-1 audio packetMPEG-1<br/> Pacote de vídeo MPEG-1<br/> Carga de vídeo MPEG-1<br/> |
| Codec de áudio de software | Entrada     | Carga de áudio MPEG-1 audio packetMPEG-1<br/>                                                                |
| Codec de vídeo de software | Entrada     | Carga de vídeo MPEG-1 Video packetMPEG-1<br/>                                                                |
| Codec de áudio de software | Saída    | Áudio PCM                                                                                                         |
| Codec de vídeo de software | Saída    | Vídeo descompactado (Y41P, YUY2, UYVY, RGB-24, RGB-32, RGB-565, RGB-555, RGB-8)                                    |



 

O pacote de vídeo MPEG-1 e os tipos de mídia de carga contêm um cabeçalho de sequência completo para que os dados possam ser reproduzidos do meio de um arquivo sem precisar de um cabeçalho de sequência para inicializar a reprodução do vídeo.

O cabeçalho de sequência de vídeo é anexado ao tipo de dados vídeo para vídeo MPEG para que a reprodução possa começar do meio de um fluxo. O comprimento deste campo é de até 140 bytes; Ele inclui o código de início do cabeçalho de sequência (0x000001B3) no início, juntamente com todas as matrizes de quantização encontradas no primeiro cabeçalho de sequência encontrado.

 

 




