---
title: Implementando pipes de entrada no cliente
description: Ao usar um pipe de entrada para transferir dados do cliente para o servidor do, você deve implementar um procedimento de pull.
ms.assetid: e941a6be-ca91-42b1-9323-ffc63d521f6c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2810caa31c4932294797a5ed502c6f93d8613ea0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823895"
---
# <a name="implementing-input-pipes-on-the-client"></a><span data-ttu-id="70160-103">Implementando pipes de entrada no cliente</span><span class="sxs-lookup"><span data-stu-id="70160-103">Implementing Input Pipes on the Client</span></span>

<span data-ttu-id="70160-104">Ao usar um pipe de entrada para transferir dados do cliente para o servidor do, você deve implementar um procedimento de pull.</span><span class="sxs-lookup"><span data-stu-id="70160-104">When using an input pipe to transfer data from the client to the server, you must implement a pull procedure.</span></span> <span data-ttu-id="70160-105">O procedimento de pull deve localizar os dados a serem transferidos, ler os dados no buffer e definir o número de elementos a serem enviados.</span><span class="sxs-lookup"><span data-stu-id="70160-105">The pull procedure must find the data to be transferred, read the data into the buffer, and set the number of elements to send.</span></span> <span data-ttu-id="70160-106">Nem todos os dados têm que estar no buffer quando o servidor começa a efetuar pull de dados para si mesmo.</span><span class="sxs-lookup"><span data-stu-id="70160-106">Not all of the data has to be in the buffer when the server begins to pull data to itself.</span></span> <span data-ttu-id="70160-107">O procedimento pull pode preencher o buffer de forma incremental.</span><span class="sxs-lookup"><span data-stu-id="70160-107">The pull procedure can fill the buffer incrementally.</span></span>

<span data-ttu-id="70160-108">Quando não houver mais dados a serem enviados, o procedimento definirá seu último argumento como zero.</span><span class="sxs-lookup"><span data-stu-id="70160-108">When there is no more data to send, the procedure sets its last argument to zero.</span></span> <span data-ttu-id="70160-109">Quando todos os dados são enviados, o procedimento de pull deve fazer qualquer limpeza necessária antes de retornar.</span><span class="sxs-lookup"><span data-stu-id="70160-109">When all the data is sent, the pull procedure should do any needed cleanup before returning.</span></span> <span data-ttu-id="70160-110">Para um parâmetro que é um \[ pipe de entrada, saída \] , o procedimento de pull deve redefinir a variável de estado do cliente depois que todos os dados tiverem sido transmitidos, para que o procedimento de push possa usá-lo para receber dados.</span><span class="sxs-lookup"><span data-stu-id="70160-110">For a parameter that is an \[in, out\] pipe, the pull procedure must reset the client's state variable after all the data has been transmitted, so that the push procedure can use it to receive data.</span></span>

<span data-ttu-id="70160-111">O exemplo a seguir é extraído do programa Pipedemo incluído no SDK (Software Development Kit) da plataforma.</span><span class="sxs-lookup"><span data-stu-id="70160-111">The following example is extracted from the Pipedemo program included with the Platform Software Development Kit (SDK).</span></span>


```C++
//file: client.c (fragment)
#include <windows.h>
#include "pipedemo.h"
long *globalPipeData;
long    globalBuffer[BUF_SIZE];
 
ulong   pipeDataIndex; /* state variable */
 
void SendLongs()
{
    LONG_PIPE inPipe;
    int i;
    globalPipeData =
        (long *)malloc( sizeof(long) * PIPE_SIZE );
 
    for (i=0; i<PIPE_SIZE; i++)
        globalPipeData[i] = IN_VALUE;
 
    pipeDataIndex = 0;
    inPipe.state =  (rpc_ss_pipe_state_t )&pipeDataIndex;
    inPipe.pull  = PipePull;
    inPipe.alloc = PipeAlloc;
 
    InPipe( inPipe ); /* Make the rpc */
 
    free( (void *)globalPipeData );

}//end SendLongs
 
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
 
void PipePull( rpc_ss_pipe_state_t stateInfo,
               long *inputBuffer,
               ulong maxBufSize,
               ulong *sizeToSend )
{
    ulong currentIndex;
    ulong i;
    ulong elementsToRead;
    ulong *state = (ulong *)stateInfo;

    currentIndex = *state;
    if (*state >=  PIPE_SIZE )
    {
        *sizeToSend = 0; /* end of pipe data */
        *state = 0; /* Reset the state = global index */
    }
    else 
    {
        if ( currentIndex + maxBufSize > PIPE_SIZE )
            elementsToRead = PIPE_SIZE - currentIndex;
        else
            elementsToRead = maxBufSize;
 
        for (i=0; i < elementsToRead; i++)
        {
            /*client sends data */
            inputBuffer[i] = globalPipeData[i + currentIndex];
        }
 
        *state +=   elementsToRead;
        *sizeToSend = elementsToRead;
    } 
}//end PipePull
```



