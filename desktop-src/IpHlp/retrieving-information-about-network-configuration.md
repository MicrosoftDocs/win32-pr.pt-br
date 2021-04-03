---
description: O IP Helper fornece informações sobre a configuração de rede do computador local.
ms.assetid: 6135dca5-00c8-4ed4-bb89-7c99abeb7c7c
title: Recuperando informações sobre a configuração de rede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64a6860b329ba7c69575be1dfeaaa2e19c57558f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922626"
---
# <a name="retrieving-information-about-network-configuration"></a><span data-ttu-id="22f04-103">Recuperando informações sobre a configuração de rede</span><span class="sxs-lookup"><span data-stu-id="22f04-103">Retrieving Information About Network Configuration</span></span>

<span data-ttu-id="22f04-104">O IP Helper fornece informações sobre a configuração de rede do computador local.</span><span class="sxs-lookup"><span data-stu-id="22f04-104">IP Helper provides information about the network configuration of the local computer.</span></span> <span data-ttu-id="22f04-105">Para recuperar informações gerais de configuração, use a função [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) .</span><span class="sxs-lookup"><span data-stu-id="22f04-105">To retrieve general configuration information, use the [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) function.</span></span> <span data-ttu-id="22f04-106">Essa função retorna informações que não são específicas de um adaptador ou interface específica.</span><span class="sxs-lookup"><span data-stu-id="22f04-106">This function returns information that is not specific to a particular adapter or interface.</span></span> <span data-ttu-id="22f04-107">Por exemplo, **GetNetworkParams** retorna uma lista dos servidores DNS que são usados pelo computador local.</span><span class="sxs-lookup"><span data-stu-id="22f04-107">For example, **GetNetworkParams** returns a list of the DNS servers that are used by the local computer.</span></span>

-   <span data-ttu-id="22f04-108">Para obter exemplos de código envolvendo [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) , consulte [recuperando informações usando GetNetworkParams](retrieving-information-using-getnetworkparams.md).</span><span class="sxs-lookup"><span data-stu-id="22f04-108">For code samples involving [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) see [Retrieving Information Using GetNetworkParams](retrieving-information-using-getnetworkparams.md).</span></span>

 

 



