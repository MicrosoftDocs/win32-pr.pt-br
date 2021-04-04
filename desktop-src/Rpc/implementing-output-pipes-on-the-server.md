---
title: Implementando os pipes de saída no servidor
description: Para começar a receber dados de um servidor, um cliente chama um dos procedimentos remotos do servidor.
ms.assetid: 5d791f4f-1d95-4bc0-b68f-db4fccc75ff8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb3eb1362736207f9cc79d82ab6c981431d0bfe7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104008050"
---
# <a name="implementing-output-pipes-on-the-server"></a>Implementando os pipes de saída no servidor

Para começar a receber dados de um servidor, um cliente chama um dos procedimentos remotos do servidor. Esse procedimento deve chamar repetidamente o procedimento de push no stub do servidor. O compilador MIDL usa o arquivo IDL do aplicativo para gerar automaticamente o procedimento de push do servidor.

A rotina do servidor remoto deve preencher o buffer do pipe de saída com os dados antes de chamar o procedimento de push. Cada vez que o programa de servidor invoca o procedimento de push em seu stub, o procedimento de push realiza marshaling dos dados e os transmite para o cliente. O loop continua até que o servidor envie um buffer de comprimento zero.

O exemplo a seguir é do programa Pipedemo contido nos exemplos fornecidos com o SDK do Windows. Ele ilustra um procedimento de servidor remoto que usa um pipe para enviar dados por push do servidor para o cliente.


```C++
void OutPipe(LONG_PIPE *outputPipe )
{
    long *outputPipeData;
    ulong index = 0;
    ulong elementsToSend = PIPE_TRANSFER_SIZE;
 
    /* Allocate memory for the data to be passed back in the pipe */
    outputPipeData = (long *)malloc( sizeof(long) * PIPE_SIZE );
    
    while(elementsToSend >0) /* Loop to send pipe data elements */
    {
        if (index >= PIPE_SIZE)
            elementsToSend = 0;
        else
        {
            if ( (index + PIPE_TRANSFER_SIZE) > PIPE_SIZE )
                elementsToSend = PIPE_SIZE - index;
            else
                elementsToSend = PIPE_TRANSFER_SIZE;
        }
                    
        outputPipe->push( outputPipe->state,
                          &(outputPipeData[index]),
                          elementsToSend ); 
        index += elementsToSend;
 
    } //end while
 
    free((void *)outputPipeData);
 
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[pipe](/windows/desktop/Midl/pipe)
</dt> <dt>

[**/Oi**](/windows/desktop/Midl/-oi)
</dt> </dl>

 

 