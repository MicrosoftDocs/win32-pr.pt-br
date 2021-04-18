---
description: Transportes
ms.assetid: 63c5ff5b-293d-4a80-92e8-3ece41321095
title: Transportes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c3d87ffacc871fc45ef1e8e645849afc956fb1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105810379"
---
# <a name="transports"></a>Transportes

Para mover os dados de mídia por meio do grafo de filtro, um filtro do DirectShow deve dar suporte a um dos vários protocolos possíveis. Esses protocolos são chamados de transportes. Quando dois filtros se conectam, eles devem dar suporte ao mesmo transporte; caso contrário, eles não poderão trocar dados de mídia. Normalmente, um transporte requer que um dos Pins dê suporte a uma interface específica. Quando os filtros se conectam, um PIN consulta o outro para a interface.

A maioria dos filtros do DirectShow mantém os dados de mídia na memória principal e os entrega para outros filtros em conexões de PIN. Esse tipo de transporte é chamado de transporte de memória local. Embora o transporte de memória local seja o transporte mais comum no DirectShow, nem todos os filtros o utilizam. Por exemplo, alguns filtros enviam dados de mídia ao longo de um caminho de hardware e usam Pins apenas para fornecer informações de controle. Por exemplo, consulte a interface [**IOverlay**](/windows/desktop/api/Strmif/nn-strmif-ioverlay) .

O DirectShow define dois mecanismos para o transporte de memória local, o modelo de push e o modelo de pull. No modelo de push, um filtro de origem gera dados e os entrega para o próximo filtro downstream. Esse filtro recebe passivamente os dados, processa-os e envia-os ainda mais downstream. No modelo de pull, o filtro de origem é conectado a um filtro do analisador. O filtro do analisador solicita dados do filtro de origem. O filtro de origem responde às solicitações fornecendo dados. O modelo de push usa a interface [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) e o modelo de pull usa a interface [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) .

O modelo de Push é mais comum do que o modelo de pull. Portanto, os artigos a seguir pressupõem um modelo de push. O último artigo nesta seção, [pull Model](pull-model.md), descreve como a interface **IAsyncReader** difere de **IMemInputPin**.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Fluxo de dados no grafo de filtro](data-flow-in-the-filter-graph.md)
</dt> </dl>

 

 



