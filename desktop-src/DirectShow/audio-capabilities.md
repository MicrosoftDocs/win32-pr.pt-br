---
description: Recursos de áudio
ms.assetid: de96f6ee-b526-4ac2-93ac-a731f86ef5d5
title: Recursos de áudio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c2cf02927b69d807f400c4185a7d4ddbdd14322
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500669"
---
# <a name="audio-capabilities"></a>Recursos de áudio

Para recursos de áudio, [**IAMStreamConfig:: GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) retorna uma matriz de pares das estruturas de [**Caps de \_ \_ configuração de \_ fluxo de áudio**](/windows/win32/api/strmif/ns-strmif-audio_stream_config_caps) e de [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) . Assim como acontece com o vídeo, você pode usar isso para expor todos os tipos de recursos de áudio no PIN, como a taxa de dados e se ele dá suporte a mono ou estéreo.

Para obter exemplos de vídeo relacionados ao GetStreamCaps, consulte [recursos de vídeo](video-capabilities.md).

Suponha que você ofereça suporte ao formato Wave de codificação de código de pulso (PCM) (conforme representado pela estrutura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) ) em taxas de amostragem de 11.025, 22.050 e 44.100 amostras por segundo, tudo em mono ou estéreo de 8 ou 16 bits. Nesse caso, você ofereceria dois pares de estruturas. O primeiro par teria uma estrutura de capacidade de configuração de fluxo de áudio, dizendo que você dá suporte a um mínimo de 11.025 a um máximo de 22.050 amostras por segundo com uma granularidade de 11.025 amostras por segundo (a granularidade é a diferença entre os valores com suporte); um mínimo de 8 bits para um máximo de bits de 16 bits por amostra com uma granularidade de 8 bits por amostra; e o máximo de um canal e mínimo de dois canais. **\_ \_ \_** O tipo de mídia do primeiro par seria o formato PCM padrão nesse intervalo, talvez 22 kilohertz (kHz), estéreo de 16 bits. Seu segundo par seria um recurso que mostra 44.100 para os exemplos mínimo e máximo por segundo; bits de 8 bits (mínimo) e 16 bits (máximo) por amostra, com uma granularidade de 8 bits por amostra; e o mínimo de um canal e o máximo de dois canais. O tipo de mídia seria o formato padrão de 44 kHz, talvez 44 kHz de 16 bits.

Se você der suporte a formatos Wave não PCM, o tipo de mídia retornado por esse método poderá mostrar a quais formatos não PCM são suportados (com uma taxa de amostragem padrão, taxa de bits e canais) e a estrutura de recursos que acompanha esse tipo de mídia pode descrever quais outras taxas de amostra, taxas de bits e canais são suportados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Expondo os formatos de captura e compactação](exposing-capture-and-compression-formats.md)
</dt> </dl>

 

 
