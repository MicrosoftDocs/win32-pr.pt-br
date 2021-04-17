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
# <a name="process-and-thread-structures"></a><span data-ttu-id="17a5c-103">Estruturas de processo e thread</span><span class="sxs-lookup"><span data-stu-id="17a5c-103">Process and Thread Structures</span></span>

<span data-ttu-id="17a5c-104">Este tópico lista as estruturas usadas com processos, threads, processadores, objetos de trabalho e UMS (agendamento de modo de usuário).</span><span class="sxs-lookup"><span data-stu-id="17a5c-104">This topic lists structures that are used with processes, threads, processors, job objects, and user-mode scheduling (UMS).</span></span>

## <a name="process-and-thread-structures"></a><span data-ttu-id="17a5c-105">Estruturas de processo e thread</span><span class="sxs-lookup"><span data-stu-id="17a5c-105">Process and Thread Structures</span></span>

<span data-ttu-id="17a5c-106">As seguintes estruturas são usadas com processos e threads:</span><span class="sxs-lookup"><span data-stu-id="17a5c-106">The following structures are used with processes and threads:</span></span>

-   [<span data-ttu-id="17a5c-107">**\_informações de memória do aplicativo \_**</span><span class="sxs-lookup"><span data-stu-id="17a5c-107">**APP\_MEMORY\_INFORMATION**</span></span>](/windows/win32/api/processthreadsapi/ns-processthreadsapi-app_memory_information)
-   [<span data-ttu-id="17a5c-108">**\_estado ar**</span><span class="sxs-lookup"><span data-stu-id="17a5c-108">**AR\_STATE**</span></span>](/windows/win32/api/winuser/ne-winuser-ar_state)
-   [<span data-ttu-id="17a5c-109">**\_descritor de cache**</span><span class="sxs-lookup"><span data-stu-id="17a5c-109">**CACHE\_DESCRIPTOR**</span></span>](/windows/desktop/api/WinNT/ns-winnt-cache_descriptor)
-   [<span data-ttu-id="17a5c-110">**contadores de e/s \_**</span><span class="sxs-lookup"><span data-stu-id="17a5c-110">**IO\_COUNTERS**</span></span>](/windows/desktop/api/WinNT/ns-winnt-io_counters)
-   [<span data-ttu-id="17a5c-111">**preferência de orientação \_**</span><span class="sxs-lookup"><span data-stu-id="17a5c-111">**ORIENTATION\_PREFERENCE**</span></span>](/windows/desktop/api/WinUser/ne-winuser-orientation_preference)
-   [<span data-ttu-id="17a5c-112">**PEB**</span><span class="sxs-lookup"><span data-stu-id="17a5c-112">**PEB**</span></span>](/windows/desktop/api/Winternl/ns-winternl-peb)
-   [<span data-ttu-id="17a5c-113">**\_dados PEB LDR \_**</span><span class="sxs-lookup"><span data-stu-id="17a5c-113">**PEB\_LDR\_DATA**</span></span>](/windows/desktop/api/Winternl/ns-winternl-peb_ldr_data)
-   [<span data-ttu-id="17a5c-114">**informações do processo \_**</span><span class="sxs-lookup"><span data-stu-id="17a5c-114">**PROCESS\_INFORMATION**</span></span>](/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_information)
-   [<span data-ttu-id="17a5c-115">**\_informações de \_ esgotamento de memória do processo \_**</span><span class="sxs-lookup"><span data-stu-id="17a5c-115">**PROCESS\_MEMORY\_EXHAUSTION\_INFO**</span></span>](/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_memory_exhaustion_info)
-   [<span data-ttu-id="17a5c-116">**\_política de ASLR de mitigação de processo \_ \_**</span><span class="sxs-lookup"><span data-stu-id="17a5c-116">**PROCESS\_MITIGATION\_ASLR\_POLICY**</span></span>](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_aslr_policy)
-   [<span data-ttu-id="17a5c-117">**\_ \_ política de assinatura binária de mitigação de processos \_ \_**</span><span class="sxs-lookup"><span data-stu-id="17a5c-117">**PROCESS\_MITIGATION\_BINARY\_SIGNATURE\_POLICY**</span></span>](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_binary_signature_policy)
-   [<span data-ttu-id="17a5c-118">**\_política de proteção do fluxo de controle de mitigação de processos \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="17a5c-118">**PROCESS\_MITIGATION\_CONTROL\_FLOW\_GUARD\_POLICY**</span></span>](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_control_flow_guard_policy)
-   [<span data-ttu-id="17a5c-119">**\_política DEP de mitigação de processos \_ \_**</span><span class="sxs-lookup"><span data-stu-id="17a5c-119">**PROCESS\_MITIGATION\_DEP\_POLICY**</span></span>](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_dep_policy)
-   [<span data-ttu-id="17a5c-120">**\_ \_ política de código dinâmico de mitigação de processos \_ \_**</span><span class="sxs-lookup"><span data-stu-id="17a5c-120">**PROCESS\_MITIGATION\_DYNAMIC\_CODE\_POLICY**</span></span>](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_dynamic_code_policy)
-   [<span data-ttu-id="17a5c-121">**\_ \_ política de \_ \_ desabilitação de ponto de extensão \_ de mitigação de processo**</span><span class="sxs-lookup"><span data-stu-id="17a5c-121">**PROCESS\_MITIGATION\_EXTENSION\_POINT\_DISABLE\_POLICY**</span></span>](/windows/desktop/api/winnt/ns-winnt-process_mitigation_extension_point_disable_policy)
-   [<span data-ttu-id="17a5c-122">**\_ \_ política de \_ desabilitação de fonte de MITIGAção de processo \_**</span><span class="sxs-lookup"><span data-stu-id="17a5c-122">**PROCESS\_MITIGATION\_FONT\_DISABLE\_POLICY**</span></span>](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_font_disable_policy)
-   [<span data-ttu-id="17a5c-123">**\_política de carregamento de imagem de mitigação de processos \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="17a5c-123">**PROCESS\_MITIGATION\_IMAGE\_LOAD\_POLICY**</span></span>](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_image_load_policy)
-   [<span data-ttu-id="17a5c-124">**\_política de \_ \_ verificação de identificador \_ estrito \_ de mitigação de processo**</span><span class="sxs-lookup"><span data-stu-id="17a5c-124">**PROCESS\_MITIGATION\_STRICT\_HANDLE\_CHECK\_POLICY**</span></span>](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_strict_handle_check_policy)
-   [<span data-ttu-id="17a5c-125">**\_ \_ política de \_ \_ desabilitação de chamada do sistema \_ de mitigação de processos**</span><span class="sxs-lookup"><span data-stu-id="17a5c-125">**PROCESS\_MITIGATION\_SYSTEM\_CALL\_DISABLE\_POLICY**</span></span>](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_system_call_disable_policy)
-   [<span data-ttu-id="17a5c-126">**\_parâmetros de \_ processo de usuário DPE \_**</span><span class="sxs-lookup"><span data-stu-id="17a5c-126">**RTL\_USER\_PROCESS\_PARAMETERS**</span></span>](/windows/desktop/api/Winternl/ns-winternl-rtl_user_process_parameters)
-   [<span data-ttu-id="17a5c-127">**STARTUPINFO**</span><span class="sxs-lookup"><span data-stu-id="17a5c-127">**STARTUPINFO**</span></span>](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)
-   [<span data-ttu-id="17a5c-128">**STARTUPINFOEX**</span><span class="sxs-lookup"><span data-stu-id="17a5c-128">**STARTUPINFOEX**</span></span>](/windows/desktop/api/WinBase/ns-winbase-startupinfoexa)
-   [<span data-ttu-id="17a5c-129">**TEB**</span><span class="sxs-lookup"><span data-stu-id="17a5c-129">**TEB**</span></span>](/windows/desktop/api/Winternl/ns-winternl-teb)

