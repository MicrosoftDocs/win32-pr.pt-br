---
title: Limpeza no lado do servidor
description: Limpeza do lado do servidor e RPC (chamada de procedimento remoto).
ms.assetid: 8a48f698-82ae-464b-bdd9-f0245bbc7733
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72a66272fc3cca209d6825ac34d5158094ddff39
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005777"
---
# <a name="server-side-cleanup"></a>Limpeza no lado do servidor

Imagine o seguinte cenário:

Um cliente abre um identificador de contexto e, em seguida, interrompe ou perde a conectividade com o servidor. Como o servidor detecta que o cliente falhou e o identificador de contexto deve ser executado? Há dois subcenários: um é que o cliente é desligado de maneira ordenada. Nesse caso, ele notifica o servidor de que ele está sendo desligado e o servidor pode ser limpo, incluindo a execução de um contexto. Se o cliente não desligar de maneira ordenada ou não puder notificar o servidor, o servidor usará o Keep Alive para determinar se o cliente ainda está disponível. No lado do servidor, a função [**RpcMgmtSetComTimeout**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetcomtimeout) não tem nenhum efeito. Em vez disso, o servidor usa a configuração global por máquina – Keep Alive, cujo padrão é aproximadamente duas horas. Se o cliente não responder à Keep Alive do servidor, a conexão será fechada. Quando todas as conexões com um determinado processo de cliente são fechadas, o servidor limpa e executa identificadores de contexto pendentes.

 

 




