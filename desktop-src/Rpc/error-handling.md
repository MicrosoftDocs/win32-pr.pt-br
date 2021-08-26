---
title: Tratamento de erro (RPC)
description: Em RPC síncrono, um cliente faz uma chamada remota que retorna com um código de êxito ou falha.
ms.assetid: 7dfc9f84-ce3c-49f3-8f72-b212095133fd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6daf29091602c36a23c0ed7e08eb0459985e13ca26ec128f401754f64c2329ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021655"
---
# <a name="error-handling-rpc"></a>Tratamento de erro (RPC)

Em RPC síncrono, um cliente faz uma chamada remota que retorna com um código de êxito ou falha. O RPC assíncrono fornece mais oportunidades para uma chamada falhar e essas falhas são tratadas de maneira diferente, dependendo de onde e quando elas ocorrem. A tabela a seguir descreve as maneiras pelas quais uma chamada pode falhar e como ela é tratada.

## <a name="client-side-cleanup"></a>Limpeza do lado do cliente



| Sintoma de falha                                                                                                                                  | Limpeza                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| O cliente captura uma exceção quando chama o procedimento remoto.                                                                                  | Nenhuma chamada à API RPC é necessária. Todo o estado RPC foi limpo.                                                              |
| O cliente recebe uma notificação de chamada completa, mas quando chama [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall), ele recebe um código de erro. | Nenhuma chamada à API RPC é necessária. Todo o estado RPC foi limpo.                                                              |
| O cliente emite cancelamento não anulativo ou anulativo.                                                                                                   | O cliente deve aguardar a notificação e [**chamar RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) quando a notificação chegar. |



 

Na limpeza do lado do servidor, um conceito fundamental é o ponto de entrega. Durante o processamento do lado do servidor de uma chamada assíncrona, alguns processamentos geralmente são executados no thread que recebeu a chamada (também conhecido como *thread dispatcher*) e, em seguida, opcionalmente, o thread dispatcher coloca estado suficiente em um bloco de memória e sinaliza outro thread (também conhecido como *thread* de trabalho ) para continuar o processamento para a chamada. O momento em que o thread do dispatcher sinaliza com êxito que o thread de trabalho é chamado *de ponto de entrega*.

## <a name="server-side-cleanup"></a>Limpeza do lado do servidor



| Erro encontrado      | Limpeza                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Antes do ponto de entrega. | Lançar exceção. Nenhuma chamada para [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) é necessária.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Após o ponto de entrega.  | Chame [**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall) ou, se o erro não for fatal e os resultados ainda puderem ser retornados ao cliente, [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall). Se a **chamada de função RpcAsyncCompleteCall** falhar, o runtime RPC liberará os parâmetros. O usuário não deve acessar esses parâmetros. O thread do dispatcher não deve executar nenhum processamento substancial que possa falhar após o ponto de entrega, pois ele não pode mais anular com segurança a chamada. Especificamente, ele não deve lançar uma exceção após o ponto de entrega ou o servidor pode falhar. |



 

## <a name="special-error-handling-cases-for-pipes"></a>Casos especiais de tratamento de erros para pipes

Há casos especiais para tratamento de erros ao usar pipes. A lista a seguir explica a origem da falha e como tratar o erro.



| Origem da falha                                                                                                 | Como foi tratado                                                                                                |
|-------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| O cliente chama push e a chamada falha.                                                                             | Nenhuma chamada à API RPC é necessária. Todo o estado RPC foi limpo.                                         |
| O cliente [**chama RpcAsyncCompleteCall antes**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) que [**os pipes**](/windows/desktop/Midl/in) em sejam esvaziados. | A chamada falha com o código de erro de preenchimento de pipe apropriado.                                                   |
| O cliente chama pull e a chamada falha.                                                                             | Nenhuma chamada à API RPC é necessária. Todo o estado RPC foi limpo.                                         |
| O cliente ou o servidor chama push ou pull na ordem errada.                                                    | O tempo de executar retorna o status do erro de preenchimento de pipe.                                                                |
| O servidor chama push ou pull e a chamada falha.                                                                     | Push retorna um código de falha. Nenhuma chamada para [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) é necessária. |
| O servidor **chama RpcAsyncCompleteCall** antes que os pipes tenham sido esvaziados.                                         | A chamada de pipe retorna um status de erro de preenchimento de pipe.                                                         |
| Após a expedição, uma operação de recebimento falha.                                                                    | Na próxima vez que o servidor chamar pull para receber dados de pipe, um erro será retornado.                            |



 

 

 