## <a name="processor-structures"></a><span data-ttu-id="17a5c-130">Estruturas de processador</span><span class="sxs-lookup"><span data-stu-id="17a5c-130">Processor Structures</span></span>

<span data-ttu-id="17a5c-131">As seguintes estruturas são usadas com processadores e grupos de processadores:</span><span class="sxs-lookup"><span data-stu-id="17a5c-131">The following structures are used with processors and processor groups:</span></span>

-   [<span data-ttu-id="17a5c-132">**relação de CACHE \_**</span><span class="sxs-lookup"><span data-stu-id="17a5c-132">**CACHE\_RELATIONSHIP**</span></span>](/windows/desktop/api/WinNT/ns-winnt-cache_relationship)
-   [<span data-ttu-id="17a5c-133">**afinidade de grupo \_**</span><span class="sxs-lookup"><span data-stu-id="17a5c-133">**GROUP\_AFFINITY**</span></span>](/windows/desktop/api/WinNT/ns-winnt-group_affinity)
-   [<span data-ttu-id="17a5c-134">**relação de grupo \_**</span><span class="sxs-lookup"><span data-stu-id="17a5c-134">**GROUP\_RELATIONSHIP**</span></span>](/windows/desktop/api/WinNT/ns-winnt-group_relationship)
-   [<span data-ttu-id="17a5c-135">**\_relacionamento de nó numa \_**</span><span class="sxs-lookup"><span data-stu-id="17a5c-135">**NUMA\_NODE\_RELATIONSHIP**</span></span>](/windows/desktop/api/WinNT/ns-winnt-numa_node_relationship)
-   [<span data-ttu-id="17a5c-136">**\_informações do grupo de processador \_**</span><span class="sxs-lookup"><span data-stu-id="17a5c-136">**PROCESSOR\_GROUP\_INFO**</span></span>](/windows/desktop/api/WinNT/ns-winnt-processor_group_info)
-   [<span data-ttu-id="17a5c-137">**número do processador \_**</span><span class="sxs-lookup"><span data-stu-id="17a5c-137">**PROCESSOR\_NUMBER**</span></span>](/windows/desktop/api/WinNT/ns-winnt-processor_number)
-   [<span data-ttu-id="17a5c-138">**relação do processador \_**</span><span class="sxs-lookup"><span data-stu-id="17a5c-138">**PROCESSOR\_RELATIONSHIP**</span></span>](/windows/desktop/api/WinNT/ne-winnt-logical_processor_relationship)
-   [<span data-ttu-id="17a5c-139">**\_informações do \_ conjunto de CPU do sistema \_**</span><span class="sxs-lookup"><span data-stu-id="17a5c-139">**SYSTEM\_CPU\_SET\_INFORMATION**</span></span>](/windows/desktop/api/winnt/ns-winnt-system_cpu_set_information)
-   [<span data-ttu-id="17a5c-140">**\_informações do \_ processador \_ lógico do sistema**</span><span class="sxs-lookup"><span data-stu-id="17a5c-140">**SYSTEM\_LOGICAL\_PROCESSOR\_INFORMATION**</span></span>](/windows/desktop/api/WinNT/ns-winnt-system_logical_processor_information)
-   [<span data-ttu-id="17a5c-141">**\_informações do processador lógico do sistema \_ \_ \_ ex.**</span><span class="sxs-lookup"><span data-stu-id="17a5c-141">**SYSTEM\_LOGICAL\_PROCESSOR\_INFORMATION\_EX**</span></span>](/windows/desktop/api/WinNT/ns-winnt-system_logical_processor_information_ex)

