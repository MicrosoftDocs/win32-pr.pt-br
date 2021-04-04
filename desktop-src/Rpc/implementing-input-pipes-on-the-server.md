---
title: Implementando pipes de entrada no servidor
description: Para começar a enviar dados para um servidor, um cliente chama um dos procedimentos remotos do servidor.
ms.assetid: 6abaa851-41bf-4a03-8d12-cd595d74c8c9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d60c2436129b59619f5a9954c70823631d72ae3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822725"
---
# <a name="implementing-input-pipes-on-the-server"></a><span data-ttu-id="1764b-103">Implementando pipes de entrada no servidor</span><span class="sxs-lookup"><span data-stu-id="1764b-103">Implementing Input Pipes on the Server</span></span>

<span data-ttu-id="1764b-104">Para começar a enviar dados para um servidor, um cliente chama um dos procedimentos remotos do servidor.</span><span class="sxs-lookup"><span data-stu-id="1764b-104">To begin sending data to a server, a client calls one of the server's remote procedures.</span></span> <span data-ttu-id="1764b-105">Esse procedimento deve chamar repetidamente o procedimento de pull no stub do servidor.</span><span class="sxs-lookup"><span data-stu-id="1764b-105">This procedure must repeatedly call the pull procedure in the server's stub.</span></span> <span data-ttu-id="1764b-106">O compilador MIDL usa o arquivo IDL do aplicativo para gerar automaticamente o procedimento de pull do servidor.</span><span class="sxs-lookup"><span data-stu-id="1764b-106">The MIDL compiler uses the application's IDL file to automatically generate the server's pull procedure.</span></span>

<span data-ttu-id="1764b-107">Cada vez que o programa de servidor invoca o procedimento de pull em seu stub, o procedimento de pull recebe blocos de dados do cliente.</span><span class="sxs-lookup"><span data-stu-id="1764b-107">Each time the server program invokes the pull procedure in its stub, the pull procedure receives blocks of data from the client.</span></span> <span data-ttu-id="1764b-108">Ele desempacota os dados no buffer do servidor.</span><span class="sxs-lookup"><span data-stu-id="1764b-108">It unmarshals the data into the server's buffer.</span></span> <span data-ttu-id="1764b-109">O procedimento remoto do servidor pode, então, processar esses dados de qualquer maneira necessária.</span><span class="sxs-lookup"><span data-stu-id="1764b-109">The server's remote procedure can then process this data in any way required.</span></span> <span data-ttu-id="1764b-110">O loop continua até que o servidor receba um buffer de comprimento zero.</span><span class="sxs-lookup"><span data-stu-id="1764b-110">The loop continues until the server receives a buffer of zero length.</span></span>

<span data-ttu-id="1764b-111">O exemplo a seguir é do programa Pipedemo contido nos exemplos fornecidos com o SDK (Software Development Kit) da plataforma.</span><span class="sxs-lookup"><span data-stu-id="1764b-111">The following example is from the Pipedemo program contained in the samples that come with the Platform Software Development Kit (SDK).</span></span> <span data-ttu-id="1764b-112">Ele ilustra um procedimento de servidor remoto que usa um pipe para efetuar pull de dados do cliente para o servidor.</span><span class="sxs-lookup"><span data-stu-id="1764b-112">It illustrates a remote server procedure that uses a pipe to pull data from the client to the server.</span></span>

``` syntax
//file: server.c (fragment)
#include uc_server.c
#define PIPE_TRANSFER_SIZE 100 /* Transfer 100 pipe elements at one time */
 
void InPipe(LONG_PIPE     long_pipe )
{
    long local_pipe_buf[PIPE_TRANSFER_SIZE];
    ulong actual_transfer_count = PIPE_TRANSFER_SIZE;
 
    while(actual_transfer_count > 0) /* Loop to get all 
                                        the pipe data elements */
    {
        long_pipe.pull( long_pipe.state,
                        local_pipe_buf,
                        PIPE_TRANSFER_SIZE,
                        &actual_transfer_count);
        /* process the elements */
    } // end while
} //end InPipe
```

 

 




