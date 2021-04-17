---
description: Este tópico lista as estruturas usadas com processos, threads, processadores, objetos de trabalho e UMS (agendamento de modo de usuário).
ms.assetid: dbb50193-4c67-494e-9c46-2ac3106fac9a
title: Estruturas de processo e thread
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59b2b4a8209c3f1f9fb3163c849fa2c229d2bdf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105812883"
---
# <a name="process-and-thread-structures"></a>Estruturas de processo e thread

Este tópico lista as estruturas usadas com processos, threads, processadores, objetos de trabalho e UMS (agendamento de modo de usuário).

## <a name="process-and-thread-structures"></a>Estruturas de processo e thread

As seguintes estruturas são usadas com processos e threads:

-   [**\_informações de memória do aplicativo \_**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-app_memory_information)
-   [**\_estado ar**](/windows/win32/api/winuser/ne-winuser-ar_state)
-   [**\_descritor de cache**](/windows/desktop/api/WinNT/ns-winnt-cache_descriptor)
-   [**contadores de e/s \_**](/windows/desktop/api/WinNT/ns-winnt-io_counters)
-   [**preferência de orientação \_**](/windows/desktop/api/WinUser/ne-winuser-orientation_preference)
-   [**PEB**](/windows/desktop/api/Winternl/ns-winternl-peb)
-   [**\_dados PEB LDR \_**](/windows/desktop/api/Winternl/ns-winternl-peb_ldr_data)
-   [**informações do processo \_**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_information)
-   [**\_informações de \_ esgotamento de memória do processo \_**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_memory_exhaustion_info)
-   [**\_política de ASLR de mitigação de processo \_ \_**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_aslr_policy)
-   [**\_ \_ política de assinatura binária de mitigação de processos \_ \_**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_binary_signature_policy)
-   [**\_política de proteção do fluxo de controle de mitigação de processos \_ \_ \_ \_**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_control_flow_guard_policy)
-   [**\_política DEP de mitigação de processos \_ \_**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_dep_policy)
-   [**\_ \_ política de código dinâmico de mitigação de processos \_ \_**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_dynamic_code_policy)
-   [**\_ \_ política de \_ \_ desabilitação de ponto de extensão \_ de mitigação de processo**](/windows/desktop/api/winnt/ns-winnt-process_mitigation_extension_point_disable_policy)
-   [**\_ \_ política de \_ desabilitação de fonte de MITIGAção de processo \_**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_font_disable_policy)
-   [**\_política de carregamento de imagem de mitigação de processos \_ \_ \_**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_image_load_policy)
-   [**\_política de \_ \_ verificação de identificador \_ estrito \_ de mitigação de processo**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_strict_handle_check_policy)
-   [**\_ \_ política de \_ \_ desabilitação de chamada do sistema \_ de mitigação de processos**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_system_call_disable_policy)
-   [**\_parâmetros de \_ processo de usuário DPE \_**](/windows/desktop/api/Winternl/ns-winternl-rtl_user_process_parameters)
-   [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)
-   [**STARTUPINFOEX**](/windows/desktop/api/WinBase/ns-winbase-startupinfoexa)
-   [**TEB**](/windows/desktop/api/Winternl/ns-winternl-teb)

## <a name="processor-structures"></a>Estruturas de processador

As seguintes estruturas são usadas com processadores e grupos de processadores:

-   [**relação de CACHE \_**](/windows/desktop/api/WinNT/ns-winnt-cache_relationship)
-   [**afinidade de grupo \_**](/windows/desktop/api/WinNT/ns-winnt-group_affinity)
-   [**relação de grupo \_**](/windows/desktop/api/WinNT/ns-winnt-group_relationship)
-   [**\_relacionamento de nó numa \_**](/windows/desktop/api/WinNT/ns-winnt-numa_node_relationship)
-   [**\_informações do grupo de processador \_**](/windows/desktop/api/WinNT/ns-winnt-processor_group_info)
-   [**número do processador \_**](/windows/desktop/api/WinNT/ns-winnt-processor_number)
-   [**relação do processador \_**](/windows/desktop/api/WinNT/ne-winnt-logical_processor_relationship)
-   [**\_informações do \_ conjunto de CPU do sistema \_**](/windows/desktop/api/winnt/ns-winnt-system_cpu_set_information)
-   [**\_informações do \_ processador \_ lógico do sistema**](/windows/desktop/api/WinNT/ns-winnt-system_logical_processor_information)
-   [**\_informações do processador lógico do sistema \_ \_ \_ ex.**](/windows/desktop/api/WinNT/ns-winnt-system_logical_processor_information_ex)

## <a name="dispatcher-queue-structure"></a>Estrutura da fila do Dispatcher

A estrutura a seguir é usada para criar um [DispatcherQueueController](/uwp/api/windows.system.dispatcherqueuecontroller).

-   [**DispatcherQueueOptions**](/windows/desktop/api/DispatcherQueue/ns-dispatcherqueue-dispatcherqueueoptions)

## <a name="job-object-structures"></a>Estruturas de objeto de trabalho

As seguintes estruturas são usadas com objetos de trabalho:

-   [**\_porta de \_ conclusão da associação do JOBOBJECT \_**](/windows/desktop/api/WinNT/ns-winnt-jobobject_associate_completion_port)
-   [**informações de contabilidade do JOBOBJECT \_ Basic \_ \_**](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_accounting_information)
-   [**\_ \_ informações de contabilidade do JOBOBJECT Basic e \_ Io \_ \_**](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_and_io_accounting_information)
-   [**\_informações de \_ limite \_ básico do JOBOBJECT**](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_limit_information)
-   [**\_lista de \_ ID de processo básica \_ do JOBOBJECT \_**](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_process_id_list)
-   [**\_restrições básicas de \_ interface do usuário do JOBOBJECT \_**](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_ui_restrictions)
-   [**JOBOBJECT \_ fim \_ das \_ \_ informações de hora do trabalho \_**](/windows/desktop/api/WinNT/ns-winnt-jobobject_end_of_job_time_information)
-   [**\_informações de \_ limite ESTENDIdo JOBOBJECT \_**](/windows/desktop/api/WinNT/ns-winnt-jobobject_extended_limit_information)
-   [**\_informações de \_ limite de segurança do JOBOBJECT \_**](/windows/desktop/api/WinNT/ns-winnt-jobobject_security_limit_information)

## <a name="user-mode-scheduling-structures"></a>Estruturas de agendamento de User-Mode

As seguintes estruturas são usadas com UMS:

-   [**UMS \_ criar \_ atributos de thread \_**](/windows/desktop/api/WinNT/ns-winnt-ums_create_thread_attributes)
-   [**\_informações de inicialização do Agendador ums \_ \_**](/windows/desktop/api/WinBase/ns-winbase-ums_scheduler_startup_info)
-   [**\_informações de \_ thread do sistema ums \_**](/windows/desktop/api/WinBase/ns-winbase-ums_system_thread_information)

 

 
