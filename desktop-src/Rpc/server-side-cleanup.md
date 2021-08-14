---
title: Limpeza no lado do servidor
description: Limpeza do lado do servidor e RPC (chamada de procedimento remoto).
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
# <a name="server-side-cleanup"></a>Limpeza no lado do servidor

Imagine o cenário a seguir:

Um cliente abre um identificador de contexto e, em seguida, interrompe ou perde a conectividade com o servidor. Como o servidor detecta que o cliente falhou e o identificador de contexto deve ser executado? Há dois subcenários: um é que o cliente é desligado de maneira ordenada. Nesse caso, ele notifica o servidor de que ele está sendo desligado e o servidor pode ser limpo, incluindo a execução de um contexto. Se o cliente não desligar de maneira ordenada ou não puder notificar o servidor, o servidor usará o Keep Alive para determinar se o cliente ainda está disponível. No lado do servidor, a função [**RpcMgmtSetComTimeout**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetcomtimeout) não tem nenhum efeito. Em vez disso, o servidor usa a configuração global por máquina – Keep Alive, cujo padrão é aproximadamente duas horas. Se o cliente não responder à Keep Alive do servidor, a conexão será fechada. Quando todas as conexões com um determinado processo de cliente são fechadas, o servidor limpa e executa identificadores de contexto pendentes.

 

 




