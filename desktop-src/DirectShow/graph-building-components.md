---
description: Componentes do Graph-Building
ms.assetid: d803c56c-6fb1-4937-92e7-9ed2db2afc46
title: Componentes do Graph-Building
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea3ba346356109d8080d887a510cfcb85b6a6c80
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104088800"
---
# <a name="graph-building-components"></a>Componentes do Graph-Building

O DirectShow fornece vários componentes que podem ser usados para criar gráficos de filtro. Entre elas estão as seguintes:

-   [Gerenciador do grafo de filtro](filter-graph-manager.md). Esse objeto controla o grafo de filtro. Ele dá suporte às interfaces [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder), [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol)e [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) , entre outras. Todos os aplicativos do DirectShow usam esse objeto em algum momento, embora, em alguns casos, outro objeto crie o Gerenciador de gráfico de filtro para o aplicativo.
-   [Capture o construtor de gráficos](capture-graph-builder.md). Esse objeto fornece métodos adicionais para criar gráficos de filtro. Ele foi projetado originalmente para a criação de gráficos que executam captura de vídeo (portanto, o nome), mas é útil para muitos outros tipos de grafo de filtro personalizado. Ele dá suporte à interface [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) .
-   [Mapeador de filtro](filter-mapper.md) e [enumerador de dispositivo do sistema](system-device-enumerator.md). Esses objetos localizam filtros que são registrados no sistema do usuário ou que representam dispositivos de hardware.
-   [Construtor de gráficos de DVD](dvd-graph-builder.md). Esse objeto cria gráficos de filtro para reprodução e navegação em DVD. Ele dá suporte à interface [**IDvdGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-idvdgraphbuilder) .

### <a name="intelligent-connect"></a>Conexão inteligente

O termo "conexão inteligente" abrange um conjunto de algoritmos que o Gerenciador do grafo de filtro usa para criar todo ou parte de um grafo de filtro. Sempre que o Gerenciador de grafo de filtro exigir filtros adicionais para concluir o grafo, ele faz aproximadamente o seguinte:

1.  Se houver um filtro atualmente no grafo, com pelo menos um pino de entrada não conectado, o Gerenciador do grafo de filtro tentará usar esse filtro.
2.  Caso contrário, o Gerenciador de gráfico de filtro procurará no registro os filtros que podem aceitar o tipo de mídia correto para a conexão. Cada filtro tem um valor de registro chamado "mérito", que indica aproximadamente a probabilidade de o filtro ser útil na conclusão do grafo. O Gerenciador de gráfico de filtro tenta filtros em ordem de valor de mérito. Para cada tipo de fluxo (como áudio, vídeo ou MIDI), o renderizador padrão tem um grande mérito. Os decodificadores também têm um grande mérito. Filtros de finalidade especial têm poucos méritos.

Se o Gerenciador do grafo de filtro ficar preso, ele fará o failback e tentará uma combinação diferente de filtros. Você pode encontrar os detalhes exatos no tópico [Intelligent Connect](intelligent-connect.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando o grafo de filtro](building-the-filter-graph.md)
</dt> </dl>

 

 



