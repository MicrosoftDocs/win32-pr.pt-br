---
description: 'O encerramento de um thread tem os seguintes resultados: todos os recursos pertencentes ao thread, como janelas e ganchos, são liberados. O código de saída do thread está definido. O objeto de thread é sinalizado. Se o thread for o único thread ativo no processo, o processo será encerrado. Para obter mais informações, consulte Terminando um processo.'
ms.assetid: 633e5d0c-e9d8-4f9a-9411-17cbe9e2e6e4
title: Encerrando um thread
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef64729db5490ebdab3ba759b34a105c31d2cbc421a404d07b041aa9b611ba08
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799036"
---
# <a name="terminating-a-thread"></a>Encerrando um thread

O encerramento de um thread tem os seguintes resultados:

-   Todos os recursos pertencentes ao thread, como janelas e ganchos, são liberados.
-   O código de saída do thread está definido.
-   O objeto de thread é sinalizado.
-   Se o thread for o único thread ativo no processo, o processo será encerrado. Para obter mais informações, [consulte Terminando um processo](terminating-a-process.md).

A [**função GetExitCodeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getexitcodethread) retorna o status de encerramento de um thread. Enquanto um thread está em execução, seu status de encerramento é STILL \_ ACTIVE. Quando um thread é encerrado, seu status de encerramento muda de STILL ACTIVE para o código \_ de saída do thread.

Quando um thread é encerrado, o estado do objeto de thread muda para sinalizado, liberando quaisquer outros threads que estavam aguardando o thread terminar. Para obter mais informações sobre sincronização, [consulte Synchronizing Execution of Multiple Threads](synchronizing-execution-of-multiple-threads.md).

Quando um thread é encerrado, seu objeto de thread não é liberado até que todos os identificadodores abertos para o thread sejam fechados.

## <a name="how-threads-are-terminated"></a>Como os threads são encerrados

Um thread é executado até que ocorra um dos seguintes eventos:

-   O thread chama a [**função ExitThread.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread)
-   Qualquer thread do processo chama a [**função ExitProcess.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess)
-   A função de thread retorna.
-   Qualquer thread chama a [**função TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread) com um alça para o thread.
-   Qualquer thread chama a [**função TerminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess) com um handle para o processo.

O código de saída para um thread é o valor especificado na chamada para [**ExitThread,**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread) [**ExitProcess,**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) [**TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread)ou [**TerminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess)ou o valor retornado pela função de thread.

Se um thread for encerrado por [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread), o sistema chamará a função de ponto de entrada de cada DLL anexada com um valor que indica que o thread está desconectando da DLL (a menos que você chame a função [**DisableThreadLibraryCalls).**](/windows/win32/api/libloaderapi/nf-libloaderapi-disablethreadlibrarycalls) Se um thread for encerrado por [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess), as funções de ponto de entrada de DLL serão invocadas uma vez, para indicar que o processo está desconectando. As DLLs não são notificadas quando um thread é encerrado por [**TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread) ou [**TerminateProcess.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess) Para obter mais informações sobre DLLs, consulte [Bibliotecas de vínculo dinâmico.](../dlls/dynamic-link-libraries.md)

As funções [**TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread) e [**TerminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess) devem ser usadas apenas em circunstâncias extremas, pois elas não permitem a limpeza de threads, não notificam DLLs anexadas e não liberam a pilha inicial. Além disso, os tratamentos para objetos pertencentes ao thread não são fechados até que o processo seja encerrado. As etapas a seguir fornecem uma solução melhor:

-   Crie um objeto de evento usando a [**função CreateEvent.**](/windows/win32/api/synchapi/nf-synchapi-createeventa)
-   Crie os threads.
-   Cada thread monitora o estado do evento chamando a [**função WaitForSingleObject.**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) Use um intervalo de tempo de espera de zero.
-   Cada thread encerra sua própria execução quando o evento é definido como o estado sinalizado ([**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) retorna WAIT \_ OBJECT \_ 0).

 

 
