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
# <a name="sending-the-asynchronous-reply"></a><span data-ttu-id="debad-103">Enviando a resposta assíncrona</span><span class="sxs-lookup"><span data-stu-id="debad-103">Sending the Asynchronous Reply</span></span>

<span data-ttu-id="debad-104">Quando a chamada assíncrona é concluída, o servidor envia uma resposta ao cliente chamando a função [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) e passando-a para o identificador assíncrono.</span><span class="sxs-lookup"><span data-stu-id="debad-104">When the asynchronous call is complete, the server sends a reply to the client by calling the [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) function and passing it the asynchronous handle.</span></span> <span data-ttu-id="debad-105">Essa chamada é necessária mesmo se a chamada assíncrona tiver um valor de retorno void e nenhum \[ \] parâmetro out.</span><span class="sxs-lookup"><span data-stu-id="debad-105">This call is necessary even if the asynchronous call has a void return value and no \[out\] parameters.</span></span> <span data-ttu-id="debad-106">Se a função tiver um valor de retorno, ela será passada por referência a **RpcAsyncCompleteCall**.</span><span class="sxs-lookup"><span data-stu-id="debad-106">If the function has a return value, it is passed by reference to **RpcAsyncCompleteCall**.</span></span>

<span data-ttu-id="debad-107">Quando o servidor chama [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) ou **RpcAsyncAbortCall**, ou uma chamada é concluída porque uma exceção foi gerada na rotina Server-Manager, a biblioteca de tempo de execução RPC destrói automaticamente o identificador assíncrono do servidor.</span><span class="sxs-lookup"><span data-stu-id="debad-107">When the server calls [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) or **RpcAsyncAbortCall**, or a call completes because an exception was raised in the server-manager routine, the RPC run-time library automatically destroys the server's asynchronous handle.</span></span>

> [!Note]  
> <span data-ttu-id="debad-108">O servidor deve concluir a atualização dos \[ parâmetros in, out \] e \[ out \] antes de chamar **RpcAsyncCompleteCall**.</span><span class="sxs-lookup"><span data-stu-id="debad-108">The server must finish updating the \[in, out\] and \[out\] parameters before calling **RpcAsyncCompleteCall**.</span></span> <span data-ttu-id="debad-109">Nenhuma alteração pode ser feita nesses parâmetros ou no identificador assíncrono após chamar **RpcAsyncCompleteCall**.</span><span class="sxs-lookup"><span data-stu-id="debad-109">No changes can be made to those parameters or to the asynchronous handle after calling **RpcAsyncCompleteCall**.</span></span> <span data-ttu-id="debad-110">Se a chamada de função **RpcAsyncCompleteCall** falhar, o tempo de execução RPC liberará os parâmetros.</span><span class="sxs-lookup"><span data-stu-id="debad-110">If the **RpcAsyncCompleteCall** function call fails, the RPC runtime frees the parameters.</span></span>

 

<span data-ttu-id="debad-111">O exemplo a seguir demonstra uma chamada de procedimento assíncrono simples.</span><span class="sxs-lookup"><span data-stu-id="debad-111">The following example demonstrates a simple asynchronous procedure call.</span></span>


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



<span data-ttu-id="debad-112">Para simplificar, essa rotina assíncrona de servidor não processa dados reais.</span><span class="sxs-lookup"><span data-stu-id="debad-112">For the sake of simplicity, this asynchronous server routine does not process actual data.</span></span> <span data-ttu-id="debad-113">Ele simplesmente se coloca em suspensão por algum tempo.</span><span class="sxs-lookup"><span data-stu-id="debad-113">It simply puts itself to sleep for awhile.</span></span>

> [!Note]  
> <span data-ttu-id="debad-114">A função **RpcAsyncCompleteCall** pode ser chamada no thread que recebeu a chamada ou em qualquer outro thread no processo.</span><span class="sxs-lookup"><span data-stu-id="debad-114">The **RpcAsyncCompleteCall** function can be called either on the thread that received the call, or on any other thread in the process.</span></span> <span data-ttu-id="debad-115">Se todos os dados necessários para concluir a chamada estiverem prontamente disponíveis, o servidor poderá preenchê-los no mesmo thread e chamar o **RpcAsyncCompleteCall** no mesmo thread.</span><span class="sxs-lookup"><span data-stu-id="debad-115">If all the data necessary to complete the call are readily available, the server may fill them in on the same thread, and call the **RpcAsyncCompleteCall** on the same thread.</span></span> <span data-ttu-id="debad-116">Essa abordagem salva alguma alternância de contexto e melhora o desempenho.</span><span class="sxs-lookup"><span data-stu-id="debad-116">This approach saves some context switching and improves performance.</span></span> <span data-ttu-id="debad-117">Essas chamadas são chamadas assíncronas de forma oportuna.</span><span class="sxs-lookup"><span data-stu-id="debad-117">Such calls are called opportunistically asynchronous.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="debad-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="debad-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="debad-119">**\_estado assíncrono de RPC \_**</span><span class="sxs-lookup"><span data-stu-id="debad-119">**RPC\_ASYNC\_STATE**</span></span>](/windows/desktop/api/Rpcasync/ns-rpcasync-rpc_async_state)
</dt> <dt>

[<span data-ttu-id="debad-120">**RpcAsyncCompleteCall**</span><span class="sxs-lookup"><span data-stu-id="debad-120">**RpcAsyncCompleteCall**</span></span>](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall)
</dt> <dt>

[<span data-ttu-id="debad-121">**RpcAsyncAbortCall**</span><span class="sxs-lookup"><span data-stu-id="debad-121">**RpcAsyncAbortCall**</span></span>](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall)
</dt> <dt>

[<span data-ttu-id="debad-122">**RpcServerTestCancel**</span><span class="sxs-lookup"><span data-stu-id="debad-122">**RpcServerTestCancel**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcservertestcancel)
</dt> </dl>

 

 




