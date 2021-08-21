---
description: Filtro MJPEG Ltda
ms.assetid: de30a2c4-3e51-4f2b-b3f9-ed78e2d6512d
title: Filtro MJPEG Ltda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7891a85aa32b0ec7572a8c3be08f216c75f8655a7782261a675521aa952bf40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119791386"
---
# <a name="mjpeg-compressor-filter"></a>Filtro MJPEG Ltda

Esse filtro compacta um fluxo de vídeo descompactado usando a compactação JPEG de movimento.



| Rótulo | Valor |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtro                        | [**IBaseFilter,**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) **IPersistStream**                                                                                                                                                                                             |
| Tipos de mídia de pino de entrada                    | MEDIATYPE \_ VIDEO, MEDIASUBTYPE \_ NULL                                                                                                                                                                                                               |
| Interfaces de pino de entrada                     | [**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                             |
| Tipos de mídia de pino de saída                   | MEDIATYPE \_ Video, MEDIASUBTYPE \_ MJPG                                                                                                                                                                                                               |
| Interfaces de pino de saída                    | [**IAMStreamConfig,**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) [**IAMVideoCompression,**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) [**IMediaPosition,**](/windows/desktop/api/Control/nn-control-imediaposition) [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| Filtrar CLSID                             | CLSID \_ MJPGEnc                                                                                                                                                                                                                                     |
| CLSID da página de propriedades                      | Nenhuma página de propriedades                                                                                                                                                                                                                                   |
| Executável                               | quartz.dll                                                                                                                                                                                                                                         |
| [Mérito](merit.md)                       | NÃO USE O NÃO \_ \_ USO \_ DE LIMITED                                                                                                                                                                                                                                |
| [Categoria de filtro](filter-categories.md) | CLSID \_ VideoCompressorCategory                                                                                                                                                                                                                     |



 

## <a name="remarks"></a>Comentários

Esse filtro codifica usando o subtipo de mídia MEDIASUBTYPE MJPG, que corresponde ao \_ código FOURCC 'MJPG'.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> </dl>

 

 



