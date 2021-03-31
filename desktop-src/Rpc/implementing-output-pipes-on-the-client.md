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
# <a name="implementing-output-pipes-on-the-client"></a>Implementando os pipes de saída no cliente

Ao usar um pipe de saída para transferir dados do servidor para o cliente do, você deve implementar um procedimento de push em seu cliente. O procedimento de push usa um ponteiro para um buffer e uma contagem de elementos do stub do cliente e, se a contagem de elementos for maior que 0, processará os dados. Por exemplo, ele pode copiar os dados do buffer do stub para sua própria memória. Como alternativa, ele pode processar os dados no buffer do stub e salvá-los em um arquivo. Quando a contagem de elementos for igual a zero, o procedimento de push concluirá todas as tarefas de limpeza necessárias antes de retornar.

No exemplo a seguir, a função de cliente ReceiveLongs aloca uma estrutura de pipe e um buffer de memória global. Ele inicializa a estrutura, faz a chamada de procedimento remoto e libera a memória.

## <a name="example"></a>Exemplo


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



Este exemplo inclui o arquivo de cabeçalho gerado pelo compilador MIDL. Para obter detalhes, consulte [definindo pipes no arquivo IDL](defining-pipes-in-idl-files.md). Ele também declara uma variável, globalPipeData, que ela usa como o coletor de dados. A variável globalBuffer é um buffer usado pelo procedimento de push para receber blocos de dados armazenados em globalPipeData.

A função ReceiveLongs declara um pipe e aloca espaço de memória para a variável de coletor de dados global. No seu programa cliente/servidor, o coletor de dados pode ser uma estrutura de arquivo ou de dados que o cliente cria. Neste exemplo simples, a fonte de dados é um buffer alocado dinamicamente de inteiros longos.

Antes que a transferência de dados possa começar, o programa cliente deve inicializar a estrutura do pipe de saída. Ele deve definir ponteiros para a variável de estado, o procedimento de push e o procedimento de alocação. Neste exemplo, a variável de pipe de saída é chamada outputPipe.

Os clientes sinalizam os servidores que estão prontos para receber dados invocando um procedimento remoto no servidor. Neste exemplo, o procedimento remoto é chamado de outpipe. Quando o cliente chama o procedimento remoto, o servidor inicia a transferência de dados. Cada vez que os dados chegam, o stub do cliente chama os procedimentos de alocação e push do cliente, conforme necessário.

Em vez de alocar memória toda vez que um buffer é necessário, o procedimento de alocação neste exemplo simplesmente define um ponteiro para a variável globalBuffer. Em seguida, o procedimento de pull reutiliza esse buffer sempre que ele transfere dados. Programas de cliente mais complexos talvez precisem alocar um novo buffer sempre que o servidor receber dados do cliente.

O procedimento de envio neste exemplo usa a variável de estado para acompanhar a próxima posição em que armazenará dados no buffer de coletor de dados global. Ele grava dados do buffer de pipe no buffer do coletor. O stub do cliente recebe o próximo bloco de dados do servidor e o armazena no buffer do pipe. Quando todos os dados são enviados, o servidor transmite um buffer de tamanho zero. Isso indicações sobre o procedimento de push para parar de receber dados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[pipe](/windows/desktop/Midl/pipe)
</dt> <dt>

[**/Oi**](/windows/desktop/Midl/-oi)
</dt> </dl>

 

 