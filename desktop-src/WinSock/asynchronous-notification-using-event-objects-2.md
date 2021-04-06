---
description: As funções WSAEventSelect e WSAEnumNetworkEvents são fornecidas para acomodar aplicativos como daemons e serviços que não têm nenhuma interface do usuário (e, portanto, não usam identificadores do Windows).
ms.assetid: 4254937c-7ee6-49a3-9f30-09aebaf2265b
title: Notificação assíncrona usando objetos de evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d0495507eacf0960dc98f31594d7f4881d51488
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827125"
---
# <a name="asynchronous-notification-using-event-objects"></a>Notificação assíncrona usando objetos de evento

As funções [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) e [**WSAEnumNetworkEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnetworkevents) são fornecidas para acomodar aplicativos como daemons e serviços que não têm nenhuma interface do usuário (e, portanto, não usam identificadores do Windows). A função **WSAEventSelect** se comporta exatamente como a função [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) . No entanto, em vez de fazer com que uma mensagem do Windows seja enviada na ocorrência de um \_ evento de rede FD xxx (por exemplo, FD \_ Read e FD \_ Write), um objeto de evento designado pelo aplicativo é definido.

Além disso, o fato de que um \_ evento de rede FD xxx específico ocorreu é lembrado pelo provedor de serviços. O aplicativo pode chamar [**WSAEnumNetworkEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) para que o conteúdo atual da memória de evento de rede seja copiado para um buffer fornecido pelo aplicativo e que a memória do evento de rede seja automaticamente limpa. Se necessário, o aplicativo também pode designar um objeto de evento específico que é limpo junto com a memória de evento de rede.

 

 



