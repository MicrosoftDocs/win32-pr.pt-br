---
description: Filtro de compressor AVI
ms.assetid: addde51d-2982-4964-b16a-406fea89a0ce
title: Filtro de compressor AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa074f5ad4a72fe1e1a32f45baa4888a526b1a0532a562c2fadb7753ea71e0aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118159268"
---
# <a name="avi-compressor-filter"></a>Filtro de compressor AVI

O filtro AVI compressor permite que os codecs do VCM (Gerenciador de compactação de vídeo) ingressem em um grafo de filtro. Cada codec aparece como uma instância separada do filtro. Você não pode criar esse filtro diretamente com CoCreateInstance. Em vez disso, você deve usar o enumerador de dispositivo do sistema. Para obter mais informações, consulte [usando o enumerador de dispositivo do sistema](using-the-system-device-enumerator.md).

O PIN de entrada do filtro se conecta a filtros que geram dados de vídeo não compactados, como filtros de captura de vídeo ou o [filtro de Splitter AVI](avi-splitter-filter.md). O pino de saída do filtro normalmente se conecta a um filtro MUX, como o [filtro AVI Mux](avi-mux-filter.md).

Se o codec der suporte a uma caixa de diálogo de configuração de VFW estilo antigo ou a caixa de diálogo sobre, um aplicativo poderá exibi-lo usando a interface [**IAMVfwCompressDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs) .

> [!Note]  
> os compactadores MPEG nunca são implementados como codecs VCM, mas somente como filtros de DirectShow nativos.

 



| Rótulo | Valor |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Filtrar interfaces                        | [**IAMVfwCompressDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), IPersistPropertyBag, ISpecifyPropertyPages                                                                                                             |
| Tipos de mídia de pino de entrada                    | \_Vídeo de MediaType, MEDIASUBTYPE \_ nulo                                                                                                                                                                                                               |
| Interfaces de pino de entrada                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                             |
| Tipos de mídia do pino de saída                   | \_Vídeo de MediaType, MEDIASUBTYPE \_ nulo                                                                                                                                                                                                               |
| Interfaces de pino de saída                    | [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| CLSID do filtro                             | Não se aplica                                                                                                                                                                                                                                     |
| CLSID de página de propriedades                      | Nenhuma página de propriedades.                                                                                                                                                                                                                                  |
| Executável                               | qcap.dll                                                                                                                                                                                                                                           |
| [Núcleo](merit.md)                       | MÉRITO \_ \_ não \_ use                                                                                                                                                                                                                                |
| [Categoria do filtro](filter-categories.md) | \_VIDEOCOMPRESSORCATEGORY CLSID                                                                                                                                                                                                                     |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DirectShow Filter](directshow-filters.md)
</dt> </dl>

 

 