<span data-ttu-id="70160-112">Este exemplo inclui o arquivo de cabeçalho gerado pelo compilador MIDL.</span><span class="sxs-lookup"><span data-stu-id="70160-112">This example includes the header file generated by the MIDL compiler.</span></span> <span data-ttu-id="70160-113">Para obter detalhes, consulte [definindo pipes em arquivos IDL](defining-pipes-in-idl-files.md).</span><span class="sxs-lookup"><span data-stu-id="70160-113">For details see [Defining Pipes in IDL Files](defining-pipes-in-idl-files.md).</span></span> <span data-ttu-id="70160-114">Ele também declara uma variável que ele usa como a fonte de dados chamada globalPipeData.</span><span class="sxs-lookup"><span data-stu-id="70160-114">It also declares a variable it uses as the data source called globalPipeData.</span></span> <span data-ttu-id="70160-115">A variável globalBuffer é um buffer que o procedimento de pull usa para enviar os blocos de dados obtidos de globalPipeData.</span><span class="sxs-lookup"><span data-stu-id="70160-115">The variable globalBuffer is a buffer that the pull procedure uses to send the blocks of data it obtains from globalPipeData.</span></span>

<span data-ttu-id="70160-116">A função SendLongs declara o pipe de entrada e aloca memória para a variável de fonte de dados globalPipeData.</span><span class="sxs-lookup"><span data-stu-id="70160-116">The SendLongs function declares the input pipe, and allocates memory for the data source variable globalPipeData.</span></span> <span data-ttu-id="70160-117">No seu programa cliente/servidor, a fonte de dados pode ser um arquivo ou uma estrutura que o cliente cria.</span><span class="sxs-lookup"><span data-stu-id="70160-117">In your client/server program, the data source can be a file or structure that the client creates.</span></span> <span data-ttu-id="70160-118">Você também pode fazer com que seu programa cliente obtenha dados do servidor, processe-os e devolva-os para o servidor usando um pipe de entrada.</span><span class="sxs-lookup"><span data-stu-id="70160-118">You can also have your client program obtain data from the server, process it, and return it to the server using an input pipe.</span></span> <span data-ttu-id="70160-119">Neste exemplo simples, a fonte de dados é um buffer alocado dinamicamente de inteiros longos.</span><span class="sxs-lookup"><span data-stu-id="70160-119">In this simple example, the data source is a dynamically allocated buffer of long integers.</span></span>

<span data-ttu-id="70160-120">Antes que a transferência possa começar, o cliente deve definir ponteiros para a variável de estado, o procedimento de pull e o procedimento de alocação.</span><span class="sxs-lookup"><span data-stu-id="70160-120">Before the transfer can begin, the client must set pointers to the state variable, the pull procedure, and the alloc procedure.</span></span> <span data-ttu-id="70160-121">Esses ponteiros são mantidos na variável de pipe que o cliente declara.</span><span class="sxs-lookup"><span data-stu-id="70160-121">These pointers are kept in the pipe variable the client declares.</span></span> <span data-ttu-id="70160-122">Nesse caso, SendLongs declara inpipe.</span><span class="sxs-lookup"><span data-stu-id="70160-122">In this case, SendLongs declares inPipe.</span></span> <span data-ttu-id="70160-123">Você pode usar qualquer tipo de dados apropriado para sua variável de estado.</span><span class="sxs-lookup"><span data-stu-id="70160-123">You can use any appropriate data type for your state variable.</span></span>

