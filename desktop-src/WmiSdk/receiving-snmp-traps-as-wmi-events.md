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
# <a name="receiving-snmp-traps-as-wmi-events"></a>Recebendo interceptações SNMP como eventos WMI

O WMI mapeia automaticamente interceptações SNMP para eventos WMI. O sistema coloca os dados contidos na interceptação nas propriedades correspondentes de uma instância de evento WMI para acesso pelo computador host WMI.

> [!Note]  
> Para obter mais informações sobre como instalar o provedor, consulte [Configurando o ambiente SNMP WMI](setting-up-the-wmi-snmp-environment.md).

 

O recebimento de uma interceptação SNMP é quase idêntico ao recebimento de eventos de qualquer outro provedor WMI. No entanto, o filtro de eventos SNMP tem várias classes exclusivas que você deve conhecer antes de se registrar para eventos. Além disso, o provedor de eventos requer o uso \\ exclusivo do namespace Smir.

As classes mais comuns a serem registradas são [SnmpNotification](snmpnotification.md) e [SnmpExtendedNotification](snmpextendednotification.md). Os consumidores tentam usar notificações de eventos para atualizar valores em dispositivos SNMP monitorados devem se registrar para eventos SnmpExtendedNotification. As informações de eventos SnmpNotification não são reutilizáveis.

A tabela a seguir lista informações sobre como configurar seu computador para receber Interceptações SNMP como eventos WMI.



| Tarefa                                                                               | Descrição                                                                        |
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [Escolhendo entre provedores de eventos SNMP](choosing-between-snmp-event-providers.md) | O WMI inclui dois provedores de eventos SNMP.                                             |
| [Recebendo eventos SNMP](receiving-snmp-events.md)                                 | Os provedores de eventos SNMP dão suporte a três tipos de interceptações de SNMPv1 e notificações de SNMPv2. |



 

O exemplo a seguir configura um computador para monitorar o evento **SnmpLinkUpNotification** de um hub gerenciado.


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



 

 



