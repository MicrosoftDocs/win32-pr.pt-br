---
title: Manipulando chamadas assíncronas
description: A rotina Manager de uma função assíncrona sempre recebe o identificador assíncrono como o primeiro parâmetro. O servidor deve manter o controle desse identificador e usá-lo para enviar a resposta quando a chamada de procedimento remoto assíncrona for concluída.
ms.assetid: 4f38b68b-0bea-4fa7-8c7e-dd09e7daf8bf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e04dc7feed0d7bee47f6fa51583cf8de3a8e42f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364111"
---
# <a name="handling-asynchronous-calls"></a>Manipulando chamadas assíncronas

A rotina Manager de uma função assíncrona sempre recebe o identificador assíncrono como o primeiro parâmetro. O servidor deve manter o controle desse identificador e usá-lo para enviar a resposta quando a chamada de procedimento remoto assíncrona for concluída.

Se o servidor precisar anular um RPC assíncrono, ele chamará [**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall). Essa função executa a mesma limpeza do lado do servidor como [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) e propaga um código de exceção (fornecido pelo aplicativo de servidor) de volta para o cliente, exceto que ele não executa o marshaling dos argumentos de saída.

Para obter um exemplo de um procedimento assíncrono, consulte [enviando a resposta assíncrona](sending-the-asynchronous-reply.md).

 

 