<span data-ttu-id="70160-124">Os clientes iniciam transferências de dados em um pipe invocando um procedimento remoto no servidor.</span><span class="sxs-lookup"><span data-stu-id="70160-124">Clients initiate data transfers across a pipe by invoking a remote procedure on the server.</span></span> <span data-ttu-id="70160-125">Chamar o procedimento remoto informa ao programa do servidor que o cliente está pronto para transmitir.</span><span class="sxs-lookup"><span data-stu-id="70160-125">Calling the remote procedure tells the server program that the client is ready to transmit.</span></span> <span data-ttu-id="70160-126">O servidor pode então extrair os dados para si mesmo.</span><span class="sxs-lookup"><span data-stu-id="70160-126">The server can then pull the data to itself.</span></span> <span data-ttu-id="70160-127">Este exemplo invoca um procedimento remoto chamado inpipe.</span><span class="sxs-lookup"><span data-stu-id="70160-127">This example invokes a remote procedure called InPipe.</span></span> <span data-ttu-id="70160-128">Depois que os dados são transferidos para o servidor, a função SendLongs libera o buffer alocado dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="70160-128">After the data is transferred to the server, the SendLongs function frees the dynamically allocated buffer.</span></span>

<span data-ttu-id="70160-129">Em vez de alocar memória toda vez que um buffer é necessário.</span><span class="sxs-lookup"><span data-stu-id="70160-129">Rather than allocate memory each time a buffer is needed.</span></span> <span data-ttu-id="70160-130">o procedimento de alocação neste exemplo simplesmente define um ponteiro para a variável globalBuffer.</span><span class="sxs-lookup"><span data-stu-id="70160-130">the alloc procedure in this example simply sets a pointer to the variable globalBuffer.</span></span> <span data-ttu-id="70160-131">O procedimento de pull reutiliza esse buffer cada vez que transfere dados.</span><span class="sxs-lookup"><span data-stu-id="70160-131">The pull procedure reuses this buffer each time it transfers data.</span></span> <span data-ttu-id="70160-132">Programas de cliente mais complexos talvez precisem alocar um novo buffer sempre que o servidor receber dados do cliente.</span><span class="sxs-lookup"><span data-stu-id="70160-132">More complex client programs may need to allocate a new buffer each time the server pulls data from the client.</span></span>

<span data-ttu-id="70160-133">O stub do cliente chama o procedimento pull.</span><span class="sxs-lookup"><span data-stu-id="70160-133">The client stub calls the pull procedure.</span></span> <span data-ttu-id="70160-134">O procedimento de pull neste exemplo usa a variável de estado para acompanhar a próxima posição no buffer de fonte de dados global para leitura.</span><span class="sxs-lookup"><span data-stu-id="70160-134">The pull procedure in this example uses the state variable to track the next position in the global data source buffer to read from.</span></span> <span data-ttu-id="70160-135">Ele lê os dados do buffer de origem para o buffer de pipe.</span><span class="sxs-lookup"><span data-stu-id="70160-135">It reads data from the source buffer into the pipe buffer.</span></span> <span data-ttu-id="70160-136">O stub do cliente transmite os dados para o servidor.</span><span class="sxs-lookup"><span data-stu-id="70160-136">The client stub transmits the data to the server.</span></span> <span data-ttu-id="70160-137">Quando todos os dados forem enviados, o procedimento de pull definirá o tamanho do buffer como zero.</span><span class="sxs-lookup"><span data-stu-id="70160-137">When all the data has been sent, the pull procedure sets the buffer size to zero.</span></span> <span data-ttu-id="70160-138">Isso instrui o servidor a parar de extrair dados.</span><span class="sxs-lookup"><span data-stu-id="70160-138">This tells the server to stop pulling data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="70160-139">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="70160-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="70160-140">pipe</span><span class="sxs-lookup"><span data-stu-id="70160-140">pipe</span></span>](/windows/desktop/Midl/pipe)
</dt> <dt>

[<span data-ttu-id="70160-141">**/Oi**</span><span class="sxs-lookup"><span data-stu-id="70160-141">**/Oi**</span></span>](/windows/desktop/Midl/-oi)
</dt> </dl>

 

 