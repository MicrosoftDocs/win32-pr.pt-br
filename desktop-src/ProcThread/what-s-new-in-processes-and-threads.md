---
description: O Windows 7 e o Windows Server 2008 R2 incluem os seguintes novos elementos de programação para processos e threads.
ms.assetid: 69cd8713-b40c-4fec-a256-9c2ee3d73da5
title: O que há de novo em processos e threads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee7dfb708a2890bab1fcd3fd66385f74bd8513b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828352"
---
# <a name="whats-new-in-processes-and-threads"></a>O que há de novo em processos e threads

O Windows 7 e o Windows Server 2008 R2 incluem os seguintes novos elementos de programação para processos e threads.

## <a name="new-capabilities"></a>Novos recursos

As versões de 64 bits do Windows 7 e do Windows Server 2008 R2 dão suporte a mais de 64 processadores lógicos em um único computador. Para obter mais informações, consulte [grupos de processadores](processor-groups.md).

O UMS (agendamento de modo de usuário) é um mecanismo leve que os aplicativos podem usar para agendar seus próprios threads. Para obter mais informações, consulte [agendamento do modo de usuário](user-mode-scheduling.md).

## <a name="new-functions"></a>Novas funções

As novas funções a seguir são usadas com processadores e grupos de processadores.



| Função                                                                                | Descrição                                                                                                                                                          |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateRemoteThreadEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethreadex)<br/>                         | Cria um thread que é executado no espaço de endereço virtual de outro processo e, opcionalmente, especifica atributos estendidos, como afinidade de grupo de processador.<br/> |
| [**GetActiveProcessorCount**](/windows/desktop/api/WinBase/nf-winbase-getactiveprocessorcount)<br/>                   | Retorna o número de processadores ativos em um grupo de processador ou no sistema.<br/>                                                                            |
| [**GetActiveProcessorGroupCount**](/windows/desktop/api/WinBase/nf-winbase-getactiveprocessorgroupcount)<br/>         | Retorna o número de grupos de processadores ativos no sistema.<br/>                                                                                              |
| [**GetCurrentProcessorNumberEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessornumberex)<br/>           | Recupera o grupo de processadores e o número do processador lógico no qual o thread de chamada está em execução.<br/>                                                 |
| [**GetLogicalProcessorInformationEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformationex)<br/> | Recupera informações sobre as relações de processadores lógicos e hardwares relacionados.<br/>                                                                 |
| [**GetMaximumProcessorCount**](/windows/desktop/api/WinBase/nf-winbase-getmaximumprocessorcount)<br/>                 | Retorna o número máximo de processadores lógicos que um grupo de processador ou o sistema pode ter.<br/>                                                           |
| [**GetMaximumProcessorGroupCount**](/windows/desktop/api/WinBase/nf-winbase-getmaximumprocessorgroupcount)<br/>       | Retorna o número máximo de grupos de processadores que o sistema pode ter. <br/>                                                                                 |
| [**GetNumaAvailableMemoryNodeEx**](/windows/desktop/api/WinBase/nf-winbase-getnumaavailablememorynodeex)<br/>         | Recupera a quantidade de memória que está disponível no nó especificado como um valor USHORT.<br/>                                                                 |
| [**GetNumaNodeNumberFromHandle**](/windows/desktop/api/WinBase/nf-winbase-getnumanodenumberfromhandle)<br/>           | Recupera o nó NUMA associado ao dispositivo subjacente para um identificador de arquivo.<br/>                                                                          |
| [**GetNumaNodeProcessorMaskEx**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumanodeprocessormaskex)<br/>             | Recupera a máscara do processador para o nó NUMA especificado como um valor USHORT.<br/>                                                                               |
| [**GetNumaProcessorNodeEx**](/windows/desktop/api/WinBase/nf-winbase-getnumaprocessornodeex)<br/>                     | Recupera o número do nó do processador lógico especificado como um valor USHORT.<br/>                                                                           |
| [**GetNumaProximityNodeEx**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumaproximitynodeex)<br/>                     | Recupera o número do nó como um valor USHORT para o identificador de proximidade especificado.<br/>                                                                       |
| [**GetProcessGroupAffinity**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-getprocessgroupaffinity)<br/>                   | Recupera a afinidade do grupo de processadores do processo especificado.<br/>                                                                                          |
| [**GetProcessorSystemCycleTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getprocessorsystemcycletime)<br/>           | Recupera o tempo de ciclo de cada processador no grupo especificado gasto na execução de DPCs (chamadas de procedimento deferidas) e ISRs (rotinas de serviço de interrupção).<br/>     |
| [**GetThreadGroupAffinity**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-getthreadgroupaffinity)<br/>                     | Recupera a afinidade do grupo de processadores do thread especificado.<br/>                                                                                           |
| [**GetThreadIdealProcessorEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadidealprocessorex)<br/>               | Recupera o número do processador do processador ideal para o thread especificado.<br/>                                                                           |
| [**QueryIdleProcessorCycleTimeEx**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryidleprocessorcycletimeex)<br/>       | Recupera o tempo de ciclo acumulado para o thread ocioso em cada processador lógico no grupo de processador especificado. <br/>                                     |
| [**SetThreadGroupAffinity**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-setthreadgroupaffinity)<br/>                     | Define a afinidade de grupo de processador para o thread especificado.<br/>                                                                                               |
| [**SetThreadIdealProcessorEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadidealprocessorex)<br/>               | Define o processador ideal para o thread especificado e, opcionalmente, recupera o processador ideal anterior.<br/>                                                  |



 

