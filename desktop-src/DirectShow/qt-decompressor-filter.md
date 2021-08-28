---
description: Filtro de descompactador QT
ms.assetid: d013075f-deab-40ef-8438-4fb09820da3e
title: Filtro de descompactador QT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d6f28058a1c729c9d42b20651a86ba31b4d98c7
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467963"
---
# <a name="qt-decompressor-filter"></a>Filtro de descompactador QT

Esse componente foi removido do Windows Vista e sistemas operacionais posteriores. Ele está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.

O filtro de descompactador QT descompacta o vídeo ® QuickTime® 2.0 da Apple. Normalmente, esse formato é usado em arquivos QuickTime mais antigos.




| | | Interfaces de filtro | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a> | | Tipos de mídia de pino de entrada | MEDIATYPE_Video, FORMAT_VideoInfo<br /> Os seguintes subtipos são válidos:<br /><ul><li>MEDIASUBTYPE_QTRpza</li><li>MEDIASUBTYPE_QTSmc</li><li>MEDIASUBTYPE_QTRle</li><li>MEDIASUBTYPE_QTJpeg</li></ul> | | Interfaces de pino de entrada | <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | | Tipos de mídia de pino de | MEDIATYPE_Video, MEDIASUBTYPE_NULL, FORMAT_VideoInfo | | Interfaces de pino de | <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | | Filtrar CLSID | CLSID_QTDec | | ClSID da página de propriedades | Nenhuma página de propriedades. | | Arquivo executável | quartz.dll | | <a href="merit.md">|</a> MERIT_NORMAL | | <a href="filter-categories.md">Categoria de</a> filtro | CLSID_LegacyAmFilterCategory | 




 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> </dl>

 

 




