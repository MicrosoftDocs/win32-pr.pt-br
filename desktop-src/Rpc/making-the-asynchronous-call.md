---
title: Fazendo a chamada assíncrona
description: Antes de poder fazer uma chamada remota assíncrona, o cliente deve inicializar o identificador assíncrono. Os programas cliente e servidor usam ponteiros para \_ a \_ estrutura de estado assíncrono RPC para identificadores assíncronos.
ms.assetid: b40308ef-88ae-4c80-9118-29c5ffee77ad
keywords:
- Chamada de procedimento remoto RPC, tarefas, fazendo chamadas assíncronas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa06f60b43a7dff3a29223ff1d8e9ad726c0e938
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105778523"
---
# <a name="making-the-asynchronous-call"></a>Fazendo a chamada assíncrona

Antes de poder fazer uma chamada remota assíncrona, o cliente deve inicializar o identificador assíncrono. Os programas cliente e servidor usam ponteiros para a estrutura de [**\_ \_ estado assíncrono RPC**](/windows/desktop/api/Rpcasync/ns-rpcasync-rpc_async_state) para identificadores assíncronos.

Cada chamada pendente deve ter seu próprio identificador assíncrono exclusivo. O cliente cria o identificador e o passa para a função [**RpcAsyncInitializeHandle**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncinitializehandle) . Para que a chamada seja concluída corretamente, o cliente deve garantir que a memória do identificador não seja liberada até receber a resposta assíncrona do servidor. Além disso, antes de fazer outra chamada em um identificador assíncrono existente, o cliente deve reinicializar o identificador. A falha em fazer isso pode fazer com que o stub do cliente gere uma exceção durante a chamada. O cliente também deve garantir que os buffers que ele fornece para parâmetros de \[ [**saída**](/windows/desktop/Midl/out-idl) \] e os \[ parâmetros [**de**](/windows/desktop/Midl/in) **saída** \] para um procedimento remoto assíncrono permaneçam alocados até que ele tenha recebido a resposta do servidor.

Quando ele invoca um procedimento remoto assíncrono, o cliente deve selecionar o método que a biblioteca de tempo de execução RPC usará para notificá-lo da conclusão da chamada. O cliente pode receber essa notificação em qualquer uma das seguintes maneiras:

-   Circunstância. O cliente pode especificar um evento a ser acionado quando a chamada for concluída. Para obter detalhes, consulte [objetos de evento](/windows/desktop/Sync/event-objects).
-   Executar a sondagem. O cliente pode chamar repetidamente [**RpcAsyncGetCallStatus**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncgetcallstatus). Se o valor de retorno for algo diferente da \_ \_ chamada assíncrona de RPC S \_ \_ pendente, a chamada será concluída. Esse método usa mais tempo de CPU do que os outros métodos descritos aqui.
-   APC. O cliente pode especificar uma [APC (chamada de procedimento assíncrono)](/windows/desktop/Sync/asynchronous-procedure-calls) que é chamada quando a chamada é concluída. Para o protótipo da função APC, consulte [**\_ rotina RPCNOTIFICATION**](/previous-versions/aa375808(v=vs.80)). A APC é chamada com seu parâmetro de evento definido como RpcCallComplete. Para que o APCs seja expedido, o thread do cliente deve estar em um estado de espera alertável.

    Se o campo **hThread** no identificador assíncrono for definido como 0, os APCs serão enfileirados no thread que fez a chamada assíncrona. Se ele for diferente de zero, os APCs serão enfileirados no thread especificado por m.

-   IOC. A porta de conclusão de e/s é notificada com os parâmetros especificados no identificador assíncrono. Para obter mais informações, consulte [**CreateIoCompletionPort**](/windows/desktop/FileIO/createiocompletionport).
-   Identificador do Windows. Uma mensagem é postada para o identificador de janela especificado (HWND).

O fragmento de código a seguir mostra as etapas essenciais necessárias para inicializar um identificador assíncrono e usá-lo para fazer uma chamada de procedimento remoto assíncrona.


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



Como demonstra este exemplo, o programa cliente pode executar chamadas síncronas de procedimento remoto enquanto uma chamada de procedimento assíncrono ainda está pendente. Esse cliente cria um objeto de evento para a biblioteca de tempo de execução RPC a ser usada para notificá-lo quando a chamada assíncrona for concluída.

> [!Note]  
> A notificação de conclusão não será retornada de uma rotina RPC assíncrona se uma exceção RPC for gerada durante uma chamada assíncrona.

 

 

 