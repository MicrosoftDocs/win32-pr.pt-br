---
description: Filtro de conversor de espaço de cor
ms.assetid: a6765184-43ce-47b8-9eb1-e15af7e11c93
title: Filtro de conversor de espaço de cor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6cadc3f980116f6745d578a06220639b181fe13
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477362"
---
# <a name="color-space-converter-filter"></a>Filtro de conversor de espaço de cor

Esse filtro de transformação converte de um tipo de cor RGB em outro tipo RGB, como entre cores RGB de 24 e 8 bits. Como esse tipo de conversão geralmente é tratado com mais eficiência em um descompactador de vídeo, o uso principal do conversor de espaço de cor é quando a origem do fluxo consiste em quadros RGB não compactados.




| | | Filtrar interfaces | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a> | | Tipos de mídia de pino de entrada | MEDIATYPE_Video, FORMAT_VideoInfo.<br /> Os seguintes subtipos são válidos:<br /><ul><li>MEDIASUBTYPE_RGB8</li><li>MEDIASUBTYPE_RGB555</li><li>MEDIASUBTYPE_RGB565</li><li>MEDIASUBTYPE_RGB24</li><li>MEDIASUBTYPE_RGB32</li></ul> | | Interfaces de pino de entrada | <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | | Tipos de mídia de pino de saída | MEDIATYPE_Video, FORMAT_VideoInfo.<br /> Os seguintes subtipos são válidos:<br /><ul><li>MEDIASUBTYPE_RGB8</li><li>MEDIASUBTYPE_RGB555</li><li>MEDIASUBTYPE_RGB565</li><li>MEDIASUBTYPE_RGB24</li><li>MEDIASUBTYPE_RGB32</li></ul> | | Interfaces de pino de saída | <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | | CLSID de filtro | CLSID_Colour | | CLSID da página de propriedades | Nenhuma página de propriedades. | | Executável | quartz.dll | | <a href="merit.md">Mérito</a> | MERIT_UNLIKELY | | <a href="filter-categories.md">Categoria do filtro</a> | CLSID_LegacyAmFilterCategory | 




 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DirectShow Filter](directshow-filters.md)
</dt> </dl>

 

 




