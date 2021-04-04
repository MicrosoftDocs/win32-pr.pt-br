---
title: Manipulação de pipes assíncronos do lado do servidor
description: A rotina Manager de uma função assíncrona sempre recebe o identificador assíncrono como o primeiro parâmetro.
ms.assetid: ddf9c319-6c4d-4de1-ab29-0ef9b76531ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2b0f11372090f1fd181c0d7272aa1446e5e3d22
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007657"
---
# <a name="server-side-asynchronous-pipe-handling"></a><span data-ttu-id="a3e7b-103">Manipulação de pipes assíncronos do lado do servidor</span><span class="sxs-lookup"><span data-stu-id="a3e7b-103">Server-side Asynchronous Pipe Handling</span></span>

<span data-ttu-id="a3e7b-104">A rotina Manager de uma função assíncrona sempre recebe o identificador assíncrono como o primeiro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="a3e7b-104">The manager routine of an asynchronous function always receives the asynchronous handle as the first parameter.</span></span> <span data-ttu-id="a3e7b-105">O servidor usa esse identificador para enviar a resposta e enviar os dados de pipe de saída conforme eles ficam disponíveis.</span><span class="sxs-lookup"><span data-stu-id="a3e7b-105">The server uses this handle to send the reply and to send the out pipe data as it becomes available.</span></span> <span data-ttu-id="a3e7b-106">O identificador permanece válido até que [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) seja chamado nele, a chamada é anulada por [**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall)ou uma exceção ocorre na rotina do Gerenciador.</span><span class="sxs-lookup"><span data-stu-id="a3e7b-106">The handle remains valid until [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) is called on it, the call is aborted by [**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall), or an exception occurs in the manager routine.</span></span> <span data-ttu-id="a3e7b-107">O aplicativo deve manter o controle de todos os ponteiros de nível superior para os \[ parâmetros **out** \] e \[ **in, out** \] para atualizá-los antes de concluir a chamada.</span><span class="sxs-lookup"><span data-stu-id="a3e7b-107">The application must keep track of all top-level pointers for the \[**out**\] and \[**in, out**\] parameters, in order to update them before completing the call.</span></span> <span data-ttu-id="a3e7b-108">O aplicativo também deve manter o controle dos \[ [](/windows/desktop/Midl/in) \] pipes de entrada e \[ [**saída**](/windows/desktop/Midl/out-idl) \] .</span><span class="sxs-lookup"><span data-stu-id="a3e7b-108">The application must also keep track of the \[[**in**](/windows/desktop/Midl/in)\] and \[[**out**](/windows/desktop/Midl/out-idl)\] pipes.</span></span>

<span data-ttu-id="a3e7b-109">O servidor envia dados de pipe assíncrono da mesma maneira que o cliente.</span><span class="sxs-lookup"><span data-stu-id="a3e7b-109">The server sends asynchronous pipe data in the same manner as the client.</span></span> <span data-ttu-id="a3e7b-110">Consulte [manipulação de pipes assíncronos do lado do cliente](client-side-asynchronous-pipe-handling.md).</span><span class="sxs-lookup"><span data-stu-id="a3e7b-110">See [Client-Side Asynchronous Pipe Handling](client-side-asynchronous-pipe-handling.md).</span></span>

<span data-ttu-id="a3e7b-111">O servidor recebe dados de pipe assíncrono da mesma maneira que o cliente.</span><span class="sxs-lookup"><span data-stu-id="a3e7b-111">The server receives asynchronous pipe data in the same manner as the client.</span></span> <span data-ttu-id="a3e7b-112">Se o mecanismo de recebimento é chamado de procedimento assíncrono (APCs), o servidor deve especificar um identificador de thread (em pAsync->u. APC. hThread) e registrar o identificador assíncrono com a biblioteca de tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="a3e7b-112">If the receive mechanism is asynchronous procedure calls (APCs), the server must specify a thread handle (in pAsync->u.APC.hThread) and register the asynchronous handle with the run-time library.</span></span>

## <a name="example"></a><span data-ttu-id="a3e7b-113">Exemplo</span><span class="sxs-lookup"><span data-stu-id="a3e7b-113">Example</span></span>

<span data-ttu-id="a3e7b-114">Neste exemplo, a rotina do Gerenciador de servidores, MyAsyncPipeFunc, manipula a chamada de procedimento remoto do cliente.</span><span class="sxs-lookup"><span data-stu-id="a3e7b-114">In this example, the server manager routine, MyAsyncPipeFunc, handles the remote procedure call from the client.</span></span>


