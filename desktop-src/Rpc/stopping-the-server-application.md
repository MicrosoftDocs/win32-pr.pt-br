---
title: Parando o aplicativo de servidor
description: Um aplicativo de servidor pode parar de escutar clientes chamando RpcMgmtStopServerListening e RpcServerUnregisterIf ou simplesmente saindo do processo de host.
ms.assetid: 9d310cfb-72ad-448f-a66a-db6ac2478824
keywords:
- Chamada de procedimento remoto RPC, tarefas, parando o aplicativo de servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31f95ba05588e0575949614e05370f86de78207d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636962"
---
# <a name="stopping-the-server-application"></a>Parando o aplicativo de servidor

Um aplicativo de servidor pode parar de escutar clientes chamando [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) e [**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif)ou simplesmente saindo do processo de host. Ambos os métodos são aceitáveis. Se o servidor seguir a primeira abordagem, ele deverá implementar as seguintes etapas:

A função de servidor [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) não retorna ao programa de chamada até que ocorra uma exceção ou até que ocorra uma chamada para [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) . Por padrão, somente outro thread do servidor tem permissão para interromper o servidor RPC usando **RpcMgmtStopServerListening**. Os clientes que tentarem interromper o servidor receberão o erro \_ acesso a RPC S \_ \_ negado. No entanto, é possível configurar o RPC para permitir que alguns ou todos os clientes interrompam o servidor. Consulte **RpcMgmtStopServerListening** para obter detalhes.

Você também pode fazer com que o aplicativo cliente faça uma chamada de procedimento remoto para uma rotina de desligamento no servidor. A rotina de desligamento chama [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) e [**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif). Este exemplo de aplicativo de programa de tutorial usa essa abordagem adicionando uma nova função remota, **desligada**, ao arquivo Hellop. c.

Na função de **desligamento** , o único parâmetro nulo para [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) indica que o aplicativo local deve parar de escutar chamadas de procedimento remotas. Os dois parâmetros nulos para [**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif) são curingas, indicando que todas as interfaces devem ter o registro cancelado. O parâmetro **false** indica que a interface deve ser removida do registro imediatamente, em vez de esperar que as chamadas pendentes sejam concluídas.


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



 

 




