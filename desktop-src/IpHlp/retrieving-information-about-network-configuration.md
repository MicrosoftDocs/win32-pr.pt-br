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
# <a name="retrieving-information-about-network-configuration"></a>Recuperando informações sobre a configuração de rede

O IP Helper fornece informações sobre a configuração de rede do computador local. Para recuperar informações gerais de configuração, use a função [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) . Essa função retorna informações que não são específicas de um adaptador ou interface específica. Por exemplo, **GetNetworkParams** retorna uma lista dos servidores DNS que são usados pelo computador local.

-   Para obter exemplos de código envolvendo [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) , consulte [recuperando informações usando GetNetworkParams](retrieving-information-using-getnetworkparams.md).

 

 



