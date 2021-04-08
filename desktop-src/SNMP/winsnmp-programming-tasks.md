---
title: Tarefas de programação de WinSNMP
description: A tabela a seguir resume os procedimentos básicos de programação que você deve executar para codificar um aplicativo WinSNMP e os tópicos que fornecem informações sobre essas tarefas.
ms.assetid: 70c24042-bf44-4484-8e5e-d117e2ba28d5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d75fa8d2ad223fbd8f71eff78c7cd232ddc492a9
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/11/2020
ms.locfileid: "103823551"
---
# <a name="winsnmp-programming-tasks"></a><span data-ttu-id="c589c-103">Tarefas de programação de WinSNMP</span><span class="sxs-lookup"><span data-stu-id="c589c-103">WinSNMP Programming Tasks</span></span>

<span data-ttu-id="c589c-104">A tabela a seguir resume os procedimentos básicos de programação que você deve executar para codificar um aplicativo WinSNMP e os tópicos que fornecem informações sobre essas tarefas.</span><span class="sxs-lookup"><span data-stu-id="c589c-104">The following table summarizes the basic programming procedures that you must perform to code a WinSNMP application, and the topics that provide information about these tasks.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c589c-105">Tarefa de programação</span><span class="sxs-lookup"><span data-stu-id="c589c-105">Programming task</span></span></th>
<th><span data-ttu-id="c589c-106">Funções e tópicos relacionados a tarefas</span><span class="sxs-lookup"><span data-stu-id="c589c-106">Task-related function and topics</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c589c-107">Abra o aplicativo WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="c589c-107">Open the WinSNMP application.</span></span></td>
<td><span data-ttu-id="c589c-108">Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup"><strong>SnmpStartup</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c589c-108">Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup"><strong>SnmpStartup</strong></a>.</span></span> <span data-ttu-id="c589c-109">Consulte <a href="opening-and-closing-a-winsnmp-application.md">abrindo e fechando um aplicativo WinSNMP</a>.</span><span class="sxs-lookup"><span data-stu-id="c589c-109">See <a href="opening-and-closing-a-winsnmp-application.md">Opening and Closing a WinSNMP Application</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c589c-110">Abra uma ou mais sessões de WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="c589c-110">Open one or more WinSNMP sessions.</span></span></td>
<td><span data-ttu-id="c589c-111">Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession"><strong>SnmpCreateSession</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c589c-111">Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession"><strong>SnmpCreateSession</strong></a>.</span></span> <span data-ttu-id="c589c-112">Consulte <a href="opening-and-closing-a-winsnmp-session.md">abrindo e fechando uma sessão WinSNMP</a>.</span><span class="sxs-lookup"><span data-stu-id="c589c-112">See <a href="opening-and-closing-a-winsnmp-session.md">Opening and Closing a WinSNMP Session</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c589c-113">Registre-se para receber Interceptações ou notificações.</span><span class="sxs-lookup"><span data-stu-id="c589c-113">Register to receive traps or notifications.</span></span></td>
<td><span data-ttu-id="c589c-114">Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister"><strong>SnmpRegister</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c589c-114">Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister"><strong>SnmpRegister</strong></a>.</span></span> <span data-ttu-id="c589c-115">Consulte <a href="managing-traps-and-notifications.md">Gerenciando interceptações e notificações</a>.</span><span class="sxs-lookup"><span data-stu-id="c589c-115">See <a href="managing-traps-and-notifications.md">Managing Traps and Notifications</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c589c-116">Crie uma ou mais listas de associação de variáveis para a Incorporation em uma PDU.</span><span class="sxs-lookup"><span data-stu-id="c589c-116">Create one or more variable binding lists for incorporation in a PDU.</span></span></td>
<td><span data-ttu-id="c589c-117">Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl"><strong>SnmpCreateVbl</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl"><strong>SnmpDuplicateVbl</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetvb"><strong>SnmpSetVb</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c589c-117">Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl"><strong>SnmpCreateVbl</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl"><strong>SnmpDuplicateVbl</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetvb"><strong>SnmpSetVb</strong></a>.</span></span> <span data-ttu-id="c589c-118">Consulte <a href="working-with-variable-binding-lists.md">trabalhando com listas de associação de variáveis</a>.</span><span class="sxs-lookup"><span data-stu-id="c589c-118">See <a href="working-with-variable-binding-lists.md">Working with Variable Binding Lists</a>.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="c589c-119">O aplicativo pode precisar chamar outras <a href="winsnmp-functions.md">funções de associação de variáveis</a> para criar a lista de associação de variáveis.</span><span class="sxs-lookup"><span data-stu-id="c589c-119">The application may need to call other <a href="winsnmp-functions.md">variable binding functions</a> to create the variable binding list.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c589c-120">Crie um ou mais PDUs para transmissão e processamento.</span><span class="sxs-lookup"><span data-stu-id="c589c-120">Create one or more PDUs for transmission and processing.</span></span></td>
<td><span data-ttu-id="c589c-121">Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu"><strong>SnmpCreatePDU</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata"><strong>SnmpSetPduData</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatepdu"><strong>SnmpDuplicatePDU</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c589c-121">Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu"><strong>SnmpCreatePDU</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata"><strong>SnmpSetPduData</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatepdu"><strong>SnmpDuplicatePDU</strong></a>.</span></span> <span data-ttu-id="c589c-122">Consulte <a href="working-with-protocol-data-units.md">trabalhando com unidades de dados de protocolo</a>.</span><span class="sxs-lookup"><span data-stu-id="c589c-122">See <a href="working-with-protocol-data-units.md">Working with Protocol Data Units</a>.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="c589c-123">O aplicativo pode precisar chamar outras <a href="winsnmp-functions.md">funções de PDU</a> e <a href="winsnmp-functions.md">funções de utilitário</a> WINSNMP para criar a PDU.</span><span class="sxs-lookup"><span data-stu-id="c589c-123">The application may need to call other <a href="winsnmp-functions.md">PDU functions</a> and WinSNMP <a href="winsnmp-functions.md">utility functions</a> to create the PDU.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c589c-124">Envie uma ou mais solicitações de operação SNMP.</span><span class="sxs-lookup"><span data-stu-id="c589c-124">Submit one or more SNMP operation requests.</span></span></td>
<td><span data-ttu-id="c589c-125">Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg"><strong>SnmpSendMsg</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c589c-125">Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg"><strong>SnmpSendMsg</strong></a>.</span></span> <span data-ttu-id="c589c-126">Consulte <a href="sending-snmp-messages.md">enviando mensagens SNMP</a>.</span><span class="sxs-lookup"><span data-stu-id="c589c-126">See <a href="sending-snmp-messages.md">Sending SNMP Messages</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c589c-127">Recupere a resposta para a solicitação de operação SNMP.</span><span class="sxs-lookup"><span data-stu-id="c589c-127">Retrieve the response to the SNMP operation request.</span></span></td>
<td><span data-ttu-id="c589c-128">Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg"><strong>SnmpRecvMsg</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c589c-128">Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg"><strong>SnmpRecvMsg</strong></a>.</span></span> <span data-ttu-id="c589c-129">Consulte <a href="receiving-snmp-messages.md">recebendo mensagens SNMP</a>.</span><span class="sxs-lookup"><span data-stu-id="c589c-129">See <a href="receiving-snmp-messages.md">Receiving SNMP Messages</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c589c-130">Processar a resposta da solicitação.</span><span class="sxs-lookup"><span data-stu-id="c589c-130">Process the request response.</span></span></td>
<td><span data-ttu-id="c589c-131">Use a lógica específica do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c589c-131">Use application-specific logic.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c589c-132">Feche cada sessão de WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="c589c-132">Close each WinSNMP session.</span></span></td>
<td><span data-ttu-id="c589c-133">Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose"><strong>SnmpClose</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c589c-133">Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose"><strong>SnmpClose</strong></a>.</span></span> <span data-ttu-id="c589c-134">Consulte <a href="opening-and-closing-a-winsnmp-session.md">abrindo e fechando uma sessão WinSNMP</a>.</span><span class="sxs-lookup"><span data-stu-id="c589c-134">See <a href="opening-and-closing-a-winsnmp-session.md">Opening and Closing a WinSNMP Session</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c589c-135">Feche o aplicativo WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="c589c-135">Close the WinSNMP application.</span></span></td>
<td><span data-ttu-id="c589c-136">Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup"><strong>SnmpCleanup</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c589c-136">Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup"><strong>SnmpCleanup</strong></a>.</span></span> <span data-ttu-id="c589c-137">Consulte <a href="opening-and-closing-a-winsnmp-application.md">abrindo e fechando um aplicativo WinSNMP</a>.</span><span class="sxs-lookup"><span data-stu-id="c589c-137">See <a href="opening-and-closing-a-winsnmp-application.md">Opening and Closing a WinSNMP Application</a>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="c589c-138">Os tópicos a seguir contêm informações adicionais sobre outros conceitos gerais de programação específicos ao ambiente WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="c589c-138">The following topics contain additional information about other general programming concepts specific to the WinSNMP environment.</span></span>



