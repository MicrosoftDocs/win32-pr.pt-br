---
title: Gerenciando identificadores
description: O Gerenciador de tabela de roteamento mantém uma contagem de referência para todas as informações que ele mantém.
ms.assetid: bcd02881-b021-414f-8a40-14baac5baac7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c701dbe8469baab54c427d42f9d603a976402ebb5693d1799989aeff74b65945
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117790599"
---
# <a name="managing-handles"></a>Gerenciando identificadores

O Gerenciador de tabela de roteamento mantém uma contagem de referência para todas as informações que ele mantém. Isso impede que o Gerenciador de tabelas de roteamento retorne a um cliente quaisquer identificadores para a memória liberada. Cada vez que um identificador é retornado para o chamador, como um identificador explícito ou como parte de uma estrutura de informações, como [**\_ \_ informações de destino do RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_dest_info), a contagem de referência para o objeto que corresponde ao identificador é incrementada. Quando o identificador ou a estrutura de informações é liberada, a contagem de referência apropriada é diminuída. Quando a contagem de referência se torna zero, o objeto é liberado.

As funções [**RtmGetDestInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetdestinfo), [**RtmGetEntityInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetentityinfo), [**RtmGetRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetrouteinfo) e [**RtmGetNextHopInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetnexthopinfo) retornam estruturas de informações. Essas funções correspondem às funções [**RtmReleaseDestInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedestinfo), [**RtmReleaseEntityInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentityinfo), [**RtmReleaseRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaserouteinfo) e [**RtmRelaseNextHopInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthopinfo) , respectivamente.

> [!Note]  
> A função [**RtmReleaseChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasechangeddests) deve ser usada para liberar identificadores que foram retornados por uma chamada para [**RtmGetChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangeddests). Não use [**RtmReleaseDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedests) para estruturas de destino alteradas.

 

Se um cliente precisar manter um identificador específico em uma estrutura de informações ao liberar o restante, o cliente poderá chamar [**RtmReferenceHandles**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreferencehandles) com esse identificador antes de liberar a estrutura de informações. O identificador pode então ser liberado por uma chamada para as funções [**RtmReleaseDestInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedestinfo), [**RtmReleaseEntityInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentityinfo), [**RtmReleaseRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaserouteinfo) e [**RtmRelaseNextHopInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthopinfo) .

 

 




