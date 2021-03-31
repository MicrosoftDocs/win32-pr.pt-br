---
title: Implementando os pipes de saída no cliente
description: Ao usar um pipe de saída para transferir dados do servidor para o cliente do, você deve implementar um procedimento de push em seu cliente.
ms.assetid: ab544daf-fbf7-4b00-95a8-55c149a86c27
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ff274491e2b665d86b550853d07c3ff6a4b2a83
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641222"
---
# <a name="implementing-output-pipes-on-the-client"></a><span data-ttu-id="1a6ef-103">Implementando os pipes de saída no cliente</span><span class="sxs-lookup"><span data-stu-id="1a6ef-103">Implementing Output Pipes on the Client</span></span>

<span data-ttu-id="1a6ef-104">Ao usar um pipe de saída para transferir dados do servidor para o cliente do, você deve implementar um procedimento de push em seu cliente.</span><span class="sxs-lookup"><span data-stu-id="1a6ef-104">When using an output pipe to transfer data from the server to the client, you must implement a push procedure in your client.</span></span> <span data-ttu-id="1a6ef-105">O procedimento de push usa um ponteiro para um buffer e uma contagem de elementos do stub do cliente e, se a contagem de elementos for maior que 0, processará os dados.</span><span class="sxs-lookup"><span data-stu-id="1a6ef-105">The push procedure takes a pointer to a buffer and an element count from the client stub and, if the element count is greater than 0, processes the data.</span></span> <span data-ttu-id="1a6ef-106">Por exemplo, ele pode copiar os dados do buffer do stub para sua própria memória.</span><span class="sxs-lookup"><span data-stu-id="1a6ef-106">For example, it could copy the data from the stub's buffer to its own memory.</span></span> <span data-ttu-id="1a6ef-107">Como alternativa, ele pode processar os dados no buffer do stub e salvá-los em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="1a6ef-107">Alternately, it could process the data in the stub's buffer and save it to a file.</span></span> <span data-ttu-id="1a6ef-108">Quando a contagem de elementos for igual a zero, o procedimento de push concluirá todas as tarefas de limpeza necessárias antes de retornar.</span><span class="sxs-lookup"><span data-stu-id="1a6ef-108">When the element count equals zero, the push procedure completes any needed cleanup tasks before returning.</span></span>

<span data-ttu-id="1a6ef-109">No exemplo a seguir, a função de cliente ReceiveLongs aloca uma estrutura de pipe e um buffer de memória global.</span><span class="sxs-lookup"><span data-stu-id="1a6ef-109">In the following example, the client function ReceiveLongs allocates a pipe structure and a global memory buffer.</span></span> <span data-ttu-id="1a6ef-110">Ele inicializa a estrutura, faz a chamada de procedimento remoto e libera a memória.</span><span class="sxs-lookup"><span data-stu-id="1a6ef-110">It initializes the structure, makes the remote procedure call, and then frees the memory.</span></span>

## <a name="example"></a><span data-ttu-id="1a6ef-111">Exemplo</span><span class="sxs-lookup"><span data-stu-id="1a6ef-111">Example</span></span>


