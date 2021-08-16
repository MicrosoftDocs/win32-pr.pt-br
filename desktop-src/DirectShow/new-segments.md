---
description: Novos segmentos
ms.assetid: 6c470b38-481f-4e52-93b8-eb6b343dcefc
title: Novos segmentos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28701a29a3b4edd61e9eb408aeab744297eac56408c49dc77dd4328a5afd24b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119790926"
---
# <a name="new-segments"></a>Novos segmentos

Um *segmento* é um grupo de exemplos de mídia que compartilham uma hora de início comum, hora de parada e taxa de reprodução. O [**método IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) sinaliza o início de um novo segmento. Ele fornece uma maneira para um filtro de origem informar filtros downstream de que as informações de tempo e taxa foram alteradas. Por exemplo, se o filtro de origem buscar um novo ponto no fluxo, ele **chamará NewSegment** com a nova hora de início.

Alguns filtros downstream usam as informações de segmento ao processar exemplos. Por exemplo, em um formato que usa compactação entre quadros, se o tempo de parada cair em um quadro delta, o filtro de origem poderá precisar enviar amostras adicionais após a hora de parada. Isso permite que o decodificador decodificar o quadro delta final. Para determinar o quadro final correto, o decodificador refere-se à hora de parada do segmento. Como outro exemplo, os renderadores de áudio usam a taxa de segmento junto com a taxa de amostragem de áudio para gerar a saída de áudio correta.

No modelo de push, o filtro de origem inicia a **chamada NewSegment.** No modelo de pull, isso é feito pelo filtro do analisador. Em ambos os casos, o filtro chama **NewSegment** no pino de entrada downstream, que propaga a chamada para o próximo filtro, até que a chamada atinja o renderdor. Os filtros devem **serializar chamadas NewSegment** com outras chamadas de streaming, como [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive).

O tempo de fluxo é redefinido como zero após cada novo segmento. Carimbos de data/hora em exemplos entregues após o segmento começar do zero.

 

 



