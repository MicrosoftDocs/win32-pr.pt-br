---
title: Implementando pipes de entrada no cliente
description: Ao usar um pipe de entrada para transferir dados do cliente para o servidor, você deve implementar um procedimento de pull.
ms.assetid: e941a6be-ca91-42b1-9323-ffc63d521f6c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0301fc7324a982db81b6c728131762361cfce185f3d432f238ca2cf8d715546
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118929115"
---
# <a name="implementing-input-pipes-on-the-client"></a>Implementando pipes de entrada no cliente

Ao usar um pipe de entrada para transferir dados do cliente para o servidor, você deve implementar um procedimento de pull. O procedimento de pull deve encontrar os dados a serem transferidos, ler os dados no buffer e definir o número de elementos a serem enviado. Nem todos os dados devem estar no buffer quando o servidor começa a fazer pull de dados para si mesmo. O procedimento de pull pode preencher o buffer incrementalmente.

Quando não há mais dados a enviar, o procedimento define seu último argumento como zero. Quando todos os dados são enviados, o procedimento de pull deve fazer qualquer limpeza necessária antes de retornar. Para um parâmetro que é um pipe de entrada e saída, o procedimento de pull deve redefinir a variável de estado do cliente depois que todos os dados foram transmitidos, para que o procedimento de push possa usá-lo para receber \[ \] dados.

O exemplo a seguir é extraído do programa Pipedemo incluído no SDK (Kit de Desenvolvimento de Software de Plataforma).


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



Este exemplo inclui o arquivo de cabeça gerado pelo compilador MIDL. Para obter detalhes, [consulte Definindo pipes em arquivos IDL](defining-pipes-in-idl-files.md). Ele também declara uma variável que usa como a fonte de dados chamada globalPipeData. A variável globalBuffer é um buffer que o procedimento de pull usa para enviar os blocos de dados obtidos de globalPipeData.

A função SendLongs declara o pipe de entrada e aloca memória para a variável de fonte de dados globalPipeData. No programa cliente/servidor, a fonte de dados pode ser um arquivo ou estrutura que o cliente cria. Você também pode fazer com que seu programa cliente obtenha dados do servidor, processe-os e retorne-os ao servidor usando um pipe de entrada. Neste exemplo simples, a fonte de dados é um buffer alocado dinamicamente de inteiros longos.

Antes que a transferência possa começar, o cliente deve definir ponteiros para a variável de estado, o procedimento de pull e o procedimento de aloc. Esses ponteiros são mantidos na variável de pipe declarada pelo cliente. Nesse caso, SendLongs declara inPipe. Você pode usar qualquer tipo de dados apropriado para sua variável de estado.

Os clientes iniciam transferências de dados em um pipe invocando um procedimento remoto no servidor. Chamar o procedimento remoto informa ao programa de servidor que o cliente está pronto para transmitir. Em seguida, o servidor pode fazer pull dos dados para si mesmo. Este exemplo invoca um procedimento remoto chamado InPipe. Depois que os dados são transferidos para o servidor, a função SendLongs libera o buffer alocado dinamicamente.

Em vez de alocar memória sempre que um buffer for necessário. o procedimento de alocação neste exemplo simplesmente define um ponteiro para a variável globalBuffer. O procedimento de pull reutiliza esse buffer sempre que transfere dados. Programas cliente mais complexos podem precisar alocar um novo buffer sempre que o servidor recebe dados do cliente.

O stub do cliente chama o procedimento de pull. O procedimento de pull neste exemplo usa a variável de estado para acompanhar a próxima posição no buffer de fonte de dados global da leitura. Ele lê dados do buffer de origem no buffer de pipe. O stub do cliente transmite os dados para o servidor. Quando todos os dados foram enviados, o procedimento de pull define o tamanho do buffer como zero. Isso informa ao servidor para interromper a coleta de dados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tubo](/windows/desktop/Midl/pipe)
</dt> <dt>

[**/Oi**](/windows/desktop/Midl/-oi)
</dt> </dl>

 

 