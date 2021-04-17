---
description: Filtro de compressor de MJPEG
ms.assetid: de30a2c4-3e51-4f2b-b3f9-ed78e2d6512d
title: Filtro de compressor de MJPEG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a20c559bb889750959a4868fa08c03b3eb12dfb5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105812770"
---
# <a name="mjpeg-compressor-filter"></a>Filtro de compressor de MJPEG

Esse filtro compacta um fluxo de vídeo descompactado, usando a compactação JPEG de movimento.



|                                          |                                                                                                                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Filtrar interfaces                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), **IPersistStream**                                                                                                                                                                                             |
| Tipos de mídia de pino de entrada                    | \_vídeo de MediaType, MEDIASUBTYPE \_ nulo                                                                                                                                                                                                               |
| Interfaces de pino de entrada                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                             |
| Tipos de mídia do pino de saída                   | \_Vídeo de MediaType, MEDIASUBTYPE \_ MJPG                                                                                                                                                                                                               |
| Interfaces de pino de saída                    | [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| CLSID do filtro                             | \_MJPGENC CLSID                                                                                                                                                                                                                                     |
| CLSID de página de propriedades                      | Nenhuma página de propriedades                                                                                                                                                                                                                                   |
| Executável                               | quartz.dll                                                                                                                                                                                                                                         |
| [Núcleo](merit.md)                       | MÉRITO \_ \_ não \_ use                                                                                                                                                                                                                                |
| [Categoria do filtro](filter-categories.md) | \_VIDEOCOMPRESSORCATEGORY CLSID                                                                                                                                                                                                                     |



 

## <a name="remarks"></a>Comentários

Esse filtro codifica usando o subtipo de mídia MEDIASUBTYPE \_ MJPG, que corresponde ao código FOURCC ' MJPG '.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Filtros do DirectShow](directshow-filters.md)
</dt> </dl>

 

 



