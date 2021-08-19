---
title: Gerenciando interceptações e notificações
description: O aplicativo WinSNMP deve se registrar para receber interceptações e notificações chamando a função SnmpRegister com SNMPAPI \_ ON. O aplicativo pode desativar o registro e desabilitar interceptações e notificações chamando a função com SNMPAPI \_ OFF.
ms.assetid: 2bccba35-bf5c-4e5c-94e4-59980f2b9776
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 402a768aa28efb6f2fdc18994d749cfca2f2c412f748f853fb76fcd7fe3e41d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009374"
---
# <a name="managing-traps-and-notifications"></a>Gerenciando interceptações e notificações

O aplicativo WinSNMP deve se registrar para receber interceptações e notificações chamando a função [**SnmpRegister**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister) com SNMPAPI \_ ON. O aplicativo pode desativar o registro e desabilitar interceptações e notificações chamando a função com SNMPAPI \_ OFF.

Várias opções estão disponíveis quando o aplicativo chama **SnmpRegister**. O aplicativo pode registrar ou não registrar para as seguintes interceptações e notificações:

-   Um tipo de interceptação ou notificação
-   Todas as interceptações e notificações
-   Todas as fontes de solicitações de interceptação e notificação
-   Interceptações e notificações de todas as entidades de gerenciamento
-   Interceptações e notificações para cada contexto

Para registrar e receber um tipo predefinido de interceptação ou notificação, o aplicativo deve definir um identificador de objeto (uma estrutura [**smiOID)**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) para cada tipo predefinido. A estrutura deve conter uma sequência de correspondência de padrões para o tipo de interceptação ou notificação. RFC 1907, "Base de informações de gerenciamento para a versão 2 do protocolo SNMPv2)" define identificadores de objeto de interceptação e notificação.

Para recuperar dados de interceptação e notificações pendentes para uma sessão WinSNMP, um aplicativo WinSNMP deve chamar a função [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) com o alçamento de sessão retornado pela [**função SnmpCreateSession.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession)

Para obter mais informações, consulte [Enviando mensagens SNMP e](sending-snmp-messages.md) recebendo mensagens [SNMP](receiving-snmp-messages.md). Para obter informações adicionais sobre alocação e desalocação de recursos para interceptações e notificações, consulte [Alocando objetos de memória WinSNMP.](allocating-winsnmp-memory-objects.md)

 

 




