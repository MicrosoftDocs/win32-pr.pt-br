---
description: Classes de solução de problemas de eventos do serviço WMI são geradas por eventos dentro do serviço WMI, como a criação do pool de threads.
ms.assetid: 1a1251c8-a2f7-47ac-9db1-d780d7d272f0
ms.tgt_platform: multiple
title: Classes de solução de problemas de eventos do serviço WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99be30a6b2f0551cae4e0abe269da5341e34e1444eb1545ca96377a43b5415ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119502796"
---
# <a name="wmi-service-event-troubleshooting-classes"></a>Classes de solução de problemas de eventos do serviço WMI

Classes de solução de problemas de eventos do serviço WMI são geradas por eventos dentro do serviço WMI, como a criação do pool de threads.

Você pode assinar as notificações da classe base [**abstrata \_ MSFT WmiEssEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiessevent) para obter todos os eventos derivados listados na tabela a seguir.



|   Evento                                                                                        |   Descrição                                                                                             |
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**MSFT \_ WmiEssEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiessevent)                                   | Classe pai para todos os Windows eventos de ESS (Subsistema de Eventos) de WMI (Instrumentação de Gerenciamento) de todos os eventos. |
| [**MSFT \_ WmiRegisterNotificationEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiregisternotificationevent) | Representa a criação de um sink de evento para notificação de uma consulta de evento.                       |
| [**MSFT \_ WmiCancelNotificationSink**](/previous-versions/windows/desktop/wmisystemprov/msft-wmicancelnotificationsink)       | gerado quando um sink de evento é cancelado.                                                           |
| [**MSFT \_ WmiThreadPoolEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmithreadpoolevent)                     | fornece notificação de eventos de thread no ESS (Subsistema de Eventos WMI).                           |
| [**MSFT \_ WmiThreadPoolCreated**](/previous-versions/windows/desktop/wmisystemprov/msft-wmithreadpoolcreated)                 | Fornece notificação quando um thread é criado no ESS (Subsistema de Eventos WMI).                   |
| [**MSFT \_ WmiThreadPoolDeleted**](/previous-versions/windows/desktop/wmisystemprov/msft-wmithreadpooldeleted)                 | Fornece notificação quando um thread é excluído no ESS (Subsistema de Eventos WMI).                   |
| [**MSFT \_ WmiFilterEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmifilterevent)                             | Classe pai para todos os eventos de filtro de consumidor de eventos permanentes.                                        |
| [**MSFT \_ WmiFilterActivated**](/previous-versions/windows/desktop/wmisystemprov/msft-wmifilteractivated)                     | Define a ativação bem-sucedida de um filtro de assinatura de consumidor de evento permanente.                |
| [**MSFT \_ WmiFilterDeactivated**](/previous-versions/windows/desktop/wmisystemprov/msft-wmifilterdeactivated)                 | Define a desativação bem-sucedida de um filtro de assinatura de consumidor permanente.                    |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Solução de problemas de WMI](wmi-troubleshooting.md)
</dt> <dt>

Solução de problemas de WMI
</dt> <dt>

[Eventos de monitoramento](monitoring-events.md)
</dt> <dt>

[Recebendo um evento WMI](receiving-a-wmi-event.md)
</dt> </dl>

 

 
