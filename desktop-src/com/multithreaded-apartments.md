---
title: Apartments multithread
description: Apartments multithread
ms.assetid: d3e6acd9-cd5c-4a2c-8526-4f43db3b606b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f69271b4fb6447d48c15fa9005d39020075af09bcc327b12ce539a739c33f8d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047914"
---
# <a name="multithreaded-apartments"></a>Apartments multithread

Em um modelo de apartamento multi-threaded, todos os threads no processo que foram inicializados como de thread livre residem em um único apartamento. Portanto, não há necessidade de realizar marshaling entre threads. Os threads não precisam recuperar e despachar mensagens porque o COM não usa mensagens de janela neste modelo.

Chamadas para métodos de objetos no apartamento multithread podem ser executadas em qualquer thread no apartamento. Não há nenhuma serialização de chamadas; muitas chamadas podem ocorrer no mesmo método ou no mesmo objeto simultaneamente. Os objetos criados no apartamento multithread devem ser capazes de lidar com chamadas em seus métodos de outros threads a qualquer momento.

Como as chamadas para objetos não são serializadas de nenhuma forma, a simultaneidade do objeto multithread oferece o melhor desempenho e aproveita a vantagem do hardware de multiprocessador para a chamada entre threads, processos cruzados e chamadas entre computadores. No entanto, isso significa que o código para objetos deve fornecer sincronização em suas implementações de interface, normalmente por meio do uso de primitivos de sincronização, como objetos de evento, seções críticas, mutexes ou semáforos, que são descritos posteriormente nesta seção. Além disso, como o objeto não controla o tempo de vida dos threads que estão acessando, nenhum estado específico do thread pode ser armazenado no objeto (no armazenamento local do thread).

A seguir estão algumas considerações importantes sobre a sincronização para Apartments multithread:

-   O COM fornece sincronização de chamadas somente para Apartments de thread único.
-   Apartments multithread não recebem chamadas ao fazer chamadas (no mesmo thread).
-   Apartments multithread não podem fazer chamadas com sincronização de entrada.
-   As chamadas assíncronas são convertidas em chamadas síncronas em Apartments multithread.
-   O filtro de mensagem não é chamado para nenhum thread em um apartamento multithread.

Para inicializar um thread como livre de threads, chame [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex), especificando o coinit \_ multi-threaded. Para obter informações sobre threads de servidor em processo, consulte [problemas de thread de servidor em processo](in-process-server-threading-issues.md).

Vários clientes podem chamar simultaneamente, de threads diferentes, um objeto que dá suporte a threads livres. Em servidores de fora de processo de thread livre, COM, por meio do subsistema RPC, o cria um pool de threads no processo do servidor e uma chamada de cliente (ou várias chamadas de cliente) pode ser entregue por qualquer um desses threads a qualquer momento. Um servidor fora do processo também deve implementar a sincronização em sua fábrica de classes. Os objetos de thread livre, em processo, podem receber chamadas diretas de vários threads do cliente.

O cliente pode fazer COM trabalho em vários threads. Todos os threads pertencem ao mesmo apartamento multi-threaded. Os ponteiros de interface são passados diretamente do thread para o thread em um apartamento multithread, portanto, os ponteiros de interface não são empacotados entre seus threads. Os filtros de mensagem (implementações de [**IMessageFilter**](/windows/desktop/api/ObjIdl/nn-objidl-imessagefilter)) não são usados em Apartments multithread. O thread do cliente será suspenso quando fizer uma chamada COM para objetos fora do apartamento e será retomado quando a chamada retornar. As chamadas entre os processos ainda são manipuladas pelo RPC.

Os threads inicializados com o modelo de thread livre devem implementar sua própria sincronização. conforme mencionado anteriormente nesta seção, Windows habilita essa implementação por meio dos primitivos de sincronização a seguir:

-   Os objetos de evento fornecem uma maneira de sinalizar um ou mais threads que um evento ocorreu. Qualquer thread dentro de um processo pode criar um objeto de evento. Um identificador para o evento é retornado pela função de criação de evento, [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa). Depois que um objeto de evento é criado, os threads com um identificador para o objeto podem aguardar nele antes de continuar a execução.
-   As seções críticas são usadas para uma seção de código que requer acesso exclusivo a alguns conjuntos de dados compartilhados antes que ele possa ser executado e que é usado somente pelos threads em um único processo. Uma seção crítica é como uma borboleta através da qual apenas um thread de cada vez pode passar, funcionando da seguinte maneira:
    -   Para garantir que nenhum mais de um thread acesse dados compartilhados, o thread primário de um processo aloca uma estrutura de dados de seção crítica global \_ e inicializa seus membros. Um thread que insere uma seção crítica chama a função [**EnterCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-entercriticalsection) e modifica os membros da estrutura de dados.
    -   Um thread que tenta inserir uma seção crítica chama [**EnterCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-entercriticalsection) que verifica se a estrutura de dados da \_ seção crítica foi modificada. Nesse caso, outro thread está atualmente na seção crítica e o thread subsequente é colocado no modo de suspensão. Um thread que deixa uma seção crítica chama [**LeaveCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-leavecriticalsection), que redefine a estrutura de dados. Quando um thread deixa uma seção crítica, o sistema ativa um dos threads em suspensão, que, em seguida, entra na seção crítica.
-   Os mutexs executam a mesma função que uma seção crítica, exceto que o mutex é acessível para threads em execução em processos diferentes. Possuir um objeto mutex é como ter o andar em um debate. Um processo cria um objeto mutex chamando a função [**CreateMutex**](/windows/desktop/api/synchapi/nf-synchapi-createmutexa) , que retorna um identificador. O primeiro thread solicitando um objeto mutex Obtém a propriedade dele. Quando o thread termina com o mutex, a propriedade passa para outros threads de acordo com a primeira base fornecida pela primeira vez.
-   Os semáforos são usados para manter uma contagem de referência em algum recurso disponível. Um thread cria um semáforo para um recurso chamando a função [**CreateSemaphore**](/windows/desktop/api/winbase/nf-winbase-createsemaphorea) e passando um ponteiro para o recurso, uma contagem de recursos inicial e a contagem máxima de recursos. Essa função retorna um identificador. Um thread solicitando um recurso passa seu identificador de semáforo em uma chamada para a função [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) . O objeto Semaphore pesquisa o recurso para determinar se ele está disponível. Nesse caso, o semáforo decrementa a contagem de recursos e ativa o thread em espera. Se a contagem for zero, o thread permanecerá em suspensão até que outro thread Libere um recurso, fazendo com que o semáforo aumente a contagem para um.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Acessando interfaces em Apartments](accessing-interfaces-across-apartments.md)
</dt> <dt>

[Escolhendo o modelo de Threading](choosing-the-threading-model.md)
</dt> <dt>

[Problemas de Threading do servidor em processo](in-process-server-threading-issues.md)
</dt> <dt>

[Processos, threads e Apartments](processes--threads--and-apartments.md)
</dt> <dt>

[Comunicação de thread único e multithread](single-threaded-and-multithreaded-communication.md)
</dt> <dt>

[Apartments de thread único](single-threaded-apartments.md)
</dt> </dl>

 

 