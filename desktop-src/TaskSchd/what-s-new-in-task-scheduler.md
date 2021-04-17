---
title: O que há de novo no Agendador de Tarefas
description: Lista de novas funcionalidades introduzidas por diferentes versões do Agendador de Tarefas.
ms.assetid: 43fbbbd2-6e97-4ba5-9474-23c5e2b33612
keywords:
- Agendador de Tarefas Agendador de Tarefas, o que há de novo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5245ab4e681af937924cfbd217095009d80d6a11
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105769390"
---
# <a name="whats-new-in-task-scheduler"></a><span data-ttu-id="4ba95-104">O que há de novo no Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="4ba95-104">What's New in Task Scheduler</span></span>

<span data-ttu-id="4ba95-105">As alterações a seguir resumem o que há de novo em versões diferentes do Agendador de Tarefas.</span><span class="sxs-lookup"><span data-stu-id="4ba95-105">The following changes summarize what is new in different versions of Task Scheduler.</span></span>

## <a name="windows-10-and-windows-server-2016"></a><span data-ttu-id="4ba95-106">Windows 10 (e Windows Server 2016)</span><span class="sxs-lookup"><span data-stu-id="4ba95-106">Windows 10 (and Windows Server 2016)</span></span>

<span data-ttu-id="4ba95-107">As seguintes Agendador de Tarefas alterações são introduzidas no Windows 10.</span><span class="sxs-lookup"><span data-stu-id="4ba95-107">The following Task Scheduler changes are introduced in Windows 10.</span></span>

