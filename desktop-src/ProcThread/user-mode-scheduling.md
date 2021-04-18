---
description: O UMS (agendamento de modo de usuário) é um mecanismo leve que os aplicativos podem usar para agendar seus próprios threads.
ms.assetid: f9dd92fe-6d7a-452c-893e-e6df1757e377
title: Agendamento de User-Mode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3ceea3c4d4e40d73f48414d074bcb5b4f6e911d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757740"
---
# <a name="user-mode-scheduling"></a>Agendamento de User-Mode

O UMS (agendamento de modo de usuário) é um mecanismo leve que os aplicativos podem usar para agendar seus próprios threads. Um aplicativo pode alternar entre threads UMS no modo de usuário sem envolver o [Agendador do sistema](scheduling.md) e reobter o controle do processador se um thread UMS for bloqueado no kernel. Threads UMS diferem de [fibras](fibers.md) em que cada thread UMS tem seu próprio contexto de thread em vez de compartilhar o contexto de thread de um único thread. A capacidade de alternar entre threads no modo de usuário torna o UMS mais eficiente do que os [pools de threads](thread-pools.md) para gerenciar grandes números de itens de trabalho de curta duração que exigem poucas chamadas do sistema.

O UMS é recomendado para aplicativos com requisitos de alto desempenho que precisam executar com eficiência vários threads simultaneamente em sistemas multiprocessadores ou de vários núcleos. Para tirar proveito do UMS, um aplicativo deve implementar um componente do Agendador que gerencia os threads do UMS do aplicativo e determina quando eles devem ser executados. Os desenvolvedores devem considerar se os requisitos de desempenho do aplicativo justificam o trabalho envolvido no desenvolvimento desse componente. Os aplicativos com requisitos de desempenho moderado podem ser melhor atendidos permitindo que o Agendador do sistema agende seus threads.

O UMS está disponível para aplicativos de 64 bits executados em versões de 64 bits do Windows 7 e Windows Server 2008 R2 ou versões mais recentes de 64 bits do Windows. Esse recurso não está disponível nas versões de 32 bits do Windows.

Para obter detalhes, consulte as seguintes seções:

