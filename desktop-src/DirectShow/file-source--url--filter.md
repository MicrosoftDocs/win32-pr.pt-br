---
description: Filtro de origem do arquivo (URL)
ms.assetid: 405fd6ea-aa17-4d11-8f07-067468cb090b
title: Filtro de origem do arquivo (URL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a096d25e5e04246385ece9662ed93e209115756491b1a3581cbb01de38225e66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119685616"
---
# <a name="file-source-url-filter"></a>Filtro de origem do arquivo (URL)

O filtro de origem do arquivo de URL é um filtro de origem assíncrono genérico que funciona com qualquer arquivo de origem que pode ser identificado por um Uniform Resource Locator (URL) e cujo tipo principal de mídia é Stream. Isso inclui arquivos AVI, MOV, MPEG e WAV. Ele requer que o filtro downstream seja um analisador, como o [divisor de fluxo MPEG-1](mpeg-1-stream-splitter-filter.md), o [divisor AVI](avi-splitter-filter.md)ou o [analisador de filmes do QuickTime](quicktime-movie-parser-filter.md).



| Rótulo | Valor |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| Filtrar interfaces                        | [**IAMOpenProgress**](/windows/desktop/api/Strmif/nn-strmif-iamopenprogress), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter)       |
| Tipos de mídia de pino de entrada                    | Não se aplica                                                                                                                       |
| Interfaces de pino de entrada                     | Não se aplica                                                                                                                       |
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

[DirectShow Filter](directshow-filters.md)
</dt> </dl>

 

 