-   <span data-ttu-id="4ba95-108">Quando a economia de bateria estiver ativada, as tarefas do Windows Agendador de Tarefas serão disparadas somente se a tarefa for:</span><span class="sxs-lookup"><span data-stu-id="4ba95-108">When battery saver is on, Windows Task Scheduler tasks are triggered only if the task is:</span></span>

    -   <span data-ttu-id="4ba95-109">Não definido para **iniciar a tarefa somente se o computador estiver ocioso...** (a tarefa não usa [**IdleSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_idlesettings))</span><span class="sxs-lookup"><span data-stu-id="4ba95-109">Not set to **Start the task only if the computer is idle...** (task doesn't use [**IdleSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_idlesettings))</span></span>
    -   <span data-ttu-id="4ba95-110">Não definido para execução durante a manutenção automática (a tarefa não usa [**MaintenanceSettings**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_maintenancesettings))</span><span class="sxs-lookup"><span data-stu-id="4ba95-110">Not set to run during automatic maintenance (task doesn't use [**MaintenanceSettings**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_maintenancesettings))</span></span>
    -   <span data-ttu-id="4ba95-111">Está definido para ser **executado somente quando o usuário está conectado** (o Task [**LoginType**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_logontype) é um **\_ \_ \_ token interativo de logon de tarefa** ou **\_ \_ grupo de logon de tarefa**)</span><span class="sxs-lookup"><span data-stu-id="4ba95-111">Is set to **Run only when user is logged on** (task [**LogonType**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_logontype) is **TASK\_LOGON\_INTERACTIVE\_TOKEN** or **TASK\_LOGON\_GROUP**)</span></span>

    <span data-ttu-id="4ba95-112">Todos os outros gatilhos serão atrasados até que a economia de bateria esteja desativada.</span><span class="sxs-lookup"><span data-stu-id="4ba95-112">All other triggers are delayed until battery saver is off.</span></span> <span data-ttu-id="4ba95-113">Para obter mais informações sobre como acessar o status de economia de bateria em seu aplicativo, consulte [**\_ \_ status de energia do sistema**](/windows/desktop/api/winbase/ns-winbase-system_power_status).</span><span class="sxs-lookup"><span data-stu-id="4ba95-113">For more information about accessing battery saver status in your application, see [**SYSTEM\_POWER\_STATUS**](/windows/desktop/api/winbase/ns-winbase-system_power_status).</span></span> <span data-ttu-id="4ba95-114">Para obter informações gerais sobre a economia de bateria, consulte [economia de bateria (nas diretrizes de componente de hardware)](/windows-hardware/design/component-guidelines/battery-saver).</span><span class="sxs-lookup"><span data-stu-id="4ba95-114">For general information about battery saver, see [battery saver (in the hardware component guidelines)](/windows-hardware/design/component-guidelines/battery-saver).</span></span>

-   <span data-ttu-id="4ba95-115">Por motivos de segurança, um usuário não administrador não pode exibir nem gerenciar uma tarefa do Windows Agendador de Tarefas que foi criada por outro usuário.</span><span class="sxs-lookup"><span data-stu-id="4ba95-115">For security reasons, a non-administrator user cannot view nor manage a Windows Task Scheduler task that was created by another user.</span></span>

## <a name="windows-8"></a><span data-ttu-id="4ba95-116">Windows 8</span><span class="sxs-lookup"><span data-stu-id="4ba95-116">Windows 8</span></span>

<span data-ttu-id="4ba95-117">As alterações Agendador de Tarefas 2,0 a seguir são introduzidas no Windows 8:</span><span class="sxs-lookup"><span data-stu-id="4ba95-117">The following Task Scheduler 2.0 changes are introduced in Windows 8:</span></span>

-   <span data-ttu-id="4ba95-118">Suporte do PowerShell: os usuários podem gerenciar (criar, excluir, modificar, iniciar explicitamente, parar etc.) Tarefas do Windows Agendador de Tarefas usando o módulo do PowerShell do ScheduledTasks.</span><span class="sxs-lookup"><span data-stu-id="4ba95-118">Powershell support: users can manage (create, delete, modify, explicitly start, stop etc.) Windows Task Scheduler tasks using the ScheduledTasks powershell module.</span></span>
-   <span data-ttu-id="4ba95-119">Senhas gerenciadas: os administradores podem usar o Active Directory contas de senha gerenciada como entidades de tarefa.</span><span class="sxs-lookup"><span data-stu-id="4ba95-119">Managed passwords: administrators can use the Active Directory managed password accounts as task principals.</span></span> <span data-ttu-id="4ba95-120">Essas tarefas não exigem mais uma política de redefinição de senha imposta.</span><span class="sxs-lookup"><span data-stu-id="4ba95-120">These tasks no longer require an enforced password reset policy.</span></span>
-   <span data-ttu-id="4ba95-121">Alterações de API: introduziu duas novas configurações de tarefa com a interface [**ITaskSettings3**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings3) .</span><span class="sxs-lookup"><span data-stu-id="4ba95-121">API changes: Introduced two new task settings with the [**ITaskSettings3**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings3) interface.</span></span>
    -   <span data-ttu-id="4ba95-122">[**MaintenanceSettings**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_maintenancesettings): as tarefas que usam essas configurações são tratadas como um novo tipo de tarefas agendadas que são invocadas durante o tempo de manutenção automática do so, de acordo com a periodicidade e a data limite especificadas.</span><span class="sxs-lookup"><span data-stu-id="4ba95-122">[**MaintenanceSettings**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_maintenancesettings): tasks using these settings are treated as a new type of scheduled tasks that are invoked during OS automatic maintenance time, according to the specified periodicity and deadline.</span></span>
    -   <span data-ttu-id="4ba95-123">[**Volátil**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_volatile): tarefas que são definidas como voláteis são sempre desabilitadas em uma inicialização de sistema operacional e devem ser reabilitadas explicitamente quando necessário.</span><span class="sxs-lookup"><span data-stu-id="4ba95-123">[**Volatile**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_volatile): tasks that are set to be volatile are always disabled on an OS boot and must be explicitly re-enabled back when required.</span></span> <span data-ttu-id="4ba95-124">As tarefas voláteis são utilizadas pelos clusters de failover para garantir que apenas uma instância de tarefa seja agendada em um cluster por vez.</span><span class="sxs-lookup"><span data-stu-id="4ba95-124">Volatile tasks are utilized by the failover clusters to ensure only one task instance is scheduled on a cluster at a time.</span></span>
-   <span data-ttu-id="4ba95-125">O mecanismo de agendamento unificado agora dá suporte aos seguintes recursos:</span><span class="sxs-lookup"><span data-stu-id="4ba95-125">The unified scheduling engine now supports the following features:</span></span>
    -   <span data-ttu-id="4ba95-126">Tipo de logon S4U, por meio do elemento [**Logontype**](taskschedulerschema-logontype-principaltype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="4ba95-126">S4U Logon type, through the [**LogonType**](taskschedulerschema-logontype-principaltype-element.md) element.</span></span>
    -   <span data-ttu-id="4ba95-127">Valores de consulta XPath para gatilhos de evento, por meio do elemento [**ValueQueries**](taskschedulerschema-valuequeries-eventtriggertype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="4ba95-127">XPath query values for event triggers, through the [**ValueQueries**](taskschedulerschema-valuequeries-eventtriggertype-element.md) element.</span></span>
    -   <span data-ttu-id="4ba95-128">Não permita o encerramento de uma tarefa, por meio do elemento [**AllowHardTerminate**](taskschedulerschema-allowhardterminate-settingstype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="4ba95-128">Do not allow task hard terminate, through the [**AllowHardTerminate**](taskschedulerschema-allowhardterminate-settingstype-element.md) element.</span></span>
-   <span data-ttu-id="4ba95-129">Recursos preteridos nesta versão</span><span class="sxs-lookup"><span data-stu-id="4ba95-129">Features deprecated in this release</span></span>
    -   <span data-ttu-id="4ba95-130">Ação: [**sendEmail**](taskschedulerschema-sendemail-actiongroup-element.md) (você pode usar [**IExecAction**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction) com o cmdlet [Send-MailMessage](/powershell/module/microsoft.powershell.utility/send-mailmessage?view=powershell-7&preserve-view=true) do [Windows PowerShell](https://technet.microsoft.com/library/bb978526.aspx)como uma solução alternativa).</span><span class="sxs-lookup"><span data-stu-id="4ba95-130">Action: [**sendEmail**](taskschedulerschema-sendemail-actiongroup-element.md) (you can use [**IExecAction**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction) with the [Windows PowerShell](https://technet.microsoft.com/library/bb978526.aspx)[Send-MailMessage](/powershell/module/microsoft.powershell.utility/send-mailmessage?view=powershell-7&preserve-view=true) cmdlet as a workaround).</span></span>
    -   <span data-ttu-id="4ba95-131">Ação: [**exmessage**](taskschedulerschema-showmessage-actiongroup-element.md).</span><span class="sxs-lookup"><span data-stu-id="4ba95-131">Action: [**showMessage**](taskschedulerschema-showmessage-actiongroup-element.md).</span></span>
    -   <span data-ttu-id="4ba95-132">AT.exe o utilitário cmdline</span><span class="sxs-lookup"><span data-stu-id="4ba95-132">AT.exe cmdline utility</span></span>

## <a name="windows-7"></a><span data-ttu-id="4ba95-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4ba95-133">Windows 7</span></span>

<span data-ttu-id="4ba95-134">As seguintes Agendador de Tarefas 2,0 alterações são introduzidas no Windows 7:</span><span class="sxs-lookup"><span data-stu-id="4ba95-134">The following Task Scheduler 2.0 changes are introduced in Windows 7:</span></span>

-   <span data-ttu-id="4ba95-135">Usando o mecanismo de agendamento unificado fornecido pelo sistema operacional subjacente.</span><span class="sxs-lookup"><span data-stu-id="4ba95-135">Using the unified scheduling engine provided by the underlying operating system.</span></span>
-   <span data-ttu-id="4ba95-136">Capacidade de rejeitar tarefas iniciais em sessões do trilho (integradas ao local) de aplicativos remotos.</span><span class="sxs-lookup"><span data-stu-id="4ba95-136">Ability to reject starting tasks in Remote Applications Integrated Locally (RAIL) sessions.</span></span>
-   <span data-ttu-id="4ba95-137">Proteção de segurança de tarefa (somente para tarefas em execução como "serviço de rede" ou "serviço LOCAL"):</span><span class="sxs-lookup"><span data-stu-id="4ba95-137">Task security hardening (for tasks running as "NETWORK SERVICE" or "LOCAL SERVICE" only):</span></span>

    -   <span data-ttu-id="4ba95-138">Capacidade de atribuir um tipo de SID (identificador de segurança) de token de processo (por exemplo, irrestrito ou nenhum) a uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="4ba95-138">Ability to assign a process token security identifier (SID) type (for example, unrestricted or none) to a task.</span></span>
    -   <span data-ttu-id="4ba95-139">Permitir que os desenvolvedores de tarefas solicitem o conjunto exato de privilégios exigidos por sua tarefa.</span><span class="sxs-lookup"><span data-stu-id="4ba95-139">Allow task developers to request the exact set of privileges that their task requires.</span></span>

-   <span data-ttu-id="4ba95-140">Alterações de API:</span><span class="sxs-lookup"><span data-stu-id="4ba95-140">API changes:</span></span>

    -   <span data-ttu-id="4ba95-141">Suporte à proteção de segurança de tarefas: o novo recurso de proteção de segurança de tarefas é introduzido com a nova interface IPrincipal2.</span><span class="sxs-lookup"><span data-stu-id="4ba95-141">Task security hardening support: new task security hardening feature is introduced with new IPrincipal2 interface.</span></span>
    -   <span data-ttu-id="4ba95-142">Introduziu duas novas configurações de tarefa com a nova interface ITaskSettings2.</span><span class="sxs-lookup"><span data-stu-id="4ba95-142">Introduced two new task settings with the new ITaskSettings2 interface.</span></span>

        -   <span data-ttu-id="4ba95-143">DisallowStartOnRemoteAppSession: a nova configuração DisallowStartOnRemoteAppSession pode rejeitar uma tarefa de início se disparada em sessões do [trilho (integradas localmente) de aplicativos remotos](/openspecs/windows_protocols/MS-WINPROTLP/df36f95e-6a6b-48d6-a3ae-35a17674f546) .</span><span class="sxs-lookup"><span data-stu-id="4ba95-143">DisallowStartOnRemoteAppSession: The new DisallowStartOnRemoteAppSession setting can reject a task start if triggered in [Remote Applications Integrated Locally (RAIL)](/openspecs/windows_protocols/MS-WINPROTLP/df36f95e-6a6b-48d6-a3ae-35a17674f546) sessions.</span></span>
        -   <span data-ttu-id="4ba95-144">UseUnifiedSchedulingEngine: usar a configuração UseUnifiedSchedulingEngine fornece um comportamento coeso para tarefas e serviços do Windows, pois ele está sendo gerenciado de maneira uniforme por um mecanismo de agendamento comum em todo o sistema.</span><span class="sxs-lookup"><span data-stu-id="4ba95-144">UseUnifiedSchedulingEngine: Using the UseUnifiedSchedulingEngine setting provides a cohesive behavior for Windows Tasks and Services because it is being managed in a uniform manner by a common system-wide scheduling engine.</span></span> <span data-ttu-id="4ba95-145">Embora o uso de um mecanismo unificado seja recomendado, ele não oferece suporte a alguns dos recursos de Agendador de Tarefas.</span><span class="sxs-lookup"><span data-stu-id="4ba95-145">Although using a unified engine is recommended, it does not support some of the Task Scheduler features.</span></span> <span data-ttu-id="4ba95-146">Se a combinação de propriedades não permitir a execução da tarefa em um mecanismo unificado, o registro de tal será rejeitado.</span><span class="sxs-lookup"><span data-stu-id="4ba95-146">If the combination of properties will not allow running of the task under a unified engine, the registration of such will be rejected.</span></span>
        -   <span data-ttu-id="4ba95-147">Os recursos de tarefa que não são suportados pelo mecanismo de agendamento unificado incluem:</span><span class="sxs-lookup"><span data-stu-id="4ba95-147">The task features that are not supported by the unified scheduling engine include:</span></span>

            -   <span data-ttu-id="4ba95-148">Tipos de logon:</span><span class="sxs-lookup"><span data-stu-id="4ba95-148">Logon types:</span></span>

                -   [<span data-ttu-id="4ba95-149">\_ \_ \_ token \_ ou senha de logon \_ interativo da tarefa</span><span class="sxs-lookup"><span data-stu-id="4ba95-149">TASK\_LOGON\_INTERACTIVE\_TOKEN\_OR\_PASSWORD</span></span>](./taskschedulerschema-logontype-principaltype-element.md)

            -   <span data-ttu-id="4ba95-150">Política de várias instâncias:</span><span class="sxs-lookup"><span data-stu-id="4ba95-150">Multiple instance policy:</span></span>

                -   [<span data-ttu-id="4ba95-151">**as \_ instâncias de tarefa \_ param \_ existentes**</span><span class="sxs-lookup"><span data-stu-id="4ba95-151">**TASK\_INSTANCES\_STOP\_EXISTING**</span></span>](taskschedulerschema-multipleinstancespolicy-settingstype-element.md)

            -   <span data-ttu-id="4ba95-152">Ações:</span><span class="sxs-lookup"><span data-stu-id="4ba95-152">Actions:</span></span>

                -   [<span data-ttu-id="4ba95-153">Enviar email</span><span class="sxs-lookup"><span data-stu-id="4ba95-153">Send email</span></span>](./taskschedulerschema-sendemail-actiongroup-element.md)
                -   [<span data-ttu-id="4ba95-154">Exibir mensagem</span><span class="sxs-lookup"><span data-stu-id="4ba95-154">Display message</span></span>](./taskschedulerschema-showmessage-actiongroup-element.md)

            -   <span data-ttu-id="4ba95-155">Configurações:</span><span class="sxs-lookup"><span data-stu-id="4ba95-155">Settings:</span></span>

                -   [<span data-ttu-id="4ba95-156">Configurações de rede de tarefas</span><span class="sxs-lookup"><span data-stu-id="4ba95-156">Task network settings</span></span>](./taskschedulerschema-networksettings-settingstype-element.md)
                -   [<span data-ttu-id="4ba95-157">Não permitir o encerramento forçado da tarefa</span><span class="sxs-lookup"><span data-stu-id="4ba95-157">Do not allow task hard terminate</span></span>](./taskschedulerschema-allowhardterminate-settingstype-element.md)

            -   <span data-ttu-id="4ba95-158">Gatilhos:</span><span class="sxs-lookup"><span data-stu-id="4ba95-158">Triggers:</span></span>

                -   [<span data-ttu-id="4ba95-159">Limite de tempo de execução do gatilho</span><span class="sxs-lookup"><span data-stu-id="4ba95-159">Trigger execution time limit</span></span>](./taskschedulerschema-executiontimelimit-triggerbasetype-element.md)
                -   [<span data-ttu-id="4ba95-160">Padrões de repetição para gatilhos de calendário</span><span class="sxs-lookup"><span data-stu-id="4ba95-160">Repetition patterns for calendar triggers</span></span>]( ./taskschedulerschema-repetition-triggerbasetype-element.md)
                -   [<span data-ttu-id="4ba95-161">Valores de consulta XPath para gatilhos de eventos</span><span class="sxs-lookup"><span data-stu-id="4ba95-161">XPath query values for event triggers</span></span>]( ./taskschedulerschema-valuequeries-eventtriggertype-element.md)
                -   <span data-ttu-id="4ba95-162">Tipos de gatilhos [mensais](./taskschedulerschema-schedulebymonth-calendartriggertype-element.md) e [mensais do dia da semana](./taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md)</span><span class="sxs-lookup"><span data-stu-id="4ba95-162">[Monthly](./taskschedulerschema-schedulebymonth-calendartriggertype-element.md) and [Monthly day-of-week](./taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) trigger types</span></span>

## <a name="windows-vista"></a><span data-ttu-id="4ba95-163">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4ba95-163">Windows Vista</span></span>

<span data-ttu-id="4ba95-164">A API Agendador de Tarefas 2,0 deve ser usada no desenvolvimento de aplicativos que usam o serviço Agendador de Tarefas no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="4ba95-164">The Task Scheduler 2.0 API should be used in developing applications that use the Task Scheduler service on Windows Vista.</span></span> <span data-ttu-id="4ba95-165">Para obter mais informações, consulte [Agendador de tarefas referência](task-scheduler-reference.md) e [usando o Agendador de tarefas](using-the-task-scheduler.md).</span><span class="sxs-lookup"><span data-stu-id="4ba95-165">For more information, see [Task Scheduler Reference](task-scheduler-reference.md) and [Using the Task Scheduler](using-the-task-scheduler.md).</span></span>

## <a name="windows-2000-windows-xp-and-windows-server-2003"></a><span data-ttu-id="4ba95-166">Windows 2000, Windows XP e Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4ba95-166">Windows 2000, Windows XP, and Windows Server 2003</span></span>

<span data-ttu-id="4ba95-167">A API Agendador de Tarefas 2,0 não está disponível.</span><span class="sxs-lookup"><span data-stu-id="4ba95-167">The Task Scheduler 2.0 API is not available.</span></span> <span data-ttu-id="4ba95-168">Use Agendador de Tarefas 1,0.</span><span class="sxs-lookup"><span data-stu-id="4ba95-168">Use Task Scheduler 1.0.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4ba95-169">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4ba95-169">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ba95-170">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="4ba95-170">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="4ba95-171">Sobre o Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="4ba95-171">About The Task Scheduler</span></span>](about-the-task-scheduler.md)
</dt> </dl>

 

 
