---
description: O WMI mapeia automaticamente interceptações SNMP para eventos WMI. O sistema coloca os dados contidos na interceptação nas propriedades correspondentes de uma instância de evento WMI para acesso pelo computador host WMI.
ms.assetid: 549f58a9-9d3b-41b9-a374-ab83877f63a7
ms.tgt_platform: multiple
title: Recebendo interceptações SNMP como eventos WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da24be8ea9a4882af0b961b1d0f6f0c3d442c70c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505679"
---
# <a name="receiving-snmp-traps-as-wmi-events"></a><span data-ttu-id="01ddd-104">Recebendo interceptações SNMP como eventos WMI</span><span class="sxs-lookup"><span data-stu-id="01ddd-104">Receiving SNMP Traps as WMI Events</span></span>

<span data-ttu-id="01ddd-105">O WMI mapeia automaticamente interceptações SNMP para eventos WMI.</span><span class="sxs-lookup"><span data-stu-id="01ddd-105">WMI automatically maps SNMP traps to WMI events.</span></span> <span data-ttu-id="01ddd-106">O sistema coloca os dados contidos na interceptação nas propriedades correspondentes de uma instância de evento WMI para acesso pelo computador host WMI.</span><span class="sxs-lookup"><span data-stu-id="01ddd-106">The system places the data contained in the trap in the corresponding properties of a WMI event instance for access by the WMI host machine.</span></span>

> [!Note]  
> <span data-ttu-id="01ddd-107">Para obter mais informações sobre como instalar o provedor, consulte [Configurando o ambiente SNMP WMI](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="01ddd-107">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="01ddd-108">O recebimento de uma interceptação SNMP é quase idêntico ao recebimento de eventos de qualquer outro provedor WMI.</span><span class="sxs-lookup"><span data-stu-id="01ddd-108">Receiving an SNMP trap is nearly identical to receiving events from any other WMI provider.</span></span> <span data-ttu-id="01ddd-109">No entanto, o filtro de eventos SNMP tem várias classes exclusivas que você deve conhecer antes de se registrar para eventos.</span><span class="sxs-lookup"><span data-stu-id="01ddd-109">However, the SNMP event filter has several unique classes to be aware of before registering for events.</span></span> <span data-ttu-id="01ddd-110">Além disso, o provedor de eventos requer o uso \\ exclusivo do namespace Smir.</span><span class="sxs-lookup"><span data-stu-id="01ddd-110">Also, the event provider requires the use of the \\smir namespace exclusively.</span></span>

<span data-ttu-id="01ddd-111">As classes mais comuns a serem registradas são [SnmpNotification](snmpnotification.md) e [SnmpExtendedNotification](snmpextendednotification.md).</span><span class="sxs-lookup"><span data-stu-id="01ddd-111">The most common classes to register with are [SnmpNotification](snmpnotification.md) and [SnmpExtendedNotification](snmpextendednotification.md).</span></span> <span data-ttu-id="01ddd-112">Os consumidores tentam usar notificações de eventos para atualizar valores em dispositivos SNMP monitorados devem se registrar para eventos SnmpExtendedNotification.</span><span class="sxs-lookup"><span data-stu-id="01ddd-112">Consumers intent on using event notifications to update values in monitored SNMP devices must register for SnmpExtendedNotification events.</span></span> <span data-ttu-id="01ddd-113">As informações de eventos SnmpNotification não são reutilizáveis.</span><span class="sxs-lookup"><span data-stu-id="01ddd-113">The information from SnmpNotification events is not reusable.</span></span>

<span data-ttu-id="01ddd-114">A tabela a seguir lista informações sobre como configurar seu computador para receber Interceptações SNMP como eventos WMI.</span><span class="sxs-lookup"><span data-stu-id="01ddd-114">The following table lists information about setting up your computer to receive SNMP traps as WMI events.</span></span>



| <span data-ttu-id="01ddd-115">Tarefa</span><span class="sxs-lookup"><span data-stu-id="01ddd-115">Task</span></span>                                                                               | <span data-ttu-id="01ddd-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="01ddd-116">Description</span></span>                                                                        |
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="01ddd-117">Escolhendo entre provedores de eventos SNMP</span><span class="sxs-lookup"><span data-stu-id="01ddd-117">Choosing Between SNMP Event Providers</span></span>](choosing-between-snmp-event-providers.md) | <span data-ttu-id="01ddd-118">O WMI inclui dois provedores de eventos SNMP.</span><span class="sxs-lookup"><span data-stu-id="01ddd-118">WMI includes two SNMP event providers.</span></span>                                             |
| [<span data-ttu-id="01ddd-119">Recebendo eventos SNMP</span><span class="sxs-lookup"><span data-stu-id="01ddd-119">Receiving SNMP Events</span></span>](receiving-snmp-events.md)                                 | <span data-ttu-id="01ddd-120">Os provedores de eventos SNMP dão suporte a três tipos de interceptações de SNMPv1 e notificações de SNMPv2.</span><span class="sxs-lookup"><span data-stu-id="01ddd-120">SNMP event providers support three types of SNMPv1 traps and SNMPv2 notifications.</span></span> |



 

<span data-ttu-id="01ddd-121">O exemplo a seguir configura um computador para monitorar o evento **SnmpLinkUpNotification** de um hub gerenciado.</span><span class="sxs-lookup"><span data-stu-id="01ddd-121">The following example sets up a computer to monitor for the **SnmpLinkUpNotification** event from a managed hub.</span></span>


```VB
Set objLocator = CreateObject("wbemscripting.swbemlocator")
Set objServices = objLocator.ConnectServer(, "root\snmp\mngd_hub")

set objwbemEventsource = _ 
    objServices.ExecNotificationQuery _
   ("SELECT * FROM SnmpLinkUpNotification")

set objWbemObject = objwbemEventsource.NextEvent()

wscript.echo "Received " & objWbemObject.path_.class

for each prop in objWbemObject.properties_
    wscript.echo prop.name & " -- " & prop.value
next
```



 

 