As novas funções a seguir são usadas com pools de threads.



| Função                                                                              | Descrição                                                                                                    |
|---------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**QueryThreadpoolStackInformation**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-querythreadpoolstackinformation)<br/> | Recupera a reserva de pilha e os tamanhos de confirmação para threads no pool de threads especificado.<br/>              |
| [**SetThreadpoolCallbackPersistent**](/windows/desktop/api/WinBase/nf-winbase-setthreadpoolcallbackpersistent)<br/> | Especifica que o retorno de chamada deve ser executado em um thread persistente.<br/>                                      |
| [**SetThreadpoolCallbackPriority**](/windows/desktop/api/WinBase/nf-winbase-setthreadpoolcallbackpriority)<br/>     | Especifica a prioridade de uma função de retorno de chamada relativa a outros itens de trabalho no mesmo pool de threads.<br/> |
| [**SetThreadpoolStackInformation**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolstackinformation)<br/>     | Define a reserva de pilha e os tamanhos de confirmação para novos threads no pool de threads especificado. <br/>              |



 

As novas funções a seguir são usadas com UMS.



| Função                                                                          | Descrição                                                                                                   |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [**CreateUmsCompletionList**](/windows/desktop/api/WinBase/nf-winbase-createumscompletionlist)<br/>             | Cria uma lista de conclusão de UMS.<br/>                                                                     |
| [**CreateUmsThreadContext**](/windows/desktop/api/WinBase/nf-winbase-createumsthreadcontext)<br/>               | Cria um contexto de thread UMS para representar um thread de trabalho do UMS.<br/>                                     |
| [**DeleteUmsCompletionList**](/windows/desktop/api/WinBase/nf-winbase-deleteumscompletionlist)<br/>             | Exclui a lista de conclusão de UMS especificada. A lista deve estar vazia.<br/>                                 |
| [**DeleteUmsThreadContext**](/windows/desktop/api/WinBase/nf-winbase-deleteumsthreadcontext)<br/>               | Exclui o contexto de thread UMS especificado. O thread deve ser encerrado.<br/>                           |
| [**DequeueUmsCompletionListItems**](/windows/desktop/api/WinBase/nf-winbase-dequeueumscompletionlistitems)<br/> | Recupera os threads de trabalho do UMS da lista de conclusão de UMS especificada.<br/>                               |
| [**EnterUmsSchedulingMode**](/windows/desktop/api/WinBase/nf-winbase-enterumsschedulingmode)<br/>               | Converte o thread de chamada em um thread do Agendador UMS.<br/>                                           |
| [**ExecuteUmsThread**](/windows/desktop/api/WinBase/nf-winbase-executeumsthread)<br/>                           | Executa o thread de trabalho do UMS especificado.<br/>                                                              |
| [**GetCurrentUmsThread**](/windows/desktop/api/WinBase/nf-winbase-getcurrentumsthread)<br/>                     | Retorna o contexto do thread UMS do thread de chamada UMS.<br/>                                          |
| [**GetNextUmsListItem**](/windows/desktop/api/WinBase/nf-winbase-getnextumslistitem)<br/>                       | Retorna o próximo contexto de thread UMS em uma lista de contextos de thread UMS.<br/>                              |
| [**GetUmsCompletionListEvent**](/windows/desktop/api/WinBase/nf-winbase-getumscompletionlistevent)<br/>         | Recupera um identificador para o evento associado à lista de conclusão de UMS especificada.<br/>                 |
| [**QueryUmsThreadInformation**](/windows/desktop/api/WinBase/nf-winbase-queryumsthreadinformation)<br/>         | Recupera informações sobre o thread de trabalho do UMS especificado.<br/>                                       |
| [**SetUmsThreadInformation**](/windows/desktop/api/WinBase/nf-winbase-setumsthreadinformation)<br/>             | Define informações de contexto específicas do aplicativo para o thread de trabalho UMS especificado.<br/>                 |
| [*UmsSchedulerProc*](/windows/desktop/api/WinNT/nc-winnt-rtl_ums_scheduler_entry_point)<br/>                             | A função de ponto de entrada do Agendador UMS definida pelo aplicativo associada a uma lista de conclusão de UMS. <br/> |
| [**UmsThreadYield**](/windows/desktop/api/WinBase/nf-winbase-umsthreadyield)<br/>                               | Produz o controle para o thread do Agendador UMS no qual o thread de trabalho de chamada UMS está em execução.<br/>      |



 

