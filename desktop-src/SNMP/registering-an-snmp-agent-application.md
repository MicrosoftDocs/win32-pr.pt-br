---
title: Registrando um aplicativo de agente SNMP
description: Além das operações do Gerenciador SNMP, a versão de API WinSNMP 2,0 também dá suporte a operações de agente SNMP.
ms.assetid: 473560b5-4611-410e-aeae-764c9c76e765
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40922469c52e33e4b5c2f408c1c107b6784529f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916447"
---
# <a name="registering-an-snmp-agent-application"></a>Registrando um aplicativo de agente SNMP

Além das operações do Gerenciador SNMP, a versão de API WinSNMP 2,0 também dá suporte a operações de agente SNMP.

Para registrar um aplicativo WinSNMP como um agente SNMP, o aplicativo pode chamar a função [**SnmpListen**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmplisten) . Essa função informa à implementação do Microsoft WinSNMP que uma entidade SNMP atuará na função de um agente SNMP. O aplicativo também pode chamar **SnmpListen** para informar a implementação quando ela não funcionará mais como um agente.

Se um aplicativo chamar a função [**SnmpListen**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmplisten) e passar o valor snmpapi no \_ parâmetro *lStatus* , ocorrerão as seguintes ações:

1.  A entidade que estará funcionando em uma função de agente SNMP será vinculada à sua porta atribuída e "escuta" para solicitações de mensagens SNMP de entrada.
2.  O agente usa a lógica específica do aplicativo para processar cada solicitação SNMP.
3.  O agente forma as respostas apropriadas a cada solicitação.
4.  O agente transmite a resposta para a entidade solicitante chamando a função [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) . Quando o agente chama **SnmpSendMsg**, ele especifica o endereço do agente no parâmetro *srcEntity* e o endereço da entidade Gerenciador remoto no parâmetro *dstEntity* . (Esses valores são o inverso dos valores que a entidade de agente recebeu nesses parâmetros quando ele chamou a função [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) para recuperar uma solicitação de SNMP.)

Para obter mais informações sobre aplicativos de gerenciamento SNMP e aplicativos de agente, consulte [sobre SNMP](about-snmp.md).

 

 




