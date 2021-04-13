---
description: Visão geral do fluxo de dados no DirectShow
ms.assetid: a1b30592-5106-44f5-8ee0-577573670167
title: Visão geral do fluxo de dados no DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b5a34444991d6cba62026935f5ec2d7aa4eba77
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456759"
---
# <a name="overview-of-data-flow-in-directshow"></a>Visão geral do fluxo de dados no DirectShow

Esta seção fornece uma ampla visão geral de como funciona o fluxo de dados no DirectShow. Os detalhes podem ser encontrados em outras seções da documentação.

Os dados são mantidos em buffers, que são simplesmente matrizes de bytes. Cada buffer é encapsulado por um objeto COM chamado de *exemplo de mídia*, que implementa a interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) . Os exemplos são criados por outro tipo de objeto, chamado de alocador, que implementa a interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) . Um alocador é atribuído a cada conexão de PIN, embora duas ou mais conexões de PIN possam compartilhar o mesmo alocador. A imagem a seguir ilustra esse processo.

![buffers, amostras e alocadores](images/dataflow.png)

Cada alocador cria um pool de amostras de mídia e aloca os buffers para cada amostra. Sempre que um filtro precisa preencher um buffer com dados, ele solicita um exemplo do alocador chamando [**IMemAllocator:: GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer). Se o alocador tiver exemplos que não estão atualmente em uso por outro filtro, o método **GetBuffer** retornará imediatamente com um ponteiro para o exemplo. Se todas as amostras do alocador estiverem em uso, o método será bloqueado até que um exemplo se torne disponível. Quando o método retorna um exemplo, o filtro coloca os dados no buffer, define os sinalizadores apropriados no exemplo (normalmente incluindo um carimbo de data/hora) e entrega o exemplo downstream.

Quando um filtro de renderizador recebe um exemplo, ele verifica o carimbo de data/hora e se mantém na amostra até que o relógio de referência do grafo de filtro indique que os dados devem ser renderizados. Depois que o filtro renderiza os dados, ele libera o exemplo. O exemplo não volta para o pool de exemplos do alocador até que a contagem de referência da amostra seja zero, o que significa que cada filtro liberou o exemplo. A imagem a seguir ilustra esse processo.

![decodificador aguardando um exemplo de mídia livre](images/dataflow2.png)

O filtro upstream pode ser executado antes do renderizador, ou seja, ele pode preencher buffers mais rápido do que o renderizador consumi-los. Mesmo assim, os exemplos não são renderizados antecipadamente, porque o renderizador mantém cada um até seu tempo de apresentação. Além disso, o filtro upstream não substituirá os buffers acidentalmente, porque **getsample** retorna apenas exemplos que não estão em uso de outra forma. O valor pelo qual o filtro upstream pode ser executado à frente é determinado pelo número de amostras no pool do alocador.

O diagrama anterior mostra apenas um alocador, mas normalmente há vários alocadores por fluxo. Assim, quando o renderizador libera um exemplo, ele pode ter um efeito em cascata. O diagrama a seguir mostra uma situação em que um decodificador mantém um quadro de vídeo compactado enquanto aguarda o processador liberar um exemplo. Um filtro do analisador também está aguardando que o decodificador Libere um exemplo.

![dois filtros aguardando exemplos](images/dataflow3.png)

Quando o renderizador libera seu exemplo, a chamada pendente do decodificador para **GetBuffer** retorna. O decodificador pode, então, decodificar o quadro de vídeo compactado e liberar o exemplo que estava segurando, desbloqueando, assim, a chamada **GetBuffer** pendente do analisador.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Fluxo de dados no grafo de filtro](data-flow-in-the-filter-graph.md)
</dt> </dl>

 

 



