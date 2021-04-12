---
title: Grupos de processamento e retornos de chamada
description: A tabela a seguir resume uma série de etapas em uma interação operacional entre um protocolo de roteamento e o Gerenciador do grupo de multicast.
ms.assetid: 43c1dc12-70fd-4e02-a7b1-5818e6d7ddc6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2878ec15cfb663353f3dd0bc1dc5aeadbd2e1e7
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/08/2020
ms.locfileid: "104294560"
---
# <a name="processing-groups-and-callbacks"></a><span data-ttu-id="5c894-103">Grupos de processamento e retornos de chamada</span><span class="sxs-lookup"><span data-stu-id="5c894-103">Processing Groups and Callbacks</span></span>

<span data-ttu-id="5c894-104">A tabela a seguir resume uma série de etapas em uma interação operacional entre um protocolo de roteamento e o Gerenciador do grupo de multicast.</span><span class="sxs-lookup"><span data-stu-id="5c894-104">The following table summarizes a series of steps in an operational interaction between a routing protocol and the multicast group manager.</span></span> <span data-ttu-id="5c894-105">A primeira coluna descreve as ações que o protocolo de roteamento executa e as respostas do protocolo de roteamento para o Gerenciador do grupo de multicast.</span><span class="sxs-lookup"><span data-stu-id="5c894-105">The first column describes the actions that the routing protocol performs and the routing protocol's responses to the multicast group manager.</span></span> <span data-ttu-id="5c894-106">A segunda coluna descreve as respostas do Gerenciador do grupo de multicast para o protocolo de roteamento e quaisquer ações que o Gerenciador de grupo de multicast executa, como retornos de chamada.</span><span class="sxs-lookup"><span data-stu-id="5c894-106">The second column describes the multicast group manager's responses to the routing protocol and any actions the multicast group manager performs such as callbacks.</span></span> <span data-ttu-id="5c894-107">A terceira coluna apresenta informações adicionais.</span><span class="sxs-lookup"><span data-stu-id="5c894-107">The third column presents any additional information.</span></span>

<span data-ttu-id="5c894-108">Cada linha da tabela representa uma etapa.</span><span class="sxs-lookup"><span data-stu-id="5c894-108">Each row of the table represents one step.</span></span>

<span data-ttu-id="5c894-109">As tarefas listadas nesta tabela não ocorrem em nenhuma ordem específica; em vez disso, eles ocorrem com base no status das associações de grupo multicast.</span><span class="sxs-lookup"><span data-stu-id="5c894-109">The tasks listed in this table do not occur in any specific order; rather, they occur based on the status of multicast group memberships.</span></span> <span data-ttu-id="5c894-110">A tabela a seguir mostra um exemplo de ordem.</span><span class="sxs-lookup"><span data-stu-id="5c894-110">The table below shows an example order.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5c894-111">Ação do protocolo de roteamento</span><span class="sxs-lookup"><span data-stu-id="5c894-111">Routing protocol action</span></span></th>
<th><span data-ttu-id="5c894-112">Ação do Gerenciador de grupo multicast</span><span class="sxs-lookup"><span data-stu-id="5c894-112">Multicast group manager action</span></span></th>
<th><span data-ttu-id="5c894-113">Observações</span><span class="sxs-lookup"><span data-stu-id="5c894-113">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5c894-114">Gerencie associações de grupo com base nas informações de protocolo recebidas nessas interfaces que o protocolo possui.</span><span class="sxs-lookup"><span data-stu-id="5c894-114">Manage group memberships based on protocol information received on those interfaces that the protocol owns.</span></span> <span data-ttu-id="5c894-115">O gerenciamento é executado usando as seguintes funções:</span><span class="sxs-lookup"><span data-stu-id="5c894-115">Management is performed using the following functions:</span></span>
<ul>
<li><span data-ttu-id="5c894-116"><a href="/windows/desktop/api/Mgm/nf-mgm-mgmaddgroupmembershipentry"><strong>MgmAddGroupMembershipEntry</strong></a></span><span class="sxs-lookup"><span data-stu-id="5c894-116"><a href="/windows/desktop/api/Mgm/nf-mgm-mgmaddgroupmembershipentry"><strong>MgmAddGroupMembershipEntry</strong></a></span></span></li>
<li><span data-ttu-id="5c894-117"><a href="/windows/desktop/api/Mgm/nf-mgm-mgmdeletegroupmembershipentry"><strong>MgmDeleteGroupMembershipEntry</strong></a></span><span class="sxs-lookup"><span data-stu-id="5c894-117"><a href="/windows/desktop/api/Mgm/nf-mgm-mgmdeletegroupmembershipentry"><strong>MgmDeleteGroupMembershipEntry</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="5c894-118">Adicione e exclua da lista de interface de saída para as entradas especificadas (s, g), (*, g) e (*, \*).</span><span class="sxs-lookup"><span data-stu-id="5c894-118">Add to and delete from the outgoing interface list for the specified (s, g), (*, g), and (*, \*) entries.</span></span> <span data-ttu-id="5c894-119">Essa lista representa o conjunto de interfaces em que os dados desse grupo são encaminhados.</span><span class="sxs-lookup"><span data-stu-id="5c894-119">This list represents the set of interfaces on which data for this group is forwarded.</span></span> <span data-ttu-id="5c894-120">Os dados deste grupo são da origem especificada.</span><span class="sxs-lookup"><span data-stu-id="5c894-120">The data for this group is from the specified source.</span></span></td>

