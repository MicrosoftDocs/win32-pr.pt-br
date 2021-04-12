---
description: Filtro de descompactação de MJPEG
ms.assetid: 0862fd8c-7e64-4472-9405-4d8e31e4401f
title: Filtro de descompactação de MJPEG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ebe8f5f19cb94d75c1ce01cd94dc723100560de
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500651"
---
# <a name="mjpeg-decompressor-filter"></a>Filtro de descompactação de MJPEG

Esse filtro decodifica um fluxo de vídeo do movimento JPEG para vídeo descompactado. Algumas câmeras de vídeo digital produzem um fluxo de vídeo JPEG de movimento.



|                                          |                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Filtrar interfaces                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                 |
| Tipos de mídia de pino de entrada                    | \_Vídeo de MediaType, MEDIASUBTYPE \_ MJPG                                                                                                               |
| Interfaces de pino de entrada                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                             |
| Tipos de mídia do pino de saída                   | \_vídeo de MediaType, MEDIASUBTYPE \_ nulo                                                                                                               |
| Interfaces de pino de saída                    | [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| CLSID do filtro                             | \_MJPEGDEC CLSID                                                                                                                                    |
| CLSID de página de propriedades                      | Nenhuma página de propriedades                                                                                                                                   |
| Executável                               | quartz.dll                                                                                                                                         |
| [Núcleo](merit.md)                       | MÉRITO \_ normal                                                                                                                                      |
| [Categoria do filtro](filter-categories.md) | \_LEGACYAMFILTERCATEGORY CLSID                                                                                                                      |



 

## <a name="remarks"></a>Comentários

Esse filtro é compatível com o vídeo JPEG de movimento que usa o código FOURCC ' MJPG '. Ele não pode decodificar outras variedades de JPEG de movimento. Para isso, será necessário usar um filtro de decodificador de terceiros.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Filtros do DirectShow](directshow-filters.md)
</dt> </dl>

 

 



