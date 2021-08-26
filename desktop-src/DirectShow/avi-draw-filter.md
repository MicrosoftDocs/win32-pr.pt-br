---
description: Filtro de desenho DE AVI
ms.assetid: 86cd8e48-7cfa-46e4-b8f4-609b4d09fe80
title: Filtro de desenho DE AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 003336a68bdc1591e6e9a3f8af139f4bf27ddc4d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471272"
---
# <a name="avi-draw-filter"></a>Filtro de desenho DE AVI

O filtro Desenho DE AVI é retirado automaticamente para um grafo de reprodução em vez do [Descompactador AVI](avi-decompressor-filter.md) quando o vídeo está sendo gerado para um monitor de tv NTSC externo.




| | | Interfaces de filtro | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a> | | Tipos de mídia de pino de entrada | Tipo principal: MEDIATYPE_VideoSubtypes:<br /><ul><li>MEDIASUBTYPE_MJPG</li><li>MEDIASUBTYPE_TVMJ</li><li>MEDIASUBTYPE_WAKE</li><li>MEDIASUBTYPE_CFCC</li><li>MEDIASUBTYPE_IJPG</li><li>MEDIASUBTYPE_Plum</li><li>MEDIASUBTYPE_DVCS</li><li>MEDIASUBTYPE_DVSD</li><li>MEDIASUBTYPE_MDVF</li><li>Tipo de formato: FORMAT_VideoInfo</li></ul> | | Interfaces de pino de entrada | <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | | Tipos de mídia de pino de | MEDIATYPE_Video, MEDIASUBTYPE_NULL | | Interfaces de pino de | <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ioverlaynotify"><strong>IOverlayNotify,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | | Filtrar CLSID | CLSID_AVIDraw | | ClSID da página de propriedades | Nenhuma página de propriedades. | | Arquivo executável | quartz.dll | | <a href="merit.md">|</a> MERIT_NORMAL + 100 | | <a href="filter-categories.md">Categoria de</a> filtro | CLSID_LegacyAmFilterCategory | 




 

## <a name="remarks"></a>Comentários

Como o filtro Desenho DE AVI e o [Filtro de Captura VFW](vfw-capture-filter.md) se conectam ao mesmo hardware, eles não podem estar no mesmo grafo de filtro.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> </dl>

 

 




