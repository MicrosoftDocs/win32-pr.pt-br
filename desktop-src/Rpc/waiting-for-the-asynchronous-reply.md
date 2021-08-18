---
title: Aguardando a resposta assíncrona
description: O que o cliente faz enquanto aguarda ser notificado de uma resposta do servidor depende do mecanismo de notificação que ele seleciona.
ms.assetid: b1d4ea54-26bc-49f9-8cc1-a74fd4ffced3
keywords:
- Chamada de procedimento remoto RPC, tarefas, aguardando respostas assíncronas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff50357402d96c32444f077d07558c01ed93d0367514e947643a28bf3041f204
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010474"
---
# <a name="waiting-for-the-asynchronous-reply"></a>Aguardando a resposta assíncrona

O que o cliente faz enquanto aguarda ser notificado de uma resposta do servidor depende do mecanismo de notificação que ele seleciona.

Se o cliente usar um evento para notificação, ele normalmente chamará a função [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) ou a função [**WaitForSingleObjectEx**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex) . O cliente entra em um estado bloqueado quando chama uma dessas funções. Isso é eficiente porque o cliente não consome ciclos de execução de CPU enquanto está bloqueado.

Quando ele usa a sondagem para aguardar seus resultados, o programa cliente entra em um loop que chama repetidamente a função [**RpcAsyncGetCallStatus**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncgetcallstatus). Esse é um método eficiente de espera se o seu programa cliente faz outro processamento no loop de sondagem. Por exemplo, ele pode preparar dados em pequenas partes para uma chamada de procedimento remoto assíncrona subsequente. Depois que cada parte for concluída, o cliente poderá sondar a chamada de procedimento remoto assíncrona pendente para ver se ela está concluída.

O programa cliente pode fornecer uma APC (chamada de procedimento assíncrono), que é um tipo de função de chamada de retorno que a biblioteca de tempo de execução RPC invocará quando a chamada de procedimento remoto assíncrona for concluída. O programa cliente deve estar em um estado de espera alertável. isso normalmente significa que o cliente chama uma função de API Windows para se colocar em um estado bloqueado. Para obter mais informações, consulte [chamadas de procedimento assíncrono](/windows/desktop/Sync/asynchronous-procedure-calls).

> [!Note]  
> A notificação de conclusão não será retornada de uma rotina RPC assíncrona se uma exceção RPC for gerada durante uma chamada assíncrona.

 

Se o programa cliente usar uma porta de conclusão de e/s para receber a notificação de conclusão, ele deverá chamar a função [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) . Quando isso é feito, ele pode aguardar indefinidamente uma resposta ou continuar a fazer outro processamento. Se ele faz outro processamento enquanto aguarda uma resposta, ele deve sondar a porta de conclusão com a função **GetQueuedCompletionStatus** . Nesse caso, normalmente, ele precisa definir *dwMilliseconds* como zero. Isso faz com que o **GetQueuedCompletionStatus** retorne imediatamente, mesmo que a chamada assíncrona não tenha sido concluída.

Os programas cliente também podem receber a notificação de conclusão por meio de suas filas de mensagens do Windows. nessa situação, eles simplesmente processam a mensagem de conclusão como fariam com qualquer Windows mensagem.

Em um aplicativo multithread, uma chamada assíncrona pode ser cancelada pelo cliente somente depois que o thread que originou a chamada foi retornado com êxito da chamada. Isso garante que a chamada não seja cancelada de forma assíncrona por outro thread após a falha de uma chamada síncrona. Como prática padrão, uma chamada assíncrona que falha de forma síncrona não deve ser cancelada de modo assíncrono. O aplicativo cliente deve observar esse comportamento se as chamadas podem ser emitidas e canceladas em threads diferentes. Além disso, após a chamada ser cancelada, o código do cliente deve aguardar a notificação de conclusão e concluir a chamada. A função [**RpcAsyncCancelCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall) simplesmente recorrendo a notificação de conclusão; Não é um substituto da conclusão da chamada.

O fragmento de código a seguir ilustra como um programa cliente pode usar um evento para aguardar uma resposta assíncrona.


```C++
// This code fragment assumes that Async is a valid asynchronous
// RPC handle.
if (WaitForSingleObject(Async.u.hEvent, INFINITE) == WAIT_FAILED)
{
    RpcRaiseException(APP_ERROR);
}
```



Os programas cliente que usam uma APC para receber notificação de uma resposta assíncrona normalmente se colocam em um estado bloqueado. O fragmento de código a seguir mostra isso.


```C++
if (SleepEx(INFINITE, TRUE) != WAIT_IO_COMPLETION)
{
    RpcRaiseException(APP_ERROR);
}
```



Nesse caso, o programa cliente entra em suspensão, não consumindo ciclos de CPU, até que a biblioteca de tempo de execução RPC chame a APC (não mostrada).

O exemplo a seguir demonstra um cliente que usa uma porta de conclusão de e/s para aguardar uma resposta assíncrona.


```C++
// This code fragment assumes that Async is a valid asynchronous
// RPC handle.
if (!GetQueuedCompletionStatus(
         Async.u.IOC.hIOPort,
         &Async.u.IOC.dwNumberOfBytesTransferred,
         &Async.u.IOC.dwCompletionKey,
         &Async.u.IOC.lpOverlapped,
         INFINITE))
{
    RpcRaiseException(APP_ERROR);
}
```



No exemplo anterior, a chamada para [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) aguarda indefinidamente até que a chamada de procedimento remoto assíncrona seja concluída.

Uma possível armadilha ocorre durante a gravação de aplicativos multithread. Se um thread invocar uma chamada de procedimento remoto e terminar antes de receber a notificação de que o envio foi concluído, a chamada de procedimento remoto poderá falhar e o stub do cliente poderá fechar a conexão com o servidor. Portanto, os threads que chamam um procedimento remoto não devem terminar antes que a chamada seja concluída ou cancelada quando o comportamento for indesejável.

 

 