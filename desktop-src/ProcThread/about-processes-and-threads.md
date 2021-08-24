---
description: Cada processo fornece os recursos necessários para executar um programa.
ms.assetid: 055458cf-9fc7-4a16-be14-1122b3cf0251
title: Sobre Processos e Threads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62cbce9375d3c27fd58d6bab48c11fe2bdb825dfc729c2176dd2f14eba0a958e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032616"
---
# <a name="about-processes-and-threads"></a>Sobre Processos e Threads

Cada *processo* fornece os recursos necessários para executar um programa. Um processo tem um espaço de endereço virtual, um código executável, identificadores abertos para objetos do sistema, um contexto de segurança, um identificador de processo exclusivo, variáveis de ambiente, uma classe de prioridade, tamanhos mínimos e máximos de conjunto de trabalho e pelo menos um thread de execução. Cada processo é iniciado com um único thread, geralmente chamado de *thread primário,* mas pode criar threads adicionais de qualquer um de seus threads.

Um *thread* é a entidade dentro de um processo que pode ser agendado para execução. Todos os threads de um processo compartilham seu espaço de endereço virtual e recursos do sistema. Além disso, cada thread mantém manipuladores de exceção, uma prioridade de agendamento, armazenamento local de thread, um identificador de thread exclusivo e um conjunto de estruturas que o sistema usará para salvar o contexto de thread até que ele seja agendado. O *contexto de thread* inclui o conjunto de registros de computador do thread, a pilha de kernel, um bloco de ambiente de thread e uma pilha de usuário no espaço de endereço do processo do thread. Os threads também podem ter seu próprio contexto de segurança, que pode ser usado para representar clientes.

O Microsoft Windows dá suporte à *multitarefa preemptiva*, que cria o efeito da execução simultânea de vários threads de vários processos. Em um computador multiprocessador, o sistema pode executar simultaneamente tantos threads quanto processadores no computador.

Um *objeto de trabalho* permite que grupos de processos sejam gerenciados como uma unidade. Os objetos de trabalho são objetos que podem ser encontrados, que podem ser controlados por objetos compartilháveis que controlam os atributos dos processos associados a eles. As operações executadas no objeto de trabalho afetam todos os processos associados ao objeto de trabalho.

Um aplicativo pode usar o *pool de threads* para reduzir o número de threads de aplicativo e fornecer gerenciamento dos threads de trabalho. Os aplicativos podem enfilfilar itens de trabalho, associar o trabalho a alças de espera, enfilfilá-los automaticamente com base em um temporizador e associar à E/S.

*O UMS (agendamento de* modo de usuário) é um mecanismo leve que os aplicativos podem usar para agendar seus próprios threads. Um aplicativo pode alternar entre threads UMS no modo de usuário sem envolver o agendador do sistema e recuperar o controle do processador se um thread UMS bloquear no kernel. [](scheduling.md) Cada thread UMS tem seu próprio contexto de thread em vez de compartilhar o contexto de thread de um único thread. A capacidade de alternar entre threads no modo de usuário torna o UMS mais eficiente do que os pools de threads para itens de trabalho de curta duração que exigem poucas chamadas do sistema.

Uma *fibra* é uma unidade de execução que deve ser agendada manualmente pelo aplicativo. As fibra são executados no contexto dos threads que as agendam. Cada thread pode agendar várias fibra. Em geral, as fibra não oferecem vantagens em relação a um aplicativo multithread bem projetado. No entanto, o uso de fibra pode facilitar a portabilidade de aplicativos que foram projetados para agendar seus próprios threads.

Para obter mais informações, consulte estes tópicos:

-   [Multitarefa](multitasking.md)
-   [Agendamento](scheduling.md)
-   [Vários threads](multiple-threads.md)
-   [Processos filho](child-processes.md)
-   [Pools de Threads](thread-pools.md)
-   [Objetos de trabalho](job-objects.md)
-   [Agendamento de modo de usuário](user-mode-scheduling.md)
-   [Fibras](fibers.md)

 

 



