---
description: Cadeias de filtro
ms.assetid: c17b3b58-65ab-4e83-91f2-54a995f22ddf
title: Cadeias de filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4650c49dd796ff3aa7ddecbd21076a4e217def9bfb6504149fdb740c2810b48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119685468"
---
# <a name="filter-chains"></a>Cadeias de filtro

Uma *cadeia de filtros* é uma sequência de filtros que atende às seguintes condições:

-   Cada filtro na cadeia tem no máximo um pino de entrada conectado e um pino de saída conectado.
-   É possível percorrer todos os filtros na cadeia sem passar filtros fora da cadeia.

Por exemplo, no diagrama a seguir, os filtros A-B, C-D e F-G-H são cadeias de filtro. Cada sub-cadeia em F-G–H (F-G e G-H) também é uma cadeia de filtros. Uma cadeia de filtros pode consistir em um único filtro, portanto, os filtros A, B, C, D, F, G e H também são cadeias de filtro distintas. O filtro E tem duas conexões de entrada, portanto, qualquer sequência de filtros que inclua o filtro E não é uma cadeia de filtros.

![cadeia de filtros (exemplo 1)](images/filter-chain1.png)

A [**interface IFilterChain**](/windows/desktop/api/Strmif/nn-strmif-ifilterchain) fornece os seguintes métodos para controlar cadeias de filtro:



| Rótulo | Valor |
|---------------------------------------------------------------|---------------------------------|
| [**IFilterChain::StartChain**](/windows/desktop/api/Strmif/nf-strmif-ifilterchain-startchain)   | Inicia uma cadeia.                 |
| [**IFilterChain::StopChain**](/windows/desktop/api/Strmif/nf-strmif-ifilterchain-stopchain)     | Interrompe uma cadeia.                  |
| [**IFilterChain::P auseChain**](/windows/desktop/api/Strmif/nf-strmif-ifilterchain-pausechain)   | Pausa uma cadeia.                 |
| [**IFilterChain::RemoveChain**](/windows/desktop/api/Strmif/nf-strmif-ifilterchain-removechain) | Remove uma cadeia do grafo. |



 

Não há nenhum método específico para adicionar uma cadeia. Para adicionar uma cadeia, insira os novos filtros usando o [**método IFilterGraph::AddFilter.**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) Em seguida, conecte os filtros chamando [**IGraphBuilder::Conexão**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect), [**IGraphBuilder::Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render)ou métodos semelhantes.

Quando o grafo está em execução, uma cadeia de filtros pode alternar entre a execução e a parada. Quando o grafo é pausado, ele pode alternar entre pausado e parado. Essas são as únicas transições de estado possíveis com cadeias de filtro.

## <a name="filter-chain-guidelines"></a>Diretrizes de cadeia de filtros

Quando você usa **métodos IFilterChain,** é importante garantir que os filtros no grafo possam dar suporte a operações de encadeamento de filtro. Caso contrário, você poderá causar deadlocks ou erros de grafo. Os filtros conectados à cadeia devem funcionar corretamente após a cadeia mudar de estado.

A melhor maneira de usar **IFilterChain** é com um conjunto de filtros que você projetou especificamente para encadeamento. Use as diretrizes a seguir para garantir que seus filtros sejam seguros para operações de cadeia de filtros. Esses pontos se referem ao diagrama a seguir.

![cadeia de filtros (exemplo 2)](images/filter-chain2.png)

-   Antes que o estado da cadeia de filtros mude, todas as chamadas de processamento de dados no limite da cadeia de filtros devem ser concluídas. Essa regra se aplica aos métodos [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive), [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment)e [**IPin::EndOfStream.**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) Os filtros na cadeia devem retornar de chamadas para esses métodos feitas por filtros fora da cadeia; e filtros fora da cadeia devem retornar de chamadas feitas por filtros dentro da cadeia.

Por exemplo, no diagrama anterior, o filtro B deve concluir todas as chamadas de processamento de dados do filtro A e o filtro E deve concluir todas as chamadas do filtro D. Se os pinos expõem as interfaces [**IPinFlowControl**](/windows/desktop/api/Strmif/nn-strmif-ipinflowcontrol) e [**IPinConnection,**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection) você pode efetuar push dos dados por meio do grafo chamando os métodos [**IPinFlowControl::Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) e [**IGraphConfig::P throughThroughData,**](/windows/desktop/api/Strmif/nf-strmif-igraphconfig-pushthroughdata) conforme descrito em [Reconexão dinâmica](dynamic-reconnection.md). Os filtros também podem dar suporte a métodos privados para esvasá-los.

-   Os filtros upstream devem esperar que o estado da cadeia mude. Por exemplo, no diagrama anterior, suponha que a cadeia seja interrompida, mas filtre A chama **IMemInputPin::Receive**. A chamada falha e a resposta do filtro A é parar o streaming. Quando o aplicativo reinicia a cadeia, ele não tem efeito porque o filtro A não está mais transmitindo dados.
-   Os filtros downstream também devem esperar que o estado da cadeia mude. Caso não, o filtro downstream poderá ser bloqueado enquanto aguarda amostras que nunca chegam. Por exemplo, filtros MUX (multiplexador) geralmente exigem dados de todos os seus pinos de entrada. Interromper o fluxo de dados de um pino de entrada pode impedir o processamento dos outros fluxos. Isso pode fazer com que o grafo seja deadlock.
-   Cada conexão de pino de um filtro fora da cadeia para um filtro dentro da cadeia deve ter seu próprio alocador, que não é compartilhado por outras conexões. Quando a cadeia altera o estado ou é removida do grafo, o alocador pode ser descommitido. Se outras conexões estavam usando o mesmo alocador, elas não podem mais processar exemplos.
-   Não remova uma cadeia, a menos que os filtros conectados à cadeia deem suporte à desconexão dinâmica. Normalmente, os filtros conectados darão suporte à interface **IPinConnection** ou **IPinFlowControl,** mas podem dar suporte a interfaces privadas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criação Graph dinâmica](dynamic-graph-building.md)
</dt> </dl>

 

 



