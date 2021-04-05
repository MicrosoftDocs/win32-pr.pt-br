---
description: Filtro de compressor AVI
ms.assetid: addde51d-2982-4964-b16a-406fea89a0ce
title: Filtro de compressor AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58f3ef342d1ea740503d9fc1e9e9b898aadc3801
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825481"
---
# <a name="avi-compressor-filter"></a>Filtro de compressor AVI

O filtro AVI compressor permite que os codecs do VCM (Gerenciador de compactação de vídeo) ingressem em um grafo de filtro. Cada codec aparece como uma instância separada do filtro. Você não pode criar esse filtro diretamente com CoCreateInstance. Em vez disso, você deve usar o enumerador de dispositivo do sistema. Para obter mais informações, consulte [usando o enumerador de dispositivo do sistema](using-the-system-device-enumerator.md).

O PIN de entrada do filtro se conecta a filtros que geram dados de vídeo não compactados, como filtros de captura de vídeo ou o [filtro de Splitter AVI](avi-splitter-filter.md). O pino de saída do filtro normalmente se conecta a um filtro MUX, como o [filtro AVI Mux](avi-mux-filter.md).

Se o codec der suporte a uma caixa de diálogo de configuração de VFW estilo antigo ou a caixa de diálogo sobre, um aplicativo poderá exibi-lo usando a interface [**IAMVfwCompressDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs) .

> [!Note]  
> Os compactadores MPEG nunca são implementados como codecs VCM, mas somente como filtros nativos do DirectShow.

 



|                                          |                                                                                                                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Filtrar interfaces                        | [**IAMVfwCompressDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), IPersistPropertyBag, ISpecifyPropertyPages                                                                                                             |
| Tipos de mídia de pino de entrada                    | \_Vídeo de MediaType, MEDIASUBTYPE \_ nulo                                                                                                                                                                                                               |
| Interfaces de pino de entrada                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                             |
| Tipos de mídia do pino de saída                   | \_Vídeo de MediaType, MEDIASUBTYPE \_ nulo                                                                                                                                                                                                               |
| Interfaces de pino de saída                    | [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| CLSID do filtro                             | Não aplicável                                                                                                                                                                                                                                     |
| CLSID de página de propriedades                      | Nenhuma página de propriedades.                                                                                                                                                                                                                                  |
| Executável                               | qcap.dll                                                                                                                                                                                                                                           |
| [Núcleo](merit.md)                       | MÉRITO \_ \_ não \_ use                                                                                                                                                                                                                                |
| [Categoria do filtro](filter-categories.md) | \_VIDEOCOMPRESSORCATEGORY CLSID                                                                                                                                                                                                                     |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Filtros do DirectShow](directshow-filters.md)
</dt> </dl>

 

 



