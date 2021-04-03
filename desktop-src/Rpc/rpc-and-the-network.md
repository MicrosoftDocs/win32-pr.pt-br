---
title: RPC e a rede
description: Esta seção discute como lidar com a não confiabilidade de rede ao usar o RPC e explica como as APIs de nível de RPC se convertem em atividade de rede. A seção refere-se somente às \_ \_ sequências de protocolo http TCP e ncacn de IP ncacn \_ .
ms.assetid: af7c67ea-32af-40b0-b74b-0a339e5088c4
keywords:
- RPC de chamada de procedimento remoto, práticas recomendadas, RPC e rede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87c0373bb81d9da0bf20eed1fb9f80863604b040
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084771"
---
# <a name="rpc-and-the-network"></a>RPC e a rede

Esta seção discute como lidar com a não confiabilidade de rede ao usar o RPC e explica como as APIs de nível de RPC se convertem em atividade de rede. A seção refere-se somente às sequências de [**protocolo \_ http**](/windows/desktop/Midl/ncacn-http) TCP e ncacn de [**\_ \_ IP ncacn**](/windows/desktop/Midl/ncacn-ip-tcp) .

Esta seção é dividida nos seguintes tópicos:

-   [Desenvolvimento versus implantação na rede](development-versus-deployment-in-the-network.md)
-   [Evitar travamentos de Client-Side](preventing-client-side-hangs.md)
-   [Gerenciando conjuntos de conexões de rede (associações)](managing-network-connection-sets-associations-.md)
-   [Limpeza de conexão ociosa](idle-connection-cleanup.md)
-   [Lidando com a perda de conectividade](dealing-with-loss-of-connectivity.md)
-   [Limpeza do lado do servidor](server-side-cleanup.md)

 

 