---
title: Limpeza do lado do servidor
description: Limpeza do lado do servidor e RPC (Chamada de Procedimento Remoto).
ms.assetid: 8a48f698-82ae-464b-bdd9-f0245bbc7733
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 223cd15eb659a62c4a758098e9b0f70e977ebb069a2a305d2909b97b5fb12010
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118925288"
---
# <a name="server-side-cleanup"></a>Limpeza do lado do servidor

Imagine o seguinte cenário:

Um cliente abre um handle de contexto e, em seguida, para ou perde a conectividade com o servidor. Como o servidor detecta que o cliente falhou e o identificador de contexto deve ser executado? Há dois subscenários: um é que o cliente é desligado de maneira organizada. Nesse caso, ele notifica o servidor de que está desligando e o servidor pode limpar, incluindo a execução de run downs de contexto. Se o cliente não for desligado de maneira organizada ou não puder notificar o servidor, o servidor usará keep alives para determinar se o cliente ainda está disponível. No lado do servidor, a [**função RpcMgmtSetComTimeout**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetcomtimeout) não tem nenhum efeito. Em vez disso, o servidor usa a configuração global por computador keep alive, que usa como padrão aproximadamente duas horas. Se o cliente não responder aos keep alives do servidor, a conexão será fechada. Quando todas as conexões com um determinado processo de cliente são fechadas, o servidor limpa e executa os alças de contexto pendentes.

 

 




