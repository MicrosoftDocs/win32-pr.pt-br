---
description: Reconectando Pins
ms.assetid: 34b3e4de-e4eb-48c5-aaef-fc99b63e8691
title: Reconectando Pins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9fc71b4d5a62ee066edaa5f97b4cc3332b2231d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500367"
---
# <a name="reconnecting-pins"></a>Reconectando Pins

Durante uma conexão de PIN, um filtro pode desconectar e reconectar um de seus outros Pins, da seguinte maneira:

1.  O filtro chama [**IPin:: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) no PIN do outro filtro e especifica o novo tipo de mídia.
2.  Se **QueryAccept** retornar S \_ OK, o filtro chamará [**IFilterGraph2:: ReconnectEx**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-reconnectex) para reconectar os Pins.

Veja a seguir alguns exemplos de quando um filtro pode precisar reconectar Pins:

-   **Filtros de t.** Um *filtro de t* divide um fluxo de entrada em várias saídas sem alterar os dados no fluxo. Um filtro de "t" pode aceitar um intervalo de tipos de mídia, mas os tipos devem corresponder em todas as conexões de PIN. Portanto, quando o PIN de entrada se conecta, o filtro pode precisar renegociar todas as conexões existentes nos Pins de saída e vice-versa. Para obter um exemplo, consulte o [exemplo de filtro InfTee](inftee-filter-sample.md).
-   **Filtros de trans-in-Place.** Um filtro de *Trans-in-Place* modifica os dados de entrada no buffer original em vez de copiar os dados para um buffer de saída separado. Um filtro de trans-in-Place deve usar o mesmo alocador para as conexões upstream e downstream. O primeiro PIN a ser conectado (entrada ou saída) negocia um alocador da maneira usual. No entanto, quando o outro PIN se conecta, o primeiro alocador pode não ser aceitável. Nesse caso, o segundo PIN escolhe um alocador diferente e o primeiro PIN se reconecta usando o novo alocador. Para obter um exemplo de implementação, consulte a classe [**CTransInPlaceFilter**](ctransinplacefilter.md) .

No método **ReconnectEx** , o Gerenciador de gráfico de filtro desconecta-se de forma assíncrona e reconecta os Pins. O filtro não deve tentar a reconexão, a menos que **QueryAccept** retorne S \_ OK. Caso contrário, o PIN será deixado desconectado, causando erros de grafo. Além disso, o filtro deve solicitar a reconexão de dentro do método [**IPin:: Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) , no mesmo thread. Se o método **Connect** retornar em um thread, enquanto outro thread fizer a solicitação de reconexão, o Gerenciador do grafo de filtro poderá executar o grafo antes que ele faça a reconexão, causando erros de grafo.

 

 



