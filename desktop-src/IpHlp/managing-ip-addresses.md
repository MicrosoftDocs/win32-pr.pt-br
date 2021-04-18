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
# <a name="managing-ip-addresses"></a>Gerenciando endereços IP

O IP Helper pode auxiliar no gerenciamento de endereços IP associados a interfaces no computador local. Use as funções descritas nos parágrafos a seguir para o gerenciamento de endereços IP.

A função [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) recupera uma tabela que contém o mapeamento de endereços IP para interfaces. Mais de um endereço IP pode estar associado à mesma interface.

Use a função [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) para adicionar um endereço IP a uma interface específica. Para remover os endereços IP que foram adicionados anteriormente usando **AddIPAddress**, use a função [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) .

As funções [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) e [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) exigem que o computador local esteja usando o protocolo DHCP. A função **IpReleaseAddress** libera um endereço IP que foi obtido anteriormente do DHCP. A função **IpRenewAddress** renova uma concessão DHCP em um endereço IP específico. Uma concessão de DHCP permite que um computador use um endereço IP por um período de tempo especificado.

-   Para obter exemplos de código envolvendo [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) , consulte [Managing IP addresses using GetIpAddrTable](managing-ip-addresses-using-getipaddrtable.md).

-   Para obter exemplos de código envolvendo [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) e [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress), consulte [Gerenciando endereços IP usando AddIPAddress e DeleteIPAddress](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md).

-   Para obter exemplos de código envolvendo [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) e [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) , consulte [Gerenciando concessões DHCP usando IpReleaseAddress e IpRenewAddress](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md).

 

 



