---
description: Um objeto de semáforo é um objeto de sincronização que mantém uma contagem entre zero e um valor máximo especificado.
ms.assetid: d9da1d98-a306-4e2d-a149-1eef6a724751
title: Objetos de semáforo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c814be0ab2fafe7fbabfdeca5b640cfb550172a09e465dddc71629dfa5b0068
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118886255"
---
# <a name="semaphore-objects"></a>Objetos de semáforo

Um *objeto de semáforo* é um objeto de sincronização que mantém uma contagem entre zero e um valor máximo especificado. A contagem é decrementada sempre que um thread conclui uma espera pelo objeto de semáforo e incrementada sempre que um thread libera o semáforo. Quando a contagem atinge zero, nenhum outro thread pode aguardar com êxito o estado do objeto de semáforo ser sinalizado. O estado de um semáforo é definido como sinalizado quando a contagem é maior que zero e não sinalizado quando a contagem é zero.

O objeto de semáforo é útil para controlar um recurso compartilhado que pode dar suporte a um número limitado de usuários. Ele atua como uma porta que limita o número de threads que compartilham o recurso a um número máximo especificado. Por exemplo, um aplicativo pode colocar um limite no número de janelas que ele cria. Ele usa um semáforo com uma contagem máxima igual ao limite da janela, diminuindo a contagem sempre que uma janela é criada e incrementando-a sempre que uma janela é fechada. O aplicativo especifica o objeto de semáforo na chamada para uma das funções [de espera](wait-functions.md) antes de cada janela ser criada. Quando a contagem é zero , indicando que o limite da janela foi atingido, a função wait bloqueia a execução do código de criação de janela.

Um thread usa a [**função CreateSemaphore**](/windows/desktop/api/WinBase/nf-winbase-createsemaphorea) [**ou CreateSemaphoreEx**](/windows/desktop/api/WinBase/nf-winbase-createsemaphoreexa) para criar um objeto semáforo. O thread de criação especifica a contagem inicial e o valor máximo da contagem para o objeto . A contagem inicial não deve ser menor que zero nem maior que o valor máximo. O thread de criação também pode especificar um nome para o objeto de semáforo. Threads em outros processos podem abrir um identificador para um objeto de semáforo existente especificando seu nome em uma chamada para a [**função OpenSemaphore.**](/windows/win32/api/synchapi/nf-synchapi-opensemaphorew) Para obter informações adicionais sobre nomes para objetos mutex, evento, semáforo e temporizador, consulte [Sincronização entre processos](interprocess-synchronization.md).

Se mais de um thread estiver aguardando em um semáforo, um thread em espera será selecionado. Não suponha uma ordem FIFO (primeiro a entrar, primeiro a sair). Eventos externos, como APCs de modo kernel, podem alterar a ordem de espera.

Sempre que uma das funções [de](wait-functions.md) espera retorna porque o estado de um semáforo foi definido como sinalizado, a contagem do semáforo é reduzida em um. A [**função ReleaseSemaphore**](/windows/win32/api/synchapi/nf-synchapi-releasesemaphore) aumenta a contagem de um semáforo em um valor especificado. A contagem nunca pode ser menor que zero ou maior que o valor máximo.

A contagem inicial de um semáforo normalmente é definida como o valor máximo. A contagem é então decrementada desse nível à medida que o recurso protegido é consumido. Como alternativa, você pode criar um semáforo com uma contagem inicial de zero para bloquear o acesso ao recurso protegido enquanto o aplicativo está sendo inicializado. Após a inicialização, você pode usar [**ReleaseSemaphore**](/windows/win32/api/synchapi/nf-synchapi-releasesemaphore) para incrementar a contagem para o valor máximo.

Um thread que possui um objeto mutex pode aguardar repetidamente que o mesmo objeto mutex seja sinalizado sem que sua execução seja bloqueada. Um thread que aguarda repetidamente pelo mesmo objeto de semáforo, no entanto, diminui a contagem do semáforo sempre que uma operação de espera é concluída; o thread é bloqueado quando a contagem chega a zero. Da mesma forma, somente o thread que possui um mutex pode chamar com êxito a função [**ReleaseMutex,**](/windows/win32/api/synchapi/nf-synchapi-releasemutex) embora qualquer thread possa usar [**ReleaseSemaphore**](/windows/win32/api/synchapi/nf-synchapi-releasesemaphore) para aumentar a contagem de um objeto de semáforo.

Um thread pode decrementar a contagem de um semáforo mais de uma vez especificando repetidamente o mesmo objeto de semáforo em chamadas para qualquer uma das funções [de espera](wait-functions.md). No entanto, chamar uma das funções de espera de vários objetos com uma matriz que contém vários identificador do mesmo semáforo não resulta em vários decrementos.

Quando terminar de usar o objeto semáforo, chame a [**função CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) para fechar o identificador. O objeto de semáforo é destruído quando seu último identificador foi fechado. Fechar o handle não afeta a contagem de semáforo; portanto, certifique-se de chamar [**ReleaseSemaphore**](/windows/win32/api/synchapi/nf-synchapi-releasesemaphore) antes de fechar o handle ou antes que o processo seja encerrado. Caso contrário, as operações de espera pendentes terão o tempo máximo ou continuarão indefinidamente, dependendo de um valor de tempo-out ter sido especificado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando objetos semáforos](using-semaphore-objects.md)
</dt> </dl>

 

 
