---
description: Funcionalidades de áudio
ms.assetid: de96f6ee-b526-4ac2-93ac-a731f86ef5d5
title: Funcionalidades de áudio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd12f3e151a73c2a297d10fec4233ac0e931e11d8bf16e1068f6335c781ed6da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117824226"
---
# <a name="audio-capabilities"></a>Funcionalidades de áudio

Para recursos de áudio, [**IAMStreamConfig::GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) retorna uma matriz de pares de estruturas [**CAPS DE CONFIGURAÇÃO \_ \_**](/windows/win32/api/strmif/ns-strmif-am_media_type) DE TIPO DE MÍDIA AM e FLUXO [**\_ DE \_ \_ ÁUDIO.**](/windows/win32/api/strmif/ns-strmif-audio_stream_config_caps) Assim como no vídeo, você pode usar isso para expor todos os tipos de recursos de áudio no pino, como a taxa de dados e se ele dá suporte a mono ou estéreo.

Para obter exemplos relacionados a vídeo relacionados a GetStreamCaps, consulte [Funcionalidades de vídeo](video-capabilities.md).

Suponha que você tenha suporte para formato de onda de PCM (modularidade de código de pulso) (conforme representado pela estrutura [**WAVEFORMATEX)**](/previous-versions/dd757713(v=vs.85)) a taxas de amostragem de 11.025, 22.050 e 44.100 amostras por segundo, tudo em 8 ou 16 bits mono ou estéreo. Nesse caso, você ofereceria dois pares de estruturas. O primeiro par teria uma estrutura de funcionalidade CAPS de **\_ \_ CONFIGURAÇÃO \_** DE FLUXO DE ÁUDIO que diz que você dá suporte a um mínimo de 11.025 a um máximo de 22.050 amostras por segundo com uma granularidade de 11.025 amostras por segundo (granularidade é a diferença entre os valores com suporte); um mínimo de 8 bits a um máximo de 16 bits por amostra com uma granularidade de 8 bits por exemplo; e mínimo de um canal e máximo de dois canais. O tipo de mídia do primeiro par seria o formato de PCM padrão nesse intervalo, talvez 22 quilohertz (kHz), estéreo de 16 bits. O segundo par seria uma funcionalidade mostrando 44.100 para amostras mínimas e máximas por segundo; Bits de 8 bits (mínimo) e 16 bits (máximo) por exemplo, com uma granularidade de 8 bits por exemplo; e mínimo de um canal e máximo de dois canais. O tipo de mídia seria o formato padrão de 44 kHz, talvez estéreo de 44 kHz de 16 bits.

Se você dá suporte a formatos de onda não PCM, o tipo de mídia retornado por esse método pode mostrar quais formatos não PCM você dá suporte (com uma taxa de exemplo padrão, taxa de bits e canais) e a estrutura de recursos que acompanha esse tipo de mídia pode descrever quais outras taxas de exemplo, taxas de bits e canais que você dá suporte.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Expondo formatos de captura e compactação](exposing-capture-and-compression-formats.md)
</dt> </dl>

 

 
