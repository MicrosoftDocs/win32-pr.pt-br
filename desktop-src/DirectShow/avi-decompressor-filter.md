---
description: Filtro de descompactação AVI
ms.assetid: 6a9914db-483a-429c-9b26-9451578951c9
title: Filtro de descompactação AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 214ccfeee18a01fa9c8d52ffbf4593b9de5664bb
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910094"
---
# <a name="avi-decompressor-filter"></a>Filtro de descompactação AVI

O filtro do descompactador AVI permite que os codecs VCM (Gerenciador de compactação de vídeo) ingressem em um grafo de filtro. O aplicativo não precisa adicionar o filtro ao grafo de filtro; Ele é retirado automaticamente pelo Gerenciador de gráficos de filtro quando necessário.

Quando o Gerenciador de gráfico de filtro está criando um grafo para renderizar um arquivo AVI, ele verifica o FOURCC no cabeçalho AVI do arquivo para determinar se o fluxo de vídeo está compactado. Se for, o Gerenciador de gráficos de filtro adicionará o descompactador AVI, que então pesquisará o registro em busca de um descompactador instalado que possa manipular o arquivo.

> [!Note]  
> Os decompactadores MPEG nunca são implementados como codecs VCM, mas somente como filtros nativos do DirectShow.

 

Em seu PIN de upstream, o descompactador AVI normalmente se conecta ao [divisor AVI](avi-splitter-filter.md). Em seu pino de saída, ele normalmente se conecta ao [processador de vídeo](video-renderer-filter.md) ou ao [filtro AVI Mux](avi-mux-filter.md).



| Label | Valor |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Filtrar interfaces                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                                                                                 |
| Tipos de mídia de pino de entrada                    | Tipo principal: MEDIATYPE \_ VideoSubtype: deve corresponder ao código FOURCC para o tipo de compactação. Para obter mais informações, consulte [Códigos FOURCC](fourcc-codes.md).<br/> Tipo de formato: formato \_ VIDEOINFO<br/> |
| Interfaces de pino de entrada                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                             |
| Tipos de mídia do pino de saída                   | \_Vídeo de MediaType, MEDIASUBTYPE \_ NULL, Format \_ VIDEOINFO                                                                                                                                                            |
| Interfaces de pino de saída                    | [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                 |
| CLSID do filtro                             | \_AVIDEC CLSID                                                                                                                                                                                                      |
| CLSID de página de propriedades                      | Nenhuma página de propriedades.                                                                                                                                                                                                  |
| Executável                               | quartz.dll                                                                                                                                                                                                         |
| [Núcleo](merit.md)                       | MÉRITO \_ normal                                                                                                                                                                                                      |
| [Categoria do filtro](filter-categories.md) | \_LEGACYAMFILTERCATEGORY CLSID                                                                                                                                                                                      |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Filtros do DirectShow](directshow-filters.md)
</dt> </dl>

 

 




