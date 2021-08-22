---
title: Escutando chamadas de cliente
description: Depois que seu aplicativo de servidor registrar suas interfaces, criar as informações de associação necessárias e registrar seus pontos de extremidade, ele estará pronto para começar a escutar chamadas de procedimento remoto de programas cliente.
ms.assetid: ca9d24ed-0acc-45de-bbb2-761c56745a58
keywords:
- RPC de Chamada de Procedimento Remoto , tarefas, escutando chamadas de cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62f94453a3250cfc1adae72aa0af96297a741beb501839f7f7831e3f88a8c218
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118928601"
---
# <a name="listening-for-client-calls"></a>Escutando chamadas de cliente

Depois que seu aplicativo de servidor registrar suas interfaces, criar as informações de associação necessárias e registrar seus pontos de extremidade, ele estará pronto para começar a escutar chamadas de procedimento remoto de programas cliente.

Para escutar chamadas de procedimento remoto, seu programa de servidor deve chamar [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten), conforme mostrado no seguinte fragmento de código:


```C++
RPC_STATUS status;
status = RpcServerListen(
    1,
    RPC_C_LISTEN_MAX_CALLS_DEFAULT,
    0);
```



Um servidor RPC tem um ou mais threads que escolhem chamadas de cliente e as entregam às rotinas nas interfaces registradas. O primeiro parâmetro para a [**função RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) é o número mínimo de threads a criar. O parâmetro é apenas uma dica; o tempo de executar RPC pode optar por ignorá-lo.

O segundo parâmetro para [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) é o número máximo de chamadas de procedimento remoto simultâneas para manipular. Se você quiser que seu aplicativo use o valor máximo padrão, passe RPC C LISTEN MAX CALLS DEFAULT como o \_ \_ valor para esse \_ \_ \_ parâmetro.

A especificação DCE exige [**que RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) continue em execução até receber um sinal para parar. Uma extensão da Microsoft para essa função é permitir que ela comece a escutar e retornar imediatamente. Se você quiser que seu aplicativo use o comportamento de DCE padrão, de definido o terceiro parâmetro como zero. Consulte [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten), [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening)e [**RpcMgmtWaitServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtwaitserverlisten) para obter detalhes.

 

 




