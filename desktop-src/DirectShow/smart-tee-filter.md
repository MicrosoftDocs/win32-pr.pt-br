---
description: Filtro de "t" inteligente
ms.assetid: 25bfbd62-b6be-4d1f-aa4c-77798bbb9fc9
title: Filtro de "t" inteligente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c52077066f69e50fbb5218012a402a8d556c15c1
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909294"
---
# <a name="smart-tee-filter"></a>Filtro de "t" inteligente

O filtro de monitoração inteligente é usado em gráficos de captura de vídeo para dividir o fluxo de vídeo em um fluxo de visualização e em um fluxo de captura. Isso é feito sem qualquer cópia de dados adicional. Os Pins de saída dão suporte a qualquer tipo de mídia com suporte na conexão de downstream.

O filtro de monitoração inteligente é útil quando um filtro de captura de vídeo não fornece Pins separados para captura e visualização. O filtro de desempenho inteligente só fornecerá dados de visualização se isso não prejudicar o desempenho da captura. Ele também remove os carimbos de data/hora do fluxo de visualização. O construtor de grafo de captura insere automaticamente o filtro de "t inteligente" quando necessário. Para obter mais informações, consulte [combinando captura de vídeo e visualização](combining-video-capture-and-preview.md).

A ilustração a seguir mostra um grafo de captura típico que usa o filtro de "t" inteligente.

![usando o filtro de "t inteligente"](images/smarttee.png)



| Label | Valor |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Filtrar interfaces                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                             |
| Tipos de mídia de pino de entrada                    | \_Vídeo de MediaType, MEDIASUBTYPE \_ nulo                                                                           |
| Interfaces de pino de entrada                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)         |
| Tipos de mídia do pino de saída                   | \_Vídeo de MediaType, MEDIASUBTYPE \_ nulo                                                                           |
| Interfaces de pino de saída                    | [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| CLSID do filtro                             | \_SMARTTEE CLSID                                                                                                |
| CLSID de página de propriedades                      | Nenhuma página de propriedades.                                                                                              |
| Executável                               | qcap.dll                                                                                                       |
| [Núcleo](merit.md)                       | MÉRITO \_ \_ não \_ use                                                                                            |
| [Categoria do filtro](filter-categories.md) | \_LEGACYAMFILTERCATEGORY CLSID                                                                                  |



 

## <a name="remarks"></a>Comentários

O pino de captura é o pino de saída 0 e o pino de visualização é o pino de saída 1.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Filtros do DirectShow](directshow-filters.md)
</dt> </dl>

 

 



