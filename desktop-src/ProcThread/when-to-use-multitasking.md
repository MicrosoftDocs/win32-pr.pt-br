---
description: 'Há duas maneiras de implementar multitarefas: como um único processo com vários threads ou vários processos, cada um com um ou mais threads.'
ms.assetid: ac0a8163-1498-4274-acfc-6a36b4c02a27
title: Quando usar multitarefa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b17e52f39a08120d3038663a95307ad72f228cfc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105760806"
---
# <a name="when-to-use-multitasking"></a>Quando usar multitarefa

Há duas maneiras de implementar multitarefas: como um único processo com vários threads ou vários processos, cada um com um ou mais threads. Um aplicativo pode colocar cada thread que exige um espaço de endereço privado e recursos privados em seu próprio processo, para protegê-lo das atividades de outros threads de processo.

Um processo multi-threaded pode gerenciar tarefas mutuamente exclusivas com threads, como fornecer uma interface do usuário e executar cálculos em segundo plano. Criar um processo multi-threaded também pode ser uma maneira conveniente de estruturar um programa que executa várias tarefas semelhantes ou idênticas simultaneamente. Por exemplo, um servidor de pipe nomeado pode criar um thread para cada processo de cliente que é anexado ao pipe. Esse thread gerencia a comunicação entre o servidor e o cliente. Seu processo pode usar vários threads para realizar as seguintes tarefas:

-   Gerencie a entrada para várias janelas.
-   Gerencie a entrada de vários dispositivos de comunicação.
-   Diferenciar as tarefas de prioridade variada. Por exemplo, um thread de alta prioridade gerencia tarefas cujo tempo é algo crítico e um thread de baixa prioridade executa outras tarefas.
-   Permitir que a interface do usuário continue responsiva, durante a alocação de tempo a tarefas em segundo plano.

Normalmente, é mais eficiente que um aplicativo implemente multitarefas criando um único processo multithread, em vez de criar vários processos, pelos seguintes motivos:

-   O sistema pode executar uma alternância de contexto mais rapidamente para threads do que processos, porque um processo tem mais sobrecarga do que um thread faz (o contexto do processo é maior do que o contexto do thread).
-   Todos os threads de um processo compartilham o mesmo espaço de endereço e podem acessar as variáveis globais do processo, o que pode simplificar a comunicação entre threads.
-   Todos os threads de um processo podem compartilhar identificadores abertos para recursos, como arquivos e pipes.

Há outras técnicas que você pode usar no lugar de multithreading. Os mais significativos são os seguintes: entrada e saída assíncrona (e/s), portas de conclusão de e/s, APC (chamadas de procedimento assíncrono) e a capacidade de aguardar vários eventos.

Um único thread pode iniciar várias solicitações de e/s demoradas que podem ser executadas simultaneamente usando e/s assíncronas. A e/s assíncrona pode ser executada em arquivos, Pipes e dispositivos de comunicação serial. Para obter mais informações, consulte [sincronização e entrada e saída sobrepostas](../sync/synchronization-and-overlapped-input-and-output.md).

Um único thread pode bloquear sua própria execução enquanto aguarda a ocorrência de qualquer um ou todos os vários eventos. Isso é mais eficiente do que usar vários threads, cada um esperando por um único evento e mais eficiente do que usar um único thread que consome tempo do processador, verificando continuamente se os eventos ocorrem. Para obter mais informações, consulte [Wait Functions](../sync/wait-functions.md).

 

 
