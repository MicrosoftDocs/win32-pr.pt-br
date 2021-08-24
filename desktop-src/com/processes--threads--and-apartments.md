---
title: Processos, threads e apartments
description: Um processo é uma coleção de espaço de memória virtual, código, dados e recursos do sistema.
ms.assetid: cb62412a-d079-40f9-89dc-cce0bf3889af
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 320b09d76200739c77c7202af4d53a35089b2eca2e6fd282dd507f048aa7a10b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130028"
---
# <a name="processes-threads-and-apartments"></a>Processos, threads e apartments

Um *processo* é uma coleção de espaço de memória virtual, código, dados e recursos do sistema. Um *thread* é um código que deve ser executado em série dentro de um processo. Um processador executa threads, não processos, portanto, cada aplicativo tem pelo menos um processo e um processo sempre tem pelo menos um thread de execução, conhecido como thread primário. Um processo pode ter vários threads além do thread primário.

Os processos se comunicam entre si por meio de mensagens, usando a tecnologia RPC (Chamada de Procedimento Remoto) da Microsoft para passar informações entre si. Não há nenhuma diferença para o chamador entre uma chamada proveniente de um processo em um computador remoto e uma chamada proveniente de outro processo no mesmo computador.

Quando um thread começa a ser executado, ele continua até que seja interrompido ou até que seja interrompido por um thread com prioridade mais alta (por uma ação do usuário ou pelo agendador de threads do kernel). Cada thread pode executar seções separadas do código ou vários threads podem executar a mesma seção de código. Os threads que executam o mesmo bloco de código mantêm pilhas separadas. Cada thread em um processo compartilha as variáveis e os recursos globais do processo.

O agendador de thread determina quando e com que frequência executar um thread, de acordo com uma combinação do atributo de classe de prioridade do processo e a prioridade base do thread. Você definirá o atributo de classe de prioridade de um processo chamando a função [**SetPriorityClass**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setpriorityclass) e definirá a prioridade base de um thread com uma chamada para [**SetThreadPriority**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setthreadpriority).

Aplicativos multithread devem evitar dois problemas de threading: *deadlocks* e *corridas.* Um deadlock ocorre quando cada thread está aguardando o outro fazer algo. O controle de chamada COM ajuda a evitar deadlocks em chamadas entre objetos . Uma condição de corrida ocorre quando um thread é finalizado antes de outro do qual depende, fazendo com que o primeiro use um valor não reinicializado porque o último ainda não forneceu um válido. O COM fornece algumas funções especificamente projetadas para ajudar a evitar condições de corrida em servidores fora do processo. (Consulte [Auxiliares de implementação de servidor](out-of-process-server-implementation-helpers.md)fora de processo .)

## <a name="the-apartment-and-the-com-threading-architecture"></a>O apartment e a arquitetura de threading COM

Embora o COM dê suporte ao modelo de thread único por processo predominante antes da introdução de vários threads de execução, você pode escrever código para aproveitar vários threads, resultando em aplicativos mais eficientes, permitindo que um thread seja executado enquanto outro thread aguarda a conclusão de alguma operação demorada.

> [!Note]  
> Usar vários threads não é uma garantia de melhor desempenho. Na verdade, como a fatoração de thread é um problema difícil, o uso de vários threads geralmente causa problemas de desempenho. A chave é usar vários threads somente se você tiver certeza do que está fazendo.

 

Em geral, a maneira mais simples de exibir a arquitetura de threading COM é pensar em todos os objetos COM no processo, como divididos em grupos chamados *apartments*. Um objeto COM reside em exatamente um apartment, no sentido de que seus métodos podem ser legalmente chamados diretamente apenas por um thread que pertence a esse apartment. Qualquer outro thread que deseja chamar o objeto deve passar por um proxy.

Há dois tipos de apartments: [apartments](single-threaded-apartments.md)de thread único e [multithreaded apartments](multithreaded-apartments.md).

