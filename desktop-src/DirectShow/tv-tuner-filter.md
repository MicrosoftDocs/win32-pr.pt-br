---
description: Filtro de sintonizador de TV
ms.assetid: a8e101dc-78ab-495f-9086-7b1d1e87c357
title: Filtro de sintonizador de TV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81dd03b965275f5e9b9405b027c8e66a7fb0f157
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297360"
---
# <a name="tv-tuner-filter"></a>Filtro de sintonizador de TV

O filtro de sintonizador de TV seleciona uma difusão analógica ou canal de cabo a ser exibido. O fluxo de saída único é um caminho de hardware para o vídeo de banda básica analógica. Essa saída deve se conectar ao filtro Crossbar de vídeo analógico. Os Pins de entrada incluem uma entrada para o cabo e uma entrada de antena.



|                                          |                                                                                                                                                                                   |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Filtrar interfaces                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IAMTVTuner**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner), **ISpecifyPropertyPages**, **IPersistPropertyBag**, **IKsObject**, [**IKsPropertySet**](ikspropertyset.md) |
| Tipos de mídia de pino de entrada                    | Não aplicável.                                                                                                                                                                   |
| Interfaces de pino de entrada                     | Não aplicável.                                                                                                                                                                   |
| Tipos de mídia do pino de saída                   | Vídeo: MEDIATYPE \_ AnalogVideo, \_ subtipo de KSDATAFORMAT \_ nenhum áudio: MediaType \_ AnalogAudio, MEDIASUBTYPE \_ nulo                                                                      |
| Interfaces de pino de saída                    | [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)                                                                                                                                                              |
| CLSID do filtro                             | \_TVTUNERFILTER CLSID                                                                                                                                                              |
| CLSID de página de propriedades                      | \_TVTUNERFILTERPROPERTYPAGE CLSID                                                                                                                                                  |
| Executável                               | KSTVTune.ax                                                                                                                                                                       |
| [Núcleo](merit.md)                       | MÉRITO \_ \_ não \_ use                                                                                                                                                               |
| [Categoria do filtro](filter-categories.md) | \_KSCATEGORY \_ TVTUNER                                                                                                                                                           |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Filtros do DirectShow](directshow-filters.md)
</dt> </dl>

 

 



