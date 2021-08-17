---
description: Para evitar condições de corrida e deadlocks, é necessário sincronizar o acesso por vários threads a recursos compartilhados. A sincronização também é necessária para garantir que o código interdependente seja executado na sequência adequada.
ms.assetid: 74af0502-dae1-438c-8e4b-7663093b3fe3
title: Sincronizando a execução de vários threads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c04a7e80f3c1d4ffdd874d9627a8212e26ee4923a5f2349bdebc4ff09299936c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117793089"
---
# <a name="synchronizing-execution-of-multiple-threads"></a>Sincronizando a execução de vários threads

Para evitar condições de corrida e deadlocks, é necessário sincronizar o acesso por vários threads a recursos compartilhados. A sincronização também é necessária para garantir que o código interdependente seja executado na sequência adequada.

Há vários objetos cujos alças podem ser usados para sincronizar vários threads. Esses objetos incluem:

-   Buffers de entrada do console
-   Eventos
-   Mutexes
-   Processos
-   Semáforos
-   Threads
-   Temporizadores

O estado de cada um desses objetos é sinalizado ou não sinalizado. Quando você especifica um identificador para qualquer um desses objetos em uma chamada para uma das funções de espera [,](../sync/wait-functions.md)a execução do thread de chamada é bloqueada até que o estado do objeto especificado seja sinalizado.

Alguns desses objetos são úteis para bloquear um thread até que ocorra algum evento. Por exemplo, uma alça de buffer de entrada do console é sinalizada quando há entrada não lida, como um clique de botão de tecla ou do mouse. As alças de processo e thread são sinalizadas quando o processo ou o thread é encerrado. Isso permite que um processo, por exemplo, crie um processo filho e, em seguida, bloqueie sua própria execução até que o novo processo seja encerrado.

Outros objetos são úteis na proteção de recursos compartilhados contra acesso simultâneo. Por exemplo, vários threads podem ter um identificador para um objeto mutex. Antes de acessar um recurso compartilhado, os [](../sync/wait-functions.md) threads devem chamar uma das funções de espera para aguardar o estado do mutex ser sinalizado. Quando o mutex é sinalizado, apenas um thread em espera é liberado para acessar o recurso. O estado do mutex é redefinido imediatamente para não sinalizado para que outros threads em espera permaneçam bloqueados. Quando o thread é concluído com o recurso, ele deve definir o estado do mutex como sinalizado para permitir que outros threads acessem o recurso.

Para os threads de um único processo, objetos de seção crítica fornecem um meio de sincronização mais eficiente do que mutexes. Uma seção crítica é usada como um mutex para habilitar um thread por vez a usar o recurso protegido. Um thread pode usar a [**função EnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-entercriticalsection) para solicitar a propriedade de uma seção crítica. Se ele já pertence a outro thread, o thread solicitante será bloqueado. Um thread pode usar a [**função TryEnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-tryentercriticalsection) para solicitar a propriedade de uma seção crítica, sem bloquear após falha ao obter a seção crítica. Depois de receber a propriedade, o thread fica livre para usar o recurso protegido. A execução dos outros threads do processo não é afetada, a menos que eles tentem inserir a mesma seção crítica.

A [**função WaitForInputIdle**](/windows/desktop/api/Winuser/nf-winuser-waitforinputidle) faz com que um thread aguarde até que um processo especificado seja inicializado e aguarde a entrada do usuário sem entrada pendente. Chamar **WaitForInputIdle** pode ser útil para sincronizar processos pai e filho, pois [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) retorna sem esperar que o processo filho conclua sua inicialização.

Para obter mais informações, consulte [Synchronization](../sync/synchronization.md).

 

 
