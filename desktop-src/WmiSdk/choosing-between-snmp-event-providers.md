---
description: Os provedores de eventos SNMP recebem pacotes de eventos SNMP da pilha WINSNMP e convertem as informações incluídas nos pacotes em eventos WMI.
ms.assetid: 4ae0a734-39b0-4418-b55c-6d8f093806a8
ms.tgt_platform: multiple
title: Escolhendo entre provedores de eventos SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dabd8f6d432025406a5faecc3ace423cd6671e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105768335"
---
# <a name="choosing-between-snmp-event-providers"></a>Escolhendo entre provedores de eventos SNMP

Os provedores de eventos SNMP recebem pacotes de eventos SNMP da pilha WINSNMP e convertem as informações incluídas nos pacotes em eventos WMI.

O WMI inclui os dois provedores de eventos SNMP a seguir:

-   Provedor de eventos encapsulados SNMP (SEEP)

    O provisionamento encapsulado significa que a instância de evento tem propriedades simples que descrevem as informações mapeadas diretamente da interceptação SNMP.

-   Provedor de eventos Referent SNMP (SREP)

    O provisionamento de Referent abstrai as informações presentes dentro da interceptação SNMP para que as propriedades que compartilham a mesma classe e instância sejam apresentadas como objetos incorporados. Isso permite a instância exclusiva, com a qual a interceptação está associada, a ser recuperada após o recebimento do evento, usando o SNMP \_ \_ RelPath.

> [!Note]  
> Para obter mais informações sobre como instalar o provedor, consulte [Configurando o ambiente SNMP WMI](setting-up-the-wmi-snmp-environment.md).

 

Independentemente de o evento SNMP ser um Trap de SNMPv1 ou uma notificação de SNMPv2C, a pilha o relatará como uma notificação de SNMPv2. Portanto, os provedores de eventos processam todos os eventos SNMP como notificações de SNMPv2.

Para descrever os eventos SNMP para consumidores do WMI, cada provedor de eventos dá suporte a uma hierarquia de classes que deriva da classe de sistema [**\_ \_ ExtrinsicEvent**](--extrinsicevent.md) . A classe [SNMPNotification](snmpnotification.md) é a classe pai da hierarquia seep; a classe [SNMPExtendedNotification](snmpextendednotification.md) é a classe pai da hierarquia SREP.

 

 



