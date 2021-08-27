---
title: Implantando o balanceamento de carga
description: Implantando o balanceamento de carga
ms.assetid: d80b8999-16c9-4fc8-a1cb-35a65f434884
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c36d1ba29aedd5e94c29095d18fb84790ec4b76956ea20bc2ffd584b5a6a179f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021836"
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

 

 




