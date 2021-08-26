---
description: O UMS (agendamento de modo de usuário) é um mecanismo leve que os aplicativos podem usar para agendar seus próprios threads.
ms.assetid: f9dd92fe-6d7a-452c-893e-e6df1757e377
title: User-Mode agendamento de User-Mode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8a13b30685dbcbfc4d3d502e02bdbfdc10d15ea1f804cc6a8391073c44ce447
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074236"
---
# <a name="user-mode-scheduling"></a>User-Mode agendamento de User-Mode

O UMS (agendamento de modo de usuário) é um mecanismo leve que os aplicativos podem usar para agendar seus próprios threads. Um aplicativo pode alternar entre threads UMS no modo de usuário sem envolver o agendador do sistema e recuperar o controle do processador se um thread UMS bloquear no kernel. [](scheduling.md) Os threads UMS diferem das [fibra,](fibers.md) já que cada thread UMS tem seu próprio contexto de thread em vez de compartilhar o contexto de thread de um único thread. A capacidade de alternar entre threads no modo de usuário torna o UMS mais eficiente do que [os pools](thread-pools.md) de threads para gerenciar grandes números de itens de trabalho de curta duração que exigem poucas chamadas do sistema.

UMS é recomendado para aplicativos com requisitos de alto desempenho que precisam executar com eficiência muitos threads simultaneamente em sistemas multiprocessador ou multicore. Para aproveitar o UMS, um aplicativo deve implementar um componente do agendador que gerencia os threads UMS do aplicativo e determina quando eles devem ser executados. Os desenvolvedores devem considerar se os requisitos de desempenho do aplicativo justificam o trabalho envolvido no desenvolvimento desse componente. Aplicativos com requisitos de desempenho moderados podem ser melhor atendidos permitindo que o agendador do sistema agende seus threads.

O UMS está disponível para aplicativos de 64 bits em execução em versões de 64 bits do Windows 7 e do Windows Server 2008 R2 ou versões posteriores de 64 bits do Windows. Esse recurso não está disponível em versões de 32 bits do Windows.

Para obter detalhes, consulte as seguintes seções:

