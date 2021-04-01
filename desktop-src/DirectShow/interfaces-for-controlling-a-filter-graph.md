---
description: Interfaces para controlar um grafo de filtro
ms.assetid: f7de0165-e356-45d5-baed-d127caeebaf6
title: Interfaces para controlar um grafo de filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61e88dc4ba2143bbbf33a58763a5ff9005254236
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103646051"
---
# <a name="interfaces-for-controlling-a-filter-graph"></a>Interfaces para controlar um grafo de filtro

Essas interfaces fornecem métodos para controlar um grafo de filtro.



| Interface                                  | Descrição                                                                                               |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [**IAMClockAdjust**](/windows/desktop/api/Strmif/nn-strmif-iamclockadjust)   | Ajuste o relógio do grafo.                                                                                   |
| [**IAMGraphStreams**](/windows/desktop/api/Strmif/nn-strmif-iamgraphstreams) | Sincronizar fluxos ao vivo em um grafo de filtro.                                                               |
| [**IFilterChain**](/windows/desktop/api/Strmif/nn-strmif-ifilterchain)       | Cadeias de controle de filtros.                                                                                |
| [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol)     | Execute, pause e interrompa o gráfico de filtro. (Também fornece métodos compatíveis com a automação para a criação de grafos.) |
| [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex)     | Responder a eventos no grafo.                                                                           |
| [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)     | Busque dentro de um arquivo.                                                                                       |
| [**IQueueCommand**](/windows/desktop/api/Control/nn-control-iqueuecommand)     | Comandos de fila para serem executados mais tarde.                                                                    |
| [**IVideoFrameStep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) | Quadro – percorrer um fluxo de vídeo.                                                                        |



 

 

 



