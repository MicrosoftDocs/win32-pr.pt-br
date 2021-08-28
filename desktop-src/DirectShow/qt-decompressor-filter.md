---
description: Filtro de descompactação de QT
ms.assetid: d013075f-deab-40ef-8438-4fb09820da3e
title: Filtro de descompactação de QT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cedb26acdcfabb3c0be4aeb2cbf306b654f9570
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983640"
---
# <a name="qt-decompressor-filter"></a>Filtro de descompactação de QT

este componente foi removido do Windows Vista e sistemas operacionais posteriores. ele está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.

O filtro de descompactação QT descompacta vídeo Apple® QuickTime® 2,0. Esse formato é normalmente usado em arquivos mais antigos do QuickTime.




| Rótulo | Valor |
|--------|-------|
| Filtrar interfaces | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a> | 
| Tipos de mídia de pino de entrada | MEDIATYPE_Video, FORMAT_VideoInfo<br /> Os seguintes subtipos são válidos:<br /><ul><li>MEDIASUBTYPE_QTRpza</li><li>MEDIASUBTYPE_QTSmc</li><li>MEDIASUBTYPE_QTRle</li><li>MEDIASUBTYPE_QTJpeg</li></ul> | 
| Interfaces de pino de entrada | <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | 
| Tipos de mídia do pino de saída | MEDIATYPE_Video, MEDIASUBTYPE_NULL, FORMAT_VideoInfo | 
| Interfaces de pino de saída | <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | 
| CLSID do filtro | CLSID_QTDec | 
| CLSID de página de propriedades | Nenhuma página de propriedades. | 
| Executável | quartz.dll | 
| <a href="merit.md">Núcleo</a> | MERIT_NORMAL | 
| <a href="filter-categories.md">Categoria do filtro</a> | CLSID_LegacyAmFilterCategory | 




 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DirectShow Filter](directshow-filters.md)
</dt> </dl>

 

 




