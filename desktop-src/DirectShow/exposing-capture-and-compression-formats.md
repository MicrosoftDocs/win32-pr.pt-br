---
description: Expondo formatos de captura e compactação
ms.assetid: f7466cfe-b13e-4ee9-82f9-0528ed97bf99
title: Expondo formatos de captura e compactação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d80821ade82b894a7c3e2752528ffdd72bc2223a4616b629f7e2b236461b31e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119685736"
---
# <a name="exposing-capture-and-compression-formats"></a>Expondo formatos de captura e compactação

Este artigo descreve como retornar formatos de captura e compactação usando o [**método IAMStreamConfig::GetStreamCaps.**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) Esse método pode obter mais informações sobre tipos de mídia aceitos do que a maneira tradicional de enumerar os tipos de mídia de um pino, portanto, ele normalmente deve ser usado em vez disso. **GetStreamCaps** pode retornar informações sobre os tipos de formatos permitidos para áudio ou vídeo. Além disso, este artigo fornece um código de exemplo que demonstra como reconectar o pino de entrada de um filtro de transformação para garantir que o filtro possa produzir uma saída específica.

O **método GetStreamCaps** retorna uma matriz de pares de estruturas de tipos de mídia e recursos. O tipo de mídia é uma [**estrutura AM \_ MEDIA \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) e os recursos são representados por uma estrutura CAPS de [**\_ \_ CONFIGURAÇÃO \_**](/windows/win32/api/strmif/ns-strmif-audio_stream_config_caps) DE FLUXO DE ÁUDIO ou uma estrutura CAPS DE [**\_ \_ CONFIGURAÇÃO DE \_**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) FLUXO DE VÍDEO. A primeira seção deste artigo apresenta um exemplo de vídeo e a segunda apresenta um exemplo de áudio.

Este artigo contém os seguintes tópicos:

-   [Funcionalidades de vídeo](video-capabilities.md)
-   [Funcionalidades de áudio](audio-capabilities.md)
-   [Reconectar sua entrada para garantir tipos de saída específicos](reconnecting-your-input-to-ensure-specific-output-types.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Escrevendo DirectShow filtros](writing-directshow-filters.md)
</dt> </dl>

 

 



