---
title: Implantando o balanceamento de carga
description: Implantando o balanceamento de carga
ms.assetid: d80b8999-16c9-4fc8-a1cb-35a65f434884
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc00430e8e93334c04dc74c57fc8b50db7d3c899
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159604"
---
# <a name="deploying-load-balancing"></a>Implantando o balanceamento de carga

O ambiente de implantação típico e o caso de uso é o que o balanceador de carga RPC é utilizado é mostrado abaixo:![balanceamento de carga RPC](images/rpc-load-balancing.png)

1.  O cliente RPC faz uma conexão RPC/HTTP com o farm de servidores.
2.  A conexão é encaminhada pela rede para um balanceador de carga de front-end
3.  O balanceador de carga de front-end escolhe um servidor para atender à solicitação. Neste exemplo, o balanceador de carga de front-end encaminha a conexão para o servidor 1.
4.  O serviço de balanceador de carga RPC arbitra a conexão. Ele determina que essa é a primeira conexão do cliente e associa a conexão ao servidor local, servidor 1.
5.  O cliente faz uma segunda solicitação RPC/HTTP.
6.  A solicitação é encaminhada pela rede para o balanceador de carga de front-end.
7.  O balanceador de carga de front-end escolhe um servidor para atender à solicitação. Nesse caso, o balanceador de carga de front-end escolhe o servidor 2 para atender à solicitação.
8.  O serviço de Load Balancer RPC arbitra a conexão. Ele reconhece que as conexões desse cliente estão sendo atendidas pelo servidor 1.
9.  A conexão é encaminhada para o servidor 1.

 

 




