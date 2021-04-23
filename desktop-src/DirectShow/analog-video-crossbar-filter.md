---
description: Filtro Crossbar de vídeo analógico
ms.assetid: 668f6a8b-a4ed-4e4a-956c-a87f165225fa
title: Filtro Crossbar de vídeo analógico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d17d8700131dbc658a5233d56f339c39eac7a3a0
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909594"
---
# <a name="analog-video-crossbar-filter"></a>Filtro Crossbar de vídeo analógico

O filtro Crossbar de vídeo analógico representa uma barra de vídeo em um dispositivo de captura de vídeo que dá suporte ao Windows Driver Model (WDM).

Esse filtro é um filtro de wrapper para Crossbars em dispositivos de streaming WDM. O nome amigável do filtro é obtido do dispositivo. Cada pino de saída representa um caminho de hardware para o vídeo de banda básica analógica. Um dos pinos de entrada vem de um sintonizador de TV (o [filtro de sintonizador de TV](tv-tuner-filter.md)). Outros Pins de entrada dão suporte a fluxos de áudio ou vídeo. O filtro dá suporte a quaisquer subtipos de mídia e formatos com suporte nas conexões downstream.

Você não pode criar esse filtro diretamente com CoCreateInstance. A interface [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) adiciona automaticamente esse filtro ao grafo, conforme necessário.

Para obter mais informações sobre filtros de wrapper e dispositivos de streaming WDM, consulte [como os dispositivos de hardware participam do grafo de filtro](how-hardware-devices-participate-in-the-filter-graph.md).



| Label | Valor |
|------------------------------------------|------------------------------------------------------------------------------------------------|
| Filtrar interfaces                        | [**IAMCrossbar**](/windows/desktop/api/Strmif/nn-strmif-iamcrossbar), ISpecifyPropertyPages, IPersistPropertyBag, IPersistStream |
| Tipos de mídia de pino de entrada                    | MEDIATYPE \_ AnalogAudio, MediaType \_ AnalogVideo                                                 |
| Interfaces de pino de entrada                     | [**IKsPropertySet**](ikspropertyset.md)                                                       |
| Tipos de mídia do pino de saída                   | MEDIATYPE \_ AnalogAudio, MediaType \_ AnalogVideo                                                 |
| Interfaces de pino de saída                    | [**IKsPropertySet**](ikspropertyset.md)                                                       |
| CLSID do filtro                             | Não aplicável                                                                                 |
| CLSID de página de propriedades                      | \_CROSSBARFILTERPROPERTYPAGE CLSID                                                              |
| Executável                               | ksxbar.ax                                                                                      |
| [Núcleo](merit.md)                       | Dependente de driver.                                                                              |
| [Categoria do filtro](filter-categories.md) | \_KSCATEGORY \_ CROSSBAR                                                                       |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Filtros do DirectShow](directshow-filters.md)
</dt> <dt>

[Trabalhando com Crossbars](working-with-crossbars.md)
</dt> </dl>

 

 



