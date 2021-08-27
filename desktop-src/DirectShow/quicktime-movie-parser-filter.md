---
description: Filtro do Analisador de Filme de QuickTime
ms.assetid: 9537dd7b-9aeb-4e73-a31d-86053874ef13
title: Filtro do Analisador de Filme de QuickTime
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0028b604efe31749144ca98cb80057685ed0c1db
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983609"
---
# <a name="quicktime-movie-parser-filter"></a>Filtro do Analisador de Filme de QuickTime

Esse componente foi removido do Windows Vista e sistemas operacionais posteriores. Ele está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.

O filtro Analisador de Filmes de QuickTime divide os ® QuickTime® da Apple em fluxos de áudio e vídeo. Ele dá suporte ao QuickTime 2.0 e anterior. O pino de entrada se conecta a um filtro de origem, como o filtro Origem do Arquivo [Assíncrono](file-source--async--filter.md) ou o filtro Origem [do Arquivo de URL.](file-source--url--filter.md) O Analisador usa o filtro [Descompactador AVI](avi-decompressor-filter.md) ou [Descompactador QT](qt-decompressor-filter.md) para descompactar arquivos QuickTime. O filtro cria um pino de saída para o fluxo de vídeo e um pino de saída para o fluxo de áudio.




| Rótulo | Valor |
|--------|-------|
| Interfaces de filtro | <a href="/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent"><strong>IAMMediaContent,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"> <strong>IBaseFilter</strong></a> | 
| Tipos de mídia de pino de entrada | MEDIATYPE_Stream, MEDIASUBTYPE_QTMovie; | 
| Interfaces de pino de entrada | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a> | 
| Tipos de mídia de pino de saída | <ul><li>MEDIATYPE_Video, MEDIASUBTYPE_NULL, FORMAT_VideoInfo</li><li>MEDIATYPE_Audio, MEDIASUBTYPE_NULL, FORMAT_WaveFormatEx</li></ul> | 
| Interfaces de pino de saída | <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | 
| Filtrar CLSID | CLSID_QuickTimeParser | 
| CLSID da página de propriedades | Nenhuma página de propriedades. | 
| Executável | quartz.dll | 
| <a href="merit.md">Mérito</a> | MERIT_NORMAL | 
| <a href="filter-categories.md">Categoria de filtro</a> | CLSID_LegacyAmFilterCategory | 




 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> </dl>

 

 



