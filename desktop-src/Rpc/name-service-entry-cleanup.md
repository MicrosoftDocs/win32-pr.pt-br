---
title: Limpeza de entrada de serviço de nome
description: Uma entrada de serviço de nome deve conter informações que não mudam com frequência.
ms.assetid: b581bc10-e537-4714-b89a-d998fec23360
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecfe7484d1c6d557899e3b661a3a616c97d3890becfad51df0e91f5a69467faa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120019601"
---
# <a name="name-service-entry-cleanup"></a>Limpeza de entrada de serviço de nome

Uma entrada de serviço de nome deve conter informações que não mudam com frequência. Por esse motivo, não inclua pontos de extremidade dinâmicos em seus alças de associação exportados, pois eles serão alterados em cada invocação do servidor e desorganmente sua entrada de serviço de nome. Para remover esses alças de associação, use [**RpcBindingReset.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset)

Por exemplo, uma sequência razoável de operações de servidor seria:

Para mais de um transporte:

``` syntax
RpcServerUseProtseq();
RpcServerUseProtseq();
```

Para colocar as vinculações no mapeamento de ponto de extremidade:

``` syntax
RpcServerInqBindings(&Vector);
RpcEpRegister(Interface, Vector);
```

Para remover pontos de extremidade de vinculações:

``` syntax
for (i=0; i < Vector- > Count; + + i)
{
    RpcBindingReset(Vector->BindingH[i];
}
```

Para adicionar vinculações ao serviço de nome:

``` syntax
RpcNsBindingExport(RPC_C_NS_SYNTAX_DEFAULT, EntryName, Interface
                   Vector);
RpcServerListen();
```

 

 




