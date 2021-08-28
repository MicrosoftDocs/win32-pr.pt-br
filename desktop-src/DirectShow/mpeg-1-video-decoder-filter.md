---
description: Filtro de decodificador de vídeo MPEG-1
ms.assetid: 272d2f31-6e57-4ce5-ac86-b4d47f661fea
title: Filtro de decodificador de vídeo MPEG-1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf865d0e8cf45bcbde20a2d5b6f4035a4a17f970
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468223"
---
# <a name="mpeg-1-video-decoder-filter"></a>Filtro de decodificador de vídeo MPEG-1

Decodifica o vídeo MPEG-1.




| | | Interfaces de filtro | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter,</strong></a> <strong>ISpecifyPropertyPages</strong> | | Tipos de mídia de pino de entrada | MEDIATYPE_Video, FORMAT_MPEGVideo<br /> Os seguintes subtipos são válidos:<br /><ul><li><strong>MEDIASUBTYPE_MPEG1Packet</strong></li><li><strong>MEDIASUBTYPE_MPEG1Payload</strong></li></ul> | | Interfaces de pino de entrada | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin | |</strong></a> Tipos de mídia de pino de | Tipo principal: <strong>MEDIATYPE_Video</strong>,<br /> Tipo de formato: <strong>FORMAT_VideoInfo</strong> ou <strong>FORMAT_VideoInfo2</strong><br /> Subtipos:<br /><ul><li><strong>MEDIASUBTYPE_RGB24</strong></li><li><strong>MEDIASUBTYPE_RGB32</strong></li><li><strong>MEDIASUBTYPE_RGB8</strong></li><li><strong>MEDIASUBTYPE_RGB555</strong></li><li><strong>MEDIASUBTYPE_RGB565</strong></li><li><strong>MEDIASUBTYPE_UYVY</strong></li><li><strong>MEDIASUBTYPE_Y41P</strong></li><li><strong>MEDIASUBTYPE_YUY2</strong></li></ul> | | Interfaces de pino de | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | | Filtrar CLSID | <strong>CLSID_CMpegVideoCodec</strong> | | ClSID da página de propriedades | <strong>CLSID_MpegVideoDecodePropertyPage</strong> | | Arquivo executável | quartz.dll | | <a href="merit.md">|</a> 0x40000001 | | <a href="filter-categories.md">Categoria de</a> filtro | CLSID_LegacyAmFilterCategory | 




 

## <a name="remarks"></a>Comentários

Esse filtro pode decodificar em uma Superfície directDraw. O filtro usará MMX se o computador for compatível com MMX.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> </dl>

 

 




