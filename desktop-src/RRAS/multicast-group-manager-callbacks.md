---
title: Retornos de chamada do Gerenciador de grupos multicast
description: O Gerenciador de grupos de multicast usa os seguintes retornos de chamada para notificar os clientes (normalmente, protocolos de roteamento) de eventos e alterações de estado
ms.assetid: ebabdfaf-8f5f-45be-9f01-f1dbc01a376c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5ba18f874005e23aef6daca6071362362312e8e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823876"
---
# <a name="multicast-group-manager-callbacks"></a><span data-ttu-id="1f438-103">Retornos de chamada do Gerenciador de grupos multicast</span><span class="sxs-lookup"><span data-stu-id="1f438-103">Multicast Group Manager Callbacks</span></span>

<span data-ttu-id="1f438-104">O Gerenciador de grupos de multicast usa os seguintes retornos de chamada para notificar os clientes (normalmente, protocolos de roteamento) de eventos e alterações de Estado:</span><span class="sxs-lookup"><span data-stu-id="1f438-104">The multicast group manager uses the following callbacks to notify clients (typically, routing protocols) of events and state changes:</span></span>

[<span data-ttu-id="1f438-105">**\_retorno de \_ chamada de alerta de criação de PMGM \_**</span><span class="sxs-lookup"><span data-stu-id="1f438-105">**PMGM\_CREATION\_ALERT\_CALLBACK**</span></span>](/windows/win32/api/mgm/nc-mgm-pmgm_creation_alert_callback)

[<span data-ttu-id="1f438-106">**\_retorno de \_ chamada de alerta do PMGM Join \_**</span><span class="sxs-lookup"><span data-stu-id="1f438-106">**PMGM\_JOIN\_ALERT\_CALLBACK**</span></span>](/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback)

[<span data-ttu-id="1f438-107">**retorno de chamada de alerta de remoção de PMGM \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1f438-107">**PMGM\_PRUNE\_ALERT\_CALLBACK**</span></span>](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback)

[<span data-ttu-id="1f438-108">**\_retorno de \_ chamada de junção local PMGM \_**</span><span class="sxs-lookup"><span data-stu-id="1f438-108">**PMGM\_LOCAL\_JOIN\_CALLBACK**</span></span>](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_join_callback)

[<span data-ttu-id="1f438-109">**\_retorno de \_ chamada de saída local PMGM \_**</span><span class="sxs-lookup"><span data-stu-id="1f438-109">**PMGM\_LOCAL\_LEAVE\_CALLBACK**</span></span>](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_leave_callback)

[<span data-ttu-id="1f438-110">**retorno de chamada do PMGM \_ RPF \_**</span><span class="sxs-lookup"><span data-stu-id="1f438-110">**PMGM\_RPF\_CALLBACK**</span></span>](/windows/desktop/api/Mgm/nc-mgm-pmgm_rpf_callback)

[<span data-ttu-id="1f438-111">**PMGM \_ errado \_ se o \_ retorno de chamada**</span><span class="sxs-lookup"><span data-stu-id="1f438-111">**PMGM\_WRONG\_IF\_CALLBACK**</span></span>](/windows/desktop/api/Mgm/nc-mgm-pmgm_wrong_if_callback)

<span data-ttu-id="1f438-112">O Gerenciador de grupos de multicast usa os seguintes retornos de chamada para notificar IGMP de eventos e alterações de Estado:</span><span class="sxs-lookup"><span data-stu-id="1f438-112">The multicast group manager uses the following callbacks to notify IGMP of events and state changes:</span></span>

[<span data-ttu-id="1f438-113">**PMGM \_ desabilitar \_ \_ retorno de chamada IGMP**</span><span class="sxs-lookup"><span data-stu-id="1f438-113">**PMGM\_DISABLE\_IGMP\_CALLBACK**</span></span>](/windows/win32/api/mgm/nc-mgm-pmgm_disable_igmp_callback)

[<span data-ttu-id="1f438-114">**PMGM \_ habilitar \_ \_ retorno de chamada IGMP**</span><span class="sxs-lookup"><span data-stu-id="1f438-114">**PMGM\_ENABLE\_IGMP\_CALLBACK**</span></span>](/windows/desktop/api/Mgm/nc-mgm-pmgm_enable_igmp_callback)

 

 