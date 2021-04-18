---
description: O IP Helper pode auxiliar no gerenciamento de endereços IP associados a interfaces no computador local. Use as funções descritas nos parágrafos a seguir para o gerenciamento de endereços IP.
ms.assetid: 94da3e53-1898-4721-b5f0-0b7244574c55
title: Gerenciando endereços IP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77b0917050799ea452cf1c6ee3e068cc29793df8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105767784"
---
# <a name="managing-ip-addresses"></a><span data-ttu-id="a18f3-104">Gerenciando endereços IP</span><span class="sxs-lookup"><span data-stu-id="a18f3-104">Managing IP Addresses</span></span>

<span data-ttu-id="a18f3-105">O IP Helper pode auxiliar no gerenciamento de endereços IP associados a interfaces no computador local.</span><span class="sxs-lookup"><span data-stu-id="a18f3-105">IP Helper can assist in the management of IP addresses associated with interfaces on the local computer.</span></span> <span data-ttu-id="a18f3-106">Use as funções descritas nos parágrafos a seguir para o gerenciamento de endereços IP.</span><span class="sxs-lookup"><span data-stu-id="a18f3-106">Use the functions described in the following paragraphs for IP address management.</span></span>

<span data-ttu-id="a18f3-107">A função [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) recupera uma tabela que contém o mapeamento de endereços IP para interfaces.</span><span class="sxs-lookup"><span data-stu-id="a18f3-107">The [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) function retrieves a table that contains the mapping of IP addresses to interfaces.</span></span> <span data-ttu-id="a18f3-108">Mais de um endereço IP pode estar associado à mesma interface.</span><span class="sxs-lookup"><span data-stu-id="a18f3-108">More than one IP address may be associated with the same interface.</span></span>

<span data-ttu-id="a18f3-109">Use a função [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) para adicionar um endereço IP a uma interface específica.</span><span class="sxs-lookup"><span data-stu-id="a18f3-109">Use the [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) function to add an IP address to a particular interface.</span></span> <span data-ttu-id="a18f3-110">Para remover os endereços IP que foram adicionados anteriormente usando **AddIPAddress**, use a função [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) .</span><span class="sxs-lookup"><span data-stu-id="a18f3-110">To remove IP addresses that were previously added using **AddIPAddress**, use the [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) function.</span></span>

<span data-ttu-id="a18f3-111">As funções [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) e [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) exigem que o computador local esteja usando o protocolo DHCP.</span><span class="sxs-lookup"><span data-stu-id="a18f3-111">The [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) and [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) functions require the local computer to be using Dynamic Host Configuration Protocol (DHCP).</span></span> <span data-ttu-id="a18f3-112">A função **IpReleaseAddress** libera um endereço IP que foi obtido anteriormente do DHCP.</span><span class="sxs-lookup"><span data-stu-id="a18f3-112">The **IpReleaseAddress** function releases an IP address that was previously obtained from DHCP.</span></span> <span data-ttu-id="a18f3-113">A função **IpRenewAddress** renova uma concessão DHCP em um endereço IP específico.</span><span class="sxs-lookup"><span data-stu-id="a18f3-113">The **IpRenewAddress** function renews a DHCP lease on a particular IP address.</span></span> <span data-ttu-id="a18f3-114">Uma concessão de DHCP permite que um computador use um endereço IP por um período de tempo especificado.</span><span class="sxs-lookup"><span data-stu-id="a18f3-114">A DHCP lease allows a computer to use an IP address for a specified period of time.</span></span>

-   <span data-ttu-id="a18f3-115">Para obter exemplos de código envolvendo [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) , consulte [Managing IP addresses using GetIpAddrTable](managing-ip-addresses-using-getipaddrtable.md).</span><span class="sxs-lookup"><span data-stu-id="a18f3-115">For code samples involving [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) see [Managing IP Addresses Using GetIpAddrTable](managing-ip-addresses-using-getipaddrtable.md).</span></span>

-   <span data-ttu-id="a18f3-116">Para obter exemplos de código envolvendo [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) e [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress), consulte [Gerenciando endereços IP usando AddIPAddress e DeleteIPAddress](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md).</span><span class="sxs-lookup"><span data-stu-id="a18f3-116">For code samples involving [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) and [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress), see [Managing IP Addresses Using AddIPAddress and DeleteIPAddress](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md).</span></span>

-   <span data-ttu-id="a18f3-117">Para obter exemplos de código envolvendo [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) e [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) , consulte [Gerenciando concessões DHCP usando IpReleaseAddress e IpRenewAddress](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md).</span><span class="sxs-lookup"><span data-stu-id="a18f3-117">For code samples involving [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) and [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) see [Managing DHCP Leases Using IpReleaseAddress and IpRenewAddress](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md).</span></span>

 

 



