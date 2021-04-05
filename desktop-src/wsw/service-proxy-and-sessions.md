---
title: Proxy de serviço e sessões
description: O proxy de serviço tem comportamentos especiais para associações de canal baseadas em sessão e não em sessão.
ms.assetid: 6dc9de95-b97c-4acc-9d45-d5e6ebb6bd77
keywords:
- Serviços Web de sessões e proxy de serviço para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fc8477a8cd03579e1d8cbfe4509f89890af8482
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104008619"
---
# <a name="service-proxy-and-sessions"></a>Proxy de serviço e sessões

O [proxy de serviço](service-proxy.md) tem comportamentos especiais para associações de canal baseadas em sessão e não em sessão. O proxy de serviço fornece semântica baseada em sessão se a associação de canal subjacente for baseada em sessão. Nesse caso, um único canal é usado para chamadas de serviço. No entanto, se a associação de canal não for baseada em sessão, o proxy de serviço criará um canal separado para cada chamada. Observe, no entanto, que os canais não baseados em sessão são agrupados e talvez reutilizados. Ao reutilizar um canal, o proxy de serviço mantém o canal aberto se o canal subjacente não tiver falhado ou se a chamada em um canal resultar na falha do proxy de serviço no canal. Observe que. exceto no caso de uma falha, quando um canal é aberto, ele é mantido aberto, desde que o proxy de serviço esteja aberto e seja fechado somente quando o proxy de serviço é fechado.


Se a associação de canal for baseada em sessão e se as falhas de canal subjacentes, a máquina de estado do proxy de serviço passará para o estado de [**falha do estado do \_ proxy de serviço \_ \_ \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_proxy_state) . No caso de uma associação de canal baseada em não sessão, uma falha no canal subjacente não faz com que o proxy faça a transição para o estado de **\_ \_ \_ \_ falha de proxy do WS Service** .

Para obter mais informações sobre o proxy de serviço e sua relação com o estado, consulte o tópico [proxy de serviço](service-proxy.md) . Para obter exemplos de associações de canal diferentes, consulte os exemplos a seguir:

-   Associação de canal de não sessão, [HttpCalculatorClientExample](httpcalculatorclientexample.md)
-   Associação de canal baseada em sessão, [SessionfullCalculatorClientExample](sessionfullcalculatorclientexample.md)

 

 




