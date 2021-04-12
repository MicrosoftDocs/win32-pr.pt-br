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
# <a name="processing-groups-and-callbacks"></a>Grupos de processamento e retornos de chamada

A tabela a seguir resume uma série de etapas em uma interação operacional entre um protocolo de roteamento e o Gerenciador do grupo de multicast. A primeira coluna descreve as ações que o protocolo de roteamento executa e as respostas do protocolo de roteamento para o Gerenciador do grupo de multicast. A segunda coluna descreve as respostas do Gerenciador do grupo de multicast para o protocolo de roteamento e quaisquer ações que o Gerenciador de grupo de multicast executa, como retornos de chamada. A terceira coluna apresenta informações adicionais.

Cada linha da tabela representa uma etapa.

As tarefas listadas nesta tabela não ocorrem em nenhuma ordem específica; em vez disso, eles ocorrem com base no status das associações de grupo multicast. A tabela a seguir mostra um exemplo de ordem.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Ação do protocolo de roteamento</th>
<th>Ação do Gerenciador de grupo multicast</th>
<th>Observações</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Gerencie associações de grupo com base nas informações de protocolo recebidas nessas interfaces que o protocolo possui. O gerenciamento é executado usando as seguintes funções:
<ul>
<li><a href="/windows/desktop/api/Mgm/nf-mgm-mgmaddgroupmembershipentry"><strong>MgmAddGroupMembershipEntry</strong></a></li>
<li><a href="/windows/desktop/api/Mgm/nf-mgm-mgmdeletegroupmembershipentry"><strong>MgmDeleteGroupMembershipEntry</strong></a></li>
</ul></td>
<td>Adicione e exclua da lista de interface de saída para as entradas especificadas (s, g), (*, g) e (*, *). Essa lista representa o conjunto de interfaces em que os dados desse grupo são encaminhados. Os dados deste grupo são da origem especificada.</td>

</tr>
<tr class="even">

<td>Envie alertas para protocolos de roteamento na forma de retornos de chamada. Os eventos a seguir disparam o Gerenciador de grupo multicast para invocar um retorno de chamada:
<ul>
<li>Ingressar ou deixar grupos ( <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback"><strong>PMGM_JOIN_ALERT_CALLBACK</strong></a>, <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback"><strong>PMGM_PRUNE_ALERT_CALLBACK</strong></a>).</li>
<li>Associação de grupo alterada por IGMP ( <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_local_join_callback"><strong>PMGM_LOCAL_JOIN_CALLBACK</strong></a>, <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_local_leave_callback"><strong>PMGM_LOCAL_LEAVE_CALLBACK</strong></a>).</li>
<li>Dados recebidos na interface incorreta ( <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_wrong_if_callback"><strong>PMGM_WRONG_IF_CALLBACK</strong></a>).</li>
<li>Dados recebidos de novas fontes ou para um novo grupo ( <a href="/windows/desktop/api/mgm/nc-mgm-pmgm_creation_alert_callback"><strong>PMGM_CREATION_ALERT_CALLBACK</strong></a> e <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_rpf_callback"><strong>PMGM_RPF_CALLBACK</strong></a>).</li>
</ul></td>
<td>Usando esses retornos de chamada, o Gerenciador de grupos de multicast é capaz de coordenar o encaminhamento de pacotes quando vários protocolos de roteamento multicast estão presentes em um roteador.</td>
</tr>
<tr class="odd">
<td>Enumere as entradas de encaminhamento de multicast (MFEs), usando as funções <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfe"><strong>MgmGetFirstMfe</strong></a>, <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfe"><strong>MgmGetNextMfe</strong></a>e <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetmfe"><strong>MgmGetMfe</strong></a> . Tome decisões sobre dados de multicast com base nos resultados da enumeração.</td>
<td>Retornar o MFEs solicitado. Retornar ERROR_NO_MORE itens quando não houver mais MFEs para retornar.<br/></td>
<td>Use as funções <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfestats"><strong>MgmGetFirstMfeStats</strong></a>, <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfestats"><strong>MgmGetNextMfeStats</strong></a>, <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetmfestats"><strong>MGMGETMFESTATS</strong></a> para enumerar estatísticas MFE. Consulte <a href="administrative-application-scenario.md">cenário de aplicativo administrativo</a> para obter um exemplo completo de como usar essas funções.<br/></td>
</tr>
<tr class="even">
<td>Modifique o vizinho upstream em um MFE usando a função <a href="/windows/desktop/api/Mgm/nf-mgm-mgmsetmfe"><strong>MgmSetMfe</strong></a> .</td>

<td>Os clientes usam essa função para modificar as informações relacionadas à interface de entrada.</td>
</tr>
</tbody>
</table>



 

 