-   [Agendador UMS](#ums-scheduler)
-   [Thread do Agendador UMS](#ums-scheduler-thread)
-   [Threads de trabalho UMS, contextos de thread e listas de conclusão](#ums-worker-threads-thread-contexts-and-completion-lists)
-   [Função de ponto de entrada do agendador UMS](#ums-scheduler-entry-point-function)
-   [Execução de thread UMS](#ums-thread-execution)
-   [Práticas recomendadas do UMS](#ums-best-practices)

## <a name="ums-scheduler"></a>Agendador UMS

O agendador UMS de um aplicativo é responsável por criar, gerenciar e excluir threads UMS e determinar qual thread UMS executar. O agendador de um aplicativo executa as seguintes tarefas:

-   Cria um thread do agendador UMS para cada processador no qual o aplicativo executará threads de trabalho UMS.
-   Cria threads de trabalho UMS para executar o trabalho do aplicativo.
-   Mantém sua própria fila de threads de trabalho prontos para ser executado e seleciona threads para executar com base nas políticas de agendamento do aplicativo.
-   Cria e monitora uma ou mais listas de conclusão em que o sistema enfilra threads depois de concluir o processamento no kernel. Isso inclui threads de trabalho recém-criados e threads bloqueados anteriormente em uma chamada do sistema que são desbloqueados.
-   Fornece uma função de ponto de entrada do agendador para lidar com notificações do sistema. O sistema chama a função de ponto de entrada quando um thread do agendador é criado, quando um thread de trabalho é bloco em uma chamada do sistema ou quando um thread de trabalho gera controle explicitamente.
-   Executa tarefas de limpeza para threads de trabalho que finalizaram a execução.
-   Executa um desligamento pedido do agendador quando solicitado pelo aplicativo.

## <a name="ums-scheduler-thread"></a>Thread do Agendador UMS

Um thread do agendador UMS é um thread comum que se converteu em UMS chamando a [**função EnterUmsSchedulingMode.**](/windows/desktop/api/WinBase/nf-winbase-enterumsschedulingmode) O agendador do sistema determina quando o thread do agendador UMS é executado com base em sua prioridade em relação a outros threads prontos. O processador no qual o thread do agendador é executado é influenciado pela afinidade do thread, o mesmo que para threads não UMS.

O chamador [**de EnterUmsSchedulingMode**](/windows/desktop/api/WinBase/nf-winbase-enterumsschedulingmode) especifica uma lista de conclusão e uma função de ponto de [*entrada UmsSchedulerProc*](/windows/desktop/api/WinNT/nc-winnt-rtl_ums_scheduler_entry_point) para associar ao thread do agendador UMS. O sistema chama a função de ponto de entrada especificada quando termina de converter o thread de chamada em UMS. A função de ponto de entrada do agendador é responsável por determinar a próxima ação apropriada para o thread especificado. Para obter mais informações, consulte Função de ponto de entrada [do agendador UMS](#ums-scheduler-entry-point-function) mais adiante neste tópico.

Um aplicativo pode criar um thread do agendador UMS para cada processador que será usado para executar threads UMS. O aplicativo também pode definir a afinidade de cada thread do agendador UMS para um processador lógico específico, que tende a excluir threads não relacionados da execução nesse processador, reservando-o efetivamente para esse thread do agendador. Esteja ciente de que a definição da afinidade de thread dessa maneira pode afetar o desempenho geral do sistema, deixando de lado outros processos que podem estar em execução no sistema. Para obter mais informações sobre afinidade de thread, consulte [Multiple Processors](multiple-processors.md).

## <a name="ums-worker-threads-thread-contexts-and-completion-lists"></a>Threads de trabalho UMS, contextos de thread e listas de conclusão

Um thread de trabalho UMS é criado chamando [**CreateRemoteThreadEx com**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethreadex) o atributo THREAD UMS ATTRIBUTE PROC e especificando um contexto de thread UMS e uma \_ lista de \_ \_ \_ conclusão.

Um contexto de thread UMS representa o estado do thread UMS de um thread de trabalho e é usado para identificar o thread de trabalho em chamadas de função UMS. Ele é criado chamando [**CreateUmsThreadContext.**](/windows/desktop/api/WinBase/nf-winbase-createumsthreadcontext)

Uma lista de conclusão é criada chamando a [**função CreateUmsCompletionList.**](/windows/desktop/api/WinBase/nf-winbase-createumscompletionlist) Uma lista de conclusão recebe threads de trabalho UMS que concluíram a execução no kernel e estão prontos para execução no modo de usuário. Somente o sistema pode enfilar threads de trabalho para uma lista de conclusão. Novos threads de trabalho UMS são automaticamente en ensuados para a lista de conclusão especificada quando os threads foram criados. Threads de trabalho bloqueados anteriormente também são na fila para a lista de conclusão quando não estão mais bloqueados.

Cada thread do agendador UMS está associado a uma única lista de conclusão. No entanto, a mesma lista de conclusão pode ser associada a qualquer número de threads do agendador UMS, e um thread do agendador pode recuperar contextos UMS de qualquer lista de conclusão para a qual tenha um ponteiro.

Cada lista de conclusão tem um evento associado que é sinalizado pelo sistema quando ele enfilfilia um ou mais threads de trabalho para uma lista vazia. A [**função GetUmsCompletionListEvent**](/windows/desktop/api/WinBase/nf-winbase-getumscompletionlistevent) recupera um handle para o evento para uma lista de conclusão especificada. Um aplicativo pode aguardar mais de um evento de lista de conclusão juntamente com outros eventos que fazem sentido para o aplicativo.

## <a name="ums-scheduler-entry-point-function"></a>Função de ponto de entrada do agendador UMS

A função de ponto de entrada do agendador de um aplicativo é implementada como [*uma função UmsSchedulerProc.*](/windows/desktop/api/WinNT/nc-winnt-rtl_ums_scheduler_entry_point) O sistema chama a função de ponto de entrada do agendador do aplicativo nos seguintes horários:

-   Quando um thread não UMS é convertido em um thread de agendador UMS chamando [**EnterUmsSchedulingMode**](/windows/desktop/api/WinBase/nf-winbase-enterumsschedulingmode).
-   Quando um thread de trabalho UMS chama [**UmsThreadYield.**](/windows/desktop/api/WinBase/nf-winbase-umsthreadyield)
-   Quando um thread de trabalho UMS é bloco em um serviço do sistema, como uma chamada do sistema ou uma falha de página.

O *parâmetro* Reason da [*função UmsSchedulerProc*](/windows/desktop/api/WinNT/nc-winnt-rtl_ums_scheduler_entry_point) especifica o motivo pelo qual a função de ponto de entrada foi chamada. Se a função de ponto de entrada tiver sido chamada porque um novo thread do agendador UMS foi criado, o parâmetro *SchedulerParam* conterá dados especificados pelo chamador [**de EnterUmsSchedulingMode.**](/windows/desktop/api/WinBase/nf-winbase-enterumsschedulingmode) Se a função de ponto de entrada foi chamada porque um thread de trabalho UMS yielded, o parâmetro *SchedulerParam* contém dados especificados pelo chamador [**de UmsThreadYield**](/windows/desktop/api/WinBase/nf-winbase-umsthreadyield). Se a função de ponto de entrada tiver sido chamada porque um thread de trabalho UMS foi bloqueado no kernel, o parâmetro *SchedulerParam* será NULL.

A função de ponto de entrada do agendador é responsável por determinar a próxima ação apropriada para o thread especificado. Por exemplo, se um thread de trabalho estiver bloqueado, a função de ponto de entrada do agendador poderá executar o próximo thread de trabalho UMS pronto disponível.

Quando a função de ponto de entrada do agendador é chamada, o agendador do aplicativo deve tentar recuperar todos os itens em sua lista de conclusão associada chamando a função [**DequeueUmsCompletionListItems.**](/windows/desktop/api/WinBase/nf-winbase-dequeueumscompletionlistitems) Essa função recupera uma lista de contextos de thread UMS que finalizaram o processamento no kernel e estão prontos para execução no modo de usuário. O agendador do aplicativo não deve executar threads UMS diretamente dessa lista porque isso pode causar um comportamento imprevisível no aplicativo. Em vez disso, o agendador deve recuperar todos os contextos de thread UMS chamando a função [**GetNextUmsListItem**](/windows/desktop/api/WinBase/nf-winbase-getnextumslistitem) uma vez para cada contexto, inserir os contextos de thread UMS na fila de thread pronta do agendador e executar somente threads UMS da fila de thread pronta.

Se o agendador não precisar aguardar vários eventos, ele deverá chamar [**DequeueUmsCompletionListItems**](/windows/desktop/api/WinBase/nf-winbase-dequeueumscompletionlistitems) com um parâmetro de tempoout não zero para que a função aguarde o evento da lista de conclusão antes de retornar. Se o agendador precisar aguardar vários eventos de lista de conclusão, ele deverá chamar **DequeueUmsCompletionListItems** com um parâmetro de tempoout de zero para que a função retorne imediatamente, mesmo se a lista de conclusão estiver vazia. Nesse caso, o agendador pode aguardar explicitamente os eventos da lista de conclusão, por exemplo, usando [**WaitForMultipleObjects**](/windows/win32/api/synchapi/nf-synchapi-waitformultipleobjects).

## <a name="ums-thread-execution"></a>Execução de thread UMS

Um thread de trabalho UMS recém-criado é na fila para a lista de conclusão especificada e não começa a ser executado até que o agendador UMS do aplicativo o selecione para ser executado. Isso difere dos threads não UMS, que o agendador do sistema agenda automaticamente para ser executado, a menos que o chamador crie explicitamente o thread suspenso.

O agendador executa um thread de trabalho chamando [**ExecuteUmsThread com**](/windows/desktop/api/WinBase/nf-winbase-executeumsthread) o contexto UMS do thread de trabalho. Um thread de trabalho UMS é executado até que ele produza chamando [**a função UmsThreadYield,**](/windows/desktop/api/WinBase/nf-winbase-umsthreadyield) blocos ou termina.

## <a name="ums-best-practices"></a>Práticas recomendadas do UMS

Os aplicativos que implementam UMS devem seguir estas práticas recomendadas:

-   As estruturas subjacentes para contextos de thread UMS são gerenciadas pelo sistema e não devem ser modificadas diretamente. Em vez disso, [**use QueryUmsThreadInformation**](/windows/desktop/api/WinBase/nf-winbase-queryumsthreadinformation) e [**SetUmsThreadInformation**](/windows/desktop/api/WinBase/nf-winbase-setumsthreadinformation) para recuperar e definir informações sobre um thread de trabalho UMS.
-   Para ajudar a evitar deadlocks, o thread do agendador UMS não deve compartilhar bloqueios com threads de trabalho UMS. Isso inclui bloqueios criados pelo aplicativo e bloqueios do sistema adquiridos indiretamente por operações como alocar do heap ou carregar DLLs. Por exemplo, suponha que o agendador executa um thread de trabalho UMS que carrega uma DLL. O thread de trabalho adquire o bloqueio e os blocos do carregador. O sistema chama a função de ponto de entrada do agendador, que carrega uma DLL. Isso causa um deadlock, porque o bloqueio do carregador já está mantido e não pode ser liberado até que o primeiro thread seja desbloqueado. Para ajudar a evitar esse problema, delegar trabalho que pode compartilhar bloqueios com threads de trabalho UMS para um thread de trabalho umS dedicado ou um thread não UMS.
-   O UMS é mais eficiente quando a maioria do processamento é feita no modo de usuário. Sempre que possível, evite fazer chamadas do sistema em threads de trabalho UMS.
-   Os threads de trabalho umS não devem supor que o agendador do sistema está sendo usado. Essa suposição pode ter efeitos sutis; por exemplo, se um thread no código desconhecido define uma prioridade de thread ou afinidade, o agendador UMS ainda poderá substituí-lo. O código que presume que o agendador do sistema está sendo usado pode não se comportar conforme o esperado e pode ser uma quebra quando chamado por um thread UMS.
-   O sistema pode precisar bloquear o contexto de thread de um thread de trabalho UMS. Por exemplo, uma chamada de procedimento assíncrono no modo kernel (APC) pode alterar o contexto do thread UMS, de modo que o contexto de thread deve ser bloqueado. Se o Agendador tentar executar o contexto do thread UMS enquanto ele estiver bloqueado, a chamada falhará. Esse comportamento é por design, e o Agendador deve ser projetado para tentar novamente o acesso ao contexto do thread UMS.

 

 