-   Os apartments de thread único consistem em exatamente um thread, de modo que todos os objetos COM que residam em um apartment de thread único podem receber chamadas de método somente de um thread que pertence a esse apartment. Todas as chamadas de método para um objeto COM em um apartment de thread único são sincronizadas com a fila de mensagens do Windows para o thread do apartment de thread único. Um processo com um único thread de execução é simplesmente um caso especial desse modelo.
-   Os apartments multithreaded consistem em um ou mais threads, de modo que todos os objetos COM que residam em um apartment multithread podem receber chamadas de método diretamente de qualquer um dos threads que pertencem ao apartment multithreaded. Os threads em um apartment multithread usam um modelo chamado *free-threading*. Chamadas para objetos COM em um apartment multithread são sincronizadas pelos próprios objetos.

> [!Note]  
> Para ver uma descrição da comunicação entre apartments de thread único e apartments multithread dentro do mesmo processo, consulte Comunicação de thread único e [multithread.](single-threaded-and-multithreaded-communication.md)

 

Um processo pode ter zero ou mais apartments de thread único e zero ou um apartment multithread.

Em um processo, o apartment principal é o primeiro a ser inicializado. Em um processo de thread único, esse é o único apartment. Os parâmetros de chamada têm marshaling entre apartments e COM lida com a sincronização por meio de mensagens. Se você designar vários threads em um processo para serem threads livres, todos os threads gratuitos residirão em um único apartment, os parâmetros serão passados diretamente para qualquer thread no apartment e você deverá lidar com toda a sincronização. Em um processo com threading livre e threading de apartment, todos os threads gratuitos residem em um único apartment e todos os outros apartments são apartments de thread único. Um processo que faz o trabalho COM é uma coleção de apartments com, no máximo, um apartment multithread, mas qualquer número de apartments de thread único.

Os modelos de threading no COM fornecem o mecanismo para clientes e servidores que usam arquiteturas de threading diferentes para trabalharem juntos. Chamadas entre objetos com modelos de threading diferentes em processos diferentes são naturalmente suportadas. Da perspectiva do objeto de chamada, todas as chamadas a objetos fora de um processo se comportam de forma idêntica, independentemente de como o objeto que está sendo chamado é threaded. Da mesma forma, da perspectiva do objeto que está sendo chamado, as chamadas de chegada se comportam de forma idêntica, independentemente do modelo de threading do chamador.

A interação entre um cliente e um objeto fora do processo é simples, mesmo quando eles usam modelos de threading diferentes porque o cliente e o objeto estão em processos diferentes. O COM, interposto entre o cliente e o servidor, pode fornecer o código para os modelos de threading interoperarem, usando marshaling padrão e RPC. Por exemplo, se um objeto de thread único for chamado simultaneamente por vários clientes de thread livre, as chamadas serão sincronizadas por COM colocando mensagens de janela correspondentes na fila de mensagens do servidor. O apartment do objeto receberá uma chamada sempre que recuperar e expedir mensagens. No entanto, é necessário ter algum cuidado para garantir que os servidores em processo interajam corretamente com seus clientes. (Consulte [Problemas de threading de servidor em processo.)](in-process-server-threading-issues.md)

O problema mais importante na programação com um modelo multithread é tornar seu código thread-safe para que as mensagens destinadas a um thread específico acessem apenas esse thread e o acesso a threads seja protegido.

Para obter mais informações, consulte estes tópicos:

-   [Escolhendo o modelo de threading](choosing-the-threading-model.md)
-   [Apartments de thread único](single-threaded-apartments.md)
-   [Multithreaded Apartments](multithreaded-apartments.md)
-   [Comunicação multithread e single-threaded](single-threaded-and-multithreaded-communication.md)
-   [Problemas de threading de servidor em processo](in-process-server-threading-issues.md)
-   [Acessando interfaces entre apartments](accessing-interfaces-across-apartments.md)

 

 