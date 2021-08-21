---
description: Windows 7 e Windows Server 2008 R2 incluem os novos elementos de programação a seguir para processos e threads.
ms.assetid: 69cd8713-b40c-4fec-a256-9c2ee3d73da5
title: Novidades em processos e threads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efe8b53349f5c6f19dd9beda1ffe6b933fbff63533988a40937453194df57295
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117792954"
---
# <a name="whats-new-in-processes-and-threads"></a>Novidades em processos e threads

Windows 7 e Windows Server 2008 R2 incluem os novos elementos de programação a seguir para processos e threads.

## <a name="new-capabilities"></a>Novos recursos

As versões de 64 bits do Windows 7 e Windows Server 2008 R2 são suportadas por mais de 64 processadores lógicos em um único computador. Para obter mais informações, consulte [Grupos de Processadores](processor-groups.md).

O UMS (agendamento de modo de usuário) é um mecanismo leve que os aplicativos podem usar para agendar seus próprios threads. Para obter mais informações, consulte [Agendamento de modo de usuário.](user-mode-scheduling.md)

## <a name="new-functions"></a>Novas funções

As novas funções a seguir são usadas com processadores e grupos de processadores.



| Função                                                                                | Descrição                                                                                                                                                          |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateRemoteThreadEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethreadex)<br/>                         | Cria um thread que é executado no espaço de endereço virtual de outro processo e, opcionalmente, especifica atributos estendidos, como afinidade de grupo de processadores.<br/> |
| [**GetActiveProcessorCount**](/windows/desktop/api/WinBase/nf-winbase-getactiveprocessorcount)<br/>                   | Retorna o número de processadores ativos em um grupo de processadores ou no sistema.<br/>                                                                            |
| [**GetActiveProcessorGroupCount**](/windows/desktop/api/WinBase/nf-winbase-getactiveprocessorgroupcount)<br/>         | Retorna o número de grupos de processadores ativos no sistema.<br/>                                                                                              |
| [**GetCurrentProcessorNumberEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessornumberex)<br/>           | Recupera o grupo de processadores e o número do processador lógico no qual o thread de chamada está em execução.<br/>                                                 |
| [**GetLogicalProcessorInformationEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformationex)<br/> | Recupera informações sobre as relações de processadores lógicos e hardware relacionado.<br/>                                                                 |
| [**GetMaximumProcessorCount**](/windows/desktop/api/WinBase/nf-winbase-getmaximumprocessorcount)<br/>                 | Retorna o número máximo de processadores lógicos que um grupo de processadores ou o sistema pode ter.<br/>                                                           |
| [**GetMaximumProcessorGroupCount**](/windows/desktop/api/WinBase/nf-winbase-getmaximumprocessorgroupcount)<br/>       | Retorna o número máximo de grupos de processadores que o sistema pode ter. <br/>                                                                                 |
| [**GetNumaAvailableMemoryNodeEx**](/windows/desktop/api/WinBase/nf-winbase-getnumaavailablememorynodeex)<br/>         | Recupera a quantidade de memória disponível no nó especificado como um valor USHORT.<br/>                                                                 |
| [**GetNumaNodeNumberFromHandle**](/windows/desktop/api/WinBase/nf-winbase-getnumanodenumberfromhandle)<br/>           | Recupera o nó NUMA associado ao dispositivo subjacente para um alça de arquivo.<br/>                                                                          |
| [**GetNumaNodeProcessorMaskEx**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumanodeprocessormaskex)<br/>             | Recupera a máscara do processador para o nó NUMA especificado como um valor USHORT.<br/>                                                                               |
| [**GetNumaProcessorNodeEx**](/windows/desktop/api/WinBase/nf-winbase-getnumaprocessornodeex)<br/>                     | Recupera o número do nó do processador lógico especificado como um valor USHORT.<br/>                                                                           |
| [**GetNumaProximityNodeEx**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumaproximitynodeex)<br/>                     | Recupera o número do nó como um valor USHORT para o identificador de proximidade especificado.<br/>                                                                       |
| [**GetProcessGroupAffinity**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-getprocessgroupaffinity)<br/>                   | Recupera a afinidade do grupo de processadores do processo especificado.<br/>                                                                                          |
| [**GetProcessorSystemCycleTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getprocessorsystemcycletime)<br/>           | Recupera o tempo de ciclo que cada processador no grupo especificado gastou executando DPCs (chamadas de procedimento adiadas) e isrs (rotinas de serviço de interrupção).<br/>     |
| [**GetThreadGroupAffinity**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-getthreadgroupaffinity)<br/>                     | Recupera a afinidade de grupo de processadores do thread especificado.<br/>                                                                                           |
| [**GetThreadIdealProcessorEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadidealprocessorex)<br/>               | Recupera o número do processador do processador ideal para o thread especificado.<br/>                                                                           |
| [**QueryIdleProcessorCycleTimeEx**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryidleprocessorcycletimeex)<br/>       | Recupera o tempo de ciclo acumulado para o thread ocioso em cada processador lógico no grupo de processadores especificado. <br/>                                     |
| [**SetThreadGroupAffinity**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-setthreadgroupaffinity)<br/>                     | Define a afinidade do grupo de processadores para o thread especificado.<br/>                                                                                               |
| [**SetThreadIdealProcessorEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadidealprocessorex)<br/>               | Define o processador ideal para o thread especificado e, opcionalmente, recupera o processador ideal anterior.<br/>                                                  |



 