```C++
//file: client.c (fragment)
#include <windows.h>
#include "pipedemo.h"
long *  globalPipeData;
long    globalBuffer[BUF_SIZE];
 
ulong   pipeDataIndex; /* state variable */
 
void ReceiveLongs()
{
    LONG_PIPE *outputPipe;
    idl_long_int i;
 
    globalPipeData =
        (long *)malloc( sizeof(long) * PIPE_SIZE );
    
    pipeDataIndex = 0;
    outputPipe.state =  (rpc_ss_pipe_state_t )&pipeDataIndex;
    outputPipe.push  = PipePush;
    outputPipe.alloc = PipeAlloc;
 
    OutPipe( &outputPipe ); /* Make the rpc */
 
    free( (void *)globalPipeData );
 
}//end ReceiveLongs()

void PipeAlloc( rpc_ss_pipe_state_t stateInfo,
                ulong requestedSize,
                long **allocatedBuffer,
                ulong *allocatedSize )
{ 
    ulong *state = (ulong *)stateInfo;
    if ( requestedSize > (BUF_SIZE*sizeof(long)) )
    {
       *allocatedSize = BUF_SIZE * sizeof(long);
    }
    else
    {
       *allocatedSize = requestedSize;
    }
    *allocatedBuffer = globalBuffer; 
} //end PipeAlloc
 
void PipePush( rpc_ss_pipe_state_t stateInfo,
               long *buffer,
               ulong numberOfElements )
{
    ulong elementsToCopy, i;
    ulong *state = (ulong *)stateInfo;

    if (numberOfElements == 0)/* end of data */
    {
        *state = 0; /* Reset the state = global index */
    }
    else
    {
        if (*state + numberOfElements > PIPE_SIZE)
            elementsToCopy = PIPE_SIZE - *state;
        else
            elementsToCopy = numberOfElements;
 
        for (i=0; i <elementsToCopy; i++)
        { 
            /*client receives data */
            globalPipeData[*state] = buffer[i];
            (*state)++;
        }
    }
}//end PipePush
```



<span data-ttu-id="1a6ef-112">Este exemplo inclui o arquivo de cabeçalho gerado pelo compilador MIDL.</span><span class="sxs-lookup"><span data-stu-id="1a6ef-112">This example includes the header file generated by the MIDL compiler.</span></span> <span data-ttu-id="1a6ef-113">Para obter detalhes, consulte [definindo pipes no arquivo IDL](defining-pipes-in-idl-files.md).</span><span class="sxs-lookup"><span data-stu-id="1a6ef-113">For details see [Defining Pipes in IDL File](defining-pipes-in-idl-files.md).</span></span> <span data-ttu-id="1a6ef-114">Ele também declara uma variável, globalPipeData, que ela usa como o coletor de dados.</span><span class="sxs-lookup"><span data-stu-id="1a6ef-114">It also declares a variable, globalPipeData, that it uses as the data sink.</span></span> <span data-ttu-id="1a6ef-115">A variável globalBuffer é um buffer usado pelo procedimento de push para receber blocos de dados armazenados em globalPipeData.</span><span class="sxs-lookup"><span data-stu-id="1a6ef-115">The variable globalBuffer is a buffer that the push procedure uses to receive blocks of data it stores in globalPipeData.</span></span>

<span data-ttu-id="1a6ef-116">A função ReceiveLongs declara um pipe e aloca espaço de memória para a variável de coletor de dados global.</span><span class="sxs-lookup"><span data-stu-id="1a6ef-116">The ReceiveLongs function declares a pipe and allocates memory space for the global data sink variable.</span></span> <span data-ttu-id="1a6ef-117">No seu programa cliente/servidor, o coletor de dados pode ser uma estrutura de arquivo ou de dados que o cliente cria.</span><span class="sxs-lookup"><span data-stu-id="1a6ef-117">In your client/server program, the data sink can be a file or data structure the client creates.</span></span> <span data-ttu-id="1a6ef-118">Neste exemplo simples, a fonte de dados é um buffer alocado dinamicamente de inteiros longos.</span><span class="sxs-lookup"><span data-stu-id="1a6ef-118">In this simple example, the data source is a dynamically allocated buffer of long integers.</span></span>

<span data-ttu-id="1a6ef-119">Antes que a transferência de dados possa começar, o programa cliente deve inicializar a estrutura do pipe de saída.</span><span class="sxs-lookup"><span data-stu-id="1a6ef-119">Before the data transfer can begin, your client program must initialize the output pipe structure.</span></span> <span data-ttu-id="1a6ef-120">Ele deve definir ponteiros para a variável de estado, o procedimento de push e o procedimento de alocação.</span><span class="sxs-lookup"><span data-stu-id="1a6ef-120">It must set pointers to the state variable, the push procedure, and the alloc procedure.</span></span> <span data-ttu-id="1a6ef-121">Neste exemplo, a variável de pipe de saída é chamada outputPipe.</span><span class="sxs-lookup"><span data-stu-id="1a6ef-121">In this example, the output pipe variable is called outputPipe.</span></span>

