---
description: Filtro do analisador de filmes QuickTime
ms.assetid: 9537dd7b-9aeb-4e73-a31d-86053874ef13
title: Filtro do analisador de filmes QuickTime
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a65ba14cb748eb10c6afddf3e4747f11d68a4f9
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476712"
---
# <a name="quicktime-movie-parser-filter"></a>Filtro do analisador de filmes QuickTime

este componente foi removido do Windows Vista e sistemas operacionais posteriores. ele está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.

O filtro QuickTime Movie Parser divide os dados do Apple® QuickTime® em fluxos de áudio e vídeo. Ele dá suporte ao QuickTime 2,0 e anterior. O PIN de entrada se conecta a um filtro de origem, como o filtro de [origem de arquivo assíncrono](file-source--async--filter.md) ou o filtro de [origem de arquivo de URL](file-source--url--filter.md) . O analisador usa o filtro [AVI descompactador](avi-decompressor-filter.md) ou [Qt descompactador](qt-decompressor-filter.md) para descompactar arquivos QuickTime. O filtro cria um pino de saída para o fluxo de vídeo e um PIN de saída para o fluxo de áudio.




| | | Filtrar interfaces | <a href="/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent"><strong>IAMMediaContent</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a> | | Tipos de mídia de pino de entrada | MEDIATYPE_Stream, MEDIASUBTYPE_QTMovie; | | Interfaces de pino de entrada | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | | Tipos de mídia de pino de saída | <ul><li>MEDIATYPE_Video, MEDIASUBTYPE_NULL, FORMAT_VideoInfo</li><li>MEDIATYPE_Audio, MEDIASUBTYPE_NULL, FORMAT_WaveFormatEx</li></ul> | | Interfaces de pino de saída | <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | | CLSID de filtro | CLSID_QuickTimeParser | | CLSID da página de propriedades | Nenhuma página de propriedades. | | Executável | quartz.dll | | <a href="merit.md">Mérito</a> | MERIT_NORMAL | | <a href="filter-categories.md">Categoria do filtro</a> | CLSID_LegacyAmFilterCategory | 




 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DirectShow Filter](directshow-filters.md)
</dt> </dl>

 

 



