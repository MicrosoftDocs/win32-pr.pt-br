---
description: Os provedores de eventos SNMP recebem pacotes de eventos SNMP da pilha WINSNMP e convertem as informações incluídas nos pacotes em eventos WMI.
ms.assetid: 4ae0a734-39b0-4418-b55c-6d8f093806a8
ms.tgt_platform: multiple
title: Escolhendo entre provedores de eventos SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0902c463ee0fc51505e125a329f592ebced6df20ec7f63296ba7248cd8dade98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131869"
---
# <a name="choosing-between-snmp-event-providers"></a>Escolhendo entre provedores de eventos SNMP

Os provedores de eventos SNMP recebem pacotes de eventos SNMP da pilha WINSNMP e convertem as informações incluídas nos pacotes em eventos WMI.

O WMI inclui os dois provedores de eventos SNMP a seguir:

-   SeeP (Provedor de Eventos Encapsulado SNMP)

    Provisionamento encapsulado significa que a instância de evento tem propriedades simples que descrevem as informações mapeadas diretamente da interceptação SNMP.

-   Provedor de eventos de referência SNMP (SREP)

    Provisionamento de referência abstrai as informações presentes na interceptações SNMP para que as propriedades que compartilham a mesma classe e instância sejam apresentadas como objetos inseridos. Isso permite que a instância exclusiva, com a qual a interceptação está associada, seja recuperada após o recebimento do evento, usando o SNMP \_ \_ RELPATH.

> [!Note]  
> Para obter mais informações sobre como instalar o provedor, consulte [Configurando o ambiente WMI SNMP](setting-up-the-wmi-snmp-environment.md).

 

Independentemente de o evento SNMP ser uma interceptação SNMPv1 ou uma notificação SNMPv2C, a pilha o relata como uma notificação SNMPv2. Portanto, os provedores de eventos processam todos os eventos SNMP como notificações SNMPv2.

Para descrever os eventos SNMP para consumidores WMI, cada provedor de eventos dá suporte a uma hierarquia de classes que deriva da classe de sistema [**\_ \_ ExtrinsicEvent.**](--extrinsicevent.md) A [classe SNMPNotification](snmpnotification.md) é a classe pai para a hierarquia SEEP; A [classe SNMPExtendedNotification](snmpextendednotification.md) é a classe pai da hierarquia SREP.

 

 



