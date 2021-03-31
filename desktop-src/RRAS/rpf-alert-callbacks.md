---
title: Retornos de chamada de alerta do RPF
description: Depois que o Gerenciador de grupo de multicast recebe uma notificação de um pacote de uma nova fonte ou de um pacote destinado a um novo grupo, o Gerenciador de grupo de multicast pesquisa a rota para a origem na exibição de multicast da tabela de roteamento.
ms.assetid: dacccca2-e6a5-417a-a217-06ff846d55f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7832a25f8b44821f4b46a69943b4bba3519207c1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103637290"
---
# <a name="rpf-alert-callbacks"></a><span data-ttu-id="4e2bd-103">Retornos de chamada de alerta do RPF</span><span class="sxs-lookup"><span data-stu-id="4e2bd-103">RPF Alert Callbacks</span></span>

<span data-ttu-id="4e2bd-104">Depois que o Gerenciador de grupo de multicast recebe uma notificação de um pacote de uma nova fonte ou de um pacote destinado a um novo grupo, o Gerenciador de grupo de multicast pesquisa a rota para a origem na exibição de multicast da tabela de roteamento.</span><span class="sxs-lookup"><span data-stu-id="4e2bd-104">After the multicast group manager receives notification of a packet from a new source or of a packet that is destined for a new group, the multicast group manager looks up the route to the source in the multicast view of the routing table.</span></span> <span data-ttu-id="4e2bd-105">Em seguida, o Gerenciador do grupo de multicast invoca o retorno de chamada do [**PMGM \_ RPF \_**](/windows/desktop/api/Mgm/nc-mgm-pmgm_rpf_callback) para o protocolo que possui a interface na qual os dados chegaram.</span><span class="sxs-lookup"><span data-stu-id="4e2bd-105">The multicast group manager then invokes the [**PMGM\_RPF\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_rpf_callback) callback to the protocol that owns the interface the data arrived on.</span></span>

<span data-ttu-id="4e2bd-106">Depois que esse retorno de chamada for invocado, o protocolo de roteamento poderá alterar a interface de entrada se o protocolo de roteamento precisar receber os dados para o grupo em uma interface diferente.</span><span class="sxs-lookup"><span data-stu-id="4e2bd-106">After this callback is invoked, the routing protocol can change the incoming interface if the routing protocol must receive the data for the group on a different interface.</span></span>

 

 




