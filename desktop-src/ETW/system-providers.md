---
title: Provedores de sistema
description: Habilita eventos do Provedor de Rastreamento do Sistema com EnableTraceEx2.
ms.topic: article
ms.date: 06/02/2021
ms.openlocfilehash: 48a93ab94b87a43e0eb8a292320536a04ef43477
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387784"
---
# <a name="system-providers"></a>Provedores de sistema
 
A partir do Windows 10 build 20348 do SDK, os eventos do Provedor de Rastreamento do Sistema podem ser habilitados da mesma maneira que outros provedores ETW, com [EnableTraceEx2](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2).  Os diferentes sinalizadores e máscaras de grupo [associados](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) ao Provedor de Rastreamento do Sistema foram mapeados para novos provedores de rastreamento, chamados Provedores de Sistema, e palavras-chave correspondentes.  
 
Assim como habilitar o Provedor de Rastreamento do Sistema diretamente, os Provedores de Sistema só podem ser habilitados por uma sessão com o [EVENT_TRACE_SYSTEM_LOGGER_MODE](/windows/win32/etw/logging-mode-constants) definido.

## <a name="system-provider-reference"></a>Referência do Provedor de Sistema

* [Provedor ALPC do sistema](#system-alpc-provider)
* [Provedor de Configuração do Sistema](#system-config-provider)
* [Provedor de CPU do sistema](#system-cpu-provider)
* [Provedor de Hipervisor do Sistema](#system-hypervisor-provider)
* [Provedor de Interrupção do Sistema](#system-interrupt-provider)
* [Provedor de E/S do sistema](#system-io-provider)
* [Provedor de Filtro de E/S do Sistema](#system-io-filter-provider)
* [Provedor de Bloqueio do Sistema](#system-lock-provider)
* [Provedor de Memória do Sistema](#system-memory-provider)
* [Provedor de Objetos do Sistema](#system-object-provider)
* [Provedor de Energia do Sistema](#system-power-provider)
* [Provedor de Processo do Sistema](#system-process-provider)
* [Provedor de Perfil do Sistema](#system-profile-provider)
* [Provedor de Registro do Sistema](#system-registry-provider)
* [Provedor do Agendador do Sistema](#system-scheduler-provider)
* [Provedor de Syscall do Sistema](#system-syscall-provider)
* [Provedor de Temporizador do Sistema](#system-timer-provider)
 
### <a name="system-alpc-provider"></a>Provedor ALPC do sistema

Fornece eventos relacionados ao sistema ALPC.

GUID: SystemAlpcProviderGuid {fcb9baaf-e529-4980-92e9-ced1a6aadfdf}

| Palavra-chave | Sinalizadores e grupos herdados correspondentes |
| ------- | ------------------------------------- |
| SYSTEM_ALPC_KW_GENERAL | PERF_ALPC, EVENT_TRACE_FLAG_ALPC |
 
### <a name="system-config-provider"></a>Provedor de Configuração do Sistema 

Fornece eventos de configuração do sistema.

GUID: SystemConfigProviderGuid {fef3a8b6-318d-4b67-a96a-3b0f6b8f18fe}

| Palavra-chave | Sinalizadores e grupos herdados correspondentes |
| ------- | ------------------------------------- |
| SYSTEM_CONFIG_KW_SYSTEM | PERF_SYSCFG_SYSTEM |
| SYSTEM_CONFIG_KW_GRAPHICS | PERF_SYSCFG_GRAPHICS |
| SYSTEM_CONFIG_KW_STORAGE | PERF_SYSCFG_STORAGE |
| SYSTEM_CONFIG_KW_NETWORK | PERF_SYSCFG_NETWORK |
| SYSTEM_CONFIG_KW_SERVICES | PERF_SYSCFG_SERVICES |
| SYSTEM_CONFIG_KW_PNP | PERF_SYSCFG_PNP |
| SYSTEM_CONFIG_KW_OPTICAL | PERF_SYSCFG_OPTICAL |
 
### <a name="system-cpu-provider"></a>Provedor de CPU do sistema 

Fornece eventos relacionados à CPU.

GUID: SystemCpuProviderGuid {c6c5265f-eae8-4650-aae4-9d48603d8510}

| Palavra-chave | Sinalizadores e grupos herdados correspondentes |
| ------- | ------------------------------------- |
| SYSTEM_CPU_KW_CONFIG | PERF_CPU_CONFIG |
| SYSTEM_CPU_KW_CACHE_FLUSH | PERF_CACHE_FLUSH |
| SYSTEM_CPU_KW_SPEC_CONTROL | PERF_SPEC_CONTROL |
 
### <a name="system-hypervisor-provider"></a>Provedor de Hipervisor do Sistema 

Fornece eventos relacionados ao hipervisor.

GUID: SystemHypervisorProviderGuid {bafa072a-918a-4bed-b622-bc152097098f}

| Palavra-chave | Sinalizadores e grupos herdados correspondentes |
| ------- | ------------------------------------- |
| SYSTEM_HYPERVISOR_KW_PROFILE | PERF_HV_PROFILE |
| SYSTEM_HYPERVISOR_KW_CALLOUTS | PERF_HV_CALLOUTS |
| SYSTEM_HYPERVISOR_KW_VTL_CHANGE | PERF_VTL_CHANGE |
 
### <a name="system-interrupt-provider"></a>Provedor de Interrupção do Sistema 

Fornece eventos relacionados a DPCs e interrupções.

GUID: SystemInterruptProviderGuid {d4bbee17-b545-4888-858b-744169015b25}

| Palavra-chave | Sinalizadores e grupos herdados correspondentes |
| ------- | ------------------------------------- |
| SYSTEM_INTERRUPT_KW_GENERAL | PERF_INTERRUPT, EVENT_TRACE_FLAG_INTERRUPT |
| SYSTEM_INTERRUPT_KW_CLOCK_INTERRUPT | PERF_CLOCK_INTERRUPT |
| SYSTEM_INTERRUPT_KW_DPC | PERF_DPC, EVENT_TRACE_FLAG_DPC |
| SYSTEM_INTERRUPT_KW_DPC_QUEUE | PERF_DPC_QUEUE |
| SYSTEM_INTERRUPT_KW_WDF_DPC | PERF_WDF_DPC |
| SYSTEM_INTERRUPT_KW_WDF_INTERRUPT | PERF_WDF_INTERRUPT |
| SYSTEM_INTERRUPT_KW_IPI | PERF_IPI |
 
 
### <a name="system-io-provider"></a>Provedor de E/S do sistema 

Fornece eventos relacionados a vários tipos de E/S, incluindo disco, cache e rede.

GUID: SystemIoProviderGuid {3d5c43e3-0f1c-4202-b817-174c0070dc79}

| Palavra-chave | Sinalizadores e grupos herdados correspondentes |
| ------- | ------------------------------------- |
| SYSTEM_IO_KW_DISK | EVENT_TRACE_FLAG_DISK_IO |
| SYSTEM_IO_KW_DISK_INIT | PERF_DISK_IO_INIT, EVENT_TRACE_FLAG_DISK_IO_INIT |
| SYSTEM_IO_KW_FILENAME | PERF_FILENAME, EVENT_TRACE_FLAG_DISK_FILE_IO |
| SYSTEM_IO_KW_SPLIT | PERF_SPLIT_IO, EVENT_TRACE_FLAG_SPLIT_IO |
| SYSTEM_IO_KW_FILE | PERF_FILE_IO, EVENT_TRACE_FLAG_FILE_IO |
| SYSTEM_IO_KW_OPTICAL | PERF_OPTICAL_IO, EVENT_TRACE_FLAG_FILE_IO_INIT |
| SYSTEM_IO_KW_OPTICAL_INIT | PERF_OPTICAL_IO_INIT |
| SYSTEM_IO_KW_DRIVERS | PERF_DRIVERS, EVENT_TRACE_FLAG_DRIVER |
| SYSTEM_IO_KW_CC | PERF_CC |
| SYSTEM_IO_KW_NETWORK | PERF_NETWORK, EVENT_TRACE_FLAG_NETWORK_TCPIP |

Observação: habilitar SYSTEM_IO_KW_DRIVERS palavra-chave do SYSTEM_IO_KW_FILENAME habilita automaticamente também.  O SYSTEM_IO_KW_FILENAME também é ativado automaticamente quando o Provedor de Memória do Sistema está habilitado com a palavra-chave SYSTEM_MEMORY_KW_MEMORY dados.
 
### <a name="system-io-filter-provider"></a>Provedor de Filtro de E/S do Sistema 

Fornece eventos relacionados à filtragem de E/S, incluindo tempo e falhas.

GUID: SystemIoFilterProviderGuid {fbd09363-9e22-4661-b8bf-e7a34b535b8c}

| Palavra-chave | Sinalizadores e grupos herdados correspondentes |
| ------- | ------------------------------------- |
| SYSTEM_IOFILTER_KW_GENERAL | PERF_FLT_IO |
| SYSTEM_IOFILTER_KW_INIT | PERF_FLT_IO_INIT |
| SYSTEM_IOFILTER_KW_FASTIO | PERF_FLT_FASTIO |
| SYSTEM_IOFILTER_KW_FAILURE | PERF_FLT_IO_FAILURE |
 
### <a name="system-lock-provider"></a>Provedor de Bloqueio do Sistema 

Fornece eventos relacionados a mecanismos de bloqueio de kernel.

GUID: SystemLockProviderGuid {721ddfd3-dacc-4e1e-b26a-a2cb31d4705a}

| Palavra-chave | Sinalizadores e grupos herdados correspondentes |
| ------- | ------------------------------------- |
| SYSTEM_LOCK_KW_SPINLOCK | PERF_SPINLOCK |
| SYSTEM_LOCK_KW_SPINLOCK_COUNTERS | PERF_SPINLOCK_CNTRS |
| SYSTEM_LOCK_KW_SYNC_OBJECTS | PERF_SYNC_OBJECTS |
 
### <a name="system-memory-provider"></a>Provedor de Memória do Sistema 

Fornece eventos relacionados ao gerenciador de memória.

GUID: SystemMemoryProviderGuid {82958ca9-b6cd-47f8-a3a8-03ae85a4bc24}

| Palavra-chave | Sinalizadores e grupos herdados correspondentes |
| ------- | ------------------------------------- |
| SYSTEM_MEMORY_KW_GENERAL | PERF_MEMORY |
| SYSTEM_MEMORY_KW_HARD_FAULTS | PERF_HARD_FAULTS, EVENT_TRACE_FLAG_MEMORY_HARD_FAULTS |
| SYSTEM_MEMORY_KW_ALL_FAULTS | PERF_ALL_FAULTS, EVENT_TRACE_FLAG_MEMORY_PAGE_FAULTS |
| SYSTEM_MEMORY_KW_POOL | PERF_POOL |
| SYSTEM_MEMORY_KW_MEMINFO | PERF_MEMINFO |
| SYSTEM_MEMORY_KW_PFSECTION | PERF_PFSECTION |
| SYSTEM_MEMORY_KW_MEMINFO_WS | PERF_MEMINFO_WS |
| SYSTEM_MEMORY_KW_HEAP | PERF_HEAP |
| SYSTEM_MEMORY_KW_WS | PERF_WS |
| SYSTEM_MEMORY_KW_CONTMEM_GEN | PERF_CONTMEM_GEN |
| SYSTEM_MEMORY_KW_VIRTUAL_ALLOC | PERF_VIRTUAL_ALLOC, EVENT_TRACE_FLAG_VIRTUAL_ALLOC |
| SYSTEM_MEMORY_KW_FOOTPRINT | PERF_FOOTPRINT |
| SYSTEM_MEMORY_KW_SESSION | PERF_SESSION |
| SYSTEM_MEMORY_KW_REFSET | PERF_REFSET |
| SYSTEM_MEMORY_KW_VAMAP | PERF_VAMAP, EVENT_TRACE_FLAG_VAMAP |

Observações: 
* Habilitar a SYSTEM_MEMORY_KW_MEMORY de usuário habilita automaticamente SYSTEM_IO_KW_FILENAME no Provedor de E/S do Sistema também.
* Os eventos habilitados pelo SYSTEM_MEMORY_KW_POOL dar suporte a um Filtro de Marca de Pool para gravar eventos seletivamente somente para determinadas marcas de pool.  Isso é configurado como um [Filtro Eschematizado](/windows/win32/api/evntprov/ns-evntprov-event_filter_descriptor) no Provedor de Memória do Sistema.  O filtro PoolTag é construído da seguinte forma:

    ```cpp
    {
    EVENT_FILTER_HEADER Header; 
    ULONG PoolTags[ETW_MAX_POOLTAG_FILTER];
    }
    ```

* O [EVENT_FILTER_HEADER](/windows/win32/api/evntprov/ns-evntprov-event_filter_header) deve ser inicializado com a ID definida como SYSTEM_MEMORY_POOL_FILTER_ID e o campo de tamanho definido como o tamanho de Header mais a parte usada da matriz PoolTags.  

* Cada Marca de Pool é uma cadeia de caracteres de 4 caracteres armazenada como um ULONG no filtro.  
 
 
### <a name="system-object-provider"></a>Provedor de Objetos do Sistema 

Fornece eventos relacionados ao Gerenciador de Objetos.

GUID: SystemObjectProviderGuid {febd7460-3d1d-47eb-af49-c9eeb1e146f2}

| Palavra-chave | Sinalizadores e grupos herdados correspondentes |
| ------- | ------------------------------------- |
| SYSTEM_OBJECT_KW_HANDLE | PERF_OB_HANDLE |
| SYSTEM_OBJECT_KW_OBJECT | PERF_OB_OBJECT |
 
### <a name="system-power-provider"></a>Provedor de Energia do Sistema 

Fornece eventos relacionados ao estado de energia do sistema.

GUID: SystemPowerProviderGuid {c134884a-32d5-4488-80e5-14ed7abb8269}

| Palavra-chave | Sinalizadores e grupos herdados correspondentes |
| ------- | ------------------------------------- |
| SYSTEM_POWER_KW_GENERAL | PERF_POWER |
| SYSTEM_POWER_KW_HIBER_RUNDOWN | PERF_HIBER_RUNDOWN |
| SYSTEM_POWER_KW_PROCESSOR_IDLE | PERF_PROCESSOR_IDLE |
| SYSTEM_POWER_KW_IDLE_SELECTION | PERF_IDLE_SELECTION |
| SYSTEM_POWER_KW_PPM_EXIT_LATENCY | PERF_PPM_EXIT_LATENCY |
 
### <a name="system-process-provider"></a>Provedor de processo do sistema 

Fornece eventos relacionados ao processo, incluindo informações de tempo de vida, eventos de carga de imagem e eventos relacionados a threads.

GUID: SystemProcessProviderGuid {151f55dc-467d-471f-83b5-5f889d46ff66}

| Palavra-chave | Sinalizadores e grupos herdados correspondentes |
| ------- | ------------------------------------- |
| SYSTEM_PROCESS_KW_GENERAL | PERF_PROCESS, EVENT_TRACE_FLAG_PROCESS |
| SYSTEM_PROCESS_KW_INSWAP | PERF_PROCESS_INSWAP |
| SYSTEM_PROCESS_KW_FREEZE | PERF_PROCESS_FREEZE |
| SYSTEM_PROCESS_KW_PERF_COUNTER | PERF_PERF_COUNTER, EVENT_TRACE_FLAG_PROCESS_COUNTERS |
| SYSTEM_PROCESS_KW_WAKE_COUNTER | PERF_WAKE_COUNTER |
| SYSTEM_PROCESS_KW_WAKE_DROP | PERF_WAKE_DROP |
| SYSTEM_PROCESS_KW_WAKE_EVENT | PERF_WAKE_EVENT |
| SYSTEM_PROCESS_KW_DEBUG_EVENTS | PERF_DEBUG_EVENTS, EVENT_TRACE_FLAG_DEBUG_EVENTS |
| SYSTEM_PROCESS_KW_DBGPRINT | PERF_DBGPRINT, EVENT_TRACE_FLAG_DBGPRINT |
| SYSTEM_PROCESS_KW_JOB | PERF_JOB, EVENT_TRACE_FLAG_JOB |
| SYSTEM_PROCESS_KW_WORKER_THREAD | PERF_WORKER_THREAD |
| SYSTEM_PROCESS_KW_THREAD | PERF_THREAD, EVENT_TRACE_FLAG_THREAD |
| SYSTEM_PROCESS_KW_LOADER | PERF_LOADER, EVENT_TRACE_FLAG_IMAGE_LOAD |
 
### <a name="system-profile-provider"></a>Provedor de perfil do sistema 

Fornece eventos de criação de perfil.

GUID: SystemProfileProviderGuid {bfeb0324-1cee-496F-a409-2ac2b48a6322}

| Palavra-chave | Sinalizadores e grupos herdados correspondentes |
| ------- | ------------------------------------- |
| SYSTEM_PROFILE_KW_GENERAL | PERF_PROFILE, EVENT_TRACE_FLAG_PROFILE |
| SYSTEM_PROFILE_KW_PMC_PROFILE | PERF_PMC_PROFILE |
 
### <a name="system-registry-provider"></a>Provedor de registro do sistema 

Fornece eventos relacionados ao registro.

GUID: SystemRegistryProviderGuid {16156bd9-Fab4-4cfa-A232-89d1099058e3}

| Palavra-chave | Sinalizadores e grupos herdados correspondentes |
| ------- | ------------------------------------- |
| SYSTEM_REGISTRY_KW_GENERAL | PERF_REGISTRY, EVENT_TRACE_FLAG_REGISTRY |
| SYSTEM_REGISTRY_KW_HIVE | PERF_REG_HIVE |
| SYSTEM_REGISTRY_KW_NOTIFICATION | PERF_REG_NOTIF |
 
### <a name="system-scheduler-provider"></a>Provedor do Agendador do sistema 

Fornece eventos relacionados ao agendador.

GUID: SystemSchedulerProviderGuid {599a2a76-4d91-4910-9AC7-7d33f2e97a6c}

| Palavra-chave | Sinalizadores e grupos herdados correspondentes |
| ------- | ------------------------------------- |
| SYSTEM_SCHEDULER_KW_XSCHEDULER | PERF_XSCHEDULER |
| SYSTEM_SCHEDULER_KW_DISPATCHER | PERF_DISPATCHER, EVENT_TRACE_FLAG_DISPATCHER |
| SYSTEM_SCHEDULER_KW_KERNEL_QUEUE | PERF_KERNEL_QUEUE |
| SYSTEM_SCHEDULER_KW_SHOULD_YIELD | PERF_SHOULD_YIELD |
| SYSTEM_SCHEDULER_KW_ANTI_STARVATION | PERF_ANTI_STARVATION |
| SYSTEM_SCHEDULER_KW_LOAD_BALANCER | PERF_LOAD_BALANCER |
| SYSTEM_SCHEDULER_KW_AFFINITY | PERF_AFFINITY |
| SYSTEM_SCHEDULER_KW_PRIORITY | PERF_PRIORITY |
| SYSTEM_SCHEDULER_KW_IDEAL_PROCESSOR | PERF_IDEAL_PROCESSOR |
| SYSTEM_SCHEDULER_KW_CONTEXT_SWITCH | PERF_CONTEXT_SWITCH, EVENT_TRACE_FLAG_CSWITCH |
 
### <a name="system-syscall-provider"></a>Provedor syscall do sistema 

Fornece eventos com informações sobre chamadas do sistema.

GUID: SystemSyscallProviderGuid {434286f7-6f1b-45BB-b37e-95f623046c7c}

| Palavra-chave | Sinalizadores e grupos herdados correspondentes |
| ------- | ------------------------------------- |
| SYSTEM_SYSCALL_KW_GENERAL | PERF_SYSCALL, EVENT_TRACE_FLAG_SYSTEMCALL |
 
### <a name="system-timer-provider"></a>Provedor de timer do sistema 

Fornece eventos relacionados a temporizadores no kernel.

GUID: SystemTimerProviderGuid {4f061568-E215-499f-ab2e-eda0ae890a5b}

| Palavra-chave | Sinalizadores e grupos herdados correspondentes |
| ------- | ------------------------------------- |
| SYSTEM_TIMER_KW_GENERAL | PERF_TIMER |
| SYSTEM_TIMER_KW_CLOCK_TIMER | PERF_CLOCK_TIMER |
 
## <a name="remarks"></a>Comentários

Esse novo mecanismo de habilitação é além dos métodos preexistentes para habilitar esses eventos.  Qualquer código que costumava funcionar, continuará a fazer isso.
 
Os eventos gerados pelo provedor de rastreamento do sistema não estão mudando devido a esse novo recurso.  Isso significa que os eventos de saída não são marcados como sendo emitidos por provedores de sistema individuais.
 
Para obter mais informações sobre o GUID do provedor e as definições de palavra-chave, consulte [evntrace. h](/windows/win32/api/evntrace/).

## <a name="see-also"></a>Consulte Também

[Configurando e iniciando uma sessão SystemTraceProvider](configuring-and-starting-a-systemtraceprovider-session.md)

[cabeçalho evntrace. h](/windows/win32/api/evntrace/)