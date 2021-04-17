---
description: 'O encerramento de um thread tem os seguintes resultados: todos os recursos pertencentes ao thread, como Windows e ganchos, são liberados. O código de saída do thread está definido. O objeto de thread é sinalizado. Se o thread for o único thread ativo no processo, o processo será encerrado. Para obter mais informações, consulte finalizando um processo.'
ms.assetid: 633e5d0c-e9d8-4f9a-9411-17cbe9e2e6e4
title: Finalizando um thread
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ada421356666316072aabff8281787cc140ad114
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759606"
---
# <a name="terminating-a-thread"></a>Finalizando um thread

O encerramento de um thread tem os seguintes resultados:

-   Todos os recursos pertencentes ao thread, como Windows e ganchos, são liberados.
-   O código de saída do thread está definido.
-   O objeto de thread é sinalizado.
-   Se o thread for o único thread ativo no processo, o processo será encerrado. Para obter mais informações, consulte [finalizando um processo](terminating-a-process.md).

A função [**GetExitCodeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getexitcodethread) retorna o status de encerramento de um thread. Enquanto um thread estiver em execução, seu status de encerramento ainda estará \_ ativo. Quando um thread é encerrado, seu status de encerramento é alterado de ainda \_ ativo para o código de saída do thread.

Quando um thread é encerrado, o estado do objeto de thread muda para sinalizado, liberando quaisquer outros threads que estavam aguardando o encerramento do thread. Para obter mais informações sobre sincronização, consulte [sincronizando a execução de vários threads](synchronizing-execution-of-multiple-threads.md).

Quando um thread é encerrado, seu objeto de thread não é liberado até que todos os identificadores abertos para o thread sejam fechados.

## <a name="how-threads-are-terminated"></a>Como os threads são encerrados

Um thread é executado até que ocorra um dos seguintes eventos:

-   O thread chama a função [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread) .
-   Qualquer thread do processo chama a função [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) .
-   A função thread retorna.
-   Qualquer thread chama a função [**TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread) com um identificador para o thread.
-   Qualquer thread chama a função [**TerminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess) com um identificador para o processo.

O código de saída de um thread é o valor especificado na chamada para [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread), [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess), [**TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread)ou [**TerminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess)ou o valor retornado pela função thread.

Se um thread for encerrado por [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread), o sistema chamará a função de ponto de entrada de cada DLL anexada com um valor indicando que o thread está desanexando da dll (a menos que você chame a função [**DisableThreadLibraryCalls**](/windows/win32/api/libloaderapi/nf-libloaderapi-disablethreadlibrarycalls) ). Se um thread for encerrado por [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess), as funções de ponto de entrada de DLL serão invocadas uma vez, para indicar que o processo está sendo desanexado. As DLLs não são notificadas quando um thread é encerrado por [**TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread) ou [**TerminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess). Para obter mais informações sobre DLLs, consulte [bibliotecas de vínculo dinâmico](../dlls/dynamic-link-libraries.md).

As funções [**TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread) e [**TerminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess) devem ser usadas apenas em circunstâncias extremas, já que elas não permitem que os threads sejam limpos, não notifique as DLLs anexadas e não libere a pilha inicial. Além disso, os identificadores para objetos pertencentes ao thread não são fechados até que o processo seja encerrado. As etapas a seguir fornecem uma solução melhor:

-   Crie um objeto de evento usando a função [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) .
-   Crie os threads.
-   Cada thread monitora o estado do evento chamando a função [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) . Use um intervalo de tempo limite de espera igual a zero.
-   Cada thread encerra sua própria execução quando o evento é definido como o estado sinalizado ([**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) retorna o objeto de espera \_ \_ 0).

 

 
