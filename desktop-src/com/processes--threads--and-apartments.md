---
title: Processos, threads e Apartments
description: Um processo é uma coleção de espaço de memória virtual, código, dados e recursos do sistema.
ms.assetid: cb62412a-d079-40f9-89dc-cce0bf3889af
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d598fc9d7dd39ab070b58aa7ba45a6e2fcae90db
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104366747"
---
# <a name="processes-threads-and-apartments"></a>Processos, threads e Apartments

Um *processo* é uma coleção de espaço de memória virtual, código, dados e recursos do sistema. Um *thread* é um código que deve ser executado em série em um processo. Um processador executa threads, não processos, para que cada aplicativo tenha pelo menos um processo, e um processo sempre tenha pelo menos um thread de execução, conhecido como thread primário. Um processo pode ter vários threads além do thread principal.

Os processos se comunicam entre si por meio de mensagens, usando a tecnologia RPC (chamada de procedimento remoto) da Microsoft para passar informações entre si. Não há nenhuma diferença para o chamador entre uma chamada proveniente de um processo em um computador remoto e uma chamada proveniente de outro processo no mesmo computador.

Quando um thread começa a ser executado, ele continua até ser eliminado ou até ser interrompido por um thread com prioridade mais alta (por uma ação do usuário ou o Agendador de threads do kernel). Cada thread pode executar seções separadas de código ou vários threads podem executar a mesma seção de código. Os threads que executam o mesmo bloco de código mantêm pilhas separadas. Cada thread em um processo compartilha as variáveis e os recursos globais do processo.

O Agendador de thread determina quando e com que frequência executar um thread, de acordo com uma combinação do atributo de classe de prioridade do processo e a prioridade base do thread. Você define o atributo de classe de prioridade de um processo chamando a função [**SetPriorityClass**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setpriorityclass) e define a prioridade base de um thread com uma chamada para [**SetThreadPriority**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setthreadpriority).

Os aplicativos multissegmentados devem evitar dois problemas de Threading: *deadlocks* e *corridas*. Um deadlock ocorre quando cada thread está aguardando que o outro faça algo. O controle de chamada COM ajuda a impedir deadlocks em chamadas entre objetos. Uma condição de corrida ocorre quando um thread termina antes de outro em que ele depende, fazendo com que o primeiro use um valor não inicializado porque o último ainda não forneceu um válido. O COM fornece algumas funções projetadas especificamente para ajudar a evitar condições de corrida em servidores fora do processo. (Consulte [auxiliares de implementação do servidor fora do processo](out-of-process-server-implementation-helpers.md).)

## <a name="the-apartment-and-the-com-threading-architecture"></a>A arquitetura de threading de apartamento e COM

Embora o COM ofereça suporte à predominante do modelo de thread único por processo antes da introdução de vários threads de execução, você pode escrever código para tirar proveito de vários threads, resultando em aplicativos mais eficientes, permitindo que um thread seja executado enquanto outro thread aguarda a conclusão de uma operação demorada.

> [!Note]  
> O uso de vários threads não é uma garantia de melhor desempenho. Na verdade, como o fatoração de thread é um problema difícil, o uso de vários threads geralmente causa problemas de desempenho. A chave é usar vários threads somente se você tiver certeza do que está fazendo.

 

Em geral, a maneira mais simples de exibir a arquitetura de Threading COM é considerar todos os objetos COM no processo, conforme dividido em grupos chamados *Apartments*. Um objeto COM reside exatamente em um apartamento, no sentido de que seus métodos podem ser chamados legalmente apenas por um thread que pertence a esse apartamento. Qualquer outro thread que queira chamar o objeto deve passar por um proxy.

Há dois tipos de Apartments: [Apartments de thread único](single-threaded-apartments.md)e [Apartments multithread](multithreaded-apartments.md).

