---
title: Tarefas de programação winSNMP
description: A tabela a seguir resume os procedimentos básicos de programação que você deve executar para codificar um aplicativo WinSNMP e os tópicos que fornecem informações sobre essas tarefas.
ms.assetid: 70c24042-bf44-4484-8e5e-d117e2ba28d5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bb83d6d61311866ddb84d3980f5742f82f51405
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479392"
---
# <a name="winsnmp-programming-tasks"></a>Tarefas de programação winSNMP

A tabela a seguir resume os procedimentos básicos de programação que você deve executar para codificar um aplicativo WinSNMP e os tópicos que fornecem informações sobre essas tarefas.




| Tarefa de programação | Tópicos e funções relacionadas a tarefas | 
|------------------|----------------------------------|
| Abra o aplicativo WinSNMP. | Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup"><strong>SnmpStartup</strong></a>. Consulte <a href="opening-and-closing-a-winsnmp-application.md">Abrindo e fechando um aplicativo WinSNMP.</a><br /> | 
| Abra uma ou mais sessões WinSNMP. | Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession"><strong>SnmpCreateSession</strong></a>. Consulte <a href="opening-and-closing-a-winsnmp-session.md">Abrindo e fechando uma sessão WinSNMP.</a><br /> | 
| Registre-se para receber interceptações ou notificações. | Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister"><strong>SnmpRegister</strong></a>. Consulte <a href="managing-traps-and-notifications.md">Gerenciando interceptações e notificações.</a><br /> | 
| Crie uma ou mais listas de associação de variáveis para incorporação em uma PDU. | Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl"><strong>SnmpCreateVbl,</strong></a> <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl"><strong>SnmpDuplicateVbl,</strong></a> <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetvb"><strong>SnmpSetVb</strong></a>. Consulte <a href="working-with-variable-binding-lists.md">Trabalhando com listas de associação de variáveis</a>.<br /><blockquote>[!Note]<br />O aplicativo pode precisar chamar outras funções <a href="winsnmp-functions.md">de associação de variável</a> para criar a lista de associação de variáveis.</blockquote><br /> | 
| Crie uma ou mais PDUs para transmissão e processamento. | Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu"><strong>SnmpCreatePDU,</strong></a> <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata"><strong>SnmpSetPduData,</strong></a> <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatepdu"><strong>SnmpDuplicatePDU.</strong></a> Consulte <a href="working-with-protocol-data-units.md">Trabalhando com unidades de dados de protocolo</a>.<br /><blockquote>[!Note]<br />O aplicativo pode precisar chamar outras <a href="winsnmp-functions.md">funções PDU</a> e funções de utilitário WinSNMP <a href="winsnmp-functions.md"></a> para criar a PDU.</blockquote><br /> | 
| Envie uma ou mais solicitações de operação SNMP. | Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg"><strong>SnmpSendMsg</strong></a>. Consulte <a href="sending-snmp-messages.md">Enviando mensagens SNMP.</a><br /> | 
| Recupere a resposta à solicitação de operação SNMP. | Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg"><strong>SnmpRecvMsg.</strong></a> Consulte <a href="receiving-snmp-messages.md">Recebendo mensagens SNMP.</a><br /> | 
| Processe a resposta da solicitação. | Use a lógica específica do aplicativo. | 
| Feche cada sessão winSNMP. | Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose"><strong>SnmpClose.</strong></a> Consulte <a href="opening-and-closing-a-winsnmp-session.md">Abrindo e fechando uma sessão WinSNMP.</a><br /> | 
| Feche o aplicativo WinSNMP. | Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup"><strong>SnmpCleanup</strong></a>. Consulte <a href="opening-and-closing-a-winsnmp-application.md">Abrindo e fechando um aplicativo WinSNMP.</a><br /> | 




 

Os tópicos a seguir contêm informações adicionais sobre outros conceitos gerais de programação específicos para o ambiente WinSNMP.



| Tópico                                                              | Conceitos                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Tarefas gerais de programação](general-winsnmp-programming-tasks.md) | [Gerenciando identificadores de objeto](managing-object-identifiers.md)[liberando descritores WinSNMP](freeing-winsnmp-descriptors.md)<br/> [Definindo o modo de conversão de entidade e contexto](setting-the-entity-and-context-translation-mode.md)<br/> [Gerenciando a política de retransmissão](managing-the-retransmission-policy.md)<br/> [Escrevendo aplicativos WinSNMP com vários threads](writing-winsnmp-applications-with-multiple-threads.md)<br/> [Registrando um aplicativo de agente SNMP](registering-an-snmp-agent-application.md)<br/> |



 

Além disso, o aplicativo WinSNMP pode precisar incorporar chamadas para as seguintes funções WinSNMP: [**SnmpFreeVbl,**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl) [**SnmpFreeEntity,**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity) [**SnmpFreeDescriptor,**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) [**SnmpFreeContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext)e [**SnmpFreePdu.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu) Isso permite que a implementação do Microsoft WinSNMP liberar objetos de memória WinSNMP. Como regra geral, o aplicativo WinSNMP deve liberar todos os recursos alocados como resultado de uma chamada para uma função WinSNMP. Para obter informações adicionais sobre a desalocação de recursos, consulte [Alocando objetos de memória WinSNMP.](allocating-winsnmp-memory-objects.md)

 

 





