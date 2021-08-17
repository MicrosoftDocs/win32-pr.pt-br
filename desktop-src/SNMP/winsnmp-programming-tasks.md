---
title: Tarefas de programação de WinSNMP
description: A tabela a seguir resume os procedimentos básicos de programação que você deve executar para codificar um aplicativo WinSNMP e os tópicos que fornecem informações sobre essas tarefas.
ms.assetid: 70c24042-bf44-4484-8e5e-d117e2ba28d5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 007ed1a50688ceff7cdd3bfd9916c1726773cf5ecb2e175af99880950c5c3db8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142789"
---
# <a name="winsnmp-programming-tasks"></a>Tarefas de programação de WinSNMP

A tabela a seguir resume os procedimentos básicos de programação que você deve executar para codificar um aplicativo WinSNMP e os tópicos que fornecem informações sobre essas tarefas.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tarefa de programação</th>
<th>Funções e tópicos relacionados a tarefas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Abra o aplicativo WinSNMP.</td>
<td>Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup"><strong>SnmpStartup</strong></a>. Consulte <a href="opening-and-closing-a-winsnmp-application.md">abrindo e fechando um aplicativo WinSNMP</a>.<br/></td>
</tr>
<tr class="even">
<td>Abra uma ou mais sessões de WinSNMP.</td>
<td>Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession"><strong>SnmpCreateSession</strong></a>. Consulte <a href="opening-and-closing-a-winsnmp-session.md">abrindo e fechando uma sessão WinSNMP</a>.<br/></td>
</tr>
<tr class="odd">
<td>Registre-se para receber Interceptações ou notificações.</td>
<td>Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister"><strong>SnmpRegister</strong></a>. Consulte <a href="managing-traps-and-notifications.md">Gerenciando interceptações e notificações</a>.<br/></td>
</tr>
<tr class="even">
<td>Crie uma ou mais listas de associação de variáveis para a Incorporation em uma PDU.</td>
<td>Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl"><strong>SnmpCreateVbl</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl"><strong>SnmpDuplicateVbl</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetvb"><strong>SnmpSetVb</strong></a>. Consulte <a href="working-with-variable-binding-lists.md">trabalhando com listas de associação de variáveis</a>.<br/>
<blockquote>
[!Note]<br />
O aplicativo pode precisar chamar outras <a href="winsnmp-functions.md">funções de associação de variáveis</a> para criar a lista de associação de variáveis.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>Crie um ou mais PDUs para transmissão e processamento.</td>
<td>Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu"><strong>SnmpCreatePDU</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata"><strong>SnmpSetPduData</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatepdu"><strong>SnmpDuplicatePDU</strong></a>. Consulte <a href="working-with-protocol-data-units.md">trabalhando com unidades de dados de protocolo</a>.<br/>
<blockquote>
[!Note]<br />
O aplicativo pode precisar chamar outras <a href="winsnmp-functions.md">funções de PDU</a> e <a href="winsnmp-functions.md">funções de utilitário</a> WINSNMP para criar a PDU.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Envie uma ou mais solicitações de operação SNMP.</td>
<td>Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg"><strong>SnmpSendMsg</strong></a>. Consulte <a href="sending-snmp-messages.md">enviando mensagens SNMP</a>.<br/></td>
</tr>
<tr class="odd">
<td>Recupere a resposta para a solicitação de operação SNMP.</td>
<td>Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg"><strong>SnmpRecvMsg</strong></a>. Consulte <a href="receiving-snmp-messages.md">recebendo mensagens SNMP</a>.<br/></td>
</tr>
<tr class="even">
<td>Processar a resposta da solicitação.</td>
<td>Use a lógica específica do aplicativo.</td>
</tr>
<tr class="odd">
<td>Feche cada sessão de WinSNMP.</td>
<td>Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose"><strong>SnmpClose</strong></a>. Consulte <a href="opening-and-closing-a-winsnmp-session.md">abrindo e fechando uma sessão WinSNMP</a>.<br/></td>
</tr>
<tr class="even">
<td>Feche o aplicativo WinSNMP.</td>
<td>Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup"><strong>SnmpCleanup</strong></a>. Consulte <a href="opening-and-closing-a-winsnmp-application.md">abrindo e fechando um aplicativo WinSNMP</a>.<br/></td>
</tr>
</tbody>
</table>



 

Os tópicos a seguir contêm informações adicionais sobre outros conceitos gerais de programação específicos ao ambiente WinSNMP.



| Tópico                                                              | Conceitos                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Tarefas gerais de programação](general-winsnmp-programming-tasks.md) | [Gerenciando identificadores de objeto](managing-object-identifiers.md)que[liberam descritores de WinSNMP](freeing-winsnmp-descriptors.md)<br/> [Definindo a entidade e o modo de tradução de contexto](setting-the-entity-and-context-translation-mode.md)<br/> [Gerenciando a política de retransmissão](managing-the-retransmission-policy.md)<br/> [Escrevendo aplicativos WinSNMP com vários threads](writing-winsnmp-applications-with-multiple-threads.md)<br/> [Registrando um aplicativo de agente SNMP](registering-an-snmp-agent-application.md)<br/> |



 

Além disso, o aplicativo WinSNMP pode precisar incorporar chamadas para as seguintes funções de WinSNMP: [**SnmpFreeVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl), [**SnmpFreeEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity), [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor), [**SnmpFreeContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext)e [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu). Isso permite que a implementação do Microsoft WinSNMP libere objetos de memória de WinSNMP. Como regra geral, o aplicativo WinSNMP deve liberar todos os recursos alocados como resultado de uma chamada para uma função WinSNMP. Para obter informações adicionais sobre como desalocar recursos, consulte [alocando objetos de memória WinSNMP](allocating-winsnmp-memory-objects.md).

 

 





