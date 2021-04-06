---
description: Filtro de separador de cores VGA 16
ms.assetid: 0a5f4e92-e703-4487-91b0-15265744004e
title: Filtro de separador de cores VGA 16
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85db9d8fad706c96f19bb5bea6b0476b0ddec735
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011315"
---
# <a name="vga-16-color-ditherer-filter"></a>Filtro de separador de cores VGA 16

O filtro de separador de cores VGA 16 converte de um tipo de cor RGB em uma exibição de cor de 4 bits para que os fluxos de vídeo AVI e MPEG possam ser exibidos em monitores mais antigos de 16 cores. Esse filtro é inserido no grafo entre um filtro de descompactador e um filtro de processador de vídeo.



|                                          |                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Filtrar interfaces                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                 |
| Tipos de mídia de pino de entrada                    | \_Vídeo de MediaType, MEDIASUBTYPE \_ RGB8                                                                                                               |
| Interfaces de pino de entrada                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                             |
| Tipos de mídia do pino de saída                   | \_Vídeo de MediaType, MEDIASUBTYPE \_ RGB4                                                                                                               |
| Interfaces de pino de saída                    | [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| CLSID do filtro                             | \_Pontilhamento de CLSID                                                                                                                                      |
| CLSID de página de propriedades                      | Nenhuma página de propriedades.                                                                                                                                  |
| Executável                               | quartz.dll                                                                                                                                         |
| [Núcleo](merit.md)                       | MÉRITO \_ improvável                                                                                                                                    |
| [Categoria do filtro](filter-categories.md) | \_LEGACYAMFILTERCATEGORY CLSID                                                                                                                      |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Filtros do DirectShow](directshow-filters.md)
</dt> </dl>

 

 



