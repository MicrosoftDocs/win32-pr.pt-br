---
description: Use as funções a seguir para garantir que um aplicativo receba uma notificação de determinados eventos de rede.
ms.assetid: e1ca5abf-83c2-44f0-8049-ddf1b81ef088
title: Recebendo notificação de eventos de rede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecb9840f7ddf4adbfaae5775de337da81a3e7670
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105810481"
---
# <a name="receiving-notification-of-network-events"></a><span data-ttu-id="6c39c-103">Recebendo notificação de eventos de rede</span><span class="sxs-lookup"><span data-stu-id="6c39c-103">Receiving Notification of Network Events</span></span>

<span data-ttu-id="6c39c-104">Use as funções a seguir para garantir que um aplicativo receba uma notificação de determinados eventos de rede.</span><span class="sxs-lookup"><span data-stu-id="6c39c-104">Use the following functions to ensure that an application receives notification of certain network events.</span></span>

<span data-ttu-id="6c39c-105">Use a função [**NotifyAddrChange**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-notifyaddrchange) para solicitar notificação de qualquer alteração que ocorra no mapeamento entre endereços IP e interfaces no computador local.</span><span class="sxs-lookup"><span data-stu-id="6c39c-105">Use the [**NotifyAddrChange**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-notifyaddrchange) function to request notification of any change that occurs in the mapping between IP addresses and interfaces on the local computer.</span></span>

<span data-ttu-id="6c39c-106">Da mesma forma, a função [**NotifyRouteChange**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-notifyroutechange) permite que um aplicativo solicite notificação de qualquer alteração que ocorra na tabela de roteamento de IP.</span><span class="sxs-lookup"><span data-stu-id="6c39c-106">Similarly, the [**NotifyRouteChange**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-notifyroutechange) function enables an application to request notification of any change that occurs in the IP routing table.</span></span>

<span data-ttu-id="6c39c-107">As notificações fornecidas por essas funções não especificam o que mudou; Eles simplesmente especificam que algo foi alterado.</span><span class="sxs-lookup"><span data-stu-id="6c39c-107">The notifications provided by these functions do not specify what changed; they simply specify that something changed.</span></span> <span data-ttu-id="6c39c-108">Use outras funções auxiliares de IP, como [**GetIPAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) e [**GetBestRoute**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getbestroute), para determinar a natureza exata da alteração.</span><span class="sxs-lookup"><span data-stu-id="6c39c-108">Use other IP Helper functions, such as [**GetIPAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) and [**GetBestRoute**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getbestroute), to determine the exact nature of the change.</span></span>

 

 



