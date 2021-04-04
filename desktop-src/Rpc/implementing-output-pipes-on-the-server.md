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
# <a name="implementing-output-pipes-on-the-server"></a><span data-ttu-id="78a08-103">Implementando os pipes de saída no servidor</span><span class="sxs-lookup"><span data-stu-id="78a08-103">Implementing Output Pipes on the Server</span></span>

<span data-ttu-id="78a08-104">Para começar a receber dados de um servidor, um cliente chama um dos procedimentos remotos do servidor.</span><span class="sxs-lookup"><span data-stu-id="78a08-104">To begin receiving data from a server, a client calls one of the server's remote procedures.</span></span> <span data-ttu-id="78a08-105">Esse procedimento deve chamar repetidamente o procedimento de push no stub do servidor.</span><span class="sxs-lookup"><span data-stu-id="78a08-105">This procedure must repeatedly call the push procedure in the server's stub.</span></span> <span data-ttu-id="78a08-106">O compilador MIDL usa o arquivo IDL do aplicativo para gerar automaticamente o procedimento de push do servidor.</span><span class="sxs-lookup"><span data-stu-id="78a08-106">The MIDL compiler uses the application's IDL file to automatically generate the server's push procedure.</span></span>

<span data-ttu-id="78a08-107">A rotina do servidor remoto deve preencher o buffer do pipe de saída com os dados antes de chamar o procedimento de push.</span><span class="sxs-lookup"><span data-stu-id="78a08-107">The remote server routine must fill the output pipe's buffer with data before it calls the push procedure.</span></span> <span data-ttu-id="78a08-108">Cada vez que o programa de servidor invoca o procedimento de push em seu stub, o procedimento de push realiza marshaling dos dados e os transmite para o cliente.</span><span class="sxs-lookup"><span data-stu-id="78a08-108">Each time the server program invokes the push procedure in its stub, the push procedure marshals the data and transmits it to the client.</span></span> <span data-ttu-id="78a08-109">O loop continua até que o servidor envie um buffer de comprimento zero.</span><span class="sxs-lookup"><span data-stu-id="78a08-109">The loop continues until the server sends a buffer of zero length.</span></span>

<span data-ttu-id="78a08-110">O exemplo a seguir é do programa Pipedemo contido nos exemplos fornecidos com o SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="78a08-110">The following example is from the Pipedemo program contained in the samples that come with the Windows SDK.</span></span> <span data-ttu-id="78a08-111">Ele ilustra um procedimento de servidor remoto que usa um pipe para enviar dados por push do servidor para o cliente.</span><span class="sxs-lookup"><span data-stu-id="78a08-111">It illustrates a remote server procedure that uses a pipe to push data from the server to the client.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="78a08-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="78a08-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78a08-113">pipe</span><span class="sxs-lookup"><span data-stu-id="78a08-113">pipe</span></span>](/windows/desktop/Midl/pipe)
</dt> <dt>

[<span data-ttu-id="78a08-114">**/Oi**</span><span class="sxs-lookup"><span data-stu-id="78a08-114">**/Oi**</span></span>](/windows/desktop/Midl/-oi)
</dt> </dl>

 

 