<span data-ttu-id="1a6ef-122">Os clientes sinalizam os servidores que estão prontos para receber dados invocando um procedimento remoto no servidor.</span><span class="sxs-lookup"><span data-stu-id="1a6ef-122">Clients signal servers that they are ready to receive data by invoking a remote procedure on the server.</span></span> <span data-ttu-id="1a6ef-123">Neste exemplo, o procedimento remoto é chamado de outpipe.</span><span class="sxs-lookup"><span data-stu-id="1a6ef-123">In this example, the remote procedure is called OutPipe.</span></span> <span data-ttu-id="1a6ef-124">Quando o cliente chama o procedimento remoto, o servidor inicia a transferência de dados.</span><span class="sxs-lookup"><span data-stu-id="1a6ef-124">When the client calls the remote procedure, the server begins the data transfer.</span></span> <span data-ttu-id="1a6ef-125">Cada vez que os dados chegam, o stub do cliente chama os procedimentos de alocação e push do cliente, conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="1a6ef-125">Each time data arrives, the client stub calls the client's alloc and push procedures as needed.</span></span>

<span data-ttu-id="1a6ef-126">Em vez de alocar memória toda vez que um buffer é necessário, o procedimento de alocação neste exemplo simplesmente define um ponteiro para a variável globalBuffer.</span><span class="sxs-lookup"><span data-stu-id="1a6ef-126">Rather than allocate memory each time a buffer is needed, the alloc procedure in this example simply sets a pointer to the variable globalBuffer.</span></span> <span data-ttu-id="1a6ef-127">Em seguida, o procedimento de pull reutiliza esse buffer sempre que ele transfere dados.</span><span class="sxs-lookup"><span data-stu-id="1a6ef-127">The pull procedure then reuses this buffer each time it transfers data.</span></span> <span data-ttu-id="1a6ef-128">Programas de cliente mais complexos talvez precisem alocar um novo buffer sempre que o servidor receber dados do cliente.</span><span class="sxs-lookup"><span data-stu-id="1a6ef-128">More complex client programs may need to allocate a new buffer each time the server pulls data from the client.</span></span>

<span data-ttu-id="1a6ef-129">O procedimento de envio neste exemplo usa a variável de estado para acompanhar a próxima posição em que armazenará dados no buffer de coletor de dados global.</span><span class="sxs-lookup"><span data-stu-id="1a6ef-129">The push procedure in this example uses the state variable to track the next position where it will store data in the global data sink buffer.</span></span> <span data-ttu-id="1a6ef-130">Ele grava dados do buffer de pipe no buffer do coletor.</span><span class="sxs-lookup"><span data-stu-id="1a6ef-130">It writes data from the pipe buffer into sink buffer.</span></span> <span data-ttu-id="1a6ef-131">O stub do cliente recebe o próximo bloco de dados do servidor e o armazena no buffer do pipe.</span><span class="sxs-lookup"><span data-stu-id="1a6ef-131">The client stub then receives the next block of data from the server and stores it in the pipe buffer.</span></span> <span data-ttu-id="1a6ef-132">Quando todos os dados são enviados, o servidor transmite um buffer de tamanho zero.</span><span class="sxs-lookup"><span data-stu-id="1a6ef-132">When all the data has been sent, the server transmits a zero-sized buffer.</span></span> <span data-ttu-id="1a6ef-133">Isso indicações sobre o procedimento de push para parar de receber dados.</span><span class="sxs-lookup"><span data-stu-id="1a6ef-133">This cues the push procedure to stop receiving data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1a6ef-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1a6ef-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a6ef-135">pipe</span><span class="sxs-lookup"><span data-stu-id="1a6ef-135">pipe</span></span>](/windows/desktop/Midl/pipe)
</dt> <dt>

[<span data-ttu-id="1a6ef-136">**/Oi**</span><span class="sxs-lookup"><span data-stu-id="1a6ef-136">**/Oi**</span></span>](/windows/desktop/Midl/-oi)
</dt> </dl>

 

 