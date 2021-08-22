---
description: O Auxiliar de IP pode ajudar no gerenciamento de endereços IP associados a interfaces no computador local. Use as funções descritas nos parágrafos a seguir para gerenciamento de endereços IP.
ms.assetid: 94da3e53-1898-4721-b5f0-0b7244574c55
title: Gerenciando endereços IP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b51e0e1e30adf064330a2a4070e6872ca87b50b94e3ad1ab458c3c84878d5549
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119560316"
---
# <a name="managing-ip-addresses"></a>Gerenciando endereços IP

O Auxiliar de IP pode ajudar no gerenciamento de endereços IP associados a interfaces no computador local. Use as funções descritas nos parágrafos a seguir para gerenciamento de endereços IP.

A [**função GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) recupera uma tabela que contém o mapeamento de endereços IP para interfaces. Mais de um endereço IP pode ser associado à mesma interface.

Use a [**função AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) para adicionar um endereço IP a uma interface específica. Para remover endereços IP que foram adicionados anteriormente usando **AddIPAddress**, use a [**função DeleteIPAddress.**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress)

As [**funções IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) e [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) exigem que o computador local use o protocolo DHCP. A **função IpReleaseAddress** libera um endereço IP que foi obtido anteriormente do DHCP. A **função IpRenewAddress** renova uma concessão DHCP em um endereço IP específico. Uma concessão DHCP permite que um computador use um endereço IP por um período de tempo especificado.

-   Para obter exemplos de código [**que envolvem GetIpAddrTable,**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) consulte [Gerenciando endereços IP usando GetIpAddrTable](managing-ip-addresses-using-getipaddrtable.md).

-   Para exemplos de código que [**envolvem AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) e [**DeleteIPAddress,**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress)consulte Gerenciando endereços IP usando [AddIPAddress e DeleteIPAddress](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md).

-   Para exemplos de código que envolvem [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) e [**IpRenewAddress,**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) consulte Gerenciando concessões [DHCP usando IpReleaseAddress e IpRenewAddress](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md).

 

 



