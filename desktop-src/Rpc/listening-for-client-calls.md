---
title: Escutando chamadas de cliente
description: Depois que o aplicativo de servidor registrou suas interfaces, criou as informações de associação necessárias e registrou seus pontos de extremidade, ele está pronto para começar a escutar chamadas de procedimento remoto de programas cliente.
ms.assetid: ca9d24ed-0acc-45de-bbb2-761c56745a58
keywords:
- Chamada de procedimento remoto RPC, tarefas, escutando chamadas de cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f375a4620e301f59d168bf5f7a4dbeedc0fb89f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822931"
---
# <a name="listening-for-client-calls"></a>Escutando chamadas de cliente

Depois que o aplicativo de servidor registrou suas interfaces, criou as informações de associação necessárias e registrou seus pontos de extremidade, ele está pronto para começar a escutar chamadas de procedimento remoto de programas cliente.

Para escutar chamadas de procedimento remoto, o programa do servidor deve chamar [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten), conforme mostrado no fragmento de código a seguir:


```C++
RPC_STATUS status;
status = RpcServerListen(
    1,
    RPC_C_LISTEN_MAX_CALLS_DEFAULT,
    0);
```



Um servidor RPC tem um ou mais threads que pegam chamadas de cliente e as entregam às rotinas nas interfaces registradas. O primeiro parâmetro para a função [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) é o número mínimo de threads a serem criados. O parâmetro é apenas uma dica; o tempo de execução RPC pode optar por ignorá-lo.

O segundo parâmetro para [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) é o número máximo de chamadas de procedimento remoto simultâneas a serem manipuladas. Se você quiser que seu aplicativo use o valor máximo padrão, passe RPC \_ C \_ escutar \_ Max \_ calls \_ padrão como o valor para esse parâmetro.

A especificação do DCE chama o [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) para continuar em execução até receber um sinal para parar. Uma extensão da Microsoft para essa função é permitir que ela comece a escutar e retornar imediatamente. Se você quiser que seu aplicativo use o comportamento padrão do DCE, defina o terceiro parâmetro como zero. Consulte [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten), [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening)e [**RpcMgmtWaitServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtwaitserverlisten) para obter detalhes.

 

 