## <a name="new-structures"></a>Novas estruturas



| Estrutura                                                                                                 | Descrição                                                                                         |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**relação de CACHE \_**](/windows/desktop/api/WinNT/ns-winnt-cache_relationship)<br/>                                              | Descreve os atributos de cache. <br/>                                                             |
| [**afinidade de grupo \_**](/windows/desktop/api/WinNT/ns-winnt-group_affinity)<br/>                                                      | Contém uma afinidade específica de grupo de processador, como a afinidade de um thread.<br/>          |
| [**relação de grupo \_**](/windows/desktop/api/WinNT/ns-winnt-group_relationship)<br/>                                              | Contém informações sobre grupos de processadores. <br/>                                            |
| [**\_relacionamento de nó numa \_**](/windows/desktop/api/WinNT/ns-winnt-numa_node_relationship)<br/>                                     | Contém informações sobre um nó NUMA em um grupo de processador. <br/>                            |
| [**\_informações do grupo de processador \_**](/windows/desktop/api/WinNT/ns-winnt-processor_group_info)<br/>                                         | Contém o número e a afinidade de processadores em um grupo de processadores.<br/>                     |
| [**número do processador \_**](/windows/desktop/api/WinNT/ns-winnt-processor_number)<br/>                                                  | Representa um processador lógico em um grupo de processadores.<br/>                                     |
| [**relação do processador \_**](/windows/desktop/api/WinNT/ns-winnt-processor_relationship)<br/>                                      | Contém informações sobre a afinidade dentro de um grupo de processador.<br/>                            |
| [**\_informações do processador lógico do sistema \_ \_ \_ ex.**](/windows/desktop/api/WinNT/ns-winnt-system_logical_processor_information_ex)<br/> | Contém informações sobre as relações de processadores lógicos e hardwares relacionados.<br/> |
| [**UMS \_ criar \_ atributos de thread \_**](/windows/desktop/api/WinNT/ns-winnt-ums_create_thread_attributes)<br/>                        | Especifica atributos para um thread de trabalho do UMS. <br/>                                           |
| [**\_informações de inicialização do Agendador ums \_ \_**](/windows/desktop/api/WinBase/ns-winbase-ums_scheduler_startup_info)<br/>                            | Especifica atributos para um thread do Agendador do UMS<br/>                                          |



 

 

 