-   O Apartments de thread único consiste em exatamente um thread, de modo que todos os objetos COM que residem em um apartamento single-thread pode receber chamadas de método somente de um thread que pertence a esse apartamento. Todas as chamadas de método para um objeto COM em um apartamento de thread único são sincronizadas com a fila de mensagens do Windows para o thread de apartment de thread único. Um processo com um único thread de execução é simplesmente um caso especial desse modelo.
-   O Apartments multithread consiste em um ou mais threads, de modo que todos os objetos COM que residem em um apartamento multithread podem receber chamadas de método diretamente de qualquer um dos threads que pertencem ao apartamento multi-threaded. Threads em um apartamento multithread usam um modelo chamado *Threading livre*. Chamadas para objetos COM em um apartamento multithread são sincronizadas pelos próprios objetos.

> [!Note]  
> Para obter uma descrição de comunicação entre Apartments de thread único e Apartments multithread no mesmo processo, consulte [comunicação de thread único e multithread](single-threaded-and-multithreaded-communication.md).

 

Um processo pode ter zero ou mais Apartments de thread único e zero ou um apartamento multithread.

Em um processo, o apartamento principal é o primeiro a ser inicializado. Em um processo de thread único, esse é o único apartamento. Os parâmetros de chamada são empacotados entre Apartments e o COM manipula a sincronização por meio de mensagens. Se você designar vários threads em um processo para serem de thread livre, todos os threads livres residirem em um único apartamento, os parâmetros serão passados diretamente para qualquer thread no apartamento e você deverá lidar com toda a sincronização. Em um processo com Threading livre e thread apartment, todos os threads livres residem em um único apartamento e todos os outros Apartments são Apartments de thread único. Um processo que faz trabalho COM é uma coleção de Apartments com, no máximo, um apartamento multi-threaded, mas qualquer número de Apartments de thread único.

Os modelos de threading no COM fornecem o mecanismo para clientes e servidores que usam diferentes arquiteturas de threading para trabalharem juntos. As chamadas entre objetos com modelos de Threading diferentes em processos diferentes são naturalmente suportadas. Da perspectiva do objeto de chamada, todas as chamadas para objetos fora de um processo se comportam de forma idêntica, independentemente de como o objeto que está sendo chamado é threaded. Da mesma forma, da perspectiva do objeto que está sendo chamado, chamadas de chegada se comportam de maneira idêntica, independentemente do modelo de Threading do chamador.

A interação entre um cliente e um objeto fora do processo é simples, mesmo quando eles usam modelos de Threading diferentes porque o cliente e o objeto estão em processos diferentes. COM, entre o cliente e o servidor, o pode fornecer o código para que os modelos de Threading interoperem, usando marshaling padrão e RPC. Por exemplo, se um objeto de thread único for chamado simultaneamente por vários clientes de thread livre, as chamadas serão sincronizadas pelo COM colocando as mensagens de janela correspondentes na fila de mensagens do servidor. O apartamento do objeto receberá uma chamada cada vez que recuperar e enviar mensagens. No entanto, deve-se tomar cuidado para garantir que os servidores em processo interajam corretamente com seus clientes. (Consulte [problemas de thread de servidor em processo](in-process-server-threading-issues.md).)

O problema mais importante na programação com um modelo multi-threaded é tornar seu código seguro para thread, de forma que as mensagens destinadas a um thread específico passem apenas para esse thread e o acesso aos threads seja protegido.

Para mais informações, consulte os seguintes tópicos:

-   [Escolhendo o modelo de Threading](choosing-the-threading-model.md)
-   [Apartments de thread único](single-threaded-apartments.md)
-   [Apartments multithread](multithreaded-apartments.md)
-   [Comunicação de thread único e multithread](single-threaded-and-multithreaded-communication.md)
-   [Problemas de Threading do servidor em processo](in-process-server-threading-issues.md)
-   [Acessando interfaces em Apartments](accessing-interfaces-across-apartments.md)

 

 