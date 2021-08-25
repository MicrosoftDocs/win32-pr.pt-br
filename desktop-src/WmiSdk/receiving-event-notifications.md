---
description: Consultas de eventos são usadas por consumidores de eventos temporários, consumidores de eventos permanentes e provedores de eventos. Os consumidores de eventos usam consultas de eventos para especificar eventos de interesse e os provedores de eventos usam as consultas para especificar os eventos que eles fornecem.
ms.assetid: 851ad9bd-2604-4988-8de0-8d29b5300b21
ms.tgt_platform: multiple
title: Recebendo notificações de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1064fd0098ac72c6ceecbb5fcbc212fb38f6b2b25d0e61d8149bdb0fad177267
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996006"
---
# <a name="receiving-event-notifications"></a>Recebendo notificações de eventos

Consultas de eventos são usadas por consumidores de eventos temporários, consumidores de eventos permanentes e provedores de eventos. Os consumidores de eventos usam consultas de eventos para especificar eventos de interesse e os provedores de eventos usam as consultas para especificar os eventos que eles fornecem.

Os [consumidores](receiving-events-for-the-duration-of-your-application.md) temporários fazem consultas em chamadas para o método [**IWbemServices::ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) ou [**IWbemServices::ExecNotificationQueryAsync.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) [Os consumidores de](receiving-events-at-all-times.md) eventos permanentes fazem consultas na **propriedade Consulta** de uma instância da classe do [**\_ \_ sistema EventFilter.**](--eventfilter.md)

[Os provedores de eventos](writing-an-event-provider.md) usam consultas de eventos para se registrar para dar suporte a um ou mais tipos de eventos. Eles fazem consultas na propriedade **EventQueryList** de uma instância da classe do sistema [**\_ \_ EventProviderRegistration.**](--eventproviderregistration.md) Todos os provedores de eventos criam **\_ \_ uma instância EventProviderRegistration** para se registrar com o WMI (Instrumentação Windows Gerenciamento de Dados). Para obter mais informações, consulte [Registrando um provedor de eventos](registering-an-event-provider.md).

Os consumidores e provedores de eventos usam a instrução [SELECT](select-statement-for-event-queries.md) e uma cláusula WHERE relacionada para consultas de evento, além de uma variedade de extensões específicas para o WQL (linguagem WQL). As extensões são usadas para proteger os consumidores de serem inundados com notificações que ocorrem com muita frequência para serem úteis.

Os consumidores que não exigem notificação sempre que um evento ocorre podem especificar as seguintes cláusulas em suas consultas:

-   [Cláusula WITHIN](within-clause.md)
-   [Cláusula GROUP](group-clause.md)
-   [Cláusula HAVING](having-clause.md)

As cláusulas WITHIN e HAVING afetam o tempo dos eventos e a cláusula GROUP faz com que um evento representativo seja enviado no lugar de um evento que ocorre com frequência.

 

 



