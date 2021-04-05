---
title: Remover retornos de chamada de alerta
description: Quando o Gerenciador do grupo de multicast é notificado de que os receptores estão saindo de um grupo em uma interface, o Gerenciador do grupo de multicast invoca o retorno de chamada de \_ retorno de chamada de alerta de remoção PMGM \_ \_ .
ms.assetid: 34eb6941-9488-481f-93ca-821789acc140
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a81dab70eaded0fd1fe21bd1b5ec1b5ca495272
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006052"
---
# <a name="prune-alert-callbacks"></a><span data-ttu-id="ce029-103">Remover retornos de chamada de alerta</span><span class="sxs-lookup"><span data-stu-id="ce029-103">Prune Alert Callbacks</span></span>

<span data-ttu-id="ce029-104">Quando o Gerenciador do grupo de multicast é notificado de que os receptores estão saindo de um grupo em uma interface, o Gerenciador do grupo de multicast invoca o retorno de chamada de [**retorno de chamada de \_ alerta de remoção \_ \_ PMGM**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback) .</span><span class="sxs-lookup"><span data-stu-id="ce029-104">When the multicast group manager is notified that receivers are leaving a group on an interface, the multicast group manager invokes the [**PMGM\_PRUNE\_ALERT\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback) callback.</span></span> <span data-ttu-id="ce029-105">Esse retorno de chamada notifica os protocolos de roteamento que os clientes não pertencem mais ao grupo especificado.</span><span class="sxs-lookup"><span data-stu-id="ce029-105">This callback notifies the routing protocols that clients no longer belong to the specified group.</span></span> <span data-ttu-id="ce029-106">Portanto, os protocolos de roteamento devem parar de solicitar dados multicast para os grupos especificados.</span><span class="sxs-lookup"><span data-stu-id="ce029-106">Therefore, the routing protocols must stop requesting multicast data for the specified groups.</span></span>

<span data-ttu-id="ce029-107">O Gerenciador do grupo de multicast tem um conjunto predefinido de regras que são usadas para determinar quando esse retorno de chamada é invocado.</span><span class="sxs-lookup"><span data-stu-id="ce029-107">The multicast group manager has a predefined set of rules that are used to determine when this callback is invoked.</span></span> <span data-ttu-id="ce029-108">Essas regras se baseiam no tipo de solicitação de remoção enviado pelo cliente e na ordem em que as solicitações de remoção foram recebidas.</span><span class="sxs-lookup"><span data-stu-id="ce029-108">These rules are based on both the type of prune request sent by the client and the order the prune requests were received in.</span></span>

## <a name="wildcard-prune-requests"></a><span data-ttu-id="ce029-109">Solicitações de remoção de curinga</span><span class="sxs-lookup"><span data-stu-id="ce029-109">Wildcard Prune Requests</span></span>

<span data-ttu-id="ce029-110">Quando uma remoção de caractere curinga para um grupo ( \* , g) é recebida e a interface final está sendo removida para o segundo cliente (ou seja, quando as interfaces para apenas um único cliente permanecem), o Gerenciador de grupo de multicast invoca o retorno de chamada de [**retorno de \_ \_ \_ chamada de alerta de remoção PMGM**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback) para esse cliente restante.</span><span class="sxs-lookup"><span data-stu-id="ce029-110">When a wildcard prune for a group (\*, g) is received and the final interface is being removed for the second-to-last client (that is, when interfaces for only a single client remain), the multicast group manager invokes the [**PMGM\_PRUNE\_ALERT\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback) callback to that remaining client.</span></span> <span data-ttu-id="ce029-111">Depois que a interface final for removida para o último cliente (ou seja, quando nenhuma outra interface permanecer), esse retorno de chamada será invocado para todos os outros clientes registrados com o Gerenciador do grupo de multicast.</span><span class="sxs-lookup"><span data-stu-id="ce029-111">After the final interface is removed for the last client (that is, when no other interfaces remain), then this callback is invoked for all the other clients that are registered with the multicast group manager.</span></span>

## <a name="source-specific-prune-requests"></a><span data-ttu-id="ce029-112">ReSource-Specific solicitações de remoção</span><span class="sxs-lookup"><span data-stu-id="ce029-112">Source-Specific Prune Requests</span></span>

<span data-ttu-id="ce029-113">Quando uma remoção específica de origem para um grupo (s, g) é recebida, o Gerenciador de grupo de multicast invoca o retorno de chamada de [**\_ retorno de \_ \_ chamada de alerta PMGM**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback) apenas para o cliente que possui a interface de entrada em direção às s de origem.</span><span class="sxs-lookup"><span data-stu-id="ce029-113">When a source-specific prune for a group (s, g) is received, the multicast group manager invokes the [**PMGM\_PRUNE\_ALERT\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback) callback only for the client that owns the incoming interface towards the source s.</span></span>

 

 




