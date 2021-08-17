---
description: Use as funções a seguir para garantir que um aplicativo receba notificação de determinados eventos de rede.
ms.assetid: e1ca5abf-83c2-44f0-8049-ddf1b81ef088
title: Recebendo notificação de eventos de rede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28225654bc7e4119f76eff21425e96dda83f628b88d16be9cdfc370d9fa63712
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146609"
---
# <a name="receiving-notification-of-network-events"></a>Recebendo notificação de eventos de rede

Use as funções a seguir para garantir que um aplicativo receba notificação de determinados eventos de rede.

Use a [**função NotifyAddrChange**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-notifyaddrchange) para solicitar notificação de qualquer alteração que ocorra no mapeamento entre endereços IP e interfaces no computador local.

Da mesma forma, a [**função NotifyRouteChange**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-notifyroutechange) permite que um aplicativo solicite notificação de qualquer alteração que ocorra na tabela de roteamento de IP.

As notificações fornecidas por essas funções não especificam o que mudou; eles simplesmente especificam que algo foi alterado. Use outras funções auxiliares de IP, como [**GetIPAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) e [**GetBestRoute,**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getbestroute)para determinar a natureza exata da alteração.

 

 



