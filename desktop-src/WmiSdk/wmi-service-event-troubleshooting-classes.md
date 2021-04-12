---
description: As classes de solução de problemas de eventos do serviço WMI são geradas por eventos dentro do serviço WMI, como a criação do pool de threads.
ms.assetid: 1a1251c8-a2f7-47ac-9db1-d780d7d272f0
ms.tgt_platform: multiple
title: Classes de solução de problemas de eventos do serviço WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbf3728b6ae150a948fdf71515e27f17ca7280f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171652"
---
# <a name="wmi-service-event-troubleshooting-classes"></a>Classes de solução de problemas de eventos do serviço WMI

As classes de solução de problemas de eventos do serviço WMI são geradas por eventos dentro do serviço WMI, como a criação do pool de threads.

Você pode assinar as notificações do [**MSFT \_ WmiEssEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiessevent) da classe base abstrata para obter todos os eventos derivados listados na tabela a seguir.



|                                                                                           |                                                                                                     |
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**\_WMIESSEVENT MSFT**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiessevent)                                   | Classe pai para todos Instrumentação de Gerenciamento do Windows os eventos self (WMI) auto Event Subsystem (ESS). |
| [**\_WMIREGISTERNOTIFICATIONEVENT MSFT**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiregisternotificationevent) | Representa a criação de um coletor de eventos para notificação para uma consulta de evento.                       |
| [**\_WMICANCELNOTIFICATIONSINK MSFT**](/previous-versions/windows/desktop/wmisystemprov/msft-wmicancelnotificationsink)       | gerado quando um coletor de eventos é cancelado.                                                           |
| [**\_WMITHREADPOOLEVENT MSFT**](/previous-versions/windows/desktop/wmisystemprov/msft-wmithreadpoolevent)                     | fornece a notificação de eventos de thread no grupo de eventos do WMI (ESS).                           |
| [**\_WMITHREADPOOLCREATED MSFT**](/previous-versions/windows/desktop/wmisystemprov/msft-wmithreadpoolcreated)                 | Fornece uma notificação quando um thread é criado no grupo de eventos do WMI (ESS).                   |
| [**\_WMITHREADPOOLDELETED MSFT**](/previous-versions/windows/desktop/wmisystemprov/msft-wmithreadpooldeleted)                 | Fornece notificação quando um thread é excluído no ESS (sistema de eventos do WMI).                   |
| [**\_WMIFILTEREVENT MSFT**](/previous-versions/windows/desktop/wmisystemprov/msft-wmifilterevent)                             | Classe pai para todos os eventos de filtro de consumidor de evento permanente.                                        |
| [**\_WMIFILTERACTIVATED MSFT**](/previous-versions/windows/desktop/wmisystemprov/msft-wmifilteractivated)                     | Define a ativação bem-sucedida de um filtro de assinatura de consumidor de evento permanente.                |
| [**\_WMIFILTERDEACTIVATED MSFT**](/previous-versions/windows/desktop/wmisystemprov/msft-wmifilterdeactivated)                 | Define a desativação bem-sucedida de um filtro de assinatura de consumidor permanente.                    |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Solução de problemas do WMI](wmi-troubleshooting.md)
</dt> <dt>

Solução de problemas do WMI
</dt> <dt>

[Eventos de monitoramento](monitoring-events.md)
</dt> <dt>

[Recebendo um evento WMI](receiving-a-wmi-event.md)
</dt> </dl>

 

 
