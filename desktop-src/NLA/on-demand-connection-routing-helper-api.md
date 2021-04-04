---
title: Referência da API do auxiliar de roteamento de conexão sob demanda
description: Os tópicos a seguir fornecem detalhes para o auxiliar de roteamento de conexão sob demanda.
ms.assetid: 39AFFD16-488E-4CA3-9161-9424F0D15948
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3049c62d7784af6430e8b93240ec79464b098043
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104084125"
---
# <a name="on-demand-connection-routing-helper-api-reference"></a><span data-ttu-id="7916a-103">Referência da API do auxiliar de roteamento de conexão sob demanda</span><span class="sxs-lookup"><span data-stu-id="7916a-103">On Demand Connection Routing Helper API reference</span></span>

<span data-ttu-id="7916a-104">Os tópicos a seguir fornecem detalhes para o auxiliar de roteamento de conexão sob demanda.</span><span class="sxs-lookup"><span data-stu-id="7916a-104">The following topics provide details for the On Demand Connection Routing Helper.</span></span>



| <span data-ttu-id="7916a-105">Referência</span><span class="sxs-lookup"><span data-stu-id="7916a-105">Reference</span></span>                                                                          | <span data-ttu-id="7916a-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="7916a-106">Description</span></span>                                                                                                                                                                 |
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7916a-107">**OnDemandGetRoutingHint**</span><span class="sxs-lookup"><span data-stu-id="7916a-107">**OnDemandGetRoutingHint**</span></span>](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-ondemandgetroutinghint)                           | <span data-ttu-id="7916a-108">Pesquisar um destino no cache de solicitação de rota e, se uma correspondência for encontrada, retorna a ID de interface correspondente.</span><span class="sxs-lookup"><span data-stu-id="7916a-108">Look up a destination in the Route Request cache and, if a match is found, returns the corresponding Interface ID.</span></span><br/>                                               |
| [<span data-ttu-id="7916a-109">**OnDemandRegisterNotification**</span><span class="sxs-lookup"><span data-stu-id="7916a-109">**OnDemandRegisterNotification**</span></span>](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-ondemandregisternotification)               | <span data-ttu-id="7916a-110">Registre-se para ser notificado quando o cache de solicitações de rota for modificado.</span><span class="sxs-lookup"><span data-stu-id="7916a-110">Register to be notified when the Route Requests cache is modified.</span></span><br/>                                                                                               |
| [<span data-ttu-id="7916a-111">**OnDemandUnregisterNotification**</span><span class="sxs-lookup"><span data-stu-id="7916a-111">**OnDemandUnregisterNotification**</span></span>](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-ondemandunregisternotification)           | <span data-ttu-id="7916a-112">Cancelar o registro para notificações e limpar recursos.</span><span class="sxs-lookup"><span data-stu-id="7916a-112">Unregister for notifications and clean up resources.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="7916a-113">**\_contexto de interface de rede \_**</span><span class="sxs-lookup"><span data-stu-id="7916a-113">**NET\_INTERFACE\_CONTEXT**</span></span>](/windows/desktop/api/OnDemandConnRouteHelper/ns-ondemandconnroutehelper-net_interface_context)                           | <span data-ttu-id="7916a-114">O contexto de interface que faz parte da estrutura da [**tabela de contexto da interface de rede \_ \_ \_**](/windows/desktop/api/OnDemandConnRouteHelper/ns-ondemandconnroutehelper-net_interface_context_table) .</span><span class="sxs-lookup"><span data-stu-id="7916a-114">The interface context that is part of the [**NET\_INTERFACE\_CONTEXT\_TABLE**](/windows/desktop/api/OnDemandConnRouteHelper/ns-ondemandconnroutehelper-net_interface_context_table) structure.</span></span><br/>                                       |
| [<span data-ttu-id="7916a-115">**\_tabela de \_ contexto de interface de rede \_**</span><span class="sxs-lookup"><span data-stu-id="7916a-115">**NET\_INTERFACE\_CONTEXT\_TABLE**</span></span>](/windows/desktop/api/OnDemandConnRouteHelper/ns-ondemandconnroutehelper-net_interface_context_table)              | <span data-ttu-id="7916a-116">A tabela de estruturas de [**\_ \_ contexto de interface de rede**](/windows/desktop/api/OnDemandConnRouteHelper/ns-ondemandconnroutehelper-net_interface_context) .</span><span class="sxs-lookup"><span data-stu-id="7916a-116">The table of [**NET\_INTERFACE\_CONTEXT**](/windows/desktop/api/OnDemandConnRouteHelper/ns-ondemandconnroutehelper-net_interface_context) structures.</span></span><br/>                                                                                |
| [<span data-ttu-id="7916a-117">**GetInterfaceContextTableForHostName**</span><span class="sxs-lookup"><span data-stu-id="7916a-117">**GetInterfaceContextTableForHostName**</span></span>](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-getinterfacecontexttableforhostname) | <span data-ttu-id="7916a-118">Essa função recupera uma tabela de contexto de interface para o nome de host e o filtro de perfil de conexão fornecidos.</span><span class="sxs-lookup"><span data-stu-id="7916a-118">This function retrieves an interface context table for the given hostname and connection profile filter.</span></span><br/>                                                         |
| [<span data-ttu-id="7916a-119">**FreeInterfaceContextTable**</span><span class="sxs-lookup"><span data-stu-id="7916a-119">**FreeInterfaceContextTable**</span></span>](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-freeinterfacecontexttable)                     | <span data-ttu-id="7916a-120">Essa função libera a tabela de contexto da interface recuperada usando a função [**GetInterfaceContextTableForHostName**](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-getinterfacecontexttableforhostname) .</span><span class="sxs-lookup"><span data-stu-id="7916a-120">This function frees the interface context table retrieved using the [**GetInterfaceContextTableForHostName**](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-getinterfacecontexttableforhostname) function.</span></span><br/> |



 

 

 