</tr>
<tr class="even">

<td><span data-ttu-id="5c894-121">Envie alertas para protocolos de roteamento na forma de retornos de chamada.</span><span class="sxs-lookup"><span data-stu-id="5c894-121">Send alerts to routing protocols in the form of callbacks.</span></span> <span data-ttu-id="5c894-122">Os eventos a seguir disparam o Gerenciador de grupo multicast para invocar um retorno de chamada:</span><span class="sxs-lookup"><span data-stu-id="5c894-122">The following events trigger the multicast group manager to invoke a callback:</span></span>
<ul>
<li><span data-ttu-id="5c894-123">Ingressar ou deixar grupos ( <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback"><strong>PMGM_JOIN_ALERT_CALLBACK</strong></a>, <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback"><strong>PMGM_PRUNE_ALERT_CALLBACK</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="5c894-123">Join or leave groups ( <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback"><strong>PMGM_JOIN_ALERT_CALLBACK</strong></a>, <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback"><strong>PMGM_PRUNE_ALERT_CALLBACK</strong></a>).</span></span></li>
<li><span data-ttu-id="5c894-124">Associação de grupo alterada por IGMP ( <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_local_join_callback"><strong>PMGM_LOCAL_JOIN_CALLBACK</strong></a>, <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_local_leave_callback"><strong>PMGM_LOCAL_LEAVE_CALLBACK</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="5c894-124">Group membership changed by IGMP ( <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_local_join_callback"><strong>PMGM_LOCAL_JOIN_CALLBACK</strong></a>, <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_local_leave_callback"><strong>PMGM_LOCAL_LEAVE_CALLBACK</strong></a>).</span></span></li>
<li><span data-ttu-id="5c894-125">Dados recebidos na interface incorreta ( <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_wrong_if_callback"><strong>PMGM_WRONG_IF_CALLBACK</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="5c894-125">Data received on wrong interface ( <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_wrong_if_callback"><strong>PMGM_WRONG_IF_CALLBACK</strong></a>).</span></span></li>
<li><span data-ttu-id="5c894-126">Dados recebidos de novas fontes ou para um novo grupo ( <a href="/windows/desktop/api/mgm/nc-mgm-pmgm_creation_alert_callback"><strong>PMGM_CREATION_ALERT_CALLBACK</strong></a> e <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_rpf_callback"><strong>PMGM_RPF_CALLBACK</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="5c894-126">Data received from new sources or to a new group ( <a href="/windows/desktop/api/mgm/nc-mgm-pmgm_creation_alert_callback"><strong>PMGM_CREATION_ALERT_CALLBACK</strong></a> and <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_rpf_callback"><strong>PMGM_RPF_CALLBACK</strong></a>).</span></span></li>
</ul></td>
<td><span data-ttu-id="5c894-127">Usando esses retornos de chamada, o Gerenciador de grupos de multicast é capaz de coordenar o encaminhamento de pacotes quando vários protocolos de roteamento multicast estão presentes em um roteador.</span><span class="sxs-lookup"><span data-stu-id="5c894-127">Using these callbacks, the multicast group manager is able to coordinate packet forwarding when several multicast routing protocols are present on a router.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5c894-128">Enumere as entradas de encaminhamento de multicast (MFEs), usando as funções <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfe"><strong>MgmGetFirstMfe</strong></a>, <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfe"><strong>MgmGetNextMfe</strong></a>e <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetmfe"><strong>MgmGetMfe</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="5c894-128">Enumerate the multicast forwarding entries (MFEs), using the <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfe"><strong>MgmGetFirstMfe</strong></a>, <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfe"><strong>MgmGetNextMfe</strong></a>, and <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetmfe"><strong>MgmGetMfe</strong></a> functions.</span></span> <span data-ttu-id="5c894-129">Tome decisões sobre dados de multicast com base nos resultados da enumeração.</span><span class="sxs-lookup"><span data-stu-id="5c894-129">Make decisions about multicast data based on the results of the enumeration.</span></span></td>
<td><span data-ttu-id="5c894-130">Retornar o MFEs solicitado.</span><span class="sxs-lookup"><span data-stu-id="5c894-130">Return the requested MFEs.</span></span> <span data-ttu-id="5c894-131">Retornar ERROR_NO_MORE itens quando não houver mais MFEs para retornar.</span><span class="sxs-lookup"><span data-stu-id="5c894-131">Return ERROR_NO_MORE ITEMS when there are no more MFEs to return.</span></span><br/></td>
<td><span data-ttu-id="5c894-132">Use as funções <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfestats"><strong>MgmGetFirstMfeStats</strong></a>, <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfestats"><strong>MgmGetNextMfeStats</strong></a>, <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetmfestats"><strong>MGMGETMFESTATS</strong></a> para enumerar estatísticas MFE.</span><span class="sxs-lookup"><span data-stu-id="5c894-132">Use the <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfestats"><strong>MgmGetFirstMfeStats</strong></a>, <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfestats"><strong>MgmGetNextMfeStats</strong></a>, <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetmfestats"><strong>MgmGetMfeStats</strong></a> functions to enumerate MFE statistics.</span></span> <span data-ttu-id="5c894-133">Consulte <a href="administrative-application-scenario.md">cenário de aplicativo administrativo</a> para obter um exemplo completo de como usar essas funções.</span><span class="sxs-lookup"><span data-stu-id="5c894-133">See <a href="administrative-application-scenario.md">Administrative Application Scenario</a> for a complete example of using these functions.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5c894-134">Modifique o vizinho upstream em um MFE usando a função <a href="/windows/desktop/api/Mgm/nf-mgm-mgmsetmfe"><strong>MgmSetMfe</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="5c894-134">Modify the upstream neighbor in an MFE using the <a href="/windows/desktop/api/Mgm/nf-mgm-mgmsetmfe"><strong>MgmSetMfe</strong></a> function.</span></span></td>

<td><span data-ttu-id="5c894-135">Os clientes usam essa função para modificar as informações relacionadas à interface de entrada.</span><span class="sxs-lookup"><span data-stu-id="5c894-135">Clients use this function to modify the information regarding the incoming interface.</span></span></td>
</tr>
</tbody>
</table>



 

 

