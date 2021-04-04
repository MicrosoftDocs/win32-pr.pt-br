---
title: Gerenciando interceptações e notificações
description: O aplicativo WinSNMP deve se registrar para receber interceptações e notificações chamando a função SnmpRegister com SNMPAPI \_ em. O aplicativo pode cancelar o registro e desabilitar interceptações e notificações chamando a função com SNMPAPI \_ off.
ms.assetid: 2bccba35-bf5c-4e5c-94e4-59980f2b9776
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51e3a2d9fed1f7c34dd8191550d1dbc68ed984e5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822876"
---
# <a name="managing-traps-and-notifications"></a>Gerenciando interceptações e notificações

O aplicativo WinSNMP deve se registrar para receber interceptações e notificações chamando a função [**SnmpRegister**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister) com snmpapi \_ em. O aplicativo pode cancelar o registro e desabilitar interceptações e notificações chamando a função com SNMPAPI \_ off.

Várias opções estão disponíveis quando o aplicativo chama **SnmpRegister**. O aplicativo pode registrar ou cancelar o registro para as seguintes interceptações e notificações:

-   Um tipo de interceptação ou notificação
-   Todas as interceptações e notificações
-   Todas as fontes de solicitações de interceptação e notificação
-   Interceptações e notificações de todas as entidades de gerenciamento
-   Interceptações e notificações para cada contexto

Para registrar e receber uma interceptação predefinida ou um tipo de notificação, o aplicativo deve definir um identificador de objeto (uma estrutura [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) ) para cada tipo predefinido. A estrutura deve conter uma sequência de correspondência de padrões para o tipo de interceptação ou notificação. A RFC 1907, "base de informações de gerenciamento para a versão 2 do protocolo SNMPv2 (Simple Network Management Protocol)", define os identificadores de objeto de interceptação e de notificação.

Para recuperar dados de interceptação pendentes e notificações para uma sessão de WinSNMP, um aplicativo WinSNMP deve chamar a função [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) com o identificador de sessão retornado pela função [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession) .

Para obter mais informações, consulte [enviando mensagens SNMP](sending-snmp-messages.md) e [recebendo mensagens SNMP](receiving-snmp-messages.md). Para obter informações adicionais sobre alocação e desalocação de recursos para interceptações e notificações, consulte [alocando objetos de memória WinSNMP](allocating-winsnmp-memory-objects.md).

 

 




