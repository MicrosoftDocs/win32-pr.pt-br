---
description: O IP Helper fornece informações sobre a configuração de rede do computador local.
ms.assetid: 6135dca5-00c8-4ed4-bb89-7c99abeb7c7c
title: Recuperando informações sobre a configuração de rede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 767bdf0ec8c316bc4998e50e06e6f1a88f92742adff88f11745fbbd80c0b26ab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050316"
---
# <a name="retrieving-information-about-network-configuration"></a>Recuperando informações sobre a configuração de rede

O IP Helper fornece informações sobre a configuração de rede do computador local. Para recuperar informações gerais de configuração, use a função [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) . Essa função retorna informações que não são específicas de um adaptador ou interface específica. Por exemplo, **GetNetworkParams** retorna uma lista dos servidores DNS que são usados pelo computador local.

-   Para obter exemplos de código envolvendo [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) , consulte [recuperando informações usando GetNetworkParams](retrieving-information-using-getnetworkparams.md).

 

 