## <a name="dispatcher-queue-structure"></a><span data-ttu-id="17a5c-142">Estrutura da fila do Dispatcher</span><span class="sxs-lookup"><span data-stu-id="17a5c-142">Dispatcher Queue Structure</span></span>

<span data-ttu-id="17a5c-143">A estrutura a seguir é usada para criar um [DispatcherQueueController](/uwp/api/windows.system.dispatcherqueuecontroller).</span><span class="sxs-lookup"><span data-stu-id="17a5c-143">The following structure is used to create a [DispatcherQueueController](/uwp/api/windows.system.dispatcherqueuecontroller).</span></span>

-   [<span data-ttu-id="17a5c-144">**DispatcherQueueOptions**</span><span class="sxs-lookup"><span data-stu-id="17a5c-144">**DispatcherQueueOptions**</span></span>](/windows/desktop/api/DispatcherQueue/ns-dispatcherqueue-dispatcherqueueoptions)

## <a name="job-object-structures"></a><span data-ttu-id="17a5c-145">Estruturas de objeto de trabalho</span><span class="sxs-lookup"><span data-stu-id="17a5c-145">Job Object Structures</span></span>

<span data-ttu-id="17a5c-146">As seguintes estruturas são usadas com objetos de trabalho:</span><span class="sxs-lookup"><span data-stu-id="17a5c-146">The following structures are used with job objects:</span></span>

