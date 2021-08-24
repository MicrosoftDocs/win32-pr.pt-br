---
description: Filtro de origem do arquivo (Async)
ms.assetid: 0cf6e7ab-b1fe-42f9-b682-c5484ef48c71
title: Filtro de origem do arquivo (Async)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9261cc65774fc6116a902a02ef193a205ca83ce4232a30534e7b38c040c01971
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118000737"
---
# <a name="file-source-async-filter"></a>Filtro de origem do arquivo (Async)

O filtro de origem de arquivo assíncrono é aberto e lê os arquivos locais de vários formatos de dados diferentes e passa os dados para um filtro de analisador.

Para baixar arquivos de mídia da Web por meio de HTTP, use o filtro de [origem do arquivo (URL)](file-source--url--filter.md) . Para ler arquivos ASF, use o filtro de [leitor ASF do WM](wm-asf-reader-filter.md) .



| Rótulo | Valor |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| Filtrar interfaces                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [ **IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter)                                                   |
| Tipos de mídia de pino de entrada                    | Não se aplica                                                                                                                       |
| Interfaces de pino de entrada                     | Não se aplica                                                                                                                       |
| Tipos de mídia do pino de saída                   | **MediaType \_ Fluxo**. O subtipo depende do formato de mídia. (**MEDIASUBTYPE \_ NULL** se o filtro não reconhecer o formato.) |
| Interfaces de pino de saída                    | [**IAMAsyncReaderTimestampScaling**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling), [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) |
| CLSID do filtro                             | **\_ASYNCREADER CLSID**                                                                                                               |
| CLSID de página de propriedades                      | Nenhuma página de propriedades                                                                                                                     |
| Executável                               | quartz.dll                                                                                                                           |
| [Núcleo](merit.md)                       | **MÉRITO \_ improvável**                                                                                                                  |
| [Categoria do filtro](filter-categories.md) | **\_LEGACYAMFILTERCATEGORY CLSID**                                                                                                    |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DirectShow Filter](directshow-filters.md)
</dt> </dl>

 

 



