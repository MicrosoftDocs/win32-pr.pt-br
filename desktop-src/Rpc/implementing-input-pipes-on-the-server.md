---
title: Implementando pipes de entrada no servidor
description: Para começar a enviar dados para um servidor, um cliente chama um dos procedimentos remotos do servidor.
ms.assetid: 6abaa851-41bf-4a03-8d12-cd595d74c8c9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbf133fce019328b9fa7d6b2a03e47d516de5ca74310d611ecea1686c0b9a3a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120020516"
---
# <a name="implementing-input-pipes-on-the-server"></a>Implementando pipes de entrada no servidor

Para começar a enviar dados para um servidor, um cliente chama um dos procedimentos remotos do servidor. Esse procedimento deve chamar repetidamente o procedimento de pull no stub do servidor. O compilador MIDL usa o arquivo IDL do aplicativo para gerar automaticamente o procedimento de pull do servidor.

Sempre que o programa de servidor invoca o procedimento de pull em seu stub, o procedimento de pull recebe blocos de dados do cliente. Ele desmarcará os dados no buffer do servidor. O procedimento remoto do servidor pode processar esses dados de qualquer maneira necessária. O loop continua até que o servidor receba um buffer de tamanho zero.

O exemplo a seguir é do programa Pipedemo contido nos exemplos que acompanham o SDK (Kit de Desenvolvimento de Software de Plataforma). Ele ilustra um procedimento de servidor remoto que usa um pipe para pull de dados do cliente para o servidor.

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

 

 




