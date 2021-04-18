---
description: O IP Helper fornece recursos para gerenciar adaptadores de rede. Há uma correspondência um-para-um entre as interfaces e os adaptadores em um determinado computador. Uma interface é uma abstração de nível de IP, enquanto que um adaptador é uma abstração no nível de vínculo de datalink.
ms.assetid: fbb32941-2add-4f74-90c4-1dc1bfebd64c
title: Gerenciando adaptadores de rede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaa8f42cf1499ee7873d13334d0edbc9f954794f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501602"
---
# <a name="managing-network-adapters"></a>Gerenciando adaptadores de rede

O IP Helper fornece recursos para gerenciar adaptadores de rede. Há uma correspondência um-para-um entre as interfaces e os adaptadores em um determinado computador. Uma interface é uma abstração de nível de IP, enquanto que um adaptador é uma abstração no nível de vínculo de datalink.

Use as funções descritas nos parágrafos a seguir para recuperar informações sobre os adaptadores de rede no computador local.

A função [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) retorna uma matriz de estruturas de [**\_ \_ informações do adaptador IP**](/windows/desktop/api/Iptypes/ns-iptypes-ip_adapter_info) , uma para cada adaptador no computador local. A função [**GetPerAdapterInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getperadapterinfo) retorna informações adicionais sobre um adaptador específico. A função **GetPerAdapterInfo** requer que o chamador especifique o índice do adaptador. Para obter o índice de adaptador do nome do adaptador, use a função [**GetAdapterIndex**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadapterindex) .

Alguns aplicativos usam adaptadores que recebem datagrams, mas não podem transmiti-los. Para obter informações sobre esses adaptadores, use a função [**GetUniDirectionalAdapterInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getunidirectionaladapterinfo) .

A função [**GetAdaptersAddresses**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersaddresses) permite que você recupere os endereços IP associados a um adaptador específico. Essa função dá suporte ao endereçamento IPv4 e IPv6.

-   Para obter exemplos de código envolvendo [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) , consulte [Managing Network adapters using GetAdaptersInfo](managing-network-adapters-using-getadaptersinfo.md).

 

 