|                                                                    |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c589c-139">Tarefas gerais de programação</span><span class="sxs-lookup"><span data-stu-id="c589c-139">General programming tasks</span></span>](general-winsnmp-programming-tasks.md) | <span data-ttu-id="c589c-140">[Gerenciando identificadores de objeto](managing-object-identifiers.md)que[liberam descritores de WinSNMP](freeing-winsnmp-descriptors.md)</span><span class="sxs-lookup"><span data-stu-id="c589c-140">[Managing Object Identifiers](managing-object-identifiers.md)[Freeing WinSNMP Descriptors](freeing-winsnmp-descriptors.md)</span></span><br/> [<span data-ttu-id="c589c-141">Definindo a entidade e o modo de tradução de contexto</span><span class="sxs-lookup"><span data-stu-id="c589c-141">Setting the Entity and Context Translation Mode</span></span>](setting-the-entity-and-context-translation-mode.md)<br/> [<span data-ttu-id="c589c-142">Gerenciando a política de retransmissão</span><span class="sxs-lookup"><span data-stu-id="c589c-142">Managing the Retransmission Policy</span></span>](managing-the-retransmission-policy.md)<br/> [<span data-ttu-id="c589c-143">Escrevendo aplicativos WinSNMP com vários threads</span><span class="sxs-lookup"><span data-stu-id="c589c-143">Writing WinSNMP Applications with Multiple Threads</span></span>](writing-winsnmp-applications-with-multiple-threads.md)<br/> [<span data-ttu-id="c589c-144">Registrando um aplicativo de agente SNMP</span><span class="sxs-lookup"><span data-stu-id="c589c-144">Registering an SNMP Agent Application</span></span>](registering-an-snmp-agent-application.md)<br/> |



 

