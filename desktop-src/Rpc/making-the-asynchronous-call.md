---
title: Fazendo a chamada assíncrona
description: Antes de fazer uma chamada remota assíncrona, o cliente deve inicializar o alça assíncrono. Programas cliente e servidor usam ponteiros para a estrutura RPC \_ ASYNC \_ STATE para alças assíncronas.
ms.assetid: b40308ef-88ae-4c80-9118-29c5ffee77ad
keywords:
- RPC de Chamada de Procedimento Remoto , tarefas, fazendo chamadas assíncronas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93d8399071cae6ea39aaac3f966e7e799b2c93b32a152048a7d18282b465f929
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118928372"
---
# <a name="making-the-asynchronous-call"></a>Fazendo a chamada assíncrona

Antes de fazer uma chamada remota assíncrona, o cliente deve inicializar o alça assíncrono. Programas cliente e servidor usam ponteiros para a estrutura [**RPC \_ ASYNC \_ STATE**](/windows/desktop/api/Rpcasync/ns-rpcasync-rpc_async_state) para alças assíncronas.

Cada chamada pendente deve ter seu próprio handle assíncrono exclusivo. O cliente cria o handle e o passa para a [**função RpcAsyncInitializeHandle.**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncinitializehandle) Para que a chamada seja concluída corretamente, o cliente deve garantir que a memória do handle não seja liberada até receber a resposta assíncrona do servidor. Além disso, antes de fazer outra chamada em um alça assíncrono existente, o cliente deve reinicializar o handle. A falha ao fazer isso pode fazer com que o stub do cliente aumente uma exceção durante a chamada. O cliente também deve garantir que os buffers que ele fornece para parâmetros de saída e no , os parâmetros de saída para um procedimento remoto assíncrono permaneçam alocados até que ele tenha recebido a resposta do \[ [](/windows/desktop/Midl/out-idl) \] \[ [](/windows/desktop/Midl/in)  \] servidor.

Quando ele invoca um procedimento remoto assíncrono, o cliente deve selecionar o método que a biblioteca de tempo de execução RPC usará para notificá-lo sobre a conclusão da chamada. O cliente pode receber essa notificação de qualquer uma das seguintes maneiras:

-   Evento. O cliente pode especificar um evento a ser acionado quando a chamada for concluída. Para obter detalhes, consulte [Objetos de evento](/windows/desktop/Sync/event-objects).
-   Executar a sondagem. O cliente pode chamar repetidamente [**RpcAsyncGetCallStatus**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncgetcallstatus). Se o valor de retorno for algo diferente de RPC \_ S \_ ASYNC \_ CALL \_ PENDING, a chamada será concluída. Esse método usa mais tempo de CPU do que os outros métodos descritos aqui.
-   Apc. O cliente pode especificar uma chamada de procedimento [assíncrono (APC)](/windows/desktop/Sync/asynchronous-procedure-calls) que é chamada quando a chamada é concluída. Para o protótipo da função APC, consulte [**RPCNOTIFICATION \_ ROUTINE**](/previous-versions/aa375808(v=vs.80)). O APC é chamado com seu parâmetro Event definido como RpcCallComplete. Para apCs serem expedidos, o thread do cliente deve estar em um estado de espera alertável.

    Se o **campo hThread** no handle assíncrono estiver definido como 0, as APCs serão encruadas no thread que fez a chamada assíncrona. Se for não zero, as APCs serão enquete no thread especificado por m.

-   Ioc. A porta de conclusão de E/S é notificada com os parâmetros especificados no alça assíncrono. Para obter mais informações, [**consulte CreateIoCompletionPort.**](/windows/desktop/FileIO/createiocompletionport)
-   Windows de dados. Uma mensagem é postada no HWND (alça de janela) especificado.

O fragmento de código a seguir mostra as etapas essenciais necessárias para inicializar um alça assíncrono e usá-lo para fazer uma chamada de procedimento remoto assíncrono.


```C++
RPC_ASYNC_STATE Async;
RPC_STATUS status;
 
// Initialize the handle.
status = RpcAsyncInitializeHandle(&Async, sizeof(RPC_ASYNC_STATE));
if (status)
{
    // Code to handle the error goes here.
}
 
Async.UserInfo = NULL;
Async.NotificationType = RpcNotificationTypeEvent;
 
Async.u.hEvent = CreateEvent(NULL, FALSE, FALSE, NULL);
if (Async.u.hEvent == 0)
{
    // Code to handle the error goes here.
}
// Call an asynchronous RPC routine here
RpcTryExcept
{
    printf("\nCalling the remote procedure 'AsyncFunc'\n");
    AsyncFunc(&Async, AsyncRPC_ClientIfHandle, nAsychDelay);
}
RpcExcept(1)
{
    ulCode = RpcExceptionCode();
    printf("AsyncFunc: Run time reported exception 0x%lx = %ld\n", 
            ulCode, ulCode);
}
RpcEndExcept
 
// Call a synchronous routine while
// the asynchronous procedure is still running
RpcTryExcept
{
    printf("\nCalling the remote procedure 'NonAsyncFunc'\n");
    NonAsyncFunc(AsyncRPC_ClientIfHandle, pszMessage);
    fprintf(stderr, 
            "While 'AsyncFunc' is running asynchronously,\n"
            "we still can send message to the server in the mean "
            "time.\n\n");
}
RpcExcept(1)
{
    ulCode = RpcExceptionCode();
    printf("NonAsyncFunc: Run time reported exception 0x%lx = %ld\n", 
            ulCode, ulCode);
}
RpcEndExcept
```



Como este exemplo demonstra, o programa cliente pode executar chamadas de procedimento remoto síncrono enquanto uma chamada de procedimento assíncrono ainda está pendente. Esse cliente cria um objeto de evento para a biblioteca de tempo de executar RPC a ser usada para notificá-lo quando a chamada assíncrona for concluída.

> [!Note]  
> A notificação de conclusão não será retornada de uma rotina RPC assíncrona se uma exceção RPC for gerado durante uma chamada assíncrona.

 

 

 