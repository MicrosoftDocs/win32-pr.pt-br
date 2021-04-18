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
# <a name="receiving-notification-of-network-events"></a>Recebendo notificação de eventos de rede

Use as funções a seguir para garantir que um aplicativo receba uma notificação de determinados eventos de rede.

Use a função [**NotifyAddrChange**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-notifyaddrchange) para solicitar notificação de qualquer alteração que ocorra no mapeamento entre endereços IP e interfaces no computador local.

Da mesma forma, a função [**NotifyRouteChange**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-notifyroutechange) permite que um aplicativo solicite notificação de qualquer alteração que ocorra na tabela de roteamento de IP.

As notificações fornecidas por essas funções não especificam o que mudou; Eles simplesmente especificam que algo foi alterado. Use outras funções auxiliares de IP, como [**GetIPAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) e [**GetBestRoute**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getbestroute), para determinar a natureza exata da alteração.

 

 



