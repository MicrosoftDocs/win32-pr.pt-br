---
title: Enviando a resposta assíncrona
description: Quando a chamada assíncrona é concluída, o servidor envia uma resposta ao cliente chamando a função RpcAsyncCompleteCall e passando-a para o identificador assíncrono.
ms.assetid: 458bc476-963e-4812-b4c2-9074ff0a8284
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06f861c3f2a1befdb85435f5275176c82e23bb06
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005969"
---
# <a name="sending-the-asynchronous-reply"></a>Enviando a resposta assíncrona

Quando a chamada assíncrona é concluída, o servidor envia uma resposta ao cliente chamando a função [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) e passando-a para o identificador assíncrono. Essa chamada é necessária mesmo se a chamada assíncrona tiver um valor de retorno void e nenhum \[ \] parâmetro out. Se a função tiver um valor de retorno, ela será passada por referência a **RpcAsyncCompleteCall**.

Quando o servidor chama [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) ou **RpcAsyncAbortCall**, ou uma chamada é concluída porque uma exceção foi gerada na rotina Server-Manager, a biblioteca de tempo de execução RPC destrói automaticamente o identificador assíncrono do servidor.

> [!Note]  
> O servidor deve concluir a atualização dos \[ parâmetros in, out \] e \[ out \] antes de chamar **RpcAsyncCompleteCall**. Nenhuma alteração pode ser feita nesses parâmetros ou no identificador assíncrono após chamar **RpcAsyncCompleteCall**. Se a chamada de função **RpcAsyncCompleteCall** falhar, o tempo de execução RPC liberará os parâmetros.

 

O exemplo a seguir demonstra uma chamada de procedimento assíncrono simples.


```C++
#define DEFAULT_ASYNC_DELAY 20;
#define ASYNC_CANCEL_CHECK 100;

void AsyncFunc(IN PRPC_ASYNC_STATE pAsync,
               IN RPC_BINDING_HANDLE hBinding,
               IN OUT unsigned long nAsychDelay)
{
    int nReply = 1;
    RPC_STATUS status;
    unsigned long nTmpAsychDelay;
    int i;
 
    if (nAsychDelay < 0){
        nAsychDelay = DEFAULT_ASYNC_DELAY;
    }else if (nAsychDelay < 100){
        nAsychDelay = 100;
    }

    // We only call RpcServerTestCancel if the call
    // takes longer than ASYNC_CANCEL_CHECK ms
    if(nAsychDelay > ASYNC_CANCEL_CHECK){
        
        nTmpAsychDelay = nAsychDelay/100;
 
        for (i = 0; i < 100; i++){
            Sleep(nTmpAsychDelay);
 
            if (i%5 == 0){
                fprintf(stderr, 
                        "\rRunning AsyncFunc (%lu ms) (%d%c) ... ",
                        nAsychDelay, i+5, PERCENT);
 
                status = 
                    RpcServerTestCancel(
                        RpcAsyncGetCallHandle(pAsync));
                if (status == RPC_S_OK){
                    fprintf(stderr, 
                            "\nAsyncFunc has been canceled!!!\n");
                    break;
                }else if (status != RPC_S_CALL_IN_PROGRESS){
                    printf(
                        "RpcAsyncInitializeHandle returned 0x%x\n", 
                        status);
                    exit(status); 
                }
            }
        }
    }else{
        Sleep(nAsychDelay);
    }
 
    printf("\nCalling RpcAsyncCompleteCall\n");
    status = RpcAsyncCompleteCall(pAsync, &nReply);
    printf("RpcAsyncCompleteCall returned 0x%x\n", status);
    if (status){
        exit(status);
    }
}
```



Para simplificar, essa rotina assíncrona de servidor não processa dados reais. Ele simplesmente se coloca em suspensão por algum tempo.

> [!Note]  
> A função **RpcAsyncCompleteCall** pode ser chamada no thread que recebeu a chamada ou em qualquer outro thread no processo. Se todos os dados necessários para concluir a chamada estiverem prontamente disponíveis, o servidor poderá preenchê-los no mesmo thread e chamar o **RpcAsyncCompleteCall** no mesmo thread. Essa abordagem salva alguma alternância de contexto e melhora o desempenho. Essas chamadas são chamadas assíncronas de forma oportuna.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**\_estado assíncrono de RPC \_**](/windows/desktop/api/Rpcasync/ns-rpcasync-rpc_async_state)
</dt> <dt>

[**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall)
</dt> <dt>

[**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall)
</dt> <dt>

[**RpcServerTestCancel**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcservertestcancel)
</dt> </dl>

 

 