```C++
typedef struct 
{
    PRPC_ASYNC_STATE pAsync;
    ASYNC_INTPIPE *inpipe;
    ASYNC_INTPIPE *outpipe;
    int i;
    int *b;
    int PipeBuffer[ASYNC_CHUNK_SIZE];
} PIPE_CALL_COOKIE;
 
void MyAsyncPipeFunc(
    IN PRPC_ASYNC_STATE pAsync,
    IN RPC_BINDING_HANDLE hBinding,
    IN int a,
    IN ASYNC_INTPIPE *inpipe,
    OUT ASYNC_INTPIPE *outpipe,
    OUT int *b)
{
    unsigned long ThreadIdentifier;
    HANDLE HandleToThread;
    PIPE_CALL_COOKIE *PipeCallCookie;
 
    PipeCallCookie = new PIPE_CALL_COOKIE;
    PipeCallCookie->pAsync = pAsync;
    PipeCallCookie->inpipe = inpipe;
    PipeCallCookie->outpipe = outpipe;
    PipeCallCookie->b = b;
 
    pAsync->u.APC.hThread = 0;
    pAsync->u.APC.hThread = CreateThread(
                                0, DefaultThreadStackSize,
                                (LPTHREAD_START_ROUTINE)   
                                ThreadProcPipes,
                                PipeCallCookie, 0,
                                &ThreadIdentifier);
}// endMyAsyncPipeFunc
 
//Sending pipe data
//This APC routine is called when a pipe send completes, 
//or when an asynchronous call completes. 
 
//This thread routine receives pipe data, processes the call, 
//sends the reply back to the client, and 
//completes the asynchronous call.
 
void ThreadProcPipes(IN PIPE_CALL_COOKIE  *Cookie)
{
    int *ptr ;
    int  n ;
    int retval ;
 
    while (pAsync->u.APC.hThread == 0)
    {
        Sleep(10);
    }
 
    pAsync->Flags = RPC_C_NOTIFY_ON_SEND_COMPLETE;
    pAsync->UserInfo = (void *) PipeCallCookie;
    pAsync->NotificationType = RpcNotificationTypeApc;
    pAsync->u.APC.NotificationRoutine = MyAsyncPipeAPCRoutine;
    pAsync->u.APC.hThread = HandleToThread;
 
    RpcAsyncRegisterHandle(pAsync);
 
    while (!fDone)
    {
        Cookie->inpipe->pull(
            Cookie->inpipe.state,
            (int *) Cookie->PipeBuffer,
            ASYNC_CHUNK_SIZE,
            &num_elements);
        switch (Status)
        {
            case RPC_S_ASYNC_CALL_PENDING:
                if (SleepEx(INFINITE, TRUE) != WAIT_IO_COMPLETION)
                {
                    RpcRaiseException(APP_ERROR) ;
                }
            break;
 
            case RPC_S_OK:
                if (num_elements == 0)
                {
                    fDone = 1;
                }
                else
                {
                    // process the received data
                }
            break;
 
            default:
                fDone = 1;
            break;
        }
    }
 
    Cookie->i = 1;
    Cookie->outpipe->push(
        Cookie->outpipe.state,
        0,
        Cookie->PipeBuffer,
        ASYNC_CHUNK_SIZE) ;
 
    while (Cookie->i < ASYNC_NUM_CHUNKS+1)
    {
        if (SleepEx(INFINITE, TRUE) != WAIT_IO_COMPLETION)
        {
            RpcRaiseException (APP_ERROR);
        }
    }
    // sending non pipe reply
    *(Cookie->b) = 10;
    Status = RpcAsyncCompleteCall (Cookie->pAsync, &retval);
}
 
void MyAsyncPipeAPCRoutine (
    IN PRPC_ASYNC_STATE pAsync,
    IN void *Context,
    IN unsigned int Flags)
{
    PIPE_CALL_COOKIE *Cookie = (PIPE_CALL_COOKIE *) pAsync->UserInfo;
 
    if (Flags & RPC_ASYNC_PIPE_SEND_COMPLETE)
    {
        if (Cookie->i & ASYNC_NUM_CHUNKS)
        {
            Cookie->outpipe->push(
                Cookie->outpipe.state,
                0,
                (int *) Cookie->PipeBuffer,
                ASYNC_CHUNK_SIZE);
            Cookie->i++ ;
        }
        else
        {
            pAsync->Flags = 0;
            Cookie->outpipe->push(Cookie->outpipe.state, 0, 0, 0);
            Cookie->i++;
        }
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="a3e7b-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a3e7b-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3e7b-116">Pipes</span><span class="sxs-lookup"><span data-stu-id="a3e7b-116">Pipes</span></span>](pipes.md)
</dt> <dt>

[<span data-ttu-id="a3e7b-117">MIDL assíncrono</span><span class="sxs-lookup"><span data-stu-id="a3e7b-117">Asynchronous MIDL</span></span>](/windows/desktop/Midl/async)
</dt> <dt>

[<span data-ttu-id="a3e7b-118">RPC assíncrono do lado do servidor</span><span class="sxs-lookup"><span data-stu-id="a3e7b-118">Server-Side Asynchronous RPC</span></span>](server-side-asynchronous-rpc.md)
</dt> </dl>

 

 