As novas funções a seguir são usadas com pools de threads.



| Função                                                                              | Descrição                                                                                                    |
|---------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**QueryThreadpoolStackInformation**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-querythreadpoolstackinformation)<br/> | Recupera os tamanhos de reserva de pilha e confirmação para threads no pool de threads especificado.<br/>              |
| [**SetThreadpoolCallbackPersistent**](/windows/desktop/api/WinBase/nf-winbase-setthreadpoolcallbackpersistent)<br/> | Especifica que o retorno de chamada deve ser executado em um thread persistente.<br/>                                      |
| [**SetThreadpoolCallbackPriority**](/windows/desktop/api/WinBase/nf-winbase-setthreadpoolcallbackpriority)<br/>     | Especifica a prioridade de uma função de retorno de chamada em relação a outros itens de trabalho no mesmo pool de threads.<br/> |
| [**SetThreadpoolStackInformation**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolstackinformation)<br/>     | Define os tamanhos de reserva de pilha e confirmação para novos threads no pool de threads especificado. <br/>              |



 

As novas funções a seguir são usadas com UMS.



| Função                                                                          | Descrição                                                                                                   |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [**CreateUmsCompletionList**](/windows/desktop/api/WinBase/nf-winbase-createumscompletionlist)<br/>             | Cria uma lista de conclusão de UMS.<br/>                                                                     |
| [**CreateUmsThreadContext**](/windows/desktop/api/WinBase/nf-winbase-createumsthreadcontext)<br/>               | Cria um contexto de thread UMS para representar um thread de trabalho UMS.<br/>                                     |
| [**DeleteUmsCompletionList**](/windows/desktop/api/WinBase/nf-winbase-deleteumscompletionlist)<br/>             | Exclui a lista de conclusão de UMS especificada. A lista deve estar vazia.<br/>                                 |
| [**DeleteUmsThreadContext**](/windows/desktop/api/WinBase/nf-winbase-deleteumsthreadcontext)<br/>               | Exclui o contexto de thread UMS especificado. O thread deve ser encerrado.<br/>                           |
| [**DequeueUmsCompletionListItems**](/windows/desktop/api/WinBase/nf-winbase-dequeueumscompletionlistitems)<br/> | Recupera threads de trabalho UMS da lista de conclusão de UMS especificada.<br/>                               |
| [**EnterUmsSchedulingMode**](/windows/desktop/api/WinBase/nf-winbase-enterumsschedulingmode)<br/>               | Converte o thread de chamada em um thread do agendador UMS.<br/>                                           |
| [**ExecuteUmsThread**](/windows/desktop/api/WinBase/nf-winbase-executeumsthread)<br/>                           | Executa o thread de trabalho UMS especificado.<br/>                                                              |
| [**GetCurrentUmsThread**](/windows/desktop/api/WinBase/nf-winbase-getcurrentumsthread)<br/>                     | Retorna o contexto de thread UMS do thread UMS de chamada.<br/>                                          |
| [**GetNextUmsListItem**](/windows/desktop/api/WinBase/nf-winbase-getnextumslistitem)<br/>                       | Retorna o próximo contexto de thread UMS em uma lista de contextos de thread UMS.<br/>                              |
| [**GetUmsCompletionListEvent**](/windows/desktop/api/WinBase/nf-winbase-getumscompletionlistevent)<br/>         | Recupera um alça para o evento associado à lista de conclusão de UMS especificada.<br/>                 |
| [**QueryUmsThreadInformation**](/windows/desktop/api/WinBase/nf-winbase-queryumsthreadinformation)<br/>         | Recupera informações sobre o thread de trabalho umS especificado.<br/>                                       |
| [**SetUmsThreadInformation**](/windows/desktop/api/WinBase/nf-winbase-setumsthreadinformation)<br/>             | Define informações de contexto específicas do aplicativo para o thread de trabalho umS especificado.<br/>                 |
| [*UmsSchedulerProc*](/windows/desktop/api/WinNT/nc-winnt-rtl_ums_scheduler_entry_point)<br/>                             | A função de ponto de entrada do agendador UMS definida pelo aplicativo associada a uma lista de conclusão de UMS. <br/> |
| [**UmsThreadYield**](/windows/desktop/api/WinBase/nf-winbase-umsthreadyield)<br/>                               | Gera controle para o thread do agendador UMS no qual o thread de trabalho umS de chamada está em execução.<br/>      |



 

