---
description: Você pode usar o IP Helper para executar operações de ARP (protocolo de resolução de endereço) para o computador local. Use as funções a seguir para recuperar e modificar a tabela ARP.
ms.assetid: 2c5dc1f8-590f-4b41-b6bb-f82ab093252f
title: Usando o protocolo de resolução de endereço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deec57c3b028f8f90135567bb07dbc00bda89036
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757007"
---
# <a name="using-the-address-resolution-protocol"></a><span data-ttu-id="e659a-104">Usando o protocolo de resolução de endereço</span><span class="sxs-lookup"><span data-stu-id="e659a-104">Using the Address Resolution Protocol</span></span>

<span data-ttu-id="e659a-105">Você pode usar o IP Helper para executar operações de ARP (protocolo de resolução de endereço) para o computador local.</span><span class="sxs-lookup"><span data-stu-id="e659a-105">You can use IP Helper to perform Address Resolution Protocol (ARP) operations for the local computer.</span></span> <span data-ttu-id="e659a-106">Use as funções a seguir para recuperar e modificar a tabela ARP.</span><span class="sxs-lookup"><span data-stu-id="e659a-106">Use the following functions to retrieve and modify the ARP table.</span></span>

<span data-ttu-id="e659a-107">O [**GetIpNetTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipnettable) recupera a tabela ARP.</span><span class="sxs-lookup"><span data-stu-id="e659a-107">The [**GetIpNetTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipnettable) retrieves the ARP table.</span></span> <span data-ttu-id="e659a-108">A tabela ARP contém o mapeamento de endereços IP para endereços físicos.</span><span class="sxs-lookup"><span data-stu-id="e659a-108">The ARP table contains the mapping of IP addresses to physical addresses.</span></span> <span data-ttu-id="e659a-109">Os endereços físicos às vezes são chamados de endereços MAC (controlador de acesso à mídia).</span><span class="sxs-lookup"><span data-stu-id="e659a-109">Physical addresses are sometimes referred to as Media Access Controller (MAC) addresses.</span></span>

<span data-ttu-id="e659a-110">Use as funções [**CreateIpNetEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createipnetentry) e [**DeleteIpNetEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipnetentry) para adicionar ou remover entradas ARP específicas de ou para a tabela.</span><span class="sxs-lookup"><span data-stu-id="e659a-110">Use the [**CreateIpNetEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createipnetentry) and [**DeleteIpNetEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipnetentry) functions to add or remove particular ARP entries to or from the table.</span></span> <span data-ttu-id="e659a-111">A função [**FlushIpNetTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-flushipnettable) exclui todas as entradas da tabela.</span><span class="sxs-lookup"><span data-stu-id="e659a-111">The [**FlushIpNetTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-flushipnettable) function deletes all entries from the table.</span></span>

<span data-ttu-id="e659a-112">Para criar ou excluir entradas ARP de proxy, use as funções [**CreateProxyArpEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createproxyarpentry) e [**DeleteProxyArpEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteproxyarpentry) .</span><span class="sxs-lookup"><span data-stu-id="e659a-112">To create or delete proxy ARP entries, use the [**CreateProxyArpEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createproxyarpentry) and [**DeleteProxyArpEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteproxyarpentry) functions.</span></span>

<span data-ttu-id="e659a-113">A função [**SendARP**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-sendarp) envia uma solicitação ARP para a rede local.</span><span class="sxs-lookup"><span data-stu-id="e659a-113">The [**SendARP**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-sendarp) function sends an ARP request to the local network.</span></span>

 

 



