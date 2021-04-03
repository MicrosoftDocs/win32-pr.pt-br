---
title: Associar retornos de chamada de alerta
description: Quando o Gerenciador do grupo de multicast é notificado de que há novos receptores presentes para um grupo em uma interface, o Gerenciador do grupo de multicast invoca o retorno de chamada de \_ retorno do alerta de ingresso PMGM \_ \_ .
ms.assetid: b625f8ec-f59b-4151-aa38-48cf8f004966
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c00dc70160b99c3cfc0e41078a3bd5882d930f31
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005734"
---
# <a name="join-alert-callbacks"></a><span data-ttu-id="dc3e3-103">Associar retornos de chamada de alerta</span><span class="sxs-lookup"><span data-stu-id="dc3e3-103">Join Alert Callbacks</span></span>

<span data-ttu-id="dc3e3-104">Quando o Gerenciador do grupo de multicast é notificado de que há novos receptores presentes para um grupo em uma interface, o Gerenciador do grupo de multicast invoca o retorno de chamada de [**\_ retorno do \_ alerta \_ de ingresso PMGM**](/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback) .</span><span class="sxs-lookup"><span data-stu-id="dc3e3-104">When the multicast group manager is notified that there are new receivers present for a group on an interface, the multicast group manager invokes the [**PMGM\_JOIN\_ALERT\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback) callback.</span></span> <span data-ttu-id="dc3e3-105">Esse retorno de chamada notifica os protocolos de roteamento que novos hosts ingressaram nos grupos especificados.</span><span class="sxs-lookup"><span data-stu-id="dc3e3-105">This callback notifies the routing protocols that new hosts have joined the specified groups .</span></span> <span data-ttu-id="dc3e3-106">Portanto, os protocolos de roteamento devem solicitar dados multicast para os grupos especificados pelo retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="dc3e3-106">Therefore, the routing protocols must request multicast data for the groups specified by the callback.</span></span>

<span data-ttu-id="dc3e3-107">O Gerenciador do grupo de multicast usa um conjunto predefinido de regras que são usadas para determinar quando esse retorno de chamada é invocado.</span><span class="sxs-lookup"><span data-stu-id="dc3e3-107">The multicast group manager uses a predefined set of rules that are used to determine when this callback is invoked.</span></span> <span data-ttu-id="dc3e3-108">Esse conjunto de regras se baseia no tipo de solicitação de junção enviado pelo cliente e na ordem em que as solicitações de junção foram recebidas.</span><span class="sxs-lookup"><span data-stu-id="dc3e3-108">This set of rules is based on both the type of join request sent by the client and the order the join requests were received in.</span></span>

## <a name="wildcard-join-requests"></a><span data-ttu-id="dc3e3-109">Solicitações de junção curinga</span><span class="sxs-lookup"><span data-stu-id="dc3e3-109">Wildcard Join Requests</span></span>

<span data-ttu-id="dc3e3-110">Quando uma junção curinga para um grupo ( \* , g) é recebida do primeiro cliente, o Gerenciador do grupo de multicast invoca o retorno de chamada do [**\_ alerta de ingresso \_ \_ PMGM**](/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback) para todos os outros clientes registrados.</span><span class="sxs-lookup"><span data-stu-id="dc3e3-110">When a wildcard join for a group (\*, g) is received from the first client, the multicast group manager invokes the [**PMGM\_JOIN\_ALERT\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback) callback to all other registered clients.</span></span> <span data-ttu-id="dc3e3-111">Quando uma junção curinga para um grupo é recebida do segundo cliente, o Gerenciador do grupo de multicast invoca esse retorno de chamada para o primeiro cliente para ingressar no grupo.</span><span class="sxs-lookup"><span data-stu-id="dc3e3-111">When a wildcard join for a group is received from the second client, the multicast group manager invokes this callback to the first client to join the group.</span></span>

## <a name="source-specific-join-requests"></a><span data-ttu-id="dc3e3-112">Source-Specific solicitações de junção</span><span class="sxs-lookup"><span data-stu-id="dc3e3-112">Source-Specific Join Requests</span></span>

<span data-ttu-id="dc3e3-113">O Gerenciador do grupo de multicast não invoca esse retorno de chamada para todas as junções subsequentes para o grupo.</span><span class="sxs-lookup"><span data-stu-id="dc3e3-113">The multicast group manager does not invoke this callback for any subsequent joins to the group.</span></span>

<span data-ttu-id="dc3e3-114">Quando uma junção específica de origem para um grupo (s, g) é recebida, o Gerenciador do grupo de multicast invoca o retorno de chamada do [**\_ alerta de ingresso \_ \_ PMGM**](/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback) somente para o cliente que possui a interface de entrada em direção às s de origem.</span><span class="sxs-lookup"><span data-stu-id="dc3e3-114">When a source-specific join for a group (s, g) is received, the multicast group manager invokes the [**PMGM\_JOIN\_ALERT\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback) callback only for the client that owns the incoming interface towards the source s.</span></span>

 

 




