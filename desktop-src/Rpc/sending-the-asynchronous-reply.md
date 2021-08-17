---
title: Enviando a resposta assíncrona
description: Quando a chamada assíncrona for concluída, o servidor enviará uma resposta ao cliente chamando a função RpcAsyncCompleteCall e passando a ela o alça assíncrono.
ms.assetid: 458bc476-963e-4812-b4c2-9074ff0a8284
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdcaf4db4a27a49a8025596668893518c6b6c577a0d81d91189a44ec81df4de6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118925574"
---
# <a name="sending-the-asynchronous-reply"></a>Enviando a resposta assíncrona

Quando a chamada assíncrona for concluída, o servidor enviará uma resposta ao cliente chamando a função [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) e passando a ela o alça assíncrono. Essa chamada é necessária mesmo que a chamada assíncrona tenha um valor de retorno nulo e nenhum \[ \] parâmetro out. Se a função tiver um valor de retorno, ela será passada por referência para **RpcAsyncCompleteCall**.

Quando o servidor chama [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) ou **RpcAsyncAbortCall** ou uma chamada é concluída porque uma exceção foi criada na rotina do gerenciador de servidores, a biblioteca em tempo de executar RPC destrói automaticamente o alça assíncrono do servidor.

> [!Note]  
> O servidor deve concluir a atualização dos \[ parâmetros in, out \] e out antes de chamar \[ \] **RpcAsyncCompleteCall**. Nenhuma alteração pode ser feita nesses parâmetros ou no alçamento assíncrono depois de chamar **RpcAsyncCompleteCall**. Se a **chamada de função RpcAsyncCompleteCall** falhar, o runtime RPC liberará os parâmetros.

 

O exemplo a seguir demonstra uma chamada simples de procedimento assíncrono.


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



Para simplificar, essa rotina de servidor assíncrona não processa dados reais. Ele simplesmente se coloca em sleep por algum tempo.

> [!Note]  
> A **função RpcAsyncCompleteCall** pode ser chamada no thread que recebeu a chamada ou em qualquer outro thread no processo. Se todos os dados necessários para concluir a chamada estão prontamente disponíveis, o servidor pode preenchê-los no mesmo thread e chamar **RpcAsyncCompleteCall** no mesmo thread. Essa abordagem salva algumas alternações de contexto e melhora o desempenho. Essas chamadas são chamadas de forma oportunista assíncrona.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**ESTADO \_ ASSÍNCRONO \_ RPC**](/windows/desktop/api/Rpcasync/ns-rpcasync-rpc_async_state)
</dt> <dt>

[**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall)
</dt> <dt>

[**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall)
</dt> <dt>

[**RpcServerTestCancel**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcservertestcancel)
</dt> </dl>

 

 




