---
title: Recuperando o status da alteração e ignorando as alterações
description: O cliente pode consultar o Gerenciador de tabela de roteamento para descobrir se uma notificação de uma alteração em um destino está pendente chamando RtmGetChangeStatus. Essa função retorna TRUE até que o chamador recupere essa alteração chamando RtmGetChangedDests.
ms.assetid: 778279ac-00c5-4de0-9ac7-eca1ac7fec6a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7a339cbf9ba4e97dfef25b2ebc2020ff94f8e20
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635436"
---
# <a name="retrieving-change-status-and-ignoring-changes"></a><span data-ttu-id="2a088-104">Recuperando o status da alteração e ignorando as alterações</span><span class="sxs-lookup"><span data-stu-id="2a088-104">Retrieving Change Status and Ignoring Changes</span></span>

<span data-ttu-id="2a088-105">O cliente pode consultar o Gerenciador de tabela de roteamento para descobrir se uma notificação de uma alteração em um destino está pendente chamando [**RtmGetChangeStatus**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangestatus).</span><span class="sxs-lookup"><span data-stu-id="2a088-105">The client can query the routing table manager to find out if a notification of a change to a destination is pending by calling [**RtmGetChangeStatus**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangestatus).</span></span> <span data-ttu-id="2a088-106">Essa função retorna **true** até que o chamador recupere essa alteração chamando [**RtmGetChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangeddests).</span><span class="sxs-lookup"><span data-stu-id="2a088-106">This function returns **TRUE** until the caller retrieves this change by calling [**RtmGetChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangeddests).</span></span>

<span data-ttu-id="2a088-107">Um cliente pode usar essa consulta para evitar a execução de uma ação que teria de ser desfeita depois que a notificação de alteração for recebida e processada.</span><span class="sxs-lookup"><span data-stu-id="2a088-107">A client can use this query to avoid performing an action that would have to be undone after the change notification is received and processed.</span></span> <span data-ttu-id="2a088-108">O uso desse recurso permite que o cliente trabalhe com eficiência, adiando determinadas operações para um momento posterior.</span><span class="sxs-lookup"><span data-stu-id="2a088-108">Using this feature allows the client to work efficiently by deferring certain operations to a later time.</span></span>

<span data-ttu-id="2a088-109">O cliente também pode ignorar uma notificação de alteração pendente para um destino chamando [**RtmIgnoreChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmignorechangeddests).</span><span class="sxs-lookup"><span data-stu-id="2a088-109">The client can also ignore a pending change notification for a destination by calling [**RtmIgnoreChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmignorechangeddests).</span></span> <span data-ttu-id="2a088-110">Uma chamada posterior para [**RtmGetChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangeddests) não retorna esse destino, a menos que outra alteração ocorra após a chamada para [**RtmIgnoreChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmignorechangeddests).</span><span class="sxs-lookup"><span data-stu-id="2a088-110">A later call to [**RtmGetChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangeddests) does not return this destination unless another change occurs after the call to [**RtmIgnoreChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmignorechangeddests).</span></span>

 

 




