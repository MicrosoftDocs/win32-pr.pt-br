---
title: Tarefas de programação winSNMP
description: A tabela a seguir resume os procedimentos básicos de programação que você deve executar para codificar um aplicativo WinSNMP e os tópicos que fornecem informações sobre essas tarefas.
ms.assetid: 70c24042-bf44-4484-8e5e-d117e2ba28d5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7543a0fef8fff3f2ef1672ee29d72b0f82b75af7
ms.sourcegitcommit: 5a78723ad484955ac91a23cf282cf9c176c1eab6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/22/2021
ms.locfileid: "114436612"
---
# <a name="winsnmp-programming-tasks"></a>Tarefas de programação winSNMP

A tabela a seguir resume os procedimentos básicos de programação que você deve executar para codificar um aplicativo WinSNMP e os tópicos que fornecem informações sobre essas tarefas.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tarefa de programação</th>
<th>Tópicos e funções relacionadas a tarefas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Abra o aplicativo WinSNMP.</td>
<td>Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup"><strong>SnmpStartup</strong></a>. Consulte <a href="opening-and-closing-a-winsnmp-application.md">Abrindo e fechando um aplicativo WinSNMP.</a><br/></td>
</tr>
<tr class="even">
<td>Abra uma ou mais sessões WinSNMP.</td>
<td>Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession"><strong>SnmpCreateSession</strong></a>. Consulte <a href="opening-and-closing-a-winsnmp-session.md">Abrindo e fechando uma sessão WinSNMP.</a><br/></td>
</tr>
<tr class="odd">
<td>Registre-se para receber interceptações ou notificações.</td>
<td>Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister"><strong>SnmpRegister</strong></a>. Consulte <a href="managing-traps-and-notifications.md">Gerenciando interceptações e notificações.</a><br/></td>
</tr>
<tr class="even">
<td>Crie uma ou mais listas de associação de variáveis para incorporação em uma PDU.</td>
<td>Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl"><strong>SnmpCreateVbl,</strong></a> <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl"><strong>SnmpDuplicateVbl,</strong></a> <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetvb"><strong>SnmpSetVb</strong></a>. Consulte <a href="working-with-variable-binding-lists.md">Trabalhando com listas de associação de variáveis</a>.<br/>
<blockquote>
[!Note]<br />
O aplicativo pode precisar chamar outras funções <a href="winsnmp-functions.md">de associação de variável</a> para criar a lista de associação de variáveis.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>Crie uma ou mais PDUs para transmissão e processamento.</td>
<td>Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu"><strong>SnmpCreatePDU,</strong></a> <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata"><strong>SnmpSetPduData,</strong></a> <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatepdu"><strong>SnmpDuplicatePDU.</strong></a> Consulte <a href="working-with-protocol-data-units.md">Trabalhando com unidades de dados de protocolo</a>.<br/>
<blockquote>
[!Note]<br />
O aplicativo pode precisar chamar outras <a href="winsnmp-functions.md">funções PDU</a> e funções de utilitário WinSNMP <a href="winsnmp-functions.md"></a> para criar a PDU.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Envie uma ou mais solicitações de operação SNMP.</td>
<td>Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg"><strong>SnmpSendMsg</strong></a>. Consulte <a href="sending-snmp-messages.md">Enviando mensagens SNMP.</a><br/></td>
</tr>
<tr class="odd">
<td>Recupere a resposta à solicitação de operação SNMP.</td>
<td>Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg"><strong>SnmpRecvMsg.</strong></a> Consulte <a href="receiving-snmp-messages.md">Recebendo mensagens SNMP.</a><br/></td>
</tr>
<tr class="even">
<td>Processe a resposta da solicitação.</td>
<td>Use a lógica específica do aplicativo.</td>
</tr>
<tr class="odd">
<td>Feche cada sessão winSNMP.</td>
<td>Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose"><strong>SnmpClose.</strong></a> Consulte <a href="opening-and-closing-a-winsnmp-session.md">Abrindo e fechando uma sessão WinSNMP.</a><br/></td>
</tr>
<tr class="even">
<td>Feche o aplicativo WinSNMP.</td>
<td>Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup"><strong>SnmpCleanup</strong></a>. Consulte <a href="opening-and-closing-a-winsnmp-application.md">Abrindo e fechando um aplicativo WinSNMP.</a><br/></td>
</tr>
</tbody>
</table>



 

Os tópicos a seguir contêm informações adicionais sobre outros conceitos gerais de programação específicos para o ambiente WinSNMP.



| Tópico                                                              | Conceitos                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Tarefas gerais de programação](general-winsnmp-programming-tasks.md) | [Gerenciando identificadores de objeto](managing-object-identifiers.md)[liberando descritores WinSNMP](freeing-winsnmp-descriptors.md)<br/> [Definindo o modo de conversão de entidade e contexto](setting-the-entity-and-context-translation-mode.md)<br/> [Gerenciando a política de retransmissão](managing-the-retransmission-policy.md)<br/> [Escrevendo aplicativos WinSNMP com vários threads](writing-winsnmp-applications-with-multiple-threads.md)<br/> [Registrando um aplicativo de agente SNMP](registering-an-snmp-agent-application.md)<br/> |



 

Além disso, o aplicativo WinSNMP pode precisar incorporar chamadas para as seguintes funções WinSNMP: [**SnmpFreeVbl,**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl) [**SnmpFreeEntity,**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity) [**SnmpFreeDescriptor,**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) [**SnmpFreeContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext)e [**SnmpFreePdu.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu) Isso permite que a implementação do Microsoft WinSNMP liberar objetos de memória WinSNMP. Como regra geral, o aplicativo WinSNMP deve liberar todos os recursos alocados como resultado de uma chamada para uma função WinSNMP. Para obter informações adicionais sobre a desalocação de recursos, consulte [Alocando objetos de memória WinSNMP.](allocating-winsnmp-memory-objects.md)

 

 





