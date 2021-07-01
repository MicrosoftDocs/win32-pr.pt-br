---
description: Este tópico descreve as funções de processo e thread.
ms.assetid: 8c8e8af0-bf50-4a4b-945c-83bae1eff7dd
title: Funções de thread e processo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ebb1e281feb83b4a0da0c230792399d8e21684f
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120993"
---
# <a name="process-and-thread-functions"></a>Funções de thread e processo

Este tópico descreve as funções de processo e thread.

-   [Função de fila de expedição](#dispatch-queue-function)
-   [Processar funções](#process-functions)
-   [Processar funções de enumeração](#process-enumeration-functions)
-   [Funções de política](#policy-functions)
-   [Funções de thread](#thread-functions)
-   [Funções de atributo estendido de processo e thread](#process-and-thread-extended-attribute-functions)
-   [Funções do WOW64](#wow64-functions)
-   [Funções de objeto de trabalho](#job-object-functions)
-   [Funções do pool de threads](#thread-pool-functions)
-   [Funções de serviço de ordenação de thread](#thread-ordering-service-functions)
-   [Funções de serviço do Agendador de classes de multimídia](#multimedia-class-scheduler-service-functions)
-   [Funções de fibra](#fiber-functions)
-   [Funções de suporte NUMA](#numa-support-functions)
-   [Funções de processador](#processor-functions)
-   [Funções de agendamento de modo de usuário](#user-mode-scheduling-functions)
-   [Funções obsoletas](#obsolete-functions)

## <a name="dispatch-queue-function"></a>Função de fila de expedição

A função a seguir cria um [DispatcherQueueController](/uwp/api/windows.system.dispatcherqueuecontroller).



| Função                                                                   | Descrição                                                                                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateDispatcherQueueController**](/windows/desktop/api/DispatcherQueue/nf-dispatcherqueue-createdispatcherqueuecontroller) | Cria um [DispatcherQueueController](/uwp/api/windows.system.dispatcherqueuecontroller) que gerencia o tempo de vida de um [DispatcherQueue](/uwp/api/windows.system.dispatcherqueue) que executa tarefas em fila em ordem de prioridade em outro thread. |



 

## <a name="process-functions"></a>Processar funções

As funções a seguir são usadas com [processos](child-processes.md).



| Função                                                                 | Descrição                                                                                                                                                                                   |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)                                   | Cria um novo processo e seu thread principal.                                                                                                                                                 |
| [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera)                       | Cria um novo processo e seu thread principal. O novo processo é executado no contexto de segurança do usuário representado pelo token especificado.                                                    |
| [**CreateProcessWithLogonW**](/windows/desktop/api/WinBase/nf-winbase-createprocesswithlogonw)               | Cria um novo processo e seu thread principal. Em seguida, o novo processo executa o arquivo executável especificado no contexto de segurança das credenciais especificadas (usuário, domínio e senha).      |
| [**CreateProcessWithTokenW**](/windows/desktop/api/WinBase/nf-winbase-createprocesswithtokenw)               | Cria um novo processo e seu thread principal. O novo processo é executado no contexto de segurança do token especificado.                                                                            |
| [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess)                                       | Encerra o processo de chamada e todos os seus threads.                                                                                                                                                 |
| [**FlushProcessWriteBuffers**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-flushprocesswritebuffers)             | Libera a fila de gravação de cada processador que está executando um thread do processo atual.                                                                                                    |
| [**FreeEnvironmentStrings**](/windows/win32/api/processenv/nf-processenv-freeenvironmentstringsa)                 | Libera um bloco de cadeias de caracteres de ambiente.                                                                                                                                                         |
| [**GetCommandLine**](/windows/win32/api/processenv/nf-processenv-getcommandlinea)                                 | Recupera a cadeia de caracteres de linha de comando para o processo atual.                                                                                                                                    |
| [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess)                           | Recupera um pseudodispositivo para o processo atual.                                                                                                                                            |
| [**GetCurrentProcessId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessid)                       | Recupera o identificador de processo do processo de chamada.                                                                                                                                      |
| [**GetCurrentProcessorNumber**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessornumber)           | Recupera o número do processador no qual o thread atual estava sendo executado durante a chamada para essa função.                                                                                     |
| [**GetEnvironmentStrings**](/windows/win32/api/processenv/nf-processenv-getenvironmentstrings)                   | Recupera o bloco de ambiente para o processo atual.                                                                                                                                      |
| [**GetEnvironmentVariable**](/windows/desktop/api/WinBase/nf-winbase-getenvironmentvariable)                 | Recupera o valor da variável especificada do bloco de ambiente do processo de chamada.                                                                                              |
| [**GetExitCodeProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getexitcodeprocess)                         | Recupera o status de encerramento do processo especificado.                                                                                                                                    |
| [**GetGuiResources**](/windows/desktop/api/Winuser/nf-winuser-getguiresources)                               | Recupera a contagem de identificadores para objetos GUI (interface gráfica do usuário) em uso pelo processo especificado.                                                                                     |
| [**GetLogicalProcessorInformation**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformation) | Recupera informações sobre processadores lógicos e hardwares relacionados.                                                                                                                          |
| [**GetPriorityClass**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getpriorityclass)                             | Recupera a classe de prioridade para o processo especificado.                                                                                                                                       |
| [**GetProcessAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-getprocessaffinitymask)                 | Recupera uma máscara de afinidade de processo para o processo especificado e a máscara de afinidade do sistema para o sistema.                                                                                      |
| [**GetProcessGroupAffinity**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-getprocessgroupaffinity)               | Recupera a afinidade do grupo de processadores do processo especificado.                                                                                                                              |
| [**GetProcessHandleCount**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocesshandlecount)                   | Recupera o número de identificadores abertos que pertencem ao processo especificado.                                                                                                                    |
| [**GetProcessId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessid)                                     | Recupera o identificador do processo especificado.                                                                                                                                    |
| [**GetProcessIdOfThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessidofthread)                     | Recupera o identificador do processo associado ao thread especificado.                                                                                                         |
| [**GetProcessIoCounters**](/windows/desktop/api/WinBase/nf-winbase-getprocessiocounters)                     | Recupera informações de contabilização de todas as operações de e/s executadas pelo processo especificado.                                                                                                   |
| [**GetProcessMitigationPolicy**](/windows/desktop/api/Processthreadsapi/nf-processthreadsapi-getprocessmitigationpolicy)         | Recupera as configurações de política de mitigação para o processo de chamada.                                                                                                                                 |
| [**GetProcessPriorityBoost**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocesspriorityboost)               | Recupera o estado de controle de aumento de prioridade do processo especificado.                                                                                                                          |
| [**GetProcessShutdownParameters**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessshutdownparameters)     | Recupera os parâmetros de desligamento para o processo de chamada no momento.                                                                                                                              |
| [**GetProcessTimes**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocesstimes)                               | Recupera informações de tempo sobre o processo especificado.                                                                                                                                 |
| [**GetProcessVersion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessversion)                           | Recupera os números de versão principal e secundária do sistema no qual o processo especificado espera ser executado.                                                                                    |
| [**GetProcessWorkingSetSize**](/windows/desktop/api/memoryapi/nf-memoryapi-getprocessworkingsetsize)             | Recupera os tamanhos mínimo e máximo do conjunto de trabalho do processo especificado.                                                                                                                 |
| [**GetProcessWorkingSetSizeEx**](/windows/win32/api/memoryapi/nf-memoryapi-getprocessworkingsetsizeex)         | Recupera os tamanhos mínimo e máximo do conjunto de trabalho do processo especificado.                                                                                                                 |
| [**GetProcessorSystemCycleTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getprocessorsystemcycletime)       | Recupera o tempo de ciclo de cada processador no grupo especificado gasto na execução de DPCs (chamadas de procedimento deferidas) e ISRs (rotinas de serviço de interrupção).                                         |
| [**GetStartupInfo**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getstartupinfow)                                 | Recupera o conteúdo da estrutura [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) que foi especificada quando o processo de chamada foi criado.                                                       |
| [**IsImmersiveProcess**](/windows/desktop/api/Winuser/nf-winuser-isimmersiveprocess)                         | Determina se o processo pertence a um aplicativo da Windows Store.                                                                                                                                |
| [**NeedCurrentDirectoryForExePath**](/windows/win32/api/processenv/nf-processenv-needcurrentdirectoryforexepatha) | Determina se o diretório atual deve ser incluído no caminho de pesquisa para o executável especificado.                                                                                  |
| [**Openprocess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocess)                                       | Abre um objeto de processo local existente.                                                                                                                                                       |
| [**QueryFullProcessImageName**](/windows/desktop/api/WinBase/nf-winbase-queryfullprocessimagenamea)           | Recupera o nome completo da imagem executável para o processo especificado.                                                                                                                    |
| [**QueryProcessAffinityUpdateMode**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-queryprocessaffinityupdatemode) | Recupera o modo de atualização de afinidade do processo especificado.                                                                                                                                  |
| [**QueryProcessCycleTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryprocesscycletime)                   | Recupera a soma do tempo de ciclo de todos os threads do processo especificado.                                                                                                                  |
| [**Setenvironmentvariable**](/windows/desktop/api/WinBase/nf-winbase-setenvironmentvariable)                 | Define o valor de uma variável de ambiente para o processo atual.                                                                                                                            |
| [**SetPriorityClass**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setpriorityclass)                             | Define a classe de prioridade para o processo especificado.                                                                                                                                            |
| [**SetProcessAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-setprocessaffinitymask)                 | Define uma máscara de afinidade de processador para os threads de um processo especificado.                                                                                                                        |
| [**SetProcessAffinityUpdateMode**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocessaffinityupdatemode)     | Define o modo de atualização de afinidade do processo especificado.                                                                                                                                       |
| [**SetProcessInformation**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocessinformation)                   | Define informações para o processo especificado.                                                                                                                                                   |
| [**SetProcessMitigationPolicy**](/windows/desktop/api/Processthreadsapi/nf-processthreadsapi-setprocessmitigationpolicy)         | Define a política de mitigação para o processo de chamada.                                                                                                                                           |
| [**SetProcessPriorityBoost**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocesspriorityboost)               | Desabilita a capacidade do sistema de aumentar temporariamente a prioridade dos threads do processo especificado.                                                                                 |
| [**SetProcessRestrictionExemption**](/windows/desktop/api/Winuser/nf-winuser-setprocessrestrictionexemption) | Isenta o processo de chamada de restrições, impedindo que os processos da área de trabalho interajam com o ambiente de aplicativos da Windows Store. Essa função é usada por ferramentas de desenvolvimento e depuração. |
| [**SetProcessShutdownParameters**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocessshutdownparameters)     | Define parâmetros de desligamento para o processo de chamada no momento.                                                                                                                                   |
| [**SetProcessWorkingSetSize**](/windows/desktop/api/memoryapi/nf-memoryapi-setprocessworkingsetsize)             | Define os tamanhos mínimo e máximo do conjunto de trabalho para o processo especificado.                                                                                                                     |
| [**SetProcessWorkingSetSizeEx**](/windows/win32/api/memoryapi/nf-memoryapi-setprocessworkingsetsizeex)         | Define os tamanhos mínimo e máximo do conjunto de trabalho para o processo especificado.                                                                                                                     |
| [**TerminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess)                             | Encerra o processo especificado e todos os seus threads.                                                                                                                                      |



 

## <a name="process-enumeration-functions"></a>Funções de enumeração de processo

As funções a seguir são usadas para enumerar processos.



| Função                                                    | Descrição                                                                        |
|-------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**EnumProcesses**](/windows/win32/api/psapi/nf-psapi-enumprocesses)                     | Recupera o identificador de processo para cada objeto de processo no sistema.            |
| [**Process32First**](/windows/win32/api/tlhelp32/nf-tlhelp32-process32first)                   | Recupera informações sobre o primeiro processo encontrado em um instantâneo do sistema.    |
| [**Process32Next**](/windows/win32/api/tlhelp32/nf-tlhelp32-process32next)                     | Recupera informações sobre o próximo processo registrado em um instantâneo do sistema.        |
| [**WTSEnumerateProcesses**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsenumerateprocessesa) | Recupera informações sobre os processos ativos no servidor terminal especificado. |



 

## <a name="policy-functions"></a>Funções de política

As funções a seguir são usadas com a política de todo o processo.



|  Função                                                    |  Descrição                                                     |
|------------------------------------------------------|-------------------------------------------------------|
| [**QueryProtectedPolicy**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-queryprotectedpolicy) | Consulta o valor associado a uma política protegida. |
| [**SetProtectedPolicy**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprotectedpolicy)     | Define uma política protegida.                              |



 

## <a name="thread-functions"></a>Funções de thread

As funções a seguir são usadas com [threads](multiple-threads.md).



| Função                                                           | Descrição                                                                                                                                               |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AttachThreadInput**](/windows/desktop/api/Winuser/nf-winuser-attachthreadinput)                     | Anexa o mecanismo de processamento de entrada de um thread ao de outro thread.                                                                          |
| [**CreateRemoteThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread)                   | Cria um thread que é executado no espaço de endereço virtual de outro processo.                                                                               |
| [**CreateRemoteThreadEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethreadex)               | Cria um thread que é executado no espaço de endereço virtual de outro processo e, opcionalmente, especifica atributos estendidos, como afinidade de grupo de processadores. |
| [**Createthread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread)                               | Cria um thread a ser executado dentro do espaço de endereço virtual do processo de chamada.                                                                      |
| [**Exitthread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread)                                   | Encerra o thread de chamada.                                                                                                                                  |
| [**GetCurrentThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthread)                       | Recupera um pseudocódigo para o thread atual.                                                                                                         |
| [**Getcurrentthreadid**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthreadid)                   | Recupera o identificador de thread do thread de chamada.                                                                                                    |
| [**Getexitcodethread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getexitcodethread)                     | Recupera o status de encerramento do thread especificado.                                                                                                 |
| [**GetThreadDescription**](/windows/desktop/api/ProcessThreadsApi/nf-processthreadsapi-getthreaddescription)               | Recupera a descrição atribuída a um thread chamando [**SetThreadDescription**](/windows/desktop/api/ProcessThreadsApi/nf-processthreadsapi-setthreaddescription).                                  |
| [**GetThreadGroupAffinity**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-getthreadgroupaffinity)           | Recupera a afinidade de grupo de processadores do thread especificado.                                                                                           |
| [**GetThreadId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadid)                                 | Recupera o identificador de thread do thread especificado.                                                                                                  |
| [**GetThreadIdealProcessorEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadidealprocessorex)     | Recupera o número do processador do processador ideal para o thread especificado.                                                                           |
| [**GetThreadInformation**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadinformation)               | Recupera informações sobre o thread especificado.                                                                                                         |
| [**GetThreadIOPendingFlag**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadiopendingflag)           | Determina se um thread especificado tem solicitações de E/S pendentes.                                                                                       |
| [**Getthreadpriority**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadpriority)                     | Recupera o valor de prioridade para o thread especificado.                                                                                                    |
| [**GetThreadPriorityBoost**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadpriorityboost)           | Recupera o estado de controle de aumento de prioridade do thread especificado.                                                                                       |
| [**GetThreadTimes**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadtimes)                           | Recupera informações de tempo para o thread especificado.                                                                                                    |
| [**OpenThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread)                                   | Abre um objeto de thread existente.                                                                                                                          |
| [**QueryIdleProcessorCycleTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryidleprocessorcycletime) | Recupera o tempo de ciclo para o thread ocioso de cada processador no sistema.                                                                             |
| [**QueryThreadCycleTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-querythreadcycletime)               | Recupera o tempo de ciclo para o thread especificado.                                                                                                        |
| [**Resumethread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread)                               | Diminui a contagem de suspensão de um thread.                                                                                                                      |
| [**SetThreadAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-setthreadaffinitymask)             | Define uma máscara de afinidade de processador para o thread especificado.                                                                                                  |
| [**SetThreadDescription**](/windows/desktop/api/ProcessThreadsApi/nf-processthreadsapi-setthreaddescription)               | Atribui uma descrição a um thread.                                                                                                                        |
| [**SetThreadGroupAffinity**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-setthreadgroupaffinity)           | Define a afinidade de grupo de processador para o thread especificado.                                                                                               |
| [**SetThreadIdealProcessor**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadidealprocessor)         | Especifica um processador preferencial para um thread.                                                                                                             |
| [**SetThreadIdealProcessorEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadidealprocessorex)     | Define o processador ideal para o thread especificado e, opcionalmente, recupera o processador ideal anterior.                                                  |
| [**SetThreadInformation**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadinformation)               | Define informações para o thread especificado.                                                                                                                |
| [**SetThreadPriority**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadpriority)                     | Define o valor de prioridade para o thread especificado.                                                                                                         |
| [**SetThreadPriorityBoost**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadpriorityboost)           | Desabilita a capacidade do sistema de aumentar temporariamente a prioridade de um thread.                                                                         |
| [**SetThreadStackGuarantee**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadstackguarantee)         | Define a garantia da pilha para o thread de chamada.                                                                                                          |
| [**Modo de suspensão**](/windows/win32/api/synchapi/nf-synchapi-sleep)                                             | Suspende a execução do thread atual para um intervalo especificado.                                                                                    |
| [**SleepEx**](/windows/win32/api/synchapi/nf-synchapi-sleepex)                                         | Suspende o thread atual até que a condição especificada seja atendida.                                                                                         |
| [**SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread)                             | Suspende o thread especificado.                                                                                                                            |
| [**SwitchToThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-switchtothread)                           | Faz com que o thread de chamada conceda a execução para outro thread que está pronto para ser executado no processador atual.                                             |
| [**TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread)                         | Encerra um thread.                                                                                                                                      |
| [**ThreadProc**](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85))                                   | Uma função definida pelo aplicativo que serve como o endereço inicial para um thread.                                                                         |
| [**TlsAlloc**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlsalloc)                                       | Aloca um índice de TLS (armazenamento local de thread).                                                                                                             |
| [**TlsFree**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlsfree)                                         | Libera um índice TLS.                                                                                                                                     |
| [**TlsGetValue**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlsgetvalue)                                 | Recupera o valor no slot TLS do thread de chamada para um índice TLS especificado.                                                                           |
| [**TlsSetValue**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlssetvalue)                                 | Armazena um valor no slot TLS do thread de chamada para um índice TLS especificado.                                                                                |
| [**WaitForInputIdle**](/windows/desktop/api/Winuser/nf-winuser-waitforinputidle)                       | Aguarda até que o processo especificado esteja aguardando a entrada do usuário sem nenhuma entrada pendente ou até que o intervalo de tempo limite tenha decorrido.                            |



 

## <a name="process-and-thread-extended-attribute-functions"></a>Funções de atributo estendido de processo e thread

As funções a seguir são usadas para definir atributos estendidos para criação de thread e processo.



| Função                                                                       | Descrição                                                                                          |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**DeleteProcThreadAttributeList**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-deleteprocthreadattributelist)         | Exclui a lista de atributos especificada para criação de threads e processos.                            |
| [**InitializeProcThreadAttributeList**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-initializeprocthreadattributelist) | Inicializa a lista de atributos especificada para criação de thread e processo.                        |
| [**UpdateProcThreadAttribute**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-updateprocthreadattribute)                 | Atualiza o atributo especificado na lista especificada de atributos para criação de thread e processo. |



 

## <a name="wow64-functions"></a>Funções do WOW64

As funções a seguir são usadas com o [WOW64](../winprog64/running-32-bit-applications.md).



| Função                                         | Descrição                                                                                                                            |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**IsWow64Message**](/windows/desktop/api/Winuser/nf-winuser-iswow64message)         | Determina se a última mensagem lida da fila do thread atual foi originada de um processo WOW64.                              |
| [**IsWow64Process**](/windows/win32/api/wow64apiset/nf-wow64apiset-iswow64process)         | Determina se o processo especificado está sendo executado sob WOW64.                                                                       |
| [**IsWow64Process2**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process2)       | Determina se o processo especificado está sendo executado sob WOW64; também retorna informações adicionais de processo e arquitetura do computador. |
| [**Wow64SuspendThread**](/windows/desktop/api/WinBase/nf-winbase-wow64suspendthread) | Suspende o thread WOW64 especificado.                                                                                                   |



 

## <a name="job-object-functions"></a>Funções de objeto de trabalho

As funções a seguir são usadas com [objetos de trabalho](job-objects.md).



| Função                                                       | Descrição                                                                                          |
|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**AssignProcessToJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-assignprocesstojobobject)   | Associa um processo a um objeto de trabalho existente.                                                    |
| [**CreateJobObject**](/windows/desktop/api/WinBase/nf-winbase-createjobobjecta)                     | Cria ou abre um objeto de trabalho.                                                                       |
| [**IsProcessInJob**](/windows/win32/api/jobapi/nf-jobapi-isprocessinjob)                       | Determina se o processo está em execução no trabalho especificado.                                      |
| [**OpenJobObject**](/windows/desktop/api/WinBase/nf-winbase-openjobobjecta)                         | Abre um objeto de trabalho existente.                                                                        |
| [**QueryInformationJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-queryinformationjobobject) | Recupera informações de limite e estado do trabalho do objeto de trabalho.                                       |
| [**SetInformationJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-setinformationjobobject)     | Defina os limites para um objeto de trabalho.                                                                         |
| [**TerminateJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-terminatejobobject)               | Encerra todos os processos associados ao trabalho no momento.                                          |
| [**UserHandleGrantAccess**](/windows/desktop/api/Winuser/nf-winuser-userhandlegrantaccess)         | Concede ou nega o acesso a um identificador para um objeto de usuário a um trabalho que tenha uma restrição de interface de usuário. |



 

## <a name="thread-pool-functions"></a>Funções do pool de threads

As funções a seguir são usadas com [pools de threads](thread-pools.md).



| Função                                                                                   | Descrição                                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CallbackMayRunLong**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-callbackmayrunlong)                                           | Indica que o retorno de chamada pode não retornar rapidamente.                                                                                                                                                                                                 |
| [**CancelThreadpoolIo**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-cancelthreadpoolio)                                           | Cancela a notificação da função [**StartThreadpoolIo**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-startthreadpoolio) .                                                                                                                                                          |
| [**CloseThreadpool**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-closethreadpool)                                                 | Fecha o pool de threads especificado.                                                                                                                                                                                                                   |
| [**CloseThreadpoolCleanupGroup**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-closethreadpoolcleanupgroup)                         | Fecha o grupo de limpeza especificado.                                                                                                                                                                                                                 |
| [**CloseThreadpoolCleanupGroupMembers**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-closethreadpoolcleanupgroupmembers)           | Libera os membros do grupo de limpeza especificado, aguarda a conclusão de todas as funções de retorno de chamada e, opcionalmente, cancela todas as funções de retorno de chamada pendentes.                                                                                       |
| [**CloseThreadpoolIo**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-closethreadpoolio)                                             | Libera o objeto de conclusão de e/s especificado.                                                                                                                                                                                                       |
| [**CloseThreadpoolTimer**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-closethreadpooltimer)                                       | Libera o objeto de timer especificado.                                                                                                                                                                                                                |
| [**CloseThreadpoolWait**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-closethreadpoolwait)                                         | Libera o objeto de espera especificado.                                                                                                                                                                                                                 |
| [**CloseThreadpoolWork**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-closethreadpoolwork)                                         | Libera o objeto de trabalho especificado.                                                                                                                                                                                                                 |
| [**CreateThreadpool**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-createthreadpool)                                               | Aloca um novo pool de threads para executar retornos de chamada.                                                                                                                                                                                               |
| [**CreateThreadpoolCleanupGroup**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolcleanupgroup)                       | Cria um grupo de limpeza que os aplicativos podem usar para rastrear um ou mais retornos de chamada de pool de threads.                                                                                                                                                       |
| [**CreateThreadpoolIo**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolio)                                           | Cria um novo objeto de conclusão de e/s.                                                                                                                                                                                                                |
| [**CreateThreadpoolTimer**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-createthreadpooltimer)                                     | Cria um novo objeto de temporizador.                                                                                                                                                                                                                         |
| [**CreateThreadpoolWait**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolwait)                                       | Cria um novo objeto de espera.                                                                                                                                                                                                                          |
| [**CreateThreadpoolWork**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolwork)                                       | Cria um novo objeto de trabalho.                                                                                                                                                                                                                          |
| [**DestroyThreadpoolEnvironment**](/windows/desktop/api/WinBase/nf-winbase-destroythreadpoolenvironment)                       | Exclui o ambiente de retorno de chamada especificado. Chame essa função quando o ambiente de chamada de retorno não for mais necessário para criar novos objetos do pool de threads.                                                                                              |
| [**DisassociateCurrentThreadFromCallback**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-disassociatecurrentthreadfromcallback)     | Remove a associação entre a função de retorno de chamada em execução no momento e o objeto que iniciou o retorno de chamada. O thread atual não será mais contabilizado como executar um retorno de chamada em nome do objeto.                                      |
| [**FreeLibraryWhenCallbackReturns**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-freelibrarywhencallbackreturns)                   | Especifica a DLL que o pool de threads descarregará quando o retorno de chamada atual for concluído.                                                                                                                                                             |
| [**InitializeThreadpoolEnvironment**](/windows/desktop/api/WinBase/nf-winbase-initializethreadpoolenvironment)                 | Inicializa um ambiente de chamada de retorno.                                                                                                                                                                                                                 |
| [**IsThreadpoolTimerSet**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-isthreadpooltimerset)                                       | Determina se o objeto de timer especificado está definido no momento.                                                                                                                                                                                     |
| [**LeaveCriticalSectionWhenCallbackReturns**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-leavecriticalsectionwhencallbackreturns) | Especifica a seção crítica que o pool de threads liberará quando o retorno de chamada atual for concluído.                                                                                                                                               |
| [**QueryThreadpoolStackInformation**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-querythreadpoolstackinformation)                 | Recupera a reserva de pilha e os tamanhos de confirmação para threads no pool de threads especificado.                                                                                                                                                              |
| [**ReleaseMutexWhenCallbackReturns**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-releasemutexwhencallbackreturns)                 | Especifica o mutex que o pool de threads liberará quando o retorno de chamada atual for concluído.                                                                                                                                                          |
| [**ReleaseSemaphoreWhenCallbackReturns**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-releasesemaphorewhencallbackreturns)         | Especifica o semáforo que o pool de threads liberará quando o retorno de chamada atual for concluído.                                                                                                                                                      |
| [**SetEventWhenCallbackReturns**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-seteventwhencallbackreturns)                         | Especifica o evento que o pool de threads definirá quando o retorno de chamada atual for concluído.                                                                                                                                                              |
| [**SetThreadpoolCallbackCleanupGroup**](/windows/desktop/api/WinBase/nf-winbase-setthreadpoolcallbackcleanupgroup)             | Associa o grupo de limpeza especificado ao ambiente de retorno de chamada especificado.                                                                                                                                                                     |
| [**SetThreadpoolCallbackLibrary**](/windows/desktop/api/WinBase/nf-winbase-setthreadpoolcallbacklibrary)                       | Garante que a DLL especificada permaneça carregada, desde que haja retornos de chamada pendentes.                                                                                                                                                           |
| [**SetThreadpoolCallbackPersistent**](/windows/desktop/api/WinBase/nf-winbase-setthreadpoolcallbackpersistent)                 | Especifica que o retorno de chamada deve ser executado em um thread persistente.                                                                                                                                                                                      |
| [**SetThreadpoolCallbackPool**](/windows/desktop/api/WinBase/nf-winbase-setthreadpoolcallbackpool)                             | Define o pool de threads a ser usado ao gerar retornos de chamada.                                                                                                                                                                                          |
| [**SetThreadpoolCallbackPriority**](/windows/desktop/api/WinBase/nf-winbase-setthreadpoolcallbackpriority)                     | Especifica a prioridade de uma função de retorno de chamada relativa a outros itens de trabalho no mesmo pool de threads.                                                                                                                                                 |
| [**SetThreadpoolCallbackRunsLong**](/windows/desktop/api/WinBase/nf-winbase-setthreadpoolcallbackrunslong)                     | Indica que os retornos de chamada associados a esse ambiente de retorno de chamada podem não retornar rapidamente.                                                                                                                                                          |
| [**SetThreadpoolStackInformation**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolstackinformation)                     | Define a reserva de pilha e os tamanhos de confirmação para novos threads no pool de threads especificado.                                                                                                                                                               |
| [**SetThreadpoolThreadMaximum**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolthreadmaximum)                           | Define o número máximo de threads que o pool de threads especificado pode alocar para processar retornos de chamada.                                                                                                                                                |
| [**SetThreadpoolThreadMinimum**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolthreadminimum)                           | Define o número mínimo de threads que o pool de threads especificado deve disponibilizar para processar retornos de chamada.                                                                                                                                         |
| [**SetThreadpoolTimerEx**](/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-setthreadpooltimerex)                                       | Define o objeto de timer. Um thread de trabalho chama o retorno de chamada do objeto de timer depois que o tempo limite especificado expira.                                                                                                                                       |
| [**SetThreadpoolTimer**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-setthreadpooltimer)                                           | Define o objeto de timer. Um thread de trabalho chama o retorno de chamada do objeto de timer depois que o tempo limite especificado expira.                                                                                                                                       |
| [**SetThreadpoolWait**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolwait)                                             | Define o objeto de espera. Um thread de trabalho chama a função de retorno de chamada do objeto de espera depois que o identificador é sinalizado ou após o tempo limite especificado expirar.                                                                                           |
| [**SetThreadpoolWaitEx**](/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolwaitex)                                         | Define o objeto de espera. Um thread de trabalho chama a função de retorno de chamada do objeto de espera depois que o identificador é sinalizado ou após o tempo limite especificado expirar.                                                                                           |
| [**StartThreadpoolIo**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-startthreadpoolio)                                             | Notifica o pool de threads que as operações de e/s podem possivelmente começar para o objeto de conclusão de e/s especificado. Um thread de trabalho chama a função de retorno de chamada do objeto de conclusão de e/s depois que a operação é concluída no identificador de arquivo associado a esse objeto. |
| [**SubmitThreadpoolWork**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-submitthreadpoolwork)                                       | Posta um objeto de trabalho no pool de threads. Um thread de trabalho chama a função de retorno de chamada do objeto de trabalho.                                                                                                                                                  |
| [**TpInitializeCallbackEnviron**](/windows/desktop/api/winnt/nf-winnt-tpinitializecallbackenviron)                         | Inicializa um ambiente de chamada de retorno para o pool de threads.                                                                                                                                                                                             |
| [**TpDestroyCallbackEnviron**](/windows/desktop/api/winnt/nf-winnt-tpdestroycallbackenviron)                               | Exclui o ambiente de retorno de chamada especificado. Chame essa função quando o ambiente de chamada de retorno não for mais necessário para criar novos objetos do pool de threads.                                                                                              |
| [**TpSetCallbackActivationContext**](/windows/desktop/api/winnt/nf-winnt-tpsetcallbackactivationcontext)                   | Atribui um contexto de ativação ao ambiente de chamada de retorno.                                                                                                                                                                                          |
| [**TpSetCallbackCleanupGroup**](/windows/desktop/api/winnt/nf-winnt-tpsetcallbackcleanupgroup)                             | Associa o grupo de limpeza especificado ao ambiente de retorno de chamada especificado.                                                                                                                                                                     |
| [**TpSetCallbackFinalizationCallback**](/windows/desktop/api/winnt/nf-winnt-tpsetcallbackfinalizationcallback)             | Indica uma função a ser chamada quando o ambiente de chamada de retorno é finalizado.                                                                                                                                                                            |
| [**TpSetCallbackLongFunction**](/windows/desktop/api/winnt/nf-winnt-tpsetcallbacklongfunction)                             | Indica que os retornos de chamada associados a esse ambiente de retorno de chamada podem não retornar rapidamente.                                                                                                                                                          |
| [**TpSetCallbackNoActivationContext**](/windows/desktop/api/winnt/nf-winnt-tpsetcallbacknoactivationcontext)               | Indica que o ambiente de chamada de retorno não tem nenhum contexto de ativação.                                                                                                                                                                                  |
| [**TpSetCallbackPersistent**](/windows/desktop/api/winnt/nf-winnt-tpsetcallbackpersistent)                                 | Especifica que o retorno de chamada deve ser executado em um thread persistente.                                                                                                                                                                                      |
| [**TpSetCallbackPriority**](/windows/desktop/api/winnt/nf-winnt-tpsetcallbackpriority)                                     | Especifica a prioridade de uma função de retorno de chamada relativa a outros itens de trabalho no mesmo pool de threads.                                                                                                                                                 |
| [**TpSetCallbackRaceWithDll**](/windows/desktop/api/winnt/nf-winnt-tpsetcallbackracewithdll)                               | Garante que a DLL especificada permaneça carregada, desde que haja retornos de chamada pendentes.                                                                                                                                                           |
| [**TpSetCallbackThreadpool**](/windows/desktop/api/winnt/nf-winnt-tpsetcallbackthreadpool)                                 | Atribui um pool de threads a um ambiente de chamada de retorno.                                                                                                                                                                                                    |
| [**TrySubmitThreadpoolCallback**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-trysubmitthreadpoolcallback)                         | Solicita que um thread de trabalho do pool de threads chame a função de retorno de chamada especificada.                                                                                                                                                                     |
| [**WaitForThreadpoolIoCallbacks**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-waitforthreadpooliocallbacks)                       | Aguarda a conclusão de retornos de chamada de conclusão de E/S pendentes e, opcionalmente, cancela retornos de chamada pendentes que ainda não começaram a ser executados.                                                                                                           |
| [**WaitForThreadpoolTimerCallbacks**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-waitforthreadpooltimercallbacks)                 | Aguarda a conclusão de retornos de chamada de temporizador pendentes e, opcionalmente, cancela retornos de chamada pendentes que ainda não começaram a ser executados.                                                                                                                    |
| [**WaitForThreadpoolWaitCallbacks**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-waitforthreadpoolwaitcallbacks)                   | Aguarda a conclusão dos retornos de chamada de espera pendentes e, opcionalmente, cancela os retornos de chamada pendentes que ainda não iniciaram a execução.                                                                                                                     |
| [**WaitForThreadpoolWorkCallbacks**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-waitforthreadpoolworkcallbacks)                   | Aguarda a conclusão de retornos de chamada de trabalho pendentes e, opcionalmente, cancela retornos de chamada pendentes que ainda não começaram a ser executados.                                                                                                                     |



 

As funções a seguir fazem parte da API original [de pooling de](thread-pooling.md) threads.



| Função                                                            | Descrição                                                                                                                                                                                                            |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BindIoCompletionCallback**](/windows/desktop/api/WinBase/nf-winbase-bindiocompletioncallback)        | Associa a porta de conclusão de E/S pertencente ao pool de threads ao alça de arquivo especificado. Após a conclusão de uma solicitação de E/S envolvendo esse arquivo, um thread de trabalho que não é de E/S executará a função de retorno de chamada especificada. |
| [**Queueuserworkitem**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-queueuserworkitem)                      | Enfileiro um item de trabalho em um thread de trabalho no pool de threads.                                                                                                                                                              |
| [**Registerwaitforsingleobject**](/windows/win32/api/winbase/nf-winbase-registerwaitforsingleobject) | Direciona um thread de espera no pool de threads para aguardar no objeto .                                                                                                                                                        |
| [**UnregisterWaitEx**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-unregisterwaitex)                       | Aguarda até que um ou todos os objetos especificados estão no estado sinalizado ou o intervalo de tempo-tempo de saída.                                                                                                            |



 

## <a name="thread-ordering-service-functions"></a>Funções de serviço de ordenação de thread

As funções a seguir são usadas com o [serviço de ordenação de threads](thread-ordering-service.md).



| Função                                                                   | Descrição                                                                                 |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [**Capacidade de resposta do AvQuerySystem**](/windows/desktop/api/Avrt/nf-avrt-avquerysystemresponsiveness)         | Recupera a configuração de capacidade de resposta do sistema usada pelo serviço de agendador de classes multimídia. |
| [**AvRtCreateThreadOrderingGroup**](/windows/desktop/api/Avrt/nf-avrt-avrtcreatethreadorderinggroup)     | Cria um grupo de ordenação de threads.                                                            |
| [**AvRtCreateThreadOrderingGroupEx**](/windows/desktop/api/Avrt/nf-avrt-avrtcreatethreadorderinggroupexa) | Cria um grupo de ordenação de threads e associa o thread do servidor a uma tarefa.               |
| [**AvRtDeleteThreadOrderingGroup**](/windows/desktop/api/Avrt/nf-avrt-avrtdeletethreadorderinggroup)     | Exclui o grupo de ordenação de threads especificado criado pelo chamador.                          |
| [**AvRtJoinThreadOrderingGroup**](/windows/desktop/api/Avrt/nf-avrt-avrtjointhreadorderinggroup)         | Une threads de cliente a um grupo de ordenação de threads.                                            |
| [**AvRtLeaveThreadOrderingGroup**](/windows/desktop/api/Avrt/nf-avrt-avrtleavethreadorderinggroup)       | Permite que os threads de cliente saiam de um grupo de ordenação de threads.                                    |
| [**AvRtWaitOnThreadOrderingGroup**](/windows/desktop/api/Avrt/nf-avrt-avrtwaitonthreadorderinggroup)     | Permite que os threads de cliente de um grupo de ordenação de threads aguardem até que eles deverão ser executados.        |



 

## <a name="multimedia-class-scheduler-service-functions"></a>Funções de serviço do Agendador de Classes Multimídia

As funções a seguir são usadas com o serviço [de agendador de classes multimídia](multimedia-class-scheduler-service.md).



| Função                                                                   | Descrição                                                                                           |
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**AvRevertMmThreadCharacteristics**](/windows/desktop/api/Avrt/nf-avrt-avrevertmmthreadcharacteristics) | Indica que um thread não está mais executando o trabalho associado à tarefa especificada.              |
| [**AvSetMmMaxThreadCharacteristics**](/windows/desktop/api/Avrt/nf-avrt-avsetmmmaxthreadcharacteristicsa) | Associa o thread de chamada às tarefas especificadas.                                               |
| [**AvSetMmThreadCharacteristics**](/windows/desktop/api/Avrt/nf-avrt-avsetmmthreadcharacteristicsa)       | Associa o thread de chamada à tarefa especificada.                                                |
| [**AvSetMmThreadPriority**](/windows/desktop/api/Avrt/nf-avrt-avsetmmthreadpriority)                     | Ajusta a prioridade de thread do thread de chamada em relação a outros threads que executam a mesma tarefa. |



 

## <a name="fiber-functions"></a>Funções fiber

As funções a seguir são [usadas com fibra](fibers.md).



| Função                                                 | Descrição                                                                                                  |
|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**ConvertFiberToThread**](/windows/desktop/api/WinBase/nf-winbase-convertfibertothread)     | Converte a fibra atual em um thread.                                                                    |
| [**ConvertThreadToFiber**](/windows/desktop/api/WinBase/nf-winbase-convertthreadtofiber)     | Converte o thread atual em uma fibra.                                                                    |
| [**ConvertThreadToFiberEx**](/windows/desktop/api/WinBase/nf-winbase-convertthreadtofiberex) | Converte o thread atual em uma fibra.                                                                    |
| [**Createfiber**](/windows/desktop/api/WinBase/nf-winbase-createfiber)                       | Aloca um objeto fibra, atribui a ele uma pilha e configura a execução para começar no endereço inicial especificado. |
| [**CreateFiberEx**](/windows/desktop/api/WinBase/nf-winbase-createfiberex)                   | Aloca um objeto fibra, atribui a ele uma pilha e configura a execução para começar no endereço inicial especificado. |
| [**DeleteFiber**](/windows/desktop/api/WinBase/nf-winbase-deletefiber)                       | Exclui uma fibra existente.                                                                                   |
| [**FiberProc**](/windows/win32/api/winbase/nc-winbase-pfiber_start_routine)                           | Uma função definida pelo aplicativo usada com a [**função CreateFiber.**](/windows/desktop/api/WinBase/nf-winbase-createfiber)                   |
| [**FlsAlloc**](/windows/win32/api/fibersapi/nf-fibersapi-flsalloc)                             | Aloca um índice FLS (armazenamento local de fibra).                                                                 |
| [**FlsFree**](/windows/win32/api/fibersapi/nf-fibersapi-flsfree)                               | Libera um índice FLS.                                                                                       |
| [**FlsGetValue**](/windows/win32/api/fibersapi/nf-fibersapi-flsgetvalue)                       | Recupera o valor no slot FLS da fibra de chamada para um índice FLS especificado.                               |
| [**FlsSetValue**](/windows/win32/api/fibersapi/nf-fibersapi-flssetvalue)                       | Armazena um valor no slot FLS da fibra de chamada para um índice FLS especificado.                                    |
| [**IsThreadAFiber**](/windows/win32/api/fibersapi/nf-fibersapi-isthreadafiber)                 | Determina se o thread atual é uma fibra.                                                            |
| [**SwitchToFiber**](/windows/desktop/api/WinBase/nf-winbase-switchtofiber)                   | Agenda uma fibra.                                                                                           |



 

## <a name="numa-support-functions"></a>Funções de suporte NUMA

As funções a seguir fornecem suporte [a NUMA.](numa-support.md)



| Função                                                                 | Descrição                                                                                                                                            |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AllocateUserPhysicalPagesNuma**](/windows/win32/api/memoryapi/nf-memoryapi-allocateuserphysicalpagesnuma)  | Reserva ou confirma uma região de memória dentro do espaço de endereço virtual do processo especificado e especifica o nó NUMA para a memória física. |
| [**GetLogicalProcessorInformation**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformation) | Recupera informações sobre processadores lógicos e hardware relacionado.                                                                                   |
| [**GetNumaAvailableMemoryNode**](/windows/desktop/api/WinBase/nf-winbase-getnumaavailablememorynode)         | Recupera a quantidade de memória disponível no nó especificado.                                                                                        |
| [**GetNumaAvailableMemoryNodeEx**](/windows/desktop/api/WinBase/nf-winbase-getnumaavailablememorynodeex)     | Recupera a quantidade de memória disponível no nó especificado como um valor USHORT.                                                              |
| [**GetNumaHighestNodeNumber**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumahighestnodenumber)             | Recupera o nó que atualmente tem o número mais alto.                                                                                              |
| [**GetNumaNodeNumberFromHandle**](/windows/desktop/api/WinBase/nf-winbase-getnumanodenumberfromhandle)       | Recupera o nó NUMA associado ao dispositivo subjacente para um alça de arquivo.                                                                       |
| [**GetNumaNodeProcessorMask**](/windows/desktop/api/WinBase/nf-winbase-getnumanodeprocessormask)             | Recupera a máscara do processador para o nó especificado.                                                                                                   |
| [**GetNumaNodeProcessorMaskEx**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumanodeprocessormaskex)         | Recupera a máscara do processador para o nó NUMA especificado como um valor USHORT.                                                                            |
| [**GetNumaProcessorNode**](/windows/desktop/api/WinBase/nf-winbase-getnumaprocessornode)                     | Recupera o número do nó do processador especificado.                                                                                                 |
| [**GetNumaProcessorNodeEx**](/windows/desktop/api/WinBase/nf-winbase-getnumaprocessornodeex)                 | Recupera o número do nó do processador lógico especificado como um valor USHORT.                                                                        |
| [**GetNumaProximityNode**](/windows/desktop/api/WinBase/nf-winbase-getnumaproximitynode)                     | Recupera o número do nó para o identificador de proximidade especificado.                                                                                      |
| [**GetNumaProximityNodeEx**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumaproximitynodeex)                 | Recupera o número do nó como um valor USHORT para o identificador de proximidade especificado.                                                                    |
| [**VirtualAllocExNuma**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocexnuma)                        | Reserva ou confirma uma região de memória dentro do espaço de endereço virtual do processo especificado e especifica o nó NUMA para a memória física. |



 

## <a name="processor-functions"></a>Funções de processador

As funções a seguir são usadas com processadores lógicos e [grupos de processadores](processor-groups.md).



| Função                                                                     | Descrição                                                                                                          |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**GetActiveProcessorCount**](/windows/desktop/api/WinBase/nf-winbase-getactiveprocessorcount)                   | Retorna o número de processadores ativos em um grupo de processador ou no sistema.                                       |
| [**GetActiveProcessorGroupCount**](/windows/desktop/api/WinBase/nf-winbase-getactiveprocessorgroupcount)         | Retorna o número de grupos de processadores ativos no sistema.                                                         |
| [**GetCurrentProcessorNumber**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessornumber)               | Recupera o número do processador no qual o thread atual estava sendo executado durante a chamada para essa função.            |
| [**GetCurrentProcessorNumberEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessornumberex)           | Recupera o grupo de processadores e o número do processador lógico no qual o thread de chamada está em execução.            |
| [**GetLogicalProcessorInformation**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformation)     | Recupera informações sobre processadores lógicos e hardwares relacionados.                                                 |
| [**GetLogicalProcessorInformationEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformationex) | Recupera informações sobre as relações de processadores lógicos e hardwares relacionados.                            |
| [**GetMaximumProcessorCount**](/windows/desktop/api/WinBase/nf-winbase-getmaximumprocessorcount)                 | Retorna o número máximo de processadores lógicos que um grupo de processador ou o sistema pode ter.                      |
| [**GetMaximumProcessorGroupCount**](/windows/desktop/api/WinBase/nf-winbase-getmaximumprocessorgroupcount)       | Retorna o número máximo de grupos de processadores que o sistema pode ter.                                             |
| [**QueryIdleProcessorCycleTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryidleprocessorcycletime)           | Recupera o tempo de ciclo para o thread ocioso de cada processador no sistema.                                        |
| [**QueryIdleProcessorCycleTimeEx**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryidleprocessorcycletimeex)       | Recupera o tempo de ciclo acumulado para o thread ocioso em cada processador lógico no grupo de processador especificado. |



 

## <a name="user-mode-scheduling-functions"></a>User-Mode funções de agendamento

As funções a seguir são usadas com o agendamento do modo de usuário (UMS).



| Função                                                               | Descrição                                                                                               |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [**CreateUmsCompletionList**](/windows/desktop/api/WinBase/nf-winbase-createumscompletionlist)             | Cria uma lista de conclusão de UMS.                                                                            |
| [**CreateUmsThreadContext**](/windows/desktop/api/WinBase/nf-winbase-createumsthreadcontext)               | Cria um contexto de thread UMS para representar um thread de trabalho do UMS.                                            |
| [**DeleteUmsCompletionList**](/windows/desktop/api/WinBase/nf-winbase-deleteumscompletionlist)             | Exclui a lista de conclusão de UMS especificada. A lista deve estar vazia.                                        |
| [**DeleteUmsThreadContext**](/windows/desktop/api/WinBase/nf-winbase-deleteumsthreadcontext)               | Exclui o contexto de thread UMS especificado. O thread deve ser encerrado.                                  |
| [**DequeueUmsCompletionListItems**](/windows/desktop/api/WinBase/nf-winbase-dequeueumscompletionlistitems) | Recupera os threads de trabalho do UMS da lista de conclusão de UMS especificada.                                      |
| [**EnterUmsSchedulingMode**](/windows/desktop/api/WinBase/nf-winbase-enterumsschedulingmode)               | Converte o thread de chamada em um thread do Agendador UMS.                                                  |
| [**ExecuteUmsThread**](/windows/desktop/api/WinBase/nf-winbase-executeumsthread)                           | Executa o thread de trabalho do UMS especificado.                                                                     |
| [**GetCurrentUmsThread**](/windows/desktop/api/WinBase/nf-winbase-getcurrentumsthread)                     | Retorna o contexto do thread UMS do thread de chamada UMS.                                                 |
| [**GetNextUmsListItem**](/windows/desktop/api/WinBase/nf-winbase-getnextumslistitem)                       | Retorna o próximo contexto de thread UMS em uma lista de contextos de thread UMS.                                     |
| [**GetUmsCompletionListEvent**](/windows/desktop/api/WinBase/nf-winbase-getumscompletionlistevent)         | Recupera um identificador para o evento associado à lista de conclusão de UMS especificada.                        |
| [**GetUmsSystemThreadInformation**](/windows/desktop/api/WinBase/nf-winbase-getumssystemthreadinformation) | Consulta se o thread especificado é um thread do Agendador UMS, um thread de trabalho do UMS ou um thread não UMS. |
| [**QueryUmsThreadInformation**](/windows/desktop/api/WinBase/nf-winbase-queryumsthreadinformation)         | Recupera informações sobre o thread de trabalho do UMS especificado.                                              |
| [**SetUmsThreadInformation**](/windows/desktop/api/WinBase/nf-winbase-setumsthreadinformation)             | Define informações de contexto específicas do aplicativo para o thread de trabalho UMS especificado.                        |
| [*UmsSchedulerProc*](/windows/desktop/api/WinNT/nc-winnt-rtl_ums_scheduler_entry_point)                             | A função de ponto de entrada do Agendador UMS definida pelo aplicativo associada a uma lista de conclusão de UMS.         |
| [**UmsThreadYield**](/windows/desktop/api/WinBase/nf-winbase-umsthreadyield)                               | Produz o controle para o thread do Agendador UMS no qual o thread de trabalho de chamada UMS está em execução.             |



 

## <a name="obsolete-functions"></a>Funções obsoletas

-   [**NtGetCurrentProcessorNumber**](ntgetcurrentprocessornumber.md)
-   [**NtQueryInformationProcess**](/windows/desktop/api/Winternl/nf-winternl-ntqueryinformationprocess)
-   [**NtQueryInformationThread**](/windows/desktop/api/Winternl/nf-winternl-ntqueryinformationthread)
-   [**WinExec**](/windows/desktop/api/WinBase/nf-winbase-winexec)
-   [**ZwQueryInformationProcess**](zwqueryinformationprocess.md)

 

 
