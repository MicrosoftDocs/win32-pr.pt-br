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
# <a name="implementing-input-pipes-on-the-server"></a>Implementando pipes de entrada no servidor

Para começar a enviar dados para um servidor, um cliente chama um dos procedimentos remotos do servidor. Esse procedimento deve chamar repetidamente o procedimento de pull no stub do servidor. O compilador MIDL usa o arquivo IDL do aplicativo para gerar automaticamente o procedimento de pull do servidor.

Cada vez que o programa de servidor invoca o procedimento de pull em seu stub, o procedimento de pull recebe blocos de dados do cliente. Ele desempacota os dados no buffer do servidor. O procedimento remoto do servidor pode, então, processar esses dados de qualquer maneira necessária. O loop continua até que o servidor receba um buffer de comprimento zero.

O exemplo a seguir é do programa Pipedemo contido nos exemplos fornecidos com o SDK (Software Development Kit) da plataforma. Ele ilustra um procedimento de servidor remoto que usa um pipe para efetuar pull de dados do cliente para o servidor.

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

 

 