-   [<span data-ttu-id="17a5c-147">**\_porta de \_ conclusão da associação do JOBOBJECT \_**</span><span class="sxs-lookup"><span data-stu-id="17a5c-147">**JOBOBJECT\_ASSOCIATE\_COMPLETION\_PORT**</span></span>](/windows/desktop/api/WinNT/ns-winnt-jobobject_associate_completion_port)
-   [<span data-ttu-id="17a5c-148">**informações de contabilidade do JOBOBJECT \_ Basic \_ \_**</span><span class="sxs-lookup"><span data-stu-id="17a5c-148">**JOBOBJECT\_BASIC\_ACCOUNTING\_INFORMATION**</span></span>](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_accounting_information)
-   [<span data-ttu-id="17a5c-149">**\_ \_ informações de contabilidade do JOBOBJECT Basic e \_ Io \_ \_**</span><span class="sxs-lookup"><span data-stu-id="17a5c-149">**JOBOBJECT\_BASIC\_AND\_IO\_ACCOUNTING\_INFORMATION**</span></span>](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_and_io_accounting_information)
-   [<span data-ttu-id="17a5c-150">**\_informações de \_ limite \_ básico do JOBOBJECT**</span><span class="sxs-lookup"><span data-stu-id="17a5c-150">**JOBOBJECT\_BASIC\_LIMIT\_INFORMATION**</span></span>](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_limit_information)
-   [<span data-ttu-id="17a5c-151">**\_lista de \_ ID de processo básica \_ do JOBOBJECT \_**</span><span class="sxs-lookup"><span data-stu-id="17a5c-151">**JOBOBJECT\_BASIC\_PROCESS\_ID\_LIST**</span></span>](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_process_id_list)
-   [<span data-ttu-id="17a5c-152">**\_restrições básicas de \_ interface do usuário do JOBOBJECT \_**</span><span class="sxs-lookup"><span data-stu-id="17a5c-152">**JOBOBJECT\_BASIC\_UI\_RESTRICTIONS**</span></span>](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_ui_restrictions)
-   [<span data-ttu-id="17a5c-153">**JOBOBJECT \_ fim \_ das \_ \_ informações de hora do trabalho \_**</span><span class="sxs-lookup"><span data-stu-id="17a5c-153">**JOBOBJECT\_END\_OF\_JOB\_TIME\_INFORMATION**</span></span>](/windows/desktop/api/WinNT/ns-winnt-jobobject_end_of_job_time_information)
-   [<span data-ttu-id="17a5c-154">**\_informações de \_ limite ESTENDIdo JOBOBJECT \_**</span><span class="sxs-lookup"><span data-stu-id="17a5c-154">**JOBOBJECT\_EXTENDED\_LIMIT\_INFORMATION**</span></span>](/windows/desktop/api/WinNT/ns-winnt-jobobject_extended_limit_information)
-   [<span data-ttu-id="17a5c-155">**\_informações de \_ limite de segurança do JOBOBJECT \_**</span><span class="sxs-lookup"><span data-stu-id="17a5c-155">**JOBOBJECT\_SECURITY\_LIMIT\_INFORMATION**</span></span>](/windows/desktop/api/WinNT/ns-winnt-jobobject_security_limit_information)

## <a name="user-mode-scheduling-structures"></a><span data-ttu-id="17a5c-156">Estruturas de agendamento de User-Mode</span><span class="sxs-lookup"><span data-stu-id="17a5c-156">User-Mode Scheduling Structures</span></span>

<span data-ttu-id="17a5c-157">As seguintes estruturas são usadas com UMS:</span><span class="sxs-lookup"><span data-stu-id="17a5c-157">The following structures are used with UMS:</span></span>

-   [<span data-ttu-id="17a5c-158">**UMS \_ criar \_ atributos de thread \_**</span><span class="sxs-lookup"><span data-stu-id="17a5c-158">**UMS\_CREATE\_THREAD\_ATTRIBUTES**</span></span>](/windows/desktop/api/WinNT/ns-winnt-ums_create_thread_attributes)
-   [<span data-ttu-id="17a5c-159">**\_informações de inicialização do Agendador ums \_ \_**</span><span class="sxs-lookup"><span data-stu-id="17a5c-159">**UMS\_SCHEDULER\_STARTUP\_INFO**</span></span>](/windows/desktop/api/WinBase/ns-winbase-ums_scheduler_startup_info)
-   [<span data-ttu-id="17a5c-160">**\_informações de \_ thread do sistema ums \_**</span><span class="sxs-lookup"><span data-stu-id="17a5c-160">**UMS\_SYSTEM\_THREAD\_INFORMATION**</span></span>](/windows/desktop/api/WinBase/ns-winbase-ums_system_thread_information)

 

 
