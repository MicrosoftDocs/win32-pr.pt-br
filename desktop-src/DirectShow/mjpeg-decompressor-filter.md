---
description: Filtro de descompactador MJPEG
ms.assetid: 0862fd8c-7e64-4472-9405-4d8e31e4401f
title: Filtro de descompactador MJPEG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34f0587abe77d1f76df043a37bc8e54db91d65d81e00b0a2677268b6d61bc782
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684936"
---
# <a name="mjpeg-decompressor-filter"></a>Filtro de descompactador MJPEG

Esse filtro decodifica um fluxo de vídeo do movimento JPEG para o vídeo descompactado. Algumas câmeras de vídeo digital produzem um fluxo de vídeo JPEG de movimento.



| Rótulo | Valor |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtro                        | [**Ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                 |
| Tipos de mídia de pino de entrada                    | MEDIATYPE \_ Video, MEDIASUBTYPE \_ MJPG                                                                                                               |
| Interfaces de pino de entrada                     | [**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                             |
| Tipos de mídia de pino de saída                   | MEDIATYPE \_ VIDEO, MEDIASUBTYPE \_ NULL                                                                                                               |
| Interfaces de pino de saída                    | [**IMediaPosition,**](/windows/desktop/api/Control/nn-control-imediaposition) [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| Filtrar CLSID                             | CLSID \_ MjpegDec                                                                                                                                    |
| CLSID da página de propriedades                      | Nenhuma página de propriedades                                                                                                                                   |
| Executável                               | quartz.dll                                                                                                                                         |
| [Mérito](merit.md)                       | NORMAL DE SEMPRE \_                                                                                                                                      |
| [Categoria de filtro](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                      |



 

## <a name="remarks"></a>Comentários

Esse filtro é compatível com o vídeo JPEG de movimento que usa o código FOURCC 'MJPG'. Ele não pode decodificar outras variedades de movimento JPEG. Para isso, você precisará usar um filtro de decodificador de terceiros.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> </dl>

 

 



