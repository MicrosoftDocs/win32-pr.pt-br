---
description: Fixar conexões
ms.assetid: 1406ade4-77d8-49a7-8f36-cc49ff007a26
title: Fixar conexões
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b509abddf4a915b65dfd322f76b4afb132a7f835
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370144"
---
# <a name="pin-connections"></a>Fixar conexões

Os filtros se conectam a seus Pins, por meio da interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) . Os Pins de saída se conectam aos pins de entrada. Cada conexão de PIN tem um tipo de mídia, descrito pela estrutura do [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .

Um aplicativo conecta filtros chamando métodos no Gerenciador do grafo de filtro, nunca chamando métodos nos filtros ou Pins. O aplicativo pode especificar diretamente quais filtros se conectar, chamando o método [**IFilterGraph:: ConnectDirect**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-connectdirect) ou [**IGraphBuilder:: Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) ; ou pode conectar filtros indiretamente, usando um método de criação de grafo, como [**IGraphBuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile).

Para que a conexão seja realizada com sucesso, ambos os filtros devem estar no grafo de filtro. O aplicativo pode adicionar um filtro ao grafo chamando o método [**IFilterGraph:: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) . O Gerenciador de gráfico de filtro também pode adicionar filtros ao grafo. Quando um filtro é adicionado, o Gerenciador de gráfico de filtro chama o método [**IBaseFilter:: JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) do filtro para notificar o filtro.

O contorno geral do processo de conexão é o seguinte:

1.  O Gerenciador do grafo de filtro chama [**IPin:: Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) no pino de saída, passando um ponteiro para o pino de entrada.
2.  Se o pino de saída aceitar a conexão, ele chamará [**IPin:: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) no pino de entrada.
3.  Se o PIN de entrada também aceitar a conexão, a tentativa de conexão será realizada com sucesso e os Pins serão conectados.

Alguns Pins podem ser desconectados e reconectados enquanto o filtro está ativo. Esse tipo de reconexão é chamado de reconexão *dinâmica* . Para obter mais informações, consulte [criação de grafo dinâmico](dynamic-graph-building.md). No entanto, a maioria dos filtros não oferece suporte à reconexão dinâmica.

Os filtros geralmente são conectados em ordem downstream — em outras palavras, os Pins de entrada do filtro são conectados antes de seus PINs de saída. Um filtro sempre deve dar suporte a essa ordem de conexão. Alguns filtros também dão suporte a conexões na ordem oposta — Pins de saída primeiro, seguidos por Pins de entrada. Por exemplo, pode ser possível conectar o pino de saída de um filtro MUX ao filtro de gravador de arquivo, antes de conectar os Pins de entrada do filtro MUX.

Quando o método **Connect** ou **ReceiveConnection** de um PIN é chamado, o PIN deve verificar se ele pode dar suporte à conexão. Os detalhes dependem do filtro específico. As tarefas mais comuns incluem o seguinte:

-   Verifique se o tipo de mídia é aceitável
-   Negociar um alocador
-   Consulte o outro PIN para obter as interfaces necessárias.

 

 



