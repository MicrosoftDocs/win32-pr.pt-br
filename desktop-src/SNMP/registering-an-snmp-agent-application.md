---
title: Registrando um aplicativo de agente SNMP
description: Além das operações do gerenciador SNMP, a API WinSNMP versão 2.0 também dá suporte a operações de agente SNMP.
ms.assetid: 473560b5-4611-410e-aeae-764c9c76e765
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c3415e511639c7cbbc18455ed93be74e11414c1f442797c8b72f7456092757c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009124"
---
# <a name="registering-an-snmp-agent-application"></a>Registrando um aplicativo de agente SNMP

Além das operações do gerenciador SNMP, a API WinSNMP versão 2.0 também dá suporte a operações de agente SNMP.

Para registrar um aplicativo WinSNMP como um agente SNMP, o aplicativo pode chamar a [**função SnmpListen.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmplisten) Essa função informa à implementação do Microsoft WinSNMP que uma entidade SNMP atuará na função de um agente SNMP. O aplicativo também pode chamar **SnmpListen** para informar a implementação quando ele não atuará mais como um agente.

Se um aplicativo chamar a [**função SnmpListen**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmplisten) e passar o valor SNMPAPI ON no parâmetro \_ *lStatus,* ocorrerão as seguintes ações:

1.  A entidade que funcionará em uma função de agente SNMP é vinculada à porta atribuída e "escuta" as solicitações de mensagem SNMP de entrada.
2.  O agente usa a lógica específica do aplicativo para processar cada solicitação SNMP.
3.  O agente forma respostas apropriadas para cada solicitação.
4.  O agente transmite a resposta para a entidade solicitante chamando a [**função SnmpSendMsg.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) Quando o agente chama **SnmpSendMsg**, ele especifica o endereço do agente no parâmetro *srcEntity* e o endereço da entidade do gerenciador remoto no parâmetro *dstEntity.* (Esses valores são o inverso dos valores que a entidade do agente recebeu nesses parâmetros quando chamou a função [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) para recuperar uma solicitação SNMP.)

Para obter mais informações sobre aplicativos de gerenciamento SNMP e aplicativos de agente, consulte [About SNMP](about-snmp.md).

 

 




