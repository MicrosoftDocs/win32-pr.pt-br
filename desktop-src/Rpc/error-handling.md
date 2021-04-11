---
title: Tratamento de erro (RPC)
description: No RPC síncrono, um cliente faz uma chamada remota que retorna com um código de êxito ou de falha.
ms.assetid: 7dfc9f84-ce3c-49f3-8f72-b212095133fd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 017892b94438cc73f88cbfe60c03c088bf3ebcc9
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104008772"
---
# <a name="error-handling-rpc"></a>Tratamento de erro (RPC)

No RPC síncrono, um cliente faz uma chamada remota que retorna com um código de êxito ou de falha. O RPC assíncrono fornece mais oportunidades para uma chamada falhar e essas falhas são tratadas de forma diferente, dependendo de onde e quando elas ocorrem. A tabela a seguir descreve as maneiras em que uma chamada pode falhar e como ela é manipulada.

## <a name="client-side-cleanup"></a>Limpeza do lado do cliente



| Sintoma de falha                                                                                                                                  | Limpeza                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| O cliente captura uma exceção ao chamar o procedimento remoto.                                                                                  | Não são necessárias chamadas à API RPC. Todo o estado de RPC foi limpo.                                                              |
| O cliente recebe uma notificação de chamada completa, mas quando chama [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall), ele recebe um código de erro. | Não são necessárias chamadas à API RPC. Todo o estado de RPC foi limpo.                                                              |
| O cliente emite um cancelamento não anulado ou anulado.                                                                                                   | O cliente deve aguardar a notificação e chamar [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) quando a notificação chegar. |



 

Na limpeza do lado do servidor, um conceito fundamental é o ponto de distribuição. Durante o processamento do lado do servidor de uma chamada assíncrona, um processamento geralmente é executado no thread que recebeu a chamada (também conhecida como *thread Dispatcher*) e, opcionalmente, o thread Dispatcher coloca o estado suficiente em um bloco de memória e sinaliza outro thread (também conhecido como *thread de trabalho*) para continuar o processamento para a chamada. O momento em que o thread Dispatcher sinaliza com êxito que o thread de trabalho é chamado de *ponto de entrega*.

## <a name="server-side-cleanup"></a>Limpeza do lado do servidor



| Erro encontrado      | Limpeza                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Antes do ponto de distribuição. | Exceção de geração. Nenhuma chamada para [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) é necessária.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Após o ponto de entrega.  | Chame [**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall) ou, se o erro não for fatal, e os resultados ainda poderão ser retornados ao cliente, [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall). Se a chamada de função **RpcAsyncCompleteCall** falhar, o tempo de execução RPC liberará os parâmetros. O usuário não deve acessar esses parâmetros. O thread do Dispatcher não deve executar nenhum processamento substancial que possa falhar após o ponto de desligamento, porque ele não pode mais anular a chamada com segurança. Especificamente, ele não deve lançar uma exceção após o ponto de desligamento ou o servidor pode falhar. |



 

## <a name="special-error-handling-cases-for-pipes"></a>Casos de tratamento de erros especiais para pipes

Há casos especiais para tratamento de erros ao usar pipes. A lista a seguir explica a origem da falha e como tratar o erro.



| Origem da falha                                                                                                 | Como Tratado                                                                                                |
|-------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| O cliente chama push e a chamada falha.                                                                             | Não são necessárias chamadas à API RPC. Todo o estado de RPC foi limpo.                                         |
| O cliente chama [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) antes de os pipes [**em**](/windows/desktop/Midl/in) serem descarregados. | A chamada falha com o código de erro de preenchimento de pipe apropriado.                                                   |
| O cliente chama pull e a chamada falha.                                                                             | Não são necessárias chamadas à API RPC. Todo o estado de RPC foi limpo.                                         |
| O cliente ou o servidor chama Push ou pull na ordem errada.                                                    | Tempo de execução retorna o status de erro de preenchimento de pipe.                                                                |
| O servidor chama Push ou pull e a chamada falha.                                                                     | Push retorna um código de falha. Nenhuma chamada para [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) é necessária. |
| O servidor chama **RpcAsyncCompleteCall** antes que os pipes sejam drenados.                                         | A chamada de pipe retorna um status de erro de preenchimento de pipe.                                                         |
| Após a expedição, uma operação de recebimento falhará.                                                                    | Na próxima vez que o servidor chamar pull para receber dados do pipe, um erro será retornado.                            |



 

 

 
