---
title: Limpeza da entrada do serviço de nome
description: Uma entrada de serviço de nome deve conter informações que não são alteradas com frequência.
ms.assetid: b581bc10-e537-4714-b89a-d998fec23360
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cf0ed6a21074a49a472d7505dcfea37cf182026
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005851"
---
# <a name="name-service-entry-cleanup"></a>Limpeza da entrada do serviço de nome

Uma entrada de serviço de nome deve conter informações que não são alteradas com frequência. Por esse motivo, não inclua pontos de extremidade dinâmicos em seus identificadores de associação exportados porque eles serão alterados em cada invocação do servidor e abrirão sua entrada de serviço de nome. Para remover esses identificadores de ligação, use [**RpcBindingReset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset).

Por exemplo, uma sequência razoável de operações de servidor seria:

Para mais de um transporte:

``` syntax
RpcServerUseProtseq();
RpcServerUseProtseq();
```

Para posicionar associações no mapeador de ponto de extremidade:

``` syntax
RpcServerInqBindings(&Vector);
RpcEpRegister(Interface, Vector);
```

Para remover pontos de extremidade de associações:

``` syntax
for (i=0; i < Vector- > Count; + + i)
{
    RpcBindingReset(Vector->BindingH[i];
}
```

Para adicionar associações ao serviço de nome:

``` syntax
RpcNsBindingExport(RPC_C_NS_SYNTAX_DEFAULT, EntryName, Interface
                   Vector);
RpcServerListen();
```

 

 




