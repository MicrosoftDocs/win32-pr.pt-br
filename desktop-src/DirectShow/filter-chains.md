---
description: Cadeias de filtro
ms.assetid: c17b3b58-65ab-4e83-91f2-54a995f22ddf
title: Cadeias de filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d46e374aca71b024773e4177d09e67c7ee6034ac
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825921"
---
# <a name="filter-chains"></a>Cadeias de filtro

Uma *cadeia de filtro* é uma sequência de filtros que atende às seguintes condições:

-   Cada filtro na cadeia tem, no máximo, um PIN de entrada conectado e um PIN de saída conectado.
-   É possível percorrer cada filtro na cadeia sem atravessar filtros fora da cadeia.

Por exemplo, no diagrama a seguir, os filtros A – B, C – D e F – G – H são cadeias de filtro. Cada Subcadeia em F – G – H (F – G e G – H) também é uma cadeia de filtro. Uma cadeia de filtros pode consistir em um único filtro, de modo que os filtros A, B, C, D, F, G e H também são cadeias de filtro distintas. O filtro E tem duas conexões de entrada, portanto, qualquer sequência de filtros que inclua filtro E não é uma cadeia de filtro.

![Cadeia de filtro (exemplo 1)](images/filter-chain1.png)

A interface [**IFilterChain**](/windows/desktop/api/Strmif/nn-strmif-ifilterchain) fornece os seguintes métodos para controlar cadeias de filtro:



|                                                               |                                 |
|---------------------------------------------------------------|---------------------------------|
| [**IFilterChain:: StartChain**](/windows/desktop/api/Strmif/nf-strmif-ifilterchain-startchain)   | Inicia uma cadeia.                 |
| [**IFilterChain::StopChain**](/windows/desktop/api/Strmif/nf-strmif-ifilterchain-stopchain)     | Para uma cadeia.                  |
| [**IFilterChain::P auseChain**](/windows/desktop/api/Strmif/nf-strmif-ifilterchain-pausechain)   | Pausa uma cadeia.                 |
| [**IFilterChain::RemoveChain**](/windows/desktop/api/Strmif/nf-strmif-ifilterchain-removechain) | Remove uma cadeia do grafo. |



 

Não há um método específico para adicionar uma cadeia. Para adicionar uma cadeia, insira os novos filtros usando o método [**IFilterGraph:: addfiltro**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) . Em seguida, conecte os filtros chamando [**IGraphBuilder:: Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect), [**IGraphBuilder:: render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render)ou métodos semelhantes.

Quando o grafo estiver em execução, uma cadeia de filtro poderá alternar entre running e Stopped. Quando o grafo é pausado, ele pode alternar entre pausado e parado. Essas são as únicas transições de estado possíveis com cadeias de filtro.

## <a name="filter-chain-guidelines"></a>Diretrizes de cadeia de filtro

Quando você usa métodos **IFilterChain** , é importante certificar-se de que os filtros no grafo possam dar suporte a operações de encadeamento de filtro. Caso contrário, você pode causar deadlocks ou erros de grafo. Os filtros conectados à cadeia devem funcionar corretamente após o estado de alteração da cadeia.

A melhor maneira de usar o **IFilterChain** é com um conjunto de filtros que você criou especificamente para encadeamento. Use as diretrizes a seguir para garantir que seus filtros sejam seguros para operações de cadeia de filtro. Esses pontos se referem ao diagrama a seguir.

![Cadeia de filtro (exemplo 2)](images/filter-chain2.png)

-   Antes que o estado da cadeia de filtro seja alterado, todas as chamadas de processamento de dados no limite da cadeia de filtro devem ser concluídas. Essa regra se aplica aos métodos [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive), [**IPin:: NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment)e [**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream). Os filtros na cadeia devem retornar de chamadas para esses métodos feitos por filtros fora da cadeia; e os filtros fora da cadeia devem retornar de chamadas feitas por filtros dentro da cadeia.

Por exemplo, no diagrama anterior, o filtro B deve concluir todas as chamadas de processamento de dados do filtro A e o filtro E deve concluir todas as chamadas do filtro D. Se os Pins expõem as interfaces [**IPinFlowControl**](/windows/desktop/api/Strmif/nn-strmif-ipinflowcontrol) e [**IPinConnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection) , você pode enviar os dados por Push por meio do grafo chamando os métodos [**IPinFlowControl:: Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) e [**IGraphConfig::P Ushthroughdata**](/windows/desktop/api/Strmif/nf-strmif-igraphconfig-pushthroughdata) , conforme descrito em [reconexão dinâmica](dynamic-reconnection.md). Os filtros também podem oferecer suporte a métodos privados para enviar os dados por push.

-   Os filtros upstream devem esperar que o estado da cadeia seja alterado. Por exemplo, no diagrama anterior, suponha que a cadeia seja interrompida, mas filtre uma chamada **IMemInputPin:: Receive**. A chamada falha e a resposta do filtro A é parar o streaming. Quando o aplicativo reinicia a cadeia, ele não tem nenhum efeito porque o filtro A não está mais transmitindo dados.
-   Os filtros downstream também devem esperar que o estado da cadeia seja alterado. Caso contrário, o filtro downstream pode ser bloqueado enquanto aguarda amostras que nunca chegam. Por exemplo, os filtros multiplexadores (MUX) geralmente exigem dados de todos os seus PINs de entrada. A interrupção do fluxo de dados de um PIN de entrada pode impedir que os outros fluxos sejam processados. Isso pode fazer com que o grafo seja bloqueado.
-   Cada conexão de PIN de um filtro fora da cadeia para um filtro dentro da cadeia deve ter seu próprio alocador, que não é compartilhado por outras conexões. Quando a cadeia muda de estado ou é removida do grafo, o alocador pode ser decomprometido. Se outras conexões estiverem usando o mesmo alocador, elas não poderão mais processar amostras.
-   Não remova uma cadeia, a menos que os filtros conectados à cadeia tenham suporte para desconexão dinâmica. Em geral, os filtros conectados oferecerão suporte à interface **IPinConnection** ou **IPinFlowControl** , mas podem dar suporte a interfaces privadas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criação de grafo dinâmico](dynamic-graph-building.md)
</dt> </dl>

 

 