-   [Agendador de UMS](#ums-scheduler)
-   [Thread do Agendador do UMS](#ums-scheduler-thread)
-   [UMS threads de trabalho, contextos de thread e listas de conclusão](#ums-worker-threads-thread-contexts-and-completion-lists)
-   [Função de ponto de entrada do Agendador UMS](#ums-scheduler-entry-point-function)
-   [Execução de thread UMS](#ums-thread-execution)
-   [Práticas recomendadas do UMS](#ums-best-practices)

## <a name="ums-scheduler"></a>Agendador de UMS

O Agendador UMS de um aplicativo é responsável por criar, gerenciar e excluir threads UMS e determinar qual thread do UMS executar. O Agendador de um aplicativo executa as seguintes tarefas:

-   Cria um thread do Agendador UMS para cada processador no qual o aplicativo executará UMS threads de trabalho.
-   Cria threads de trabalho do UMS para executar o trabalho do aplicativo.
-   Mantém sua própria fila de threads prontas para threads de trabalho que estão prontos para execução e seleciona threads para execução com base nas políticas de agendamento do aplicativo.
-   Cria e monitora uma ou mais listas de conclusão em que o sistema enfileira threads depois de concluir o processamento no kernel. Isso inclui threads de trabalho recém-criados e threads anteriormente bloqueados em uma chamada do sistema que se tornam desbloqueados.
-   Fornece uma função de ponto de entrada do Agendador para manipular notificações do sistema. O sistema chama a função de ponto de entrada quando um thread do Agendador é criado, quando um thread de trabalho é bloqueado em uma chamada do sistema ou quando um thread de trabalho concede explicitamente o controle.
-   Executa tarefas de limpeza para threads de trabalho que concluíram a execução.
-   Executa um desligamento ordenado do Agendador quando solicitado pelo aplicativo.

## <a name="ums-scheduler-thread"></a>Thread do Agendador do UMS

Um thread do Agendador do UMS é um thread comum que foi convertido em UMS chamando a função [**EnterUmsSchedulingMode**](/windows/desktop/api/WinBase/nf-winbase-enterumsschedulingmode) . O Agendador do sistema determina quando o thread do Agendador do UMS é executado com base em sua prioridade em relação a outros threads prontos. O processador no qual o thread do Agendador é executado é influenciado pela afinidade do thread, o mesmo que para threads não UMS.

O chamador de [**EnterUmsSchedulingMode**](/windows/desktop/api/WinBase/nf-winbase-enterumsschedulingmode) especifica uma lista de conclusão e uma função de ponto de entrada [*UmsSchedulerProc*](/windows/desktop/api/WinNT/nc-winnt-rtl_ums_scheduler_entry_point) para associar ao thread do Agendador do ums. O sistema chama a função de ponto de entrada especificada quando termina de converter o thread de chamada para UMS. A função de ponto de entrada do Agendador é responsável por determinar a próxima ação apropriada para o thread especificado. Para obter mais informações, consulte [função de ponto de entrada do Agendador ums](#ums-scheduler-entry-point-function) mais adiante neste tópico.

Um aplicativo pode criar um thread do Agendador UMS para cada processador que será usado para executar threads do UMS. O aplicativo também pode definir a afinidade de cada thread do Agendador do UMS para um processador lógico específico, o que tende a excluir threads não relacionados de serem executados no processador, preservando-os efetivamente para esse thread do Agendador. Lembre-se de que definir a afinidade de thread dessa maneira pode afetar o desempenho geral do sistema por meio da falta de outros processos que possam estar em execução no sistema. Para obter mais informações sobre afinidade de thread, consulte [vários processadores](multiple-processors.md).

## <a name="ums-worker-threads-thread-contexts-and-completion-lists"></a>UMS threads de trabalho, contextos de thread e listas de conclusão

Um thread de trabalho do UMS é criado chamando [**CreateRemoteThreadEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethreadex) com o atributo de thread proc \_ ums de \_ \_ \_ thread e especificando um contexto de thread UMS e uma lista de conclusão.

Um contexto de thread UMS representa o estado de thread UMS de um thread de trabalho e é usado para identificar o thread de trabalho nas chamadas de função UMS. Ele é criado chamando [**CreateUmsThreadContext**](/windows/desktop/api/WinBase/nf-winbase-createumsthreadcontext).

Uma lista de conclusão é criada chamando a função [**CreateUmsCompletionList**](/windows/desktop/api/WinBase/nf-winbase-createumscompletionlist) . Uma lista de conclusão recebe threads de trabalho UMS que concluíram a execução no kernel e estão prontas para execução no modo de usuário. Somente o sistema pode enfileirar threads de trabalho para uma lista de conclusão. Novos threads de trabalho do UMS são automaticamente enfileirados para a lista de conclusão especificada quando os threads foram criados. Os threads de trabalho bloqueados anteriormente também são enfileirados na lista de conclusão quando não estão mais bloqueados.

Cada thread do Agendador do UMS é associado a uma única lista de conclusão. No entanto, a mesma lista de conclusão pode ser associada a qualquer número de threads do Agendador UMS, e um thread do Agendador pode recuperar contextos UMS de qualquer lista de conclusão para a qual ele tem um ponteiro.

Cada lista de conclusão tem um evento associado que é sinalizado pelo sistema quando ele enfileira um ou mais threads de trabalho em uma lista vazia. A função [**GetUmsCompletionListEvent**](/windows/desktop/api/WinBase/nf-winbase-getumscompletionlistevent) recupera um identificador para o evento para uma lista de conclusão especificada. Um aplicativo pode aguardar mais de um evento de lista de conclusão junto com outros eventos que fazem sentido para o aplicativo.

## <a name="ums-scheduler-entry-point-function"></a>Função de ponto de entrada do Agendador UMS

A função de ponto de entrada do Agendador de um aplicativo é implementada como uma função [*UmsSchedulerProc*](/windows/desktop/api/WinNT/nc-winnt-rtl_ums_scheduler_entry_point) . O sistema chama a função de ponto de entrada do Agendador do aplicativo nos seguintes horários:

-   Quando um thread não UMS é convertido em um thread do Agendador do UMS chamando [**EnterUmsSchedulingMode**](/windows/desktop/api/WinBase/nf-winbase-enterumsschedulingmode).
-   Quando um thread de trabalho do UMS chama [**UmsThreadYield**](/windows/desktop/api/WinBase/nf-winbase-umsthreadyield).
-   Quando um thread de trabalho do UMS é bloqueado em um serviço do sistema, como uma chamada do sistema ou uma falha de página.

O parâmetro *Reason* da função [*UmsSchedulerProc*](/windows/desktop/api/WinNT/nc-winnt-rtl_ums_scheduler_entry_point) especifica o motivo pelo qual a função de ponto de entrada foi chamada. Se a função de ponto de entrada foi chamada porque um novo thread do Agendador UMS foi criado, o parâmetro *SchedulerParam* contém dados especificados pelo chamador de [**EnterUmsSchedulingMode**](/windows/desktop/api/WinBase/nf-winbase-enterumsschedulingmode). Se a função de ponto de entrada foi chamada porque um thread de trabalho UMS foi produzido, o parâmetro *SchedulerParam* conterá dados especificados pelo chamador de [**UmsThreadYield**](/windows/desktop/api/WinBase/nf-winbase-umsthreadyield). Se a função de ponto de entrada foi chamada porque um thread de trabalho do UMS foi bloqueado no kernel, o parâmetro *SchedulerParam* é nulo.

A função de ponto de entrada do Agendador é responsável por determinar a próxima ação apropriada para o thread especificado. Por exemplo, se um thread de trabalho estiver bloqueado, a função de ponto de entrada do Agendador poderá executar o próximo thread de trabalho do UMS Ready disponível.

Quando a função de ponto de entrada do Agendador é chamada, o Agendador do aplicativo deve tentar recuperar todos os itens em sua lista de conclusão associada chamando a função [**DequeueUmsCompletionListItems**](/windows/desktop/api/WinBase/nf-winbase-dequeueumscompletionlistitems) . Essa função recupera uma lista de contextos de thread UMS que concluíram o processamento no kernel e estão prontos para execução no modo de usuário. O Agendador do aplicativo não deve executar threads UMS diretamente desta lista porque isso pode causar um comportamento imprevisível no aplicativo. Em vez disso, o Agendador deve recuperar todos os contextos de thread UMS chamando a função [**GetNextUmsListItem**](/windows/desktop/api/WinBase/nf-winbase-getnextumslistitem) uma vez para cada contexto, inserir os contextos de thread UMS na fila de threads pronta do Agendador e, em seguida, executar threads de ums da fila de threads pronta.

Se o Agendador não precisar aguardar vários eventos, ele deverá chamar [**DequeueUmsCompletionListItems**](/windows/desktop/api/WinBase/nf-winbase-dequeueumscompletionlistitems) com um parâmetro de tempo limite diferente de zero para que a função aguarde o evento da lista de conclusão antes de retornar. Se o Agendador precisar aguardar vários eventos de lista de conclusão, ele deverá chamar **DequeueUmsCompletionListItems** com um parâmetro de tempo limite igual a zero para que a função retorne imediatamente, mesmo se a lista de conclusão estiver vazia. Nesse caso, o Agendador pode aguardar explicitamente nos eventos da lista de conclusão, por exemplo, usando [**WaitForMultipleObjects**](/windows/win32/api/synchapi/nf-synchapi-waitformultipleobjects).

## <a name="ums-thread-execution"></a>Execução de thread UMS

Um thread de trabalho UMS criado recentemente é enfileirado na lista de conclusão especificada e não começa a ser executado até que o Agendador UMS do aplicativo o Selecione. Isso difere dos threads não UMS, que o Agendador do sistema agendará automaticamente para ser executado, a menos que o chamador crie explicitamente o thread suspenso.

O Agendador executa um thread de trabalho chamando [**ExecuteUmsThread**](/windows/desktop/api/WinBase/nf-winbase-executeumsthread) com o contexto ums do thread de trabalho. Um thread de trabalho do UMS é executado até que ele resulte chamando a função [**UmsThreadYield**](/windows/desktop/api/WinBase/nf-winbase-umsthreadyield) , bloqueia ou termina.

## <a name="ums-best-practices"></a>Práticas recomendadas do UMS

Os aplicativos que implementam o UMS devem seguir estas práticas recomendadas:

-   As estruturas subjacentes para contextos de thread UMS são gerenciadas pelo sistema e não devem ser modificadas diretamente. Em vez disso, use [**QueryUmsThreadInformation**](/windows/desktop/api/WinBase/nf-winbase-queryumsthreadinformation) e [**SetUmsThreadInformation**](/windows/desktop/api/WinBase/nf-winbase-setumsthreadinformation) para recuperar e definir informações sobre um thread de trabalho do ums.
-   Para ajudar a evitar deadlocks, o thread do Agendador do UMS não deve compartilhar bloqueios com threads de trabalho do UMS. Isso inclui bloqueios criados por aplicativos e bloqueios do sistema que são adquiridos indiretamente por operações como alocar a partir do heap ou carregar DLLs. Por exemplo, suponha que o Agendador execute um thread de trabalho do UMS que carrega uma DLL. O thread de trabalho adquire o bloqueio e os blocos do carregador. O sistema chama a função de ponto de entrada do Agendador, que, em seguida, carrega uma DLL. Isso causa um deadlock, porque o bloqueio do carregador já está mantido e não pode ser liberado até que o primeiro thread seja desbloqueado. Para ajudar a evitar esse problema, delegue o trabalho que pode compartilhar bloqueios com threads de trabalho do UMS para um thread de trabalho UMS dedicado ou um thread que não seja de UMS.
-   O UMS é mais eficiente quando a maioria dos processamentos é feita no modo de usuário. Sempre que possível, evite fazer chamadas do sistema em threads de trabalho do UMS.
-   Os threads de trabalho do UMS não devem assumir que o Agendador do sistema está sendo usado. Essa suposição pode ter efeitos sutis; por exemplo, se um thread no código desconhecido definir uma prioridade ou afinidade de thread, o Agendador UMS ainda poderá substituí-lo. O código que assume que o Agendador do sistema está sendo usado pode não se comportar conforme o esperado e pode ser interrompido quando chamado por um thread UMS.
-   O sistema pode precisar bloquear o contexto de thread de um thread de trabalho do UMS. Por exemplo, uma APC (chamada de procedimento assíncrono) do modo kernel pode alterar o contexto do thread UMS, portanto, o contexto do thread deve ser bloqueado. Se o Agendador tentar executar o contexto do thread UMS enquanto ele estiver bloqueado, a chamada falhará. Esse comportamento é por design, e o Agendador deve ser projetado para tentar novamente o acesso ao contexto do thread UMS.

 

 
