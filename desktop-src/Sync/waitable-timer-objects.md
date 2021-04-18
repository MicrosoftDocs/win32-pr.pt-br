---
description: Um objeto de timer de espera é um objeto de sincronização cujo estado é definido como sinalizado quando o tempo de espera especificado chega.
ms.assetid: 5d39ada0-ea31-40d7-b075-aeb657ee508c
title: Objetos de timer que esperam
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b9597617705fcd78bb71f63e33a475e3bca78e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756354"
---
# <a name="waitable-timer-objects"></a>Objetos de timer que esperam

Um *objeto de timer de espera* é um objeto de sincronização cujo estado é definido como sinalizado quando o tempo de espera especificado chega. Há dois tipos de temporizadores esperados que podem ser criados: redefinição manual e sincronização. Um temporizador de qualquer tipo também pode ser um temporizador periódico.



| Objeto                | Descrição                                                                                                                                                                                             |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| temporizador de redefinição manual    | Um temporizador cujo estado permanece sinalizado até que [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer) seja chamado para estabelecer um novo tempo de conclusão.                                                                          |
| temporizador de sincronização | Um temporizador cujo estado permanece sinalizado até que um thread conclua uma operação de espera no objeto de timer.                                                                                                     |
| temporizador periódico        | Um temporizador que é reativado cada vez que o período especificado expira, até que o temporizador seja redefinido ou cancelado. Um temporizador periódico é um temporizador periódico de redefinição manual ou um temporizador de sincronização periódico. |



 

> [!Note]  
> Quando um temporizador é sinalizado, o processador deve executar para processar as instruções associadas. Temporizadores periódicos de alta frequência mantêm o processador continuamente ocupado, o que impede que o sistema permaneça em um [estado de energia](../power/system-power-states.md) menor para qualquer quantidade significativa de tempo. Isso pode causar um impacto negativo na vida útil da bateria do computador portátil e nos cenários que dependem do gerenciamento de energia efetivo, como data centers grandes. Para obter maior eficiência de energia, considere o uso de notificações baseadas em eventos em vez de notificações baseadas em tempo em seu aplicativo. Se um temporizador for necessário, use um temporizador que seja sinalizado uma vez em vez de um temporizador periódico ou defina o intervalo como um valor maior que um segundo.

 

Um thread usa a função [**CreateWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw) ou [**CreateWaitableTimerEx**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerexw) para criar um objeto de temporizador. O thread de criação especifica se o temporizador é um temporizador de redefinição manual ou um temporizador de sincronização. O thread de criação pode especificar um nome para o objeto de timer. Os threads em outros processos podem abrir um identificador para um temporizador existente especificando seu nome em uma chamada para a função [**OpenWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-openwaitabletimerw) . Qualquer thread com um identificador para um objeto de timer pode usar uma das [funções Wait](wait-functions.md) para aguardar que o estado do timer seja definido como signaled.

-   O thread chama a função [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer) para ativar o temporizador. Observe o uso dos seguintes parâmetros para **SetWaitableTimer**:
-   Use o parâmetro *lpDueTime* para especificar a hora em que o temporizador deve ser definido para o estado sinalizado. Quando um temporizador de redefinição manual é definido como o estado sinalizado, ele permanece nesse estado até que [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer) estabeleça um novo tempo de conclusão. Quando um temporizador de sincronização é definido como o estado sinalizado, ele permanece nesse estado até que um thread conclua uma operação de espera no objeto de timer.
-   Use o parâmetro *lPeriod* da função [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer) para especificar o período do temporizador. Se o período não for zero, o temporizador será um temporizador periódico; Ele é reativado toda vez que o período expira, até que o temporizador seja redefinido ou cancelado. Se o período for zero, o temporizador não será um temporizador periódico; Ela é sinalizada uma vez e, em seguida, desativada.

Um thread pode usar a função [**CancelWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-cancelwaitabletimer) para definir o temporizador para o estado inativo. Para redefinir o temporizador, chame [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer). Quando terminar com o objeto de timer, chame [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) para fechar o identificador para o objeto de timer.

O comportamento de um temporizador de espera pode ser resumido da seguinte maneira:

-   Quando um temporizador é definido, ele é cancelado se já estava ativo, o estado do temporizador não é sinalizado e o temporizador é colocado na fila de timer do kernel.
-   Quando um temporizador expira, o temporizador é definido como o estado sinalizado. Se o temporizador tiver uma rotina de conclusão, ela será enfileirada para o thread que define o temporizador. A rotina de conclusão permanece na fila da APC ( [chamada de procedimento assíncrono](asynchronous-procedure-calls.md) ) do thread até que o thread Insira um estado de espera de alerta. Nesse momento, a APC é despachada e a rotina de conclusão é chamada. Se o temporizador for periódico, ele será colocado de volta na fila de timer do kernel.
-   Quando um temporizador é cancelado, ele é removido da fila de timer do kernel se ele estava pendente. Se o temporizador tiver expirado e ainda houver uma APC na fila para o thread que definiu o temporizador, a APC será removida da fila da APC do thread. O estado sinalizado do temporizador não é afetado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Chamadas de procedimento assíncrono](asynchronous-procedure-calls.md)
</dt> <dt>

[Usando objetos de timer de espera](using-waitable-timer-objects.md)
</dt> </dl>

 

 
