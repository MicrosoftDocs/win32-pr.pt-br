---
description: Filtro de t de PIN infinito
ms.assetid: 5f3e06ec-adee-4bc7-8ea8-cce3030d3baa
title: Filtro de t de PIN infinito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90e9a80baf047cdd5559fadaa0f13ea1352d4ed0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370260"
---
# <a name="infinite-pin-tee-filter"></a>Filtro de t de PIN infinito

Esse filtro fornece amostras entregues ao seu pino de entrada para um número variável de Pins de saída. Quando uma instância do filtro é criada, ela tem um pino de saída. Cada vez que um pino de saída é conectado, o filtro cria outro pino de saída. Todos os Pins de saída compartilham o mesmo tipo de mídia que o pino de entrada.

Uma versão desse filtro também é fornecida como um exemplo de SDK. Consulte [exemplo de filtro InfTee](inftee-filter-sample.md).



|                                          |                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Filtrar interfaces                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                 |
| Tipos de mídia de pino de entrada                    | Qualquer tipo de mídia                                                                                                                                     |
| Interfaces de pino de entrada                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                             |
| Tipos de mídia do pino de saída                   | Qualquer tipo de mídia. O tipo de saída sempre corresponde ao tipo de entrada, para todos os Pins de saída                                                                 |
| Interfaces de pino de saída                    | [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| CLSID do filtro                             | \_INFTEE CLSID                                                                                                                                      |
| CLSID de página de propriedades                      | Nenhuma página de propriedades                                                                                                                                   |
| Executável                               | qcap.dll                                                                                                                                           |
| [Núcleo](merit.md)                       | MÉRITO \_ \_ não \_ use                                                                                                                                |
| [Categoria do filtro](filter-categories.md) | \_LEGACYAMFILTERCATEGORY CLSID                                                                                                                      |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Filtros do DirectShow](directshow-filters.md)
</dt> </dl>

 

 



