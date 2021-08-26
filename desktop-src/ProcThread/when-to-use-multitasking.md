---
description: 'Há duas maneiras de implementar a multitarefa: como um único processo com vários threads ou como vários processos, cada uma com um ou mais threads.'
ms.assetid: ac0a8163-1498-4274-acfc-6a36b4c02a27
title: Quando usar multitarefa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee3e37f63ada4aa1a17355ac3bc5b7361d498a1a20ec87b490965b53c4811ebb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031336"
---
# <a name="when-to-use-multitasking"></a>Quando usar multitarefa

Há duas maneiras de implementar a multitarefa: como um único processo com vários threads ou como vários processos, cada uma com um ou mais threads. Um aplicativo pode colocar cada thread que requer um espaço de endereço privado e recursos privados em seu próprio processo, para protegê-lo contra as atividades de outros threads de processo.

Um processo multithread pode gerenciar tarefas mutuamente exclusivas com threads, como fornecer uma interface do usuário e executar cálculos em segundo plano. A criação de um processo multithread também pode ser uma maneira conveniente de estruturar um programa que executa várias tarefas semelhantes ou idênticas simultaneamente. Por exemplo, um servidor de pipe nomeado pode criar um thread para cada processo de cliente anexado ao pipe. Esse thread gerencia a comunicação entre o servidor e o cliente. Seu processo pode usar vários threads para realizar as seguintes tarefas:

-   Gerenciar a entrada para várias janelas.
-   Gerenciar a entrada de vários dispositivos de comunicação.
-   Diferenciar as tarefas de prioridade variada. Por exemplo, um thread de alta prioridade gerencia tarefas cujo tempo é algo crítico e um thread de baixa prioridade executa outras tarefas.
-   Permitir que a interface do usuário continue responsiva, durante a alocação de tempo a tarefas em segundo plano.

Normalmente, é mais eficiente para um aplicativo implementar multitarefa criando um único processo multithread, em vez de criar vários processos, pelos seguintes motivos:

-   O sistema pode executar uma opção de contexto mais rapidamente para threads do que processos, porque um processo tem mais sobrecarga do que um thread (o contexto do processo é maior que o contexto de thread).
-   Todos os threads de um processo compartilham o mesmo espaço de endereço e podem acessar as variáveis globais do processo, o que pode simplificar a comunicação entre threads.
-   Todos os threads de um processo podem compartilhar alças abertas para recursos, como arquivos e pipes.

Há outras técnicas que você pode usar no lugar de multithreading. Os mais significativos são: entrada e saída assíncronas (E/S), portas de conclusão de E/S, APC (chamadas de procedimento assíncrono) e a capacidade de aguardar vários eventos.

Um único thread pode iniciar várias solicitações de E/S demoradas que podem ser executados simultaneamente usando E/S assíncrona. A E/S assíncrona pode ser executada em arquivos, pipes e dispositivos de comunicação serial. Para obter mais informações, consulte [Synchronization and Overlapped Input and Output](../sync/synchronization-and-overlapped-input-and-output.md).

Um único thread pode bloquear sua própria execução enquanto aguarda que um ou todos os vários eventos ocorram. Isso é mais eficiente do que usar vários threads, cada um aguardando um único evento e mais eficiente do que usar um único thread que consome tempo do processador verificando continuamente se eventos ocorrem. Para obter mais informações, consulte [Funções de espera.](../sync/wait-functions.md)

 

 
