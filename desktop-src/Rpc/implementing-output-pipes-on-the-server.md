---
title: Implementando pipes de saída no servidor
description: Para começar a receber dados de um servidor, um cliente chama um dos procedimentos remotos do servidor.
ms.assetid: 5d791f4f-1d95-4bc0-b68f-db4fccc75ff8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 234d93b2933499ca86ab49732d46cf2abe3c37247ed7bfa5e653e5aa0119b1e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120020486"
---
# <a name="implementing-output-pipes-on-the-server"></a>Implementando pipes de saída no servidor

Para começar a receber dados de um servidor, um cliente chama um dos procedimentos remotos do servidor. Esse procedimento deve chamar repetidamente o procedimento de push no stub do servidor. O compilador MIDL usa o arquivo IDL do aplicativo para gerar automaticamente o procedimento de push do servidor.

A rotina de servidor remoto deve preencher o buffer do pipe de saída com dados antes de chamar o procedimento de push. Sempre que o programa de servidor invoca o procedimento de push em seu stub, o procedimento de push faz marshal dos dados e os transmite para o cliente. O loop continua até que o servidor envie um buffer de comprimento zero.

O exemplo a seguir é do programa Pipedemo contido nos exemplos que acompanham o SDK Windows. Ele ilustra um procedimento de servidor remoto que usa um pipe para fazer push de dados do servidor para o cliente.


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

[Tubo](/windows/desktop/Midl/pipe)
</dt> <dt>

[**/Oi**](/windows/desktop/Midl/-oi)
</dt> </dl>

 

 