---
description: Graph-Building componentes
ms.assetid: d803c56c-6fb1-4937-92e7-9ed2db2afc46
title: Graph-Building componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14aabcf31f55d0d42117e39cb22fa286b383641c94fe21f386345fd8db1cc890
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119564636"
---
# <a name="graph-building-components"></a>Graph-Building componentes

DirectShow fornece vários componentes que podem ser usados para criar grafos de filtro. Entre elas estão as seguintes:

-   [Filtrar Graph Manager](filter-graph-manager.md). Esse objeto controla o grafo de filtro. Ele dá suporte às interfaces [**IGraphBuilder,**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol)e [**IMediaEventEx,**](/windows/desktop/api/Control/nn-control-imediaeventex) entre outros. Todos DirectShow aplicativos usam esse objeto em algum momento, embora, em alguns casos, outro objeto crie o Gerenciador Graph Filtro para o aplicativo.
-   [Capture Graph Builder.](capture-graph-builder.md) Esse objeto fornece métodos adicionais para a criação de grafos de filtro. Ele foi originalmente projetado para criar grafos que executam a captura de vídeo (portanto, o nome), mas é útil para muitos outros tipos de grafo de filtro personalizado. Ele dá suporte à interface [**ICaptureGraphBuilder2.**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2)
-   [Filtrar Mapeador](filter-mapper.md) [e Enumerador de Dispositivo do Sistema](system-device-enumerator.md). Esses objetos localizam filtros registrados no sistema do usuário ou que representam dispositivos de hardware.
-   [DVD Graph Builder](dvd-graph-builder.md). Esse objeto cria grafos de filtro para reprodução e navegação de DVD. Ele dá suporte à interface [**IDvdGraphBuilder.**](/windows/desktop/api/Strmif/nn-strmif-idvdgraphbuilder)

### <a name="intelligent-connect"></a>Inteligência Conexão

O termo "Intelligent Conexão" abrange um conjunto de algoritmos que o Gerenciador de Graph Filtro usa para criar todo ou parte de um grafo de filtro. Sempre que o Gerenciador Graph filtros requer filtros adicionais para concluir o grafo, ele faz aproximadamente o seguinte:

1.  Se houver um filtro atualmente no grafo, com pelo menos um pino de entrada não conectado, o Gerenciador Graph Filtro tentará usar esse filtro.
2.  Caso contrário, o Gerenciador Graph Filtro procura no Registro filtros que podem aceitar o tipo de mídia correto para a conexão. Cada filtro tem um valor de Registro chamado "Bruto", que indica aproximadamente a probabilidade de o filtro ser útil na conclusão do grafo. O Gerenciador Graph filtros tenta filtros em ordem de valor de benefício. Para cada tipo de fluxo (como áudio, vídeo ou MIDI), o renderador padrão tem um alto tamanho. Os decodificadores também têm alto valor. Filtros de finalidade especial têm baixo custo.

Se o Gerenciador Graph filtro ficar preso, ele fará o back-out e tentará uma combinação diferente de filtros. Você pode encontrar os detalhes exatos no tópico [Inteligência Conexão](intelligent-connect.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando o filtro Graph](building-the-filter-graph.md)
</dt> </dl>

 

 



