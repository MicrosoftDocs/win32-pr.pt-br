---
title: Interrompendo o aplicativo de servidor
description: Um aplicativo de servidor pode parar de escutar clientes chamando RpcMgmtStopServerListening e RpcServerUnregisterIf ou simplesmente saindo do processo de host.
ms.assetid: 9d310cfb-72ad-448f-a66a-db6ac2478824
keywords:
- RPC de Chamada de Procedimento Remoto , tarefas, parando o aplicativo de servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a83f0a96732b1c862cf3e00d25cc2d2d9caf27ae5d764a9edab00c78aaf18682
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118925136"
---
# <a name="stopping-the-server-application"></a>Interrompendo o aplicativo de servidor

Um aplicativo de servidor pode parar de escutar clientes chamando [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) e [**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif)ou simplesmente saindo do processo de host. Ambos os métodos são aceitáveis. Se o servidor seguir a primeira abordagem, ele deverá implementar as seguintes etapas:

A função de servidor [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) não retorna ao programa de chamada até que ocorra uma exceção ou até que ocorra uma chamada para [**RpcMgmtStopServerListening.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) Por padrão, somente outro thread de servidor tem permissão para interromper o servidor RPC usando **RpcMgmtStopServerListening**. Os clientes que tentarem interromper o servidor receberão o erro ACESSO \_ NEGADO do RPC. \_ \_ No entanto, é possível configurar o RPC para permitir que alguns ou todos os clientes parem o servidor. Consulte **RpcMgmtStopServerListening para** obter detalhes.

Você também pode fazer com que o aplicativo cliente faça uma chamada de procedimento remoto para uma rotina de desligamento no servidor. A rotina de desligamento [**chama RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) e [**RpcServerUnregisterIf.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif) Este aplicativo de programa de exemplo de tutorial usa essa abordagem adicionando uma nova função remota, **Shutdown**, ao arquivo Hellop.c.

Na função **Shutdown,** o parâmetro nulo único para [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) indica que o aplicativo local deve parar de escutar chamadas de procedimento remoto. Os dois parâmetros nulos para [**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif) são curingas, indicando que todas as interfaces devem estar sem registro. O **parâmetro FALSE** indica que a interface deve ser removida do Registro imediatamente, em vez de aguardar a conclusão das chamadas pendentes.


```C++
/* add this function to hellop.c */
void Shutdown(void)
{
    RPC_STATUS status;
 
    status = RpcMgmtStopServerListening(NULL);
 
    if (status) 
    {
       exit(status);
    }
 
    status = RpcServerUnregisterIf(NULL, NULL, FALSE);
 
    if (status) 
    {
       exit(status);
    }
} //end Shutdown
```



 

 