<span data-ttu-id="c589c-145">Além disso, o aplicativo WinSNMP pode precisar incorporar chamadas para as seguintes funções de WinSNMP: [**SnmpFreeVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl), [**SnmpFreeEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity), [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor), [**SnmpFreeContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext)e [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu).</span><span class="sxs-lookup"><span data-stu-id="c589c-145">In addition, the WinSNMP application may need to incorporate calls to the following WinSNMP functions: [**SnmpFreeVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl), [**SnmpFreeEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity), [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor), [**SnmpFreeContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext), and [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu).</span></span> <span data-ttu-id="c589c-146">Isso permite que a implementação do Microsoft WinSNMP libere objetos de memória de WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="c589c-146">This enables the Microsoft WinSNMP implementation to free WinSNMP memory objects.</span></span> <span data-ttu-id="c589c-147">Como regra geral, o aplicativo WinSNMP deve liberar todos os recursos alocados como resultado de uma chamada para uma função WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="c589c-147">As a general rule, the WinSNMP application should free all resources allocated as the result of a call to a WinSNMP function.</span></span> <span data-ttu-id="c589c-148">Para obter informações adicionais sobre como desalocar recursos, consulte [alocando objetos de memória WinSNMP](allocating-winsnmp-memory-objects.md).</span><span class="sxs-lookup"><span data-stu-id="c589c-148">For additional information about deallocating resources, see [Allocating WinSNMP Memory Objects](allocating-winsnmp-memory-objects.md).</span></span>

 

 





