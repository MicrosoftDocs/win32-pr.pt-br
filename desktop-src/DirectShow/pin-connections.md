---
description: Fixar conexões
ms.assetid: 1406ade4-77d8-49a7-8f36-cc49ff007a26
title: Fixar conexões
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cfcd407e785e15f4243f3113a63569f8b4b84de517cdde0f63a88eaef79f85c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119432286"
---
# <a name="pin-connections"></a>Fixar conexões

Os filtros se conectam em seus pinos, por meio da interface [**IPin.**](/windows/desktop/api/Strmif/nn-strmif-ipin) Os pinos de saída se conectam aos pinos de entrada. Cada conexão de pino tem um tipo de mídia, descrito pela estrutura [**AM \_ MEDIA \_ TYPE.**](/windows/win32/api/strmif/ns-strmif-am_media_type)

Um aplicativo conecta filtros chamando métodos no Gerenciador Graph Filtro, nunca chamando métodos nos filtros ou nos próprios pinos. O aplicativo pode especificar diretamente quais filtros se conectar chamando o método [**IFilterGraph::ConnectDirect**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-connectdirect) ou [**IGraphBuilder::Conexão;**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) ou pode conectar filtros indiretamente, usando um método de criação de grafo, como [**IGraphBuilder::RenderFile.**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile)

Para que a conexão seja bem-sucedida, ambos os filtros devem estar no grafo de filtro. O aplicativo pode adicionar um filtro ao grafo chamando o [**método IFilterGraph::AddFilter.**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) O Gerenciador Graph Filtro também pode adicionar filtros ao grafo. Quando um filtro é adicionado, o Gerenciador Graph Filtro chama o método [**IBaseFilter::JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) do filtro para notificar o filtro.

O contorno geral do processo de conexão é o seguinte:

1.  O Gerenciador Graph Filtro chama [**IPin::Conexão**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) no pino de saída, passando um ponteiro para o pino de entrada.
2.  Se o pino de saída aceitar a conexão, ele [**chamará IPin::ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) no pino de entrada.
3.  Se o pino de entrada também aceitar a conexão, a tentativa de conexão terá êxito e os pinos serão conectados.

Alguns pinos podem ser desconectados e reconectados enquanto o filtro está ativo. Esse tipo de reconexão é chamado *de* reconexão dinâmica. Para obter mais informações, consulte [Dynamic Graph Building](dynamic-graph-building.md). No entanto, a maioria dos filtros não é suportada pela reconexão dinâmica.

Os filtros geralmente são conectados em ordem downstream— em outras palavras, os pinos de entrada do filtro são conectados antes de seus pinos de saída. Um filtro sempre deve dar suporte a essa ordem de conexão. Alguns filtros também suportam conexões na ordem oposta – pinos de saída primeiro, seguidos por pinos de entrada. Por exemplo, pode ser possível conectar o pino de saída de um filtro MUX ao filtro de file-writer antes de conectar os pinos de entrada do filtro MUX.

Quando o método **Conexão** ou **ReceiveConnection** de um pin é chamado, o pin deve verificar se ele pode dar suporte à conexão. Os detalhes dependem do filtro específico. As tarefas mais comuns incluem o seguinte:

-   Verifique se o tipo de mídia é aceitável
-   Negociar um alocador
-   Consulte o outro pino para as interfaces necessárias.

 

 



