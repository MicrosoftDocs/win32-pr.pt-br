---
title: Retornos de chamada de junção local
description: Depois que o Gerenciador do grupo de multicast é notificado pelo IGMP que novos receptores estão presentes para um grupo em uma interface, o Gerenciador do grupo de multicast invoca o retorno de chamada de \_ retorno de chamadas de junção local PMGM \_ \_ para o protocolo de roteamento que possui a interface, se houver.
ms.assetid: 136f86e0-380d-4158-a9dd-c6de1c7f6689
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c97f0e16e08bc3781b946a51f69d2b0d65b3272
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453673"
---
# <a name="local-join-callbacks"></a><span data-ttu-id="cb8e2-103">Retornos de chamada de junção local</span><span class="sxs-lookup"><span data-stu-id="cb8e2-103">Local Join Callbacks</span></span>

<span data-ttu-id="cb8e2-104">Depois que o Gerenciador do grupo de multicast é notificado pelo IGMP que novos receptores estão presentes para um grupo em uma interface, o Gerenciador do grupo de multicast invoca o retorno de chamada de [**\_ retorno de \_ \_ chamadas de junção local PMGM**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_join_callback) para o protocolo de roteamento que possui a interface, se houver.</span><span class="sxs-lookup"><span data-stu-id="cb8e2-104">After the multicast group manager is notified by IGMP that new receivers are present for a group on an interface, the multicast group manager invokes the [**PMGM\_LOCAL\_JOIN\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_join_callback) callback to the routing protocol that owns the interface if one exists.</span></span> <span data-ttu-id="cb8e2-105">Esse retorno de chamada notifica o protocolo de roteamento da alteração.</span><span class="sxs-lookup"><span data-stu-id="cb8e2-105">This callback notifies the routing protocol of the change.</span></span>

<span data-ttu-id="cb8e2-106">Esse retorno de chamada e o retorno de chamada de [**PMGM \_ local \_ deixam \_**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_leave_callback) são usados para sincronizar o encaminhamento entre os protocolos IGMP e de roteamento.</span><span class="sxs-lookup"><span data-stu-id="cb8e2-106">This callback and the [**PMGM\_LOCAL\_LEAVE\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_leave_callback) callback are used to synchronize forwarding between IGMP and routing protocols.</span></span>

 

 




