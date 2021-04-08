---
description: Filtro de origem do arquivo (URL)
ms.assetid: 405fd6ea-aa17-4d11-8f07-067468cb090b
title: Filtro de origem do arquivo (URL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: caea04b74a6880452210f1a43d5dfb29f8753dd3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087801"
---
# <a name="file-source-url-filter"></a>Filtro de origem do arquivo (URL)

O filtro de origem do arquivo de URL é um filtro de origem assíncrono genérico que funciona com qualquer arquivo de origem que pode ser identificado por um Uniform Resource Locator (URL) e cujo tipo principal de mídia é Stream. Isso inclui arquivos AVI, MOV, MPEG e WAV. Ele requer que o filtro downstream seja um analisador, como o [divisor de fluxo MPEG-1](mpeg-1-stream-splitter-filter.md), o [divisor AVI](avi-splitter-filter.md)ou o [analisador de filmes do QuickTime](quicktime-movie-parser-filter.md).



|                                          |                                                                                                                                      |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| Filtrar interfaces                        | [**IAMOpenProgress**](/windows/desktop/api/Strmif/nn-strmif-iamopenprogress), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter)       |
| Tipos de mídia de pino de entrada                    | Não aplicável                                                                                                                       |
| Interfaces de pino de entrada                     | Não aplicável                                                                                                                       |
| Tipos de mídia do pino de saída                   | Fluxo de MEDIATYPE \_ . O subtipo depende do formato de mídia. (MEDIASUBTYPE \_ NULL se o filtro não reconhecer o formato.)         |
| Interfaces de pino de saída                    | [**IAMAsyncReaderTimestampScaling**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling), [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) |
| CLSID do filtro                             | \_URLREADER CLSID                                                                                                                     |
| CLSID de página de propriedades                      | Nenhuma página de propriedades                                                                                                                     |
| Executável                               | quartz.dll                                                                                                                           |
| [Núcleo](merit.md)                       | MÉRITO \_ improvável                                                                                                                      |
| [Categoria do filtro](filter-categories.md) | \_LEGACYAMFILTERCATEGORY CLSID                                                                                                        |



 

## <a name="remarks"></a>Comentários

Esse filtro usa URLMon e oferece suporte a páginas de código.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Filtros do DirectShow](directshow-filters.md)
</dt> </dl>

 

 



