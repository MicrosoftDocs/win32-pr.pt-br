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
# <a name="receiving-event-notifications"></a><span data-ttu-id="7b275-104">Recebendo notificações de eventos</span><span class="sxs-lookup"><span data-stu-id="7b275-104">Receiving Event Notifications</span></span>

<span data-ttu-id="7b275-105">As consultas de eventos são usadas por consumidores de eventos temporários, consumidores de eventos permanentes e provedores de eventos.</span><span class="sxs-lookup"><span data-stu-id="7b275-105">Event queries are used by temporary event consumers, permanent event consumers, and event providers.</span></span> <span data-ttu-id="7b275-106">Os consumidores de eventos usam consultas de eventos para especificar eventos de interesse, e os provedores de eventos usam as consultas para especificar os eventos que eles fornecem.</span><span class="sxs-lookup"><span data-stu-id="7b275-106">Event consumers use event queries to specify events of interest, and event providers use the queries to specify the events that they provide.</span></span>

<span data-ttu-id="7b275-107">Os [consumidores temporários](receiving-events-for-the-duration-of-your-application.md) colocam consultas em chamadas para o método [**IWbemServices:: ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) ou [**IWbemServices:: ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) .</span><span class="sxs-lookup"><span data-stu-id="7b275-107">[Temporary consumers](receiving-events-for-the-duration-of-your-application.md) place queries in calls to the [**IWbemServices::ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) or [**IWbemServices::ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) method.</span></span> <span data-ttu-id="7b275-108">Os [consumidores de eventos permanentes](receiving-events-at-all-times.md) colocam consultas na propriedade **Query** de uma instância da classe System [**\_ \_ EventFilter**](--eventfilter.md) .</span><span class="sxs-lookup"><span data-stu-id="7b275-108">[Permanent event consumers](receiving-events-at-all-times.md) place queries in the **Query** property of an instance of the [**\_\_EventFilter**](--eventfilter.md) system class.</span></span>

<span data-ttu-id="7b275-109">[Provedores de eventos](writing-an-event-provider.md) usam consultas de eventos para se registrar para dar suporte a um ou mais tipos de eventos.</span><span class="sxs-lookup"><span data-stu-id="7b275-109">[Event providers](writing-an-event-provider.md) use event queries to register to support one or more types of events.</span></span> <span data-ttu-id="7b275-110">Elas colocam consultas na propriedade **EventQueryList** de uma instância da classe de sistema [**\_ \_ EventProviderRegistration**](--eventproviderregistration.md) .</span><span class="sxs-lookup"><span data-stu-id="7b275-110">They place queries in the **EventQueryList** property of an instance of the [**\_\_EventProviderRegistration**](--eventproviderregistration.md) system class.</span></span> <span data-ttu-id="7b275-111">Todos os provedores de eventos criam uma instância de **\_ \_ EventProviderRegistration** para registrar com instrumentação de gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="7b275-111">All event providers create an **\_\_EventProviderRegistration** instance to register with Windows Management Instrumentation (WMI).</span></span> <span data-ttu-id="7b275-112">Para obter mais informações, consulte [registrando um provedor de eventos](registering-an-event-provider.md).</span><span class="sxs-lookup"><span data-stu-id="7b275-112">For more information, see [Registering an Event Provider](registering-an-event-provider.md).</span></span>

<span data-ttu-id="7b275-113">Os consumidores e os provedores de eventos usam a [instrução SELECT](select-statement-for-event-queries.md) e uma cláusula WHERE relacionada para consultas de eventos, além de uma variedade de extensões específicas para o linguagem WQL (WQL).</span><span class="sxs-lookup"><span data-stu-id="7b275-113">Event consumers and providers use the [SELECT statement](select-statement-for-event-queries.md) and a related WHERE clause for event queries, plus a variety of extensions specific to the WMI Query Language (WQL).</span></span> <span data-ttu-id="7b275-114">As extensões são usadas para proteger os consumidores de serem inundados com notificações que ocorrem com muita frequência para serem úteis.</span><span class="sxs-lookup"><span data-stu-id="7b275-114">The extensions are used to protect consumers from being flooded with notifications that occur too frequently to be useful.</span></span>

<span data-ttu-id="7b275-115">Os consumidores que não exigem notificação toda vez que um evento ocorrer podem especificar as seguintes cláusulas em suas consultas:</span><span class="sxs-lookup"><span data-stu-id="7b275-115">Consumers that do not require notification each time an event occurs can specify the following clauses in their queries:</span></span>

-   <span data-ttu-id="7b275-116">Cláusula [Within](within-clause.md)</span><span class="sxs-lookup"><span data-stu-id="7b275-116">[WITHIN](within-clause.md) clause</span></span>
-   <span data-ttu-id="7b275-117">Cláusula [Group](group-clause.md)</span><span class="sxs-lookup"><span data-stu-id="7b275-117">[GROUP](group-clause.md) clause</span></span>
-   <span data-ttu-id="7b275-118">Cláusula [having](having-clause.md)</span><span class="sxs-lookup"><span data-stu-id="7b275-118">[HAVING](having-clause.md) clause</span></span>

<span data-ttu-id="7b275-119">As cláusulas in e HAVING afetam o tempo dos eventos e a cláusula GROUP faz com que um evento representativo seja enviado no lugar de um evento que ocorre com frequência.</span><span class="sxs-lookup"><span data-stu-id="7b275-119">The WITHIN and HAVING clauses affect the timing of events, and the GROUP clause causes a representative event to be sent in place of a frequently occurring event.</span></span>

 

 