## <a name="new-structures"></a>Novas estruturas



| Estrutura                                                                                                 | Descrição                                                                                         |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**RELAÇÃO DE \_ CACHE**](/windows/desktop/api/WinNT/ns-winnt-cache_relationship)<br/>                                              | Descreve atributos de cache. <br/>                                                             |
| [**afinidade de grupo \_**](/windows/desktop/api/WinNT/ns-winnt-group_affinity)<br/>                                                      | Contém uma afinidade específica de grupo de processador, como a afinidade de um thread.<br/>          |
| [**relação de grupo \_**](/windows/desktop/api/WinNT/ns-winnt-group_relationship)<br/>                                              | Contém informações sobre grupos de processadores. <br/>                                            |
| [**\_relacionamento de nó numa \_**](/windows/desktop/api/WinNT/ns-winnt-numa_node_relationship)<br/>                                     | Contém informações sobre um nó NUMA em um grupo de processador. <br/>                            |
| [**\_informações do grupo de processador \_**](/windows/desktop/api/WinNT/ns-winnt-processor_group_info)<br/>                                         | Contém o número e a afinidade de processadores em um grupo de processadores.<br/>                     |
| [**número do processador \_**](/windows/desktop/api/WinNT/ns-winnt-processor_number)<br/>                                                  | Representa um processador lógico em um grupo de processadores.<br/>                                     |
| [**relação do processador \_**](/windows/desktop/api/WinNT/ns-winnt-processor_relationship)<br/>                                      | Contém informações sobre a afinidade dentro de um grupo de processador.<br/>                            |
| [**\_informações do processador lógico do sistema \_ \_ \_ ex.**](/windows/desktop/api/WinNT/ns-winnt-system_logical_processor_information_ex)<br/> | Contém informações sobre as relações de processadores lógicos e hardwares relacionados.<br/> |
| [**UMS \_ criar \_ atributos de thread \_**](/windows/desktop/api/WinNT/ns-winnt-ums_create_thread_attributes)<br/>                        | Especifica atributos para um thread de trabalho do UMS. <br/>                                           |
| [**\_informações de inicialização do Agendador ums \_ \_**](/windows/desktop/api/WinBase/ns-winbase-ums_scheduler_startup_info)<br/>                            | Especifica atributos para um thread do Agendador do UMS<br/>                                          |



 

 

 
