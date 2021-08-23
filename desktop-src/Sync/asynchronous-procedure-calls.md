---
description: Uma APC (chamada de procedimento assíncrono) é uma função que é executada de forma assíncrona no contexto de um thread específico.
ms.assetid: 0197d78e-a4dc-414b-88ba-c5ec5f2ed614
title: Chamadas de procedimento assíncrono
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1c024506c2afc9a895db645fd386ed76f915f6e1178c6b8ce3a257aa7d40fa6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119661446"
---
# <a name="asynchronous-procedure-calls"></a>Chamadas de procedimento assíncrono

Uma APC ( *chamada de procedimento assíncrono* ) é uma função que é executada de forma assíncrona no contexto de um thread específico. Quando uma APC é enfileirada em um thread, o sistema emite uma interrupção de software. Na próxima vez em que o thread for agendado, ele executará a função APC. Uma APC gerada pelo sistema é chamada de *APC de modo kernel*. Uma APC gerada por um aplicativo é chamada de *APC (modo de usuário*). Um thread deve estar em um estado de alerta para executar uma APC de modo de usuário.

Cada thread tem sua própria fila da APC. Um aplicativo enfileira uma APC em um thread chamando a função [**QueueUserAPC**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-queueuserapc) . O thread de chamada especifica o endereço de uma função da APC na chamada para **QueueUserAPC**. O enfileiramento de uma APC é uma solicitação para que o thread chame a função APC.

Quando um APC de modo de usuário é enfileirado, o thread no qual ele é enfileirado não é direcionado para chamar a função APC, a menos que esteja em um estado de alerta. Um thread entra em um estado alertado quando chama a função [**SleepEx**](/windows/win32/api/synchapi/nf-synchapi-sleepex), [**SignalObjectAndWait**](/windows/win32/api/synchapi/nf-synchapi-signalobjectandwait), [**MsgWaitForMultipleObjectsEx**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjectsex), [**WaitForMultipleObjectsEx**](/windows/win32/api/winuser/nf-winuser-msgwaitformultipleobjectsex)ou [**WaitForSingleObjectEx**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex) . Se a espera for satisfeita antes que a APC seja enfileirada, o thread não estará mais em um estado de espera alertado, de modo que a função APC não será executada. No entanto, a APC ainda está na fila, portanto, a função APC será executada quando o thread chamar outra função de espera alertável.

As funções [**ReadFileEx**](/windows/win32/api/fileapi/nf-fileapi-readfileex), [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer), [**SetWaitableTimerEx**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimerex)e [**WriteFileEx**](/windows/win32/api/fileapi/nf-fileapi-writefileex) são implementadas usando uma APC como o mecanismo de retorno de chamada de notificação de conclusão.

Se você estiver usando um [pool de threads](../procthread/thread-pools.md), observe que o APCs não funciona bem como outros mecanismos de sinalização porque o sistema controla o tempo de vida dos threads do pool de threads, de modo que é possível que um thread seja encerrado antes que a notificação seja entregue. Em vez de usar um mecanismo de sinalização baseado em APC, como o parâmetro *pfnCompletionRoutine* de [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer) ou [**SetWaitableTimerEx**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimerex), use um objeto de espera, como um temporizador criado com [**CreateThreadpoolTimer**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-createthreadpooltimer). Para e/s, use um objeto de conclusão de e/s criado com [**CreateThreadpoolIo**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolio) ou uma estrutura [**sobreposta**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) baseada em *hEvent*, em que o evento pode ser passado para a função [**SetThreadpoolWait**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolwait) .

## <a name="synchronization-internals"></a>Internos de sincronização

Quando uma solicitação de e/s é emitida, uma estrutura é alocada para representar a solicitação. Essa estrutura é chamada de pacote de solicitação de e/s (IRP). Com e/s síncrona, o thread cria o IRP, envia-o para a pilha do dispositivo e aguarda o kernel para que o IRP seja concluído. Com e/s assíncrona, o thread cria o IRP e o envia para a pilha do dispositivo. A pilha pode concluir o IRP imediatamente ou pode retornar um status pendente indicando que a solicitação está em andamento. Quando isso acontece, o IRP ainda está associado ao thread, portanto, ele será cancelado se o thread terminar ou chamar uma função como [**CancelIo**](/windows/win32/api/ioapiset/nf-ioapiset-cancelio). Enquanto isso, o thread pode continuar executando outras tarefas enquanto a pilha de dispositivos continua a processar o IRP.

Há várias maneiras pelas quais o sistema pode indicar que o IRP foi concluído:

-   Atualize a estrutura sobreposta com o resultado da operação para que o thread possa sondar para determinar se a operação foi concluída.
-   Sinalizar o evento na estrutura sobreposta para que um thread possa ser sincronizado no evento e seja ativadosdo quando a operação for concluída.
-   Enfileirar o IRP para a APC pendente do thread para que o thread execute a rotina da APC quando entrar em um estado de espera alertado e retorne da operação de espera com um status indicando que ele executou uma ou mais rotinas da APC.
-   Enfileirar o IRP para uma porta de conclusão de e/s, onde ele será executado pelo próximo thread que aguarda na porta de conclusão.

Os threads que esperam em uma porta de conclusão de e/s não esperam em um estado de alerta. Portanto, se esses threads emitirem IRPs que estão definidos para serem concluídos como APCs para o thread, as conclusões do IPC não ocorrerão em tempo hábil; Eles ocorrerão somente se o thread escolher uma solicitação da porta de conclusão de e/s e, em seguida, ocorrer uma espera alerta.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando um temporizador de espera com uma chamada de procedimento assíncrono](using-a-waitable-timer-with-an-asynchronous-procedure-call.md)
</dt> </dl>

 

 
