---
title: Gerenciando identificadores
description: O Gerenciador de tabela de roteamento mantém uma contagem de referência para todas as informações que ele mantém.
ms.assetid: bcd02881-b021-414f-8a40-14baac5baac7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f24653dd98db9b0427e5a3bee3f2f6613a68ce41
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916366"
---
# <a name="managing-handles"></a>Gerenciando identificadores

O Gerenciador de tabela de roteamento mantém uma contagem de referência para todas as informações que ele mantém. Isso impede que o Gerenciador de tabelas de roteamento retorne a um cliente quaisquer identificadores para a memória liberada. Cada vez que um identificador é retornado para o chamador, como um identificador explícito ou como parte de uma estrutura de informações, como [**\_ \_ informações de destino do RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_dest_info), a contagem de referência para o objeto que corresponde ao identificador é incrementada. Quando o identificador ou a estrutura de informações é liberada, a contagem de referência apropriada é diminuída. Quando a contagem de referência se torna zero, o objeto é liberado.

As funções [**RtmGetDestInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetdestinfo), [**RtmGetEntityInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetentityinfo), [**RtmGetRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetrouteinfo) e [**RtmGetNextHopInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetnexthopinfo) retornam estruturas de informações. Essas funções correspondem às funções [**RtmReleaseDestInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedestinfo), [**RtmReleaseEntityInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentityinfo), [**RtmReleaseRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaserouteinfo) e [**RtmRelaseNextHopInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthopinfo) , respectivamente.

> [!Note]  
> A função [**RtmReleaseChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasechangeddests) deve ser usada para liberar identificadores que foram retornados por uma chamada para [**RtmGetChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangeddests). Não use [**RtmReleaseDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedests) para estruturas de destino alteradas.

 

Se um cliente precisar manter um identificador específico em uma estrutura de informações ao liberar o restante, o cliente poderá chamar [**RtmReferenceHandles**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreferencehandles) com esse identificador antes de liberar a estrutura de informações. O identificador pode então ser liberado por uma chamada para as funções [**RtmReleaseDestInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedestinfo), [**RtmReleaseEntityInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentityinfo), [**RtmReleaseRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaserouteinfo) e [**RtmRelaseNextHopInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthopinfo) .

 

 




