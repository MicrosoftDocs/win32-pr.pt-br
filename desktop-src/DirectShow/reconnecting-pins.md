---
description: Reconectando pinos
ms.assetid: 34b3e4de-e4eb-48c5-aaef-fc99b63e8691
title: Reconectando pinos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d8bb214307a5c17639d98ae07284abddca4d5beb11b966150d8b7ec46013853
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072770"
---
# <a name="reconnecting-pins"></a>Reconectando pinos

Durante uma conexão de pino, um filtro pode desconectar e reconectar um de seus outros pinos, da seguinte forma:

1.  O filtro chama [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) no pino do outro filtro e especifica o novo tipo de mídia.
2.  Se **QueryAccept** retornar S OK, o filtro \_ [**chamará IFilterGraph2::ReconnectEx**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-reconnectex) para reconectar os pinos.

Veja a seguir alguns exemplos de quando um filtro pode precisar reconectar os pinos:

-   **Filtros de tee.** Um *filtro tee* divide um fluxo de entrada em várias saídas sem alterar os dados no fluxo. Um filtro tee pode aceitar uma variedade de tipos de mídia, mas os tipos devem corresponder a todas as conexões de pino. Portanto, quando o pino de entrada se conecta, o filtro pode precisar negociar quaisquer conexões existentes nos pinos de saída e vice-versa. Para ver um exemplo, consulte [o Exemplo de filtro InfTee](inftee-filter-sample.md).
-   **Filtros trans-in-place.** Um *filtro trans-in-locar* modifica os dados de entrada no buffer original em vez de copiar os dados para um buffer de saída separado. Um filtro trans-in-locar deve usar o mesmo alocador para as conexões upstream e downstream. O primeiro pino para se conectar (entrada ou saída) negocia um alocador da maneira normal. No entanto, quando o outro pino se conecta, o primeiro alocador pode não ser aceitável. Nesse caso, o segundo pin escolhe um alocador diferente e o primeiro pin se reconecta usando o novo alocador. Para ver um exemplo de implementação, consulte a [**classe CTransInPlaceFilter.**](ctransinplacefilter.md)

No método **ReconnectEx,** o Filter Graph Manager desconecta de forma assíncrona e reconecta os pinos. O filtro não deve tentar a reconexão, a menos **que QueryAccept** retorne S \_ OK. Caso contrário, o pino será deixado desconectado, causando erros de grafo. Além disso, o filtro deve solicitar a reconexão de dentro do [**método IPin::Conexão,**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) no mesmo thread. Se o **Conexão** retorna em um thread, enquanto outro thread faz a solicitação de reconexão, o Gerenciador de filtros Graph pode executar o grafo antes de fazer a reconexão, causando erros de grafo.

 

 



