---
title: RPC e a rede
description: Esta seção discute como lidar com a falta de confiabilidade de rede ao usar RPC e explica como as APIs no nível de RPC se traduzem em atividade de rede. A seção refere-se apenas às sequências de protocolo ncacn ip tcp e \_ \_ ncacn \_ http.
ms.assetid: af7c67ea-32af-40b0-b74b-0a339e5088c4
keywords:
- RPC de Chamada de Procedimento Remoto , práticas recomendadas, RPC e a rede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 212e1f3b6f281709a3344367a59d858b7f96b77a6adbdc44fc8556769f2edcaa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118926648"
---
# <a name="rpc-and-the-network"></a>RPC e a rede

Esta seção discute como lidar com a falta de confiabilidade de rede ao usar RPC e explica como as APIs no nível de RPC se traduzem em atividade de rede. A seção refere-se apenas às sequências de protocolo [**ncacn \_ ip \_ tcp**](/windows/desktop/Midl/ncacn-ip-tcp) e [**ncacn \_ http.**](/windows/desktop/Midl/ncacn-http)

Esta seção é dividida nos seguintes tópicos:

-   [Desenvolvimento versus implantação na rede](development-versus-deployment-in-the-network.md)
-   [Impedindo Client-Side travamentos](preventing-client-side-hangs.md)
-   [Gerenciando conjuntos de conexões de rede (associações)](managing-network-connection-sets-associations-.md)
-   [Limpeza de conexão ociosa](idle-connection-cleanup.md)
-   [Lidando com perda de conectividade](dealing-with-loss-of-connectivity.md)
-   [Limpeza do lado do servidor](server-side-cleanup.md)

 

 