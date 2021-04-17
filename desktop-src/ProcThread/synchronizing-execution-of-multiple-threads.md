---
description: Para evitar condições de corrida e deadlocks, é necessário sincronizar o acesso por vários threads para recursos compartilhados. A sincronização também é necessária para garantir que o código interdependentes seja executado na sequência correta.
ms.assetid: 74af0502-dae1-438c-8e4b-7663093b3fe3
title: Sincronizando a execução de vários threads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6a1b3dd51d666d507771476792e679f7980fab8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770129"
---
# <a name="synchronizing-execution-of-multiple-threads"></a>Sincronizando a execução de vários threads

Para evitar condições de corrida e deadlocks, é necessário sincronizar o acesso por vários threads para recursos compartilhados. A sincronização também é necessária para garantir que o código interdependentes seja executado na sequência correta.

Há uma série de objetos cujos identificadores podem ser usados para sincronizar vários threads. Esses objetos incluem:

-   Buffers de entrada do console
-   Eventos
-   Mutexes
-   Processos
-   Semáforos
-   Threads
-   Temporizadores

O estado de cada um desses objetos é sinalizado ou não sinalizado. Quando você especifica um identificador para qualquer um desses objetos em uma chamada para uma das [funções de espera](../sync/wait-functions.md), a execução do thread de chamada é bloqueada até que o estado do objeto especificado fique sinalizado.

Alguns desses objetos são úteis no bloqueio de um thread até que ocorra algum evento. Por exemplo, um identificador de buffer de entrada de console é sinalizado quando há entrada não lida, como um clique com o botão do mouse ou tecla. Identificadores de thread e processo são sinalizados quando o processo ou thread é encerrado. Isso permite que um processo, por exemplo, crie um processo filho e, em seguida, bloqueie sua própria execução até que o novo processo seja encerrado.

Outros objetos são úteis para proteger recursos compartilhados de acesso simultâneo. Por exemplo, vários threads podem ter um identificador para um objeto mutex. Antes de acessar um recurso compartilhado, os threads devem chamar uma das [funções Wait](../sync/wait-functions.md) para aguardar o estado do mutex ser sinalizado. Quando o mutex torna-se sinalizado, apenas um thread em espera é liberado para acessar o recurso. O estado do mutex é imediatamente redefinido para não ser sinalizado para que quaisquer outros threads em espera permaneçam bloqueados. Quando o thread é concluído com o recurso, ele deve definir o estado do mutex como sinalizado para permitir que outros threads acessem o recurso.

Para os threads de um único processo, os objetos de seção crítica fornecem um meio mais eficiente de sincronização do que os mutexes. Uma seção crítica é usada como um mutex para habilitar um thread por vez para usar o recurso protegido. Um thread pode usar a função [**EnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-entercriticalsection) para solicitar a propriedade de uma seção crítica. Se já pertencer a outro thread, o thread solicitante será bloqueado. Um thread pode usar a função [**TryEnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-tryentercriticalsection) para solicitar a propriedade de uma seção crítica, sem bloqueio após a falha de obter a seção crítica. Depois de receber a propriedade, o thread está livre para usar o recurso protegido. A execução dos outros threads do processo não é afetada, a menos que eles tentem inserir a mesma seção crítica.

A função [**WaitForInputIdle**](/windows/desktop/api/Winuser/nf-winuser-waitforinputidle) faz um thread aguardar até que um processo especificado seja inicializado e aguardando a entrada do usuário sem nenhuma entrada pendente. Chamar **WaitForInputIdle** pode ser útil para sincronizar processos pai e filho, porque [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) retorna sem esperar que o processo filho conclua sua inicialização.

Para obter mais informações, consulte [sincronização](../sync/synchronization.md).

 

 
