---
description: Expondo os formatos de captura e compactação
ms.assetid: f7466cfe-b13e-4ee9-82f9-0528ed97bf99
title: Expondo os formatos de captura e compactação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02051d9e68b3ad919b96dca53b674305787b3186
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103646184"
---
# <a name="exposing-capture-and-compression-formats"></a>Expondo os formatos de captura e compactação

Este artigo descreve como retornar formatos de captura e compactação usando o método [**IAMStreamConfig:: GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) . Esse método pode obter mais informações sobre os tipos de mídia aceitos do que a maneira tradicional de enumerar os tipos de mídia de um PIN, de modo que ele normalmente deve ser usado. **GetStreamCaps** pode retornar informações sobre os tipos de formatos permitidos para áudio ou vídeo. Além disso, este artigo fornece um código de exemplo que demonstra como reconectar o PIN de entrada de um filtro de transformação para garantir que o filtro possa produzir uma saída específica.

O método **GetStreamCaps** retorna uma matriz de pares de estruturas de tipo e recursos de mídia. O tipo de mídia é uma estrutura de [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) e os recursos são representados por uma estrutura de Caps de configuração de fluxo de áudio ou uma estrutura de [**Caps de configuração de fluxo de vídeo \_ \_ \_**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) . [**\_ \_ \_**](/windows/win32/api/strmif/ns-strmif-audio_stream_config_caps) A primeira seção deste artigo apresenta um exemplo de vídeo e o segundo apresenta um exemplo de áudio.

Este artigo contém os seguintes tópicos:

-   [Recursos de vídeo](video-capabilities.md)
-   [Recursos de áudio](audio-capabilities.md)
-   [Reconectando sua entrada para garantir tipos de saída específicos](reconnecting-your-input-to-ensure-specific-output-types.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gravando filtros do DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



