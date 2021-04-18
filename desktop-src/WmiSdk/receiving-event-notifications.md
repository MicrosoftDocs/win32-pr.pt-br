---
description: As consultas de eventos são usadas por consumidores de eventos temporários, consumidores de eventos permanentes e provedores de eventos. Os consumidores de eventos usam consultas de eventos para especificar eventos de interesse, e os provedores de eventos usam as consultas para especificar os eventos que eles fornecem.
ms.assetid: 851ad9bd-2604-4988-8de0-8d29b5300b21
ms.tgt_platform: multiple
title: Recebendo notificações de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43873c03155f2186f9d3a9a3daff9b8e322e511f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105751112"
---
# <a name="receiving-event-notifications"></a>Recebendo notificações de eventos

As consultas de eventos são usadas por consumidores de eventos temporários, consumidores de eventos permanentes e provedores de eventos. Os consumidores de eventos usam consultas de eventos para especificar eventos de interesse, e os provedores de eventos usam as consultas para especificar os eventos que eles fornecem.

Os [consumidores temporários](receiving-events-for-the-duration-of-your-application.md) colocam consultas em chamadas para o método [**IWbemServices:: ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) ou [**IWbemServices:: ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) . Os [consumidores de eventos permanentes](receiving-events-at-all-times.md) colocam consultas na propriedade **Query** de uma instância da classe System [**\_ \_ EventFilter**](--eventfilter.md) .

[Provedores de eventos](writing-an-event-provider.md) usam consultas de eventos para se registrar para dar suporte a um ou mais tipos de eventos. Elas colocam consultas na propriedade **EventQueryList** de uma instância da classe de sistema [**\_ \_ EventProviderRegistration**](--eventproviderregistration.md) . Todos os provedores de eventos criam uma instância de **\_ \_ EventProviderRegistration** para registrar com instrumentação de gerenciamento do Windows (WMI). Para obter mais informações, consulte [registrando um provedor de eventos](registering-an-event-provider.md).

Os consumidores e os provedores de eventos usam a [instrução SELECT](select-statement-for-event-queries.md) e uma cláusula WHERE relacionada para consultas de eventos, além de uma variedade de extensões específicas para o linguagem WQL (WQL). As extensões são usadas para proteger os consumidores de serem inundados com notificações que ocorrem com muita frequência para serem úteis.

Os consumidores que não exigem notificação toda vez que um evento ocorrer podem especificar as seguintes cláusulas em suas consultas:

-   Cláusula [Within](within-clause.md)
-   Cláusula [Group](group-clause.md)
-   Cláusula [having](having-clause.md)

As cláusulas in e HAVING afetam o tempo dos eventos e a cláusula GROUP faz com que um evento representativo seja enviado no lugar de um evento que ocorre com frequência.

 

 



